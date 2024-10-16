# My Wallets

[**My Wallets**](https://app.cielo.finance/my-wallets) is your mission control. It’s where you add, edit, and delete wallets and lists. It’s also where you control the Telegram/Discord alerts you receive for wallets and lists you’re following.

### Contents

1. [**Adding Wallets**](./#adding-wallets)
2. [**Editing Wallets**](./#editing-wallets)
3. [**Bulk Edits**](./#bulk-edits)
4. [**New Trade Alerts**](./#new-trade-alerts)
5. [**Token Filters**](./#token-filters)



## Adding Wallets

Click **Add Wallets** in the top right to add a wallet to your Cielo feed. You can add an Ethereum address, Solana address, ENS, or .sol.

<figure><img src="../.gitbook/assets/Screenshot 2024-03-03 at 13.22.56.png" alt="" width="350"><figcaption><p>Add Wallets popup</p></figcaption></figure>

\
Enter the wallet address and add an optional label for identification e.g. _Vitalik_. If you wish to add and configure Telegram/Discord bot alerts for the wallet, select **Alert Settings** and follow the instructions. Here you can specify notifications based on tx type, chain, and minimum USD value for swaps. You can also check the **New Trade Alerts** box to receive an alert when the wallet trades a token for the first time – see [below](./#new-trade-alerts) for more information on this feature.\


{% hint style="info" %}
**Note:** **Alert Settings** only applies filters to your Telegram or Discord bots. It does not filter the tx that appear in your Cielo feed. To change the default view for your feed, use the tabs at the top of the Feed page.\

{% endhint %}

If you wish to add multiple wallets at once, select **Bulk Import** and you can upload a CSV file. Wallet addresses should be placed in column one and an optional label for each one should go in column two.

## Editing Wallets

Tick the checkbox at the top of the page to select all wallets or select individual wallets and make edits to them. You can also use the tabs at the top of the **My Wallets** page to filter wallets by list, type, chain,  and whether they are currently unassigned to a list.

<figure><img src="../.gitbook/assets/Screenshot 2024-03-03 at 13.49.33.png" alt=""><figcaption></figcaption></figure>

After selecting one or more wallets, click the pencil icon to make edits. When you're done, click **Save Changes**.



## Bulk Edits

You can edit multiple wallets to save time. This allows you to bulk edit Telegram/Discord alerts for all of the wallets you're following or a subset of wallets. For instance, you can enable Telegram alerts for _Swaps over $100_ or for _NFT Mints on Base_. You will still be able to see all of the onchain activity for these wallets in your Cielo feed but will only receive bot alerts for tx that match your criteria.

To make a bulk edit, click the checkbox in the top left of the screen. This will select all wallets on the page. To select all wallets that youi're following, click **Select all XXX of your wallets**:



<figure><img src="../.gitbook/assets/Screenshot 2024-04-04 at 10.26.26.png" alt=""><figcaption></figcaption></figure>

You can alternatively select all wallets within a specific list. To do so, click the **Lists** tab at the top of the page and select the desired list. Then tick the **All Wallets** box.

When you have selected the wallets you wish to bulk edit, click **Alert Settings** or **Token / NFT Filters** _(Pro+Whale)_ at the bottom of the page.



## New Trade Alerts

Available to Pro and Whale users, New Trade Alerts enables you to receive an alert whenever a wallet you're following trades a particular token for the first time. To enable this feature, in **My Wallets** click the edit icon alongside a particular wallet and then click the tab marked **Alert Settings**. (Alternatively, select all wallets on a page or within a list and then click the **Alert Settings** button to make bulk edits.)

For the wallet(s) selected, click the **New Trade Alerts** switch to activate this feature. In the **Wallet Info** tab, make sure you have assigned the wallet(s) to a particular bot. You will now receive a bot alert whenever the selected wallet(s) trades a particular token for the first time.



<figure><img src="../.gitbook/assets/Screenshot 2024-09-29 at 15.52.21.png" alt="" width="357"><figcaption><p>Toggle the New Trade Alerts switch to activate this feature</p></figcaption></figure>



## Token Filters

Cielo allows you set alerts when a wallet you're following trades specific tokens or NFTs _(Pro+Whale)._ That way you can receive a notification when wallets swap particular tokens you're interested in and screen the rest of their onchain activity.

To set an alert, in **My Wallets** click the filter icon for a particular wallet or select all wallets if you want to batch add a token alert.

<figure><img src="../.gitbook/assets/Screenshot 2024-03-27 at 19.36.32.png" alt="" width="342"><figcaption><p>Click the filter icon on the right to add a token alert</p></figcaption></figure>

In the popup window that appears, enter the token address and chain for each token alert you wish to add. You can enable up to 10 unique token alerts per wallet.





\
\
