---
title: "Share Extension – WebViewGold for iOS Documentation"
description: "Let users share content from other apps directly into your iOS WebView app with a Share Extension."
lang: "en"
product: "WebViewGold for iOS"
platform: "iOS"
category: "Extensions & Plugins"
slug: "share-extension"
canonical_url: "https://www.webviewgold.com/docs/iOS/share-extension/"
keywords:
  - "Share Extension"
  - "WebViewGold for iOS"
  - "convert website to app"
  - "WebView app documentation"
  - "iOS WebView SDK"
  - "PWA to app"
  - "HTML to app"
  - "JavaScript bridge"
last_updated: "2026-10-09"
---

# Share Extension – WebViewGold for iOS

> **Summary:** Let users share content from other apps directly into your iOS WebView app with a Share Extension.

[Documentation](../README.md) › [WebViewGold for iOS](README.md) › Share Extension

**Platform:** iOS · **Category:** Extensions & Plugins · **Online version:** [www.webviewgold.com/docs/iOS/share-extension/](https://www.webviewgold.com/docs/iOS/share-extension/)

---

When users share text or images to your app from apps such as Photos or Safari, the data becomes available in the JavaScript variable `sharedData`. Shared images are provided as Base64 strings.

```html
<script>
if (typeof sharedData !== 'undefined') {
    console.log(sharedData);
}
</script>
```

---

## Continue reading

- ← Previous: [Open App Settings API](open-app-settings.md)
- Next →: [Widget Extension](widget-extension.md)
- Same feature on other platforms: [Android – ShareIntent API](../android/share-intent.md)
- Languages: **🇺🇸 English** · [🇩🇪 Deutsch](../de/ios/share-extension.md) · [🇫🇷 Français](../fr/ios/share-extension.md) · [🇪🇸 Español](../es/ios/share-extension.md) · [🇨🇳 中文](../zh/ios/share-extension.md)

> [!TIP]
> **Too busy? We set up your app for you.** Our team configures, builds & submits your WebViewGold app — done-for-you, fast turnaround, Made in Germany. [Get your app set up →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **Build in your browser:** No Mac, no IDE: the **WebViewGold Cloud Builder** configures, builds & uploads your app online. [Discover Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
