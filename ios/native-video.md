---
title: "Native Video Player API – WebViewGold for iOS Documentation"
description: "Play video streams in the native iOS video player with Picture-in-Picture support — triggered straight from your web app."
lang: "en"
product: "WebViewGold for iOS"
platform: "iOS"
category: "APIs & Features"
slug: "native-video"
canonical_url: "https://www.webviewgold.com/docs/iOS/native-video/"
keywords:
  - "Native Video API"
  - "WebViewGold for iOS"
  - "convert website to app"
  - "WebView app documentation"
  - "iOS WebView SDK"
  - "PWA to app"
  - "HTML to app"
  - "JavaScript bridge"
last_updated: "2026-10-09"
---

# Native Video Player API – WebViewGold for iOS

> **Summary:** Play video streams in the native iOS video player with Picture-in-Picture support — triggered straight from your web app.

[Documentation](../README.md) › [WebViewGold for iOS](README.md) › Native Video API

**Platform:** iOS · **Category:** APIs & Features · **Online version:** [www.webviewgold.com/docs/iOS/native-video/](https://www.webviewgold.com/docs/iOS/native-video/)

---

The **Native Video Player API** allows your website to launch a video stream in the native iOS video player with **Picture-in-Picture** support. Trigger the native playback by opening a link with the `startnativevideo://videostreamurl=` prefix:

```html
<a href="startnativevideo://videostreamurl=YOUR_VIDEO_STREAM_URL">Play Video in System Video Player with PiP Support</a>
```

The user can continue watching the video in a floating Picture-in-Picture window while navigating your web app or even other apps.

## Typical Use Cases

- Live streams that should keep playing while the user browses your web app.
- Video courses or tutorials with system-level playback controls.
- Any video that benefits from AirPlay, fullscreen, and Picture-in-Picture support of the native player.

**Note:** Use a direct video stream URL (e.g., an .mp4 file or an HLS .m3u8 stream) — not the URL of an HTML page embedding the video.

---

## Continue reading

- ← Previous: [HTML Audio API](html-audio.md)
- Next →: [File Downloader API](file-downloader.md)
- Same feature on other platforms: [Android – Native Video (PiP) API](../android/native-video.md)
- Languages: **🇺🇸 English** · [🇩🇪 Deutsch](../de/ios/native-video.md) · [🇫🇷 Français](../fr/ios/native-video.md) · [🇪🇸 Español](../es/ios/native-video.md) · [🇨🇳 中文](../zh/ios/native-video.md)

> [!TIP]
> **Too busy? We set up your app for you.** Our team configures, builds & submits your WebViewGold app — done-for-you, fast turnaround, Made in Germany. [Get your app set up →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **Build in your browser:** No Mac, no IDE: the **WebViewGold Cloud Builder** configures, builds & uploads your app online. [Discover Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
