---
title: "UUID API – WebViewGold for iOS Documentation"
description: "Identify app installations with a unique UUID appended to your WebView URL or retrieved via JavaScript."
lang: "en"
product: "WebViewGold for iOS"
platform: "iOS"
category: "APIs & Features"
slug: "uuid"
canonical_url: "https://www.webviewgold.com/docs/iOS/uuid/"
keywords:
  - "UUID API"
  - "WebViewGold for iOS"
  - "convert website to app"
  - "WebView app documentation"
  - "iOS WebView SDK"
  - "PWA to app"
  - "HTML to app"
  - "JavaScript bridge"
last_updated: "2026-10-09"
---

# UUID API – WebViewGold for iOS

> **Summary:** Identify app installations with a unique UUID appended to your WebView URL or retrieved via JavaScript.

[Documentation](../README.md) › [WebViewGold for iOS](README.md) › UUID API

**Platform:** iOS · **Category:** APIs & Features · **Online version:** [www.webviewgold.com/docs/iOS/uuid/](https://www.webviewgold.com/docs/iOS/uuid/)

---

The WebViewGold UUID API allows you to retrieve a non-personal, unique device ID (UUID - "Universally Unique Identifier"), which can **uniquely identify an iOS device**. This feature can be helpful for:

- Storing user-specific settings on the server
- Maintaining session states
- Recalling saved data on the client side

**Privacy Note:** Ensure compliance with local and international **privacy laws** when using this feature, as it involves device identification.

## How to Retrieve UUID

To retrieve the UUID from your WebView-based app, use the following code:

```html
<a href="get-uuid://">Get UUID</a>
<a href="#" onClick="alert(uuid);">Show UUID</a>
```

- **Get UUID:** Requests the UUID from WebViewGold.
- **Show UUID:** Displays the UUID via an **alert** for easy testing.

## Alternative Method: Append the UUID to the WebView URL

If you prefer to include the UUID in the URL parameters, enable the `enhanceUrlUUID` option in **Config.swift** by setting it to `true`. This will automatically append `uuid=XYZ` to your WebView URL on the first request, allowing you to access the UUID directly in your web content:

- **Example:** If your WebView URL is `https://www.example.org`, it will be requested as `https://www.example.org?uuid=XYZ`.
- **Note:** Only the initial URL request will include this GET parameter, so consider saving it in a session or cookie if you need to reference it later in the app.

## Automatically Inject UUID into JavaScript

To automatically make UUID (and other variables) available in JavaScript across all pages without modifying URLs, set `autoInjectVariable` to `true` in **Config.swift**. This allows you to access the UUID and other values directly within any page.

---

## Continue reading

- ← Previous: [Apple Wallet Pass API](wallet-pass.md)
- Next →: [Flashlight API](flashlight.md)
- Same feature on other platforms: [Android – UUID API](../android/uuid.md) · [macOS – UUID API](../macos/uuid.md)
- Languages: **🇺🇸 English** · [🇩🇪 Deutsch](../de/ios/uuid.md) · [🇫🇷 Français](../fr/ios/uuid.md) · [🇪🇸 Español](../es/ios/uuid.md) · [🇨🇳 中文](../zh/ios/uuid.md)

> [!TIP]
> **Too busy? We set up your app for you.** Our team configures, builds & submits your WebViewGold app — done-for-you, fast turnaround, Made in Germany. [Get your app set up →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **Build in your browser:** No Mac, no IDE: the **WebViewGold Cloud Builder** configures, builds & uploads your app online. [Discover Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
