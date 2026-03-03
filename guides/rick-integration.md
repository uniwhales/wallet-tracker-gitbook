# Rick Integration

[Rick](https://t.me/rickbot) is a popular Telegram and Discord token scanner. Cielo has a native integration with Rick via its custom trade buttons system, allowing you to open any token Rick surfaces directly in the Cielo Terminal with one tap.

#### Setting It Up

In your Rick bot, use the `/tb` command and include **CLO** to add the Cielo button:

```
/tb CLO
```

You can adjust the position and how many buttons are shown:

* `/tb top` — move buttons above the alert
* `/tb bot` — move buttons below (default)
* `/tb 4` — show up to 4 buttons (max 6)

#### Using the CLO Button

Once set up, a **🌙 CLO** button will appear at the bottom of every Rick token scan. Tapping it opens that token directly in the Cielo Terminal, where you can view the chart, see wallet activity, and trade without having to search or copy-paste the token address

<figure><img src="../.gitbook/assets/image (8).png" alt="" width="375"><figcaption></figcaption></figure>
