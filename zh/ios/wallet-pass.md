---
title: "Apple Wallet 凭证 API – WebViewGold for iOS 文档"
description: "让用户将 .pkpass 凭证（门票、优惠券、会员卡）从您的 Web 应用添加到 Apple Wallet。"
lang: "zh"
product: "WebViewGold for iOS"
platform: "iOS"
category: "API 与功能"
slug: "wallet-pass"
canonical_url: "https://www.webviewgold.com/zh/docs/iOS/wallet-pass/"
keywords:
  - "Apple Wallet 凭证 API"
  - "WebViewGold for iOS"
  - "将网站转换为应用"
  - "WebView 应用文档"
  - "iOS WebView SDK"
  - "PWA 转应用"
  - "HTML 转应用"
  - "JavaScript 桥接"
last_updated: "2026-10-09"
---

# Apple Wallet 凭证 API – WebViewGold for iOS

> **摘要：** 让用户将 .pkpass 凭证（门票、优惠券、会员卡）从您的 Web 应用添加到 Apple Wallet。

[文档](../README.md) › [WebViewGold for iOS](README.md) › Apple Wallet 凭证 API

**平台：** iOS · **类别：** API 与功能 · **在线版本：** [www.webviewgold.com/zh/docs/iOS/wallet-pass/](https://www.webviewgold.com/zh/docs/iOS/wallet-pass/)

---

**Apple Wallet 凭证 API** 让您的 Web 应用可以向用户提供 `.pkpass` 文件（活动门票、登机牌、优惠券、会员卡等），以便用户将其添加到 **Apple Wallet**。

## 使用方法

链接到您的 `.pkpass` 文件，但将文件 URL 的 `https://` 前缀替换为 `addpkpass://`：

```html
<a href="addpkpass://example.com/passes/ticket.pkpass">将门票添加到 Apple Wallet</a>
```

## 工作原理

1. 应用将 `addpkpass://` 链接转换回 `https://` URL。
2. 凭证 URL 在应用内浏览器标签页中打开，该标签页会识别 `.pkpass` 内容并显示原生的**添加到 Apple Wallet** 预览。
3. 用户确认后，凭证将存储在 Wallet 应用中。

**注意：**凭证必须通过 HTTPS 提供，使用正确的 MIME 类型 `application/vnd.apple.pkpass`，并使用有效的 Apple Pass Type ID 证书签名（关于如何生成凭证，请参阅 [Apple Wallet Passes 文档](https://developer.apple.com/documentation/walletpasses)）。

---

## 继续阅读

- ← 上一页： [iCal 日历 API](ical-calendar.md)
- 下一页 →： [UUID API](uuid.md)
- 语言： [🇺🇸 English](../../ios/wallet-pass.md) · [🇩🇪 Deutsch](../../de/ios/wallet-pass.md) · [🇫🇷 Français](../../fr/ios/wallet-pass.md) · [🇪🇸 Español](../../es/ios/wallet-pass.md) · **🇨🇳 中文**

> [!TIP]
> **太忙了？我们替您搭建应用。** 我们的团队为您配置、构建并提交 WebViewGold 应用——全程代劳、交付迅速、德国制造。 [让我们搭建应用 →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **在浏览器中构建：** 无需 Mac、无需 IDE：**WebViewGold Cloud Builder** 在线为您配置、构建并上传应用。 [了解 Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
