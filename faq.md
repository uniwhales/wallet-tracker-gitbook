---
description: >-
  If you're experiencing an issue with Cielo, read the Frequently Asked
  Questions to identify a solution. If you're still stuck, contact support.
---

# FAQ

<details>

<summary>Why aren't I receiving alerts?</summary>

If you’re not receiving Telegram or Discord alerts, go to **Settings** > [**Advanced**](https://app.cielo.finance/settings/advanced) and make sure you have at least one Telegram or Discord bot activated. Flick the toggle switch to blue to activate a Telegram bot.

Next, go to [My Wallets](https://app.cielo.finance/my-wallets) and select the wallets you wish to receive alerts for. Click the edit icon beside the wallet or select all and click **Alert Settings**. Make sure that alerts are being sent to the Telegram bot or Discord channel you’ve activated under settings.\
\
Finally, click on **Transaction type filters** and make sure you’ve enabled alerts for the tx you wish to see.

Remember, the number of Telegram/Discord alerts you can receive is capped at 120 per hour for Free users and 1,000/3,000 for Pro/Whale. If you hit this limit, alerts will temporarily be halted but will resume at the start of the next hour.

\


</details>

<details>

<summary>I’m receiving too many alerts</summary>

Go to [My Wallets](https://app.cielo.finance/my-wallets) and select all wallets or select the wallets that are sending too many alerts. Click Alert Settings and adjust the filters. There are several ways to reduce the number of alerts you receive:

1\. Set a minimum USD tx value. This will filter out low value tx.

2\. Reduce the number of tx types you receive alerts for.

3\. Reduce the number of chains you receive alerts for.

4\. Disable alerts for wallets marked High tx that are particularly active.

\


</details>

<details>

<summary>Why are there certain wallets that I can't follow?</summary>

Some wallets generate an extremely high volume of transactions. To prevent your feed and alerts from being overwhelmed with tx, you are unable to follow these wallets. Only a fraction of all wallets fall into this category, which typically includes bots and smart contract addresses for popular protocols.

You are unable to follow Solana wallets that generate more than 3,000 tx per day, while high volume EVM wallets are also excluded. Most of the wallets that fall into this category are MEV bots, some of which generate hundreds of tx within a single block. The more sophisticated bots route trades through proprietary closed source contracts, rendering them impossible to track.

</details>

<details>

<summary>Why can't I access full transaction data for certain wallets?</summary>

Cielo provides transaction alerts and PnL for hundreds of thousands of EVM and non-EVM wallets. However, with certain wallets providing full or even partial data is impossible. This is typically because the wallet in question is a complex MEV bot that routes trades through its own closed source contracts.

Some of these bots, which are operated by sophisticated teams, perform hundreds of trades within a single block. For this reason, it is impractical to provide transaction data or accurate PnL for these wallets.

</details>

<details>

<summary>How do I change the default charting tool?</summary>

By default, this is set to GeckoTerminal but Cielo supports multiple options. Go to **Settings** > [**Advanced** ](https://app.cielo.finance/settings/advanced)and select a different charting tool from the dropdown menu. Options include DEX Screener, DEXTools, and Photon.\


</details>

<details>

<summary>How do I view the token contract address in swap alerts?</summary>

To enable this feature, go to **Settings** > [**Advanced** ](https://app.cielo.finance/settings/advanced) and check the box marked _Display Token Address in Alerts_. Now, whenever you receive a Telegram or Discord alert for a token swap, the smart contract address will be displayed and can be copied in one click.\


</details>

<details>

<summary>Where can I find wallets to follow?</summary>

The following resources can be used to find wallets and add them to your Cielo feed:

* [Public Lists](https://app.cielo.finance/public-lists)
* [Wallet Discovery](https://app.cielo.finance/wallet-discovery) (Pro+Whale)
* [Onchain Intrigue](https://t.me/onchainintrigue)
* [Etherscan](https://etherscan.io/) and other block explorers: filter tokens by top holders and add major wallets
* Dex Screener and DEXTools: In [Dex Screener](https://dexscreener.com/) click on **Top Traders** for a token, open the wallet in a block explorer and copy the address
* Twitter/Telegram: Follow accounts that share the wallets of top traders

\


</details>

<details>

<summary>How do I bulk edit wallets?</summary>

In [My Wallets](https://app.cielo.finance/my-wallets), click the checkbox to the left of **All Wallets**. This will select all wallets on the current page. To select all of the wallets you are following, click on the text that reads "Select all XXX of your wallets."

Then click the button at the bottom of the page marked Alert Settings. Any changes you subsequently make will be applied to all of the wallets you have selected. To bulk edit wallets within a specific list, first select the list from the dropdown menu at the top of the page and then follow the instructions above.

</details>

<details>

<summary>How do I track tokens?</summary>

Go to [Custom Alerts](https://app.cielo.finance/custom-alerts) and select **Add Alert**. Enter the token address, select minimum swap value, and select the network.

</details>
