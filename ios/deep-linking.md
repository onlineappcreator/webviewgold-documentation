---
title: "Deep Linking API – WebViewGold for iOS Documentation"
description: "Launch your iOS app via custom URL schemes and deep link users to specific pages of your web app."
lang: "en"
product: "WebViewGold for iOS"
platform: "iOS"
category: "APIs & Features"
slug: "deep-linking"
canonical_url: "https://www.webviewgold.com/docs/iOS/deep-linking/"
keywords:
  - "Deep Linking API"
  - "WebViewGold for iOS"
  - "convert website to app"
  - "WebView app documentation"
  - "iOS WebView SDK"
  - "PWA to app"
  - "HTML to app"
  - "JavaScript bridge"
last_updated: "2026-10-09"
---

# Deep Linking API – WebViewGold for iOS

> **Summary:** Launch your iOS app via custom URL schemes and deep link users to specific pages of your web app.

[Documentation](../README.md) › [WebViewGold for iOS](README.md) › Deep Linking API

**Platform:** iOS · **Category:** APIs & Features · **Online version:** [www.webviewgold.com/docs/iOS/deep-linking/](https://www.webviewgold.com/docs/iOS/deep-linking/)

---

The **Deep Linking API** makes it easy to direct users to specific content inside your app. WebViewGold allows you to configure a Custom URL Scheme (e.g., `webviewgold://`) that can be triggered from apps like **Mail, Safari, and others** to open links directly in your WebView app.

**Note:** the app needs to be installed first for this feature to work.

**Alternatively**, it is possible to use our [**Universal Links API**](universal-links.md). While it operates in a similar manner, it uses a different syntax which is more common than the syntax of the Deep Linking API. For most apps, it's wise to choose either one, but not both.

To set up **Deep Linking** in your iOS app, please follow the steps below:

1. **Open Config.swift:**
   - Set `ShowExternalLink` to `true`.

![Deep Linking Setup](../assets/ios/img/universallinks.webp)
2. **Open Info.plist:**
   - Change the URL Scheme to your own app name (e.g., `your-app-name://` instead of `webviewgold://`).

![Info.plist is a powerful location to configure deep linking which can be triggered from different apps as well](../assets/ios/img/infoplist.webp)

**Done! :)** The example below would open google.com in the WebView app:

```
WebViewGold://url?link=https://www.google.com
```

[![Watch the video: Deep Linking API](https://img.youtube.com/vi/mW4H_gUKU28/hqdefault.jpg)](https://www.youtube.com/watch?v=mW4H_gUKU28)

---

## Continue reading

- ← Previous: [Universal Links API](universal-links.md)
- Next →: [App Sharing Dialog API](app-sharing-dialog.md)
- Same feature on other platforms: [macOS – Deeplinking API](../macos/deep-linking.md)
- Languages: **🇺🇸 English** · [🇩🇪 Deutsch](../de/ios/deep-linking.md) · [🇫🇷 Français](../fr/ios/deep-linking.md) · [🇪🇸 Español](../es/ios/deep-linking.md) · [🇨🇳 中文](../zh/ios/deep-linking.md)

> [!TIP]
> **Too busy? We set up your app for you.** Our team configures, builds & submits your WebViewGold app — done-for-you, fast turnaround, Made in Germany. [Get your app set up →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **Build in your browser:** No Mac, no IDE: the **WebViewGold Cloud Builder** configures, builds & uploads your app online. [Discover Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
