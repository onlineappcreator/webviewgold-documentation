---
title: "读写值 API – WebViewGold for iOS 文档"
description: "在设备上持久化存储字符串值，并将其读回到您 Web 应用的 JavaScript 中。"
lang: "zh"
product: "WebViewGold for iOS"
platform: "iOS"
category: "API 与功能"
slug: "read-write-value"
canonical_url: "https://www.webviewgold.com/zh/docs/iOS/read-write-value/"
keywords:
  - "读写值 API"
  - "WebViewGold for iOS"
  - "将网站转换为应用"
  - "WebView 应用文档"
  - "iOS WebView SDK"
  - "PWA 转应用"
  - "HTML 转应用"
  - "JavaScript 桥接"
last_updated: "2026-10-09"
---

# 读写值 API – WebViewGold for iOS

> **摘要：** 在设备上持久化存储字符串值，并将其读回到您 Web 应用的 JavaScript 中。

[文档](../README.md) › [WebViewGold for iOS](README.md) › 读写值 API

**平台：** iOS · **类别：** API 与功能 · **在线版本：** [www.webviewgold.com/zh/docs/iOS/read-write-value/](https://www.webviewgold.com/zh/docs/iOS/read-write-value/)

---

**读写值 API** 将任意字符串持久化存储在设备上（应用的私有存储中），并可将其读回到您的 JavaScript 中。只要应用未被卸载，这些值就能在应用重启和缓存清理后保留。

## 写入值

`writevalue://` 之后的所有内容都会作为一个字符串原样存储。您可以自行设计格式（query-string、JSON、CSV——只要适合您的 Web 应用即可）：

```html
<a href="writevalue://darkmode=on;user=42">保存</a>
```

## 读取值

当触发 `readvalue://` 时，应用会将存储的字符串作为 `window.storedValues` 注入回 WebView，供您的 JavaScript 读取：

```html
<a href="readvalue://" onclick="setTimeout(showSettings, 200)">加载</a>
<script>
  function showSettings() {
    console.log(window.storedValues || "尚无设置");
  }
</script>
```

## 典型使用场景

- 离线记住用户的主题、语言或引导状态。
- 在无法依赖 Cookie 时缓存会话令牌。
- 在不进行后端往返的情况下持久化少量本地偏好设置。

**注意：**值按应用安装和设备存储——**不会**跨设备同步。请保持值的体积较小；此 API 用于存储设置，而非大数据块。

---

## 继续阅读

- ← 上一页： [剪贴板 API](clipboard.md)
- 下一页 →： [打开应用设置 API](open-app-settings.md)
- 其他平台上的相同功能： [Android – Read/Write Value API](../android/read-write-value.md)
- 语言： [🇺🇸 English](../../ios/read-write-value.md) · [🇩🇪 Deutsch](../../de/ios/read-write-value.md) · [🇫🇷 Français](../../fr/ios/read-write-value.md) · [🇪🇸 Español](../../es/ios/read-write-value.md) · **🇨🇳 中文**

> [!TIP]
> **太忙了？我们替您搭建应用。** 我们的团队为您配置、构建并提交 WebViewGold 应用——全程代劳、交付迅速、德国制造。 [让我们搭建应用 →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **在浏览器中构建：** 无需 Mac、无需 IDE：**WebViewGold Cloud Builder** 在线为您配置、构建并上传应用。 [了解 Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
