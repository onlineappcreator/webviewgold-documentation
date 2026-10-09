---
title: "HTML5 地理定位 API – WebViewGold for Android 文档"
description: "在您的 Android WebView 应用中启用 HTML5 地理定位，并正确请求位置权限。"
lang: "zh"
product: "WebViewGold for Android"
platform: "Android"
category: "API 与功能"
slug: "geolocation"
canonical_url: "https://www.webviewgold.com/zh/docs/android/geolocation/"
keywords:
  - "地理定位 API"
  - "WebViewGold for Android"
  - "将网站转换为应用"
  - "WebView 应用文档"
  - "Android WebView SDK"
  - "PWA 转应用"
  - "HTML 转应用"
  - "JavaScript 桥接"
last_updated: "2026-10-09"
---

# HTML5 地理定位 API – WebViewGold for Android

> **摘要：** 在您的 Android WebView 应用中启用 HTML5 地理定位，并正确请求位置权限。

[文档](../README.md) › [WebViewGold for Android](README.md) › 地理定位 API

**平台：** Android · **类别：** API 与功能 · **在线版本：** [www.webviewgold.com/zh/docs/android/geolocation/](https://www.webviewgold.com/zh/docs/android/geolocation/)

---

HTML5 Geolocation API 使用户能够与您的应用共享其位置，从而增强诸如基于位置的内容之类的功能。在 WebViewGold 中，只要将 Geolocation API 集成到您的网页内容中，即可默认支持。以下是如何在基于 WebView 的 Android 应用中实现地理位置跟踪：

## 设置 HTML5 Geolocation

关于基本的 Geolocation 设置，请参阅 [Mozilla 的 Geolocation 指南](https://developer.mozilla.org/en-US/docs/Web/API/Geolocation_API)，了解如何将此功能集成到您的网站或 Web 应用中的详细信息。

如需演示，请访问此 [W3Schools Geolocation 演示](https://www.w3schools.com/html/html5_geolocation.asp)。

## 启用后台位置跟踪（仅限 Android）

要在您基于 WebView 的 Android 应用中启用后台位置跟踪，请按照以下步骤操作：

1. 在 **Config.java** 中设置权限：
   - 如果需要后台位置跟踪，将 `requireBackgroundLocation` 设置为 `true`。
   - 确保 `requireLocation` 也设置为 `true`，以启用任何位置服务。
2. 在 **AndroidManifest.xml** 中调整权限：
   - 取消 `android.permission.FOREGROUND_SERVICE_LOCATION` 和 `GPSService` 的权限块的注释。
   - 在文件中搜索这些术语，以确保设置了正确的权限。

## 通过 URL 方案切换后台位置跟踪

使用以下 URL 方案可在您基于 WebView 的 Android 应用中开启或关闭后台位置跟踪：

要开启后台位置跟踪，请将用户重定向到以下 URL：

```html
<script>window.location.href = "backgroundlocationon://";  </script>
```

要关闭后台位置跟踪，请将用户重定向到以下 URL：

```html
<script>window.location.href = "backgroundlocationoff://";  </script>
```

**注意：** 这些 URL 方案专用于 WebViewGold for Android，可能无法在标准 Web 浏览器中使用。为确保这些重定向仅对 Android 应用用户生效，请考虑检测 User-Agent。

---

## 继续阅读

- ← 上一页： [Multi API Call](multi-api-call.md)
- 下一页 →： [推送通知 API](push-notifications.md)
- 其他平台上的相同功能： [iOS – 地理定位 API](../ios/geolocation.md)
- 语言： [🇺🇸 English](../../android/geolocation.md) · [🇩🇪 Deutsch](../../de/android/geolocation.md) · [🇫🇷 Français](../../fr/android/geolocation.md) · [🇪🇸 Español](../../es/android/geolocation.md) · **🇨🇳 中文**

> [!TIP]
> **太忙了？我们替您搭建应用。** 我们的团队为您配置、构建并提交 WebViewGold 应用——全程代劳、交付迅速、德国制造。 [让我们搭建应用 →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_android_doc_online)
>
> **在浏览器中构建：** 无需 Mac、无需 IDE：**WebViewGold Cloud Builder** 在线为您配置、构建并上传应用。 [了解 Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=android_docs)
