---
title: "打印机 API – WebViewGold for iOS 文档"
description: "通过 AirPrint 从您的 Web 应用打印图片和 PDF：只需一个链接即可将文件发送到 iOS 原生打印对话框。"
lang: "zh"
product: "WebViewGold for iOS"
platform: "iOS"
category: "API 与功能"
slug: "printer"
canonical_url: "https://www.webviewgold.com/zh/docs/iOS/printer/"
keywords:
  - "打印机 API"
  - "WebViewGold for iOS"
  - "将网站转换为应用"
  - "WebView 应用文档"
  - "iOS WebView SDK"
  - "PWA 转应用"
  - "HTML 转应用"
  - "JavaScript 桥接"
last_updated: "2026-10-09"
---

# 打印机 API – WebViewGold for iOS

> **摘要：** 通过 AirPrint 从您的 Web 应用打印图片和 PDF：只需一个链接即可将文件发送到 iOS 原生打印对话框。

[文档](../README.md) › [WebViewGold for iOS](README.md) › 打印机 API

**平台：** iOS · **类别：** API 与功能 · **在线版本：** [www.webviewgold.com/zh/docs/iOS/printer/](https://www.webviewgold.com/zh/docs/iOS/printer/)

---

**打印机 API** 将远程文件（图片或 PDF）发送到 iOS 原生打印对话框（**AirPrint**），用户可以在任何已配置的打印机上打印，或将其保存为 PDF。

## 使用方法

```html
<a href="printitem://?jobName=Invoice%20%23123&printItem=https://example.com/invoice.pdf">
  打印发票
</a>
```

## 查询参数

| 名称 | 必填 | 说明 |
| --- | --- | --- |
| `printItem` | 是 | 要打印文件的完整 URL（PDF、JPG、PNG、WebP…）。 |
| `jobName` | 否 | 在打印对话框中显示的、易于识别的任务名称。 |

## 工作原理

1. 应用将 `printItem` 指向的文件下载到临时缓存。
2. 文件被交给原生的 `UIPrintInteractionController`，由其显示 iOS 打印对话框。
3. 用户选择 AirPrint 打印机（或通过共享选项选择**存储为 PDF**）并确认。

**注意：**目标文件必须可从设备公开访问（URL 必须可解析）。请对 `jobName` 参数中的特殊字符进行 URL 编码（例如空格用 `%20`）。

---

## 继续阅读

- ← 上一页： [文件下载 API](file-downloader.md)
- 下一页 →： [iCal 日历 API](ical-calendar.md)
- 其他平台上的相同功能： [Android – Printer API](../android/printer.md)
- 语言： [🇺🇸 English](../../ios/printer.md) · [🇩🇪 Deutsch](../../de/ios/printer.md) · [🇫🇷 Français](../../fr/ios/printer.md) · [🇪🇸 Español](../../es/ios/printer.md) · **🇨🇳 中文**

> [!TIP]
> **太忙了？我们替您搭建应用。** 我们的团队为您配置、构建并提交 WebViewGold 应用——全程代劳、交付迅速、德国制造。 [让我们搭建应用 →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **在浏览器中构建：** 无需 Mac、无需 IDE：**WebViewGold Cloud Builder** 在线为您配置、构建并上传应用。 [了解 Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
