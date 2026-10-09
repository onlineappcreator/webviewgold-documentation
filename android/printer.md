---
title: "Printer API – WebViewGold for Android Documentation"
description: "Send a remote image or PDF to the Android system print dialog — Wi-Fi printers, cloud print, or Save-as-PDF, straight from your web app."
lang: "en"
product: "WebViewGold for Android"
platform: "Android"
category: "APIs & Features"
slug: "printer"
canonical_url: "https://www.webviewgold.com/docs/android/printer/"
keywords:
  - "Printer API"
  - "WebViewGold for Android"
  - "convert website to app"
  - "WebView app documentation"
  - "Android WebView SDK"
  - "PWA to app"
  - "HTML to app"
  - "JavaScript bridge"
last_updated: "2026-10-09"
---

# Printer API – WebViewGold for Android

> **Summary:** Send a remote image or PDF to the Android system print dialog — Wi-Fi printers, cloud print, or Save-as-PDF, straight from your web app.

[Documentation](../README.md) › [WebViewGold for Android](README.md) › Printer API

**Platform:** Android · **Category:** APIs & Features · **Online version:** [www.webviewgold.com/docs/android/printer/](https://www.webviewgold.com/docs/android/printer/)

---

The **Printer API** sends a remote file (image or PDF) to the Android system print dialog, so the user can print it to any configured printer — Wi-Fi, cloud print, or "Save as PDF".

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
| `jobName` | no | Human-readable job name shown in the print dialog. Defaults to `Print Job`. |

## How It Works

1. The app downloads the file from `printItem` into a temporary cache.
2. If it is an image, the file is printed via `PrintHelper` (scaled to fit).
3. If it is a PDF (or any other document format), it is sent to the Android `PrintManager` with a proper document adapter.
4. The temporary file is deleted after the job is queued.

**Notes:** The target file must be publicly reachable from the device (the URL must resolve). Users can pick **Save as PDF** in the print dialog to export a copy.

---

## Continue reading

- ← Previous: [Document Scanner](document-scanner.md)
- Next →: [Health Connect API](health-connect.md)
- Same feature on other platforms: [iOS – Printer API](../ios/printer.md)
- Languages: **🇺🇸 English** · [🇩🇪 Deutsch](../de/android/printer.md) · [🇫🇷 Français](../fr/android/printer.md) · [🇪🇸 Español](../es/android/printer.md) · [🇨🇳 中文](../zh/android/printer.md)

> [!TIP]
> **Too busy? We set up your app for you.** Our team configures, builds & submits your WebViewGold app — done-for-you, fast turnaround, Made in Germany. [Get your app set up →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_android_doc_online)
>
> **Build in your browser:** No Mac, no IDE: the **WebViewGold Cloud Builder** configures, builds & uploads your app online. [Discover Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=android_docs)
