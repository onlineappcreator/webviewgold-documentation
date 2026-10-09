---
title: "打开应用设置 API – WebViewGold for iOS 文档"
description: "将用户直接引导至 iOS 设置应用中您的应用页面，以管理权限和通知。"
lang: "zh"
product: "WebViewGold for iOS"
platform: "iOS"
category: "API 与功能"
slug: "open-app-settings"
canonical_url: "https://www.webviewgold.com/zh/docs/iOS/open-app-settings/"
keywords:
  - "打开应用设置 API"
  - "WebViewGold for iOS"
  - "将网站转换为应用"
  - "WebView 应用文档"
  - "iOS WebView SDK"
  - "PWA 转应用"
  - "HTML 转应用"
  - "JavaScript 桥接"
last_updated: "2026-10-09"
---

# 打开应用设置 API – WebViewGold for iOS

> **摘要：** 将用户直接引导至 iOS 设置应用中您的应用页面，以管理权限和通知。

[文档](../README.md) › [WebViewGold for iOS](README.md) › 打开应用设置 API

**平台：** iOS · **类别：** API 与功能 · **在线版本：** [www.webviewgold.com/zh/docs/iOS/open-app-settings/](https://www.webviewgold.com/zh/docs/iOS/open-app-settings/)

---

WebViewGold 的**打开应用设置 API** 可将用户直接带到 iOS 原生**设置**应用中您的应用页面。用户可以在那里管理权限（相机、定位、通知…）、语言和其他应用设置——无需离开您的 Web 应用在 iOS 设置中翻找。

## 使用方法

通过 HTML 链接或 JavaScript 触发该页面：

```html
<a href="settingsapp://">打开应用设置</a>
```

```javascript
window.location.href = "settingsapp://";
```

## 典型使用场景

- 用户拒绝了某项权限（相机、麦克风、定位、通知）——将其直接引导至系统页面重新启用。
- 引导用户前往您应用的通知设置，例如与[推送通知 API](push-notifications.md) 的 `checkNativePushPermissions://` 调用结合使用。

**注意：**无参数。任何以 `settingsapp://` 开头的 URL 都会打开同一页面。

---

## 继续阅读

- ← 上一页： [读写值 API](read-write-value.md)
- 下一页 →： [Share Extension](share-extension.md)
- 其他平台上的相同功能： [Android – Open App Settings API](../android/open-app-settings.md)
- 语言： [🇺🇸 English](../../ios/open-app-settings.md) · [🇩🇪 Deutsch](../../de/ios/open-app-settings.md) · [🇫🇷 Français](../../fr/ios/open-app-settings.md) · [🇪🇸 Español](../../es/ios/open-app-settings.md) · **🇨🇳 中文**

> [!TIP]
> **太忙了？我们替您搭建应用。** 我们的团队为您配置、构建并提交 WebViewGold 应用——全程代劳、交付迅速、德国制造。 [让我们搭建应用 →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **在浏览器中构建：** 无需 Mac、无需 IDE：**WebViewGold Cloud Builder** 在线为您配置、构建并上传应用。 [了解 Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
