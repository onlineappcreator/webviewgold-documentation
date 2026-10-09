---
title: "App Version Check API – WebViewGold for Android Documentation"
description: "Detect the installed app version from your web app and prompt users to update when needed."
lang: "en"
product: "WebViewGold for Android"
platform: "Android"
category: "APIs & Features"
slug: "app-version-check"
canonical_url: "https://www.webviewgold.com/docs/android/app-version-check/"
keywords:
  - "App Version Check API"
  - "WebViewGold for Android"
  - "convert website to app"
  - "WebView app documentation"
  - "Android WebView SDK"
  - "PWA to app"
  - "HTML to app"
  - "JavaScript bridge"
last_updated: "2026-10-09"
---

# App Version Check API – WebViewGold for Android

> **Summary:** Detect the installed app version from your web app and prompt users to update when needed.

[Documentation](../README.md) › [WebViewGold for Android](README.md) › App Version Check API

**Platform:** Android · **Category:** APIs & Features · **Online version:** [www.webviewgold.com/docs/android/app-version-check/](https://www.webviewgold.com/docs/android/app-version-check/)

---

Using this WebViewGold App Version Check API, your website/web app can **retrieve the version of the Android app** being used by your Android app user. This API is especially helpful if you want to notify users of an older version to update their app. Moreover, you can hide web app sections that require app features supported by a specific app version.\
Use JavaScript to this kind of URL to read and alert the app version and app bundle number:

```html
<script>
window.location.href = "getappversion://";
alert(versionNumber);
alert(bundleNumber);
</script>
```

**Alternatively, consider turning  `AUTO_INJECT_VARIABLES`  to `true` in Config.java to automatically inject this (and other) values into JavaScript without needing to call a URL upfront.**

---

## Continue reading

- ← Previous: [Take Screenshot API](take-screenshot.md)
- Next →: [Contacts API](contacts.md)
- Same feature on other platforms: [iOS – App Version Check API](../ios/app-version-check.md)
- Languages: **🇺🇸 English** · [🇩🇪 Deutsch](../de/android/app-version-check.md) · [🇫🇷 Français](../fr/android/app-version-check.md) · [🇪🇸 Español](../es/android/app-version-check.md) · [🇨🇳 中文](../zh/android/app-version-check.md)

> [!TIP]
> **Too busy? We set up your app for you.** Our team configures, builds & submits your WebViewGold app — done-for-you, fast turnaround, Made in Germany. [Get your app set up →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_android_doc_online)
>
> **Build in your browser:** No Mac, no IDE: the **WebViewGold Cloud Builder** configures, builds & uploads your app online. [Discover Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=android_docs)
