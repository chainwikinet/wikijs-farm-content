---
title: Make fASSETs liquid
description: 
published: true
date: 2020-10-02T11:11:06.686Z
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

Check the USDC:fUSDC for evidence of automated arbitrage.

https://etherscan.io/address/0x4161Fa43eaA1Ac3882aeeD12C5FC05249e533e67

Submitted limit order that can be arbitraged. It was not, so automated arbitrage does not appear to be operating.

Are there open source arbitrage bots?

# Deposit/Withdrawal Abstraction

Make simple example to demonstrate:
- deposit dialog could compare trade quote to the deposit rate
- consider rates and transaction fees
- prompt user to go the less expensive route




