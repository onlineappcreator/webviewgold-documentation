---
title: "用户跟踪决定 API – WebViewGold for iOS 文档"
description: "遵循 App Tracking Transparency：在您的 WebViewGold iOS 应用中读取用户的跟踪决定并作出响应。"
lang: "zh"
product: "WebViewGold for iOS"
platform: "iOS"
category: "API 与功能"
slug: "user-tracking"
canonical_url: "https://www.webviewgold.com/zh/docs/iOS/user-tracking/"
keywords:
  - "用户跟踪决定 API"
  - "WebViewGold for iOS"
  - "将网站转换为应用"
  - "WebView 应用文档"
  - "iOS WebView SDK"
  - "PWA 转应用"
  - "HTML 转应用"
  - "JavaScript 桥接"
last_updated: "2026-10-09"
---

# 用户跟踪决定 API – WebViewGold for iOS

> **摘要：** 遵循 App Tracking Transparency：在您的 WebViewGold iOS 应用中读取用户的跟踪决定并作出响应。

[文档](../README.md) › [WebViewGold for iOS](README.md) › 用户跟踪决定 API

**平台：** iOS · **类别：** API 与功能 · **在线版本：** [www.webviewgold.com/zh/docs/iOS/user-tracking/](https://www.webviewgold.com/zh/docs/iOS/user-tracking/)

---

在 iOS 中，应用必须依据 Apple 的 AppTrackingTransparency 框架请求追踪用户数据的权限。WebViewGold 可让您获取用户在安装应用时所做的选择，以便您在 Web 应用中据此作出相应处理。JavaScript 变量 **trackingDisabled** 可由 WebViewGold 设置为 true，表示追踪已被阻止；若未被阻止则为 false。在您的 Web 应用中，可先获取该 JavaScript 变量再通过弹窗查看其状态：

```html
<a href="user-disable-tracking://">Set JavaScript variable</a>
<a href="#" onClick="alert(trackingDisabled);">Show tracking decision</a>
```

---

## 继续阅读

- ← 上一页： [重置应用 API](reset-app.md)
- 下一页 →： [加载标志 API](loading-sign.md)
- 语言： [🇺🇸 English](../../ios/user-tracking.md) · [🇩🇪 Deutsch](../../de/ios/user-tracking.md) · [🇫🇷 Français](../../fr/ios/user-tracking.md) · [🇪🇸 Español](../../es/ios/user-tracking.md) · **🇨🇳 中文**

> [!TIP]
> **太忙了？我们替您搭建应用。** 我们的团队为您配置、构建并提交 WebViewGold 应用——全程代劳、交付迅速、德国制造。 [让我们搭建应用 →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **在浏览器中构建：** 无需 Mac、无需 IDE：**WebViewGold Cloud Builder** 在线为您配置、构建并上传应用。 [了解 Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
