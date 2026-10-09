---
title: "VisionKit 文档扫描仪 – WebViewGold for iOS 文档"
description: "让用户使用相机扫描纸质文档，并通过您 Web 应用的文件上传功能上传——由 Apple VisionKit 驱动。"
lang: "zh"
product: "WebViewGold for iOS"
platform: "iOS"
category: "API 与功能"
slug: "document-scanner"
canonical_url: "https://www.webviewgold.com/zh/docs/iOS/document-scanner/"
keywords:
  - "文档扫描仪"
  - "WebViewGold for iOS"
  - "将网站转换为应用"
  - "WebView 应用文档"
  - "iOS WebView SDK"
  - "PWA 转应用"
  - "HTML 转应用"
  - "JavaScript 桥接"
last_updated: "2026-10-09"
---

# VisionKit 文档扫描仪 – WebViewGold for iOS

> **摘要：** 让用户使用相机扫描纸质文档，并通过您 Web 应用的文件上传功能上传——由 Apple VisionKit 驱动。

[文档](../README.md) › [WebViewGold for iOS](README.md) › 文档扫描仪

**平台：** iOS · **类别：** API 与功能 · **在线版本：** [www.webviewgold.com/zh/docs/iOS/document-scanner/](https://www.webviewgold.com/zh/docs/iOS/document-scanner/)

---

**文档扫描仪**功能会在应用的标准文件上传选择器中添加**扫描文稿**选项。用户可以使用相机扫描一页或多页；应用生成文档扫描件，并通过您的 Web 应用使用的标准 `<input type="file">` 流程上传。该功能由 Apple 的 **VisionKit** 框架（`VNDocumentCameraViewController`）驱动——支持自动边缘检测、裁剪和图像增强。

## 启用方法

在 **Config.swift** 中开启此功能：

```swift
var kVisionKitEnable = true
```

设置为 `false` 可隐藏**扫描文稿**选项。

## 用户体验

1. 在您的网页上，用户点按 `<input type="file">`。
2. 应用显示上传对话框，其中包含*扫描文稿*、*相机*和*照片图库*等选项。
3. 点按**扫描文稿**会启动 VisionKit 扫描仪：它会检测边缘、裁剪并增强每一页，还允许添加更多页面。
4. 生成的扫描件会被送回 `<input type="file">`——您的 Web 应用会像接收任何其他上传文件一样接收它。

**注意：**需要 iOS 18.4 或更高版本，以及支持 VisionKit 文档相机的设备。在不受支持的设备上，**扫描文稿**选项会自动隐藏。

---

## 继续阅读

- ← 上一页： [扫描模式 API](scanning-mode.md)
- 下一页 →： [截图 API](take-screenshot.md)
- 其他平台上的相同功能： [Android – Document Scanner](../android/document-scanner.md)
- 语言： [🇺🇸 English](../../ios/document-scanner.md) · [🇩🇪 Deutsch](../../de/ios/document-scanner.md) · [🇫🇷 Français](../../fr/ios/document-scanner.md) · [🇪🇸 Español](../../es/ios/document-scanner.md) · **🇨🇳 中文**

> [!TIP]
> **太忙了？我们替您搭建应用。** 我们的团队为您配置、构建并提交 WebViewGold 应用——全程代劳、交付迅速、德国制造。 [让我们搭建应用 →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **在浏览器中构建：** 无需 Mac、无需 IDE：**WebViewGold Cloud Builder** 在线为您配置、构建并上传应用。 [了解 Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
