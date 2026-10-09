---
title: "Haptic Feedback API – WebViewGold for Android Documentation"
description: "Trigger native vibration haptic feedback from your web app for a native app feeling on Android."
lang: "en"
product: "WebViewGold for Android"
platform: "Android"
category: "APIs & Features"
slug: "haptic-feedback"
canonical_url: "https://www.webviewgold.com/docs/android/haptic-feedback/"
keywords:
  - "Haptic Feedback API"
  - "WebViewGold for Android"
  - "convert website to app"
  - "WebView app documentation"
  - "Android WebView SDK"
  - "PWA to app"
  - "HTML to app"
  - "JavaScript bridge"
last_updated: "2026-10-09"
---

# Haptic Feedback API – WebViewGold for Android

> **Summary:** Trigger native vibration haptic feedback from your web app for a native app feeling on Android.

[Documentation](../README.md) › [WebViewGold for Android](README.md) › Haptic Feedback API

**Platform:** Android · **Category:** APIs & Features · **Online version:** [www.webviewgold.com/docs/android/haptic-feedback/](https://www.webviewgold.com/docs/android/haptic-feedback/)

---

**WebViewGold** allows for the implementation of native Android haptic control within your web app.
Using our API, you are able to perform the following actions:

| Name | URL scheme | Description |
| --- | --- | --- |
| Light Impact | lighthaptic:// | Used for a collision between small, light UI elements |
| Heavy Impact | heavyhaptic:// | Used for a collision between large, heavy UI elements |
| Success Notification | successhaptic:// | Indicates a task or action has been successfully completed |
| Warning Notification | warninghaptic:// | Indicates a task or action has produced a warning of some kind |
| Error Notificiation | errorhaptic:// | Indicates that an error has occurred |

An example of how this API can be utilised can be seen below, with an anchor tag and custom javascript function which interact with our haptic API.

```html
<a onclick="lightHaptic('index.html')">Navigation Link with Haptics</a>

<script>
function lightHaptic(url) {
  if (isWebViewBrowser) {
    window.location.href = url;
    loadInnerHref("lighthaptic://");
  } else {
    window.location.href = url;
  }
}

function loadInnerHref(url) {
  iFrame = document.createElement("iframe");
  iFrame.setAttribute("src", url);
  document.body.appendChild(iFrame);
  iFrame.parentNode.removeChild(iFrame);
  iFrame = null;
}
</script>
```

Click [here](https://webviewgoldtest.github.io/hapticFeedback.html) to view a demonstration web page for this feature. Inspect the page to view the example code.

---

## Continue reading

- ← Previous: [Dynamic UI API](dynamic-ui.md)
- Next →: [NFC Plugin](nfc.md)
- Same feature on other platforms: [iOS – Haptic Feedback API](../ios/haptic-feedback.md)
- Languages: **🇺🇸 English** · [🇩🇪 Deutsch](../de/android/haptic-feedback.md) · [🇫🇷 Français](../fr/android/haptic-feedback.md) · [🇪🇸 Español](../es/android/haptic-feedback.md) · [🇨🇳 中文](../zh/android/haptic-feedback.md)

> [!TIP]
> **Too busy? We set up your app for you.** Our team configures, builds & submits your WebViewGold app — done-for-you, fast turnaround, Made in Germany. [Get your app set up →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_android_doc_online)
>
> **Build in your browser:** No Mac, no IDE: the **WebViewGold Cloud Builder** configures, builds & uploads your app online. [Discover Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=android_docs)
