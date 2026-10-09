---
title: "屏幕捕获检测 – WebViewGold for iOS 文档"
description: "在您的 iOS 应用中检测截图和屏幕录制，并从您的网页应用作出响应。"
lang: "zh"
product: "WebViewGold for iOS"
platform: "iOS"
category: "扩展与插件"
slug: "screen-capture"
canonical_url: "https://www.webviewgold.com/zh/docs/iOS/screen-capture/"
keywords:
  - "屏幕捕获检测"
  - "WebViewGold for iOS"
  - "将网站转换为应用"
  - "WebView 应用文档"
  - "iOS WebView SDK"
  - "PWA 转应用"
  - "HTML 转应用"
  - "JavaScript 桥接"
last_updated: "2026-10-09"
---

# 屏幕捕获检测 – WebViewGold for iOS

> **摘要：** 在您的 iOS 应用中检测截图和屏幕录制，并从您的网页应用作出响应。

[文档](../README.md) › [WebViewGold for iOS](README.md) › 屏幕捕获检测

**平台：** iOS · **类别：** 扩展与插件 · **在线版本：** [www.webviewgold.com/zh/docs/iOS/screen-capture/](https://www.webviewgold.com/zh/docs/iOS/screen-capture/)

---

在 `Config.swift` 中设置 `let preventScreenCapture = true`，可检测截屏或屏幕录制行为，并自动调用 JavaScript 函数 `onScreenCaptureAttempt`。

```html
<script>
function onScreenCaptureAttempt() {
    alert('Screen capture detected');
}
</script>
```

---

## 继续阅读

- ← 上一页： [原生侧边栏](sidebar.md)
- 下一页 →： [MultiAPICall 功能](multi-api-call.md)
- 语言： [🇺🇸 English](../../ios/screen-capture.md) · [🇩🇪 Deutsch](../../de/ios/screen-capture.md) · [🇫🇷 Français](../../fr/ios/screen-capture.md) · [🇪🇸 Español](../../es/ios/screen-capture.md) · **🇨🇳 中文**

> [!TIP]
> **太忙了？我们替您搭建应用。** 我们的团队为您配置、构建并提交 WebViewGold 应用——全程代劳、交付迅速、德国制造。 [让我们搭建应用 →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **在浏览器中构建：** 无需 Mac、无需 IDE：**WebViewGold Cloud Builder** 在线为您配置、构建并上传应用。 [了解 Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
