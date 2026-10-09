---
title: "扫描模式 API – WebViewGold for iOS 文档"
description: "在 WebViewGold for iOS 中微调 QR 码和条形码扫描器的相机扫描行为。"
lang: "zh"
product: "WebViewGold for iOS"
platform: "iOS"
category: "API 与功能"
slug: "scanning-mode"
canonical_url: "https://www.webviewgold.com/zh/docs/iOS/scanning-mode/"
keywords:
  - "扫描模式 API"
  - "WebViewGold for iOS"
  - "将网站转换为应用"
  - "WebView 应用文档"
  - "iOS WebView SDK"
  - "PWA 转应用"
  - "HTML 转应用"
  - "JavaScript 桥接"
last_updated: "2026-10-09"
---

# 扫描模式 API – WebViewGold for iOS

> **摘要：** 在 WebViewGold for iOS 中微调 QR 码和条形码扫描器的相机扫描行为。

[文档](../README.md) › [WebViewGold for iOS](README.md) › 扫描模式 API

**平台：** iOS · **类别：** API 与功能 · **在线版本：** [www.webviewgold.com/zh/docs/iOS/scanning-mode/](https://www.webviewgold.com/zh/docs/iOS/scanning-mode/)

---

如果您的 Web 应用在屏幕上呈现待扫描的信息（例如二维码），那么将屏幕亮度调到 100% 并防止屏幕休眠会很有帮助。WebViewGold 提供了 Scanning Mode API，可动态启用这些最佳的扫描条件。\
该 API 包含 3 个命令：

- "auto" = 开启扫描模式，并在页面跳转时自动关闭。
- "on" = 开启扫描模式，页面跳转后仍保持开启。
- "off" = 关闭扫描模式。

链接到此类 URL 即可使用 Scanning Mode API：

```html
<a href="scanningmode://auto">Enable Scanning Mode; will automatically disable on page redirect</a>
<a href="scanningmode://on">Enable Scanning Mode; will persist until manually disabled</a>
<a href="scanningmode://off">Disable Scanning Mode</a>
```

---

## 继续阅读

- ← 上一页： [条形码扫描 API](barcode-scanner.md)
- 下一页 →： [文档扫描仪](document-scanner.md)
- 其他平台上的相同功能： [Android – 扫描模式 API](../android/scanning-mode.md)
- 语言： [🇺🇸 English](../../ios/scanning-mode.md) · [🇩🇪 Deutsch](../../de/ios/scanning-mode.md) · [🇫🇷 Français](../../fr/ios/scanning-mode.md) · [🇪🇸 Español](../../es/ios/scanning-mode.md) · **🇨🇳 中文**

> [!TIP]
> **太忙了？我们替您搭建应用。** 我们的团队为您配置、构建并提交 WebViewGold 应用——全程代劳、交付迅速、德国制造。 [让我们搭建应用 →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **在浏览器中构建：** 无需 Mac、无需 IDE：**WebViewGold Cloud Builder** 在线为您配置、构建并上传应用。 [了解 Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
