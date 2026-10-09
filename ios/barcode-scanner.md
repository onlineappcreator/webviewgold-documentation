---
title: "Barcode Scanner API – WebViewGold for iOS Documentation"
description: "Scan EAN, UPC, and other barcodes natively in your iOS WebView app and hand results to your web app."
lang: "en"
product: "WebViewGold for iOS"
platform: "iOS"
category: "APIs & Features"
slug: "barcode-scanner"
canonical_url: "https://www.webviewgold.com/docs/iOS/barcode-scanner/"
keywords:
  - "Barcode Scanner API"
  - "WebViewGold for iOS"
  - "convert website to app"
  - "WebView app documentation"
  - "iOS WebView SDK"
  - "PWA to app"
  - "HTML to app"
  - "JavaScript bridge"
last_updated: "2026-10-09"
---

# Barcode Scanner API – WebViewGold for iOS

> **Summary:** Scan EAN, UPC, and other barcodes natively in your iOS WebView app and hand results to your web app.

[Documentation](../README.md) › [WebViewGold for iOS](README.md) › Barcode Scanner API

**Platform:** iOS · **Category:** APIs & Features · **Online version:** [www.webviewgold.com/docs/iOS/barcode-scanner/](https://www.webviewgold.com/docs/iOS/barcode-scanner/)

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

- ← Previous: [QR Code Scanner API](qr-code-scanner.md)
- Next →: [Scanning Mode API](scanning-mode.md)
- Same feature on other platforms: [Android – Barcode Scanner API](../android/barcode-scanner.md)
- Languages: **🇺🇸 English** · [🇩🇪 Deutsch](../de/ios/barcode-scanner.md) · [🇫🇷 Français](../fr/ios/barcode-scanner.md) · [🇪🇸 Español](../es/ios/barcode-scanner.md) · [🇨🇳 中文](../zh/ios/barcode-scanner.md)

> [!TIP]
> **Too busy? We set up your app for you.** Our team configures, builds & submits your WebViewGold app — done-for-you, fast turnaround, Made in Germany. [Get your app set up →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **Build in your browser:** No Mac, no IDE: the **WebViewGold Cloud Builder** configures, builds & uploads your app online. [Discover Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
