---
title: "重置应用 API – WebViewGold for Android 文档"
description: "通过单个链接或 JavaScript 调用即可重置 Android WebView 应用的缓存、Cookie 和本地存储。"
lang: "zh"
product: "WebViewGold for Android"
platform: "Android"
category: "API 与功能"
slug: "reset-app"
canonical_url: "https://www.webviewgold.com/zh/docs/android/reset-app/"
keywords:
  - "重置应用 API"
  - "WebViewGold for Android"
  - "将网站转换为应用"
  - "WebView 应用文档"
  - "Android WebView SDK"
  - "PWA 转应用"
  - "HTML 转应用"
  - "JavaScript 桥接"
last_updated: "2026-10-09"
---

# 重置应用 API – WebViewGold for Android

> **摘要：** 通过单个链接或 JavaScript 调用即可重置 Android WebView 应用的缓存、Cookie 和本地存储。

[文档](../README.md) › [WebViewGold for Android](README.md) › 重置应用 API

**平台：** Android · **类别：** API 与功能 · **在线版本：** [www.webviewgold.com/zh/docs/android/reset-app/](https://www.webviewgold.com/zh/docs/android/reset-app/)

---

在某些情况下，将应用重置为其初始设置（通过清除 cookie 和缓存）可能是恢复最佳性能所必需的。**Reset App API** 提供了一种简单直接的方式来发起此重置操作。

## 用法

要重置应用数据，只需在应用中使用以下链接：

```html
<a href="reset://">Reset App Link</a>
```

此链接将执行以下操作：

- 清除所有 cookie
- 清除缓存数据

## 测试重置功能

要测试此功能，请将以下演示 URL 添加到您的 WebViewGold 应用中：<https://www.onlineappcreator.com/reset_test.html>

**注意：**请谨慎使用重置功能，因为它会清除与 cookie 和缓存相关的用户数据，这可能会影响已保存的设置或会话数据，包括使用户从当前活动会话中退出登录。

---

## 继续阅读

- ← 上一页： [原生视频（PiP）API](native-video.md)
- 下一页 →： [加载指示 API](loading-sign.md)
- 其他平台上的相同功能： [iOS – 重置应用 API](../ios/reset-app.md)
- 语言： [🇺🇸 English](../../android/reset-app.md) · [🇩🇪 Deutsch](../../de/android/reset-app.md) · [🇫🇷 Français](../../fr/android/reset-app.md) · [🇪🇸 Español](../../es/android/reset-app.md) · **🇨🇳 中文**

> [!TIP]
> **太忙了？我们替您搭建应用。** 我们的团队为您配置、构建并提交 WebViewGold 应用——全程代劳、交付迅速、德国制造。 [让我们搭建应用 →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_android_doc_online)
>
> **在浏览器中构建：** 无需 Mac、无需 IDE：**WebViewGold Cloud Builder** 在线为您配置、构建并上传应用。 [了解 Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=android_docs)
