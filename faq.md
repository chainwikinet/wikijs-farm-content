---
title: Frequently Asked Questions
description: answers to common questions about Harvest Finance
published: true
date: 2021-02-18T11:14:22.382Z
tags: 
editor: markdown
dateCreated: 2020-09-03T23:06:00.060Z
---




# Common Questions

1. Should I interact with the contract directly? **NO**, please use the website and ask for help in [#support](/en/https://discord.gg/AsRh9mCd).
1. Is Harvest audited? **[Yes](/security)**
1. Who is the Harvest team? **The Harvest Finance launch team is anonymous**
1. How is APY / APR calculated for the Pools? [**APY formulas**](/en/calculationAPY) 
1. How many FARM tokens are there? [**FARM tokens are capped at 690,420 tokens minted over a 4-year period**](/en/supply)
1. Is there a fAssets shareprice charts? [**Yes**](https://harvestcharts.on.fleek.co//) (It is created by a community member)
1. Why does my fAsset(fUSDT/fUSDC/etc...) conversion rate go down?) [**Check Here**](/en/fAsset-flucttuation)
1. Why is my DAI balance going down? [**Thorough explanation by Brandon | RADAR.**](/en/DAI)
2. Where can I trade FARM tokens? **[FARM markets on Uniswap](/trade)**
3. How do I turn tokens into Harvest `fTokens` that earn yield farming revenue? **[on the Harvest front page](/en/https://harvest.finance/)** or by **[trading on Uniswap](/trade)**
2. How do I turn `fTokens` tokens back into regular tokens? **[withdrawal instructions](/stakedrop#removing-tokens-from-farming)**
4. Do FARM tokens get yield farming revenue just be holding them?  **FARM must be deposited in [Profit Sharing][hf-earn]** to earn yield farming revenue.
5. How much yield farming revenue is shared with Profit Sharing stakers? **30% of yield farming revenue.** It is paid out using a seven-day moving average, so for the first week after launch, payouts may be small.  Yield farming revenue depends on the profitability of available yield farming opportunities and the total assets available for farming by Harvest.
6. What happens to the other 70% of yield farming revenue?  **It is paid out to users that deposit assets to Harvest for farming**.  Over time, holders of Harvest farming fTokens will receive more of the underlying tokens when they withdraw.

# Technical Stuff

1. Is the code open source? **[contracts are](https://github.com/harvest-finance/harvest); frontend UI is not currently** (to slow down clones)
2. Why is the fee to deposit and withdraw stablecoins so high?  In some cases, **[withdrawing must remove stablecoins from yield farming strategies](/stakedrop#removing-tokens-from-farming)**; come back later for lower fees, or **[trade on Uniswap](/trade)**
3. I want to see the yield farming revenue paid to FARM Profit Share.  **[example yield farming transaction][es-harvest]. [DAI inflows and outflows from the profit share contract][es-profitshare].**
4.  I want to audit the funds that Harvest is using for yield farming. **[coming soon.](/tvl)**
5.  How can I tell that the Harvest fStablecoins are changing in value due to yield farming? Look at the **[fDAI][es-fdai], [fUSDC][es-fusdc], or [fUSDT][es-fusdt] contracts.** The value that converts from fTokens to tokens is `getPricePerFullShare`. This has the same number of decimals as the underlying stablecoin and will increase over time if yield farming is profitable.
6. Are there timelocks? **Yes, 12 hours.**
7. How can I help?  Glad you asked.  **[Join Harvest on Discord][hf-discord],** or **[contribute to this wiki!](/contribute)**


# Risks

> Deposit funds at your own risk. Problems with Harvest or with protocols that Harvest integrates with may result in partial or total loss of funds. Stated yields aren't guaranteed. Do your own research and don't deposit more than you can afford to lose.
{.is-warning}

## Smart Contract Failures
Harvest's smart contracts are open source, readable, and include tests. They are not a direct fork of an existing contract system. [Audits are pending](/security), but a successful audit does not guarantee that a new or existing Harvest strategy will hit APY targets or avoid hacks of Harvest or contracts that Harvest integrates with (Curve, Swerve, Balancer, Uniswap, Cream, Compound, &etc).

## Composability Risks
Harvest contracts handle many different assets and interact with many other contracts. This contract composability gives Harvest its value, but interacting with multiple contracts creates risk if there is a failure in one of the contracts.  Harvest makes a best effort to audit and evaluate the risks of the contracts that Harvest farms, but deposits are subject to the risks inherent to each strategy. Look into the strategies employed by the vaults that you deposit into to get acquainted with the risks.

## Asset Risks

> Stablecoins aren't necessarily stable! Stablecoins and synthetics may depeg from the target price and you may lose value. Carefully evaluate the risks of all of your so-called "stable" assets!
{.is-danger}

Harvest interacts with many stablecoins and synthetic representations of other assets like Bitcoin. These assets may rely on collateralization with other digital assets (DAI, sUSD, sBTC) or may be non-bearer liabilities that are only redeemable for the underlying asset with a centralized third party (USDC, USDT, wBTC). If a non-bearer asset is blacklisted by the issuer or a synthetic asset becomes undercollateralized, your positions that hold or interact with these assets may lose value or even become worthless.

## Automated Market Maker Risks

> Harvest uses yield farming strategies that have exposure to liquidity pools. Providing liquidity on an AMM is an advanced topic and there are several ways to lose money. Proceed at your own risk!
{.is-warning}

Impermanent loss (aka Divergence Loss) is associated with providing assets to a liquidity pool. Liquidity pools are used in Decentralized Exchanges such as Uniswap, Curve, and Balancer in order to create money markets and enable traders to buy and sell the assets that the pools support.

If you deposit funds to provide liquidity in an automated market maker, you may lose some or all of the value you deposit if there is a change in the relative values of the assets in the automated market maker. If just one of the assets in the pool loses value or becomes worthless, your entire position in the pool, regardless of which assets you originally provided when you entered the pool, may lose value or become worthless.

If you provide liquidity to a pool and one of the assets *gains* in value relative to the others in the pool, you may not make as much money as you would have, had you held these assets instead of depositing them in the pool. It is critical to understand the math behind impermanent loss before providing liquidity!

Many yield farming strategies, including the yield farming strategies employed by Harvest, provide incentives for providing liquidity in an AMM. **These incentives do not guarantee that providing liquidity will be profitable for you.**

Further reading on impermanent loss and AMM risks:

- [Beginner’s Guide to (Getting Rekt by) Impermanent Loss](https://blog.bancor.network/beginners-guide-to-getting-rekt-by-impermanent-loss-7c9510cb2f22)
- [Uniswap: a good deal for liquidity providers?](https://medium.com/@pintail/uniswap-a-good-deal-for-liquidity-providers-104c0b6816f2)
- [Calculating Value, Impermanent Loss and Slippage for Balancer Pools](https://medium.com/balancer-protocol/calculating-value-impermanent-loss-and-slippage-for-balancer-pools-4371a21f1a86)
- [What Is IMPERMANENT LOSS? DEFI Explained - Uniswap, Curve, Balancer, Bancor](https://www.youtube.com/watch?v=8XJ1MSTEuU0)

## Liquidity and Market Impact

> Many new DeFi assets have extremely poor liquidity and you may experience significant losses due to market impact when buying or selling. Liquidity may disappear when prices are changing rapidly, and you may be stranded in a position and unable to sell. Carefully evaluate the liquidity profiles of the assets that you hold!
{.is-warning}

Market impact (aka price impact) occurs when a trade is large enough to change the price of the assets that are traded on the exchange where they are being traded. Market impact can increase when liquidity decreases during periods of high volatility.

Some Harvest strategies may involve entering and exiting automated market maker LP positions on Curve, Swerve, Balancer, Uniswap from a single asset supported by the AMM. If price volatility reduces the liquidity of the asset you have deposited, **you may experience market impact losses when you try to withdraw.** These losses may appear as a reduction in your deposited balance. If the liquidity situation for your asset improves, your displayed balance may also improve.

[hf]: https://harvest.finance/earn
[hf-earn]: https://harvest.finance/earn
[hf-discord]: https://discord.gg/R5SeTVR
[es-fdai]: https://etherscan.io/address/0xe85c8581e60d7cd32bbfd86303d2a4fa6a951dac#readContract
[es-pool-fdai]: https://etherscan.io/address/0xF9E5f9024c2f3f2908A1d0e7272861a767C9484b#readContract
[es-fusdc]: https://etherscan.io/address/0xc3f7ffb5d5869b3ade9448d094d81b0521e8326f#readContract
[es-pool-fusdc]: https://etherscan.io/address/0xE1f9A3EE001a2EcC906E8de637DBf20BB2d44633#readContract
[es-fusdt]: https://etherscan.io/address/0xc7ee21406bb581e741fbb8b21f213188433d9f2f#readContract
[es-pool-fusdt]: https://etherscan.io/address/0x5bd997039FFF16F653EF15D1428F2C791519f58d#readContract
[es-profitshare]: https://etherscan.io/token/0x6b175474e89094c44da98b954eedeac495271d0f?a=0xae024f29c26d6f71ec71658b1980189956b0546d
[es-harvest]: https://etherscan.io/tx/0xabd90485e1c558a25b1f8a7f04f338bc5d32151aaa72a2468b739dcf5442d07e
