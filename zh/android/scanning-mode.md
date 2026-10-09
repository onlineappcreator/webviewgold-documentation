---
title: "扫描模式 API – WebViewGold for Android 文档"
description: "在 WebViewGold for Android 中微调 QR 码和条形码扫描器的相机扫描行为。"
lang: "zh"
product: "WebViewGold for Android"
platform: "Android"
category: "API 与功能"
slug: "scanning-mode"
canonical_url: "https://www.webviewgold.com/zh/docs/android/scanning-mode/"
keywords:
  - "扫描模式 API"
  - "WebViewGold for Android"
  - "将网站转换为应用"
  - "WebView 应用文档"
  - "Android WebView SDK"
  - "PWA 转应用"
  - "HTML 转应用"
  - "JavaScript 桥接"
last_updated: "2026-10-09"
---

# 扫描模式 API – WebViewGold for Android

> **摘要：** 在 WebViewGold for Android 中微调 QR 码和条形码扫描器的相机扫描行为。

[文档](../README.md) › [WebViewGold for Android](README.md) › 扫描模式 API

**平台：** Android · **类别：** API 与功能 · **在线版本：** [www.webviewgold.com/zh/docs/android/scanning-mode/](https://www.webviewgold.com/zh/docs/android/scanning-mode/)

---

如果您的 Web 应用在屏幕上显示需要被扫描的信息（例如 QR 码），将屏幕亮度调至 100% 并防止屏幕休眠会很有帮助。WebViewGold 提供了扫描模式 API，可动态启用这些最佳扫描条件。\
此 API 包含 3 个命令：

- "auto" = 打开扫描模式，并在页面重定向时自动关闭。
- "on" = 打开扫描模式，页面重定向后仍保持开启。
- "off" = 关闭扫描模式。

链接到这些类型的 URL 以使用扫描模式 API：

```html
<a href="scanningmode://auto">Enable Scanning Mode; will automatically disable on page redirect.</a>
<a href="scanningmode://on">Enable Scanning Mode; will persist until manually disabled.</a>
<a href="scanningmode://off">Disable Scanning Mode.</a>
```

---

## 继续阅读

- ← 上一页： [QR 码扫描 API](qr-code-scanner.md)
- 下一页 →： [条形码扫描 API](barcode-scanner.md)
- 其他平台上的相同功能： [iOS – 扫描模式 API](../ios/scanning-mode.md)
- 语言： [🇺🇸 English](../../android/scanning-mode.md) · [🇩🇪 Deutsch](../../de/android/scanning-mode.md) · [🇫🇷 Français](../../fr/android/scanning-mode.md) · [🇪🇸 Español](../../es/android/scanning-mode.md) · **🇨🇳 中文**

> [!TIP]
> **太忙了？我们替您搭建应用。** 我们的团队为您配置、构建并提交 WebViewGold 应用——全程代劳、交付迅速、德国制造。 [让我们搭建应用 →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_android_doc_online)
>
> **在浏览器中构建：** 无需 Mac、无需 IDE：**WebViewGold Cloud Builder** 在线为您配置、构建并上传应用。 [了解 Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=android_docs)
