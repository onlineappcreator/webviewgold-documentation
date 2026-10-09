---
title: "重新连接 API – WebViewGold for iOS 文档"
description: "在您的离线回退页面上添加“重试”按钮，重新加载您 iOS 应用的最后一个在线 URL。"
lang: "zh"
product: "WebViewGold for iOS"
platform: "iOS"
category: "API 与功能"
slug: "reconnect"
canonical_url: "https://www.webviewgold.com/zh/docs/iOS/reconnect/"
keywords:
  - "重新连接 API"
  - "WebViewGold for iOS"
  - "将网站转换为应用"
  - "WebView 应用文档"
  - "iOS WebView SDK"
  - "PWA 转应用"
  - "HTML 转应用"
  - "JavaScript 桥接"
last_updated: "2026-10-09"
---

# 重新连接 API – WebViewGold for iOS

> **摘要：** 在您的离线回退页面上添加“重试”按钮，重新加载您 iOS 应用的最后一个在线 URL。

[文档](../README.md) › [WebViewGold for iOS](README.md) › 重新连接 API

**平台：** iOS · **类别：** API 与功能 · **在线版本：** [www.webviewgold.com/zh/docs/iOS/reconnect/](https://www.webviewgold.com/zh/docs/iOS/reconnect/)

---

**重新连接 API** 会重新加载用户在应用回退到离线 HTML 页面之前所在的最后一个在线 URL。它专为您自定义的离线/回退页面上的“重试”按钮而设计。

## 使用方法

将触发器添加到您的离线页面（通常是 `local-html/index.html`）：

```html
<button onclick="window.location.href='reconnect://'">尝试重新连接</button>
```

## 工作原理

应用会记住最后一次成功加载的 URL。当用户点按 `reconnect://` 时，WebView 会导航回该 URL。如果网络仍然不可用，则会再次显示您的回退页面。

## 相关配置

- **Config.swift** 中的 `offlinelocalhtmlswitch` 必须设置为 `true`，并且您需要一个 `local-html/index.html` 回退页面，此功能才有意义。有关离线回退模式的详细信息，请参阅[设置您的 Web 应用](setup-website.md)。

---

## 继续阅读

- ← 上一页： [社交登录助手](social-login.md)
- 下一页 →： [自定义 CSS 和 JS API](custom-css-js.md)
- 其他平台上的相同功能： [Android – Reconnect API](../android/reconnect.md)
- 语言： [🇺🇸 English](../../ios/reconnect.md) · [🇩🇪 Deutsch](../../de/ios/reconnect.md) · [🇫🇷 Français](../../fr/ios/reconnect.md) · [🇪🇸 Español](../../es/ios/reconnect.md) · **🇨🇳 中文**

> [!TIP]
> **太忙了？我们替您搭建应用。** 我们的团队为您配置、构建并提交 WebViewGold 应用——全程代劳、交付迅速、德国制造。 [让我们搭建应用 →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **在浏览器中构建：** 无需 Mac、无需 IDE：**WebViewGold Cloud Builder** 在线为您配置、构建并上传应用。 [了解 Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
