---
title: GRAIN
description: GRAIN
published: true
date: 2021-02-17T20:42:18.140Z
tags: grain flash loan attack
editor: markdown
dateCreated: 2021-02-12T17:48:58.601Z
---

# The creation of GRAIN:
On October 26th, 2020 at 02:53:31 AM +UTC www.harvest.finance was attacked by an exploit called a flash loan attack. An attacker executed a theft of funds from the USDC and USDT vaults of Harvest Finance. The attacker exploited an arbitrage and impermanent loss that influences the value of individual assets inside the Y pool of Curve.fi, which is where the funds of Harvest’s vaults were invested. The attacker transferred some funds back to the Harvest deployer within minutes of the exploit happening in transaction: 0x25119cd54a4562aa427d9770af383512f9cb5e8e4d17232ad96b69dc293a3510. This amount was 1,761,898.396474 USDC and 718,914.048541 USDT.

Immediately following the attack, Harvest Finance acted and withdrew all the funds from the shared pools. This included DAI, USDC, USDT, TUSD as well as WBTC and renBTC. The funds are currently present in the vaults and cannot suffer from further market manipulation. The attack did not involve DAI, TUSD, WBTC and renBTC, and the depositors in these vaults were not affected. Furthermore, Harvest Finance rapidly evaluated the attack and reconstructed its process so they could prevent it from happening again. 

Once the developers deconstructed the attack, they pointed out that the collateral damage was mostly on the thousands of small farmers affected. They admitted their engineering mistake and that the attacker had proven their point. They reminded the exploiter that the attack was going to be perceived poorly for extrapolating this liquidity farming model to the wider community and was detrimental to the DeFi space as a whole. 

Once the attack had been reverse engineered by the Harvest developers and some funds returned, the governance deliberated [https://snapshot.page/#/farm/proposal/QmYF62qGaqyHAXt88Hmxise6CFaSWxnTmi5VedZ3VX8Zy2] and the Harvest team decided to enact a remediation plan in the form of GRAIN. Individuals affected by the attack were able to recover their balances through a blend of USDC/USDT reparations and the GRAIN token. Based on the snapshot taken one block before the attack, the team calculated the claim amount for each user using the logic here: https://github.com/harvest-finance/snapshot. GRAIN tokens were assigned in a pro-rata manner based on both their afflicted deposits and a proportionate amount of returned funds. This was done via the GRAIN claims portal on the Harvest Finance website, a UI that the devs thought would be easy to use and straightforward. For example: 99.5945 USD would return 5.2507 USDC + 2.1424 USDT + 92.2014 GRAIN to the affected user. This portal went live on December 7, 2020 and users whose balances were affected by the drawdown due to the economic exploit were able to receive their claim for USDT, USDC and the GRAIN token.

## GRAIN tokenomics:
GRAIN is a buyback token for USDC/USDT depositors that feeds a percentage of total weekly emissions to reparations pools. GRAIN was issued such that 1 GRAIN = $1 of harvest debt. Once harvest owns the tokens, they can be burned, independent of the price they were bought at. Harvest will continue buying back GRAIN at a price of no more than $1 until they own all of it, at which point the debt will have been repaid.

GRAIN was voted in by the community shortly after the attack. The community voted for up to 0.5% of total emissions to go to GRAIN buyback and Uniswap liquidity. In the spirit of the farming cooperative, the dev and ops funds were used to contribute towards FARM used for the GRAIN buyback. 10% of the buyback amount came from the ops fund, and 20% came from the devs. The remaining 70% will come from farming incentive emissions.

The community also voted for incentivizing GRAIN/FARM as the base pair. Incentivizing GRAIN/FARM would be beneficial because it would create a FARM supply sink, while at the same time giving GRAIN holders who also own FARM the ability to get more FARM emissions by staking in Uniswap.

This gives a market value to GRAIN, by using some emissions to incentivize a liquid market. After much discussion, it was decided that creating a liquid market is the preferred option, because it allows GRAIN holders to trade with buyers that are interested in the APY of GRAIN farming instead of only having the option to hold for many months or years.

In addition to providing incentives for the FARM:GRAIN pair, Harvest uses funds from the strategic reserve for strategic GRAIN buybacks as needed to buffer price volatility. The following amounts have been saved up for this purpose:
Week 12: 1,798.98 FARM
Week 13: 658.95 FARM
Week 14: 465.3988850 FARM

## Claiming USDC and/or USDT:
As of Monday, December 7th 2020, those affected by the exploit can claim their pro-rata share of the $2.4m and GRAIN through the following steps:
Go to https://claim.harvest.finance
Connect your Metamask.
Press ‘Claim USDC’ and ‘Claim USDT’ and follow Metamask to complete the transaction

## Claiming GRAIN:
As of the same date affected users can claim their pro-rata share of the GRAIN token through the following steps:
Go to https://claim.harvest.finance
Connect your Metamask.
Press ‘Claim GRAIN’ and follow the steps.
Add GRAIN to Metamask by clicking the link given on the page. You will then be able to see GRAIN in your wallet.

## Trading GRAIN:
An incentivized Uniswap pool was created with GRAIN/FARM as the base pair. The incentivized Uniswap pool was announced on Harvest's Discord and Twitter on Monday, December 7th 2020. The pool was kick started using GRAIN bought by the operations fund. Claims began around Monday, 17:00 UTC and liquidity incentivization began 8 hours later, to make sure that there was sufficient GRAIN available for the operations fund to buy and deposit into the Uniswap pool for an orderly market to form.








