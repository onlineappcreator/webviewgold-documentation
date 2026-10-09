---
title: "应用分享对话框 API – WebViewGold for Android 文档"
description: "从您的 Web 应用触发原生 Android 分享对话框，让用户分享您的应用或任意 URL。"
lang: "zh"
product: "WebViewGold for Android"
platform: "Android"
category: "API 与功能"
slug: "app-sharing-dialog"
canonical_url: "https://www.webviewgold.com/zh/docs/android/app-sharing-dialog/"
keywords:
  - "应用分享对话框 API"
  - "WebViewGold for Android"
  - "将网站转换为应用"
  - "WebView 应用文档"
  - "Android WebView SDK"
  - "PWA 转应用"
  - "HTML 转应用"
  - "JavaScript 桥接"
last_updated: "2026-10-09"
---

# 应用分享对话框 API – WebViewGold for Android

> **摘要：** 从您的 Web 应用触发原生 Android 分享对话框，让用户分享您的应用或任意 URL。

[文档](../README.md) › [WebViewGold for Android](README.md) › 应用分享对话框 API

**平台：** Android · **类别：** API 与功能 · **在线版本：** [www.webviewgold.com/zh/docs/android/app-sharing-dialog/](https://www.webviewgold.com/zh/docs/android/app-sharing-dialog/)

---

WebViewGold 中的 App Sharing Dialog API 使您的用户能够将应用中的内容（例如下载链接或自定义消息）通过他们偏好的应用（例如 WhatsApp、SMS、Email）分享给亲朋好友。这是提升应用曝光度并扩大用户群体的有效方式。

## 如何在基于 WebView 的 Android 应用中使用应用分享对话框

您可以使用 `shareapp://` URL Scheme，并配合可自定义的消息和 URL 参数，来触发原生分享对话框。

以下是实现此功能的几种不同方式的示例：

```html
<a href="shareapp://message?=Check out this cool thing!&url=https://www.webviewgold.com">Share (message, link)</a>

<a href="shareapp://message?=&url=https://www.webviewgold.com">Share (no message, link)</a>

<a href="shareapp://message?=Check out this cool thing!">Share (message, no link)</a>
```

![应用分享对话框示例](../../assets/android/img/appshare.webp)

---

## 继续阅读

- ← 上一页： [ShareIntent API](share-intent.md)
- 下一页 →： [应用内评分 API](in-app-rating.md)
- 其他平台上的相同功能： [iOS – 应用分享对话框 API](../ios/app-sharing-dialog.md)
- 语言： [🇺🇸 English](../../android/app-sharing-dialog.md) · [🇩🇪 Deutsch](../../de/android/app-sharing-dialog.md) · [🇫🇷 Français](../../fr/android/app-sharing-dialog.md) · [🇪🇸 Español](../../es/android/app-sharing-dialog.md) · **🇨🇳 中文**

> [!TIP]
> **太忙了？我们替您搭建应用。** 我们的团队为您配置、构建并提交 WebViewGold 应用——全程代劳、交付迅速、德国制造。 [让我们搭建应用 →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_android_doc_online)
>
> **在浏览器中构建：** 无需 Mac、无需 IDE：**WebViewGold Cloud Builder** 在线为您配置、构建并上传应用。 [了解 Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=android_docs)
