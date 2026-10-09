---
title: "HTML5 地理定位 API – WebViewGold for iOS 文档"
description: "在您的 iOS WebView 应用中启用 HTML5 地理定位，并以正确的方式请求精确位置权限。"
lang: "zh"
product: "WebViewGold for iOS"
platform: "iOS"
category: "API 与功能"
slug: "geolocation"
canonical_url: "https://www.webviewgold.com/zh/docs/iOS/geolocation/"
keywords:
  - "地理定位 API"
  - "WebViewGold for iOS"
  - "将网站转换为应用"
  - "WebView 应用文档"
  - "iOS WebView SDK"
  - "PWA 转应用"
  - "HTML 转应用"
  - "JavaScript 桥接"
last_updated: "2026-10-09"
---

# HTML5 地理定位 API – WebViewGold for iOS

> **摘要：** 在您的 iOS WebView 应用中启用 HTML5 地理定位，并以正确的方式请求精确位置权限。

[文档](../README.md) › [WebViewGold for iOS](README.md) › 地理定位 API

**平台：** iOS · **类别：** API 与功能 · **在线版本：** [www.webviewgold.com/zh/docs/iOS/geolocation/](https://www.webviewgold.com/zh/docs/iOS/geolocation/)

---

HTML5 地理位置 API 允许用户与您的应用共享其位置，从而增强基于位置的内容等功能。在 WebViewGold 中，地理位置 API 一旦集成到您的网页内容中即默认支持。以下是如何将地理位置跟踪实现到基于 WebView 的 iOS 应用中的方法：

## 设置 HTML5 地理位置

关于基础地理位置的设置，请参阅 [Mozilla 的地理位置指南](https://developer.mozilla.org/en-US/docs/Web/API/Geolocation_API)，了解如何在您的网站或 Web 应用中实现此功能。

如需演示，请访问此 [W3Schools 地理位置示例](https://www.w3schools.com/html/html5_geolocation.asp)。

自 iOS 10 起，地理位置仅在 HTTPS 网站上可用，因此在使用位置请求时，请确保您的 Web 应用 URL 以 `https://` 开头，而不是 `http://`。

## 后台位置访问

默认情况下，位置请求仅在应用处于前台时有效。如果您的 Web 应用需要在应用处于后台时继续接收位置更新（例如用于轨迹跟踪或地理围栏场景），请在 **Config.swift** 中启用后台位置选项：

```swift
static let backgroundlocation = true
```

- 在 Xcode 项目设置中，为 WebViewGold target 添加 **Background Modes** 能力，并勾选 **Location updates**。
- 根据您的 Web 应用，可能还需要启用 **Background Processing**。在这种情况下，请在 **Info.plist** 中添加一个键为 `Permitted background task scheduler identifiers` 的数组，并在其中包含一个带有您应用 Bundle ID 的字符串（例如 `com.yourcompany.yourapp`）。
- 请注意，App Store 审核要求对后台位置访问给出明确理由——请在审核备注中说明其对用户的益处。

---

## 继续阅读

- ← 上一页： [修改安全区域](safe-area.md)
- 下一页 →： [推送通知 API](push-notifications.md)
- 其他平台上的相同功能： [Android – 地理定位 API](../android/geolocation.md)
- 语言： [🇺🇸 English](../../ios/geolocation.md) · [🇩🇪 Deutsch](../../de/ios/geolocation.md) · [🇫🇷 Français](../../fr/ios/geolocation.md) · [🇪🇸 Español](../../es/ios/geolocation.md) · **🇨🇳 中文**

> [!TIP]
> **太忙了？我们替您搭建应用。** 我们的团队为您配置、构建并提交 WebViewGold 应用——全程代劳、交付迅速、德国制造。 [让我们搭建应用 →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **在浏览器中构建：** 无需 Mac、无需 IDE：**WebViewGold Cloud Builder** 在线为您配置、构建并上传应用。 [了解 Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
