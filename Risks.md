---
title: Risks
description: Risks of using Harvest Finance
published: true
date: 2020-09-12T21:15:03.929Z
tags: risks
editor: markdown
dateCreated: 2020-09-12T19:15:59.710Z
---


> We at Harvest Finance take security and safety as a Top Priority.
{.is-success}


> Depositing funds doesn’t come without its fair share of risk. Please, take your time to understand the risks involved. The information below is not compiled by a financial professional, thus Do Your Own Research and never invest more than you can afford to lose. 
{.is-warning}




# **Smart Contract**
The talented engineers of Harvest Finance have created a smart contract that is an object of envy by many in the industry. Not only they built a solid, clean, and easy to understand smart contract, but they also built it from the ground up. **Our smart contract is not a fork**. In order to ensure the quality and security even more **we have commissioned 3 top notch external security companies to audit our smart contract**. Check the [security page](/en/https://farm.chainwiki.dev/e/en/security) for more information on who is commissioned and deadlines. 

While we are still waiting for full audits, we have a preliminary confirmation from PeckShield Inc stating that there are no serious business logic issues with our contract:

> [PeckShield Inc. @peckshield (2020-09-07)](https://twitter.com/peckshield/status/1303012731197382656
)
Last few days PeckShield has done a sanity check of Harvest Finance smart contracts, so far no serious business logic issue was found.  In the next several weeks, we will conduct a full security audit of the smart contracts. [@harvest_finance](https://twitter.com/harvest_finance) #DeFiFarming

**Why is this relevant for me?**
When you deposit your funds on https://harvest.finance/ they get deposited in our smart contract.
 

## Composability 
Composability risk is about using multiple smart contracts each of which has its own risk. Harvest Finance is exposed to this type of risk because it is leveraging other contracts to create more APY. Look into current strategy employed to get to know what other contracts are leveraged.

# **Impermanent Loss / Divergence loss**

Impermanent loss is associated with providing funds/coins to a liquidity pool. Liquidity pools are used in Decentralized Exchanges such as Uniswap, Curve, and Balancer in order to create money markets a.k.a. the ability for traders to buy and sell coins. 
Impermanent loss can be easily explained by the difference in holding an asset versus providing liquidity in that asset. Or simply said you might be better off by holding an asset vs providing liquidity for it on a Decentralized Exchange. For example, in Uniswap a 25% price change of an asset results in a 0.6% loss relative to if you hold the asset. There are very good resources to understand the concept and the math behind it – [HERE](/en/https://www.youtube.com/watch?v=8XJ1MSTEuU0) and [HERE](/en/https://medium.com/@pintail/uniswap-a-good-deal-for-liquidity-providers-104c0b6816f2)


**Why is this relevant for me?**
Harvest uses strategies that have exposure to liquidity pools, thus it is susceptible to this kind of risk.

## **Slippage**
Slippage occurs when coins are bought from a liquidity pool. It is the cost that the buyer must bear for disrupting the equilibrium in the liquidity pool. Slippage can occur at any time but is most prevalent during high volatility times.
 
**Why is this relevant for me?**
Sometimes when you have put funds on https://harvest.finance/, at the very beginning you could be seeing that you have fewer funds than initially deposited. This phenomenon happens due to slippage. By keeping your funds deposited for some time your deposits should return to what you initially deposited and keep growing.


