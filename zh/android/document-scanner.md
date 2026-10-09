---
title: "ML Kit Document Scanner (PDF) – WebViewGold for Android 文档"
description: "Add a Scan document option to the file upload dialog — the user scans up to 5 pages and your web app receives a PDF like any other upload."
lang: "zh"
product: "WebViewGold for Android"
platform: "Android"
category: "API 与功能"
slug: "document-scanner"
canonical_url: "https://www.webviewgold.com/zh/docs/android/document-scanner/"
keywords:
  - "Document Scanner"
  - "WebViewGold for Android"
  - "将网站转换为应用"
  - "WebView 应用文档"
  - "Android WebView SDK"
  - "PWA 转应用"
  - "HTML 转应用"
  - "JavaScript 桥接"
last_updated: "2026-10-09"
---

# ML Kit Document Scanner (PDF) – WebViewGold for Android

> **摘要：** Add a Scan document option to the file upload dialog — the user scans up to 5 pages and your web app receives a PDF like any other upload.

[文档](../README.md) › [WebViewGold for Android](README.md) › Document Scanner

**平台：** Android · **类别：** API 与功能 · **在线版本：** [www.webviewgold.com/zh/docs/android/document-scanner/](https://www.webviewgold.com/zh/docs/android/document-scanner/)

---

**文档扫描仪**功能在标准文件上传选择器中添加了一个**扫描文档**选项。用户最多可以用相机扫描 5 页；应用会生成一个 PDF，并通过您的 Web 应用使用的标准 `<input type="file">` 流程上传。它由 Google 的 ML Kit 文档扫描仪提供支持。

## 如何启用

在 **Config.java** 中开启该功能：

```java
public static final boolean ENABLE_ML_KIT_DOCUMENT_SCANNER = true;
```

设置为 `false` 以隐藏**扫描文档**条目。

## 用户体验

1. 在您的网页上，用户点击 `<input type="file">`。
2. 应用会显示一个上传对话框，其中包含*扫描文档*、*拍照*、*录制视频*和*从图库选择*等条目（具体取决于输入的 `accept` 属性）。
3. 点击**扫描文档**会启动 Google 的 ML Kit 扫描仪：它会检测边缘、裁剪并增强每一页，允许添加更多页面，并返回一个 PDF。
4. 生成的 PDF 会被送回 `<input type="file">` — 您的 Web 应用会像接收任何其他上传文件一样接收它。

**说明：** 需要 Google Play 服务（在所有安装了 Play Store 的标准 Android 手机上均可用）。结果格式为 **PDF**，每次扫描最多 5 页。扫描仪内的图库导入默认允许。

---

## 继续阅读

- ← 上一页： [Biometric Auth API](biometric-auth.md)
- 下一页 →： [Printer API](printer.md)
- 其他平台上的相同功能： [iOS – 文档扫描仪](../ios/document-scanner.md)
- 语言： [🇺🇸 English](../../android/document-scanner.md) · [🇩🇪 Deutsch](../../de/android/document-scanner.md) · [🇫🇷 Français](../../fr/android/document-scanner.md) · [🇪🇸 Español](../../es/android/document-scanner.md) · **🇨🇳 中文**

> [!TIP]
> **太忙了？我们替您搭建应用。** 我们的团队为您配置、构建并提交 WebViewGold 应用——全程代劳、交付迅速、德国制造。 [让我们搭建应用 →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_android_doc_online)
>
> **在浏览器中构建：** 无需 Mac、无需 IDE：**WebViewGold Cloud Builder** 在线为您配置、构建并上传应用。 [了解 Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=android_docs)
