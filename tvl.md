---
title: Total Value Locked
description: how to calculate TVL using the Harvest contracts
published: true
date: 2020-09-17T18:32:59.231Z
tags: 
editor: markdown
dateCreated: 2020-09-17T17:40:49.170Z
---

# TVL vs AUM
The TVL displayed on the Harvest Finance website includes assets locked in incentivized liquidity pools and FARM staked in the profit share.

# Calculating AUM

The assets that Harvest uses to farm are deposited in vault contracts, which issue farming asset tokens (fASSETs) as a receipt. As successful harvests occur, the fASSET is redeemable for a growing amount of the underlying asset.

| Vault    |      Lock Token      |  You Receive Instead | Vault Contract Address |
|-----------|:----------------------|:--------------|:--------------:|
| DAI Vault | DAI | fDAI | [0xe85C8581e60D7Cd32Bbfd86303d2A4FA6a951Dac](https://etherscan.io/address/0xe85C8581e60D7Cd32Bbfd86303d2A4FA6a951Dac) |
| USDC Vault | USDC | fUSDC| [0xc3F7ffb5d5869B3ade9448D094d81B0521e8326f](https://etherscan.io/address/0xc3F7ffb5d5869B3ade9448D094d81B0521e8326f) |
| USDT Vault | USDT | fUSDT | [0xc7EE21406BB581e741FBb8B21f213188433D9f2F](https://etherscan.io/address/0xc7EE21406BB581e741FBb8B21f213188433D9f2F) |
| WBTC Vault | WBTC | fWBTC | [0xc07eb91961662d275e2d285bdc21885a4db136b0](https://etherscan.io/address/0xc07eb91961662d275e2d285bdc21885a4db136b0) |
| RENBTC Vault | RENBTC | fRENBTC | [0xfbe122d0ba3c75e1f7c80bd27613c9f35b81feec](https://etherscan.io/address/0xfbe122d0ba3c75e1f7c80bd27613c9f35b81feec) |
| CRVRENBTC Vault | CRVRENBTC | fCRVRENBTC | [0x192e9d29d43db385063799bc239e772c3b6888f3](https://etherscan.io/address/0x192e9d29d43db385063799bc239e772c3b6888f3) |
| WETH Vault | WETH | fWETH | [0x8e298734681adbfC41ee5d17FF8B0d6d803e7098](https://etherscan.io/address/0x8e298734681adbfC41ee5d17FF8B0d6d803e7098) |

Key functions for calculating TLV that are implemented by each Vault:

- `underlying` is the address of the vault's underlying asset
- `underlyingBalanceWithInvestment` is the total amount of the underlying asset in the vault
- `underlyingUnit` is the value to divide by to convert the underlying balance to human-readable form

Other functions not needed for TLV calculations:

- `getPricePerFullShare` is the current conversion rate between fASSET and ASSET. This increases with successful harvests.

