---
title: Getting Started with UNI Pools
description: Now you have the basics down. Let's go after that high APY in the UNI Pool!
published: true
date: 2020-09-27T20:51:32.620Z
tags: 
editor: markdown
dateCreated: 2020-09-27T19:40:02.868Z
---

# Intro :corn:
Welcome back city slicker! Now that you roughed up your hands in the [first tutorial](/en/getting-started), let's start chasing some of that crazy APY in some other pools. How about the Uniswap Pool? That APY is way up there!

Sounds too good to be true, you say? Good point. You need to understand the risk if Impermanent Loss by playing in this pool.

> If you don't understand IL, I highly suggest you stop right here and do a little homework. Personally, I had to watch [this video](https://www.youtube.com/watch?v=8XJ1MSTEuU0) 3 times, and read a few blog posts for it to finally sink in.
{.is-danger}

So you do want to live on the edge! Okay! Let's get going!
# Here's What We're Going to Do :tractor:
To participate in the Uniswap LP Farm, we will need to supply USDC-FARM liquidity to Uniswap's Liquidity Pool. Then use Uniswap LP tokens minted from that transaction to deposit into the Farm.
1. Get USDC (not sure how? Go to the previous tutorial)
1. Swap half of our USDC for FARM
1. Deposit USDC and FARM into Uniswap's Liquidity Pool. Receive UNI_LP tokens
1. Deposit UNI_LP Token into Farm
1. Profit! :bread:
> These steps total 6 transactions on the Etherium blockchain. Be wary of gas prices before you start. Make sure you have enough ETH in your Wallet. Gas was at ~50 Gwei at time of doing this tutorial.
{.is-warning}

# Get USDC :watermelon:
Alright, you should already know how to do this if you followed the [first tutorial](/en/getting-started). 
In the next step, we will be exchaning half (by value) of our USDC for FARM. So make sure you have enough USDC to split.
# Buy FARM :strawberry:
Now, with our USDC, we are going to swap half of it for FARM
>  This will happen in two steps. An Approval and a Swap step. Both will charge gas!
{.is-warning}
- Click Buy FARM on the top of the [harvest.finance](https://harvest.finance) page. It will take you to Uniswap to Swap USDC for FARM.
![getting_started_uni_buy_farm.png](/getting_started_uni_buy_farm.png)
- OMG! SCARY WARNING :scream:
![getting_started_uni_uni_warning.png](/getting_started_uni_uni_warning.png)
> The warning says exactly what it means. It's up to you to make sure the addresses you are using are correct. You might want to click on those View on Etherscan links and verify them against [Harvest's Github page](https://github.com/harvest-finance/harvest).
{.is-danger}
- All set? Okay! Take half of our USDC and Swap it for FARM! in this case, we have 1500 USDC. So we will use 750 for the SWAP.![getting_started_uni_swap_usdc_farm_approve.png](/getting_started_uni_swap_usdc_farm_approve.png)
- Once the Approval goes through, we will now do the Swap![getting_started_uni_swap_usdc_farm_swap.png](/getting_started_uni_swap_usdc_farm_swap.png)
- Hooray! We now have USDC and FARM in our Wallet to add to the Liquidity Pool
![getting_started_uni_metamask_farm_usdc.png](/getting_started_uni_metamask_farm_usdc.png)
*I know, I know. You are wondering where I accumulated all that DAI and FNT. That's none of your business!*
# Add FARM and USDC to UNI LP :apple:
With the USDC and FARM in our Wallet, we are going to add it to Uniswaps USDC-FARM Liquidity Pool.
> This will also require two transaction: Approve and Supply
{.is-warning}
- Click Earn on the top of Harvest.Finance. Then select the Uniswap Farm
- ![getting_started_uni_select_uni_farm.png](/getting_started_uni_select_uni_farm.png)
- Select UNI-V2. This will take you to Uniswap's USDC-FARM Pair page
![getting_started_uni_acquire_uni_lp_tokens.png](/getting_started_images/getting_started_uni_acquire_uni_lp_tokens.png)
- At the top right of the page, select Add Liquidity
![getting_started_uni_add_liquidity.png](/getting_started_images/getting_started_uni_add_liquidity.png)
- Select Max FARM (or USDC)! Then click Approve
![getting_started_uni_approve_liquidity.png](/getting_started_images/getting_started_uni_approve_liquidity.png)
- Once Approve transaction goes through, Click Supply
![getting_started_uni_supply_liquidity.png](/getting_started_images/getting_started_uni_supply_liquidity.png)
- After this transaction, Uniswap will show your positions in the Pool
![getting_started_uni_lp_positions.png](/getting_started_images/getting_started_uni_lp_positions.png)
- Congrats! you are now a Liquidity Provider for Uniswaps USDC-FARM Liquidity Pool! You are now earning fees off user's exchange transactions from this pool. Of course, now you are also at risk of Impermanent Loss :scream: :scream: :scream:
# Deposit Tokens in to UNI LP Farm :seedling:
# Earn FARM! :bread: