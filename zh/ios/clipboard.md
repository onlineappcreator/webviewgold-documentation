---
title: "剪贴板 API – WebViewGold for iOS 文档"
description: "通过 JavaScript 从您的网页应用将文本复制到 iOS 剪贴板并读取剪贴板内容。"
lang: "zh"
product: "WebViewGold for iOS"
platform: "iOS"
category: "API 与功能"
slug: "clipboard"
canonical_url: "https://www.webviewgold.com/zh/docs/iOS/clipboard/"
keywords:
  - "剪贴板 API"
  - "WebViewGold for iOS"
  - "将网站转换为应用"
  - "WebView 应用文档"
  - "iOS WebView SDK"
  - "PWA 转应用"
  - "HTML 转应用"
  - "JavaScript 桥接"
last_updated: "2026-10-09"
---

# 剪贴板 API – WebViewGold for iOS

> **摘要：** 通过 JavaScript 从您的网页应用将文本复制到 iOS 剪贴板并读取剪贴板内容。

[文档](../README.md) › [WebViewGold for iOS](README.md) › 剪贴板 API

**平台：** iOS · **类别：** API 与功能 · **在线版本：** [www.webviewgold.com/zh/docs/iOS/clipboard/](https://www.webviewgold.com/zh/docs/iOS/clipboard/)

---

调用 `getclipboard://` 可将当前剪贴板内容注入到 JavaScript 变量 `clipboarddata` 中。

```html
<a href="getclipboard://">Read Clipboard</a>
<script>
function showClipboard() {
    console.log(clipboarddata);
}
</script>
```

---

## 继续阅读

- ← 上一页： [快捷方式 API](shortcut.md)
- 下一页 →： [读写值 API](read-write-value.md)
- 其他平台上的相同功能： [Android – 剪贴板 API](../android/clipboard.md)
- 语言： [🇺🇸 English](../../ios/clipboard.md) · [🇩🇪 Deutsch](../../de/ios/clipboard.md) · [🇫🇷 Français](../../fr/ios/clipboard.md) · [🇪🇸 Español](../../es/ios/clipboard.md) · **🇨🇳 中文**

> [!TIP]
> **太忙了？我们替您搭建应用。** 我们的团队为您配置、构建并提交 WebViewGold 应用——全程代劳、交付迅速、德国制造。 [让我们搭建应用 →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **在浏览器中构建：** 无需 Mac、无需 IDE：**WebViewGold Cloud Builder** 在线为您配置、构建并上传应用。 [了解 Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
