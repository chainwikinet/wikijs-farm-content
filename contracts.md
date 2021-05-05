---
title: Harvest Tokens and Contracts
description: Tokens, contracts, and key addresses of the Harvest Finance ecosystem
published: true
date: 2021-05-05T17:56:49.935Z
tags: 
editor: markdown
dateCreated: 2020-11-11T22:03:19.306Z
---

# Deployers, Minters, Treasuries

| Address | Description |
|:---|:---|
| [0xf00dD244228F51547f0563e60bCa65a30FBF5f7f][es-deployer] |Deploys and administers contracts|
| [0xbed04C43E74150794F2ff5b62B4F73820EDaF661][es-harvester] |Executes harvests of farmed rewards|
| [0x284D7200a0Dabb05ee6De698da10d00df164f61d][es-minter] |DelayMinter; announces and executes FARM minting|
| [0xE20c31e3d08027F5AfACe84A3A46B7b3B165053c][es-notifyhelper] |Notify Helper; Sends profitshare emissions daily.
| [0x008671Ca953EC3BAa8C1b9af4623d38789EE2236][es-vwap]|VWAP bot; auto-sells some FARM to pay for things|
| [0x49d71131396F23F0bCE31dE80526D7C025981c4d][es-dev] |Developer fund; receives 20% of minted FARM|
| [0x843002b1D545ef7abB71C716e6179570582faA40][es-ops] |Operations fund; receives 10% of minted FARM|
| [0x252E7E8B9863f81798B1fEF8CfD9741A46De653C][es-ops2]|Operations wallet; Pays piecemeal for content, different contests, listings, mods, builders, sponsorships, audits, council deals, gitcoin, partnerships, tips, app testing, etc.|
|[0x19762b3b0Fe9b4d4Bd16eFA242CD1f3bCD5fa57C](https://etherscan.io/address/0x19762b3b0Fe9b4d4Bd16eFA242CD1f3bCD5fa57C)|Strategic Reserve; It can be used for further incentivizing opportunities such as: market-making, incentivizing LPs, burning, etc. |




# Token Contracts

> Uniswap markets are linked for informational purposes. If the Uniswap market is illiquid, exchange for the underlying by depositing or withdrawing from the vault on [harvest.finance][hf].

| Token   | Address | Description |
|:---|:---|:---|
|FARM|[0xa0246c9032bC3A600820415aE600c6388619A14D][es-farm] | Harvest profit sharing token. [learn more](farm)
|iFARM| [0x1571eD0bed4D987fe2b498DdBaE7DFA19519F651][es-ifarm] | Interest-bearing FARM. You can read a very instructive article [here](https://mbroome02.medium.com/harvest-101-understanding-ifarm-and-its-potential-54d9cfe305e5) credits to "TheCryptoBlog"
|fWETH|[0xFE09e53A81Fe2808bc493ea64319109B5bAa573e][es-fweth]| deposit receipt for Harvest's WETH vault. [learn more](fweth)
|fUni_ETH_DPI|[0x2a32dcBB121D48C106F6d94cf2B4714c0b4Dfe48][es-funi-eth-dpi] | deposit receipt for Harvest's Uniswap ETH:DPI vault. [learn more](funi_weth_dpi)
|--Stablecoins|
|fCRV-HUSD| [0x29780C39164Ebbd62e9DDDE50c151810070140f2][es-fcrvhusd]|deposit receipt for Harvest's Curve HUSD metapool vault. [learn more](fcrvhusd)
|fYCRV| [0x0FE4283e0216F94f5f9750a7a11AC54D3c9C38F3][es-fycrv]| deposit receipt for Harvest's Curve yPool vault. [learn more](fycrv)
|f3CRV| [0x71B9eC42bB3CB40F017D8AD8011BE8e384a95fa5][es-f3crv]| deposit receipt for Harvest's Curve 3pool vault. [learn more](f3crv)
|fcrvComp| [0x998cEb152A42a3EaC1f555B1E911642BeBf00faD][es-fcrvcomp] | deposit receipt for Harvest's Curve BUSD vault. [learn more](fcrvcomp)
|fBUSD| [0x4b1cBD6F6D8676AcE5E412C78B7a59b4A1bbb68a][es-fbusd]| deposit receipt for Harvest's Curve BUSD vault. [learn more](fbusd)
|fUSDN| [0x683E683fBE6Cf9b635539712c999f3B3EdCB8664][es-fusdn]| deposit receipt for Harvest's Curve USDN vault. [learn more](fusdn)
|fUSDC| [0xf0358e8c3CD5Fa238a29301d0bEa3D63A17bEdBE][es-fusdc] | deposit receipt for Harvest's USDC vault. [learn more](fusdc)
|fUSDT| [0x053c80eA73Dc6941F518a68E2FC52Ac45BDE7c9C][es-fusdt] | deposit receipt for Harvest's USDT vault. [learn more](fusdt)
|fTUSD| [0x7674622c63Bee7F46E86a4A5A18976693D54441b][es-ftusd] | deposit receipt for Harvest's TUSD vault. [learn more](ftusd)
|fDAI| [0xab7FA2B2985BCcfC13c6D86b1D5A17486ab1e04C][es-fdai] | deposit receipt for Harvest's DAI vault. [learn more](fdai)
|--BTC|
|fCRV-HBTC | [0xCC775989e76ab386E9253df5B0c0b473E22102E2][es-fhbtc]| deposit receipt for Harvest's Curve HBTC metapool vault. [learn more](frenbtc)
|fcrvTBTC| [0x640704D106E79e105FDA424f05467F005418F1B5][es-fcrvtbtc] |deposit receipt for Harvest's Curve TBTC metapool vault. [learn more](fcrvtbtc)
|fcrvRenWBTC | [0x9aA8F427A17d6B0d91B6262989EdC7D45d6aEdf8][es-fcrvrenwbtc] | deposit receipt for Harvest's Curve RenWBTC pool vault. [learn more](fcrvrenwbtc)
|fWBTC   | [0x5d9d25c7C457dD82fc8668FFC6B9746b674d4EcB][es-fwbtc] | deposit receipt for Harvest's wBTC vault. [learn more](fwbtc)
|frenBTC | [0xC391d1b08c1403313B0c28D47202DFDA015633C4][es-frenbtc] | deposit receipt for Harvest's renBTC vault. [learn more](frenbtc)
|--Sushiswap|
|fSLP_WETH_DAI| [0x203E97aa6eB65A1A02d9E80083414058303f241E][es-fslp-weth-dai]|deposit receipt for Harvest's Sushiswap WETH:DAI vault. [learn more](fslp_weth_dai)
|fSLP_WETH_USDC| [0x01bd09A1124960d9bE04b638b142Df9DF942b04a][es-fslp-weth-usdc]|deposit receipt for Harvest's Sushiswap WETH:USDC vault. [learn more](fslp_weth_usdc)
|fSLP_WETH_USDT| [0x64035b583c8c694627A199243E863Bb33be60745][es-fslp-weth-usdt]|deposit receipt for Harvest's Sushiswap WETH:USDT vault. [learn more](fslp_weth_usdt)
|fSLP_WETH_WBTC| [0x5C0A3F55AAC52AA320Ff5F280E77517cbAF85524][es-fslp-weth-wbtc]|deposit receipt for Harvest's Sushiswap WETH:WBTC vault. [learn more](fslp_weth_wbtc)
|fSLP_WBTC_TBTC | [0xF553E1f826f42716cDFe02bde5ee76b2a52fc7EB][es-fslp] | deposit receipt for Harvest's Sushiswap WBTC:TBTC vault. [learn more](fslp_wbtc_tbtc)
|--Uniswap|
|fDAI_WETH_LP|[	0x307E2752e8b8a9C29005001Be66B1c012CA9CDB7][es-fdai_weth_lp]|deposit receipt for Harvest's Uniswap DAI:ETH vault. [learn more](funi_dai_eth)
|fUSDC_WETH_LP|[0xA79a083FDD87F73c2f983c5551EC974685D6bb36][es-fusdc_weth_lp]|deposit receipt for Harvest's Uniswap USDC:ETH vault. [learn more](funi_usdc_eth)
|fUSDT_WETH_LP|[0x7DDc3ffF0612E75Ea5ddC0d6Bd4e268f70362Cff][es-fusdt_weth_lp]|deposit receipt for Harvest's Uniswap USDT:ETH vault. [learn more](funi_usdt_eth)
|fWBTC_WETH_LP|[0x01112a60f427205dcA6E229425306923c3Cc2073][es-fwbtc_weth_lp]|deposit receipt for Harvest's Uniswap WBTC:ETH vault. [learn more](funi_wbtc_eth)







# Uniswap Pools

| Token   | Address | Links |
|:---|:---|:---|
| FARM_ETH_LP | [0x6555c79a8829b793F332f1535B0eFB1fE4C11958](https://etherscan.io/address/0x6555c79a8829b793F332f1535B0eFB1fE4C11958) |incentivized; [learn more](contracts/farm)


# Reward Pools



| Contract | Description |
|:---|:---|
| [0xa239d5B5BF3deeB53E6e19635E82EdCE515D32F4][es-fusdc-auto] | [experimental] automatically stakes fUSDC rewards to Profit Sharing |

[es-deployer]: https://etherscan.io/address/0xf00dd244228f51547f0563e60bca65a30fbf5f7f
[es-minter]: https://etherscan.io/address/0x284d7200a0dabb05ee6de698da10d00df164f61d
[es-dev]: https://etherscan.io/address/0x49d71131396f23f0bce31de80526d7c025981c4d
[es-notifyhelper]: https://etherscan.io/address/0xe20c31e3d08027f5aface84a3a46b7b3b165053c
[es-ops]: https://etherscan.io/address/0x843002b1d545ef7abb71c716e6179570582faa40
[es-ops2]: https://etherscan.io/address/0x252E7E8B9863f81798B1fEF8CfD9741A46De653C
[es-vwap]: https://etherscan.io/address/0x008671ca953ec3baa8c1b9af4623d38789ee2236
[es-harvester]: https://etherscan.io/address/0xbed04c43e74150794f2ff5b62b4f73820edaf661

[hf]: https://harvest.finance

[add-farm]: https://harvestfi.github.io/add-farm
[add-fdai]: https://harvestfi.github.io/add-fdai
[add-fusdc]: https://harvestfi.github.io/add-fusdc
[add-fusdt]: https://harvestfi.github.io/add-fusdt
[add-fwbtc]: https://harvestfi.github.io/add-fwbtc
[add-frenbtc]: https://harvestfi.github.io/add-frenbtc
[add-fcrvrenwbtc]: https://harvestfi.github.io/add-fcrvrenwbtc


[es-fweth]: https://etherscan.io/token/0xFE09e53A81Fe2808bc493ea64319109B5bAa573e
[es-farm]: https://etherscan.io/token/0xa0246c9032bc3a600820415ae600c6388619a14d
[es-ifarm]: https://etherscan.io/token/0x1571ed0bed4d987fe2b498ddbae7dfa19519f651
[es-farm_usdc_lp]: https://etherscan.io/address/0x514906FC121c7878424a5C928cad1852CC545892
[es-fdai]: https://etherscan.io/token/0xab7fa2b2985bccfc13c6d86b1d5a17486ab1e04c
[es-fusdc]: https://etherscan.io/token/0xf0358e8c3CD5Fa238a29301d0bEa3D63A17bEdBE
[es-fusdt]: https://etherscan.io/token/0x053c80eA73Dc6941F518a68E2FC52Ac45BDE7c9C
[es-ftusd]: https://etherscan.io/token/0x7674622c63Bee7F46E86a4A5A18976693D54441b
[es-fwbtc]: https://etherscan.io/token/0x5d9d25c7C457dD82fc8668FFC6B9746b674d4EcB
[es-fcrvtbtc]: https://etherscan.io/token/0x640704D106E79e105FDA424f05467F005418F1B5
[es-fcrvhusd]: https://etherscan.io/token/0x29780C39164Ebbd62e9DDDE50c151810070140f2
[es-f3crv]: https://etherscan.io/token/0x71B9eC42bB3CB40F017D8AD8011BE8e384a95fa5
[es-fycrv]: https://etherscan.io/token/0x0FE4283e0216F94f5f9750a7a11AC54D3c9C38F3
[es-fusdn]: https://etherscan.io/token/0x683e683fbe6cf9b635539712c999f3b3edcb8664
[es-fbusd]: https://etherscan.io/token/0x4b1cbd6f6d8676ace5e412c78b7a59b4a1bbb68a
[es-fcrvcomp]: https://etherscan.io/token/0x998cEb152A42a3EaC1f555B1E911642BeBf00faD
[es-frenbtc]: https://etherscan.io/token/0xC391d1b08c1403313B0c28D47202DFDA015633C4
[es-fcrvrenwbtc]: https://etherscan.io/token/0x9aA8F427A17d6B0d91B6262989EdC7D45d6aEdf8
[es-fhbtc]: https://etherscan.io/token/0xCC775989e76ab386E9253df5B0c0b473E22102E2
[es-fusdc_weth_lp]: https://etherscan.io/token/0xA79a083FDD87F73c2f983c5551EC974685D6bb36
[es-fusdt_weth_lp]: https://etherscan.io/token/0x7DDc3ffF0612E75Ea5ddC0d6Bd4e268f70362Cff
[es-fdai_weth_lp]: https://etherscan.io/token/0x307E2752e8b8a9C29005001Be66B1c012CA9CDB7
[es-fwbtc_weth_lp]: https://etherscan.io/token/0x01112a60f427205dcA6E229425306923c3Cc2073
[es-funi-eth-dpi]: https://etherscan.io/token/0x2a32dcBB121D48C106F6d94cf2B4714c0b4Dfe48
[es-fslp]: https://etherscan.io/token/0xF553E1f826f42716cDFe02bde5ee76b2a52fc7EB
[es-fslp-weth-dai]: https://etherscan.io/token/0x203E97aa6eB65A1A02d9E80083414058303f241E
[es-fslp-weth-usdc]: https://etherscan.io/token/0x01bd09a1124960d9be04b638b142df9df942b04a
[es-fslp-weth-usdt]: https://etherscan.io/token/0x64035b583c8c694627a199243e863bb33be60745
[es-fslp-weth-wbtc]: https://etherscan.io/token/0x5c0a3f55aac52aa320ff5f280e77517cbaf85524



[uni-buy-farm]: https://uniswap.exchange/swap?outputCurrency=0xa0246c9032bc3a600820415ae600c6388619a14d
[uni-buy_farm_usdc]: https://app.uniswap.org/#/add/0xa0246c9032bc3a600820415ae600c6388619a14d/0xa0b86991c6218b36c1d19d4a2e9eb0ce3606eb48
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

[es-fusdc-auto]: https://etherscan.io/address/0xa239d5b5bf3deeb53e6e19635e82edce515d32f4