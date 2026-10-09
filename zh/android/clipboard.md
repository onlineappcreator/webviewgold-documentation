---
title: "剪贴板 API – WebViewGold for Android 文档"
description: "通过 JavaScript 将文本复制到 Android 剪贴板，并从您的 Web 应用读取剪贴板内容。"
lang: "zh"
product: "WebViewGold for Android"
platform: "Android"
category: "API 与功能"
slug: "clipboard"
canonical_url: "https://www.webviewgold.com/zh/docs/android/clipboard/"
keywords:
  - "剪贴板 API"
  - "WebViewGold for Android"
  - "将网站转换为应用"
  - "WebView 应用文档"
  - "Android WebView SDK"
  - "PWA 转应用"
  - "HTML 转应用"
  - "JavaScript 桥接"
last_updated: "2026-10-09"
---

# 剪贴板 API – WebViewGold for Android

> **摘要：** 通过 JavaScript 将文本复制到 Android 剪贴板，并从您的 Web 应用读取剪贴板内容。

[文档](../README.md) › [WebViewGold for Android](README.md) › 剪贴板 API

**平台：** Android · **类别：** API 与功能 · **在线版本：** [www.webviewgold.com/zh/docs/android/clipboard/](https://www.webviewgold.com/zh/docs/android/clipboard/)

---

WebViewGold Clipboard API 提供了一种简单而安全的方式，让您能够从基于 WebView 的应用内部访问设备剪贴板的内容。它可以替代依赖原生 WebView 剪贴板访问的做法，在不同平台和版本更新之间提供更高的可靠性。

## 使用场景

- 使用复制的数据预填充表单字段
- 增强身份验证、笔记记录或分享类应用中的用户流程
- 创建快速粘贴功能或剪贴板历史工具

## 如何获取剪贴板内容

要访问剪贴板数据，请使用以下调用：

```html
<a href="getclipboard://">Get Clipboard Data</a>
<a href="#" onClick="alert(clipboarddata);">Show Clipboard Data</a>
```

- **Get Clipboard Data：**触发原生剪贴板读取功能。
- **Show Clipboard Data：**显示存储在 `clipboarddata` JavaScript 变量中的结果。

**技术说明：**一旦触发 `getclipboard://`，WebViewGold 会自动将剪贴板内容注入到页面上的 `clipboarddata` JavaScript 变量中，使其可供任何后续操作使用。

---

## 继续阅读

- ← 上一页： [加载指示 API](loading-sign.md)
- 下一页 →： [UUID API](uuid.md)
- 其他平台上的相同功能： [iOS – 剪贴板 API](../ios/clipboard.md)
- 语言： [🇺🇸 English](../../android/clipboard.md) · [🇩🇪 Deutsch](../../de/android/clipboard.md) · [🇫🇷 Français](../../fr/android/clipboard.md) · [🇪🇸 Español](../../es/android/clipboard.md) · **🇨🇳 中文**

> [!TIP]
> **太忙了？我们替您搭建应用。** 我们的团队为您配置、构建并提交 WebViewGold 应用——全程代劳、交付迅速、德国制造。 [让我们搭建应用 →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_android_doc_online)
>
> **在浏览器中构建：** 无需 Mac、无需 IDE：**WebViewGold Cloud Builder** 在线为您配置、构建并上传应用。 [了解 Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=android_docs)
