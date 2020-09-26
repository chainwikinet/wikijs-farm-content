---
title: Add Harvest Yield-Bearing Tokens to CREAM cyUSD
description: 
published: true
date: 2020-09-26T09:49:40.787Z
tags: 
editor: markdown
dateCreated: 2020-09-26T09:45:24.773Z
---

> Thsi is a proposal by Harvest technical contributor and wiki manager, `Silage Pete`
{.is-success}


# Problem To Solve
Harvest has yield earning assets, called `fAssets`, that represent stablecoins and other tokens that have been deposited into Harvest yield farming operations. We would like to make stablecoin fAssets, like fUSDC and fUSDT, tradeable with the underlying USDC and USDT. This would provide an alternative way of entering and exiting Harvest yield farming positions without going through the `fAsset` deposit or withdraw process, which can be expensive for small farmers when the gas price is high.

Uniswap provides poor liquidity for asset pairs that have a similar relative value. We are searching for a better automated market maker solution that can provide more liquidity at a lower cost to Harvest.

# Proposal
We proposes that the yield-bearing stablecoin `fAssets` fUSDC, fUSDT, and fDAI are added to the `cyUSD` automated market maker pool on the CREAM CreamY platform.

This would help make these `fAssets` liquid with the other stablecoins included in `cyUSD`:

- USDT, USDC, TUSD, BUSD
- yCRV, yyCRV, yUSDT, yUSDC, yTUSD
- cUSDT, cUSDC, crUSDT, crUSDC, crBUSD

Adding these Harvest `fAssets` could drive more Harvest user traffic to CreamY.

Harvest and CREAM have collaborated now on several occasions, including the `$FARM`:ETH [80/20 bull pool on CREAM Swap][cream-farmeth] and in the rescue of the `crETH` funds after the issue with the Harvest WETH farming contract. Adding the Harvest `fAssets` to the `cyUSD` pool could deepen this collaboration and open up opportunities in the future to add the Harvest BTC `fAssets` to the `cyBTC` pool and to collaborate in other ways to grow Harvest and CREAM.





# References

Stablecoin `fASSET` contracts:

| Token   | Address | Uniswap | AUM |
|---------|---------|---------|-----|
| [fDAI][add-fdai]    | [0xe85C8581e60D7Cd32Bbfd86303d2A4FA6a951Dac][es-fdai] | [deposit DAI][hf], [buy][uni-buy-fdai], [info][uni-info-fdai] | $6.4mm
| [fUSDC][add-fusdc]   | [0xc3F7ffb5d5869B3ade9448D094d81B0521e8326f][es-fusdc] | [deposit USDC][hf], [buy][uni-buy-fusdc], [info][uni-info-fusdc] | $15.7mm
| [fUSDT][add-fusdt]   | [0xc7EE21406BB581e741FBb8B21f213188433D9f2F][es-fusdt] | [deposit USDT][hf], [buy][uni-buy-fusdt], [info][uni-info-fusdt] | $23.5mm











[cream-farmeth]: https://app.cream.finance/pools/pool/0x655ad905dec61e4fb7d4840a1f450685801511b2

[hf]: https://harvest.finance

[add-farm]: https://harvestfi.github.io/add-farm
[add-fdai]: https://harvestfi.github.io/add-fdai
[add-fusdc]: https://harvestfi.github.io/add-fusdc
[add-fusdt]: https://harvestfi.github.io/add-fusdt
[add-fwbtc]: https://harvestfi.github.io/add-fwbtc
[add-frenbtc]: https://harvestfi.github.io/add-frenbtc
[add-fcrvrenwbtc]: https://harvestfi.github.io/add-fcrvrenwbtc

[es-farm]: https://etherscan.io/token/0xa0246c9032bc3a600820415ae600c6388619a14d
[es-fdai]: https://etherscan.io/token/0xe85c8581e60d7cd32bbfd86303d2a4fa6a951dac
[es-fusdc]: https://etherscan.io/token/0xc3f7ffb5d5869b3ade9448d094d81b0521e8326f
[es-fusdt]: https://etherscan.io/token/0xc7ee21406bb581e741fbb8b21f213188433d9f2f
[es-fwbtc]: https://etherscan.io/token/0xc07eb91961662d275e2d285bdc21885a4db136b0
[es-frenbtc]: https://etherscan.io/token/0xfbe122d0ba3c75e1f7c80bd27613c9f35b81feec
[es-fcrvrenwbtc]: https://etherscan.io/token/0x192E9d29D43db385063799BC239E772c3b6888F3
[es-fweth]: https://etherscan.io/token/0x8e298734681adbfc41ee5d17ff8b0d6d803e7098
[es-fusdc_weth_lp]: https://etherscan.io/token/0x63671425ef4D25Ec2b12C7d05DE855C143f16e3B
[es-fusdt_weth_lp]: https://etherscan.io/token/0xB19EbFB37A936cCe783142955D39Ca70Aa29D43c
[es-fdai_weth_lp]: https://etherscan.io/token/0x1a9F22b4C385f78650E7874d64e442839Dc32327
[es-fwbtc_weth_lp]: https://etherscan.io/token/0xb1FeB6ab4EF7d0f41363Da33868e85EB0f3A57EE

