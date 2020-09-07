---
title: Harvest Finance Governance
description: voting with FARM
published: true
date: 2020-09-07T07:17:49.896Z
tags: 
editor: markdown
---


# Potential Strategy Improvements

## Vote-Locking SWRV

**Concept**

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
{.is-info}
