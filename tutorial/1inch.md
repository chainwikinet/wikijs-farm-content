---
title: Trade fASSETs on 1inch
description: may be less expensive than depositing and withdrawing for small traders
published: true
date: 2020-09-30T13:52:08.171Z
tags: 
editor: markdown
dateCreated: 2020-09-30T13:42:27.357Z
---

# Problem To Solve

> If you are depositing an amount in excess of $1000, depositing directly into Harvest will probably give a better price than trading.
{.is-info}


Withdrawing assets from Harvest can sometimes be expensive, especially when gas prices are high.

If you are withdrawing during a period of heavy withdraws and the Harvest withdraw buffer has been depleted, then your transaction will need to pay to remove your stablecoin from the yield farming strategy.  This will be expensive ([example][es-withdraw-nobuffer] that cost 2,200,000 gas).  If you come back later after more funds have been deposited to Harvest and the withdraw buffer has been replenished, then the fees may be lower ([example][es-withdraw-buffer] that cost 468,000 gas).

**By trading fASSETs on 1inch, you may pay lower fees than depositing or withdrawing directly**.

# How To Do It

> Trades may not always be available on 1inch. This is a test run with small limit orders between the stablecoin pairs. If it is successful, we may add the BTC pairs and larger orders. Please ask questions in the #🔄trading channel on Discord.
{.is-info}

**1. Visit 1inch exchange https://1inch.exchange/**

**2. Manually add the Harvest fASSET tokens on 1inch**

![1inch-custom.png](/1inch-custom.png)

The fASSET token addresses are available on [the trade page](/trade).

**3. For best prices, swap between ASSET and fASSET**

For instance if you want fUSDT, buy with USDT.

![1inch-trade.png](/1inch-trade.png)

To check that the rate your are receiving is reasonable, check the trade quote against the fASSET share price using the `!vault` command in Harvest Discord.

1inch trade quote for USDT/fUSDT:

![1inch-rate.png](/1inch-rate.png)

Share price from `!vault fusdt` in Discord:

![discordbot-vault.png](/discordbot-vault.png)

- trade quote: **1.036 USDT per fUSDT**
- share price: **1.028 USDT per fUSDT**

The trade quote is within 1% of the share price that you would get from depositing, so this is a good price.

# Future Plans

We hope to make these fASSET trades available on more platforms in the future, including DeBank and Paradex.


[es-withdraw-buffer]: https://etherscan.io/tx/0x70fddec35fcf1f89fbfff90972be0e04ce0ae8c34abfaf2900e5210fdf86303e
[es-withdraw-nobuffer]: https://etherscan.io/tx/0x959045e3c8fb26a9eeab00e5ebe11fe62012cc7148f4d025c4c7f75ec0bed0bb

