---
title: "Haptic Feedback API – WebViewGold for iOS Documentation"
description: "Trigger native haptic feedback (vibrations) from your web app for a truly native app feeling on iOS."
lang: "en"
product: "WebViewGold for iOS"
platform: "iOS"
category: "APIs & Features"
slug: "haptic-feedback"
canonical_url: "https://www.webviewgold.com/docs/iOS/haptic-feedback/"
keywords:
  - "Haptic Feedback API"
  - "WebViewGold for iOS"
  - "convert website to app"
  - "WebView app documentation"
  - "iOS WebView SDK"
  - "PWA to app"
  - "HTML to app"
  - "JavaScript bridge"
last_updated: "2026-10-09"
---

# Haptic Feedback API – WebViewGold for iOS

> **Summary:** Trigger native haptic feedback (vibrations) from your web app for a truly native app feeling on iOS.

[Documentation](../README.md) › [WebViewGold for iOS](README.md) › Haptic Feedback API

**Platform:** iOS · **Category:** APIs & Features · **Online version:** [www.webviewgold.com/docs/iOS/haptic-feedback/](https://www.webviewgold.com/docs/iOS/haptic-feedback/)

---

**WebViewGold** allows for the implementation of native iOS haptic control within your web app.
Using our API, you are able to perform the following actions:

| Name | URL scheme | Description |
| --- | --- | --- |
| Light Impact | lighthaptic:// | Used for a collision between small, light UI elements |
| Medium Impact | mediumhaptic:// | Used for a collision between moderately sized UI elements |
| Heavy Impact | heavyhaptic:// | Used for a collision between large, heavy UI elements |
| Success Notification | successhaptic:// | Indicates a task or action has been successfully completed |
| Warning Notification | warninghaptic:// | Indicates a task or action has produced a warning of some kind |
| Error Notificiation | errorhaptic:// | Indicates that an error has occurred |

We suggest previewing Apple's [best practices](https://developer.apple.com/design/human-interface-guidelines/playing-haptics) overview before including these features into your application.
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

- ← Previous: [Biometric Auth API](biometric-authentication.md)
- Next →: [Shortcut API](shortcut.md)
- Same feature on other platforms: [Android – Haptic Feedback API](../android/haptic-feedback.md)
- Languages: **🇺🇸 English** · [🇩🇪 Deutsch](../de/ios/haptic-feedback.md) · [🇫🇷 Français](../fr/ios/haptic-feedback.md) · [🇪🇸 Español](../es/ios/haptic-feedback.md) · [🇨🇳 中文](../zh/ios/haptic-feedback.md)

> [!TIP]
> **Too busy? We set up your app for you.** Our team configures, builds & submits your WebViewGold app — done-for-you, fast turnaround, Made in Germany. [Get your app set up →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **Build in your browser:** No Mac, no IDE: the **WebViewGold Cloud Builder** configures, builds & uploads your app online. [Discover Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
