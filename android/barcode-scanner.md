---
title: "Barcode Scanner API – WebViewGold for Android Documentation"
description: "Scan EAN, UPC, and other barcodes natively in your Android WebView app and hand results to your web app."
lang: "en"
product: "WebViewGold for Android"
platform: "Android"
category: "APIs & Features"
slug: "barcode-scanner"
canonical_url: "https://www.webviewgold.com/docs/android/barcode-scanner/"
keywords:
  - "Barcode Scanner API"
  - "WebViewGold for Android"
  - "convert website to app"
  - "WebView app documentation"
  - "Android WebView SDK"
  - "PWA to app"
  - "HTML to app"
  - "JavaScript bridge"
last_updated: "2026-10-09"
---

# Barcode Scanner API – WebViewGold for Android

> **Summary:** Scan EAN, UPC, and other barcodes natively in your Android WebView app and hand results to your web app.

[Documentation](../README.md) › [WebViewGold for Android](README.md) › Barcode Scanner API

**Platform:** Android · **Category:** APIs & Features · **Online version:** [www.webviewgold.com/docs/android/barcode-scanner/](https://www.webviewgold.com/docs/android/barcode-scanner/)

---

The WebViewGold Barcode Scanner API enables your WebView-based app to activate the device camera for scanning barcodes. Once a barcode is successfully scanned, the result is automatically passed back into your web content.

## Use Cases

- Scanning product barcodes for inventory systems
- Processing tickets or access codes in logistics or event apps
- Enabling fast data capture from printed barcodes

## How to Trigger the Scanner

Use the following HTML to start the native barcode scanner:

```html
<a href="barcodescanner://">Start Barcode Scanner</a>
<a href="#" onClick="alert(barcodescanresult);">Show Scan Result</a>
```

- **Start Barcode Scanner:** Opens the device camera to detect supported barcode formats
- **Show Scan Result:** Displays the scanned barcode content stored in the `barcodescanresult` JavaScript variable

**Technical Note:** After scanning, the decoded barcode value is injected into the current page via the `barcodescanresult` JavaScript variable. You can use this variable to auto-fill forms, trigger custom logic, or perform lookups based on scanned data.

**Permissions:** Make sure the app has access to the device camera, as it is required for barcode scanning to function properly.

---

## Continue reading

- ← Previous: [Scanning Mode API](scanning-mode.md)
- Next →: [Take Screenshot API](take-screenshot.md)
- Same feature on other platforms: [iOS – Barcode Scanner API](../ios/barcode-scanner.md)
- Languages: **🇺🇸 English** · [🇩🇪 Deutsch](../de/android/barcode-scanner.md) · [🇫🇷 Français](../fr/android/barcode-scanner.md) · [🇪🇸 Español](../es/android/barcode-scanner.md) · [🇨🇳 中文](../zh/android/barcode-scanner.md)

> [!TIP]
> **Too busy? We set up your app for you.** Our team configures, builds & submits your WebViewGold app — done-for-you, fast turnaround, Made in Germany. [Get your app set up →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_android_doc_online)
>
> **Build in your browser:** No Mac, no IDE: the **WebViewGold Cloud Builder** configures, builds & uploads your app online. [Discover Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=android_docs)
