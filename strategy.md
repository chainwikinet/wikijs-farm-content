---
title: Harvest Finance Yield Farming Strategies
description: how the Total Value Locked in Harvest creates revenue for FARM holders
published: true
date: 2020-10-15T21:38:05.036Z
tags: 
editor: markdown
dateCreated: 2020-09-04T07:47:54.724Z
---

 > Grow Harvest. [Contribute to this wiki!](/contribute)
 {.is-success}


# New Strategy Proposals

## Curve hBTC Pool (wBTC, hBTC)

Curve launched a new hBTC pool with hBTC, wBTC pair: https://www.curve.fi/hbtc

CRV stakedrop weight for this pool is zero, so this is not a yield farming opportunity yet.



# Active Yield Farming Strategies

Harvest Finance launched on September 1st. New farming strategies are constantly evaluated for addition to Harvest.

- **2020-09-01** Harvest Finance launches with yCRV CRV farming support for DAI, USDC, USDT
- **2020-09-05** Within 16 hours of Swerve launch, Harvest adds SWRV farming support for DAI, USDC, USDT
- **2020-09-08** Harvest adds CurveRenWBTC CRV farming support for WBTC, renBTC, crvRenWBTC
- **2020-09-17** Harvest adds UNI farming support for ETH-DAI, ETH-USDC, ETH-USDT, ETH-WBTC.
- **2020-10-13** Harvest adds SUSHI farming support for WBTC-TBTC.

As of September 8th, 70% of the yield farming revenue is returned to users who provide capital. The remaining 30% of the yield farming revenue is distributed to users who [stake FARM in the Profit Sharing contract][farm-stakedrop]. The Harvest Finance team does not charge fees for withdrawing or depositing assets and does not claim a fee on the yield farming revenue.

## Farming CRV with BTC

This strategy farms CRV, the [Curve Finance DAO token][crv].

> You do not receive CRV directly. Instead, the farmed CRV is sold to return more BTC to you when you withdraw.
{.is-info}

