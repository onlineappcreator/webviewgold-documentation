---
title: "Open App Settings API – WebViewGold for Android Documentation"
description: "Send the user straight to the system App-info screen from your web app to manage permissions, notifications, storage, or force-stop your Android app."
lang: "en"
product: "WebViewGold for Android"
platform: "Android"
category: "APIs & Features"
slug: "open-app-settings"
canonical_url: "https://www.webviewgold.com/docs/android/open-app-settings/"
keywords:
  - "Open App Settings API"
  - "WebViewGold for Android"
  - "convert website to app"
  - "WebView app documentation"
  - "Android WebView SDK"
  - "PWA to app"
  - "HTML to app"
  - "JavaScript bridge"
last_updated: "2026-10-09"
---

# Open App Settings API – WebViewGold for Android

> **Summary:** Send the user straight to the system App-info screen from your web app to manage permissions, notifications, storage, or force-stop your Android app.

[Documentation](../README.md) › [WebViewGold for Android](README.md) › Open App Settings API

**Platform:** Android · **Category:** APIs & Features · **Online version:** [www.webviewgold.com/docs/android/open-app-settings/](https://www.webviewgold.com/docs/android/open-app-settings/)

---

The **Open App Settings API** of WebViewGold sends the user straight to the system **App info** screen for your app. From there they can manage permissions, notifications, storage, or force-stop the app — without leaving your web app to hunt through Android Settings.

## How to Use

Trigger the screen from an HTML link or from JavaScript:

```html
<a href="settingsapp://">Open app settings</a>
```

```javascript
window.location.href = "settingsapp://";
```

## Typical Use Cases

- The user denied a permission (camera, microphone, location, notifications) — send them straight to the system screen to re-enable it.
- Guide the user to disable battery optimization or clear cache from the OS side.

**Notes:** No parameters. Any URL that starts with `settingsapp://` triggers the same screen. Works on all supported Android versions.

---

## Continue reading

- ← Previous: [NFC Plugin](nfc.md)
- Next →: [Reconnect API](reconnect.md)
- Same feature on other platforms: [iOS – Open App Settings API](../ios/open-app-settings.md)
- Languages: **🇺🇸 English** · [🇩🇪 Deutsch](../de/android/open-app-settings.md) · [🇫🇷 Français](../fr/android/open-app-settings.md) · [🇪🇸 Español](../es/android/open-app-settings.md) · [🇨🇳 中文](../zh/android/open-app-settings.md)

> [!TIP]
> **Too busy? We set up your app for you.** Our team configures, builds & submits your WebViewGold app — done-for-you, fast turnaround, Made in Germany. [Get your app set up →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_android_doc_online)
>
> **Build in your browser:** No Mac, no IDE: the **WebViewGold Cloud Builder** configures, builds & uploads your app online. [Discover Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=android_docs)