[uni-buy-farm]: https://uniswap.exchange/swap?outputCurrency=0xa0246c9032bc3a600820415ae600c6388619a14d
[uni-buy-fdai]: https://uniswap.exchange/swap?outputCurrency=0xe85c8581e60d7cd32bbfd86303d2a4fa6a951dac
[uni-buy-fusdc]: https://uniswap.exchange/swap?outputCurrency=0xc3f7ffb5d5869b3ade9448d094d81b0521e8326f
[uni-buy-fusdt]: https://uniswap.exchange/swap?outputCurrency=0xc7ee21406bb581e741fbb8b21f213188433d9f2f
[uni-buy-fwbtc]: https://uniswap.exchange/swap?outputCurrency=0xc07eb91961662d275e2d285bdc21885a4db136b0
[uni-buy-frenbtc]: https://uniswap.exchange/swap?outputCurrency=0xfbe122d0ba3c75e1f7c80bd27613c9f35b81feec
[uni-buy-fcrvrenwbtc]: https://uniswap.exchange/swap?outputCurrency=0x192E9d29D43db385063799BC239E772c3b6888F3
[uni-buy-fweth]: https://app.uniswap.org/#/swap?outputCurrency=0x8e298734681adbfc41ee5d17ff8b0d6d803e7098
[uni-buy-fusdc_weth_lp]: https://uniswap.exchange/add/0xa0b86991c6218b36c1d19d4a2e9eb0ce3606eb48/0xC02aaA39b223FE8D0A0e5C4F27eAD9083C756Cc2
[uni-buy-fusdt_weth_lp]: https://app.uniswap.org/#/add/0xdac17f958d2ee523a2206206994597c13d831ec7/0xC02aaA39b223FE8D0A0e5C4F27eAD9083C756Cc2
[uni-buy-fdai_weth_lp]: https://app.uniswap.org/#/add/0x6b175474e89094c44da98b954eedeac495271d0f/0xC02aaA39b223FE8D0A0e5C4F27eAD9083C756Cc2
[uni-buy-fwbtc_weth_lp]: https://app.uniswap.org/#/add/0x2260fac5e5542a773aa44fbcfedf7c193bc2c599/0xC02aaA39b223FE8D0A0e5C4F27eAD9083C756Cc2

[uni-info-farm]: https://uniswap.info/token/0xa0246c9032bc3a600820415ae600c6388619a14d
[uni-info-fdai]: https://uniswap.info/token/0xe85c8581e60d7cd32bbfd86303d2a4fa6a951dac
[uni-info-fusdc]: https://uniswap.info/token/0xc3f7ffb5d5869b3ade9448d094d81b0521e8326f
[uni-info-fusdt]: https://uniswap.info/token/0xc7ee21406bb581e741fbb8b21f213188433d9f2f
[uni-info-fwbtc]: https://uniswap.info/token/0xc07eb91961662d275e2d285bdc21885a4db136b0
[uni-info-frenbtc]: https://uniswap.info/token/0xfbe122d0ba3c75e1f7c80bd27613c9f35b81feec
[uni-info-fcrvrenwbtc]: https://uniswap.info/token/0x192E9d29D43db385063799BC239E772c3b6888F3
[uni-info-fweth]: https://uniswap.info/token/0x8e298734681adbfc41ee5d17ff8b0d6d803e7098
[uni-info-fusdc_weth_lp]: https://uniswap.info/token/0x63671425ef4D25Ec2b12C7d05DE855C143f16e3B
[uni-info-fusdt_weth_lp]: https://uniswap.info/token/0xB19EbFB37A936cCe783142955D39Ca70Aa29D43c
[uni-info-fdai_weth_lp]: https://uniswap.info/token/0x1a9F22b4C385f78650E7874d64e442839Dc32327
[uni-info-fwbtc_weth_lp]: https://uniswap.info/token/0xb1FeB6ab4EF7d0f41363Da33868e85EB0f3A57EE

[es-pool-farm]: https://etherscan.io/address/0xae024F29C26D6f71Ec71658B1980189956B0546D
[es-pool-fdai]: https://etherscan.io/address/0xF9E5f9024c2f3f2908A1d0e7272861a767C9484b
[es-pool-fusdc]: https://etherscan.io/address/0xE1f9A3EE001a2EcC906E8de637DBf20BB2d44633
[es-pool-fusdt]: https://etherscan.io/address/0x5bd997039FFF16F653EF15D1428F2C791519f58d
