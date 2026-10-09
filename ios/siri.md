---
title: "Siri Plugin – WebViewGold for iOS Documentation"
description: "Add Siri Shortcuts support to your iOS WebView app and open app content by voice."
lang: "en"
product: "WebViewGold for iOS"
platform: "iOS"
category: "Extensions & Plugins"
slug: "siri"
canonical_url: "https://www.webviewgold.com/docs/iOS/siri/"
keywords:
  - "Siri Plugin"
  - "WebViewGold for iOS"
  - "convert website to app"
  - "WebView app documentation"
  - "iOS WebView SDK"
  - "PWA to app"
  - "HTML to app"
  - "JavaScript bridge"
last_updated: "2026-10-09"
---

# Siri Plugin – WebViewGold for iOS

> **Summary:** Add Siri Shortcuts support to your iOS WebView app and open app content by voice.

[Documentation](../README.md) › [WebViewGold for iOS](README.md) › Siri Plugin

**Platform:** iOS · **Category:** Extensions & Plugins · **Online version:** [www.webviewgold.com/docs/iOS/siri/](https://www.webviewgold.com/docs/iOS/siri/)

---

Enable Siri integration by entering your plugin token in `static let siriEnabled` within `Config.swift` and adding the Siri capability to the WebViewGold target.\
Reach out to [webviewgold-siri@onlineappcreator.com](mailto:webviewgold-siri@onlineappcreator.com) for more information.

## How to implement Siri functionality

1. Create a JavaScript function that Siri should trigger:

```javascript
function playRadio() {
   // Add desired functionality
}
```

2. Add a button or link to register the Siri command (avoid phrases like "Open" which may confuse Siri):

```html
<a href="addtosiri://?command=Play%20Radio&jsFunction=playRadio()">Add Play Radio to Siri</a>
```

The `command` parameter provides the recommended phrase, while `jsFunction` specifies the JavaScript function to execute.

---

## Continue reading

- ← Previous: [NFC Plugin](nfc.md)
- Next →: [HealthKit Plugin](healthkit.md)
- Languages: **🇺🇸 English** · [🇩🇪 Deutsch](../de/ios/siri.md) · [🇫🇷 Français](../fr/ios/siri.md) · [🇪🇸 Español](../es/ios/siri.md) · [🇨🇳 中文](../zh/ios/siri.md)

> [!TIP]
> **Too busy? We set up your app for you.** Our team configures, builds & submits your WebViewGold app — done-for-you, fast turnaround, Made in Germany. [Get your app set up →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **Build in your browser:** No Mac, no IDE: the **WebViewGold Cloud Builder** configures, builds & uploads your app online. [Discover Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
