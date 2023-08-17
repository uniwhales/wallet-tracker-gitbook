# Telegram

It's possible to use the Cielo Wallet Tracker as a standalone Telegram bot, without pairing it to the Cielo web app.

It's recommended that you use the bot in conjunction with the Cielo [web app](https://app.cielo.finance) however. The app is free to use and its interface makes it easier to adjust wallet settings than doing so within Telegram. If you'd rather just use the Telegram bot on its own, however, read on.

To initialize the [Cielo Wallet Tracker bot](https://t.me/evmtrackerbot), open it in Telegram and press the blue **Start** button.

<figure><img src="../.gitbook/assets/Screenshot 2023-06-18 at 19.10.51.png" alt=""><figcaption></figcaption></figure>

Press the blue menu icon to view wallet settings:

<figure><img src="../.gitbook/assets/Screenshot 2023-06-18 at 19.14.12.png" alt="" width="261"><figcaption></figcaption></figure>

Four options are displayed:

* **Add wallet or token**: Input the address and label for a wallet you wish to track or the smart contracxt address for a token.
* **List**: View all of the wallets that you're currently tracking. You can then click on the edit option beside each wallet to adjust its settings.
* **Menu**: View master menu that includes options for setting group and channel alerts.
* **Bot settings**: Opens options to disable bot or reset chat.



### Adding a wallet

To add a wallet using the Telegram bot, click the blue menu icon followed by the top option that appears: **Add new wallet or token**.

<figure><img src="../.gitbook/assets/Screenshot 2023-06-18 at 19.23.49.png" alt=""><figcaption></figcaption></figure>

Then click the **Wallet** button and paste in the wallet address followed by a space and then an optional name for the wallet e.g. _My Trading Wallet_. By default, all of the chains that Cielo tracks are enabled. If you wish to disable alerts for any of these chains, just click the relevant button to disable the selection.

<figure><img src="../.gitbook/assets/Screenshot 2023-06-18 at 19.26.29.png" alt=""><figcaption></figcaption></figure>

When you're done, click **Confirm**. You'll then see the following screen for controlling tx types:

<figure><img src="../.gitbook/assets/Screenshot 2023-06-18 at 19.27.13.png" alt=""><figcaption></figcaption></figure>

Click on a tx type you wish to disable and then hit **Confirm**. You will now see the following notification:

<figure><img src="../.gitbook/assets/Screenshot 2023-06-18 at 19.29.03.png" alt=""><figcaption></figcaption></figure>

And that's it: you're now tracking your first wallet using Cielo's Telegram bot.&#x20;

### Adding a token

To start tracking a token, repeat the procedure described above but select the **Token** button. You will then see the following option:

<figure><img src="../.gitbook/assets/Screenshot 2023-08-16 at 10.17.20.png" alt=""><figcaption></figcaption></figure>

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

By default, Cielo Wallet Tracker alerts include a **Chart** link, where applicable. By default this links to [GeckoTerminal](https://www.geckoterminal.com/) where you can view trading data for the token in question.

<figure><img src="../.gitbook/assets/Screenshot 2023-06-19 at 14.47.30.png" alt=""><figcaption></figcaption></figure>

Cielo allows you to choose which trading terminal you would like the **Chart** link to direct to. To adjust this setting, click the blue menu icon in the Cielo Wallet Tracker to pull up the main menu and then select **Alert Settings** followed by **Chart**.

<figure><img src="../.gitbook/assets/Screenshot 2023-06-19 at 14.50.02.png" alt=""><figcaption></figcaption></figure>

Then choose which of the four available terminals you would like to use for charting and hit **Confirm**.
