---
title: Why is my DAI balance going down?
description: 
published: true
date: 2021-01-28T13:48:49.853Z
tags: 
editor: markdown
dateCreated: 2020-10-13T10:08:29.780Z
---


# Why is my DAI balance going down?

> TL;DR. It is mainly due to the fact that DAI price is volatile for a stablecoin. This, combined with the Curve dynamics and the socialized price of down exits creates the volatility in your DAI balance. Nonetheless, you'll probably make money in the long run, but it'll be a bit more volatile than the other stablecoins. 
{.is-info}


**If you have questions about DAI deposits it's a good idea to read this thorough answer by Brandon | Radar. :**

ADMIN why is my DAI balance going down HELP ADMIN
There are several reasons why your DAI deposit balance may drop even though harvesting is going fine.

1. DAI is not too stable
The DAI price isn't stable at $1. Hasn't ever been, never will be.
When you deposit into the current Harvest stablecoin farming strategy, your stablecoin is exchanged for a receipt, yCRV, that is redeemable for approximately the dollar value in stablecoins that you deposited.  If you deposit when DAI is trading at $1.00 and then the DAI price rises to $1.02 (which it does all the time https://www.coingecko.com/en/coins/dai), your dollar value stays approximately the same so your DAI balance will decrease by about 2%.  This also works in the reverse direction and can cause your DAI balance to increase if the price of DAI decreases.
2. DAI does not work super well in Curve
Curve assumes that the stablecoins in a pool are actually stablecoins.  This is a problem for DAI.
Curve has much better liquidity for stablecoins than other AMMs like Uniswap.  This is because Curve uses a market making strategy that is closer to a constant price market maker than it is to the constant product market maker used by Uniswap.  What this means is that Curve will continue to trade the stablecoins in the pool more-or-less 1:1 right up until the pool is almost entirely depleted of one of the stablecoins.  If a stablecoin rises to, say, $1.01, Curve will trade most of it away for the other stablecoins in the pool that are still trading at $1.  The opposite is also true: if a stablecoin price falls below $1, Curve will trade away almost everything else in the pool for the lower-priced stablecoin.  What this means for DAI, which chronically trades around $1.01-1.02, is that Curve is usually nearly out of stock of DAI.

Here is the current state of the Curve yPool (from https://www.curve.fi/iearn/):
DAI: 23,162,695.77 (5.28%)
USDC: 136,200,606.19 (31.07%)
USDT: 119,753,642.32 (27.32%)
TUSD: 159,277,383.82 (36.33%)
DAI+USDC+USDT+TUSD: 438,394,328.09

As above: you are not holding DAI when you deposit into the DAI vault, you are actually holding the yCRV receipt which is redeemable for whatever Curve happens to have in stock.  But, your Vault receipt also demands DAI when you withdrawal!  Curve is an AMM that sets prices based on availability, so if there is a smaller fraction of DAI in Curve than when you deposited, then you will be charged a higher price for that DAI and will receive less DAI per unit receipt.  This also works in reverse: if the availability of DAI in the pool increases from the time that you deposited, you could receive a better price and your DAI balance may increase.

3. The current vaults socialize the price of down exits
When a user exits into a market headwind on Curve, the user eats some of the loss and the rest of the loss is spread over all of the money remaining in the vault. 

This is a design choice that Harvest made for how the single-asset vaults operate. The design choice will be updated in the Vault upgrade that will also include the timelocked proxy and strategy splitting. Desocializing losses will prevent others' actions from negatively affecting your balance—basically, fAsset value may increase or decrease on deposits, will always increase on harvests, and won't decrease on withdrawals.  Could this have negative side effects for single asset vaults under certain scenarios?  I don't know, so hopefully Harvest is looking carefully at that before implementing.

How big of an impact does this effect have on the balances of a particular vault today?  I don't know, but the data is all on-chain if you want to do the math and partition all of the gains and losses yourself.

4. What Do?
The DAI vault experiences all of these effects much more strongly than the other vaults, so just swap DAI for something else and pick a different one.  Pure-LP-position asset-agnostic vaults like CRVRENWBTC allow advanced users to fully control the timing and market impact of AMM entry and exit.  An asset-agnostic fyCRV vault could enable this as well for the stablecoins and would be a great addition to the v2 vault layout.
5. ADMIN I'm still mad about this!
If the slight fluctuations in the balance is too much to handle, and you find yourself refreshing the screen a lot, maybe withdrawing is the best option
6. Bonus Irony
Because of gain socialization on deposit, the fDAI vault has outperformed all of the other stablecoin vaults by 2-3x.  So if you want to play stupid DAI games and win stupid DAI prizes, you could play your entry and exit right and make more money in this vault than anywhere else.