---
title: "应用分享对话框 API – WebViewGold for iOS 文档"
description: "从您的网页应用触发原生 iOS 分享面板，让用户分享您的应用或任意 URL。"
lang: "zh"
product: "WebViewGold for iOS"
platform: "iOS"
category: "API 与功能"
slug: "app-sharing-dialog"
canonical_url: "https://www.webviewgold.com/zh/docs/iOS/app-sharing-dialog/"
keywords:
  - "应用分享对话框 API"
  - "WebViewGold for iOS"
  - "将网站转换为应用"
  - "WebView 应用文档"
  - "iOS WebView SDK"
  - "PWA 转应用"
  - "HTML 转应用"
  - "JavaScript 桥接"
last_updated: "2026-10-09"
---

# 应用分享对话框 API – WebViewGold for iOS

> **摘要：** 从您的网页应用触发原生 iOS 分享面板，让用户分享您的应用或任意 URL。

[文档](../README.md) › [WebViewGold for iOS](README.md) › 应用分享对话框 API

**平台：** iOS · **类别：** API 与功能 · **在线版本：** [www.webviewgold.com/zh/docs/iOS/app-sharing-dialog/](https://www.webviewgold.com/zh/docs/iOS/app-sharing-dialog/)

---

WebViewGold 中的应用分享对话框 API 让您的用户能够将应用中的内容（例如下载链接或自定义消息）通过他们偏好的应用（如 WhatsApp、短信、电子邮件）分享给亲朋好友。这是一种提升应用曝光度、扩大用户群体的有效方式。

## 如何在基于 WebView 的 iOS 应用中使用应用分享对话框

您可以使用 `shareapp://` URL 方案触发原生分享对话框，并可自定义消息和 URL 参数。

以下是实现此功能的几种不同示例：

```html
<a href="shareapp://message?=Check out this cool thing!&url=https://www.webviewgold.com">Share (message, link)</a>

<a href="shareapp://message?=&url=https://www.webviewgold.com">Share (no message, link)</a>

<a href="shareapp://message?=Check out this cool thing!">Share (message, no link)</a>
```

![应用分享对话框示例](../../assets/ios/img/sharedialog.webp)\
![应用分享消息示例](../../assets/ios/img/sharemessage.webp)

---

## 继续阅读

- ← 上一页： [深度链接 API](deep-linking.md)
- 下一页 →： [应用内评分对话框 API](in-app-rating.md)
- 其他平台上的相同功能： [Android – 应用分享对话框 API](../android/app-sharing-dialog.md)
- 语言： [🇺🇸 English](../../ios/app-sharing-dialog.md) · [🇩🇪 Deutsch](../../de/ios/app-sharing-dialog.md) · [🇫🇷 Français](../../fr/ios/app-sharing-dialog.md) · [🇪🇸 Español](../../es/ios/app-sharing-dialog.md) · **🇨🇳 中文**

> [!TIP]
> **太忙了？我们替您搭建应用。** 我们的团队为您配置、构建并提交 WebViewGold 应用——全程代劳、交付迅速、德国制造。 [让我们搭建应用 →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **在浏览器中构建：** 无需 Mac、无需 IDE：**WebViewGold Cloud Builder** 在线为您配置、构建并上传应用。 [了解 Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
