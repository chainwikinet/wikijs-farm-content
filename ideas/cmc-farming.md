---
title: API for Coinmarketcap Farming Page
description: 
published: true
date: 2020-09-21T14:03:06.346Z
tags: 
editor: markdown
dateCreated: 2020-09-21T14:03:06.346Z
---

Coinmarket cap added a yield farming summary page: https://coinmarketcap.com/beta/yield-farming/

To be listed on this page, Harvest must provide an API that returns some information.

If we are building a backend to serve Token Terminal data, an endpoint could be added for this CMC Farming data.

# Required API

```json
{
    provider: 'SushiSwap',  // Project name - Sushi
    provider_logo: 'URL', // Project logo, square, less than 100*100 px
    provider_URL: 'URL', // Project URL
    links: [        // social media info
    {
      title: 'Twitter',
      link: 'https://twitter.com/sushiswap',
     }
  ], 
    pools: [
      {
          
          name: 'Pool Name 1', // Pool name if any, eg. Sushi Party, Uniswap Sushi-ETH LP
          pair: 'SUSHI-ETH'  // Pool pairs, e.g SUSHI-ETH
          pairLink: 'https://sushiswapclassic.org/farms/SUSHI-ETH%20SLP', // The URL to this pool
          logo: 'URL', //  Pool logo if any, otherwise just use Project logo
          poolRewards: ['SUSHI'], // The reward token ticker
          apr: 1.1,  // APY, 1.1 means 110%
          totalStaked: 13987213,  // Total valued lock in USD 

      },
      {
          name: 'Pool Name 2', 
          pair: 'LEND-ETH'  
          pairLink: 'https://sushiswapclassic.org/farms/SUSHI-ETH%20SLP'
          logo: 'URL', 
          poolRewards: ['SUSHI'], 
          apr: 1.1,  
          totalStaked: 13987213, 
      }
    ]
}
```

# Notes

The APR variable should actually be APR, not APY as the comment says.

> CMC: the calc is like (daily rewards / total value locked * 365)
