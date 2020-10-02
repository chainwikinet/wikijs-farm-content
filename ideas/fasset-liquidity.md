---
title: Make fASSETs liquid
description: 
published: true
date: 2020-10-02T13:05:48.715Z
tags: 
editor: markdown
dateCreated: 2020-10-02T11:09:52.564Z
---

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




