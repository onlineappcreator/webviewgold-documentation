---
title: "加载标志 API – WebViewGold for iOS 文档"
description: "按需显示或隐藏原生加载指示器，并自定义您的 iOS 应用的加载体验。"
lang: "zh"
product: "WebViewGold for iOS"
platform: "iOS"
category: "API 与功能"
slug: "loading-sign"
canonical_url: "https://www.webviewgold.com/zh/docs/iOS/loading-sign/"
keywords:
  - "加载标志 API"
  - "WebViewGold for iOS"
  - "将网站转换为应用"
  - "WebView 应用文档"
  - "iOS WebView SDK"
  - "PWA 转应用"
  - "HTML 转应用"
  - "JavaScript 桥接"
last_updated: "2026-10-09"
---

# 加载标志 API – WebViewGold for iOS

> **摘要：** 按需显示或隐藏原生加载指示器，并自定义您的 iOS 应用的加载体验。

[文档](../README.md) › [WebViewGold for iOS](README.md) › 加载标志 API

**平台：** iOS · **类别：** API 与功能 · **在线版本：** [www.webviewgold.com/zh/docs/iOS/loading-sign/](https://www.webviewgold.com/zh/docs/iOS/loading-sign/)

---

当页面开始或结束加载时，WebViewGold 的原生 iOS 加载指示器会**自动显示**。不过，您也可以手动控制加载指示器，以应对标准页面加载事件之外的场景。这在需要让用户感知加载过程的场景中尤为有用，例如：

- 在实时聊天队列中等待
- 在云服务器上运行后台进程
- 可视化任何其他耗时较长的过程，以便用户感知

## 用法

如需为您的 WebView 应用手动控制加载指示器，请使用以下链接：

```html
<a href="spinneron://">Show the loading spinner</a>
<a href="spinneroff://">Hide the loading spinner</a>
```

---

## 继续阅读

- ← 上一页： [用户跟踪决定 API](user-tracking.md)
- 下一页 →： [下拉刷新 API](pull-to-refresh.md)
- 其他平台上的相同功能： [Android – 加载指示 API](../android/loading-sign.md)
- 语言： [🇺🇸 English](../../ios/loading-sign.md) · [🇩🇪 Deutsch](../../de/ios/loading-sign.md) · [🇫🇷 Français](../../fr/ios/loading-sign.md) · [🇪🇸 Español](../../es/ios/loading-sign.md) · **🇨🇳 中文**

> [!TIP]
> **太忙了？我们替您搭建应用。** 我们的团队为您配置、构建并提交 WebViewGold 应用——全程代劳、交付迅速、德国制造。 [让我们搭建应用 →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **在浏览器中构建：** 无需 Mac、无需 IDE：**WebViewGold Cloud Builder** 在线为您配置、构建并上传应用。 [了解 Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
