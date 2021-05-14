---
title: BSC Strategies
description: 
published: true
date: 2021-05-14T21:39:09.207Z
tags: 
editor: markdown
dateCreated: 2021-05-11T18:32:46.895Z
---



> Please do not interact directly with Smart contracts!
{.is-danger}


# Active BSC Strategies

**SPACE Strategies**
Summary: deposit funds into Harvest to automatically harvest rewards.
Rewards: Reward tokens are sold for additional deposited token.

SPACE farming: `SPACE-BNB`, `SPACE-BUSD`
Strategy vaults: 
[farm SPACE with SPACE-BNB in Pancakeswap](https://bscscan.com//address/0x14CB410659b4a4a7CCEa99E6F6C9eac8718160dF)
[farm SPACE with SPACE-BUSD in Pancakeswap](https://bscscan.com//address/0x129cCeE12A9542Ff77e066E6F8d7DF49F8Cbf89D)

**VENUS Strategies**
Summary: deposit funds into Harvest to automatically harvest rewards.
Rewards: Reward tokens are sold for additional deposited token.

VENUS farming: `WBNB`, `DAI`, `USDC`, `USDT`, `BUSD`, `XVS`, `VAI`, `BETH`, `ETH`, `BTCB`
Strategy vaults: 
[farm VENUS with WBNB](https://bscscan.com//address/0x1274B70bF34E1a57E78C2A2f3E28a4E1B66cbE48)
[farm VENUS with DAI](https://bscscan.com//address/0x78cF4a86bA3b4C5246D097E5cd0833cB641C1425)
[farm VENUS with USDC](https://bscscan.com//address/0x5089EA6c884a03823672888b57EBCE929EcE63ca)
[farm VENUS with USDT](https://bscscan.com//address/0x374787234b369b56b3701E0B932051b37726096a)
[farm VENUS with BUSD](https://bscscan.com//address/0x1BFB4ed996F4356aa705891DedB7d7776402BeC1)
[farm VENUS with XVS](https://bscscan.com//address/0xCf5F83F8FE0AB0f9E9C1db07E6606dD598b2bbf5)
[farm VENUS with VAI](https://bscscan.com//address/0x33DA6B1a05B4afcC5a321aACaA1334BDA4345a14)
[farm VENUS with BETH](https://bscscan.com//address/0x394E653bbFC9A3497A0487Abee153CA6498F053D)
[farm VENUS with ETH](https://bscscan.com//address/0x2CE34b1bb247f242f1d2A33811E01138968EFBFF)
[farm VENUS with BTCB](https://bscscan.com//address/0xd75ffA16FFbCf4078d55fF246CfBA79Bb8cE3F63)


## Farming SPACE with LP tokens
This strategy farms SPACE, the [Farm Space Token](https://coinmarketcap.com/currencies/farm-space/).

> You do not receive SPACE directly. Instead, the farmed SPACE is sold to return more LP tokens to you when you withdraw.
{.is-info}

| | |
|------------------|-|
| **Asset Farmed**        | SPACE, the Farm Space Token  |
| **Assets Used**         | SPACE-BNB, SPACE-BUSD  |
| **Basic Strategy**      | SPACE is farmed and sold for LP tokens |
| **How To Participate**  | [deposit SPACE LP tokens](https://harvest.finance/) to receive fSPACE LP |
| **Yield Payout**        | Successful farming makes the fSPACE LP redeemable for a growing number of SPACE LP tokens |
| **FARM Incentives**      | fSPACE LP deposit receipts can be staked to earn FARM incentives |
| **Vault Contract**      | [SPACE-BNB](https://bscscan.com//address/0x14CB410659b4a4a7CCEa99E6F6C9eac8718160dF) [SPACE-BUSD](https://bscscan.com//address/0x129cCeE12A9542Ff77e066E6F8d7DF49F8Cbf89D) |
| **Strategy Contract**   |  |
| **Example Harvest TX**  | [doHardWork][harvestdego] |
| **Timelock**            | 12 Hours

[es-weth-strategy]: https://etherscan.io/address/0xa23c6f2d85fe47e613ce6bbb40e74acb49ae281a#code

[harvestdego]: https://etherscan.io/tx/0x6fdb02f8f961dae5853d15c1ff06322025abdf3eb76097a1d99b2fbe888c005b

## Farming XVS with single assets
This strategy farms XVS, the [Venus Token](https://www.coingecko.com/en/coins/venus).

> You do not receive XVS directly. Instead, the farmed XVS is sold to return more tokens to you when you withdraw.
{.is-info}

| | |
|------------------|-|
| **Asset Farmed**        | XVS, the Venus token  |
| **Assets Used**         | `WBNB`, `DAI`, `USDC`, `USDT`, `BUSD`, `XVS`, `VAI`, `BETH`, `ETH`, `BTCB`  |
| **Basic Strategy**      | XVS is farmed and sold for single assets |
| **How To Participate**  | [deposit single assets tokens](https://harvest.finance/) to receive fSPACE LP |
| **Yield Payout**        | Successful farming makes the fAssets redeemable for a growing number of single assets |
| **FARM Incentives**      | fAssets tokens deposit receipts can be staked to earn FARM incentives |
| **Vault Contract**      | [SPACE-BNB](https://bscscan.com//address/0x14CB410659b4a4a7CCEa99E6F6C9eac8718160dF) [SPACE-BUSD](https://bscscan.com//address/0x129cCeE12A9542Ff77e066E6F8d7DF49F8Cbf89D) |
| **Strategy Contract**   |  |
| **Example Harvest TX**  | [doHardWork][harvestdego] |
| **Timelock**            | 12 Hours

[es-weth-strategy]: https://etherscan.io/address/0xa23c6f2d85fe47e613ce6bbb40e74acb49ae281a#code

[harvestdego]: https://etherscan.io/tx/0x6fdb02f8f961dae5853d15c1ff06322025abdf3eb76097a1d99b2fbe888c005b