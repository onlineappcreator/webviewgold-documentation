---
title: "原生视频播放器 API – WebViewGold for iOS 文档"
description: "在 iOS 原生视频播放器中播放视频流并支持画中画——直接从您的 Web 应用触发。"
lang: "zh"
product: "WebViewGold for iOS"
platform: "iOS"
category: "API 与功能"
slug: "native-video"
canonical_url: "https://www.webviewgold.com/zh/docs/iOS/native-video/"
keywords:
  - "原生视频 API"
  - "WebViewGold for iOS"
  - "将网站转换为应用"
  - "WebView 应用文档"
  - "iOS WebView SDK"
  - "PWA 转应用"
  - "HTML 转应用"
  - "JavaScript 桥接"
last_updated: "2026-10-09"
---

# 原生视频播放器 API – WebViewGold for iOS

> **摘要：** 在 iOS 原生视频播放器中播放视频流并支持画中画——直接从您的 Web 应用触发。

[文档](../README.md) › [WebViewGold for iOS](README.md) › 原生视频 API

**平台：** iOS · **类别：** API 与功能 · **在线版本：** [www.webviewgold.com/zh/docs/iOS/native-video/](https://www.webviewgold.com/zh/docs/iOS/native-video/)

---

**原生视频播放器 API** 允许您的网站在 iOS 原生视频播放器中启动视频流，并支持**画中画**（Picture-in-Picture）。通过打开带有 `startnativevideo://videostreamurl=` 前缀的链接来触发原生播放：

```html
<a href="startnativevideo://videostreamurl=YOUR_VIDEO_STREAM_URL">在系统视频播放器中播放（支持画中画）</a>
```

用户可以在浮动的画中画窗口中继续观看视频，同时浏览您的 Web 应用甚至其他应用。

## 典型使用场景

- 用户浏览您的 Web 应用时仍需继续播放的直播流。
- 带有系统级播放控制的视频课程或教程。
- 任何受益于原生播放器的 AirPlay、全屏和画中画功能的视频。

**注意：**请使用直接的视频流 URL（例如 .mp4 文件或 HLS .m3u8 流），而不是嵌入视频的 HTML 页面 URL。

---

## 继续阅读

- ← 上一页： [HTML 音频 API](html-audio.md)
- 下一页 →： [文件下载 API](file-downloader.md)
- 其他平台上的相同功能： [Android – 原生视频（PiP）API](../android/native-video.md)
- 语言： [🇺🇸 English](../../ios/native-video.md) · [🇩🇪 Deutsch](../../de/ios/native-video.md) · [🇫🇷 Français](../../fr/ios/native-video.md) · [🇪🇸 Español](../../es/ios/native-video.md) · **🇨🇳 中文**

> [!TIP]
> **太忙了？我们替您搭建应用。** 我们的团队为您配置、构建并提交 WebViewGold 应用——全程代劳、交付迅速、德国制造。 [让我们搭建应用 →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **在浏览器中构建：** 无需 Mac、无需 IDE：**WebViewGold Cloud Builder** 在线为您配置、构建并上传应用。 [了解 Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
