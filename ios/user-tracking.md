---
title: "User Tracking Decision API – WebViewGold for iOS Documentation"
description: "Respect App Tracking Transparency: read and react to the user's tracking decision inside your WebViewGold iOS app."
lang: "en"
product: "WebViewGold for iOS"
platform: "iOS"
category: "APIs & Features"
slug: "user-tracking"
canonical_url: "https://www.webviewgold.com/docs/iOS/user-tracking/"
keywords:
  - "User Tracking Decision API"
  - "WebViewGold for iOS"
  - "convert website to app"
  - "WebView app documentation"
  - "iOS WebView SDK"
  - "PWA to app"
  - "HTML to app"
  - "JavaScript bridge"
last_updated: "2026-10-09"
---

# User Tracking Decision API – WebViewGold for iOS

> **Summary:** Respect App Tracking Transparency: read and react to the user's tracking decision inside your WebViewGold iOS app.

[Documentation](../README.md) › [WebViewGold for iOS](README.md) › User Tracking Decision API

**Platform:** iOS · **Category:** APIs & Features · **Online version:** [www.webviewgold.com/docs/iOS/user-tracking/](https://www.webviewgold.com/docs/iOS/user-tracking/)

---

In iOS, apps have to ask to track user data based on the Apple AppTrackingTransparency framework. WebViewGold allows you to see what choice the user made when they installed your app to act accordingly in your web app. The JavaScript variable **trackingDisabled** can be either set by WebViewGold to true to represent that tracking has been blocked or false if it hasn't been. On your web app, you can easily check the JavaScript status by first getting the JavaScript variable and then alerting it:

```html
<a href="user-disable-tracking://">Set JavaScript variable</a>
<a href="#" onClick="alert(trackingDisabled);">Show tracking decision</a>
```

---

## Continue reading

- ← Previous: [Reset App API](reset-app.md)
- Next →: [Loading Sign API](loading-sign.md)
- Languages: **🇺🇸 English** · [🇩🇪 Deutsch](../de/ios/user-tracking.md) · [🇫🇷 Français](../fr/ios/user-tracking.md) · [🇪🇸 Español](../es/ios/user-tracking.md) · [🇨🇳 中文](../zh/ios/user-tracking.md)

> [!TIP]
> **Too busy? We set up your app for you.** Our team configures, builds & submits your WebViewGold app — done-for-you, fast turnaround, Made in Germany. [Get your app set up →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **Build in your browser:** No Mac, no IDE: the **WebViewGold Cloud Builder** configures, builds & uploads your app online. [Discover Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
