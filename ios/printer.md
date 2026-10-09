---
title: "Printer API – WebViewGold for iOS Documentation"
description: "Print images and PDFs from your web app via AirPrint: send files to the native iOS print dialog with a single link."
lang: "en"
product: "WebViewGold for iOS"
platform: "iOS"
category: "APIs & Features"
slug: "printer"
canonical_url: "https://www.webviewgold.com/docs/iOS/printer/"
keywords:
  - "Printer API"
  - "WebViewGold for iOS"
  - "convert website to app"
  - "WebView app documentation"
  - "iOS WebView SDK"
  - "PWA to app"
  - "HTML to app"
  - "JavaScript bridge"
last_updated: "2026-10-09"
---

# Printer API – WebViewGold for iOS

> **Summary:** Print images and PDFs from your web app via AirPrint: send files to the native iOS print dialog with a single link.

[Documentation](../README.md) › [WebViewGold for iOS](README.md) › Printer API

**Platform:** iOS · **Category:** APIs & Features · **Online version:** [www.webviewgold.com/docs/iOS/printer/](https://www.webviewgold.com/docs/iOS/printer/)

---

The **Printer API** sends a remote file (image or PDF) to the native iOS print dialog (**AirPrint**), so the user can print it to any configured printer or save it as a PDF.

## How to Use

```html
<a href="printitem://?jobName=Invoice%20%23123&printItem=https://example.com/invoice.pdf">
  Print invoice
</a>
```

## Query Parameters

| Name | Required | Description |
| --- | --- | --- |
| `printItem` | yes | Full URL of the file to print (PDF, JPG, PNG, WebP…). |
| `jobName` | no | Human-readable job name shown in the print dialog. |

## How It Works

1. The app downloads the file from `printItem` into a temporary cache.
2. The file is handed to the native `UIPrintInteractionController`, which shows the iOS print dialog.
3. The user picks an AirPrint printer (or **Save as PDF** via the share options) and confirms.

**Notes:** The target file must be publicly reachable from the device (the URL must resolve). URL-encode special characters in the `jobName` parameter (e.g., `%20` for spaces).

---

## Continue reading

- ← Previous: [File Downloader API](file-downloader.md)
- Next →: [iCal Calendar API](ical-calendar.md)
- Same feature on other platforms: [Android – Printer API](../android/printer.md)
- Languages: **🇺🇸 English** · [🇩🇪 Deutsch](../de/ios/printer.md) · [🇫🇷 Français](../fr/ios/printer.md) · [🇪🇸 Español](../es/ios/printer.md) · [🇨🇳 中文](../zh/ios/printer.md)

> [!TIP]
> **Too busy? We set up your app for you.** Our team configures, builds & submits your WebViewGold app — done-for-you, fast turnaround, Made in Germany. [Get your app set up →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **Build in your browser:** No Mac, no IDE: the **WebViewGold Cloud Builder** configures, builds & uploads your app online. [Discover Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
