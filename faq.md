---
title: Frequently Asked Questions
description: answers to common questions about Harvest Finance
published: true
date: 2020-09-09T06:25:57.980Z
tags: 
editor: markdown
dateCreated: 2020-09-03T23:06:00.060Z
---




# Common Questions

1. How many FARM tokens are there? **[FARM supply is 5,000,000 distributed over 4 years](/supply)**
2. Where can I trade FARM tokens? **[FARM markets on Uniswap and Balancer](/trade)**
3. How do I turn stablecoins into Harvest `fStablecoins` that earn yield farming revenue? **[On the Harvest front page](https://harvest.finance/)**
2. How do I turn `fStablecoin` tokens back into regular stablecoins? **[withdrawal instructions](/stakedrop#removing-tokens-from-farming)**
4. Do FARM tokens get yield farming revenue just be holding them?  **FARM must be deposited in [Profit Sharing](https://harvest.finance/earn)** to earn yield farming revenue.
5. How much yield farming revenue is shared with Profit Sharing stakers? **30% of yield farming revenue.** It is paid out using a seven-day moving average, so for the first week after launch, payouts may be small.  Yield farming revenue depends on the profitability of available yield farming opportunities and the total assets available for farming by Harvest.
6. What happens to the other 70% of of yield farming revenue?  **It is paid out to users that deposit assets to Harvest for farming**.  Over time, holders of Harvest farming deposit tokens—like fDAI, fUSDC, and fUSDT—will receive more of the underlying stablecoins when they withdraw.


# Technical Stuff

1. Is the code open source? **[contracts are](https://github.com/harvest-finance/harvest); frontend UI is not currently** (to slow down clones)
2. Why is the fee to deposit and withdraw stablecoins so high?  In some cases, **[withdrawing must remove stablecoins from yield farming strategies](/stakedrop#removing-tokens-from-farming)**; try coming back later for lower fees.
3. I want to see the 5% of yield farming revenue paid to FARM Profit Share.  **[example yield farming transaction](https://etherscan.io/tx/0xabd90485e1c558a25b1f8a7f04f338bc5d32151aaa72a2468b739dcf5442d07e). [DAI inflows and outflows from the profit share contract](https://etherscan.io/token/0x6b175474e89094c44da98b954eedeac495271d0f?a=0xae024f29c26d6f71ec71658b1980189956b0546d).**
4.  I want to audit the funds that Harvest is using for yield farming. **[coming soon.](/tvl)**
5.  How can I tell that the Harvest fStablecoins are changing in value due to yield farming? Look at the **[fDAI][es-fdai], [fUSDC][es-fusdc], or [fUSDT][es-fusdt] contracts.** The value that converts from fStablecoins to stablecoins is `getPricePerFullShare`. This has the same number of decimals as the underlying stablecoin and will increase over time if yield farming is profitable.
6. How can I help?  Glad you asked.  **[Join Harvest on Discord](/team),** or **[contribute to this wiki!](/contribute)**


[es-fdai]: https://etherscan.io/address/0xe85c8581e60d7cd32bbfd86303d2a4fa6a951dac#readContract
[es-pool-fdai]: https://etherscan.io/address/0xF9E5f9024c2f3f2908A1d0e7272861a767C9484b#readContract
[es-fusdc]: https://etherscan.io/address/0xc3f7ffb5d5869b3ade9448d094d81b0521e8326f#readContract
[es-pool-fusdc]: https://etherscan.io/address/0xE1f9A3EE001a2EcC906E8de637DBf20BB2d44633#readContract
[es-fusdt]: https://etherscan.io/address/0xc7ee21406bb581e741fbb8b21f213188433d9f2f#readContract
[es-pool-fusdt]: https://etherscan.io/address/0x5bd997039FFF16F653EF15D1428F2C791519f58d#readContract

