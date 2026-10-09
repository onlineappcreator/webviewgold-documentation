---
title: "QR 码扫描 API – WebViewGold for iOS 文档"
description: "从您的网页应用打开原生 QR 码扫描器，并通过 URL 或 JavaScript 处理扫描结果。"
lang: "zh"
product: "WebViewGold for iOS"
platform: "iOS"
category: "API 与功能"
slug: "qr-code-scanner"
canonical_url: "https://www.webviewgold.com/zh/docs/iOS/qr-code-scanner/"
keywords:
  - "QR 码扫描 API"
  - "WebViewGold for iOS"
  - "将网站转换为应用"
  - "WebView 应用文档"
  - "iOS WebView SDK"
  - "PWA 转应用"
  - "HTML 转应用"
  - "JavaScript 桥接"
last_updated: "2026-10-09"
---

# QR 码扫描 API – WebViewGold for iOS

> **摘要：** 从您的网页应用打开原生 QR 码扫描器，并通过 URL 或 JavaScript 处理扫描结果。

[文档](../README.md) › [WebViewGold for iOS](README.md) › QR 码扫描 API

**平台：** iOS · **类别：** API 与功能 · **在线版本：** [www.webviewgold.com/zh/docs/iOS/qr-code-scanner/](https://www.webviewgold.com/zh/docs/iOS/qr-code-scanner/)

---

要在您基于 WebView 的 iOS 应用中触发二维码扫描器，请使用以下 HTML 链接格式：

```html
<a href="qrcode://">Scan QR Code</a>
```

点击此链接将打开设备的相机以扫描二维码，二维码中编码的任何 URL 都会在 WebView 内自动加载。

## 使用场景

- 连接印刷内容与数字内容（例如，扫描杂志上的二维码以打开网页）。
- 快速访问促销活动、产品信息或活动。
- 安全地将用户链接到应用内部资源或特定的落地页。

---

## 继续阅读

- ← 上一页： [购买历史 API](iap-history.md)
- 下一页 →： [条形码扫描 API](barcode-scanner.md)
- 其他平台上的相同功能： [Android – QR 码扫描 API](../android/qr-code-scanner.md)
- 语言： [🇺🇸 English](../../ios/qr-code-scanner.md) · [🇩🇪 Deutsch](../../de/ios/qr-code-scanner.md) · [🇫🇷 Français](../../fr/ios/qr-code-scanner.md) · [🇪🇸 Español](../../es/ios/qr-code-scanner.md) · **🇨🇳 中文**

> [!TIP]
> **太忙了？我们替您搭建应用。** 我们的团队为您配置、构建并提交 WebViewGold 应用——全程代劳、交付迅速、德国制造。 [让我们搭建应用 →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **在浏览器中构建：** 无需 Mac、无需 IDE：**WebViewGold Cloud Builder** 在线为您配置、构建并上传应用。 [了解 Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
