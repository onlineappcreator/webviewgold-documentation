---
title: "条形码扫描 API – WebViewGold for Android 文档"
description: "在您的 Android WebView 应用中以原生方式扫描 EAN、UPC 及其他条形码，并将结果传递给您的 Web 应用。"
lang: "zh"
product: "WebViewGold for Android"
platform: "Android"
category: "API 与功能"
slug: "barcode-scanner"
canonical_url: "https://www.webviewgold.com/zh/docs/android/barcode-scanner/"
keywords:
  - "条形码扫描 API"
  - "WebViewGold for Android"
  - "将网站转换为应用"
  - "WebView 应用文档"
  - "Android WebView SDK"
  - "PWA 转应用"
  - "HTML 转应用"
  - "JavaScript 桥接"
last_updated: "2026-10-09"
---

# 条形码扫描 API – WebViewGold for Android

> **摘要：** 在您的 Android WebView 应用中以原生方式扫描 EAN、UPC 及其他条形码，并将结果传递给您的 Web 应用。

[文档](../README.md) › [WebViewGold for Android](README.md) › 条形码扫描 API

**平台：** Android · **类别：** API 与功能 · **在线版本：** [www.webviewgold.com/zh/docs/android/barcode-scanner/](https://www.webviewgold.com/zh/docs/android/barcode-scanner/)

---

WebViewGold Barcode Scanner API 使您基于 WebView 的应用能够启用设备摄像头来扫描条形码。条形码成功扫描后，结果会自动传回您的网页内容。

## 使用场景

- 扫描产品条形码以用于库存系统
- 在物流或活动类应用中处理票据或访问码
- 实现从印刷条形码快速采集数据

## 如何触发扫描器

使用以下 HTML 启动原生条形码扫描器：

```html
<a href="barcodescanner://">Start Barcode Scanner</a>
<a href="#" onClick="alert(barcodescanresult);">Show Scan Result</a>
```

- **Start Barcode Scanner：**打开设备摄像头以识别受支持的条形码格式
- **Show Scan Result：**显示存储在 `barcodescanresult` JavaScript 变量中的已扫描条形码内容

**技术说明：**扫描完成后，解码得到的条形码值会通过 `barcodescanresult` JavaScript 变量注入到当前页面。您可以使用此变量来自动填充表单、触发自定义逻辑，或根据扫描数据执行查询。

**权限：**请确保应用能够访问设备摄像头，因为条形码扫描功能的正常运行需要此权限。

---

## 继续阅读

- ← 上一页： [扫描模式 API](scanning-mode.md)
- 下一页 →： [截屏 API](take-screenshot.md)
- 其他平台上的相同功能： [iOS – 条形码扫描 API](../ios/barcode-scanner.md)
- 语言： [🇺🇸 English](../../android/barcode-scanner.md) · [🇩🇪 Deutsch](../../de/android/barcode-scanner.md) · [🇫🇷 Français](../../fr/android/barcode-scanner.md) · [🇪🇸 Español](../../es/android/barcode-scanner.md) · **🇨🇳 中文**

> [!TIP]
> **太忙了？我们替您搭建应用。** 我们的团队为您配置、构建并提交 WebViewGold 应用——全程代劳、交付迅速、德国制造。 [让我们搭建应用 →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_android_doc_online)
>
> **在浏览器中构建：** 无需 Mac、无需 IDE：**WebViewGold Cloud Builder** 在线为您配置、构建并上传应用。 [了解 Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=android_docs)
