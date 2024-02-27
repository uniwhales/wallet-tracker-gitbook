---
description: >-
  The Cielo Wallet Tracker is a Telegram and Discord bot that provides real-time
  alerts for onchain transactions. It can monitor activity across 20
  EVM-compatible blockchains.
---

# Introduction

The Cielo Wallet Tracker is the most powerful onchain bot of its kind. It provides unrivaled network coverage and transaction filtering. The bot can be set up within the Cielo web app or directly within Telegram. Once initialized, it will deliver a Telegram alert any time a tx occurs that matches your criteria. The Discord bot works in exactly the same way but must be configured within the Cielo web app.

The Cielo Wallet Tracker works as a customizable bot that detects onchain transactions and relays them to Telegram/Discord. It allows you to monitor addresses and transaction types that are relevant to your interests while filtering out everything else. Tx are labeled to show the network, tx type, value, and protocol where it occurred together with informational links.

Using the Cielo Wallet Tracker you can:

* Track up to 250 wallets
* Track up to 5 tokens
* Receive real-time alerts for swaps, NFT mints, LP adds etc
* Add the bot to Telegram groups and Discord channels

…and much more

### Labeling

The Cielo Wallet Tracker automatically labels tx involving known tokens, DEXs, lending platforms, NFTs, bridges, and other DeFi protocols. This makes it easier to understand which asset is being used by whom, where, and why. For instance:

<figure><img src="../.gitbook/assets/Screenshot 2023-06-19 at 14.58.50.png" alt=""><figcaption></figcaption></figure>

The above tx was made by the founder of Curve protocol. Because they are a known entity, Cielo has applied labels and links that make it easy to determine what this transaction has involved.

* **#MichaelEgorovCurve1**: _Wallet name_. Clicking this link will use Telegram search to produce a list of any other tx involving this wallet that your Cielo Wallet Tracker bot has recorded.
* **Curve.fi: Voting Ownership:** _Tx type_. This describes the nature of the tx. Clicking on this will open a blockchain explorer link to the smart contract that was interacted with.
* **#ethereum**: _Network_. Shows the blockchain network where the tx originated.
* **Cielo**: _Cielo web app link_. Clicking on this allows you to view the tx in Cielo.
* **ViewTx**: _Blockchain explorer link_. Opens a link for the transaction hash.
* **Tweet**: Opens a Twitter window pre-populated with information about this tx. Add your own commentary and then publish it as a tweet.

<figure><img src="../.gitbook/assets/Screenshot 2023-06-19 at 15.08.13.png" alt=""><figcaption></figcaption></figure>

Above is another example of a tx published by the Cielo Wallet Tracker. In this example, the trader has sold an NFT for a loss of more than 2 ETH. The red emoji denotes that they lost money on this trade; a green emoji would show that they made a profit.

### See for yourself

As an example of the Cielo Wallet Tracker in action, check out our [Onchain Intrigue](https://t.me/CelsiusEVMTracker) channel. It's used for monitoring onchain activity associated with whales, hackers, VCs, and other market-movers. And here’s [another channel](https://t.me/NFTideasEVMTracker) for monitoring leading NFT traders. The Cielo Wallet Tracker allows you to set up a custom Telegram/Discord stream of alerts that are tailored to your interests.

It’s up to you to select, segment, and sort the wallets and transaction types you wish to follow so as to optimize the signal-to-noise ratio. This will allow you to zero in on the transaction types and users that are of interest to you and to screen the rest.

{% hint style="info" %}
The Cielo Wallet tracker can be used as a standalone application within Telegram, or as a complement to the Cielo web app. Although it’s possible to manage the bot within Telegram, you may find it easier to adjust settings within the Cielo web app. The Discord bot must be configured within the Cielo web app.
{% endhint %}
