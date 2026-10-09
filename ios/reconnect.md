---
title: "Reconnect API – WebViewGold for iOS Documentation"
description: "Add a \"Try again\" button to your offline fallback page that reloads the last online URL of your iOS app."
lang: "en"
product: "WebViewGold for iOS"
platform: "iOS"
category: "APIs & Features"
slug: "reconnect"
canonical_url: "https://www.webviewgold.com/docs/iOS/reconnect/"
keywords:
  - "Reconnect API"
  - "WebViewGold for iOS"
  - "convert website to app"
  - "WebView app documentation"
  - "iOS WebView SDK"
  - "PWA to app"
  - "HTML to app"
  - "JavaScript bridge"
last_updated: "2026-10-09"
---

# Reconnect API – WebViewGold for iOS

> **Summary:** Add a "Try again" button to your offline fallback page that reloads the last online URL of your iOS app.

[Documentation](../README.md) › [WebViewGold for iOS](README.md) › Reconnect API

**Platform:** iOS · **Category:** APIs & Features · **Online version:** [www.webviewgold.com/docs/iOS/reconnect/](https://www.webviewgold.com/docs/iOS/reconnect/)

---

The **Reconnect API** reloads the last online URL the user was on before your app fell back to the offline HTML page. It is designed as a "Try again" button on your custom offline / fallback screen.

## How to Use

Add the trigger to your offline page (typically `local-html/index.html`):

```html
<button onclick="window.location.href='reconnect://'">Try to reconnect</button>
```

## How It Works

The app remembers the last URL that was loaded successfully. When the user taps `reconnect://`, the WebView navigates back to that URL. If connectivity is still down, your fallback page is shown again.

## Related Config

- `offlinelocalhtmlswitch` in **Config.swift** must be set to `true`, and you need a `local-html/index.html` fallback page for this feature to make sense. See [Set up your web app](setup-website.md) for details on the offline fallback mode.

---

## Continue reading

- ← Previous: [Social Login Helper](social-login.md)
- Next →: [Custom CSS & JS API](custom-css-js.md)
- Same feature on other platforms: [Android – Reconnect API](../android/reconnect.md)
- Languages: **🇺🇸 English** · [🇩🇪 Deutsch](../de/ios/reconnect.md) · [🇫🇷 Français](../fr/ios/reconnect.md) · [🇪🇸 Español](../es/ios/reconnect.md) · [🇨🇳 中文](../zh/ios/reconnect.md)

> [!TIP]
> **Too busy? We set up your app for you.** Our team configures, builds & submits your WebViewGold app — done-for-you, fast turnaround, Made in Germany. [Get your app set up →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **Build in your browser:** No Mac, no IDE: the **WebViewGold Cloud Builder** configures, builds & uploads your app online. [Discover Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
