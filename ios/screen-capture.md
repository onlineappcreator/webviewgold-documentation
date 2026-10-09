---
title: "Screen Capture Detection – WebViewGold for iOS Documentation"
description: "Detect screenshots and screen recordings in your iOS app and react from your web app."
lang: "en"
product: "WebViewGold for iOS"
platform: "iOS"
category: "Extensions & Plugins"
slug: "screen-capture"
canonical_url: "https://www.webviewgold.com/docs/iOS/screen-capture/"
keywords:
  - "Screen Capture Detection"
  - "WebViewGold for iOS"
  - "convert website to app"
  - "WebView app documentation"
  - "iOS WebView SDK"
  - "PWA to app"
  - "HTML to app"
  - "JavaScript bridge"
last_updated: "2026-10-09"
---

# Screen Capture Detection – WebViewGold for iOS

> **Summary:** Detect screenshots and screen recordings in your iOS app and react from your web app.

[Documentation](../README.md) › [WebViewGold for iOS](README.md) › Screen Capture Detection

**Platform:** iOS · **Category:** Extensions & Plugins · **Online version:** [www.webviewgold.com/docs/iOS/screen-capture/](https://www.webviewgold.com/docs/iOS/screen-capture/)

---

Set `let preventScreenCapture = true` in `Config.swift` to detect screenshots or screen recordings and automatically call the JavaScript function `onScreenCaptureAttempt`.

```html
<script>
function onScreenCaptureAttempt() {
    alert('Screen capture detected');
}
</script>
```

---

## Continue reading

- ← Previous: [Native Sidebar](sidebar.md)
- Next →: [MultiAPICall Feature](multi-api-call.md)
- Languages: **🇺🇸 English** · [🇩🇪 Deutsch](../de/ios/screen-capture.md) · [🇫🇷 Français](../fr/ios/screen-capture.md) · [🇪🇸 Español](../es/ios/screen-capture.md) · [🇨🇳 中文](../zh/ios/screen-capture.md)

> [!TIP]
> **Too busy? We set up your app for you.** Our team configures, builds & submits your WebViewGold app — done-for-you, fast turnaround, Made in Germany. [Get your app set up →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **Build in your browser:** No Mac, no IDE: the **WebViewGold Cloud Builder** configures, builds & uploads your app online. [Discover Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
