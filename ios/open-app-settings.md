---
title: "Open App Settings API – WebViewGold for iOS Documentation"
description: "Send users straight to your app's page in the iOS Settings app to manage permissions and notifications."
lang: "en"
product: "WebViewGold for iOS"
platform: "iOS"
category: "APIs & Features"
slug: "open-app-settings"
canonical_url: "https://www.webviewgold.com/docs/iOS/open-app-settings/"
keywords:
  - "Open App Settings API"
  - "WebViewGold for iOS"
  - "convert website to app"
  - "WebView app documentation"
  - "iOS WebView SDK"
  - "PWA to app"
  - "HTML to app"
  - "JavaScript bridge"
last_updated: "2026-10-09"
---

# Open App Settings API – WebViewGold for iOS

> **Summary:** Send users straight to your app's page in the iOS Settings app to manage permissions and notifications.

[Documentation](../README.md) › [WebViewGold for iOS](README.md) › Open App Settings API

**Platform:** iOS · **Category:** APIs & Features · **Online version:** [www.webviewgold.com/docs/iOS/open-app-settings/](https://www.webviewgold.com/docs/iOS/open-app-settings/)

---

The **Open App Settings API** of WebViewGold sends the user straight to your app's page in the native iOS **Settings** app. From there they can manage permissions (camera, location, notifications…), language, and other app settings — without leaving your web app to hunt through iOS Settings.

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
- Guide the user to the notification settings of your app, e.g. in combination with the `checkNativePushPermissions://` call of the [Push Notifications API](push-notifications.md).

**Notes:** No parameters. Any URL that starts with `settingsapp://` opens the same screen.

---

## Continue reading

- ← Previous: [Read/Write Value API](read-write-value.md)
- Next →: [Share Extension](share-extension.md)
- Same feature on other platforms: [Android – Open App Settings API](../android/open-app-settings.md)
- Languages: **🇺🇸 English** · [🇩🇪 Deutsch](../de/ios/open-app-settings.md) · [🇫🇷 Français](../fr/ios/open-app-settings.md) · [🇪🇸 Español](../es/ios/open-app-settings.md) · [🇨🇳 中文](../zh/ios/open-app-settings.md)

> [!TIP]
> **Too busy? We set up your app for you.** Our team configures, builds & submits your WebViewGold app — done-for-you, fast turnaround, Made in Germany. [Get your app set up →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **Build in your browser:** No Mac, no IDE: the **WebViewGold Cloud Builder** configures, builds & uploads your app online. [Discover Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
