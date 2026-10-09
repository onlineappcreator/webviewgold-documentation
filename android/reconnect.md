---
title: "Reconnect API – WebViewGold for Android Documentation"
description: "Reload the last online URL from your offline / fallback HTML page — the perfect \"Try again\" button for your custom offline screen."
lang: "en"
product: "WebViewGold for Android"
platform: "Android"
category: "APIs & Features"
slug: "reconnect"
canonical_url: "https://www.webviewgold.com/docs/android/reconnect/"
keywords:
  - "Reconnect API"
  - "WebViewGold for Android"
  - "convert website to app"
  - "WebView app documentation"
  - "Android WebView SDK"
  - "PWA to app"
  - "HTML to app"
  - "JavaScript bridge"
last_updated: "2026-10-09"
---

# Reconnect API – WebViewGold for Android

> **Summary:** Reload the last online URL from your offline / fallback HTML page — the perfect "Try again" button for your custom offline screen.

[Documentation](../README.md) › [WebViewGold for Android](README.md) › Reconnect API

**Platform:** Android · **Category:** APIs & Features · **Online version:** [www.webviewgold.com/docs/android/reconnect/](https://www.webviewgold.com/docs/android/reconnect/)

---

The **Reconnect API** reloads the last online URL the user was on before your app fell back to the offline HTML page. It is designed as a "Try again" button on your custom offline / fallback screen.

## How to Use

Add the trigger to your offline page (typically `local-html/index.html`):

```html
<button onclick="window.location.href='reconnect://'">Try to reconnect</button>
```

## How It Works

The app remembers the last non-helper URL that was loaded successfully. When the user taps `reconnect://`, the WebView navigates back to that URL. If connectivity is still down, your fallback page is shown again.

## Related Config

- `FALLBACK_USE_LOCAL_HTML_FOLDER_IF_OFFLINE` in **Config.java** must be `true`, and you need a `local-html/index.html` fallback page for this feature to make sense.

---

## Continue reading

- ← Previous: [Open App Settings API](open-app-settings.md)
- Next →: [Read/Write Value API](read-write-value.md)
- Same feature on other platforms: [iOS – Reconnect API](../ios/reconnect.md)
- Languages: **🇺🇸 English** · [🇩🇪 Deutsch](../de/android/reconnect.md) · [🇫🇷 Français](../fr/android/reconnect.md) · [🇪🇸 Español](../es/android/reconnect.md) · [🇨🇳 中文](../zh/android/reconnect.md)

> [!TIP]
> **Too busy? We set up your app for you.** Our team configures, builds & submits your WebViewGold app — done-for-you, fast turnaround, Made in Germany. [Get your app set up →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_android_doc_online)
>
> **Build in your browser:** No Mac, no IDE: the **WebViewGold Cloud Builder** configures, builds & uploads your app online. [Discover Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=android_docs)
