---
title: "VisionKit Document Scanner – WebViewGold for iOS Documentation"
description: "Let users scan paper documents with the camera and upload them through your web app's file upload — powered by Apple VisionKit."
lang: "en"
product: "WebViewGold for iOS"
platform: "iOS"
category: "APIs & Features"
slug: "document-scanner"
canonical_url: "https://www.webviewgold.com/docs/iOS/document-scanner/"
keywords:
  - "Document Scanner"
  - "WebViewGold for iOS"
  - "convert website to app"
  - "WebView app documentation"
  - "iOS WebView SDK"
  - "PWA to app"
  - "HTML to app"
  - "JavaScript bridge"
last_updated: "2026-10-09"
---

# VisionKit Document Scanner – WebViewGold for iOS

> **Summary:** Let users scan paper documents with the camera and upload them through your web app's file upload — powered by Apple VisionKit.

[Documentation](../README.md) › [WebViewGold for iOS](README.md) › Document Scanner

**Platform:** iOS · **Category:** APIs & Features · **Online version:** [www.webviewgold.com/docs/iOS/document-scanner/](https://www.webviewgold.com/docs/iOS/document-scanner/)

---

The **Document Scanner** feature adds a **Scan Document** option to the standard file-upload chooser of your app. The user can scan one or more pages with the camera; the app produces a document scan and uploads it through the standard `<input type="file">` flow used by your web app. It is powered by Apple's **VisionKit** framework (`VNDocumentCameraViewController`) — with automatic edge detection, cropping, and enhancement.

## How to Enable

Turn the feature on in **Config.swift**:

```swift
var kVisionKitEnable = true
```

Set to `false` to hide the **Scan Document** entry.

## User Experience

1. On your web page, the user taps an `<input type="file">`.
2. The app shows an upload dialog with entries such as *Scan Document*, *Camera*, and *Photo Library*.
3. Tapping **Scan Document** launches the VisionKit scanner: it detects edges, crops and enhances each page, and allows adding more pages.
4. The resulting scan is fed back into the `<input type="file">` — your web app receives it exactly like any other uploaded file.

**Notes:** Requires iOS 18.4 or higher and a device that supports the VisionKit document camera. On unsupported devices, the **Scan Document** entry is hidden automatically.

---

## Continue reading

- ← Previous: [Scanning Mode API](scanning-mode.md)
- Next →: [Take Screenshot API](take-screenshot.md)
- Same feature on other platforms: [Android – Document Scanner](../android/document-scanner.md)
- Languages: **🇺🇸 English** · [🇩🇪 Deutsch](../de/ios/document-scanner.md) · [🇫🇷 Français](../fr/ios/document-scanner.md) · [🇪🇸 Español](../es/ios/document-scanner.md) · [🇨🇳 中文](../zh/ios/document-scanner.md)

> [!TIP]
> **Too busy? We set up your app for you.** Our team configures, builds & submits your WebViewGold app — done-for-you, fast turnaround, Made in Germany. [Get your app set up →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **Build in your browser:** No Mac, no IDE: the **WebViewGold Cloud Builder** configures, builds & uploads your app online. [Discover Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
