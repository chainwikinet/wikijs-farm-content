---
title: Harvest Finance Yield Farming Strategies
description: how the Total Value Locked in Harvest creates revenue for FARM holders
published: true
date: 2020-09-07T21:02:23.226Z
tags: 
editor: markdown
---

# Active Yield Farming Strategies

Harvest Finance is launching with one active yield farming strategy. More strategies will be added soon after user feedback is incorporated into the Harvest Finance site.

95% of the yield farming revenue is returned to users who provide capital. The remaining 5% of the yield farming revenue is distributed to users who [stake FARM in the Profit Sharing contract][farm-stakedrop]. The Harvest Finance team does not charge fees for withdrawing or depositing assets and does not claim a fee on the yield farming revenue.

## Farming SWRV

The second yield farming strategy active on Harvest Finance farms SWRV, the [Swerve Finance DAO token][swrv].

> You do not receive CRV directly. Instead, the farmed CRV is sold to return more stablecoins to you when you withdraw.
{.is-info}

 | | |
|------------------|-|
| **Asset Farmed**        | SWRV, Swerve Finance DAO token  |
| **Assets Used**         | DAI, USDC, USDT               |
| **Basic Strategy**      | SWRV is farmed and sold for stablecoins |
| **How To Participate**  | [deposit DAI, USDC, USDT][hf] to receive fDAI, fUSDC, fUSDT |
| **Yield Payout**        | Successful farming makes the fDAI, fUSDC, and fUSDT redeemable for a growing number of DAI, USDC, and USDT |
| **FARM Incentives**      | [The fDAI, fUSDC, and fUSDT can be deposited to earn a stakedrop of FARM][farm-stakedrop] |
| **Vault Contracts**      | [VaultDAI](https://etherscan.io/address/0xe85c8581e60d7cd32bbfd86303d2a4fa6a951dac#code), [VaultUSDC](https://etherscan.io/address/0xc3f7ffb5d5869b3ade9448d094d81b0521e8326f#code), [VaultUSDT](https://etherscan.io/address/0xc7ee21406bb581e741fbb8b21f213188433d9f2f#code) |
| **Strategy Contracts**   | [CRVStrategySwerveUSDTMainnet](https://etherscan.io/address/0x892171eb51d56dc340e586652068cf758e5f798c#code), [CRVStrategySwerveDAIMainnet](https://etherscan.io/address/0xf60afebb76c43f636e4d1a099847fc97dc8bded0#code), [CRVStrategySwerveUSDCMainnet](https://etherscan.io/address/0x892171eb51d56dc340e586652068cf758e5f798c#code) |
| **Example Harvest TX**  | [doHardWork](https://etherscan.io/tx/0x1c838d667a553139bc81c8913e48c1ceb3dccd626f8c97a9e7c4ebe25b588531) |



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
 
 
 # New Strategy Proposals
 
 > Grow Harvest. [Contribute to this wiki!](/contribute)
 {.is-success}





[farm-stakedrop]: https://harvest.finance/earn
[harvest]: https://etherscan.io/tx/0xf69262029ce30403101cda38d110ae897a6c23b4b8748d10a9a3514c012c365d
[crvstrategy]: https://etherscan.io/address/0xcf5f83f8fe0ab0f9e9c1db07e6606dd598b2bbf5
[vaultycrv]: https://etherscan.io/address/0xf2b223eb3d2b382ead8d85f3c1b7ef87c1d35f3a
[crv]: https://www.coingecko.com/en/coins/curve-dao-token
[hf]: https://harvest.finance
[swrv]: https://www.coingecko.com/en/coins/swerve

