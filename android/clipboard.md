---
title: "Clipboard API – WebViewGold for Android Documentation"
description: "Copy text to the Android clipboard and read clipboard content from your web app via JavaScript."
lang: "en"
product: "WebViewGold for Android"
platform: "Android"
category: "APIs & Features"
slug: "clipboard"
canonical_url: "https://www.webviewgold.com/docs/android/clipboard/"
keywords:
  - "Clipboard API"
  - "WebViewGold for Android"
  - "convert website to app"
  - "WebView app documentation"
  - "Android WebView SDK"
  - "PWA to app"
  - "HTML to app"
  - "JavaScript bridge"
last_updated: "2026-10-09"
---

# Clipboard API – WebViewGold for Android

> **Summary:** Copy text to the Android clipboard and read clipboard content from your web app via JavaScript.

[Documentation](../README.md) › [WebViewGold for Android](README.md) › Clipboard API

**Platform:** Android · **Category:** APIs & Features · **Online version:** [www.webviewgold.com/docs/android/clipboard/](https://www.webviewgold.com/docs/android/clipboard/)

---

The WebViewGold Clipboard API provides a simple and secure way to access the device clipboard contents from within your WebView-based app. This serves as an alternative to relying on native WebView clipboard access, offering more reliability across platforms and updates.

## Use Cases

- Pre-filling form fields with copied data
- Enhancing user flows in authentication, note-taking, or sharing apps
- Creating quick paste features or clipboard history tools

## How to Retrieve Clipboard Content

To access the clipboard data, use the following call:

```html
<a href="getclipboard://">Get Clipboard Data</a>
<a href="#" onClick="alert(clipboarddata);">Show Clipboard Data</a>
```

- **Get Clipboard Data:** Triggers the native clipboard read functionality.
- **Show Clipboard Data:** Displays the result stored in the `clipboarddata` JavaScript variable.

**Technical Note:** Once `getclipboard://` is triggered, WebViewGold automatically injects the clipboard content into the `clipboarddata` JavaScript variable on the page, making it accessible for any further actions.

---

## Continue reading

- ← Previous: [Loading Sign API](loading-sign.md)
- Next →: [UUID API](uuid.md)
- Same feature on other platforms: [iOS – Clipboard API](../ios/clipboard.md)
- Languages: **🇺🇸 English** · [🇩🇪 Deutsch](../de/android/clipboard.md) · [🇫🇷 Français](../fr/android/clipboard.md) · [🇪🇸 Español](../es/android/clipboard.md) · [🇨🇳 中文](../zh/android/clipboard.md)

> [!TIP]
> **Too busy? We set up your app for you.** Our team configures, builds & submits your WebViewGold app — done-for-you, fast turnaround, Made in Germany. [Get your app set up →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_android_doc_online)
>
> **Build in your browser:** No Mac, no IDE: the **WebViewGold Cloud Builder** configures, builds & uploads your app online. [Discover Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=android_docs)
