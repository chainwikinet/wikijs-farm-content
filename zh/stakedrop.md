---
title: FARM Stake 耕作
description: 
published: true
date: 2020-09-08T12:52:46.267Z
tags: 
editor: markdown
---

> 当心诈骗！在 GitHub 上验证[令牌地址](https://github.com/harvest-finance/harvest)，以确保您交易的是正确的 Harvest Finance 令牌！
{.is-warning}

>热心的社区成员创建了[非常全面的参与 Staking 获得收益的图文指南](https://medium.com/@BIBI_CAT/harvest-finance-%E5%BC%80%E5%BF%83%E5%86%9C%E5%9C%BA%E6%9C%80%E5%85%A8%E6%8C%96%E7%9F%BF%E6%89%8B%E5%86%8C-50351af924eb)
{.is-info}



# Stake 代币，赚取 FARM

要参与并赚取 FARM，需要 Stake 以下几种资产中的一种，并获得在 Harvest Finance 推出后分配的 FARM 份额：

-[Harvest Finance上线公告](https://medium.com/harvest-finance/the-harvest-finance-project-338c3e5806fc)
- 开始Staking时间：2020年9月1日
- Staking结束时间：2024年9月1日
- [FARM代币供应信息](/总供应量)

## 第一波挖矿可以在多个地方进行管理：

- [官网](https：//harvest.finance/)
- 独立的第三方网站
- 直接和 Etherscan 合同交互



# 将令牌添加到耕作中

> 将 USDC，DAI 或 USDT 存入 Harvest 来接收你参与 FARM 质押的 fUSDC，fDAI 或 fUSDT 的 Gas 费可能很高。或者，您可以直接在[在Uniswap上购买fUSDC](https://app.uniswap.org/#/swap?outputCurrency=0xc3f7ffb5d5869b3ade9448d094d81b0521e8326f)。用于fDAI和fUSDT的Uniswap池也即将推出。
{.is-warning}



# 从耕作中取出令牌

> 注意 Gas 交易价格极高。使用[工具](gasnow.org)来确保您将 Gas 价格设置得足够高，否则您的交易可能需要很长时间才能确认。
{.is-info}


对于 fDAI，fUSDC 和 fUSDT，您必须首先从 Staking 的奖励合约中取出。然后在首页将它们取出，重新转化为基础 DAI，USDC 和 USDT。

- 1.从Staking奖励合约中取出：https://harvest.finance/earn
  - 点击`Unstake & Claim` ，然后点击下面的“`UNSTAKE & CLAIM` ”按钮来进行交易。
  - 等待交易确认，然后您将获得之前质押的 fToken 和 FARM 奖励。
  
- 2.要将 fToken 换回基础稳定币中，需要到[官网](https://harvest.finance/)执行以下操作：
  - 输入您想交换的 fToken的 余额。如果不确定你目前钱包的实际余额，可以将 fToken 作为[自定义令牌添加到您的钱包](https://metamask.zendesk.com/hc/zh-cn/articles/360015489031-How-to-View-See -您的通行证令牌)或通过将您的地址放入 [fDAI](https://etherscan.io/address/0xe85c8581e60d7cd32bbfd86303d2a4fa6a951dac#readContract)，[fUSDC](https://etherscan.io/address/0xc3f7ffb5d5869b3ade9448d094d81b0521e8326f#readContract)或[fUSDT](https://etherscan.io/address/0xc7ee21406bb581e741fbb8b21f213188433d9f2f#readContract)令牌合约中，通过调用的`balanceOf` 合约功能查看。如果使用 Etherscan 的合约，请注意，返回的fUSDC和fUSDT的余额有六个小数位（比如 987654321 = 987.654321 fUSDC），而fDAI的位数为18。这应大约等于您存入的 DAI，USDC 或 USDT 的金额。如果你尝试提超过余额的数量，你钱包就会返回交易将失败的报错。
  - 点击`Withdraw`的提款按钮并发送交易。如果您在大量提款期间选择提款并且 Harvest 的提款缓冲用完了的话，你就要支付一笔费用，用于弥补你从以从收益耕作策略中提取你的稳定币。该笔交易将会很贵，[比如这个案例](https://etherscan.io/tx/0x959045e3c8fb26a9eeab00e5ebe11fe62012cc7148f4d025c4c7f75ec0bed0bb) 消耗了 220 万 Gas 费）。如果你通过将更多资金存入 Harvest 并在等带提款缓冲得到补充之后之后再回来，那么费用可能会更低些（[例如](https://etherscan.io/tx/0x70fddec35fcf1f89fbfff90972be0e04ce0ae8c34abfaf2900e5210fdf86303e)，只花费了 468,000 Gas 费）。
  - 最后等待交易确认，确认之后你就会收到稳定币。如果耕种策略成功实施的话，您的稳定币会获得超额利息，因此你获得的收益可能超过您投入的成本。

