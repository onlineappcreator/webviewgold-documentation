---
title: "文件下载 API – WebViewGold for iOS 文档"
description: "让用户将图片、PDF 和其他文件从您的网页应用直接下载到 iPhone 或 iPad 上。"
lang: "zh"
product: "WebViewGold for iOS"
platform: "iOS"
category: "API 与功能"
slug: "file-downloader"
canonical_url: "https://www.webviewgold.com/zh/docs/iOS/file-downloader/"
keywords:
  - "文件下载 API"
  - "WebViewGold for iOS"
  - "将网站转换为应用"
  - "WebView 应用文档"
  - "iOS WebView SDK"
  - "PWA 转应用"
  - "HTML 转应用"
  - "JavaScript 桥接"
last_updated: "2026-10-09"
---

# 文件下载 API – WebViewGold for iOS

> **摘要：** 让用户将图片、PDF 和其他文件从您的网页应用直接下载到 iPhone 或 iPad 上。

[文档](../README.md) › [WebViewGold for iOS](README.md) › 文件下载 API

**平台：** iOS · **类别：** API 与功能 · **在线版本：** [www.webviewgold.com/zh/docs/iOS/file-downloader/](https://www.webviewgold.com/zh/docs/iOS/file-downloader/)

---

WebViewGold 的下载 API 允许您在 WebView 应用中提供文档、图片和音频文件下载。以下步骤介绍了如何启用和自定义下载器功能：

## 1. 下载图片

通过调用带有 savethisimage://?url= 前缀的链接，将图片保存到用户的相册：

```html
<a href="savethisimage://?url=IMAGE URL HERE">Download Image</a>
```

## 2. 下载文件

通过调用带有相应后缀（例如 .mp3）的链接来保存文件：

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

## 3. 自定义支持的文件类型

您可以添加更多应触发文件下载器功能的文件类型（例如 .epub、.zip 等）。这可以通过 **Config.swift** 文件中的列表变量 `extentionARY` 完成。

## 4. 启用自动文件下载

可考虑在 **Config.swift** 中设置 `autodownloader` 选项，以启用带 Content-Disposition HTTP 标头文件的自动下载，独立于 `extentionARY` 列表。这样可确保文件根据服务器配置自动下载。

[![观看视频: 文件下载 API](https://img.youtube.com/vi/V0LnwnzJx6I/hqdefault.jpg)](https://www.youtube.com/watch?v=V0LnwnzJx6I)

---

## 继续阅读

- ← 上一页： [原生视频 API](native-video.md)
- 下一页 →： [打印机 API](printer.md)
- 其他平台上的相同功能： [Android – 文件下载 API](../android/file-downloader.md)
- 语言： [🇺🇸 English](../../ios/file-downloader.md) · [🇩🇪 Deutsch](../../de/ios/file-downloader.md) · [🇫🇷 Français](../../fr/ios/file-downloader.md) · [🇪🇸 Español](../../es/ios/file-downloader.md) · **🇨🇳 中文**

> [!TIP]
> **太忙了？我们替您搭建应用。** 我们的团队为您配置、构建并提交 WebViewGold 应用——全程代劳、交付迅速、德国制造。 [让我们搭建应用 →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **在浏览器中构建：** 无需 Mac、无需 IDE：**WebViewGold Cloud Builder** 在线为您配置、构建并上传应用。 [了解 Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
