---
title: "App Version Check API – WebViewGold for iOS Documentation"
description: "Detect the installed app version from your web app and prompt users to update when needed."
lang: "en"
product: "WebViewGold for iOS"
platform: "iOS"
category: "APIs & Features"
slug: "app-version-check"
canonical_url: "https://www.webviewgold.com/docs/iOS/app-version-check/"
keywords:
  - "App Version Check API"
  - "WebViewGold for iOS"
  - "convert website to app"
  - "WebView app documentation"
  - "iOS WebView SDK"
  - "PWA to app"
  - "HTML to app"
  - "JavaScript bridge"
last_updated: "2026-10-09"
---

# App Version Check API – WebViewGold for iOS

> **Summary:** Detect the installed app version from your web app and prompt users to update when needed.

[Documentation](../README.md) › [WebViewGold for iOS](README.md) › App Version Check API

**Platform:** iOS · **Category:** APIs & Features · **Online version:** [www.webviewgold.com/docs/iOS/app-version-check/](https://www.webviewgold.com/docs/iOS/app-version-check/)

---

Using this WebViewGold JavaScript API approach, your website/web app can **retrieve the version of the iOS app** being used by your app user. This is especially helpful if you want to notify users of an older version to update their app. Moreover, you can hide web app sections that require app features supported by a specific app version.\
Use JavaScript to this kind of URL to read and alert the app version and app bundle number:

```html
<script>
window.location.href = "getappversion://";
alert(versionNumber);
alert(bundleNumber);
</script>
```

**Alternatively, consider turning `autoInjectVariable` to `true` in Config.swift to automatically inject this (and other) values into JavaScript without needing to call a URL upfront.**

---

## Continue reading

- ← Previous: [Take Screenshot API](take-screenshot.md)
- Next →: [Dynamic UI API](dynamic-ui.md)
- Same feature on other platforms: [Android – App Version Check API](../android/app-version-check.md)
- Languages: **🇺🇸 English** · [🇩🇪 Deutsch](../de/ios/app-version-check.md) · [🇫🇷 Français](../fr/ios/app-version-check.md) · [🇪🇸 Español](../es/ios/app-version-check.md) · [🇨🇳 中文](../zh/ios/app-version-check.md)

> [!TIP]
> **Too busy? We set up your app for you.** Our team configures, builds & submits your WebViewGold app — done-for-you, fast turnaround, Made in Germany. [Get your app set up →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **Build in your browser:** No Mac, no IDE: the **WebViewGold Cloud Builder** configures, builds & uploads your app online. [Discover Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
