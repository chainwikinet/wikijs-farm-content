---
title: Contract: FARM Token
description: FARM token contract information and links
published: true
date: 2020-11-12T03:25:57.463Z
tags: 
editor: markdown
dateCreated: 2020-11-11T15:49:59.488Z
---

# FARM Description
**Contract Address**
[0xa0246c9032bC3A600820415aE600c6388619A14D][es-farm]
[Add FARM to Metamask or other supported wallet][wallet-add-farm]

**Contract Purpose**
The FARM token represents ownership in the Harvest platform. FARM can be staked in the Profit Sharing pool to receive a fraction of Harvest's revenue from yield farming and other operations.

# Trading FARM

The primary market for FARM is Uniswap decentralized exchange.

- [Trade FARM on Uniswap][uni-buy-farm]
- [FARM on Coingecko][coingecko-farm] also lists CEX markets
- [FARM on Coinmarketcap][cmc-farm] also lists CEX markets

**FARM:USDC Uniswap Pool**
Most liquidity comes from a FARM:USDC Uniswap pool that Harvest incentivizes.
Pool contract address: [0x514906FC121c7878424a5C928cad1852CC545892][es-pool-farmusdc]

- [FARM:USDC pool - chart][dexvision-farm]
- [FARM:USDC pool - statistics][uni-info-farm]
- [FARM:USDC pool - add liquidity][uni-add-farm]
- [FARM:USDC pool - remove liquidity][uni-remove-farm]

# FARM Token Supply

> Use the `!supply week 50` command in Discord to see supply and emission statistics
{.is-info}


The FARM token became available when Harvest Finance launched on September 1st, 2020. 

The FARM token contract caps the maximum issuance at 5,000,000 FARM. The original intent was to distribute these tokens, roughly linearly, over four years.

On September 27th 2020 the community voted to reduce issuance by 4.45% per week and to cap the issuance at 690,420 FARM.

## Development Funding

FARM is bootstrapped and has no VCs or investors.

Tokens are distributed to protocol users to incentivize deposits and liquidity and to the launch team to incentivize further development.

- 70% to capital and liquidity providers
- 20% to the launch team
- 10% to an Operational Treasury for development and promotion

## Burn Transactions

In week 3, a portion of planned emissions were burned by minting FARM and sending it to a provably unrecoverable address:

- [Operations Burn](https://etherscan.io/tx/0xcfd1378afdab6980a498edeeecccbf1aa6ff4822dc98eb9dcfe1caf47cc17390) (1,485.0108 FARM)
- [Dev Burn](https://etherscan.io/tx/0x455612eb4be5b32eb3662f9acb2b5cb59ad594d28851ad688bf10a8fd545bb30) (2,970.0216 FARM)
- [Capital Provider Burn](https://etherscan.io/tx/0x8c291fe6a2e2f3c56c6df33f197f49bf3f363a4bb93ab050a1a71c85c32ededb) (10,395.0756 FARM)

In subsequent weeks, FARM has not been burned. Instead, issuance has been reduced by minting less FARM to follow the issuance curve agreed upon by the community. Minting is timelocked for 24 hours so that the community can see the minting amount before it occurs.

## Issuance Schedule

| Week | Distributed |% of total supply  | Total Supply | % of total supply
|------|-------------|-----------------|--------------|-------------------------
|  1   | 57,569.1    | 8.34%           | 57,569.1     | 8.34% 
|  2   | 51,676.2    | 6.48%           | 109,245.3    | 15.82%
|  3   | 26,400.3    | 3.82%           | 135,645.3    | 19.64%
|  4   | 24,997.5    | 3.61%           | 160,622.8    | 23.26%
|  5   | 23,555.0    | 3.41%           | 184,177.8    | 26.67%
|  6   | 22,507.3    | 3.26%           | 206,685.6    | 29.93%
|  7   | 21,507.22   | 3.11%           | 228,192.8    | 33.05%
|  8   | 20,551.42   | 2.98%           | 248,744.2    | 36.03%
|  9   | 19,637.46   | 2.84%           | 248,744.2    | 38.87%
|  10  | 18,764.45   | 2.71%           | 248,744.2    | 41.59%
|  11  | 17,930.26   | 2.59%           | 305,076.1    | 44.18%

- Continues until week 208 and a Total Supply of 690,420 FARM tokens.

- After week 5, every week will have a 4.45% reduction from the prior week until week 208 which is exactly 4 years. 

![screen_shot_2020-10-03_at_10.12.12_pm.png](/screen_shot_2020-10-03_at_10.12.12_pm.png)

[cmc-farm]: https://coinmarketcap.com/currencies/harvest-finance/
[coingecko-farm]: https://www.coingecko.com/en/coins/harvest-finance
[es-farm]: https://etherscan.io/token/0xa0246c9032bc3a600820415ae600c6388619a14d
[es-pool-farmusdc]: https://etherscan.io/address/0x514906FC121c7878424a5C928cad1852CC545892
[uni-info-farm]: https://uniswap.info/token/0xa0246c9032bc3a600820415ae600c6388619a14d
[uni-buy-farm]: https://uniswap.exchange/swap?outputCurrency=0xa0246c9032bc3a600820415ae600c6388619a14d
[uni-add-farm]: https://app.uniswap.org/#/add/0xa0246c9032bC3A600820415aE600c6388619A14D/0xA0b86991c6218b36c1d19D4a2e9Eb0cE3606eB48
[uni-remove-farm]: https://app.uniswap.org/#/remove/0xa0246c9032bC3A600820415aE600c6388619A14D/0xA0b86991c6218b36c1d19D4a2e9Eb0cE3606eB48
[dexvision-farm]: https://beta.dex.vision/?ticker=UniswapV2:FARMUSDC-0x514906FC121c7878424a5C928cad1852CC545892&interval=15
[wallet-add-farm]: https://harvestfi.github.io/add-farm
