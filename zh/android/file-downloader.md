---
title: "文件下载 API – WebViewGold for Android 文档"
description: "让用户将图片、PDF 及其他文件从您的 Web 应用下载到 Android 设备。"
lang: "zh"
product: "WebViewGold for Android"
platform: "Android"
category: "API 与功能"
slug: "file-downloader"
canonical_url: "https://www.webviewgold.com/zh/docs/android/file-downloader/"
keywords:
  - "文件下载 API"
  - "WebViewGold for Android"
  - "将网站转换为应用"
  - "WebView 应用文档"
  - "Android WebView SDK"
  - "PWA 转应用"
  - "HTML 转应用"
  - "JavaScript 桥接"
last_updated: "2026-10-09"
---

# 文件下载 API – WebViewGold for Android

> **摘要：** 让用户将图片、PDF 及其他文件从您的 Web 应用下载到 Android 设备。

[文档](../README.md) › [WebViewGold for Android](README.md) › 文件下载 API

**平台：** Android · **类别：** API 与功能 · **在线版本：** [www.webviewgold.com/zh/docs/android/file-downloader/](https://www.webviewgold.com/zh/docs/android/file-downloader/)

---

WebViewGold 的 Download API 允许您在 WebView 应用中提供文档、图片和音频文件的下载。以下步骤介绍了如何启用和自定义下载器功能：

## 1. 下载图片

通过调用带有 savethisimage://?url= 前缀的链接，将图片保存到用户的相机胶卷中：

```html
<a href="savethisimage://?url=IMAGE URL HERE">Download Image</a>
```

## 2. 下载 PDF 文件

通过调用带有 .pdf 后缀的链接来保存 PDF 文件：

```html
<a href="https://www.example.org/file.pdf">Download PDF</a>
```

## 3. 下载音乐文件

只需调用带有 .mp3、.mp4 或 .wav 后缀的链接即可保存音乐文件：

```html
<a href="https://www.example.org/file.mp3">Download MP3</a>
<a href="https://www.example.org/file.mp4">Download MP4</a>
<a href="https://www.example.org/file.wav">Download WAV</a>
```

## 4. 自定义支持的文件类型

要向下载器添加其他文件格式，请将它们插入到 **Config.java** 中的 `downloadableExtension` 列表内。

## 5. 启用自动文件下载

可以考虑在 **Config.java** 中设置 `AUTO_DOWNLOAD_FILES` 选项，以便对带有 Content-Disposition HTTP 标头标记的文件启用自动下载，而不受 `downloadableExtension` 列表的限制。这可确保文件根据服务器配置自动下载。

---

## 继续阅读

- ← 上一页： [Facebook 广告 API](facebook-ads.md)
- 下一页 →： [原生视频（PiP）API](native-video.md)
- 其他平台上的相同功能： [iOS – 文件下载 API](../ios/file-downloader.md)
- 语言： [🇺🇸 English](../../android/file-downloader.md) · [🇩🇪 Deutsch](../../de/android/file-downloader.md) · [🇫🇷 Français](../../fr/android/file-downloader.md) · [🇪🇸 Español](../../es/android/file-downloader.md) · **🇨🇳 中文**

> [!TIP]
> **太忙了？我们替您搭建应用。** 我们的团队为您配置、构建并提交 WebViewGold 应用——全程代劳、交付迅速、德国制造。 [让我们搭建应用 →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_android_doc_online)
>
> **在浏览器中构建：** 无需 Mac、无需 IDE：**WebViewGold Cloud Builder** 在线为您配置、构建并上传应用。 [了解 Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=android_docs)
