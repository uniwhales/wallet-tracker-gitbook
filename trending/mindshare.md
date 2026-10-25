---
description: How Cielo ranks Trending tokens by real wallet activity.
---

# Mindshare

Mindshare is the metric behind [Trending](./). It measures how much of the buying among wallets tracked on Cielo goes into a token. A token ranks high when many of those wallets buy it, which is much harder to fake with bots than volume.

## How it works

Cielo watches swaps from every wallet its users track, across Solana, Base, Robinhood and Arc. Pick a timeframe from 1 minute up to 24 hours. Rankings reflect relative conviction, not raw token metrics. The number under the % is the number of tracked wallets buying.

Hover the Mindshare % to see where that buying comes from, broken down by trading app (for example Axiom, Fomo, Trojan and Cielo).

<figure><img src="https://1250667054-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FgZTvWhkjLJ8uCLtiUaPq%2Fuploads%2FXcgMftvvYTECUytj0CUm%2Fimage.png?alt=media&#x26;token=bc639e75-4ad4-4e9c-8ee4-6f7a004912bf" alt=""><figcaption></figcaption></figure>

When enough tracked wallets start buying the same token inside the window, it enters Trending. Because this is driven by wallet behavior rather than price or volume, Trending often shows a token before the usual metrics catch up.

## How to use it

Mindshare tells you where attention is going. It doesn't tell you whether a token is safe or whether it will keep going.

* A high Mindshare token with thin liquidity or a dev holding a big chunk of supply is still risky. Check the [token checklist](../trading/overview.md#token-checklist) before you buy.
* A token that leads on 1m but doesn't show on 1h is a quick rotation. One that holds on 6h and 24h has staying power.
* Check the wallet count as well as the %. On a quiet chain, a handful of wallets can produce a big percentage.

We filter out known honeypots and spam, but new tokens are launched faster than anyone can review them. Mindshare is a signal, not a guarantee.
