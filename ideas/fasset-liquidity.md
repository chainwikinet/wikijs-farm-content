---
title: Make fASSETs liquid
description: 
published: true
date: 2020-10-04T13:59:09.921Z
tags: 
editor: markdown
dateCreated: 2020-10-02T11:09:52.564Z
---

# Deposit/Withdrawal Abstraction

If there is fAsset liquidity availale, the website can automatically compare the rates and costs of withdrawing or depositing with the rates and costs of trading in or out of the fAsset. **It can automatically direct users along the route that gives the best deal.**

Make simple example app to demonstrate:
- deposit dialog could compare trade quote to the deposit rate
- consider rates and transaction fees
- prompt user to go the less expensive route


# Vault Deposit/Withdrawal Costs

Investigating how much it costs to deposit and withdraw from vaults and strategies. This can help determine where the ability to trade fAssets could save the most in transaction fees.

| Asset   | Deposit Gas | Withdraw Gas        |
|---------|-------------|---------------------|
| fSTABLE | 873,405     | 482,391 to 2,210,864|
| fBTC    | 289,296     | 160,928 to 769,901  |
| fWETH   | 155,385     | 64,226 to 2,157,646 |
| Uniswap | 140,673     | 96,904 to 216,015   |
 



## Withdraw TXs
 
withdraw WBTC from Strategy
- https://etherscan.io/tx/0x1e9c6e42ffc0b49d2aa6726104b74406974053e33aa62866286a07ee674552c4
- 769,901 gas

withdraw WBTC from Vault
- https://etherscan.io/tx/0x6650df8ddc170de1043e38963006e3eae3aa3c1c6d83b09f9cc680f4b8d3e778
- 160,928 gas

withdraw WETH from Strategy
- https://etherscan.io/tx/0xa7ead29fd4cc5279780e44632139ff7522790624e1c29c6340ea0adf9a101f20
- 2,157,646 gas

withdraw WETH from Vault
- https://etherscan.io/tx/0xe6d3fff6d59ee1891143b851dbf89975e1fb6782b4277b5626f7be0f5c000be5
- 64,226 gas

withdraw USDC from Vault
- https://etherscan.io/tx/0xc2f2fe17cef2c35a64e9ad666823f33428249b587f150ecd9af6447bdd05ae86
- 482,391 gas

withdraw USDC from Strategy
- https://etherscan.io/tx/0x35ae13f29334a67e22323f079d69a20c62b0a0ca0c4c0bccc5ac36445a6e642a
- 2,210,864 gas

withdraw Uniswap LP from Vault
- https://etherscan.io/tx/0xfa318b03fd62f066ee2c1140989c484a800f3fd6f0f913de0d95ee9e7160b506
- 96,904 gas

withdraw Uniswap LP from Strategy
- https://etherscan.io/tx/0x9dbd2aa564f2cba2ebab8691e4858c6374f2ea46547a180519fb108bc6f1eec9
- 216,015 gas


## Deposit TXs

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



