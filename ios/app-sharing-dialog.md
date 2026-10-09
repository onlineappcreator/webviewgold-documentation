---
title: "App Sharing Dialog API – WebViewGold for iOS Documentation"
description: "Trigger the native iOS share sheet from your web app to let users share your app or any URL."
lang: "en"
product: "WebViewGold for iOS"
platform: "iOS"
category: "APIs & Features"
slug: "app-sharing-dialog"
canonical_url: "https://www.webviewgold.com/docs/iOS/app-sharing-dialog/"
keywords:
  - "App Sharing Dialog API"
  - "WebViewGold for iOS"
  - "convert website to app"
  - "WebView app documentation"
  - "iOS WebView SDK"
  - "PWA to app"
  - "HTML to app"
  - "JavaScript bridge"
last_updated: "2026-10-09"
---

# App Sharing Dialog API – WebViewGold for iOS

> **Summary:** Trigger the native iOS share sheet from your web app to let users share your app or any URL.

[Documentation](../README.md) › [WebViewGold for iOS](README.md) › App Sharing Dialog API

**Platform:** iOS · **Category:** APIs & Features · **Online version:** [www.webviewgold.com/docs/iOS/app-sharing-dialog/](https://www.webviewgold.com/docs/iOS/app-sharing-dialog/)

---

The App Sharing Dialog API in WebViewGold enables your users to share content from your app, such as the download link or custom messages, with friends and family via their preferred apps (e.g., WhatsApp, SMS, Email). This can be an effective way to increase your app’s visibility and grow your user base.

## How to Use the App Sharing Dialog in Your WebView-Based iOS App

You can trigger a native sharing dialog by using the `shareapp://` URL scheme with customizable message and URL parameters.

Below are examples of the different ways to implement this feature:

```html
<a href="shareapp://message?=Check out this cool thing!&url=https://www.webviewgold.com">Share (message, link)</a>

<a href="shareapp://message?=&url=https://www.webviewgold.com">Share (no message, link)</a>

<a href="shareapp://message?=Check out this cool thing!">Share (message, no link)</a>
```

![App Sharing Dialog Example](../assets/ios/img/sharedialog.webp)\
![App Sharing Message Example](../assets/ios/img/sharemessage.webp)

---

## Continue reading

- ← Previous: [Deep Linking API](deep-linking.md)
- Next →: [In-App Rating Dialog API](in-app-rating.md)
- Same feature on other platforms: [Android – App Sharing Dialog API](../android/app-sharing-dialog.md)
- Languages: **🇺🇸 English** · [🇩🇪 Deutsch](../de/ios/app-sharing-dialog.md) · [🇫🇷 Français](../fr/ios/app-sharing-dialog.md) · [🇪🇸 Español](../es/ios/app-sharing-dialog.md) · [🇨🇳 中文](../zh/ios/app-sharing-dialog.md)

> [!TIP]
> **Too busy? We set up your app for you.** Our team configures, builds & submits your WebViewGold app — done-for-you, fast turnaround, Made in Germany. [Get your app set up →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **Build in your browser:** No Mac, no IDE: the **WebViewGold Cloud Builder** configures, builds & uploads your app online. [Discover Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
