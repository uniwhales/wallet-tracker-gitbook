# Customize



[Customize](https://app.cielo.finance/customize) is the nerve center of Cielo. It’s where you control not only what appears in your Feed, but also in your EVM Wallet Tracker bot Telegram channels. In Customize you can:

* Create custom lists
* Import premade Cielo lists
* Activate and deactivate wallets you’re following
* Rename wallets and map them to different bots
* Set advanced filters for tx alerts

## Getting started

If you have no wallets assigned to your Telegram bots, the Customize page shows the following message:

<figure><img src=".gitbook/assets/unnamed (8).png" alt=""><figcaption></figcaption></figure>

You can start adding wallets by pasting their address into the box on the right hand side. Let’s run through an example of how to do that.

We’re going to create an alert for the following address:

_0xAb5801a7D398351b8bE11C439e05C5B3259aeC9B_

This is one of Vitalik Buterin’s known public wallets. It’s already labeled as such on [Etherscan](https://etherscan.io/address/0xab5801a7d398351b8be11c439e05c5b3259aec9b). Here’s how to add it to Cielo:

1. Paste the address into the **Wallet Address** field.
2. Add an optional label. Here, we’ll call it VB.
3. Choose which List you wish to assign it to. In this example, we only have one List created so it will default to **All**.
4. Choose which bot you wish to assign the wallet to (Whale members only).
5. Click **Add Alert**.

<figure><img src=".gitbook/assets/unnamed (9).png" alt=""><figcaption></figcaption></figure>

And that’s it. You’re now following your first wallet in Cielo.

You’ll see the wallet appear on the Customize page like so:

<figure><img src=".gitbook/assets/unnamed (10).png" alt=""><figcaption></figcaption></figure>

Go to your Cielo Feed and you’ll see it’s now populated with recent tx involving this wallet. As you can see, Vitalik’s address receives a lot of spam tx.

<figure><img src=".gitbook/assets/unnamed (11).png" alt=""><figcaption></figcaption></figure>

Now let’s return to Customize and add a second wallet. This time we’ll go with an ENS address. _99th.eth_ is an active NFT collector with a few BAYC to their name. There’s no need to add their wallet address: the ENS will suffice.

This time, let’s click **Advanced Settings** and include some additional filters. In the pop-up that appears you can set a minimum transaction value (in USD), deselect any chains you don’t wish to receive alerts for, and do the same for transaction types you wish to screen under **Alert Filter**.

{% hint style="info" %}
**Note:** Advanced Settings only filters tx that appear in your Telegram bot. It does not exert any effect on Cielo. For example, if you select _Avalanche_ only under Advanced Settings, your Telegram bot will only show tx from that occur on Avalanche network – but Cielo will display tx across all 12 EVM chains.
{% endhint %}

When you’ve finished adjusting Advanced Settings, click the blue **Add Alert** button and within a couple of seconds the wallet will appear in your list of addresses on the Customize page.

<figure><img src=".gitbook/assets/unnamed (12).png" alt=""><figcaption></figcaption></figure>

Now let’s adjust some settings for the two wallets we’ve just added. As you can see, the bot that each address is assigned to is clearly displayed, while hovering over the wallet address allows you to copy it to clipboard.

Click on the three horizontal dots and you’ll be given three options:

**Profile**: Takes you to a Cielo page showing all recent tx for that address.

**Edit Alert**: Opens a popup where you can adjust the wallet name, bot, and any lists it’s assigned to.

**Unfollow**: Delete the wallet from your Cielo dashboard and Telegram altogether.

The final option that appears alongside each wallet is a blue button. Click on this to disable Telegram alerts for the wallet.

{% hint style="info" %}
**Note**: After switching off the blue button, the wallet will remain in Cielo and its tx will be visible in your Cielo Feed. It will only disappear from the Telegram bot channel. Click the button again to re-enable Telegram alerts.
{% endhint %}

## Bulk Actions

Near the top of the Customize page is an option titled **Bulk Actions**. Clicking on this produces a range of editing options you can apply to some or all wallets you’ve added. Click **Bulk Actions** again and a tick icon will appear alongside all of your wallets. Now click on any wallet(s) you _don’t_ wish to edit. Finally, click on the action you wish to perform (e.g. _Unfollow_) and it will be applied to all wallets that have been ticked.

The **Bulk Actions** option is particularly useful when managing a large number of wallets.

<figure><img src=".gitbook/assets/unnamed (13).png" alt=""><figcaption></figcaption></figure>
