---
title: "重置应用 API – WebViewGold for iOS 文档"
description: "通过单个链接或 JavaScript 调用重置您的 iOS WebView 应用的缓存、Cookie 和本地存储。"
lang: "zh"
product: "WebViewGold for iOS"
platform: "iOS"
category: "API 与功能"
slug: "reset-app"
canonical_url: "https://www.webviewgold.com/zh/docs/iOS/reset-app/"
keywords:
  - "重置应用 API"
  - "WebViewGold for iOS"
  - "将网站转换为应用"
  - "WebView 应用文档"
  - "iOS WebView SDK"
  - "PWA 转应用"
  - "HTML 转应用"
  - "JavaScript 桥接"
last_updated: "2026-10-09"
---

# 重置应用 API – WebViewGold for iOS

> **摘要：** 通过单个链接或 JavaScript 调用重置您的 iOS WebView 应用的缓存、Cookie 和本地存储。

[文档](../README.md) › [WebViewGold for iOS](README.md) › 重置应用 API

**平台：** iOS · **类别：** API 与功能 · **在线版本：** [www.webviewgold.com/zh/docs/iOS/reset-app/](https://www.webviewgold.com/zh/docs/iOS/reset-app/)

---

在某些情况下，可能需要通过清除 Cookie 和缓存将应用重置到初始设置，以恢复最佳性能。**Reset App API** 提供了一种简单的方法来触发此重置。

## 用法

如需重置应用数据，只需在应用中使用以下链接即可：

```html
<a href="reset://">Reset App Link</a>
```

此链接将会：

- 清除所有 Cookie
- 清除已缓存的数据

## 测试重置功能

如需测试此功能，请将以下演示 URL 添加到您的 WebViewGold 应用中：<https://www.onlineappcreator.com/reset_test.html>

**注意：**请谨慎使用重置功能，因为它会清除与 Cookie 和缓存相关的用户数据，可能影响已保存的设置或会话数据，包括将处于活动会话中的用户注销登录。

---

## 继续阅读

- ← 上一页： [手电筒 API](flashlight.md)
- 下一页 →： [用户跟踪决定 API](user-tracking.md)
- 其他平台上的相同功能： [Android – 重置应用 API](../android/reset-app.md)
- 语言： [🇺🇸 English](../../ios/reset-app.md) · [🇩🇪 Deutsch](../../de/ios/reset-app.md) · [🇫🇷 Français](../../fr/ios/reset-app.md) · [🇪🇸 Español](../../es/ios/reset-app.md) · **🇨🇳 中文**

> [!TIP]
> **太忙了？我们替您搭建应用。** 我们的团队为您配置、构建并提交 WebViewGold 应用——全程代劳、交付迅速、德国制造。 [让我们搭建应用 →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **在浏览器中构建：** 无需 Mac、无需 IDE：**WebViewGold Cloud Builder** 在线为您配置、构建并上传应用。 [了解 Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
