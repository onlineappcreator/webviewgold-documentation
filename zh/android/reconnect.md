---
title: "Reconnect API – WebViewGold for Android 文档"
description: "Reload the last online URL from your offline / fallback HTML page — the perfect \"Try again\" button for your custom offline screen."
lang: "zh"
product: "WebViewGold for Android"
platform: "Android"
category: "API 与功能"
slug: "reconnect"
canonical_url: "https://www.webviewgold.com/zh/docs/android/reconnect/"
keywords:
  - "Reconnect API"
  - "WebViewGold for Android"
  - "将网站转换为应用"
  - "WebView 应用文档"
  - "Android WebView SDK"
  - "PWA 转应用"
  - "HTML 转应用"
  - "JavaScript 桥接"
last_updated: "2026-10-09"
---

# Reconnect API – WebViewGold for Android

> **摘要：** Reload the last online URL from your offline / fallback HTML page — the perfect "Try again" button for your custom offline screen.

[文档](../README.md) › [WebViewGold for Android](README.md) › Reconnect API

**平台：** Android · **类别：** API 与功能 · **在线版本：** [www.webviewgold.com/zh/docs/android/reconnect/](https://www.webviewgold.com/zh/docs/android/reconnect/)

---

**Reconnect API** 用于重新加载用户在应用回退到离线 HTML 页面之前所访问的最后一个在线 URL。它被设计为您自定义的离线/回退屏幕上的"重试"按钮。

## 使用方法

将触发器添加到您的离线页面（通常是 `local-html/index.html`）：

```html
<button onclick="window.location.href='reconnect://'">Try to reconnect</button>
```

## 工作原理

应用会记住最后一个成功加载的非辅助 URL。当用户点击 `reconnect://` 时，WebView 会导航回该 URL。如果连接仍然中断，则会再次显示您的回退页面。

## 相关配置

- **Config.java** 中的 `FALLBACK_USE_LOCAL_HTML_FOLDER_IF_OFFLINE` 必须为 `true`，并且您需要一个 `local-html/index.html` 回退页面，此功能才有意义。

---

## 继续阅读

- ← 上一页： [Open App Settings API](open-app-settings.md)
- 下一页 →： [Read/Write Value API](read-write-value.md)
- 其他平台上的相同功能： [iOS – 重新连接 API](../ios/reconnect.md)
- 语言： [🇺🇸 English](../../android/reconnect.md) · [🇩🇪 Deutsch](../../de/android/reconnect.md) · [🇫🇷 Français](../../fr/android/reconnect.md) · [🇪🇸 Español](../../es/android/reconnect.md) · **🇨🇳 中文**

> [!TIP]
> **太忙了？我们替您搭建应用。** 我们的团队为您配置、构建并提交 WebViewGold 应用——全程代劳、交付迅速、德国制造。 [让我们搭建应用 →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_android_doc_online)
>
> **在浏览器中构建：** 无需 Mac、无需 IDE：**WebViewGold Cloud Builder** 在线为您配置、构建并上传应用。 [了解 Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=android_docs)
