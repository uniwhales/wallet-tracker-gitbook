# Telegram

1. [**Bypassing the Cielo web app**](getting-started.md#bypassing-the-cielo-web-app)
2. [**Adding a wallet**](getting-started.md#adding-a-wallet)
3. [**Adding a token**](getting-started.md#adding-a-token)
4. [**Editing wallets + tokens**](getting-started.md#editing-wallets--tokens)
5. [**Alert settings**](getting-started.md#alert-settings)
6. [**Viewing contract address**](getting-started.md#viewing-contract-address)
7. [**Telegram trading with Banana Gun**](getting-started.md#telegram-trading-with-banana-gun)



Cielo provides free users with one Telegram bot. Any wallets or tokens you enable alerts for will automatically be assigned to this bot. However, Pro + Whale members can access **two** and **six** bots respectively.

This allows you to map specific tx types to a specific bot. For instance, you could use one bot for your own wallets, another for NFT traders, and another for DEX whales.

To activate your Telegram bots, in the Cielo web app visit [Alerts](https://app.cielo.finance/settings/alerts).

To change which bot a wallet is assigned to, on the configure page, click the edit icon alongside the wallet name. In the popup that appears, click the dropdown titled **Telegram bot**. Pick a desired bot and then hit **Save changes**.

## Bypassing the Cielo web app

It's possible to use the Cielo as a standalone Telegram bot, without pairing it to the Cielo web app.

However it's recommended that you use the bot in conjunction with the Cielo [web app](https://app.cielo.finance). The app is free to use and its interface makes it easier to adjust wallet settings than doing so within Telegram. If you'd rather just use the Telegram bot on its own, however, read on.

To initialize the [Cielo Wallet Tracker bot](https://t.me/evmtrackerbot), open it in Telegram and press the blue **Start** button.

<figure><img src="../.gitbook/assets/Screenshot 2024-09-12 at 14.36.28.png" alt=""><figcaption></figcaption></figure>

Press the blue menu icon to view wallet settings:

<figure><img src="../.gitbook/assets/Screenshot 2023-06-18 at 19.14.12.png" alt="" width="261"><figcaption></figcaption></figure>

The following options are displayed:

* **Add wallet or token**: Input the address and label for a wallet you wish to track or the smart contracxt address for a token.
* **List**: View all of the wallets that you're currently tracking. You can then click on the edit option beside each wallet to adjust its settings.
* **Menu**: View master menu that includes options for setting group and channel alerts.
* **Bot settings**: Opens options to disable bot or reset chat.



You can also control the Telegram bot by entering the following commands:

<mark style="color:blue;">/start -</mark> Initialize the bot

<mark style="color:blue;">/add\_wallet\_or\_token</mark> - Add new wallet or token

<mark style="color:blue;">/list</mark> - Get the list of all tracked wallets / tokens

<mark style="color:blue;">/bots</mark> - View available reserve bots

<mark style="color:blue;">/pnl</mark> - Get PnL stats for a wallet

<mark style="color:blue;">/menu</mark> - Open the menu

<mark style="color:blue;">/add \[wallet] \[label]</mark> - Add a new wallet. You can specify multiple wallets separated by comma (e.g. /add WALLET\_ADDRESS\_1 LABEL\_1, WALLET\_ADDRESS\_2 LABEL\_2)

<mark style="color:blue;">/add\_token \[chain\_name] \[token\_address] \[min\_amount\_usd]</mark> - Add a new token

<mark style="color:blue;">/bot\_settings</mark> - Open bot settings

<mark style="color:blue;">/delete \[wallet</mark>] - Delete wallet. You can specify multiple wallets separated by comma (e.g. /delete WALLET\_ADDRESS\_1, WALLET\_ADDRESS\_2)

<mark style="color:blue;">/help</mark> - View a list of all supported commands

### Adding a wallet

To add a wallet using the Telegram bot, click the blue menu icon followed by the top option that appears: **Add new wallet or token**.

<figure><img src="../.gitbook/assets/Screenshot 2023-06-18 at 19.23.49.png" alt=""><figcaption></figcaption></figure>

Then click the **Wallet** button and paste in the wallet address followed by a space and then an optional name for the wallet e.g. _My Trading Wallet_. By default, all of the chains that Cielo tracks are enabled. If you wish to disable alerts for any of these chains, just click the relevant button to disable the selection.

<figure><img src="../.gitbook/assets/Screenshot 2024-09-12 at 14.46.35.png" alt=""><figcaption></figcaption></figure>

When you're done, click **Confirm**. You'll then see the following screen for controlling tx types:

<figure><img src="../.gitbook/assets/Screenshot 2023-06-18 at 19.27.13.png" alt=""><figcaption></figcaption></figure>

Click on a tx type you wish to disable and then hit **Confirm**. You will now see the following notification:

<figure><img src="../.gitbook/assets/Screenshot 2023-06-18 at 19.29.03.png" alt=""><figcaption></figcaption></figure>

And that's it: you're now tracking your first wallet using Cielo's Telegram bot.&#x20;

### Adding a token

To start tracking a token, repeat the procedure described above but select the **Token** button. You will then see the following option:

<figure><img src="../.gitbook/assets/Screenshot 2024-09-12 at 14.49.54 (1).png" alt=""><figcaption></figcaption></figure>

Select your desired chain, enter the smart contract address for the token and hit return. You can find this in a block explorer or using a market data site such as [CoinGecko](https://www.coingecko.com/).

You will now be asked to set a DEX swap threshold. This is to prevent you from being overwhelmed with alerts for popular tokens.

<figure><img src="../.gitbook/assets/Screenshot 2023-06-18 at 19.34.37.png" alt=""><figcaption></figcaption></figure>

Enter a value (demoninated in USD) and press return or hit **Skip** if you wish to receive alerts for all swaps, regardless of size. You will now see the following notification:

<figure><img src="../.gitbook/assets/Screenshot 2023-06-18 at 19.36.13.png" alt=""><figcaption></figcaption></figure>

### Editing wallets + tokens

To edit a wallet or token you're tracking, click the blue menu icon followed by the _/list_ option. This will produce a list of all wallets you're following.

<figure><img src="../.gitbook/assets/Screenshot 2023-06-18 at 19.47.25.png" alt=""><figcaption><p>In this example, the ARB token is being tracked.</p></figcaption></figure>

Click the blue edit link beneath the address to make an edit to the wallet or token. In addition to adjusting which chains and tx types are enabled (wallet) and the minimum tx size (tokens), you can disable alerts or delete the address altogether.

<figure><img src="../.gitbook/assets/Screenshot 2023-06-18 at 19.49.33.png" alt=""><figcaption></figcaption></figure>

&#x20;To re-enable alerts for a particular address, just repeat the process above and click the **Enable** button when prompted.&#x20;

<figure><img src="../.gitbook/assets/Screenshot 2023-06-18 at 19.50.39.png" alt=""><figcaption></figcaption></figure>

### Alert settings

Pro and Whale users can opt to have market cap and liquidity information displayed in bot alerts for token swaps. To enable this, in the web app check the **Display Market Cap and Liquidity** button in [Settings > Advanced](https://app.cielo.finance/settings/advanced).

By default, Cielo Wallet Tracker alerts include a **Chart** link, where applicable.

<figure><img src="../.gitbook/assets/Screenshot 2023-06-19 at 14.47.30.png" alt=""><figcaption></figcaption></figure>

Cielo allows you to choose which trading terminal you would like the **Chart** link to direct to. To adjust this setting, click the blue menu icon in the Cielo Wallet Tracker to pull up the main menu and then select **Alert Settings** followed by **Chart**.

<figure><img src="../.gitbook/assets/Screenshot 2023-06-19 at 14.50.02.png" alt=""><figcaption></figcaption></figure>

Then choose which of the four available terminals you would like to use for charting and hit **Confirm**.



### Viewing contract address

\
To trade a token that is displayed in the Cielo web app or Telegram bot, the contract address is required. Upon pasting this into a DEX such as Uniswap or an aggregator like Dexscreener, you can trade the token in question. There are a number of ways to obtain the contract address:<br>

1\. Click the **ViewTx** link to inspect the transaction in a block explorer.

2\. Click **Chart** to view the tx in a platform such as Gecko Terminal.

3\. Enable one-click contract address copy within Telegram.



To enable the latter option when using the Cielo Telegram bot, select **Menu** > **Alert Settings** > **Show Token Address**. When activated, this displays the contract address with each tx alert, allowing you to trade tokens faster and on the platform of your choosing.

<figure><img src="../.gitbook/assets/Screenshot 2023-08-28 at 11.52.29.png" alt=""><figcaption><p>The contract address is shown in red.</p></figcaption></figure>

### Telegram trading with Banana Gun

Using Cielo Telegram bots, you can execute trades directly within Telegram with Banana Gun. Cielo has integrated Banana Gun allowing you to click the **Buy on Banana Gun** link that appears in Cielo Telegram alerts.

{% hint style="info" %}
_**Disclaimer**: Trading tokens, particularly new memecoins, is risky as there is a high chance of financial loss. It is the responsibility of each user to research any asset they wish to purchase and to acknowledge the risks inherent to Telegram trading. Cielo has no control over the Banana Gun bot used for executing swaps and is not liable for losses incurred due to tokens losing value due to rug pulls and major sell-offs._

_tl;dr DYOR._
{% endhint %}

To enable Telegram swaps, create a [**Banana Gun bot**](https://t.me/BananaGunRegister_bot). You can then click the **Buy on Banana Gun** link displayed in Cielo alerts to instantly buy the token in question.

<figure><img src="../.gitbook/assets/Screenshot 2024-08-14 at 14.14.18.png" alt=""><figcaption></figcaption></figure>

If you _don't_ wish to see a Banana Gun link, you can disable this option in the [**Settings menu**](https://app.cielo.finance/settings/advanced) or within the Cielo Telegram bot menu by selecting **Menu > Alert Settings > Banana Gun**.
