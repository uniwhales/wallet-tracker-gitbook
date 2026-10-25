---
description: >-
  How your account and trading wallets are protected, and what you can do to
  keep them safe.
---

# Security

Cielo gives you trading wallets inside the app, so the account that controls them needs to be hard to take over. This page explains how sign-in works, what passkeys protect, how your wallet keys are stored, and the habits that keep your funds safe.

## How you sign in

You can sign in to Cielo in two ways, and you can link both to the same account.

| Method             | How it works                                                                                                                                                                           |
| ------------------ | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Web wallet**     | Connect a Solana or EVM wallet (Phantom, MetaMask, Robinhood Wallet and others) and sign a message. The signature proves you own the wallet. It never gives Cielo access to its funds. |
| **Social account** | Sign in with Google, X or Telegram. In Telegram you can also send `/signin` to the Cielo bot.                                                                                          |

{% embed url="https://x.com/CieloFinance/status/2054259973459247449" %}

Manage your sign-in methods in **Settings > Account**. **Connected Wallet** shows the wallet linked to your account, and **Socials** lets you connect or unlink Google, X and Telegram.

{% hint style="info" %}
Linking a new social account asks for proof that it's really you: your passkey if you have one, or a one-time signature from your account wallet. If you only use social sign-in and have no passkey yet, Cielo asks you to set one up first. This stops someone with access to an open session from attaching their own login to your account.
{% endhint %}

## Passkeys

A passkey is a second check on the actions that move money or keys out of your account. When you withdraw, export a private key or link a mobile device, Cielo asks you to confirm with Face ID, Touch ID, Windows Hello or your device PIN. Someone who gets into your session still can't withdraw your funds or export your keys without your device. If you sign in with a wallet and haven't added a passkey, you confirm these actions with a signature from that wallet instead.

Anyone can add a passkey. If you sign in with Google, X or Telegram, you need one: a social login has no wallet to sign with, so the passkey is how you confirm these actions. If you sign in with a wallet, a passkey is optional.

### What a passkey confirms

* Withdrawals from your trading wallets
* Private key exports
* Linking a mobile device to your account (see [Sign in on your phone](security.md#sign-in-on-your-phone))
* Linking a new social account or wallet

Passkeys don't change how you trade. Buys, sells, limit orders and trading agents run without a passkey prompt.

### Add a passkey

1. Go to **Settings > Account** and scroll to **Passkeys**.
2. Click **Add passkey**.
3. Follow your browser or device prompt. Your passkey is saved in your password manager, such as iCloud Keychain, Google Password Manager or 1Password.
4. The passkey appears in the list with the date you added it and when it was last used.

Add more than one, for example one on your laptop and one on your phone. Adding or removing a passkey asks you to confirm with an existing one, so a second passkey is your backup if you lose a device.

{% hint style="info" %}
Some password managers list the Cielo passkey as **cielo:** followed by a number rather than your email or handle. It's still your Cielo passkey.
{% endhint %}

## Sign in on your phone

**Link Mobile Device**, a button in the top bar, signs your phone in to Cielo by QR code, so you don't have to connect a wallet on mobile.

1. Click **Link Mobile Device**.
2. Click **Verify Ownership** and prove it's your account: sign with your account wallet, or confirm with your passkey if you signed up with a social account.
3. A QR code appears. Scan it with your phone's camera to open Cielo signed in.

The phone session can trade, but it can't deposit or withdraw.

{% hint style="danger" %}
The QR code logs whoever scans it in to your account. Never share it or a screenshot of it, and close it before you share your screen.
{% endhint %}

## Your trading wallets

Your trading wallets are embedded wallets secured by [Turnkey](https://www.turnkey.com), a provider that specializes in wallet key management.

You own these wallets. You can export the private key of any trading wallet at any time from **Portfolio > Wallets** (the key icon on the wallet's row) and import it into another wallet app. Exporting needs your passkey or a wallet signature.

{% hint style="danger" %}
Anyone with your private key controls the wallet. Never paste it into a website, a Telegram chat or a support ticket. Cielo staff will never ask for it.
{% endhint %}

## Withdrawals

To withdraw, open the wallet menu in the top right, pick the wallet and click **Withdraw**. Choose the chain, enter the amount and the destination address, then click **Review withdrawal**. The review screen shows:

* The full destination address, with a link to it on the block explorer
* The amount and currency
* The network

Check the address character by character, then confirm. If you sign in with a social account, you confirm with your passkey, and Cielo walks you through setting one up if you don't have one yet. Withdrawals are final: crypto sent to the wrong address or the wrong network can't be recovered.

## Keep your account safe

* Add a passkey, especially if you sign in with a social account.
* Bookmark [app.cielo.finance](https://app.cielo.finance) and use the bot links on the [Telegram](discord-+-telegram-bots/getting-started.md) page instead of links from DMs.
* Ignore DMs offering support. The Cielo team will never DM you first, ask for your private key or seed phrase, or ask you to "verify" your wallet on another site.
* Don't visit links in the names of tokens that show up in your wallet unasked. It's a common phishing trick.
* Keep your [private Telegram bot](discord-+-telegram-bots/telegram-private-bot.md) tokens secret. Anyone with one can send messages as your bot.
* Keep only what you trade in your trading wallets, and move profits you're not using to a wallet you control offline.

## Report a problem

If you think someone has accessed your account, move your funds to a wallet you control, remove any passkeys you don't recognize and unlink social accounts you didn't add.
