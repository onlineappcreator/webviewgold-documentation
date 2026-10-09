---
title: "HTML5 Geolocation API – WebViewGold for iOS Documentation"
description: "Enable HTML5 geolocation in your iOS WebView app and request precise location permissions the right way."
lang: "en"
product: "WebViewGold for iOS"
platform: "iOS"
category: "APIs & Features"
slug: "geolocation"
canonical_url: "https://www.webviewgold.com/docs/iOS/geolocation/"
keywords:
  - "Geolocation API"
  - "WebViewGold for iOS"
  - "convert website to app"
  - "WebView app documentation"
  - "iOS WebView SDK"
  - "PWA to app"
  - "HTML to app"
  - "JavaScript bridge"
last_updated: "2026-10-09"
---

# HTML5 Geolocation API – WebViewGold for iOS

> **Summary:** Enable HTML5 geolocation in your iOS WebView app and request precise location permissions the right way.

[Documentation](../README.md) › [WebViewGold for iOS](README.md) › Geolocation API

**Platform:** iOS · **Category:** APIs & Features · **Online version:** [www.webviewgold.com/docs/iOS/geolocation/](https://www.webviewgold.com/docs/iOS/geolocation/)

---

The HTML5 Geolocation API enables users to share their location with your app, enhancing features like location-based content. In WebViewGold, the Geolocation API is supported by default once integrated into your web content. Here is how to implement Geolocation tracking into your WebView-based iOS app:

## Setting up HTML5 Geolocation

For basic Geolocation setup, refer to [Mozilla's Geolocation Guide](https://developer.mozilla.org/en-US/docs/Web/API/Geolocation_API) for details on how to implement this feature into your website or web app.

For a demonstration, visit this [W3Schools Geolocation Demo](https://www.w3schools.com/html/html5_geolocation.asp).

Since iOS 10, Geolocation is available for https-sites only, so please make sure to use a web app URL starting with `https://` instead of `http://` when using location requests.

## Background Location Access

By default, location requests only work while the app is in the foreground. If your web app needs to keep receiving location updates while the app is in the background (e.g., for tracking or geofencing use cases), enable the background location option in **Config.swift**:

```swift
static let backgroundlocation = true
```

- In the Xcode project settings, add the **Background Modes** capability to the WebViewGold target and check **Location updates**.
- Depending on your web app, you may additionally need to activate **Background Processing**. In that case, also add an array with the key `Permitted background task scheduler identifiers` to your **Info.plist** and include a string with your app bundle ID (e.g., `com.yourcompany.yourapp`).
- Keep in mind that background location access requires a clear justification during App Store review — describe the user-facing benefit in your review notes.

---

## Continue reading

- ← Previous: [Modify Safe Area](safe-area.md)
- Next →: [Push Notifications API](push-notifications.md)
- Same feature on other platforms: [Android – Geolocation API](../android/geolocation.md)
- Languages: **🇺🇸 English** · [🇩🇪 Deutsch](../de/ios/geolocation.md) · [🇫🇷 Français](../fr/ios/geolocation.md) · [🇪🇸 Español](../es/ios/geolocation.md) · [🇨🇳 中文](../zh/ios/geolocation.md)

> [!TIP]
> **Too busy? We set up your app for you.** Our team configures, builds & submits your WebViewGold app — done-for-you, fast turnaround, Made in Germany. [Get your app set up →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **Build in your browser:** No Mac, no IDE: the **WebViewGold Cloud Builder** configures, builds & uploads your app online. [Discover Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
