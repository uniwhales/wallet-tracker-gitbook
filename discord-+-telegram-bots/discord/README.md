# Discord

Cielo allows you to add a custom bot that will share notifications within a Discord channel. You can enable this feature and customize the bot using the Cielo web app. You will also require admin rights for the channel within the Discord server you intend to use. If the server owner is unwilling to grant you admin privileges within the Discord channel, you will be unable to connect a Cielo bot.

The bot does not require admin privileges to be added to a public channel: it simply requires the same permissions as an ordinary user, allowing it to post messages. To add the bot to a private channel, however, the bot requires admin rights.

<figure><img src="https://1250667054-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FgZTvWhkjLJ8uCLtiUaPq%2Fuploads%2FAxiJYQgcNZBwdAqH2d2g%2FScreenshot%202023-08-16%20at%2015.01.01.png?alt=media&#x26;token=67c00cfa-8265-473b-8e9d-abb07d9d7078" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
If the owner of a Discord server is willing to allow a Cielo bot to be added to a channel, but does not wish to share admin rights, they can connect to the Cielo [web app](https://app.cielo.finance/) themselves and complete the process. Each Cielo user can access one Discord bot for free.
{% endhint %}

To activate a Discord bot, first make sure you're signed in to [Cielo](https://app.cielo.finance/). In [Alerts](https://app.cielo.finance/settings/alerts), connect to Discord and select the server you wish to authenticate. Then return to Cielo, refresh the page and click the Discord icon again. You will now be able to select a channel within the Discord server you have connected to receive bot notifications.

<figure><img src="https://1250667054-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FgZTvWhkjLJ8uCLtiUaPq%2Fuploads%2FDmx0EKnbTlZUN76XbVx0%2FScreenshot%202023-08-16%20at%2014.57.20.png?alt=media&#x26;token=060d0fa7-8809-428d-bdd4-d192d0159f4a" alt=""><figcaption><p>Discord activated within the Cielo app.</p></figcaption></figure>

## FAQ

* _How many Discord bots can I run?_

Free accounts can run one Discord channel, Pro accounts two, and Whale accounts 20. This applies to all Discord servers that you may be a member of.<br>

* _How do I activate a Discord bot?_

Go to [Alerts](https://app.cielo.finance/settings/alerts), connect to Discord and select the server you wish to authenticate. Then return to Cielo, refresh the page and click the Discord icon again. You will now be able to select a channel within the Discord server you connected to receive bot notifications.

* _How do I choose which notifications are sent to my Discord channel?_

After linking your Cielo and Discord accounts, the next step is to assign specific lists or wallets to your Discord bot. You can do this in [Tracking](https://app.cielo.finance/tracking): select the wallets or list, click **Alert Settings** and pick your Discord channel.

* _How do I add a Cielo public list to my Discord channel?_

After following a public list, go to [Tracking](https://app.cielo.finance/tracking), select the list, click **Alert Settings** and pick your Discord channel.

* _How do I remove the bot from Discord?_

Go to [Alerts](https://app.cielo.finance/settings/alerts). To remove the bot from the channel it is assigned to, click the trashcan icon alongside the channel name. To remove the bot from the Discord server altogether, click the trashcan icon alongside the Discord server name.<br>

* _I’ve connected Cielo but transactions aren’t showing up in Discord._

Have you double-checked that Discord is connected to Cielo, and that a channel within your chosen server has been specified? If you’re still not seeing transactions appearing, check the settings for any lists and wallets you have assigned to the Discord bot. In particular, make sure that you have not set a minimum USD transaction threshold to all wallets. This can result in the vast majority of tx being screened out. If you’re still not seeing Discord notifications, check the list you’ve assigned to the Discord bot and, in Tracking, sort it by Last Active. This will show you when a wallet within the list last made an onchain transaction.<br>

* _I am receiving too many Discord notifications_

To dial down the number of alerts you’re receiving, in Tracking select the lists or wallets whose activity is being sent to the Discord bot. Then click **Alert Settings** and apply filters that will reduce the number of alerts you receive. For example, you can raise the minimum transaction threshold or filter out certain transaction types or networks. If you are still receiving too many notifications, reduce the number of wallets and lists that are paired with the Discord bot.

<br>
