---
title: Harvest Deposit Stakedrop
description: deposit assets into Harvest yield farming strategies, receive FARM
published: true
date: 2021-08-29T20:51:49.845Z
tags: 
editor: markdown
dateCreated: 2020-09-08T03:09:48.188Z
---

> Use the [harvest.finance](https://harvest.finance) site to stake assets. Sending tokens directly to contracts will result in loss of funds! Verify all [token addresses](https://github.com/harvest-finance/harvest) to avoid trading fake tokens.
{.is-warning}

Harvest Finance works by directing assets deposited by users into the yield farming strategies that are currently offering the highest rewards.

To bootstrap deposits into Harvest, holders of Harvest deposit tokens (`fASSETs`) can stake these `fASSETs` to receive a stakedrop of `$FARM` tokens.

> Participants receive their share of revenue from Harvest yield farming in adition to the `$FARM` stakedrop.
{.is-success}


| Dates  | Eligible Assets | Rewards |
|--------|-----------------|---------|
| Week 1, Sept 1-8  | USDC, USDT, DAI | ~12,000 `$FARM` split evenly between the eligible assets|     
| Week 2, Sept 8-15 | USDC, USDT, DAI | ~11,000 `$FARM` split evenly between the eligible assets|     
| Week 3, Sept 15-22 | USDC, USDT, DAI | ~5,000 `$FARM` split evenly between the eligible assets|  

# How To Participate

### 1. Acquire fASSETs

The simplest option is to deposit eligible assets on [harvest.finance](https://harvest.finance). This is the best option for holders who want to acquire >$1000. Deposit transactions cost around 450,000 gas, so it makes sense to leave funds deposited for several weeks. For smaller purchases of amounts <$1000, it's typically more economical to buy `fASSETS` on Uniswap. Selling `fASSETs` on Uniswap is also an inexpensive way for smaller holders to exit Harvest without paying transaction fees to withdraw.


| Deposit    | Receive      | Buy on Uniswap |
|:----------:|:------------:|----------------|
| `USDC`     | `fUSDC`   		|[buy fUSDC](https://app.uniswap.org/#/swap?outputCurrency=0xc3f7ffb5d5869b3ade9448d094d81b0521e8326f)|
| `USDT`     | `fUSDT`   		|[buy fUSDT](https://app.uniswap.org/#/swap?outputCurrency=0xc7ee21406bb581e741fbb8b21f213188433d9f2f)|
| `DAI`			 | `fDAI`				|[buy fDAI](http://uniswap.exchange/swap?outputCurrency=0xe85c8581e60d7cd32bbfd86303d2a4fa6a951dac)|
| `WBTC`	   | `fWBTC`	  	|[buy fWBTC](https://app.uniswap.org/#/swap?outputCurrency=0xc07eb91961662d275e2d285bdc21885a4db136b0)
| `renBTC`   |`frenBTC`   	|[buy frenBTC](https://app.uniswap.org/#/swap?outputCurrency=0xfbe122d0ba3c75e1f7c80bd27613c9f35b81feec)
|`CrvRenWBTC`|`fcrvRenWBTC`	|[buy fcrvRenWBTC](https://app.uniswap.org/#/swap?outputCurrency=0x192e9d29d43db385063799bc239e772c3b6888f3)
| `WETH`  	 |`fWETH`				|[buy fWETH](https://app.uniswap.org/#/swap?outputCurrency=0x8e298734681adbfc41ee5d17ff8b0d6d803e7098)

FARM may also be aquired by depositing `UNI-V2` LP tokens. These tokens must first be aquired by providing liquidity to Uniswap pools of appropriate asset pairs. Upon deposit, you will receive the corresponding `fUNI-V2` token.

| Asset Pair  | 		Receive  | Supply Liquidity on Uniswap |
|:-----------:|:------------:|-----------------------------|
| `USDC` - `WETH` | `FUSDC_WETH_LP`|[Buy USDC-WETH LP][uni-buy-fusdc_weth_lp]
| `USDT` - `WETH` | `FUSDT_WETH_LP`|[Buy USDT-WETH LP][uni-buy-fusdt_weth_lp]
| `DAI` - `WETH` | `FDAI_WETH_LP`|[Buy DAI-WETH LP][uni-buy-fdai_weth_lp]
| `WBTC` - `WETH` | `FWBTC_WETH_LP`|[Buy WBTC-WETH LP][uni-buy-fwbtc_weth_lp]

[uni-buy-fusdc_weth_lp]: https://uniswap.exchange/add/0xa0b86991c6218b36c1d19d4a2e9eb0ce3606eb48/0xC02aaA39b223FE8D0A0e5C4F27eAD9083C756Cc2
[uni-buy-fusdt_weth_lp]: https://app.uniswap.org/#/add/0xdac17f958d2ee523a2206206994597c13d831ec7/0xC02aaA39b223FE8D0A0e5C4F27eAD9083C756Cc2
[uni-buy-fdai_weth_lp]: https://app.uniswap.org/#/add/0x6b175474e89094c44da98b954eedeac495271d0f/0xC02aaA39b223FE8D0A0e5C4F27eAD9083C756Cc2
[uni-buy-fwbtc_weth_lp]: https://app.uniswap.org/#/add/0x2260fac5e5542a773aa44fbcfedf7c193bc2c599/0xC02aaA39b223FE8D0A0e5C4F27eAD9083C756Cc2





Over time, yield farming will cause these fASSETs will grow in value. Simply holding these fASSETs will not entitle you to the FARM stakedrop.

### 2. Deposit fASSETs on [harvest.finance/earn](https://harvest.finance/earn)

Deposit the `fASSETs` using the `EARN` tab. You will immediately begin receiving `$FARM` stakedrop rewards that can be claimed at any time.




# Technical Details

> Contract addresses are provided for technical information only; **do not interact directly with the contracts unless you know what you are doing!**
{.is-warning}

| Token | Address | Underlying | Rewards Staking Pool |
|-------|---------|------------|----------------------|
| FARM  | [0xa0246c9032bC3A600820415aE600c6388619A14D][es-farm]  | [0xa0246c9032bC3A600820415aE600c6388619A14D][es-farm] | [0xae024F29C26D6f71Ec71658B1980189956B0546D][es-pool-farm-week1] |
| fUSDC | [0xc3F7ffb5d5869B3ade9448D094d81B0521e8326f][es-fusdc] | [0xA0b86991c6218b36c1d19D4a2e9Eb0cE3606eB48][es-usdc] | [0xE1f9A3EE001a2EcC906E8de637DBf20BB2d44633][es-pool-fusdc-week1] |
| fUSDT | [0xc7EE21406BB581e741FBb8B21f213188433D9f2F][es-fusdt] | [0xdAC17F958D2ee523a2206206994597C13D831ec7][es-usdt] | [0x5bd997039FFF16F653EF15D1428F2C791519f58d][es-pool-fusdt-week1] |
| fDAI  | [0xe85C8581e60D7Cd32Bbfd86303d2A4FA6a951Dac][es-fdai]  | [0x6B175474E89094C44Da98b954EedeAC495271d0F][es-dai]  | [0xF9E5f9024c2f3f2908A1d0e7272861a767C9484b][es-pool-fdai-week1] |
| fWBTC | [0xc07EB91961662D275E2D285BdC21885A4Db136B0][es-fWBTC] | [0x2260FAC5E5542a773Aa44fBCfeDf7C193bc2C599][es-wbtc] | [0x6291eCe696CB6682a9bb1d42fca4160771b1D7CC][es-pool-fwbtc]|
| frenBTC| [0xfBe122D0ba3c75e1F7C80bd27613c9f35B81FEeC][es-frenbtc]| [0xEB4C2781e4ebA804CE9a9803C67d0893436bB27D][es-renbtc] | [0xCFE1103863F9e7Cf3452Ca8932Eef44d314bf9C5][es-pool-frenbtc]|
|fcrvRenWBTC|[0x192E9d29D43db385063799BC239E772c3b6888F3][es-fcrvrenwbtc]| [0x49849C98ae39Fff122806C06791Fa73784FB3675][es-crvrenwbtc] | [0x5365A2C47b90EE8C9317faC20edC3ce7037384FB][es-pool-fcrvrenwbtc]|
| fWETH	|[0x8e298734681adbfC41ee5d17FF8B0d6d803e7098][es-fweth]  | [0xC02aaA39b223FE8D0A0e5C4F27eAD9083C756Cc2][es-weth] | [0xe11c81b924bb91b44bae19793539054b48158a9d][es-pool-fweth]|
| FUSDC_WETH_LP |[0x63671425ef4D25Ec2b12C7d05DE855C143f16e3B][es-fusdc_weth_lp]|[0xb4e16d0168e52d35cacd2c6185b44281ec28c9dc][es-usdc_weth_lp]|[0xc24da7a6b5adc8771588d58b6109ef52c95a311e][es-pool-fusdc_weth_lp]
| FUSDT_WETH_LP |[0xB19EbFB37A936cCe783142955D39Ca70Aa29D43c][es-fusdt_weth_lp]|[0x0d4a11d5eeaac28ec3f61d100daf4d40471f1852][es-usdt_weth_lp]|[0x9494a3026f28d0b189252428cebbfa52e69608c4][es-pool-fusdt_weth_lp]
| FDAI_WETH_LP |[0x1a9F22b4C385f78650E7874d64e442839Dc32327][es-fdai_weth_lp]|[0xa478c2975ab1ea89e8196811f51a7b7ade33eb11][es-dai_weth_lp]|[0xdc27244311c56ed038e7acf104245ec6a040d07f][es-pool-fdai_weth_lp]
| FWBTC_WETH_LP |[0xb1FeB6ab4EF7d0f41363Da33868e85EB0f3A57EE][es-fwbtc_weth_lp]|[0xbb2b8038a1640196fbe3e38816f3e67cba72d940][es-wbtc_weth_lp]|[0x3bdc3e2572a5540bb1eb1e55bb8749d33fd1a105][es-pool-fwbtc_weth_lp]



[es-farm]: https://etherscan.io/token/0xa0246c9032bC3A600820415aE600c6388619A14D
[es-fusdc]: https://etherscan.io/token/0xc3F7ffb5d5869B3ade9448D094d81B0521e8326f
[es-fusdt]: https://etherscan.io/token/0xc7EE21406BB581e741FBb8B21f213188433D9f2F
[es-fdai]: https://etherscan.io/token/0xe85C8581e60D7Cd32Bbfd86303d2A4FA6a951Dac
[es-fwbtc]: https://etherscan.io/token/0xc07EB91961662D275E2D285BdC21885A4Db136B0
[es-frenbtc]: https://etherscan.io/token/0xfBe122D0ba3c75e1F7C80bd27613c9f35B81FEeC
[es-fcrvrenwbtc]: https://etherscan.io/token/0x192E9d29D43db385063799BC239E772c3b6888F3
[es-fweth]: https://etherscan.io/token/0x8e298734681adbfC41ee5d17FF8B0d6d803e7098
[es-fusdc_weth_lp]: https://etherscan.io/token/0x63671425ef4D25Ec2b12C7d05DE855C143f16e3B
[es-fusdt_weth_lp]: https://etherscan.io/token/0xB19EbFB37A936cCe783142955D39Ca70Aa29D43c
[es-fdai_weth_lp]: https://etherscan.io/token/0x1a9F22b4C385f78650E7874d64e442839Dc32327
[es-fwbtc_weth_lp]: https://etherscan.io/token/0xb1FeB6ab4EF7d0f41363Da33868e85EB0f3A57EE

[es-usdc]: https://etherscan.io/token/0xA0b86991c6218b36c1d19D4a2e9Eb0cE3606eB48
[es-usdt]: https://etherscan.io/token/0xdAC17F958D2ee523a2206206994597C13D831ec7
[es-dai]: https://etherscan.io/token/0x6B175474E89094C44Da98b954EedeAC495271d0F
[es-wbtc]: https://etherscan.io/token/0x2260FAC5E5542a773Aa44fBCfeDf7C193bc2C599
[es-renbtc]: https://etherscan.io/token/0xEB4C2781e4ebA804CE9a9803C67d0893436bB27D
[es-crvrenwbtc]: https://etherscan.io/token/0x49849C98ae39Fff122806C06791Fa73784FB3675
[es-weth]: https://etherscan.io/token/0xC02aaA39b223FE8D0A0e5C4F27eAD9083C756Cc2
[es-usdc_weth_lp]: https://etherscan.io/token/0xb4e16d0168e52d35cacd2c6185b44281ec28c9dc
[es-usdt_weth_lp]: https://etherscan.io/token/0x0d4a11d5eeaac28ec3f61d100daf4d40471f1852
[es-dai_weth_lp]: https://etherscan.io/token/0xa478c2975ab1ea89e8196811f51a7b7ade33eb11
[es-wbtc_weth_lp]: https://etherscan.io/token/0xbb2b8038a1640196fbe3e38816f3e67cba72d940


[es-fdai-contract]: https://etherscan.io/address/0xe85c8581e60d7cd32bbfd86303d2a4fa6a951dac#readContract
[es-fusdt-contract]: https://etherscan.io/address/0xc7ee21406bb581e741fbb8b21f213188433d9f2f#readContract
[es-fusdc-contract]: https://etherscan.io/address/0xc3f7ffb5d5869b3ade9448d094d81b0521e8326f#readContract

[es-pool-farm-week1]: https://etherscan.io/address/0xae024F29C26D6f71Ec71658B1980189956B0546D#readContract
[es-pool-fdai-week1]: https://etherscan.io/address/0xF9E5f9024c2f3f2908A1d0e7272861a767C9484b#readContract
[es-pool-fusdc-week1]: https://etherscan.io/address/0xE1f9A3EE001a2EcC906E8de637DBf20BB2d44633#readContract
[es-pool-fusdt-week1]: https://etherscan.io/address/0x5bd997039FFF16F653EF15D1428F2C791519f58d#readContract
[es-pool-fwbtc]: https://etherscan.io/address/0x6291eCe696CB6682a9bb1d42fca4160771b1D7CC#readContract
[es-pool-frenbtc]: https://etherscan.io/address/0xCFE1103863F9e7Cf3452Ca8932Eef44d314bf9C5#readContract
[es-pool-fcrvrenwbtc]: https://etherscan.io/address/0x5365A2C47b90EE8C9317faC20edC3ce7037384FB#readContract
[es-pool-fweth]: https://etherscan.io/address/0xe11c81b924bb91b44bae19793539054b48158a9d#readContract

[es-pool-fusdc_weth_lp]: https://etherscan.io/address/0xc24da7a6b5adc8771588d58b6109ef52c95a311e
[es-pool-fusdt_weth_lp]: https://etherscan.io/address/0x9494a3026f28d0b189252428cebbfa52e69608c4
[es-pool-fdai_weth_lp]: https://etherscan.io/address/0xdc27244311c56ed038e7acf104245ec6a040d07f
[es-pool-fwbtc_weth_lp]: https://etherscan.io/address/0x3bdc3e2572a5540bb1eb1e55bb8749d33fd1a105

[es-withdraw-buffer]: https://etherscan.io/tx/0x70fddec35fcf1f89fbfff90972be0e04ce0ae8c34abfaf2900e5210fdf86303e
[es-withdraw-nobuffer]: https://etherscan.io/tx/0x959045e3c8fb26a9eeab00e5ebe11fe62012cc7148f4d025c4c7f75ec0bed0bb
[uni-fusdc]: https://app.uniswap.org/#/swap?outputCurrency=0xc3f7ffb5d5869b3ade9448d094d81b0521e8326f










