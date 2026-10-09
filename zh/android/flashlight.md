---
title: "手电筒 API – WebViewGold for Android 文档"
description: "在 WebViewGold for Android 中，通过简单的 JavaScript 链接从您的 Web 应用控制设备手电筒。"
lang: "zh"
product: "WebViewGold for Android"
platform: "Android"
category: "API 与功能"
slug: "flashlight"
canonical_url: "https://www.webviewgold.com/zh/docs/android/flashlight/"
keywords:
  - "手电筒 API"
  - "WebViewGold for Android"
  - "将网站转换为应用"
  - "WebView 应用文档"
  - "Android WebView SDK"
  - "PWA 转应用"
  - "HTML 转应用"
  - "JavaScript 桥接"
last_updated: "2026-10-09"
---

# 手电筒 API – WebViewGold for Android

> **摘要：** 在 WebViewGold for Android 中，通过简单的 JavaScript 链接从您的 Web 应用控制设备手电筒。

[文档](../README.md) › [WebViewGold for Android](README.md) › 手电筒 API

**平台：** Android · **类别：** API 与功能 · **在线版本：** [www.webviewgold.com/zh/docs/android/flashlight/](https://www.webviewgold.com/zh/docs/android/flashlight/)

---

WebViewGold 的 Flashlight API 允许您的网站控制设备的手电筒（闪光灯）。此功能在以下场景中很有用：

- 构建需要手电筒开关的实用工具类应用
- 通过游戏化提升应用使用过程中的用户体验
- 提供额外的无障碍功能

## 如何使用

您可以直接在 HTML 内容中使用以下链接来触发手电筒的开启或关闭：

```html
<a href="enableflashlight://">Turn On Flashlight</a>
<a href="disableflashlight://">Turn Off Flashlight</a>
```

**注意：**请确保您的应用在 AndroidManifest.xml 中拥有所需的摄像头权限，因为手电筒功能与设备的摄像头硬件相关联。

---

## 继续阅读

- ← 上一页： [UUID API](uuid.md)
- 下一页 →： [App Links / 深度链接](app-links.md)
- 其他平台上的相同功能： [iOS – 手电筒 API](../ios/flashlight.md)
- 语言： [🇺🇸 English](../../android/flashlight.md) · [🇩🇪 Deutsch](../../de/android/flashlight.md) · [🇫🇷 Français](../../fr/android/flashlight.md) · [🇪🇸 Español](../../es/android/flashlight.md) · **🇨🇳 中文**

> [!TIP]
> **太忙了？我们替您搭建应用。** 我们的团队为您配置、构建并提交 WebViewGold 应用——全程代劳、交付迅速、德国制造。 [让我们搭建应用 →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_android_doc_online)
>
> **在浏览器中构建：** 无需 Mac、无需 IDE：**WebViewGold Cloud Builder** 在线为您配置、构建并上传应用。 [了解 Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=android_docs)
