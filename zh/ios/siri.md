---
title: "Siri 插件 – WebViewGold for iOS 文档"
description: "为您的 iOS WebView 应用添加 Siri 快捷指令支持，并通过语音打开应用内容。"
lang: "zh"
product: "WebViewGold for iOS"
platform: "iOS"
category: "扩展与插件"
slug: "siri"
canonical_url: "https://www.webviewgold.com/zh/docs/iOS/siri/"
keywords:
  - "Siri 插件"
  - "WebViewGold for iOS"
  - "将网站转换为应用"
  - "WebView 应用文档"
  - "iOS WebView SDK"
  - "PWA 转应用"
  - "HTML 转应用"
  - "JavaScript 桥接"
last_updated: "2026-10-09"
---

# Siri 插件 – WebViewGold for iOS

> **摘要：** 为您的 iOS WebView 应用添加 Siri 快捷指令支持，并通过语音打开应用内容。

[文档](../README.md) › [WebViewGold for iOS](README.md) › Siri 插件

**平台：** iOS · **类别：** 扩展与插件 · **在线版本：** [www.webviewgold.com/zh/docs/iOS/siri/](https://www.webviewgold.com/zh/docs/iOS/siri/)

---

要启用 Siri 集成，请在 `Config.swift` 中的 `static let siriEnabled` 里填入您的插件令牌，并为 WebViewGold 目标添加 Siri 功能。\
如需了解更多信息，请联系 [webviewgold-siri@onlineappcreator.com](mailto:webviewgold-siri@onlineappcreator.com)。

## 如何实现 Siri 功能

1. 创建一个供 Siri 触发的 JavaScript 函数：

```javascript
function playRadio() {
   // Add desired functionality
}
```

2. 添加一个按钮或链接，用于注册 Siri 指令（请避免使用“Open”等可能让 Siri 产生歧义的词语）：

```html
<a href="addtosiri://?command=Play%20Radio&jsFunction=playRadio()">Add Play Radio to Siri</a>
```

`command` 参数用于提供推荐的语音短语，而 `jsFunction` 则指定要执行的 JavaScript 函数。

---

## 继续阅读

- ← 上一页： [NFC 插件](nfc.md)
- 下一页 →： [HealthKit 插件](healthkit.md)
- 语言： [🇺🇸 English](../../ios/siri.md) · [🇩🇪 Deutsch](../../de/ios/siri.md) · [🇫🇷 Français](../../fr/ios/siri.md) · [🇪🇸 Español](../../es/ios/siri.md) · **🇨🇳 中文**

> [!TIP]
> **太忙了？我们替您搭建应用。** 我们的团队为您配置、构建并提交 WebViewGold 应用——全程代劳、交付迅速、德国制造。 [让我们搭建应用 →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **在浏览器中构建：** 无需 Mac、无需 IDE：**WebViewGold Cloud Builder** 在线为您配置、构建并上传应用。 [了解 Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
