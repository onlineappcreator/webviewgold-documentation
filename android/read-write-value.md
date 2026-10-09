---
title: "Read/Write Value API – WebViewGold for Android Documentation"
description: "Persist small strings on the device from JavaScript and read them back — for theme, language, session tokens, or onboarding state."
lang: "en"
product: "WebViewGold for Android"
platform: "Android"
category: "APIs & Features"
slug: "read-write-value"
canonical_url: "https://www.webviewgold.com/docs/android/read-write-value/"
keywords:
  - "Read/Write Value API"
  - "WebViewGold for Android"
  - "convert website to app"
  - "WebView app documentation"
  - "Android WebView SDK"
  - "PWA to app"
  - "HTML to app"
  - "JavaScript bridge"
last_updated: "2026-10-09"
---

# Read/Write Value API – WebViewGold for Android

> **Summary:** Persist small strings on the device from JavaScript and read them back — for theme, language, session tokens, or onboarding state.

[Documentation](../README.md) › [WebViewGold for Android](README.md) › Read/Write Value API

**Platform:** Android · **Category:** APIs & Features · **Online version:** [www.webviewgold.com/docs/android/read-write-value/](https://www.webviewgold.com/docs/android/read-write-value/)

---

The **Read/Write Value API** persistently stores an arbitrary string on the device (via the app's private storage) and reads it back into your JavaScript. Values survive app restarts and cache clears — unless the OS wipes app data.

## Writing a Value

Everything after `writevalue://` is stored verbatim as one string. Design your own format (query-string, JSON, CSV — whatever fits your web app):

```html
<a href="writevalue://darkmode=on;user=42">Save</a>
```

## Reading a Value

When `readvalue://` is triggered, the app injects the stored string back into the WebView so your JavaScript can read it:

```html
<a href="readvalue://" onclick="setTimeout(showSettings, 200)">Load</a>
<script>
  function showSettings() {
    console.log(window.appSettings || "no settings yet");
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

- ← Previous: [Reconnect API](reconnect.md)
- Next →: [Biometric Auth API](biometric-auth.md)
- Same feature on other platforms: [iOS – Read/Write Value API](../ios/read-write-value.md)
- Languages: **🇺🇸 English** · [🇩🇪 Deutsch](../de/android/read-write-value.md) · [🇫🇷 Français](../fr/android/read-write-value.md) · [🇪🇸 Español](../es/android/read-write-value.md) · [🇨🇳 中文](../zh/android/read-write-value.md)

> [!TIP]
> **Too busy? We set up your app for you.** Our team configures, builds & submits your WebViewGold app — done-for-you, fast turnaround, Made in Germany. [Get your app set up →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_android_doc_online)
>
> **Build in your browser:** No Mac, no IDE: the **WebViewGold Cloud Builder** configures, builds & uploads your app online. [Discover Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=android_docs)
