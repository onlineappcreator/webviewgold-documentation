---
title: "条形码扫描 API – WebViewGold for iOS 文档"
description: "在您的 iOS WebView 应用中原生扫描 EAN、UPC 及其他条形码，并将结果传递给网页应用。"
lang: "zh"
product: "WebViewGold for iOS"
platform: "iOS"
category: "API 与功能"
slug: "barcode-scanner"
canonical_url: "https://www.webviewgold.com/zh/docs/iOS/barcode-scanner/"
keywords:
  - "条形码扫描 API"
  - "WebViewGold for iOS"
  - "将网站转换为应用"
  - "WebView 应用文档"
  - "iOS WebView SDK"
  - "PWA 转应用"
  - "HTML 转应用"
  - "JavaScript 桥接"
last_updated: "2026-10-09"
---

# 条形码扫描 API – WebViewGold for iOS

> **摘要：** 在您的 iOS WebView 应用中原生扫描 EAN、UPC 及其他条形码，并将结果传递给网页应用。

[文档](../README.md) › [WebViewGold for iOS](README.md) › 条形码扫描 API

**平台：** iOS · **类别：** API 与功能 · **在线版本：** [www.webviewgold.com/zh/docs/iOS/barcode-scanner/](https://www.webviewgold.com/zh/docs/iOS/barcode-scanner/)

---

WebViewGold 的条形码扫描 API 允许您基于 WebView 的应用激活设备摄像头以扫描条形码。条形码扫描成功后，结果会自动传回您的网页内容。

## 使用场景

- 为库存系统扫描产品条形码
- 在物流或活动应用中处理票据或访问代码
- 从印刷条形码中快速采集数据

## 如何触发扫描器

使用以下 HTML 启动原生条形码扫描器：

```html
<a href="barcodescanner://">Start Barcode Scanner</a>
<a href="#" onClick="alert(barcodescanresult);">Show Scan Result</a>
```

- **启动条形码扫描器：**打开设备摄像头以识别受支持的条形码格式
- **显示扫描结果：**显示存储在 JavaScript 变量 `barcodescanresult` 中的已扫描条形码内容

**技术说明：**扫描完成后，解码后的条形码值会通过 JavaScript 变量 `barcodescanresult` 注入到当前页面。您可以使用此变量自动填充表单、触发自定义逻辑或基于扫描数据执行查询。

**权限：**请确保应用具有访问设备摄像头的权限，因为条形码扫描功能需要该权限才能正常工作。

---

## 继续阅读

- ← 上一页： [QR 码扫描 API](qr-code-scanner.md)
- 下一页 →： [扫描模式 API](scanning-mode.md)
- 其他平台上的相同功能： [Android – 条形码扫描 API](../android/barcode-scanner.md)
- 语言： [🇺🇸 English](../../ios/barcode-scanner.md) · [🇩🇪 Deutsch](../../de/ios/barcode-scanner.md) · [🇫🇷 Français](../../fr/ios/barcode-scanner.md) · [🇪🇸 Español](../../es/ios/barcode-scanner.md) · **🇨🇳 中文**

> [!TIP]
> **太忙了？我们替您搭建应用。** 我们的团队为您配置、构建并提交 WebViewGold 应用——全程代劳、交付迅速、德国制造。 [让我们搭建应用 →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **在浏览器中构建：** 无需 Mac、无需 IDE：**WebViewGold Cloud Builder** 在线为您配置、构建并上传应用。 [了解 Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
