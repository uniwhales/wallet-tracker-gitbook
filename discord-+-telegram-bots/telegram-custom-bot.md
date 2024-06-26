---
description: >-
  Pro + Whale users can create custom Telegram bots for more consistent alert
  delivery.
---

# Telegram custom bot

Cielo provides a number of Telegram bots that can be used to receive custom alerts. Free users can access **one** bot, Pro users **two**, and Whale users **nine**. These bots are accessed by all Cielo users who share a corresponding plan. Due to limitations in Telegram’s architecture, however, the demand placed on these bots can occasionally cause alerts to be dropped or delayed.

To resolve this, Cielo Pro + Whale users can create custom bots that are exclusive to their personal use. This will ensure that alerts are delivered promptly and consistently. Just as experienced onchain users can create a custom RPC to access a faster blockchain connection, creating a custom Cielo bot ensures a consistent alert stream.

## Creating a Custom Bot <a href="#creating-a-custom-bot" id="creating-a-custom-bot"></a>

Creating a custom bot is quick and easy. Here’s how:

1. Go to [BotFather](https://t.me/BotFather) on Telegram, click the menu button and select _/newbot_
2. Give your bot a name e.g. _Cielo Custom Bot 1_
3. Choose a username for your bot. This must be a unique name that is not currently used on Telegram and must end with ‘bot’
4. Copy the token that BotFather displays in red. It will read something like _7024425312:AGHJo0WgmLqkaWzMgxO7tdqhvXzxVUJQR2c_
5. Now visit the Telegram menu for an existing Cielo bot e.g. _Cielo Premium Bot #1_ (The only bot this will not work with is the free bot titled _Cielo Wallet Tracker_)
6. Click the button marked _Add custom bot_
7. Paste in the API token
8. Repeat this process with as many bots as you wish to add
9. Click the menu button marked _Custom bots_ to see a list of all custom bots you have active
10. Open the Cielo web app, go to [My Wallets](https://app.cielo.finance/my-wallets) and you can start assigning wallets to your custom bot(s).

<figure><img src="../.gitbook/assets/Screenshot 2024-06-26 at 14.45.59.png" alt=""><figcaption><p>Select "Add custom bot" from the menu of an existing Cielo Telegram bot.</p></figcaption></figure>

You can create as many custom bots as your current Cielo plan permits. Visit [Alerts](https://app.cielo.finance/settings/alerts) in the Cielo web app and you will see all of your custom bots listed.

To make it easier to keep track of your Cielo bots, including custom bots, it is recommended that you create a dedicated Telegram folder and assign all bots to it.

{% hint style="info" %}
The alerts you assign to your custom bot must be made using the Cielo web app. The normal menu options available with a regular Cielo Telegram bot, such as for adding wallets, are unavailable with a custom bot.\
\
In every other respect, however, your custom bot will operate as normal with the added bonus of greater speed and reliability.
{% endhint %}

