---
title: "手电筒 API – WebViewGold for iOS 文档"
description: "在 WebViewGold for iOS 中，通过简单的 JavaScript 链接从您的网页应用控制设备手电筒。"
lang: "zh"
product: "WebViewGold for iOS"
platform: "iOS"
category: "API 与功能"
slug: "flashlight"
canonical_url: "https://www.webviewgold.com/zh/docs/iOS/flashlight/"
keywords:
  - "手电筒 API"
  - "WebViewGold for iOS"
  - "将网站转换为应用"
  - "WebView 应用文档"
  - "iOS WebView SDK"
  - "PWA 转应用"
  - "HTML 转应用"
  - "JavaScript 桥接"
last_updated: "2026-10-09"
---

# 手电筒 API – WebViewGold for iOS

> **摘要：** 在 WebViewGold for iOS 中，通过简单的 JavaScript 链接从您的网页应用控制设备手电筒。

[文档](../README.md) › [WebViewGold for iOS](README.md) › 手电筒 API

**平台：** iOS · **类别：** API 与功能 · **在线版本：** [www.webviewgold.com/zh/docs/iOS/flashlight/](https://www.webviewgold.com/zh/docs/iOS/flashlight/)

---

WebViewGold 的手电筒 API 允许您的网站控制设备上的手电筒（闪光灯）。此功能适用的场景包括：

- 构建需要切换手电筒的工具类应用
- 通过游戏化元素提升应用使用中的用户体验
- 提供额外的辅助功能

## 使用方法

您可以在 HTML 内容中通过以下链接直接开启或关闭手电筒：

```html
<a href="enableflashlight://">Turn On Flashlight</a>
<a href="disableflashlight://">Turn Off Flashlight</a>
```

**注意：**请确保您的应用已在 Info.plist 中获得所需的相机权限，因为手电筒功能与设备的相机硬件相关联。

---

## 继续阅读

- ← 上一页： [UUID API](uuid.md)
- 下一页 →： [重置应用 API](reset-app.md)
- 其他平台上的相同功能： [Android – 手电筒 API](../android/flashlight.md)
- 语言： [🇺🇸 English](../../ios/flashlight.md) · [🇩🇪 Deutsch](../../de/ios/flashlight.md) · [🇫🇷 Français](../../fr/ios/flashlight.md) · [🇪🇸 Español](../../es/ios/flashlight.md) · **🇨🇳 中文**

> [!TIP]
> **太忙了？我们替您搭建应用。** 我们的团队为您配置、构建并提交 WebViewGold 应用——全程代劳、交付迅速、德国制造。 [让我们搭建应用 →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **在浏览器中构建：** 无需 Mac、无需 IDE：**WebViewGold Cloud Builder** 在线为您配置、构建并上传应用。 [了解 Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
