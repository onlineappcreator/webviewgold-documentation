---
title: "Scanning Mode API – WebViewGold for iOS Documentation"
description: "Fine-tune the camera scanning behavior of the QR and barcode scanner in WebViewGold for iOS."
lang: "en"
product: "WebViewGold for iOS"
platform: "iOS"
category: "APIs & Features"
slug: "scanning-mode"
canonical_url: "https://www.webviewgold.com/docs/iOS/scanning-mode/"
keywords:
  - "Scanning Mode API"
  - "WebViewGold for iOS"
  - "convert website to app"
  - "WebView app documentation"
  - "iOS WebView SDK"
  - "PWA to app"
  - "HTML to app"
  - "JavaScript bridge"
last_updated: "2026-10-09"
---

# Scanning Mode API – WebViewGold for iOS

> **Summary:** Fine-tune the camera scanning behavior of the QR and barcode scanner in WebViewGold for iOS.

[Documentation](../README.md) › [WebViewGold for iOS](README.md) › Scanning Mode API

**Platform:** iOS · **Category:** APIs & Features · **Online version:** [www.webviewgold.com/docs/iOS/scanning-mode/](https://www.webviewgold.com/docs/iOS/scanning-mode/)

---

If your web app presents information on the screen to be scanned (for example, a QR code), it can be helpful to turn the screen brightness up to 100% and to prevent the screen from sleeping. WebViewGold provides the Scanning Mode API to dynamically enable these optimal scanning conditions.\
This API includes 3 commands:

- "auto" = turns on scanning mode and automatically turns it off on page redirect.
- "on" = turns on scanning mode, stays on after page redirects.
- "off" = turns off scanning mode.

Link to these kinds of URLs to use the Scanning Mode API:

```html
<a href="scanningmode://auto">Enable Scanning Mode; will automatically disable on page redirect</a>
<a href="scanningmode://on">Enable Scanning Mode; will persist until manually disabled</a>
<a href="scanningmode://off">Disable Scanning Mode</a>
```

---

## Continue reading

- ← Previous: [Barcode Scanner API](barcode-scanner.md)
- Next →: [Document Scanner](document-scanner.md)
- Same feature on other platforms: [Android – Scanning Mode API](../android/scanning-mode.md)
- Languages: **🇺🇸 English** · [🇩🇪 Deutsch](../de/ios/scanning-mode.md) · [🇫🇷 Français](../fr/ios/scanning-mode.md) · [🇪🇸 Español](../es/ios/scanning-mode.md) · [🇨🇳 中文](../zh/ios/scanning-mode.md)

> [!TIP]
> **Too busy? We set up your app for you.** Our team configures, builds & submits your WebViewGold app — done-for-you, fast turnaround, Made in Germany. [Get your app set up →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **Build in your browser:** No Mac, no IDE: the **WebViewGold Cloud Builder** configures, builds & uploads your app online. [Discover Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
