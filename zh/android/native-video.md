---
title: "支持 Picture-in-Picture 的原生视频 API – WebViewGold for Android 文档"
description: "在您的 Android WebView 应用中以原生方式播放视频，并支持 Picture-in-Picture 画中画。"
lang: "zh"
product: "WebViewGold for Android"
platform: "Android"
category: "API 与功能"
slug: "native-video"
canonical_url: "https://www.webviewgold.com/zh/docs/android/native-video/"
keywords:
  - "原生视频（PiP）API"
  - "WebViewGold for Android"
  - "将网站转换为应用"
  - "WebView 应用文档"
  - "Android WebView SDK"
  - "PWA 转应用"
  - "HTML 转应用"
  - "JavaScript 桥接"
last_updated: "2026-10-09"
---

# 支持 Picture-in-Picture 的原生视频 API – WebViewGold for Android

> **摘要：** 在您的 Android WebView 应用中以原生方式播放视频，并支持 Picture-in-Picture 画中画。

[文档](../README.md) › [WebViewGold for Android](README.md) › 原生视频（PiP）API

**平台：** Android · **类别：** API 与功能 · **在线版本：** [www.webviewgold.com/zh/docs/android/native-video/](https://www.webviewgold.com/zh/docs/android/native-video/)

---

Native Video API 允许您的网站在设备的原生播放器中启动视频流，并支持画中画（Picture-in-Picture）。通过打开带有 `startnativevideo://videostreamurl=` 前缀的链接来触发原生播放：

```html
<a href="startnativevideo://videostreamurl=YOUR_VIDEO_STREAM_URL">Play Video in System Video Player with PiP Support</a>
```

用户可以在浮动窗口中继续观看视频，同时浏览您的应用或其他应用。

---

## 继续阅读

- ← 上一页： [文件下载 API](file-downloader.md)
- 下一页 →： [重置应用 API](reset-app.md)
- 其他平台上的相同功能： [iOS – 原生视频 API](../ios/native-video.md)
- 语言： [🇺🇸 English](../../android/native-video.md) · [🇩🇪 Deutsch](../../de/android/native-video.md) · [🇫🇷 Français](../../fr/android/native-video.md) · [🇪🇸 Español](../../es/android/native-video.md) · **🇨🇳 中文**

> [!TIP]
> **太忙了？我们替您搭建应用。** 我们的团队为您配置、构建并提交 WebViewGold 应用——全程代劳、交付迅速、德国制造。 [让我们搭建应用 →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_android_doc_online)
>
> **在浏览器中构建：** 无需 Mac、无需 IDE：**WebViewGold Cloud Builder** 在线为您配置、构建并上传应用。 [了解 Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=android_docs)
