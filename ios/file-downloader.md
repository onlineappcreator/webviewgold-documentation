---
title: "File Downloader API – WebViewGold for iOS Documentation"
description: "Let users download images, PDFs, and other files from your web app straight to their iPhone or iPad."
lang: "en"
product: "WebViewGold for iOS"
platform: "iOS"
category: "APIs & Features"
slug: "file-downloader"
canonical_url: "https://www.webviewgold.com/docs/iOS/file-downloader/"
keywords:
  - "File Downloader API"
  - "WebViewGold for iOS"
  - "convert website to app"
  - "WebView app documentation"
  - "iOS WebView SDK"
  - "PWA to app"
  - "HTML to app"
  - "JavaScript bridge"
last_updated: "2026-10-09"
---

# File Downloader API – WebViewGold for iOS

> **Summary:** Let users download images, PDFs, and other files from your web app straight to their iPhone or iPad.

[Documentation](../README.md) › [WebViewGold for iOS](README.md) › File Downloader API

**Platform:** iOS · **Category:** APIs & Features · **Online version:** [www.webviewgold.com/docs/iOS/file-downloader/](https://www.webviewgold.com/docs/iOS/file-downloader/)

---

WebViewGold’s Download API allows you to provide document, image, and audio file downloads within your WebView app. The following steps outline how to enable and customize the downloader functionality:

## 1. Downloading Images

Save images to the camera roll of the user by calling links with savethisimage://?url= prefix:

```html
<a href="savethisimage://?url=IMAGE URL HERE">Download Image</a>
```

## 2. Downloading Files

Save files by calling links with a relevant suffix (e.g., .mp3):

```html
<a href="https://www.example.org/file.pdf">Link PDF</a>
<a href="https://www.example.org/file.mp3">Link mp3 Music</a>
<a href="https://www.example.org/file.mp4">Link mp4 Music</a>
<a href="https://www.example.org/file.wav">Link wav Music</a>
<a href="https://www.example.org/file.epub">Link epub eBook</a>
<a href="https://www.example.org/file.pkpass">Link Passbook / Apple Wallet</a>
<a href="https://www.example.org/file.docx">Link Word</a>
<a href="https://www.example.org/file.pptx">Link PowerPoint</a>
<a href="https://www.example.org/file.xlsx">Link Excel</a>
```

## 3. Customizing Supported File Types

You can add more filetypes that should trigger the file downloader functionality (e.g., .epub, .zip, ...) This can be done via the list variable `extentionARY` that can be found in the **Config.swift** file.

## 4. Enabling Automatic File Downloads

Consider setting the `autodownloader` option in **Config.swift** to enable automatic downloads for files flagged with Content-Disposition HTTP headers, independent of the `extentionARY` list. This ensures files are downloaded automatically based on server configurations.

[![Watch the video: File Downloader API](https://img.youtube.com/vi/V0LnwnzJx6I/hqdefault.jpg)](https://www.youtube.com/watch?v=V0LnwnzJx6I)

---

## Continue reading

- ← Previous: [Native Video API](native-video.md)
- Next →: [Printer API](printer.md)
- Same feature on other platforms: [Android – File Downloader API](../android/file-downloader.md)
- Languages: **🇺🇸 English** · [🇩🇪 Deutsch](../de/ios/file-downloader.md) · [🇫🇷 Français](../fr/ios/file-downloader.md) · [🇪🇸 Español](../es/ios/file-downloader.md) · [🇨🇳 中文](../zh/ios/file-downloader.md)

> [!TIP]
> **Too busy? We set up your app for you.** Our team configures, builds & submits your WebViewGold app — done-for-you, fast turnaround, Made in Germany. [Get your app set up →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **Build in your browser:** No Mac, no IDE: the **WebViewGold Cloud Builder** configures, builds & uploads your app online. [Discover Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