| | |
|------------------|-|
| **Asset Farmed**        | CRV, Curve Finance DAO token  |
| **Assets Used**         | wBTC, renBTC, crvRenWBTC      |
| **Basic Strategy**      | CRV is farmed and sold for stablecoins |
| **How To Participate**  | [deposit a supported asset][hf] |
| **Yield Payout**        | Successful farming makes your deposit redeemable for a growing amount of the deposited asset |
| **FARM Incentives**      | [fWBTC, frenBTC, and fcrvRenWBTC deposit receipts can be deposited to earn a stakedrop of FARM][farm-stakedrop] |
| **Vault Contract**      | [fWBTC][es-fwbtc], [frenBTC][es-frenbtc], [fcrvRenWBTC][es-fcrvrenwbtc] |
| **Strategy Contract**   | [CRVStrategyWBTCMainnet][es-strat-fwbtc-v1], [CRVStrategyRENBTCMainnet][es-strat-renbtc-v1], [CRVStrategyWRenBTCMixMainnet][es-strat-crvrenwbtc-v1] |
| **Example Harvest TX**  | [doHardWork](https://etherscan.io/tx/0x01dfcfd6dd1ca0db042fb516767c3725e06cc1db28a40781314c72d897351ba8) |

[es-strat-fwbtc-v1]: https://etherscan.io/address/0xe7048e7186cb6f12c566a6c8a818d9d41da6df19#code
[es-strat-renbtc-v1]: https://etherscan.io/address/0x2eadfb06f9d890eba80e999eaba2d445bc70f006#code
[es-strat-crvrenwbtc-v1]: https://etherscan.io/address/0xaf2d2e5c5af90c782c008b5b287f20334eeb308e#code

## Farming CRV with Stablecoins

This strategy farms CRV, the [Curve Finance DAO token][crv].

> You do not receive CRV directly. Instead, the farmed CRV is sold to return more stablecoins to you when you withdraw.
{.is-info}

| | |
|------------------|-|
| **Asset Farmed**        | CRV, Curve Finance DAO token  |
| **Assets Used**         | DAI, USDC, USDT               |
| **Basic Strategy**      | CRV is farmed and sold for stablecoins |
| **How To Participate**  | [deposit DAI, USDC, USDT, TUSD][hf] to receive fDAI, fUSDC, fUSDT |
| **Yield Payout**        | Successful farming makes the fDAI, fUSDC, and fUSDT redeemable for a growing number of DAI, USDC, and USDT |
| **FARM Incentives**      | [The fDAI, fUSDC, fUSDT, and fTUSD can be deposited to earn a stakedrop of FARM][farm-stakedrop] |
| **Vault Contract**      | [VaultYCRV][es-vaultycrv], [fDAI][es-fdai], [fUSDC][es-fusdc], [fUSDT][es-fusdt], [fTUSD Vault Proxy Address][es-ftusd-proxy] ([Current TUSD Vault implementation][es-ftusd]) |
| **Strategy Contract**   | [CRVStrategyYCRVMainnet][es-strat-crvstable-v2], [DAI Strategy][es-strat-crystable-dai], [USDC Strategy][es-strat-crystable-usdc], [USDT Strategy][es-strat-crystable-usdt], [TUSD Strategy][es-strat-crystable-tusd] |
| **Example Harvest TX**  | [doHardWork][es-crvstable-harvest] |

> Note: This strategy is using a two-tiered vault. All stablecoins deposited are combined into a single pool, thus farming yields are equal for all three pools.
{.is-info}

[es-strat-crvstable-v2]: https://etherscan.io/address/0x2427da81376a0c0a0c654089a951887242d67c92
[es-strat-crystable-dai]: https://etherscan.io/address/0x810b83fc33e6f5da9be9ae5dd0f918338e980938#code
[es-strat-crystable-usdc]: https://etherscan.io/address/0x68e6aa634b22dd28c4c22cc9fc4c1900e8bea90b#code
[es-strat-crystable-usdt]: https://etherscan.io/address/0x03292bdfE36591F70575C77847d7f004FFd0966A
[es-strat-crystable-tusd]: https://etherscan.io/address/0x9d356fda8437f7c7b6a4bc84466a98a4a6eec462

[es-crvstable-harvest]: https://etherscan.io/tx/0x0b8f78bb74fc5e1451af4c6b15dd48b263fc5b29006a3555bd5942313235d22a

## Farming UNI With LP Tokens
This strategy farms UNI, the [Uniswap Token][uni].

> You do not receive UNI directly. Instead, the farmed UNI is sold to return more lp tokens of the type deposited when you withdraw.
{.is-info}

| | |
|------------------|-|
| **Asset Farmed**        | UNI, Uniswap token  |
| **Assets Used**         | ETH-DAI, ETH-USDC, ETH-USDT, ETH-WBTC              |
| **Basic Strategy**      | UNI is automatically farmed and sold for more LP tokens. Harvest pays your gas fees to grow the underlying LP. 30% of rewards are kept for FARM profit sharing. |
| **How To Participate**  | [deposit LP Tokens][hf] to receive fUNI-V2 |
| **Yield Payout**        | Successful farming makes the fUNISWAP_LP redeemable for a growing number of LP tokens. |
| **FARM Incentives**     | [The fUNISWAP_LP can be deposited to earn a stakedrop of FARM][farm-stakedrop] |
| **Vault Contract**      | fUNI-V2 [fWBTC_WETH_LP][es-fwbtc-weth-LP] ([implementation][es-fwbtc-weth-LP-proxy]), [fUSDC_WETH_LP][es-fusdc-weth-LP] ([implementation][es-fusdc-weth-LP-proxy]), [fUSDT_WETH_LP][es-fusdt-weth-LP] ([implementation][es-fusdt-weth-LP-proxy]), [fDAI-WETH-LP][es-fdai-weth-LP] ([implementation][es-fdai-weth-LP-proxy]) |
| **Strategy Contract**   | SNXRewardUniLPStrategy [WBTC-WETH][es-weth-wbtc-strategy], [USDT-WETH][es-weth-usdt-strategy], [USDC-WETH][es-weth-usdc-strategy], [DAI-WETH][es-weth-dai-strategy]|
| **Example Harvest TX**  | [doHardWork][es-weth-wbtc-harvest]|

[es-fwbtc-weth-LP]: https://etherscan.io/address/0x01112a60f427205dca6e229425306923c3cc2073 
[es-fusdc-weth-LP]: https://etherscan.io/address/0xa79a083fdd87f73c2f983c5551ec974685d6bb36
[es-fusdt-weth-LP]: https://etherscan.io/address/0x7ddc3fff0612e75ea5ddc0d6bd4e268f70362cff
[es-fdai-weth-LP]: https://etherscan.io/address/0x307e2752e8b8a9c29005001be66b1c012ca9cdb7

[es-fwbtc-weth-LP-proxy]: https://etherscan.io/address/0x9b3be0cc5dd26fd0254088d03d8206792715588b
[es-fusdc-weth-LP-proxy]: https://etherscan.io/address/0x9b3be0cc5dd26fd0254088d03d8206792715588b
[es-fusdt-weth-LP-proxy]: https://etherscan.io/address/0x9b3be0cc5dd26fd0254088d03d8206792715588b
[es-fdai-weth-LP-proxy]: https://etherscan.io/address/0x9b3be0cc5dd26fd0254088d03d8206792715588b

[es-weth-wbtc-strategy]: https://etherscan.io/address/0x46ec909099f9691b43b64413f1bc662edfbee00a
[es-weth-usdt-strategy]: https://etherscan.io/address/0xc6e973b8fe772c58ad0d20099d43d2b3f0aef5c0
[es-weth-usdc-strategy]: https://etherscan.io/address/0x0fd7c77b473e3efe3170536805a14b61050efc6e
[es-weth-dai-strategy]: https://etherscan.io/address/0x2cf4ceb36172fb2196a47490419d57584234cbd4

[es-weth-wbtc-harvest]: https://etherscan.io/tx/0x7e9f139d796487bebe3b0d6e629aee01fafc6b1dd05a8783aa297c96625510cd

## Farming SUSHI with LP Tokens

This strategy farms SUSHI, the [Sushiswap token][sushi].

> You do not receive SUSHI directly. Instead, the farmed SUSHI is sold to return more BTC to you when you withdraw.
{.is-info}

| | |
|------------------|-|
| **Asset Farmed**        | SUSHI, Sushiswap token  |
| **Assets Used**         | WBTC-TBTC |
| **Basic Strategy**      | SUSHI is automatically farmed and sold for more LP tokens. Harvest pays your gas fees to grow the underlying LP. 30% of rewards are kept for FARM profit sharing. |
| **How To Participate**  | [deposit a supported asset][hf] |
| **Yield Payout**        | Successful farming makes your deposit redeemable for a growing amount of the deposited asset |
| **FARM Incentives**      | [fSLP deposit receipts can be deposited to earn a stakedrop of FARM][farm-stakedrop] |
| **Vault Contract**      | fSLP [fWBTC_TBTC_LP][es-fwbtc-tbtc-LP] ([implementation][es-fwbtc-tbtc-LP-proxy]) |
| **Strategy Contract**   | SushiMasterChefLPStrategy [fWBTC_TBTC_LP][es-wbtc-tbtc-strategy] |
| **Example Harvest TX**  | [doHardWork][es-wbtc-tbtc-harvest] |

[es-fwbtc-tbtc-LP]: https://etherscan.io/address/0xF553E1f826f42716cDFe02bde5ee76b2a52fc7EB

[es-fwbtc-tbtc-LP-proxy]: https://etherscan.io/address/0x9b3be0cc5dd26fd0254088d03d8206792715588b

[es-wbtc-tbtc-strategy]: https://etherscan.io/address/0x53df6664b3ddE086DCe6315c317d1002b14B87E3

[es-wbtc-tbtc-harvest]: https://etherscan.io/tx/0xdb0f7cd77685b5ac36cbf251771b4d26c9056aaa583eccc2cabdc43be50640d6

## Farming Cream with WETH
This strategy farms CREAM, the [Cream Finance Token][cream].

> You do not receive CREAM directly. Instead, the farmed CREAM is sold to return more wETH to you when you withdraw.
{.is-info}

| | |
|------------------|-|
| **Asset Farmed**        | CREAM, Cream Finance token  |
| **Assets Used**         | WETH               |
| **Basic Strategy**      | CREAM is farmed and sold for stablecoins |
| **How To Participate**  | [deposit WETH][hf] to receive fWETH |
| **Yield Payout**        | Successful farming makes the fWETH redeemable for a growing number of WETH |
| **FARM Incentives**      | [The fWETH can be deposited to earn a stakedrop of FARM][farm-stakedrop] |
| **Vault Contract**      | [fWETH][es-fweth] |
| **Strategy Contract**   | [WETHCreamNoFoldStrategy][es-weth-strategy] |
| **Example Harvest TX**  | [doHardWork][harvestcream] |

[es-weth-strategy]: https://etherscan.io/address/0xcf477f117caa349ca92dedb3955481628d463bf1#code

[harvestcream]: https://etherscan.io/tx/0x9f9e3640b8cfd503cbd9115f8c457b1273858f582c4dfb928e21f32eb78e717c

## Farming Other Things

Evidence that more is in the works:

**FARM_crvRenWBTC**
https://etherscan.io/address/0x192e9d29d43db385063799bc239e772c3b6888f3#readContract
strategy: 0xaf2d2e5c5af90c782c008b5b287f20334eeb308e ???
underlying: 0x49849c98ae39fff122806c06791fa73784fb3675 Curve.fi renBTC/wBTC (crvRenWBTC)
NoMintRewardPool: https://etherscan.io/address/0x5365a2c47b90ee8c9317fac20edc3ce7037384fb#readContract

**FARM_renBTC (frenBTC)**
https://etherscan.io/address/0xfbe122d0ba3c75e1f7c80bd27613c9f35b81feec#code
strategy: 0x86de355d20ce83692ec4744b71b74f01a8e838b3 CRVStrategyRENBTCMainnet
underlying: 0xeb4c2781e4eba804ce9a9803c67d0893436bb27d renBTC (renBTC)
NoMintRewardPool: https://etherscan.io/address/0xcfe1103863f9e7cf3452ca8932eef44d314bf9c5#code

**FARM_WBTC (fWBTC)**
https://etherscan.io/address/0xc07eb91961662d275e2d285bdc21885a4db136b0
strategy: 0x16438572ce90caacd83f175b4b9e22e360a76b48 CRVStrategyWBTCMainnet
underlying: 0x2260fac5e5542a773aa44fbcfedf7c193bc2c599 Wrapped BTC (WBTC)
NoMintRewardPool: https://etherscan.io/address/0x6291ece696cb6682a9bb1d42fca4160771b1d7cc#readContract

**CRVStrategySwerveUSDTMainnet** (v2?)
https://etherscan.io/address/0x0477b3b746f99010d255f6556444039e2e58864e#code

**CRVStrategySwerveUSDCMainnet** (v2?)
https://etherscan.io/address/0x00f9d525828beebf1ee75fb72b1f21932e195bdf#code




# Potential Strategy Improvements
 
 ## Vote-Locking SWRV
 
 **Concept**
 
 > Curve has protections in place to only allow whitelisted contracts to vote-lock, but these protections have been removed by Swerve. Verify this by inspecting [Curve](https://github.com/curvefi/curve-dao-contracts/blob/master/contracts/VotingEscrow.vy) and [Swerve](https://github.com/SwerveFinance/SwervContracts/blob/master/VotingEscrow.vy) VotingEscrow code and by [diffing the deployed contracts](https://yieldfarming.info/tools/diff/?contract1=0x5f3b5dfeb7b28cdbd7faba78963ee202a494e2a2&contract2=0xe5e7ddadd563018b0e692c1524b60b754fbd7f02).
{.is-success}
 
 The Curve and Swerve AMMs both support a feature whereby governance tokens can be locked for a time to increase the user's voting power and governance token rewards.
 
 Governance token reward rate can be boosted up to 2.5x by locking a sufficient proportion of available tokens for a sufficient length of time.
 
 Both Curve and Swerve offer calculators to make it straightforward to determine how much of an asset needs to be locked to obtain the maximum boost:
 
 - https://dao.curve.fi/minter/calc
 - http://ipfs2.swerve.fi/dao/#/minter/calc
 
 As of September 7th 2020, 1 SWRV locked for the maximum duration of 4 years would yield the maximum vote boost on up to 8700 swUSD.

 
 **Implementation**
 
 Ideally, it would be possible for anyone to acquire the necessary CRV/SWRV to lock it and boost the Curve/Swerve strategy's rewards rate.
 
 The `VotingEscrow` contract does offer a `deposit_for(_addr: address, _value: uint256)` function. This function can only increase the balance of an existing lock, but cannot be used to create a new lock for the target account:
 
 ```
 @external
 @nonreentrant('lock')
 def deposit_for(_addr: address, _value: uint256):
     """
     @notice Deposit `_value` tokens for `_addr` and add to the lock
     @dev Anyone (even a smart contract) can deposit for someone else, but
          cannot extend their locktime and deposit for a brand new user
     @param _addr User's wallet address
     @param _value Amount to add to user's lock
     """
     _locked: LockedBalance = self.locked[_addr]
 
     assert _value > 0  # dev: need non-zero value
     assert _locked.amount > 0, "No existing lock found"
     assert _locked.end > block.timestamp, "Cannot add to expired lock. Withdraw"
 
     self._deposit_for(_addr, _value, 0, self.locked[_addr], DEPOSIT_FOR_TYPE)
 ```
 
 To initiate the lock, the Harvest contract must call `create_lock` directly:
 
 ```
 @external
 @nonreentrant('lock')
 def create_lock(_value: uint256, _unlock_time: uint256):
     """
     @notice Deposit `_value` tokens for `msg.sender` and lock until `_unlock_time`
     @param _value Amount to deposit
     @param _unlock_time Epoch time when tokens unlock, rounded down to whole weeks
     """
     unlock_time: uint256 = (_unlock_time / WEEK) * WEEK  # Locktime is rounded down to weeks
     _locked: LockedBalance = self.locked[msg.sender]
 
     assert _value > 0  # dev: need non-zero value
     assert _locked.amount == 0, "Withdraw old tokens first"
     assert unlock_time > block.timestamp, "Can only lock until time in the future"
     assert unlock_time <= block.timestamp + MAXTIME, "Voting lock can be 4 years max"
 
     self._deposit_for(msg.sender, _value, unlock_time, _locked, CREATE_LOCK_TYPE)
 ```
 
 This probably requires the deployment of new Curve/Swerve strategy contracts that implement a locking function.
 
 **Example Contract Calls**
 
 Note that `user_checkpoint`, or another function that creates a checkpoint, must be called after `create_lock` in order to begin receiving the reward boost.
 
 Approval to lock
 https://etherscan.io/tx/0x8287d96920c3a54b84bc89cb34a605683457392e3b84213f1f910f3b4116c4b4
 Contract https://etherscan.io/address/0xb8baa0e4287890a5f79863ab62b7f175cecbd433
 SWRV Token https://github.com/SwerveFinance/SwervContracts/blob/master/ERC20CRV.vy 
 ```Function: approve(address _spender, uint256 _value)
 MethodID: 0x095ea7b3
 [0]:  000000000000000000000000e5e7ddadd563018b0e692c1524b60b754fbd7f02
 [1]:  0000000000000000000000000000000000000000000000000de0b6b3a7640000
 ```
 
 Lock
 https://etherscan.io/tx/0xb5180cb9cac469382338667efbfb7cf3eb4083ef3c4adcc6a1929298edcf3ed0
 Contract https://etherscan.io/address/0xe5e7ddadd563018b0e692c1524b60b754fbd7f02
 Voting Escrow https://github.com/SwerveFinance/SwervContracts/blob/master/VotingEscrow.vy
 ```Function: create_lock(uint256 _value, uint256 _unlock_time)
 MethodID: 0x65fc3873
 [0]:  0000000000000000000000000000000000000000000000000de0b6b3a7640000
 [1]:  0000000000000000000000000000000000000000000000000000000066da9c04
 ```
 
 Checkpoint
 https://etherscan.io/tx/0x8f44f99284bdc54ddda99d5f106b66705151634099aa7bfd624bbdbda7621997
 Contract https://etherscan.io/address/0xb4d0c929cd3a1fbdc6d57e7d3315cf0c4d6b4bfa
 Liquidity Gauge https://github.com/SwerveFinance/SwervContracts/blob/master/LiquidityGauge.vy
 ```Contract 0xb4d0c929cd3a1fbdc6d57e7d3315cf0c4d6b4bfa Liquidity Gauge
 Function: user_checkpoint(address addr)
 MethodID: 0x4b820093
 [0]:  00000000000000000000000051d2c880493ac63140ffe0e645cc99afc228ab59
 ```
 
 



# Inactive Farming Strategies

> Strategies in this section have been deployed, but are not presently in active use. Note that some of these represent obsolete strategies that have been updated in the active strategy section.
{.is-warning}

## Farming SWRV with Stablecoins

This strategy farms SWRV, the [Swerve Finance DAO token][swrv].

> You do not receive SWRV directly. Instead, the farmed SWRV is sold to return more stablecoins to you when you withdraw.
{.is-info}



 | | |
|------------------|-|
| **Asset Farmed**        | SWRV, Swerve Finance DAO token  |
| **Assets Used**         | DAI, USDC, USDT               |
| **Basic Strategy**      | SWRV is farmed and sold for stablecoins |
| **How To Participate**  | [deposit a supported asset][hf] |
| **Yield Payout**        | Successful farming makes your deposit redeemable for a growing amount of the deposited asset |
| **FARM Incentives**      | [fDAI, fUSDC, and fUSDT deposit receipts can be deposited to earn a stakedrop of FARM][farm-stakedrop] |
| **Vault Contracts**      | [VaultDAI](https://etherscan.io/address/0xe85c8581e60d7cd32bbfd86303d2a4fa6a951dac#code), [VaultUSDC](https://etherscan.io/address/0xc3f7ffb5d5869b3ade9448d094d81b0521e8326f#code), [VaultUSDT](https://etherscan.io/address/0xc7ee21406bb581e741fbb8b21f213188433d9f2f#code) |
| **Strategy Contracts**   | [CRVStrategySwerveUSDTMainnet](https://etherscan.io/address/0x892171eb51d56dc340e586652068cf758e5f798c#code), [CRVStrategySwerveDAIMainnet](https://etherscan.io/address/0xf60afebb76c43f636e4d1a099847fc97dc8bded0#code), [CRVStrategySwerveUSDCMainnet](https://etherscan.io/address/0x66b7611f35e48e311929e25d73428410c2335c34#code) |
| **Example Harvest TX**  | [doHardWork](https://etherscan.io/tx/0x1c838d667a553139bc81c8913e48c1ceb3dccd626f8c97a9e7c4ebe25b588531) |

## Farming CRV with Stablecoins v1

This strategy farms CRV, the [Curve Finance DAO token][crv].

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
| **Vault Contract**      | [VaultYCRV][es-vaultycrv] |
| **Strategy Contract**   | [CRVStrategyYCRVMainnet][es-strat-crvstable-v1] |
| **Example Harvest TX**  | [doHardWork](https://etherscan.io/tx/0xf69262029ce30403101cda38d110ae897a6c23b4b8748d10a9a3514c012c365d) |

[es-strat-crvstable-v1]: https://etherscan.io/address/0xcf5f83f8fe0ab0f9e9c1db07e6606dd598b2bbf5
[es-vaultycrv]: https://etherscan.io/address/0xf2b223eb3d2b382ead8d85f3c1b7ef87c1d35f3a

![harvestcrvstrategy.png](/harvestcrvstrategy.png)

## Farming Cream with WETH V1
This strategy farms CREAM, the [Cream Finance Token][cream].

> You do not receive CREAM directly. Instead, the farmed CREAM is sold to return more stablecoins to you when you withdraw.
{.is-info}

| | |
|------------------|-|
| **Asset Farmed**        | CREAM, Cream Finance token  |
| **Assets Used**         | WETH               |
| **Basic Strategy**      | CREAM is farmed and sold for stablecoins |
| **How To Participate**  | [deposit WETH][hf] to receive fWETH |
| **Yield Payout**        | Successful farming makes the fWETH redeemable for a growing number of WETH |
| **FARM Incentives**      | [The fWETH can be deposited to earn a stakedrop of FARM][farm-stakedrop] |
| **Vault Contract**      | [fWETH][es-fweth] |
| **Strategy Contract**   | [WETHCreamNoFoldStrategy][es-weth-strategy-v1] |
| **Example Harvest TX**  | [doHardWork][harvestcream-v1] |

[es-weth-strategy-v1]: https://etherscan.io/address/0x4e015af8e1c5eb020f91063661cc5ce43719ebcf#code

[harvestcream-v1]: https://etherscan.io/tx/0x9b5f2b36e960f533b3eec83773306c9a3a4a74f596addff2951d4cfd6a9b7694

## Farming UNI With LP Tokens V1 (No FARM Rewards)
This strategy farms UNI, the [Uniswap Token][uni].

> You do not receive UNI directly. Instead, the farmed UNI is sold to return more lp tokens of the type deposited when you withdraw.
{.is-info}

| | |
|------------------|-|
| **Asset Farmed**        | UNI, Uniswap token  |
| **Assets Used**         | ETH-DAI, ETH-USDC, ETH-USDT, ETH-WBTC              |
| **Basic Strategy**      | UNI is automatically farmed and sold for more LP tokens. Harvest pays your gas fees to grow the underlying LP. 5% of rewards are kept for FARM profit sharing. |
| **How To Participate**  | [deposit LP Tokens][hf] to receive fUNI-V2 |
| **Yield Payout**        | Successful farming makes the fUNI-V2 redeemable for a growing number of LP tokens. |
| **FARM Incentives**     | There are no current FARM incentives for depositing your UNI LP. |
| **Vault Contract**      | fUNI-V2 [fWBTC_WETH_LP][es-fwbtc-weth-LP-v1], [fUSDC_WETH_LP][es-fusdc-weth-LP-v1], [fUSDT_WETH_LP][es-fusdt-weth-LP-v1], [fDAI-WETH-LP][es-fdai-weth-LP-v1] |
| **Strategy Contract**   | SNXRewardUniLPStrategy [WBTC-WETH][es-weth-wbtc-strategy-v1], [USDT-WETH][es-weth-usdt-strategy-v1], [USDC-WETH][es-weth-usdc-strategy-v1], [DAI-WETH][es-weth-dai-strategy-v1]|
| **Example Harvest TX**  | [doHardWork][es-weth-wbtc-harvest-v1]|

[es-fwbtc-weth-LP-v1]: https://etherscan.io/address/0xb1feb6ab4ef7d0f41363da33868e85eb0f3a57ee
[es-fusdc-weth-LP-v1]: https://etherscan.io/address/0x63671425ef4D25Ec2b12C7d05DE855C143f16e3B
[es-fusdt-weth-LP-v1]: https://etherscan.io/address/0xB19EbFB37A936cCe783142955D39Ca70Aa29D43c
[es-fdai-weth-LP-v1]: https://etherscan.io/address/0x1a9F22b4C385f78650E7874d64e442839Dc32327


[es-weth-wbtc-strategy-v1]: https://etherscan.io/address/0x0a7d74604b39229d444855ef294f287099774ac8
[es-weth-usdt-strategy-v1]: https://etherscan.io/address/0xb43aa2c44b99bad346143fb44e264213d412b6c2
[es-weth-usdc-strategy-v1]: https://etherscan.io/address/0x50f1191f3059069888d9e16a327b96afdd26c6fd
[es-weth-dai-strategy-v1]: https://etherscan.io/address/0x2fee56e039acccefa3cb1f3051ad00fe550a472c

[es-weth-wbtc-harvest-v1]: https://etherscan.io/tx/0x5b609ca7f6a78d879a6ca36917ff7f8f7916cd5cd8fc4276d28cedc2e66fdc8c

## Farming UNI With LP Tokens (V2, no timelocks)
This strategy farms UNI, the [Uniswap Token][uni].

> You do not receive UNI directly. Instead, the farmed UNI is sold to return more lp tokens of the type deposited when you withdraw.
{.is-info}

| | |
|------------------|-|
| **Asset Farmed**        | UNI, Uniswap token  |
| **Assets Used**         | ETH-DAI, ETH-USDC, ETH-USDT, ETH-WBTC              |
| **Basic Strategy**      | UNI is automatically farmed and sold for more LP tokens. Harvest pays your gas fees to grow the underlying LP. 5% of rewards are kept for FARM profit sharing. |
| **How To Participate**  | [deposit LP Tokens][hf] to receive fUNI-V2 |
| **Yield Payout**        | Successful farming makes the fUNISWAP_LP redeemable for a growing number of LP tokens. |
| **FARM Incentives**     | [The fUNISWAP_LP can be deposited to earn a stakedrop of FARM][farm-stakedrop] |
| **Vault Contract**      | fUNI-V2 [fWBTC_WETH_LP][es-fwbtc-weth-LP-v2], [fUSDC_WETH_LP][es-fusdc-weth-LP-v2], [fUSDT_WETH_LP][es-fusdt-weth-LP-v2], [fDAI-WETH-LP][es-fdai-weth-LP-v2] |
| **Strategy Contract**   | SNXRewardUniLPStrategy [WBTC-WETH][es-weth-wbtc-strategy-v2], [USDT-WETH][es-weth-usdt-strategy-v2], [USDC-WETH][es-weth-usdc-strategy-v2], [DAI-WETH][es-weth-dai-strategy-v2]|
| **Example Harvest TX**  | [doHardWork][es-weth-wbtc-harvest-v2]|

[es-fwbtc-weth-LP-v2]: https://etherscan.io/address/0xb1feb6ab4ef7d0f41363da33868e85eb0f3a57ee
[es-fusdc-weth-LP-v2]: https://etherscan.io/address/0x63671425ef4D25Ec2b12C7d05DE855C143f16e3B
[es-fusdt-weth-LP-v2]: https://etherscan.io/address/0xB19EbFB37A936cCe783142955D39Ca70Aa29D43c
[es-fdai-weth-LP-v2]: https://etherscan.io/address/0x1a9F22b4C385f78650E7874d64e442839Dc32327


[es-weth-wbtc-strategy-v2]: https://etherscan.io/address/0xd3927f43d622e8bc9ce9a1111becd5d6d3cf3c90
[es-weth-usdt-strategy-v2]: https://etherscan.io/address/0x13627b75cf955eee2d57fc11a7082de5c36050c3
[es-weth-usdc-strategy-v2]: https://etherscan.io/address/0x987a168e19f6f64d6ab08ae0e0fe77ea3d79baac
[es-weth-dai-strategy-v2]: https://etherscan.io/address/0xa82660a0a468bba63db950532cdbda47144c212c

[es-weth-wbtc-harvest-v2]: https://etherscan.io/tx/0x5b609ca7f6a78d879a6ca36917ff7f8f7916cd5cd8fc4276d28cedc2e66fdc8c






[farm-stakedrop]: https://harvest.finance/earn

[crv]: https://www.coingecko.com/en/coins/curve-dao-token
[hf]: https://harvest.finance
[swrv]: https://www.coingecko.com/en/coins/swerve
[cream]: https://www.coingecko.com/en/coins/cream
[uni]: https://www.coingecko.com/en/coins/uniswap
[sushi]: https://www.coingecko.com/en/coins/sushi



[es-farm]: https://etherscan.io/address/0xa0246c9032bc3a600820415ae600c6388619a14d
[es-fdai]: https://etherscan.io/address/0xe85c8581e60d7cd32bbfd86303d2a4fa6a951dac
[es-fusdc]: https://etherscan.io/address/0xc3f7ffb5d5869b3ade9448d094d81b0521e8326f
[es-fusdt]: https://etherscan.io/address/0xc7ee21406bb581e741fbb8b21f213188433d9f2f
[es-vaultycrv]: https://etherscan.io/address/0xf2b223eb3d2b382ead8d85f3c1b7ef87c1d35f3a
[es-fwbtc]: https://etherscan.io/address/0xc07eb91961662d275e2d285bdc21885a4db136b0
[es-frenbtc]: https://etherscan.io/address/0xfbe122d0ba3c75e1f7c80bd27613c9f35b81feec
[es-fcrvrenwbtc]: https://etherscan.io/address/0x192E9d29D43db385063799BC239E772c3b6888F3
[es-fweth]: https://etherscan.io/address/0x8e298734681adbfc41ee5d17ff8b0d6d803e7098
[es-ftusd]: https://etherscan.io/address/0x9b3be0cc5dd26fd0254088d03d8206792715588b
[es-ftusd-proxy]: https://etherscan.io/address/0x7674622c63bee7f46e86a4a5a18976693d54441b
