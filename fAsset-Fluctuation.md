---
title: fAsset fluctuation
description: 
published: true
date: 2020-10-13T15:38:20.045Z
tags: 
editor: markdown
dateCreated: 2020-10-13T15:38:20.045Z
---

# Why is my fAsset balance fluctuating?

> Your fAsset carries a conversion rate to the underlying asset you deposited. This conversation rate increases with every succesfull harvest. There are also events that impact the conversion rate negatively. Consider when using a system like Curve there is slippage when withdrawing to a singular asset, as well as a withdraw fee. When a user exits Harvest, those fees are currently socialized across the fAsset pools, but in the near future will be directly charged to the user triggering the slippage/fee. This means the pool value of fAssets will no longer be impacted by these negatively impacting the conversion events. 
{.is-info}


A cause for positive fluctuation:
- You deposit 1000 USDC in Harvest and receive 1000 fUSDC. (fUSDC conversion rate to USDC is 1)
Let's say that Harvest managed to generate 10% return on your USDC in 14 days. 
Now fUSDC conversation rate is 1.1 to 1 USDC. If you withdraw you will receive 1100 USDC. (1000x1.1)

A cause for negative fluctuation:
- Let's take the case above. You have 1000 fUSDC ,14 days have passed and your fUSDC carries 1.1 to 1 UDSC rate. Unfortunately, on the 15th day there are large withdraws from the protocol. Slippage and fees occur and are socialized throughout the fPools thus that affects your fUSDC conversation rate negatively. Let's say now it has fallen to 1.09. If you decide to withdraw you will receive 1090USDC (1000x1.09)

