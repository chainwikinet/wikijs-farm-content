---
title: Harvest Vault
description: 
published: true
date: 2020-12-10T20:05:38.840Z
tags: 
editor: markdown
dateCreated: 2020-12-10T20:05:38.840Z
---

# Harvest Vaults
A vault is an Ethereum scaling solution that allows users to safely deposit and withdraw funds from a pool of investable assets. 

When a user deposits funds, they are issued a share of the vault, represented by an `fASSET`. These user's funds are then made available for investment according to a pre-defined "strategy" specified by the Harvest devs. Whenever an investment strategy generates revenue (or losses), the total amount of assets in the Vault is updated, however the number of existing `fASSET` shares does not change. As a result, the value of each `fASSET` share increases with every successful harvest. When a user withdraws `fASSET` shares from the vault, the `fASSET` is burned and the user receives funds proportional to the growth of the investment since their deposit.

User funds are protected in vaults by a number of mechanism:
1. The owners of the vault can only move the underlying funds in and out of the pre-defined investment strategy.
2. The investment strategy is protected from changes by a 'timelock.'
3. `fASSET`shares can only be minted by depositing funds into the vault, and are destroyed when the user withdraws funds.

Harvest Vaults do not track the wallet addresses of depositors. Instead, `fASSET` shares are represented by fungible ERC-20 tokens that can be transferred between accounts and traded on secondary markets. Users that trade away or lose their `fASSET` shares will not have access to their deposited funds. 

Because ethereum gas usage is defined by the number of contracts interacted with and the complexity of the interactions, depositing tokens through the Vault smart contract and minting new `fASSET` shares requires signifantly more gas than than the token trading that most Ethereum users may be used to. Users should take care to monitor gas expenses, as they may reduce or even overwhelm the profitability of smaller scale investments (<$1000), especially when network activity is high.

Harvest provides additional incentives for users to deposit funds in the form of `FARM` tokens. These rewards are distributed to users who prove ownership of deposits by "staking" their `fASSETs` in reward pool contracts. For more information, see [staking](staking). 