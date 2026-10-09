---
title: "ML Kit Document Scanner (PDF) – WebViewGold for Android Documentation"
description: "Add a Scan document option to the file upload dialog — the user scans up to 5 pages and your web app receives a PDF like any other upload."
lang: "en"
product: "WebViewGold for Android"
platform: "Android"
category: "APIs & Features"
slug: "document-scanner"
canonical_url: "https://www.webviewgold.com/docs/android/document-scanner/"
keywords:
  - "Document Scanner"
  - "WebViewGold for Android"
  - "convert website to app"
  - "WebView app documentation"
  - "Android WebView SDK"
  - "PWA to app"
  - "HTML to app"
  - "JavaScript bridge"
last_updated: "2026-10-09"
---

# ML Kit Document Scanner (PDF) – WebViewGold for Android

> **Summary:** Add a Scan document option to the file upload dialog — the user scans up to 5 pages and your web app receives a PDF like any other upload.

[Documentation](../README.md) › [WebViewGold for Android](README.md) › Document Scanner

**Platform:** Android · **Category:** APIs & Features · **Online version:** [www.webviewgold.com/docs/android/document-scanner/](https://www.webviewgold.com/docs/android/document-scanner/)

---

The **Document Scanner** feature adds a **Scan document** option to the standard file-upload chooser. The user can scan up to 5 pages with the camera; the app produces a PDF and uploads it through the standard `<input type="file">` flow used by your web app. It is powered by Google's ML Kit Document Scanner.

## How to Enable

Turn the feature on in **Config.java**:

```java
public static final boolean ENABLE_ML_KIT_DOCUMENT_SCANNER = true;
```

Set to `false` to hide the **Scan document** entry.

## User Experience

1. On your web page, the user taps an `<input type="file">`.
2. The app shows an upload dialog with entries such as *Scan document*, *Take photo*, *Capture video*, and *Choose from gallery* (depending on the input's `accept` attribute).
3. Tapping **Scan document** launches Google's ML Kit scanner: it detects edges, crops and enhances each page, allows adding more pages, and returns a PDF.
4. The resulting PDF is fed back into the `<input type="file">` — your web app receives it exactly like any other uploaded file.

**Notes:** Requires Google Play Services (available on all standard Android phones with Play Store). Result format is **PDF**, maximum 5 pages per scan. Gallery import inside the scanner is allowed by default.

---

## Continue reading

- ← Previous: [Biometric Auth API](biometric-auth.md)
- Next →: [Printer API](printer.md)
- Same feature on other platforms: [iOS – Document Scanner](../ios/document-scanner.md)
- Languages: **🇺🇸 English** · [🇩🇪 Deutsch](../de/android/document-scanner.md) · [🇫🇷 Français](../fr/android/document-scanner.md) · [🇪🇸 Español](../es/android/document-scanner.md) · [🇨🇳 中文](../zh/android/document-scanner.md)

> [!TIP]
> **Too busy? We set up your app for you.** Our team configures, builds & submits your WebViewGold app — done-for-you, fast turnaround, Made in Germany. [Get your app set up →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_android_doc_online)
>
> **Build in your browser:** No Mac, no IDE: the **WebViewGold Cloud Builder** configures, builds & uploads your app online. [Discover Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=android_docs)
