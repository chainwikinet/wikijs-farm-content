---
title: APY Calculation
description: 
published: true
date: 2020-11-23T17:12:04.420Z
tags: apy
editor: markdown
dateCreated: 2020-11-23T17:12:04.420Z
---

# **APY computation formulas**

Below is the description of how the displayed APYs currently computed. All computations are performed on our back-end APY and are cached for the duration of one hour to reduce the server load and prevent from the web3 provider's throttling.

**FARM APR/APY for pools**

`APR = farm_token_price * pool.rewardRate (per second) * 604800 seconds * 52 weeks / f_token_price / pool.totalSupply (of f-tokens)`.

`APY`:
1. For the auto-staking profit sharing pool: `APY` = `APR` is compounded daily.
2. For a regular reward pool (e.g., DAI, SUSHI, etc.): `APY` = `APR` is compounded weekly.

`pool.rewardRate` is updated whenever a pool is notified with additional FARM using the `pool.notifyRewardAmount(...)` method.
For regular pools, it happens once per week (on the emissions day).
For the profit-sharing pool, it happens daily: the weekly emissions are split into 7 equal portions, and the pool is notified daily with each
portion. In addition, the profit-sharing pool is notified on every `doHardWork` (whenever there is some FARM bought).

Upon each notification, `pool.rewardRate` is calculated using the formula:
`(newly notified FARM + remaining prior non-distributed FARM) / pool_duration`, where `pool_duration` is `1 day` for the profit-sharing pool (for the exact code, look for `notifyRewardAmount(...)` of [the profit-sharing pool](https://etherscan.io/address/0x8f5adC58b32D4e5Ca02EAC0E293D35855999436C#code))
This leads to some fluctuations of `rewardRate` for the profit sharing pool, because on every `notifyRewardAmount` call,
`rewardRate` is recalculated using the duration of one day and the to-be-distributed reward amount.

**Farming APYs for Curve vaults**

`APR` is calculated using the formula taken from `curve.fi`. It takes into account the lending APY, the price of the CRV token, the reward rate defined at the Curve controller level, the weight of the corresponding Gauge pool, and the strategy's so-called "working supply" (the invested amount). The result is multiplied by `0.7` (since `30%` of the profits are shared) and compounded daily (because the underlying that is traded for is being re-invested on every `doHardWork` call).

**Farming APYs for Sushi vaults**

`APR` is calculated using the formula taken from `sushiswapclassic.org`. The only difference is that we removed the `.times(3)` from the formula because the Sushi website displays a three-times-higher APY due to the promised vesting. Like with other vaults, we multiply by `0.7` and compound the computation result daily.

**Farming APYs for Compound vaults**

`APR` is calculated using the Compound lending rate for the given token and the COMP distribution rate. Both are taken from Compound's API. The COMP distribution is multiplied by `0.7` because `30%` of the profits are shared.

**Farming APYs for other vaults**

In cases when it is impossible or impractical to write a formula or an API for the APY computation (e.g., for DEGO), we take the value from the original website, multiply it by `0.7` to account for profit-sharing and hard-code it in our API. We update the hard-coded value periodically (usually, daily).
