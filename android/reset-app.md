---
title: "Reset App API – WebViewGold for Android Documentation"
description: "Reset cache, cookies, and local storage of your Android WebView app with a single link or JavaScript call."
lang: "en"
product: "WebViewGold for Android"
platform: "Android"
category: "APIs & Features"
slug: "reset-app"
canonical_url: "https://www.webviewgold.com/docs/android/reset-app/"
keywords:
  - "Reset App API"
  - "WebViewGold for Android"
  - "convert website to app"
  - "WebView app documentation"
  - "Android WebView SDK"
  - "PWA to app"
  - "HTML to app"
  - "JavaScript bridge"
last_updated: "2026-10-09"
---

# Reset App API – WebViewGold for Android

> **Summary:** Reset cache, cookies, and local storage of your Android WebView app with a single link or JavaScript call.

[Documentation](../README.md) › [WebViewGold for Android](README.md) › Reset App API

**Platform:** Android · **Category:** APIs & Features · **Online version:** [www.webviewgold.com/docs/android/reset-app/](https://www.webviewgold.com/docs/android/reset-app/)

---

In certain cases, resetting the app to its initial settings (by clearing cookies and cache) can be necessary to restore optimal performance. The **Reset App API** provides a straightforward way to initiate this reset.

## Usage

To reset the app data, simply use the following link within your app:

```html
<a href="reset://">Reset App Link</a>
```

This link will:

- Clear all cookies
- Clear cached data

## Testing the Reset Functionality

To test this feature, add the following demo URL to your WebViewGold app: <https://www.onlineappcreator.com/reset_test.html>

**Note:** Use the reset functionality sensibly, as it will clear user data related to cookies and cache, which could impact saved settings or session data, including logging users out of active sessions.

---

## Continue reading

- ← Previous: [Native Video (PiP) API](native-video.md)
- Next →: [Loading Sign API](loading-sign.md)
- Same feature on other platforms: [iOS – Reset App API](../ios/reset-app.md)
- Languages: **🇺🇸 English** · [🇩🇪 Deutsch](../de/android/reset-app.md) · [🇫🇷 Français](../fr/android/reset-app.md) · [🇪🇸 Español](../es/android/reset-app.md) · [🇨🇳 中文](../zh/android/reset-app.md)

> [!TIP]
> **Too busy? We set up your app for you.** Our team configures, builds & submits your WebViewGold app — done-for-you, fast turnaround, Made in Germany. [Get your app set up →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_android_doc_online)
>
> **Build in your browser:** No Mac, no IDE: the **WebViewGold Cloud Builder** configures, builds & uploads your app online. [Discover Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=android_docs)
