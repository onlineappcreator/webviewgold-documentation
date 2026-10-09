---
title: "File Downloader API – WebViewGold for Android Documentation"
description: "Let users download images, PDFs, and other files from your web app to their Android device."
lang: "en"
product: "WebViewGold for Android"
platform: "Android"
category: "APIs & Features"
slug: "file-downloader"
canonical_url: "https://www.webviewgold.com/docs/android/file-downloader/"
keywords:
  - "File Downloader API"
  - "WebViewGold for Android"
  - "convert website to app"
  - "WebView app documentation"
  - "Android WebView SDK"
  - "PWA to app"
  - "HTML to app"
  - "JavaScript bridge"
last_updated: "2026-10-09"
---

# File Downloader API – WebViewGold for Android

> **Summary:** Let users download images, PDFs, and other files from your web app to their Android device.

[Documentation](../README.md) › [WebViewGold for Android](README.md) › File Downloader API

**Platform:** Android · **Category:** APIs & Features · **Online version:** [www.webviewgold.com/docs/android/file-downloader/](https://www.webviewgold.com/docs/android/file-downloader/)

---

WebViewGold’s Download API allows you to provide document, image, and audio file downloads within your WebView app. The following steps outline how to enable and customize the downloader functionality:

## 1. Downloading Images

Save images to the camera roll of the user by calling links with savethisimage://?url= prefix:

```html
<a href="savethisimage://?url=IMAGE URL HERE">Download Image</a>
```

## 2. Downloading PDF Files

Save PDF files by calling links with a .pdf suffix:

```html
<a href="https://www.example.org/file.pdf">Download PDF</a>
```

## 3. Downloading Music Files

Save music files by simply calling links with a .mp3, .mp4 or .wav suffix:

```html
<a href="https://www.example.org/file.mp3">Download MP3</a>
<a href="https://www.example.org/file.mp4">Download MP4</a>
<a href="https://www.example.org/file.wav">Download WAV</a>
```

## 4. Customizing Supported File Types

To add additional file formats to the downloader, insert them into the `downloadableExtension` list in **Config.java**.

## 5. Enabling Automatic File Downloads

Consider setting the `AUTO_DOWNLOAD_FILES` option in **Config.java** to enable automatic downloads for files flagged with Content-Disposition HTTP headers, independent of the `downloadableExtension` list. This ensures files are downloaded automatically based on server configurations.

---

## Continue reading

- ← Previous: [Facebook Ads API](facebook-ads.md)
- Next →: [Native Video (PiP) API](native-video.md)
- Same feature on other platforms: [iOS – File Downloader API](../ios/file-downloader.md)
- Languages: **🇺🇸 English** · [🇩🇪 Deutsch](../de/android/file-downloader.md) · [🇫🇷 Français](../fr/android/file-downloader.md) · [🇪🇸 Español](../es/android/file-downloader.md) · [🇨🇳 中文](../zh/android/file-downloader.md)

> [!TIP]
> **Too busy? We set up your app for you.** Our team configures, builds & submits your WebViewGold app — done-for-you, fast turnaround, Made in Germany. [Get your app set up →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_android_doc_online)
>
> **Build in your browser:** No Mac, no IDE: the **WebViewGold Cloud Builder** configures, builds & uploads your app online. [Discover Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=android_docs)
