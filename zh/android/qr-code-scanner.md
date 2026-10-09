---
title: "QR 码扫描 API – WebViewGold for Android 文档"
description: "从您的 Web 应用打开原生 QR 码扫描器，并通过 URL 或 JavaScript 处理扫描结果。"
lang: "zh"
product: "WebViewGold for Android"
platform: "Android"
category: "API 与功能"
slug: "qr-code-scanner"
canonical_url: "https://www.webviewgold.com/zh/docs/android/qr-code-scanner/"
keywords:
  - "QR 码扫描 API"
  - "WebViewGold for Android"
  - "将网站转换为应用"
  - "WebView 应用文档"
  - "Android WebView SDK"
  - "PWA 转应用"
  - "HTML 转应用"
  - "JavaScript 桥接"
last_updated: "2026-10-09"
---

# QR 码扫描 API – WebViewGold for Android

> **摘要：** 从您的 Web 应用打开原生 QR 码扫描器，并通过 URL 或 JavaScript 处理扫描结果。

[文档](../README.md) › [WebViewGold for Android](README.md) › QR 码扫描 API

**平台：** Android · **类别：** API 与功能 · **在线版本：** [www.webviewgold.com/zh/docs/android/qr-code-scanner/](https://www.webviewgold.com/zh/docs/android/qr-code-scanner/)

---

要在基于 WebView 的 Android 应用中触发二维码扫描器，请使用以下 HTML 链接格式：

```html
<a href="qrcode://">Scan QR Code</a>
```

点击此链接将打开设备的摄像头以扫描二维码，二维码中编码的任何 URL 都会自动在 WebView 中加载。

## 使用场景

- 连接印刷内容与数字内容（例如，扫描杂志上的二维码以打开网页）。
- 快速访问促销活动、产品信息或活动。
- 安全地将用户链接到应用内部资源或特定的着陆页。

---

## 继续阅读

- ← 上一页： [IAP History API](iap-history.md)
- 下一页 →： [扫描模式 API](scanning-mode.md)
- 其他平台上的相同功能： [iOS – QR 码扫描 API](../ios/qr-code-scanner.md)
- 语言： [🇺🇸 English](../../android/qr-code-scanner.md) · [🇩🇪 Deutsch](../../de/android/qr-code-scanner.md) · [🇫🇷 Français](../../fr/android/qr-code-scanner.md) · [🇪🇸 Español](../../es/android/qr-code-scanner.md) · **🇨🇳 中文**

> [!TIP]
> **太忙了？我们替您搭建应用。** 我们的团队为您配置、构建并提交 WebViewGold 应用——全程代劳、交付迅速、德国制造。 [让我们搭建应用 →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_android_doc_online)
>
> **在浏览器中构建：** 无需 Mac、无需 IDE：**WebViewGold Cloud Builder** 在线为您配置、构建并上传应用。 [了解 Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=android_docs)
