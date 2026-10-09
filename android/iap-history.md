---
title: "In-App Purchase History API – WebViewGold for Android Documentation"
description: "Return the user's Google Play purchase history as window.purchaseHistory so your web app can list subscriptions or unlock premium content client-side."
lang: "en"
product: "WebViewGold for Android"
platform: "Android"
category: "APIs & Features"
slug: "iap-history"
canonical_url: "https://www.webviewgold.com/docs/android/iap-history/"
keywords:
  - "IAP History API"
  - "WebViewGold for Android"
  - "convert website to app"
  - "WebView app documentation"
  - "Android WebView SDK"
  - "PWA to app"
  - "HTML to app"
  - "JavaScript bridge"
last_updated: "2026-10-09"
---

# In-App Purchase History API – WebViewGold for Android

> **Summary:** Return the user's Google Play purchase history as window.purchaseHistory so your web app can list subscriptions or unlock premium content client-side.

[Documentation](../README.md) › [WebViewGold for Android](README.md) › IAP History API

**Platform:** Android · **Category:** APIs & Features · **Online version:** [www.webviewgold.com/docs/android/iap-history/](https://www.webviewgold.com/docs/android/iap-history/)

---

The **In-App Purchase History API** returns the list of the user's previous purchases (product IDs, timestamps, tokens) made through Google Play Billing and injects it into your web app as `window.purchaseHistory`. Make sure to own an [Extended License](credits.md) of WebViewGold if you plan to use this feature in an end product.

## How to Use

```html
<a href="getpurchasehistory://" onclick="setTimeout(renderHistory, 300)">My purchases</a>

<script>
function renderHistory() {
  const data = window.purchaseHistory;
  if (!data) return;
  data.purchases.forEach(function (p) {
    console.log(p.productId, p.purchaseTime, p.orderId);
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
      "purchaseTime": 1721600000000,
      "orderId": "GPA.xxxx-xxxx-xxxx",
      "purchaseToken": "..."
    }
  ]
}
```

Exact fields depend on the store record — treat the value as a JSON array to iterate.

## Typical Use Cases

- Show a "My subscriptions" or "My purchases" page inside your web app.
- Client-side unlock of premium content based on past purchases without hitting your backend.
- Debugging and customer-support workflows.

**Notes:** The list contains only purchases made under the currently signed-in Google Play account on this device.

---

## Continue reading

- ← Previous: [In-App Purchases API](in-app-purchases.md)
- Next →: [QR Code Scanner API](qr-code-scanner.md)
- Same feature on other platforms: [iOS – IAP History API](../ios/iap-history.md)
- Languages: **🇺🇸 English** · [🇩🇪 Deutsch](../de/android/iap-history.md) · [🇫🇷 Français](../fr/android/iap-history.md) · [🇪🇸 Español](../es/android/iap-history.md) · [🇨🇳 中文](../zh/android/iap-history.md)

> [!TIP]
> **Too busy? We set up your app for you.** Our team configures, builds & submits your WebViewGold app — done-for-you, fast turnaround, Made in Germany. [Get your app set up →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_android_doc_online)
>
> **Build in your browser:** No Mac, no IDE: the **WebViewGold Cloud Builder** configures, builds & uploads your app online. [Discover Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=android_docs)
