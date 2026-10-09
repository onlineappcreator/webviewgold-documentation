---
title: "Share Extension – WebViewGold for iOS 文档"
description: "借助 Share Extension，让用户将其他应用中的内容直接分享到您的 iOS WebView 应用中。"
lang: "zh"
product: "WebViewGold for iOS"
platform: "iOS"
category: "扩展与插件"
slug: "share-extension"
canonical_url: "https://www.webviewgold.com/zh/docs/iOS/share-extension/"
keywords:
  - "Share Extension"
  - "WebViewGold for iOS"
  - "将网站转换为应用"
  - "WebView 应用文档"
  - "iOS WebView SDK"
  - "PWA 转应用"
  - "HTML 转应用"
  - "JavaScript 桥接"
last_updated: "2026-10-09"
---

# Share Extension – WebViewGold for iOS

> **摘要：** 借助 Share Extension，让用户将其他应用中的内容直接分享到您的 iOS WebView 应用中。

[文档](../README.md) › [WebViewGold for iOS](README.md) › Share Extension

**平台：** iOS · **类别：** 扩展与插件 · **在线版本：** [www.webviewgold.com/zh/docs/iOS/share-extension/](https://www.webviewgold.com/zh/docs/iOS/share-extension/)

---

当用户通过“照片”或 Safari 等应用向您的应用分享文本或图片时，这些数据将出现在 JavaScript 变量 `sharedData` 中。共享的图片以 Base64 字符串形式提供。

```html
<script>
if (typeof sharedData !== 'undefined') {
    console.log(sharedData);
}
</script>
```

---

## 继续阅读

- ← 上一页： [打开应用设置 API](open-app-settings.md)
- 下一页 →： [Widget Extension](widget-extension.md)
- 其他平台上的相同功能： [Android – ShareIntent API](../android/share-intent.md)
- 语言： [🇺🇸 English](../../ios/share-extension.md) · [🇩🇪 Deutsch](../../de/ios/share-extension.md) · [🇫🇷 Français](../../fr/ios/share-extension.md) · [🇪🇸 Español](../../es/ios/share-extension.md) · **🇨🇳 中文**

> [!TIP]
> **太忙了？我们替您搭建应用。** 我们的团队为您配置、构建并提交 WebViewGold 应用——全程代劳、交付迅速、德国制造。 [让我们搭建应用 →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **在浏览器中构建：** 无需 Mac、无需 IDE：**WebViewGold Cloud Builder** 在线为您配置、构建并上传应用。 [了解 Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
