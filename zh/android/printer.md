---
title: "Printer API – WebViewGold for Android 文档"
description: "Send a remote image or PDF to the Android system print dialog — Wi-Fi printers, cloud print, or Save-as-PDF, straight from your web app."
lang: "zh"
product: "WebViewGold for Android"
platform: "Android"
category: "API 与功能"
slug: "printer"
canonical_url: "https://www.webviewgold.com/zh/docs/android/printer/"
keywords:
  - "Printer API"
  - "WebViewGold for Android"
  - "将网站转换为应用"
  - "WebView 应用文档"
  - "Android WebView SDK"
  - "PWA 转应用"
  - "HTML 转应用"
  - "JavaScript 桥接"
last_updated: "2026-10-09"
---

# Printer API – WebViewGold for Android

> **摘要：** Send a remote image or PDF to the Android system print dialog — Wi-Fi printers, cloud print, or Save-as-PDF, straight from your web app.

[文档](../README.md) › [WebViewGold for Android](README.md) › Printer API

**平台：** Android · **类别：** API 与功能 · **在线版本：** [www.webviewgold.com/zh/docs/android/printer/](https://www.webviewgold.com/zh/docs/android/printer/)

---

**打印机 API** 将远程文件（图像或 PDF）发送到 Android 系统的打印对话框，以便用户将其打印到任何已配置的打印机 — Wi-Fi、云打印或"另存为 PDF"。

## 使用方法

```html
<a href="printitem://?jobName=Invoice%20%23123&printItem=https://example.com/invoice.pdf">
  Print invoice
</a>
```

## 查询参数

| 名称 | 必填 | 描述 |
| --- | --- | --- |
| `printItem` | 是 | 要打印的文件的完整 URL（PDF、JPG、PNG、WebP…）。 |
| `jobName` | 否 | 显示在打印对话框中的可读作业名称。默认为 `Print Job`。 |

## 工作原理

1. 应用将文件从 `printItem` 下载到临时缓存。
2. 如果是图像，则通过 `PrintHelper` 打印（按比例适配）。
3. 如果是 PDF（或任何其他文档格式），则会通过适当的文档适配器发送到 Android `PrintManager`。
4. 作业排队后，临时文件将被删除。

**说明：** 目标文件必须能从设备公开访问（该 URL 必须可解析）。用户可以在打印对话框中选择**另存为 PDF**以导出副本。

---

## 继续阅读

- ← 上一页： [Document Scanner](document-scanner.md)
- 下一页 →： [Health Connect API](health-connect.md)
- 其他平台上的相同功能： [iOS – 打印机 API](../ios/printer.md)
- 语言： [🇺🇸 English](../../android/printer.md) · [🇩🇪 Deutsch](../../de/android/printer.md) · [🇫🇷 Français](../../fr/android/printer.md) · [🇪🇸 Español](../../es/android/printer.md) · **🇨🇳 中文**

> [!TIP]
> **太忙了？我们替您搭建应用。** 我们的团队为您配置、构建并提交 WebViewGold 应用——全程代劳、交付迅速、德国制造。 [让我们搭建应用 →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_android_doc_online)
>
> **在浏览器中构建：** 无需 Mac、无需 IDE：**WebViewGold Cloud Builder** 在线为您配置、构建并上传应用。 [了解 Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=android_docs)
