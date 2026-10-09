---
title: "Apple Wallet Pass API – WebViewGold for iOS Documentation"
description: "Let users add .pkpass passes (tickets, coupons, membership cards) from your web app to Apple Wallet."
lang: "en"
product: "WebViewGold for iOS"
platform: "iOS"
category: "APIs & Features"
slug: "wallet-pass"
canonical_url: "https://www.webviewgold.com/docs/iOS/wallet-pass/"
keywords:
  - "Apple Wallet Pass API"
  - "WebViewGold for iOS"
  - "convert website to app"
  - "WebView app documentation"
  - "iOS WebView SDK"
  - "PWA to app"
  - "HTML to app"
  - "JavaScript bridge"
last_updated: "2026-10-09"
---

# Apple Wallet Pass API – WebViewGold for iOS

> **Summary:** Let users add .pkpass passes (tickets, coupons, membership cards) from your web app to Apple Wallet.

[Documentation](../README.md) › [WebViewGold for iOS](README.md) › Apple Wallet Pass API

**Platform:** iOS · **Category:** APIs & Features · **Online version:** [www.webviewgold.com/docs/iOS/wallet-pass/](https://www.webviewgold.com/docs/iOS/wallet-pass/)

---

The **Apple Wallet Pass API** lets your web app hand a `.pkpass` file (event ticket, boarding pass, coupon, loyalty or membership card) to the user so they can add it to **Apple Wallet**.

## How to Use

Link to your `.pkpass` file, but replace the `https://` prefix of the file URL with `addpkpass://`:

```html
<a href="addpkpass://example.com/passes/ticket.pkpass">Add ticket to Apple Wallet</a>
```

## How It Works

1. The app converts the `addpkpass://` link back to a `https://` URL.
2. The pass URL is opened in an in-app browser tab, which recognizes the `.pkpass` content and shows the native **Add to Apple Wallet** preview.
3. The user confirms and the pass is stored in the Wallet app.

**Notes:** The pass must be served over HTTPS with the correct `application/vnd.apple.pkpass` MIME type, and it must be signed with a valid Apple Pass Type ID certificate (see the [Apple Wallet Passes documentation](https://developer.apple.com/documentation/walletpasses) for how to generate passes).

---

## Continue reading

- ← Previous: [iCal Calendar API](ical-calendar.md)
- Next →: [UUID API](uuid.md)
- Languages: **🇺🇸 English** · [🇩🇪 Deutsch](../de/ios/wallet-pass.md) · [🇫🇷 Français](../fr/ios/wallet-pass.md) · [🇪🇸 Español](../es/ios/wallet-pass.md) · [🇨🇳 中文](../zh/ios/wallet-pass.md)

> [!TIP]
> **Too busy? We set up your app for you.** Our team configures, builds & submits your WebViewGold app — done-for-you, fast turnaround, Made in Germany. [Get your app set up →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **Build in your browser:** No Mac, no IDE: the **WebViewGold Cloud Builder** configures, builds & uploads your app online. [Discover Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
