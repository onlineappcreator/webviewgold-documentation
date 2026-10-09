---
title: "Clipboard API – WebViewGold for iOS Documentation"
description: "Copy text to the iOS clipboard and read clipboard content from your web app via JavaScript."
lang: "en"
product: "WebViewGold for iOS"
platform: "iOS"
category: "APIs & Features"
slug: "clipboard"
canonical_url: "https://www.webviewgold.com/docs/iOS/clipboard/"
keywords:
  - "Clipboard API"
  - "WebViewGold for iOS"
  - "convert website to app"
  - "WebView app documentation"
  - "iOS WebView SDK"
  - "PWA to app"
  - "HTML to app"
  - "JavaScript bridge"
last_updated: "2026-10-09"
---

# Clipboard API – WebViewGold for iOS

> **Summary:** Copy text to the iOS clipboard and read clipboard content from your web app via JavaScript.

[Documentation](../README.md) › [WebViewGold for iOS](README.md) › Clipboard API

**Platform:** iOS · **Category:** APIs & Features · **Online version:** [www.webviewgold.com/docs/iOS/clipboard/](https://www.webviewgold.com/docs/iOS/clipboard/)

---

Call `getclipboard://` to inject the current clipboard contents into the JavaScript variable `clipboarddata`.

```html
<a href="getclipboard://">Read Clipboard</a>
<script>
function showClipboard() {
    console.log(clipboarddata);
}
</script>
```

---

## Continue reading

- ← Previous: [Shortcut API](shortcut.md)
- Next →: [Read/Write Value API](read-write-value.md)
- Same feature on other platforms: [Android – Clipboard API](../android/clipboard.md)
- Languages: **🇺🇸 English** · [🇩🇪 Deutsch](../de/ios/clipboard.md) · [🇫🇷 Français](../fr/ios/clipboard.md) · [🇪🇸 Español](../es/ios/clipboard.md) · [🇨🇳 中文](../zh/ios/clipboard.md)

> [!TIP]
> **Too busy? We set up your app for you.** Our team configures, builds & submits your WebViewGold app — done-for-you, fast turnaround, Made in Germany. [Get your app set up →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **Build in your browser:** No Mac, no IDE: the **WebViewGold Cloud Builder** configures, builds & uploads your app online. [Discover Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
