---
title: "深度链接 API – WebViewGold for iOS 文档"
description: "通过自定义 URL 方案启动您的 iOS 应用，并将用户深度链接到网页应用的特定页面。"
lang: "zh"
product: "WebViewGold for iOS"
platform: "iOS"
category: "API 与功能"
slug: "deep-linking"
canonical_url: "https://www.webviewgold.com/zh/docs/iOS/deep-linking/"
keywords:
  - "深度链接 API"
  - "WebViewGold for iOS"
  - "将网站转换为应用"
  - "WebView 应用文档"
  - "iOS WebView SDK"
  - "PWA 转应用"
  - "HTML 转应用"
  - "JavaScript 桥接"
last_updated: "2026-10-09"
---

# 深度链接 API – WebViewGold for iOS

> **摘要：** 通过自定义 URL 方案启动您的 iOS 应用，并将用户深度链接到网页应用的特定页面。

[文档](../README.md) › [WebViewGold for iOS](README.md) › 深度链接 API

**平台：** iOS · **类别：** API 与功能 · **在线版本：** [www.webviewgold.com/zh/docs/iOS/deep-linking/](https://www.webviewgold.com/zh/docs/iOS/deep-linking/)

---

**Deep Linking API** 可让您轻松将用户引导至应用内特定内容。WebViewGold 允许您配置自定义 URL Scheme（例如 `webviewgold://`），可从 **Mail、Safari 等应用**中触发，从而直接在您的 WebView 应用中打开链接。

**注意：**此功能生效的前提是设备上已经安装了该应用。

**另外**，也可以使用我们的 [**Universal Links API**](universal-links.md)。两者的工作方式类似，但使用不同的语法，而 Universal Links API 的语法比 Deep Linking API 更为常见。对于大多数应用来说，建议在两者中选择其一，而不要同时使用。

要在您的 iOS 应用中设置 **Deep Linking**，请按以下步骤操作：

1. **打开 Config.swift：**
   - 将 `ShowExternalLink` 设置为 `true`。

![Deep Linking 设置](../../assets/ios/img/universallinks.webp)
2. **打开 Info.plist：**
   - 将 URL Scheme 改为您自己的应用名称（例如将 `webviewgold://` 改为 `your-app-name://`）。

![Info.plist 是配置 Deep Linking 的关键位置，该功能也可从其他应用中触发](../../assets/ios/img/infoplist.webp)

**完成！:)** 下面的示例会在 WebView 应用中打开 google.com：

```
WebViewGold://url?link=https://www.google.com
```

[![观看视频: 深度链接 API](https://img.youtube.com/vi/mW4H_gUKU28/hqdefault.jpg)](https://www.youtube.com/watch?v=mW4H_gUKU28)

---

## 继续阅读

- ← 上一页： [Universal Links API](universal-links.md)
- 下一页 →： [应用分享对话框 API](app-sharing-dialog.md)
- 其他平台上的相同功能： [macOS – Deeplinking API](../macos/deep-linking.md)
- 语言： [🇺🇸 English](../../ios/deep-linking.md) · [🇩🇪 Deutsch](../../de/ios/deep-linking.md) · [🇫🇷 Français](../../fr/ios/deep-linking.md) · [🇪🇸 Español](../../es/ios/deep-linking.md) · **🇨🇳 中文**

> [!TIP]
> **太忙了？我们替您搭建应用。** 我们的团队为您配置、构建并提交 WebViewGold 应用——全程代劳、交付迅速、德国制造。 [让我们搭建应用 →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **在浏览器中构建：** 无需 Mac、无需 IDE：**WebViewGold Cloud Builder** 在线为您配置、构建并上传应用。 [了解 Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
