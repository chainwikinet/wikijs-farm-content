---
title: Make fASSETs liquid
description: 
published: true
date: 2020-10-04T01:21:44.425Z
tags: 
editor: markdown
dateCreated: 2020-10-02T11:09:52.564Z
---

# Vault Deposit/Withdrawal Costs

By depositing teh 

| Asset   | Deposit Gas | Withdraw Gas |
|---------|-------------|--------------|
| fSTABLE | 873,405     | |
| fBTC    | 289,296     | |
| fWETH   | 155,385     | |
| Uniswap | 140,673     | |
 

depositing Uniswap LP tokens
- https://etherscan.io/tx/0xa847d681abe98cc092c49e757836d69d937ac71c54032955b1b6a5025c5658e1
- 140,673 gas

depositing 2x Uniswap LP tokens
- https://etherscan.io/tx/0x5b6368182cb1f90bee726cc55cd17ca30ab12d73407b8d0774b64852cd30b350
- 266,749 gas

depositing WBTC, Uniswap
- https://etherscan.io/tx/0x2b10b20f459c42aeea8c8d0929dd265d2fc93ff7308d6ffe8099a53c268ef01f
- 415,361 gas

depositing USDC, Uniswap
- https://etherscan.io/tx/0x5bb88276cad79082fc13b83f7154612287eb34efc00fc1e9748f91f1108e0b75
- 1,040,915

depositing DAI
- https://etherscan.io/tx/0x35af786af05116cd8e1b8e2fcf6c8033fb6457d5e5e43664790c7363fd88048f
- 873,405 gas

depositing USDT, WBTC
- https://etherscan.io/tx/0xc92511827a184b7c34f595a15aa98f7f655d420b0d4142376c4c007bb1be2b57
- 1,139,733 gas

depositing WBTC
- https://etherscan.io/tx/0xd8ff6f3933418fb5f9791e710364afcddb46f5bc9f865f726db0adebaee3742c
- 289,296 gas

depositing WBTC, renBTC
- https://etherscan.io/tx/0x92afa219b7d3a3412435c072ee7a41e43cfc93f87db4932b3ada57ac309a5810
- 563,558 gas

depositing WBTC, WETH
- https://etherscan.io/tx/0xaeb0bf41b7fd949894d2d4061299e0f6fce33e02b897c7ba0143b772b19cfc24
- 415,109 gas

depositing WETH, USDC, Uniswap
- https://etherscan.io/tx/0x8bd9cf2ad14d60d70f78b4fa330a8ceff5ce23ef7410995eb112cd99bfe718f2
- 1,166,720 gas

depositing WETH
- https://etherscan.io/tx/0x0c881a911bd817e6b2137312cb86fdfbf73549ece71b3b6d9551519a80108870
- 155,385 gas

depositing WETH, USDC, USDT, WBTC
- https://etherscan.io/tx/0x9922a23d0caffbc0b0d0af60f2cc7f123335bdb9dddefe1781fb1d939afbd25d
- 2,165,757 gas


# Uniswap
How much Uniswap liquidity is required to reduce the market impact of a $1000 trade to 1%?

At $1.2mm in liquidity, the USDC:fUSDC pair has market impact of 1% on a $6,500 order.

A liquidity of $185k would be needed to keep market impact below 1% on a $1000 trade.



# 0x Limit Orders

Are there bots operating between the trading pairs that ensure that limit orders are filled when they cross with the Uniswap price? This would be helpful, because a small value of Uniswap liquidity could be backed by a small value of limit order liquidity to provide a deeper book while allowing users to trade gas efficiently on Uniswap.

## Check for Bots

Check the USDC:fUSDC for evidence of automated arbitrage.

https://etherscan.io/address/0x4161Fa43eaA1Ac3882aeeD12C5FC05249e533e67

Submitted limit order that can be arbitraged. It was not, so automated arbitrage does not appear to be operating.

## Open Source Bots

Are there open source arbitrage bots?
 - [MakerDAO Market Maker Keeper](https://github.com/makerdao/market-maker-keeper/commit/bb4543559843d3e8d6b1b5979629e7d6f85bb933)
- [MakerDAO Simple Arbitrage Keeper](https://github.com/makerdao/simple-arbitrage-keeper) references Uniswap and 0x but not updated recently
- [Hummingbot](https://hummingbot.io/) says market making or arbitrage
  - [Hummingbot AMM Arb strategy](https://github.com/CoinAlpha/hummingbot/issues/2245)
  
## Capital Efficiency

Can the same ETH fund limit orders to buy multiple fASSETs?

Will the order be removed if it becomes underfunded, or just unfunded?


## Listings

Bamboo Relay has open listing process.
- https://bamboorelay.com/
- https://bamboorelay.com/add-token
- https://0xtracker.com/relayers/bamboo-relay
- I can add any token to Bamboo
- I can do market orders
- I can do limit orders for FARM:WETH, but they don't show up in 1inch
- I get an error when doing FARM:USDC limit orders
- Mesh limit orders for fUSDC don't show up
- possible that only WETH pairs are allowed for unverified tokens?
  - FARM:WETH order on Bamboo does not show up on 1inch
  - FARM:WETH order on 1inch does not show up on Bamboo

1inch listing
- 0.25% taker fee on limit orders
- uses 0xAPI / 0xMesh

Matcha listing
- no listing process described
- orders created on Matcha show up on 1inch
- no maker or taker fee

# Deposit/Withdrawal Abstraction

Make simple example to demonstrate:
- deposit dialog could compare trade quote to the deposit rate
- consider rates and transaction fees
- prompt user to go the less expensive route




