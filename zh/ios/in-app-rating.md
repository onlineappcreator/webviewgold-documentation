---
title: "应用内评分对话框 API – WebViewGold for iOS 文档"
description: "在最佳时机请求用户进行 App Store 评分——从您的 Web 应用触发 iOS 原生评分对话框。"
lang: "zh"
product: "WebViewGold for iOS"
platform: "iOS"
category: "API 与功能"
slug: "in-app-rating"
canonical_url: "https://www.webviewgold.com/zh/docs/iOS/in-app-rating/"
keywords:
  - "应用内评分对话框 API"
  - "WebViewGold for iOS"
  - "将网站转换为应用"
  - "WebView 应用文档"
  - "iOS WebView SDK"
  - "PWA 转应用"
  - "HTML 转应用"
  - "JavaScript 桥接"
last_updated: "2026-10-09"
---

# 应用内评分对话框 API – WebViewGold for iOS

> **摘要：** 在最佳时机请求用户进行 App Store 评分——从您的 Web 应用触发 iOS 原生评分对话框。

[文档](../README.md) › [WebViewGold for iOS](README.md) › 应用内评分对话框 API

**平台：** iOS · **类别：** API 与功能 · **在线版本：** [www.webviewgold.com/zh/docs/iOS/in-app-rating/](https://www.webviewgold.com/zh/docs/iOS/in-app-rating/)

---

App Store 上的好评是应用增长最有力的驱动因素之一。WebViewGold 的**应用内评分对话框 API** 让您可以在最合适的时机请求用户评分——例如在成功购买后，或用户在您的 Web 应用中完成某项任务之后。

## 方式 1：原生 iOS 评分对话框（默认）

通过 HTML 链接或 JavaScript 调用以下 URL，以显示原生的 **SKStoreReviewController** 评分对话框：

```html
<a href="rateapp://">喜欢这个应用吗？给我们评分吧！</a>
```

```javascript
window.location.href = "rateapp://";
```

**注意：**Apple 限制了原生评分对话框的显示频率（每位用户每年约三次），因此它可能不会在每次调用时都出现——这是有意为之，在开发期间也同样适用。

## 方式 2：自定义评分对话框

如果您希望对话框始终显示，并将用户引导至您的 App Store 页面，请在 **Config.swift** 中进行配置：

- `showcustomrateappdialog` — 设置为 `true`，在触发 `rateapp://` 时显示自定义评分对话框，而不是尝试原生评分调用。
- `ratemyappurl` — 设置您应用的 App Store URL，例如 `https://apps.apple.com/app/idXXXXXXXXX?action=write-review`。

## 典型使用场景

- 在积极互动（完成订单、升级、预订成功）之后立即请求评价。
- 先在您的网站上展示自己的“您喜欢这个应用吗？”流程，只将满意的用户引导至 `rateapp://`。

---

## 继续阅读

- ← 上一页： [应用分享对话框 API](app-sharing-dialog.md)
- 下一页 →： [应用内购买 API](in-app-purchases.md)
- 其他平台上的相同功能： [Android – 应用内评分 API](../android/in-app-rating.md)
- 语言： [🇺🇸 English](../../ios/in-app-rating.md) · [🇩🇪 Deutsch](../../de/ios/in-app-rating.md) · [🇫🇷 Français](../../fr/ios/in-app-rating.md) · [🇪🇸 Español](../../es/ios/in-app-rating.md) · **🇨🇳 中文**

> [!TIP]
> **太忙了？我们替您搭建应用。** 我们的团队为您配置、构建并提交 WebViewGold 应用——全程代劳、交付迅速、德国制造。 [让我们搭建应用 →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **在浏览器中构建：** 无需 Mac、无需 IDE：**WebViewGold Cloud Builder** 在线为您配置、构建并上传应用。 [了解 Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
