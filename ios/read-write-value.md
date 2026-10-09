---
title: "Read/Write Value API – WebViewGold for iOS Documentation"
description: "Persistently store a string value on the device and read it back into your web app's JavaScript."
lang: "en"
product: "WebViewGold for iOS"
platform: "iOS"
category: "APIs & Features"
slug: "read-write-value"
canonical_url: "https://www.webviewgold.com/docs/iOS/read-write-value/"
keywords:
  - "Read/Write Value API"
  - "WebViewGold for iOS"
  - "convert website to app"
  - "WebView app documentation"
  - "iOS WebView SDK"
  - "PWA to app"
  - "HTML to app"
  - "JavaScript bridge"
last_updated: "2026-10-09"
---

# Read/Write Value API – WebViewGold for iOS

> **Summary:** Persistently store a string value on the device and read it back into your web app's JavaScript.

[Documentation](../README.md) › [WebViewGold for iOS](README.md) › Read/Write Value API

**Platform:** iOS · **Category:** APIs & Features · **Online version:** [www.webviewgold.com/docs/iOS/read-write-value/](https://www.webviewgold.com/docs/iOS/read-write-value/)

---

The **Read/Write Value API** persistently stores an arbitrary string on the device (via the app's private storage) and reads it back into your JavaScript. Values survive app restarts and cache clears — unless the app is uninstalled.

## Writing a Value

Everything after `writevalue://` is stored verbatim as one string. Design your own format (query-string, JSON, CSV — whatever fits your web app):

```html
<a href="writevalue://darkmode=on;user=42">Save</a>
```

## Reading a Value

When `readvalue://` is triggered, the app injects the stored string back into the WebView as `window.storedValues` so your JavaScript can read it:

```html
<a href="readvalue://" onclick="setTimeout(showSettings, 200)">Load</a>
<script>
  function showSettings() {
    console.log(window.storedValues || "no settings yet");
  }
</script>
```

## Typical Use Cases

- Remember a user's theme, language, or onboarding state offline.
- Cache a session token when you cannot rely on cookies.
- Persist a small local preference without a backend round-trip.

**Notes:** Values are per-app-install and per-device — they are **not** synced across devices. Keep values small; this API is intended for settings, not blob storage.

---

## Continue reading

- ← Previous: [Clipboard API](clipboard.md)
- Next →: [Open App Settings API](open-app-settings.md)
- Same feature on other platforms: [Android – Read/Write Value API](../android/read-write-value.md)
- Languages: **🇺🇸 English** · [🇩🇪 Deutsch](../de/ios/read-write-value.md) · [🇫🇷 Français](../fr/ios/read-write-value.md) · [🇪🇸 Español](../es/ios/read-write-value.md) · [🇨🇳 中文](../zh/ios/read-write-value.md)

> [!TIP]
> **Too busy? We set up your app for you.** Our team configures, builds & submits your WebViewGold app — done-for-you, fast turnaround, Made in Germany. [Get your app set up →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **Build in your browser:** No Mac, no IDE: the **WebViewGold Cloud Builder** configures, builds & uploads your app online. [Discover Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
