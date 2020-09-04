---
title: FARM Stake Farming
description: stake tokens and get FARM
published: true
date: 2020-09-04T20:24:11.734Z
tags: 
editor: markdown
---

> Beware of scams! Verify token addresses [on GitHub](https://github.com/harvest-finance/harvest) to ensure that you are trading the correct Harvest Finance tokens!
{.is-warning}

> A community member has created [an illustrated guide to staking and unstaking](https://medium.com/@bbbolongx/the-humble-farmers-handbook-d7101a06d5bf?sk=74f9a5238760afa198312908e5849579)
{.is-info}



# Stake Tokens, Earn FARM

To participate and earn FARM, stake one of several supported assets to receive a share of FARM distributed in the first four years after Harvest Finance launches:

- [Harvest Finance launch announcement](https://medium.com/harvest-finance/the-harvest-finance-project-338c3e5806fc)
- staking started: September 1st, 2020
- staking ends: September 1st, 2024
- [FARM token supply information](/supply)

Wave1 staking can be managed in several places:

- Official launch site: https://harvest.finance/
- Independent third-party sites
- Directly on Etherscan contracts


[Contribute additional information!](/contribute)

# Removing Tokens from Farming

> Gas prices are extremely high.  Use tools like gasnow.org to ensure that you set the gas price high enough or your transaction may take a very long time to confirm.
{.is-info}


For fDAI, fUSDC, and fUSDT, you must first withdraw from the staking rewards contracts.  Then, you can unwrap them back into the underlying DAI, USDC, and USDT.

1. To withdraw from the staking rewards contracts: https://harvest.finance/earn
  - Click on `Unstake & Claim` and then click on the `UNSTAKE & CLAIM` button below to initiate the transaction.
  - Wait for your transaction to confirm, and then you will receive the fToken and FARM rewards.
  
2. To unwrap the fTokens back into the underlying tokens: https://harvest.finance/
  - Put in your balance of the fTokens that you want to exchange.  If you are not sure of your balance, you can add the fTokens as [custom tokens to your wallet](https://metamask.zendesk.com/hc/en-us/articles/360015489031-How-to-View-See-Your-Tokens-in-Metamask) or check it by putting your address into `balanceOf` on the [fDAI][es-fdai], [fUSDC][es-fusdc], or [fUSDT][es-fusdt] token contracts.  If using the Etherscan contracts, note that the balance number returned for fUSDC and fUSDT has six decimal places (so 987654321 = 987.654321 fUSDC) and fDAI has 18.  This should be approximately equal to the amount of DAI, USDC, or USDT that you deposited.  If you try to withdraw a balance that is too high, your wallet should indicate that the transaction will fail.
  - Hit the withdraw button and send the transaction.  If you are withdrawing during a period of heavy withdraws and the Harvest withdraw buffer has been depleted, then your transaction will need to pay to remove your stablecoin from the yield farming strategy.  This will be expensive ([example][es-withdraw-nobuffer] that cost 2,200,000 gas).  If you come back later after more funds have been deposited to Harvest and the withdraw buffer has been replenished, then the fees may be lower ([example][es-withdraw-buffer] that cost 468,000 gas).
  - Wait for your transaction to confirm, and then you will receive your stablecoin.  Your stablecoin will earn interest if the yield farming strategy has been successful, so you may receive more than you put in.


[es-fdai]: https://etherscan.io/address/0xe85c8581e60d7cd32bbfd86303d2a4fa6a951dac#readContract
[es-fusdt]: https://etherscan.io/address/0xc7ee21406bb581e741fbb8b21f213188433d9f2f#readContract
[es-fusdc]: https://etherscan.io/address/0xc3f7ffb5d5869b3ade9448d094d81b0521e8326f#readContract
[es-pool-fdai]: https://etherscan.io/address/0xF9E5f9024c2f3f2908A1d0e7272861a767C9484b#readContract
[es-pool-fusdc]: https://etherscan.io/address/0xE1f9A3EE001a2EcC906E8de637DBf20BB2d44633#readContract
[es-pool-fusdt]: https://etherscan.io/address/0x5bd997039FFF16F653EF15D1428F2C791519f58d#readContract


[es-withdraw-buffer]: https://etherscan.io/tx/0x70fddec35fcf1f89fbfff90972be0e04ce0ae8c34abfaf2900e5210fdf86303e
[es-withdraw-nobuffer]: https://etherscan.io/tx/0x959045e3c8fb26a9eeab00e5ebe11fe62012cc7148f4d025c4c7f75ec0bed0bb

















