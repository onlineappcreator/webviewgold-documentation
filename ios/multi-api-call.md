---
title: "MultiAPICall Feature – WebViewGold for iOS Documentation"
description: "Chain multiple WebViewGold API calls in a single request with the MultiAPICall feature for iOS."
lang: "en"
product: "WebViewGold for iOS"
platform: "iOS"
category: "Extensions & Plugins"
slug: "multi-api-call"
canonical_url: "https://www.webviewgold.com/docs/iOS/multi-api-call/"
keywords:
  - "MultiAPICall Feature"
  - "WebViewGold for iOS"
  - "convert website to app"
  - "WebView app documentation"
  - "iOS WebView SDK"
  - "PWA to app"
  - "HTML to app"
  - "JavaScript bridge"
last_updated: "2026-10-09"
---

# MultiAPICall Feature – WebViewGold for iOS

> **Summary:** Chain multiple WebViewGold API calls in a single request with the MultiAPICall feature for iOS.

[Documentation](../README.md) › [WebViewGold for iOS](README.md) › MultiAPICall Feature

**Platform:** iOS · **Category:** Extensions & Plugins · **Online version:** [www.webviewgold.com/docs/iOS/multi-api-call/](https://www.webviewgold.com/docs/iOS/multi-api-call/)

---

This is an **optional feature for iOS** since Apple-based browsers process multiple page reloads on the same script differently to Android-based browsers.
This means calling *window.location.href = "exampleAPItrigger"* multiple times on the same web page script will not work on iOS, unlike on Android.\
The MultiAPICall feature **allows you to call multiple APIs in a single *window.location.href* assignment** at the end of your web page script. This may be useful to you if you wanted to pre-load more than one data feature from the app, ready to be used on a page.\
**MultiAPICall supports the following data collection APIs as entries:**
"[get-uuid](uuid.md)", "[user-disable-tracking](user-tracking.md)", "[getonesignalplayerid](push-notifications.md#getonesignalid)", "[getappversion](app-version-check.md)", "[__haptics (light, medium, heavy, success, warning, error)](haptic-feedback.md)"\
Use JavaScript to this kind of URL to call multiple APIs at once (**make sure to include a check to only use on the iOS platform**):

```html
<script>
// Example combination: "getonesignalplayerid" and "getappversion"

if (getMobileOperatingSystem() == "iOS") {
    // iOS: Use MultiAPICall feature, separate API names by commas (","), NO spaces
    window.location.href = "multiapicall://getonesignalplayerid,getappversion";
} else {
    // Android: Can handle multiple calls at once, use normal API call structure
    window.location.href = "getonesignalplayerid://";
    window.location.href = "getappversion://";
}
</script>
```

Click [here](https://webviewgoldtest.github.io/multiAPI.html) to view a demonstration web page for this feature. Inspect the page to view the example code.

---

## Continue reading

- ← Previous: [Screen Capture Detection](screen-capture.md)
- Next →: [NFC Plugin](nfc.md)
- Same feature on other platforms: [Android – Multi API Call](../android/multi-api-call.md)
- Languages: **🇺🇸 English** · [🇩🇪 Deutsch](../de/ios/multi-api-call.md) · [🇫🇷 Français](../fr/ios/multi-api-call.md) · [🇪🇸 Español](../es/ios/multi-api-call.md) · [🇨🇳 中文](../zh/ios/multi-api-call.md)

> [!TIP]
> **Too busy? We set up your app for you.** Our team configures, builds & submits your WebViewGold app — done-for-you, fast turnaround, Made in Germany. [Get your app set up →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **Build in your browser:** No Mac, no IDE: the **WebViewGold Cloud Builder** configures, builds & uploads your app online. [Discover Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
