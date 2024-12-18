---
description: >-
  If you're experiencing an issue with Cielo, read the Frequently Asked
  Questions to identify a solution. If you're still stuck, contact support.
---

# FAQ

<details>

<summary>What's the difference between My Wallets and Custom Alerts?</summary>

My Wallets is where you create alerts for specific wallets you're following. Custom Alerts is where you create general alerts based on all the wallets you're following.

</details>

<details>

<summary>Why aren't I receiving alerts?</summary>

There are typically three reasons why you might not be receiving bot alerts:

1. You haven't assigned alerts to a specific Telegram bot or Discord channel.
2. You've set a minimum USD filter so aren't receiving alerts below this threshold.
3. You've deselected certain EVM networks so aren't receiving alerts for tx on these chains.

If you’re not receiving Telegram or Discord alerts, go to **Settings** > [**Advanced**](https://app.cielo.finance/settings/advanced) and make sure you have at least one Telegram or Discord bot activated. Flick the toggle switch to blue to activate a Telegram bot.

Next, go to [My Wallets](https://app.cielo.finance/my-wallets) and select the wallets you wish to receive alerts for. Click the edit icon beside the wallet or select all and click **Alert Settings**. Make sure that alerts are being sent to the Telegram bot or Discord channel you’ve activated under settings.\
\
Finally, click on **Transaction type filters** and make sure you’ve enabled alerts for the tx you wish to see. Ensure that you haven't set a USD minimum or deselected certain networks.

Remember, the number of Telegram/Discord alerts you can receive is capped at 120 per hour for Free users and 1,000/3,000 for Pro/Whale. If you hit this limit, alerts will temporarily be halted but will resume at the start of the next hour.

\


</details>

<details>

<summary>Why are Telegram alerts delayed?</summary>

Due to the limits of Telegram's architecture, high user demand can occasionally max out the capacity of bots such as Cielo wallet trackers. While this issue quickly corrects, it can cause temporary delays in receiving alerts or for alerts to drop out altogether.

To solve this, Pro and Whale users can create custom Cielo bots that are exclusive to their use. This provides a more reliable alert stream and overcomes the limitations inherent to using public Telegram bots. Find out how to create a custom bot [here.](https://docs.cielo.finance/discord-+-telegram-bots/telegram-custom-bot)

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

<summary>What’s the difference between Premium and Private bots?</summary>

Tl;dr: Private bots are faster than Premium but can’t be added to groups or channels.

Premium is the name given to Cielo Telegram bots that are available to Pro + Whale users e.g. Cielo Premium Bot #1. While the alerts published by each of these bots is unique to the user, the bandwidth is shared. In other words, there might be 2,000 users accessing Premium Bot #1 concurrently.

Private bots allow Pro + Whale users to access the same service through a dedicated Telegram channel that is exclusively theirs. This should ensure more consistent alert delivery, since bandwidth isn’t at risk of being consumed by other users. While there is no obligation to use private bots, it is recommended that Pro + Whale users do so.

There are just two disadvantages to private bots: unlike regular Cielo bots, they can’t be added to groups

\


</details>

<details>

<summary>How do I view my connected wallet in Telegram?</summary>

To view the wallet connected with your Telegram account, open the Cielo Telegram bot and press the menu button or type _/menu_. Your wallet will be displayed at the top of the menu bar that appears. To change this wallet, visit [Settings](https://app.cielo.finance/settings/general) in the Cielo web app.

</details>

<details>

<summary>How do I work out which wallet I paired with my Cielo account?</summary>

If you’ve been signed out of the Cielo web app and have multiple wallets installed, it can be hard working out which one to connect to regain account access. To solve this, open any Cielo bot in Telegram and click the menu icon or type /menu and your connected wallet address will be displayed.

_**Note**: If you used Phantom wallet to sign up to Cielo and have since disabled EVM within the wallet, this will account for why you can’t sign in to Cielo. Reactivate your Phantom EVM address to resolve this._

\


</details>

<details>

<summary>How do I pair my Cielo account with a different Telegram account?</summary>

If you need to change the Telegram account you’re using with Cielo, in the web app go to **Settings >** [**Alerts**](https://app.cielo.finance/settings/alerts) and where your current Telegram handle is displayed, select **Disconnect**. After logging in to Telegram with the account you wish to pair, refresh the web app and select **Connect** to complete the process.

</details>

<details>

<summary>Why are there certain wallets that I can't follow?</summary>

Some wallets generate an extremely high volume of transactions. To prevent your feed and alerts from being overwhelmed with tx, you are unable to follow these wallets. Only a fraction of all wallets fall into this category, which typically includes bots and smart contract addresses for popular protocols.

Most of the wallets that cannot be tracked are bots which generate hundreds of tx within a single block. The more sophisticated bots route trades through proprietary closed source contracts, rendering them impossible to track.

We also take additional measures to exclude high volume wallets. For example, if a Solana wallet makes more than 3,000 txs per day, it is filtered from our system.

</details>

<details>

<summary>Why is there a limit on the number of wallet profiles I can view?</summary>

To prevent our servers from melting, we're obliged to place a cap on the number of wallet profiles that can be viewed within a 24-hour period as follows:

* **Free**: 100
* **Pro**: 1,000
* **Whale**: 5,000

The vast majority of users will never hit this limit, but should this occur you will receive a notification. Your alert limit will reset 24 hours later, allowing you to start loading wallet profiles again.

You can check the amount of alerts you have used [here](https://app.cielo.finance/settings/alert-limits).

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

<details>

<summary>How is PnL calculated?</summary>

PnL is a unit for measuring the net profit or loss recorded by onchain traders. Cielo calculates both Realized and Unrealized PnL for wallets.

* **Realized PnL** applies to tokens a wallet has bought and since sold, be it for profit or loss.
* **Unrealized PnL** calculates the value of the tokens a wallet is still holding based on their current market price.

Both realized and unrealized PnL can be viewed for wallet profiles, while Wallet Discovery ranks wallets on _realized_ PnL only.

**Note**: While the basic formula for calculating PnL is simple, there are many variables that can affect the PnL that is displayed for a particular wallet. Due to the presence of honeypots (tokens that can be bought but not sold) and the complexities of blockchain architecture such as Solana, there may be occasions when Cielo is unable to accurately calculate PnL for a wallet. We are constantly working to improve our PnL calculation algorithm with the goal of providing accurate wallet PnL.

</details>

<details>

<summary>What data is utilized in generating the Popular Wallets tag?</summary>

Cielo assigns tags to certain wallets to support filtering for Wallet Discovery. The same tag is also displayed on the profile page of qualifying wallets. The Popular Wallets tag is added to any wallet that is being followed by more than 30 users on the Cielo free plan. Because Cielo uses aggregated data to generate this tag, information concerning the behavior of individual users is neither stored nor discoverable by other users. Moreover, aggregated Pro and Whale data is not used in the calculation of the Popular Wallets tag.

\


</details>
