---
title: "In-App Purchase & In-App Subscription API – WebViewGold for macOS Documentation"
description: "Sell Mac App Store in-app purchases and subscriptions from your web app: add your product ID in Constants.h and trigger purchases with inapppurchase:// links."
lang: "en"
product: "WebViewGold for macOS"
platform: "macOS"
category: "APIs & Features"
slug: "in-app-purchases"
canonical_url: "https://www.webviewgold.com/docs/mac/#inapppurchases"
keywords:
  - "In-App Purchases API"
  - "WebViewGold for macOS"
  - "convert website to app"
  - "WebView app documentation"
  - "macOS WebView SDK"
  - "PWA to app"
  - "HTML to app"
  - "JavaScript bridge"
last_updated: "2026-10-09"
---

# In-App Purchase & In-App Subscription API – WebViewGold for macOS

> **Summary:** Sell Mac App Store in-app purchases and subscriptions from your web app: add your product ID in Constants.h and trigger purchases with inapppurchase:// links.

[Documentation](../README.md) › [WebViewGold for macOS](README.md) › In-App Purchases API

**Platform:** macOS · **Category:** APIs & Features · **Online version:** [www.webviewgold.com/docs/mac/#inapppurchases](https://www.webviewgold.com/docs/mac/#inapppurchases)

---

Within some macOS/Mac apps, you can buy additional content or services. These kinds of purchases are called "in-app purchases". They can be an attractive source of revenue for developers and are very convenient for customers as they use existing accounts and payment sources for settlement. WebViewGold allows triggering Mac App Store In-App Purchases. Just add your In-App Purchase Product ID (obtained from *App Store Connect*) in the *Constants.h* file: \
![Mac App Store In-App Purchase Product ID in Constants.h file](../assets/macos/img/inapppurchase.png)\
Afterward, just link to this kind of URL:

```html
<a href="inapppurchase://?successful_url=https://www.google.com">Buy In-App Purchase</a>
```

Alternatively, use this kind of URL for subscription products:

```html
<a href="inappsubscription://?successful_url=https://www.google.com&expired_url=https://www.yahoo.com">Start In-App Subscription</a>
```

In this URL example, https://www.google.com should be called after the successful subscription activation, and https://www.yahoo.com should be called as soon as the subscription is expired.

---

## Continue reading

- ← Previous: [Splash Screen](splash-screen.md)
- Next →: [UUID API](uuid.md)
- Same feature on other platforms: [iOS – In-App Purchases API](../ios/in-app-purchases.md) · [Android – In-App Purchases API](../android/in-app-purchases.md)
- Languages: **🇺🇸 English** · [🇩🇪 Deutsch](../de/macos/in-app-purchases.md) · [🇫🇷 Français](../fr/macos/in-app-purchases.md) · [🇪🇸 Español](../es/macos/in-app-purchases.md) · [🇨🇳 中文](../zh/macos/in-app-purchases.md)

