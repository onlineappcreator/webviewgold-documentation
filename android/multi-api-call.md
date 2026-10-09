---
title: "Multi API Call (multiapicall://) – WebViewGold for Android Documentation"
description: "Call several WebViewGold data APIs in one single window.location.href assignment — ideal for cross-platform web apps that also target the iOS version."
lang: "en"
product: "WebViewGold for Android"
platform: "Android"
category: "APIs & Features"
slug: "multi-api-call"
canonical_url: "https://www.webviewgold.com/docs/android/multi-api-call/"
keywords:
  - "Multi API Call"
  - "WebViewGold for Android"
  - "convert website to app"
  - "WebView app documentation"
  - "Android WebView SDK"
  - "PWA to app"
  - "HTML to app"
  - "JavaScript bridge"
last_updated: "2026-10-09"
---

# Multi API Call (multiapicall://) – WebViewGold for Android

> **Summary:** Call several WebViewGold data APIs in one single window.location.href assignment — ideal for cross-platform web apps that also target the iOS version.

[Documentation](../README.md) › [WebViewGold for Android](README.md) › Multi API Call

**Platform:** Android · **Category:** APIs & Features · **Online version:** [www.webviewgold.com/docs/android/multi-api-call/](https://www.webviewgold.com/docs/android/multi-api-call/)

---

The **Multi API Call feature** allows you to trigger **several WebViewGold APIs in one single *window.location.href* assignment**. This is especially useful for **cross-platform web apps**: Apple-based browsers process multiple page redirects on the same script differently than Android — calling *window.location.href = "exampleAPItrigger"* multiple times in the same script works on Android, but not on iOS. With `multiapicall://`, the very same web code works on both platforms.

## Supported APIs as entries

- [get-uuid](uuid.md)
- [getonesignalplayerid](push-notifications.md)
- [getappversion](app-version-check.md)
- [statusbarcolor](dynamic-ui.md) (followed by three entries for the RGB values)
- [statusbartextcolor](dynamic-ui.md) (followed by one entry: `black` or `white`)
- [bottombarcolor](dynamic-ui.md) (followed by three entries for the RGB values)
- [navbartextcolor](dynamic-ui.md) (followed by one entry: `black` or `white`)

## How to Use

Separate the API names (and their values, if any) by commas (`,`) — **no spaces**:

```html
<script>
// Example combination: "getonesignalplayerid" and "getappversion"
window.location.href = "multiapicall://getonesignalplayerid,getappversion";
</script>
```

Passing values to the Dynamic UI APIs works like this:

```html
<script>
// Set the status bar to red, its text color to white, and fetch the UUID — all in one call
window.location.href = "multiapicall://statusbarcolor,255,0,0,statusbartextcolor,white,get-uuid";
</script>
```

**Note:** On Android, calling the individual APIs one after another (e.g., `window.location.href = "get-uuid://";` followed by `window.location.href = "getappversion://";`) works as well. Use `multiapicall://` if you want to share one code path with the [iOS version of WebViewGold](../ios/multi-api-call.md).

Click [here](https://webviewgoldtest.github.io/multiAPI.html) to view a demonstration web page for this feature. Inspect the page to view the example code.

---

## Continue reading

- ← Previous: [Custom CSS & JS API](custom-css-js.md)
- Next →: [Geolocation API](geolocation.md)
- Same feature on other platforms: [iOS – MultiAPICall Feature](../ios/multi-api-call.md)
- Languages: **🇺🇸 English** · [🇩🇪 Deutsch](../de/android/multi-api-call.md) · [🇫🇷 Français](../fr/android/multi-api-call.md) · [🇪🇸 Español](../es/android/multi-api-call.md) · [🇨🇳 中文](../zh/android/multi-api-call.md)

> [!TIP]
> **Too busy? We set up your app for you.** Our team configures, builds & submits your WebViewGold app — done-for-you, fast turnaround, Made in Germany. [Get your app set up →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_android_doc_online)
>
> **Build in your browser:** No Mac, no IDE: the **WebViewGold Cloud Builder** configures, builds & uploads your app online. [Discover Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=android_docs)
