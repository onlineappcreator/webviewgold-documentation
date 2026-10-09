---
title: "In-App Rating Dialog API – WebViewGold for iOS Documentation"
description: "Ask users for an App Store rating at the perfect moment — trigger the native iOS rating dialog from your web app."
lang: "en"
product: "WebViewGold for iOS"
platform: "iOS"
category: "APIs & Features"
slug: "in-app-rating"
canonical_url: "https://www.webviewgold.com/docs/iOS/in-app-rating/"
keywords:
  - "In-App Rating Dialog API"
  - "WebViewGold for iOS"
  - "convert website to app"
  - "WebView app documentation"
  - "iOS WebView SDK"
  - "PWA to app"
  - "HTML to app"
  - "JavaScript bridge"
last_updated: "2026-10-09"
---

# In-App Rating Dialog API – WebViewGold for iOS

> **Summary:** Ask users for an App Store rating at the perfect moment — trigger the native iOS rating dialog from your web app.

[Documentation](../README.md) › [WebViewGold for iOS](README.md) › In-App Rating Dialog API

**Platform:** iOS · **Category:** APIs & Features · **Online version:** [www.webviewgold.com/docs/iOS/in-app-rating/](https://www.webviewgold.com/docs/iOS/in-app-rating/)

---

Positive App Store reviews are one of the most powerful growth drivers for your app. The **In-App Rating Dialog API** of WebViewGold lets you ask your users for a rating at exactly the right moment — for example, right after a successful purchase or after they completed a task in your web app.

## Option 1: Native iOS rating dialog (default)

Call the following URL from an HTML link or from JavaScript to show the native **SKStoreReviewController** rating dialog:

```html
<a href="rateapp://">Enjoying the app? Rate us!</a>
```

```javascript
window.location.href = "rateapp://";
```

**Note:** Apple limits how often the native rating dialog may be displayed (about three times per year per user), so it might not appear on every call — this is by design and also applies during development.

## Option 2: Custom rating dialog

If you prefer a dialog that always appears and sends the user to your App Store page instead, configure it in **Config.swift**:

- `showcustomrateappdialog` — set to `true` to show a custom rate dialog when triggering `rateapp://` instead of attempting the native review call.
- `ratemyappurl` — set the App Store URL of your app, e.g. `https://apps.apple.com/app/idXXXXXXXXX?action=write-review`.

## Typical Use Cases

- Ask for a review right after a positive interaction (completed order, level up, successful booking).
- Show your own custom "Do you like the app?" flow on your website first, and only send happy users to `rateapp://`.

---

## Continue reading

- ← Previous: [App Sharing Dialog API](app-sharing-dialog.md)
- Next →: [In-App Purchases API](in-app-purchases.md)
- Same feature on other platforms: [Android – In-App Rating API](../android/in-app-rating.md)
- Languages: **🇺🇸 English** · [🇩🇪 Deutsch](../de/ios/in-app-rating.md) · [🇫🇷 Français](../fr/ios/in-app-rating.md) · [🇪🇸 Español](../es/ios/in-app-rating.md) · [🇨🇳 中文](../zh/ios/in-app-rating.md)

> [!TIP]
> **Too busy? We set up your app for you.** Our team configures, builds & submits your WebViewGold app — done-for-you, fast turnaround, Made in Germany. [Get your app set up →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **Build in your browser:** No Mac, no IDE: the **WebViewGold Cloud Builder** configures, builds & uploads your app online. [Discover Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
