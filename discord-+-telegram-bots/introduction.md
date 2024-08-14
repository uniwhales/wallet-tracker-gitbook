---
description: >-
  Cielo provides Telegram and Discord bots that deliver real-time alerts for
  onchain transactions across dozens of blockchains.
---

# Introduction

Bots can be set up within the Cielo web app or directly within Telegram. Once initialized, the bot will deliver a Telegram alert any time a tx occurs that matches your criteria. The Discord bot works in exactly the same way but must be configured within the Cielo web app.

Cielo bots allow you to monitor addresses and transaction types that are relevant to your interests while filtering out everything else. Tx are labeled to show the network, tx type, value, and protocol together with informational links.

{% hint style="info" %}
Because Cielo Telegram bots are integrated with Banana Gun, you can trade tokens instantly within Telegram. First create a [**Banana Gun bot**](https://t.me/BananaGunRegister\_bot). You can then click the **Buy on Banana Gun** link displayed in Cielo Telegram alerts to instantly buy the token in question.
{% endhint %}

### Labeling

Cielo automatically labels tx involving known tokens, DEXs, lending platforms, NFTs, bridges, and other DeFi protocols. This makes it easier to understand which asset is being used by whom, where, and why. For instance:

<figure><img src="../.gitbook/assets/Screenshot 2024-03-03 at 14.19.07.png" alt=""><figcaption></figcaption></figure>

* **#DWFLabs**: _Wallet label_. Clicking this link will use Telegram search to produce a list of any other tx involving this wallet that your Cielo Wallet Tracker bot has recorded.
* **Transferred:** _Tx type_. This describes the nature of the tx. Clicking on this will open a blockchain explorer link to the smart contract that was interacted with.
* **#bnb**: _Network_. Shows the blockchain network where the tx originated.
* **Cielo**: _Cielo web app link_. Clicking on this allows you to view the tx in Cielo.
* **ViewTx**: _Blockchain explorer link_. Opens a link for the transaction hash.

To see Cielo bots in action, check the [Onchain Intrigue](https://t.me/CelsiusEVMTracker) channel. It's used for monitoring whales, hackers, VCs, and other market-movers.

Cielo bots enable to you to select, segment, and sort wallets and transactions to optimize the signal-to-noise. This will allow you to zero in on tx of interest and screen the rest.

{% hint style="info" %}
The Cielo bot can be used as a standalone application within Telegram or as a complement to the Cielo web app. Although it’s possible to configuree the bot within Telegram, you may find it easier to adjust settings within the Cielo web app. The Discord bot must be configured within the Cielo web app.
{% endhint %}
