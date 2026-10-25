---
description: >-
  Pro + Whale users can create private Telegram bots for more consistent alert
  delivery.
---

# Telegram Private Bot

Cielo provides a number of Telegram bots that can be used to receive custom alerts. Free users can access **one** bot, Pro users **two**, and Whale users **nine**. These bots are accessed by all Cielo users who share a corresponding plan. Due to limitations in Telegram’s architecture, however, the demand placed on these bots can occasionally cause alerts to be dropped or delayed.

To resolve this, Cielo Pro + Whale users can create private bots that are exclusive to their personal use. This will ensure that alerts are delivered promptly and consistently. Just as experienced onchain users can create a custom RPC to access a faster blockchain connection, creating a private Cielo bot ensures a consistent alert stream.

{% hint style="info" %}
Private Telegram bots are available _in addition_ to your existing Cielo bots e.g. if you are a Pro user, the two bots you currently have can now be complemented by two additional private bots.
{% endhint %}

## Creating a Private Bot <a href="#creating-a-custom-bot" id="creating-a-custom-bot"></a>

Follow these steps to set up your private bot:

1. Visit [BotFather](https://t.me/BotFather) on Telegram, click the menu and select _/newbot_
2. Assign your bot a name like _Cielo Private Bot 1_
3. Select a unique username ending in 'bot'
4. Copy the token BotFather displays in red (formatted like _7024425312:AGHJo0WgmLqkaWzMgxO7tdqhvXzxVUJQR2c_) without sharing it publicly
5. Open the Cielo web app and go to [Settings > Alerts](https://app.cielo.finance/settings/alerts)
6. In the private bots section, add a new bot and paste in your BotFather token
7. Repeat for additional bots, up to your plan's limit
8. Go to [Tracking](https://app.cielo.finance/tracking) to assign wallets to your private bot(s)

You can create as many private bots as your current Cielo plan permits. Visit [Alerts](https://app.cielo.finance/settings/alerts) in the Cielo web app and you will see all of your private bots listed.

Type _/start_ in your private bot to load the Cielo menu. You can also add private bots to Telegram groups and topics just as you can with a regular Cielo bot.

<figure><img src="https://1250667054-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FgZTvWhkjLJ8uCLtiUaPq%2Fuploads%2FtweuFe94oL2Q8njRYJnU%2FScreenshot%202024-06-27%20at%2012.46.16.png?alt=media&#x26;token=3fe3daa9-bdf9-4563-ab18-f5a5f14deb91" alt=""><figcaption><p>After creating a private bot, it will appear in <strong>Tracking</strong> as a bot you can assign alerts to.</p></figcaption></figure>

To make it easier to keep track of your Cielo bots, including private bots, it is recommended that you create a dedicated Telegram folder and assign all bots to it.

{% hint style="info" %}
The alerts you assign to your private bot must be made using the Cielo web app. In every other respect, however, your private bot will operate as normal with the added bonus of greater speed and reliability.
{% endhint %}
