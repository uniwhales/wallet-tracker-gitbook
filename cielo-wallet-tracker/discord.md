# Discord

Cielo allows you to add a custom bot that will share notifications within a Discord channel. You can enable this feature and customize the bot using the Cielo web app. You will also require admin rights for the channel within the Discord server you intend to use. If the server owner is unwilling to grant you admin privileges within the Discord channel, you will be unable to connect a Cielo bot.

{% hint style="info" %}
If the owner of a Discord server is willing to allow a Cielo bot to be added to a channel, but does not wish to share admin rights, they can connect to the Cielo [web app](https://app.cielo.finance/) themselves and complete the process. Each Cielo user can access one Discord bot for free.
{% endhint %}

To activate a Discord bot, first make sure your web wallet is connected to [Cielo](https://app.cielo.finance/). In [configure](https://app.cielo.finance/configure), click the Discord icon in the top right, connect to Discord and select the server you wish to authenticate. Then return to Cielo, refresh the configure page and click the Discord icon again. You will now be able to select a channel within the Discord server you have connected to receive bot notifications.

<figure><img src="../.gitbook/assets/Screenshot 2023-08-16 at 14.57.20.png" alt=""><figcaption><p>Discord activated within the Cielo app.</p></figcaption></figure>



## FAQ

* How many Discord bots can I run?

You can run a maximum of one Discord bot per Cielo account. This applies to all Discord servers that you may be a member of.

\


* How do I activate a Discord bot?

Go to [configure](https://app.cielo.finance/configure), click the Discord icon in the top right, connect to Discord and select the server you wish to authenticate. Then return to Cielo, refresh the configure page and click the Discord icon again. You will now be able to select a channel with the Discord server you connected to receive bot notifications.

\


* How do I choose which notifications are sent to my Discord channel?

After linking your Cielo and Discord accounts, the next step is to assign specific lists or wallets to your Discord bot. You can do this in [configure](https://app.cielo.finance/configure) by clicking on the toggle icon for advanced list settings. Click the dropdown menu from the Discord Channel box, make your selection and hit Save changes.

\


* How do I add a Cielo public list to my Discord channel?

After following a public list, go to [configure](https://app.cielo.finance/configure) and select the name of the list from the dropdown menu. Then click the toggle icon for advanced list settings and enable Discord alerts.

\


* How do I remove the bot from Discord?

Go to [configure](https://app.cielo.finance/configure) and click the Discord icon in the top right. To remove the bot from the channel it is assigned to, click the trashcan icon alongside the channel name. To remove the bot from the Discord server altogether, click the trasjcan icon alongside the Discord server name.

\


* I’ve connected Cielo but transactions aren’t showing up in Discord.

Have you double-checked that Discord is connected to Cielo, and that a channel within your chosen server has been specified? If you’re still not seeing transactions appearing, check the settings for any lists and wallets you have assigned to the Discord bot. In particular, make sure that you have not set a minimum USD transaction threshold to all wallets. This can result in the vast majority of tx being screened out. If you’re still not seeing Discord notifications, check the list you’ve assigned to the Discord bot and, on configure, click to filter it by Last Active. This will show you when a wallet within the list last made an onchain transaction.

\


* I am receiving too many Discord notifications

To dial down the number of alerts you’re receiving, on configure select the lists or wallets whose activity is being sent to the Discord bot. Then click the toggle slider on configure to pull up advanced list settings and apply filters that will reduce the number of alerts you receive. For example, you can raise the minimum transaction threshold or filter out certain transaction types or networks. If you are still receiving too many notifications, reduce the number of wallets and lists that are paired with the Discord bot.

\