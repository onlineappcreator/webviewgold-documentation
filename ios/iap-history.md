---
title: "In-App Purchase History API – WebViewGold for iOS Documentation"
description: "Read the user's previous in-app purchases from your web app as JSON — perfect for \"My purchases\" pages."
lang: "en"
product: "WebViewGold for iOS"
platform: "iOS"
category: "APIs & Features"
slug: "iap-history"
canonical_url: "https://www.webviewgold.com/docs/iOS/iap-history/"
keywords:
  - "IAP History API"
  - "WebViewGold for iOS"
  - "convert website to app"
  - "WebView app documentation"
  - "iOS WebView SDK"
  - "PWA to app"
  - "HTML to app"
  - "JavaScript bridge"
last_updated: "2026-10-09"
---

# In-App Purchase History API – WebViewGold for iOS

> **Summary:** Read the user's previous in-app purchases from your web app as JSON — perfect for "My purchases" pages.

[Documentation](../README.md) › [WebViewGold for iOS](README.md) › IAP History API

**Platform:** iOS · **Category:** APIs & Features · **Online version:** [www.webviewgold.com/docs/iOS/iap-history/](https://www.webviewgold.com/docs/iOS/iap-history/)

---

The **In-App Purchase History API** returns the list of the user's previous purchases made through the [In-App Purchases API](in-app-purchases.md) on this device and injects it into your web app as `window.purchaseHistory`. Make sure to own an [Extended License](credits.md) of WebViewGold if you plan to use this feature in an end product.

## How to Use

```html
<a href="getpurchasehistory://" onclick="setTimeout(renderHistory, 300)">My purchases</a>

<script>
function renderHistory() {
  const data = window.purchaseHistory;
  if (!data) return;
  data.purchases.forEach(function (p) {
    console.log(p.productId, p.transactionId, p.purchaseDateMs);
  });
}
</script>
```

## Payload Shape

```json
{
  "purchases": [
    {
      "productId": "com.example.premium",
      "transactionId": "2000000123456789",
      "purchaseDateMs": "1721600000000"
    }
  ]
}
```

`purchaseDateMs` is the purchase timestamp in Unix milliseconds (as a string).

## Typical Use Cases

- Show a "My subscriptions" or "My purchases" page inside your web app.
- Client-side unlock of premium content based on past purchases without hitting your backend.
- Debugging and customer-support workflows.

**Notes:** The list contains purchases made within the app on this device. It is stored locally, so it does not sync across devices — for cross-device entitlement checks, validate receipts on your server instead.

---

## Continue reading

- ← Previous: [In-App Purchases API](in-app-purchases.md)
- Next →: [QR Code Scanner API](qr-code-scanner.md)
- Same feature on other platforms: [Android – IAP History API](../android/iap-history.md)
- Languages: **🇺🇸 English** · [🇩🇪 Deutsch](../de/ios/iap-history.md) · [🇫🇷 Français](../fr/ios/iap-history.md) · [🇪🇸 Español](../es/ios/iap-history.md) · [🇨🇳 中文](../zh/ios/iap-history.md)

> [!TIP]
> **Too busy? We set up your app for you.** Our team configures, builds & submits your WebViewGold app — done-for-you, fast turnaround, Made in Germany. [Get your app set up →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **Build in your browser:** No Mac, no IDE: the **WebViewGold Cloud Builder** configures, builds & uploads your app online. [Discover Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
