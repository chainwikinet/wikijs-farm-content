---
title: Harvest Security
description: testing and auditing the Harvest Finance contracts
published: true
date: 2020-10-12T21:20:15.219Z
tags: 
editor: markdown
dateCreated: 2020-09-06T07:52:56.974Z
---

# Contract Tests

Harvest's talented tractor engineers have created one of the best test suites, learn more [here](https://github.com/harvest-finance/harvest/tree/master/test)

The contracts also have extensive comments to understand what each part of the code is doing.

# Contract Audits

To keep the crops secure, you must invest in fences. The Harvest operations budget (10% of supply) will be used to ensure that Harvest farming strategies are audited and secure.


## PeckShield Audit

> We acquired an audit from PeckShield  which should assure our farmers that their crops are safe and bread for the people will be produced, no matter what the future brings. The main issue pointed out by PeckShield is the privileged role of our 0xf00d deployer address. Based on the discussion with our community, we have implemented timelock mechanisms that provide the farmers with an opportunity to leave the farm if they disagree with the deployer's actions before these actions are executed. An additional issue related to CRVStrategyStable's depositArbCheck() was pointed out by our wonderful community and was already fixed before the report by PeckShield was completed. Other non-informational issues do not affect the system, or are explicit design choices and decentralization features made by our team. We would like to thank PeckShield for their hard work on this audit and keeping our farmers safe.
> 
> [PeckShield Audit](/en/https://github.com/harvest-finance/harvest/blob/master/audits/PeckShield-Harvest.pdf)



> On September 7th 2020, PeckShield indicated that no serious business logic issues had been found in a preliminary review:
 [PeckShield Inc. @peckshield (2020-09-07)](https://twitter.com/peckshield/status/1303012731197382656
)
Last few days PeckShield has done a sanity check of Harvest Finance smart contracts, so far no serious business logic issue was found.  In the next several weeks, we will conduct a full security audit of the smart contracts. [@harvest_finance](https://twitter.com/harvest_finance) #DeFiFarming


## Haechi Labs

> We acquired an audit from Haechi which should assure our farmers that their crops are safe and bread for the people will be produced, no matter what the future brings. The audit highlighted one issue classified as major (initially pointed out by the community, thus it is already fixed), and 5 additional minor issues, 4 of which are in fact decentralization features and design choices that we actively made for our platform. The one remaining minor issue was fixed as well. We would like to thank Haechi for their hard work on this audit and keeping our farmers safe.
> 
>  [Haechi Labs Audit](/en/https://github.com/harvest-finance/harvest/blob/master/audits/Haechi-Harvest.pdf)
 


>  Preliminary results from 14th of September 2020: Thanks to Harvest.Finance developer’s hard work, we could not identify any serious bug in smart contracts. We were able to find that Harvest.Finance development team had put a lot of effort into testing the smart contracts. Including external contract tests which were very helpful while reviewing the contracts.
As a result, what we could find was minor issues including missing interface files which do not affect the security of the business logic. [LINK to the original post](https://medium.com/haechi-audit/harvest-finance-security-review-64782c98d2ae)

[haechi.io](https://haechi.io) is a Korean security company that has performed audits for LG, Samsung, Carry Protocol, and the Ethereum Foundation.


## Certik Audit

An audit from [Certik](https://twitter.com/certik_io) has also been commissioned. Certik is expected to complete in Week7.

# Incident Retrospectives

## fWETH Withdraw Failure Sept 18 2020

> This summary was prepared by user `Silage Pete` and has not been reviewed for accuracy or completeness by the Harvest team.
{.is-info}


At around 06:00 UTC on Friday September 18th 2020, users in the Harvest Finance Discord chat began reporting problems with fWETH withdrawals.

At the time of the incident, the fWETH vault was using a farming strategy that earned interest for depositors by deposited the underlying WETH onto the CREAM platform for lending. CREAM lending is based on a fork of the Compound lending codebase.

When an fWETH withdrawal is processed, the underlying WETH should be removed from CREAM and returned to the claimant, and the interest-bearing fWETH deposit receipt should be burned. In the faulty transactions, the deposit receipt was burned, but only some or even none of the requested WETH was withdrawn from CREAM and returned to the user:

- https://etherscan.io/tx/0x8231e0136b47526d9dd55367767ea0bbda174758b1ce3b8f07ac5cd207c1a4f9
- https://etherscan.io/tx/0xe77f253d3035e60fc6629e7d553e8b5a1d0ed2870d38666d4d27c9818d940d69

CREAM, like Compound, cannot always guarantee that withdrawals of any size can be honored at any time. As a result, large withdrawals may result in partial or no return of funds and the error message `TOKEN_INSUFFICIENT_CASH`. Due to an oversight, the Harvest strategy contract failed to check for this error and would burn the user's fWETH even if only some or none of the requested WETH was returned.

When the issue was understood, Harvest community wiki managers `BIBI CAT`, `Silage Pete`, and several other Harvest Discord moderators and helpful users notified the Harvest development team of the problem and alerted everyone in Discord that they should not attempt any more WETH withdrawals until the issue was fixed. Notices to avoid withdrawals were placed in Discord and the wiki.

At 07:00 UTC, around 1 hour after the incident was reported, contributor `Byron McKeeby` submitted [a pull request to the WETH strategy repository](https://github.com/harvest-finance/harvest/pull/4/files) attempting to fix this bug. This PR would not recover the WETH for those who had failed to withdraw, but it proposed an approach for avoiding the failed withdrawal problem in future strategy deployments.

Approximately 5% of the fWETH supply held by 11 owners attempted to withdraw and was affected by this bug. When a withdrawal failed, ownership of the WETH in CREAM that failed to be withdrawn was transferred to the remaining shareholders in the fWETH pool and causing the fWETH share price to increase.

![fweth-shareprice.png](/fweth-shareprice.png)


Around 14:00 UTC, Discord administrator and development team member `Bread for the People` posted in Discord to announce that the problem was being worked on:

> Withdrawals for WETH are currently disabled due to a lack of ETH inside Cream lending. We are working with CREAM and are actively working to resolve the issue. Safe withdrawals of WETH will be enabled soon. We would like to take responsibility and to thank Andre Cronje and the CREAM team for actively assisting with the fix.

Around 16:00 UTC, `Bread for the People` announced that the Harvest and CREAM teams had a plan to restore the funds:

> :rice_scene: Working together with the CREAM team, we have a plan to restore peace and harmony to the WETH Farm. :rice_scene: :man_farmer: Users do not need to do anything, the strategy will be updated with the fix. After that, all values will be double-checked, and then withdrawals will be re-enabled.

Around 17:00 UTC, `Bread for the People` announced that the WETH had been recovered:

> Update: crWETH from the CREAM strategy has been successfully redeemed to WETH. 
:man_farmer: Users do not need to do anything, all values will be double-checked once the strategy is updated with the fix, and then withdrawals will be re-enabled.

Around 19:00 UTC, `Bread for the People` announced that the incident was resolved:

> :rice_scene: Peace and harmony has been restored to the WETH Farm. :rice_scene: 
:white_check_mark: fWETH balances have been restored. 
:white_check_mark: Withdrawals have been re-enabled.
:white_check_mark: All WETH Farm participants are in profit.
:man_farmer: Thanks to the excellent Cream team and the prolific Andre Cronje for helping out.

Recovery transactions:
- [all WETH is redeemed from CREAM and deposited in the fWETH contract](https://etherscan.io/tx/0x519acf0a0a71f944e2ae573740d399b77d60220e7c8e4b22742c2a76f2cad69a)
- [fWETH strategy is changed to a recovery strategy contract](https://etherscan.io/tx/0x4482df10258c414853155be260ce4626a645779aa9b600deead35eb621395675)
- [all WETH is moved from fWETH to an intermediate recovery strategy contract](https://etherscan.io/address/0x26d3e02999beffaeb07af3a94438769df0ee4150#tokentxns)
- [4,295 WETH from failed withdrawals are pooled for return to their 11 owners](https://etherscan.io/address/0x23b6c1f600111895cc4536d070eb35660500d670#tokentxns)
- [85,271 WETH is returned to the fWETH contract and fWETH strategy switched to safewithdrawal contract](https://etherscan.io/tx/0x706068b557f9b61a3780f357daf0f6b710d80db86fec72aaae003b4a8110af1d)






