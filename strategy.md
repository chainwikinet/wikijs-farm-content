---
title: Harvest Finance Yield Farming Strategies
description: how the Total Value Locked in Harvest creates revenue for FARM holders
published: true
date: 2020-09-06T01:42:34.778Z
tags: 
editor: markdown
---

# Active Yield Farming Strategies

Harvest Finance is launching with one active yield farming strategy. More strategies will be added soon after user feedback is incorporated into the Harvest Finance site.

95% of the yield farming revenue is returned to users who provide capital. The remaining 5% of the yield farming revenue is distributed to users who [stake FARM in the Profit Sharing contract][farm-stakedrop]. The Harvest Finance team does not charge fees for withdrawing or depositing assets and does not claim a fee on the yield farming revenue.

## Farming CRV

The first yield farming strategy active on Harvest Finance farms CRV, the [Curve Finance DAO token][crv].

> You do not receive CRV directly. Instead, the farmed CRV is sold to return more stablecoins to you when you withdraw.
{.is-info}

| | |
|------------------|-|
| **Asset Farmed**        | CRV, Curve Finance DAO token  |
| **Assets Used**         | DAI, USDC, USDT               |
| **Basic Strategy**      | CRV is farmed and sold for stablecoins |
| **How To Participate**  | [deposit DAI, USDC, USDT][hf] to receive fDAI, fUSDC, fUSDT |
| **Yield Payout**        | Successful farming makes the fDAI, fUSDC, and fUSDT redeemable for a growing number of DAI, USDC, and USDT |
| **FARM Incentives**      | [The fDAI, fUSDC, and fUSDT can be deposited to earn a stakedrop of FARM][farm-stakedrop] |
| **Vault Contract**      | [VaultYCRV][vaultycrv] |
| **Strategy Contract**   | [CRVStrategyYCRVMainnet][crvstrategy] |
| **Example Harvest TX**  | [doHardWork][harvest] |

![harvestcrvstrategy.png](/harvestcrvstrategy.png)


[farm-stakedrop]: https://harvest.finance/earn
[harvest]: https://etherscan.io/tx/0xf69262029ce30403101cda38d110ae897a6c23b4b8748d10a9a3514c012c365d
[crvstrategy]: https://etherscan.io/address/0xcf5f83f8fe0ab0f9e9c1db07e6606dd598b2bbf5
[vaultycrv]: https://etherscan.io/address/0xf2b223eb3d2b382ead8d85f3c1b7ef87c1d35f3a
[crv]: https://www.coingecko.com/en/coins/curve-dao-token
[hf]: https://harvest.finance