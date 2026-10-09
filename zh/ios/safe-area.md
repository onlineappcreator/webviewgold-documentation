---
title: "修改安全区域大小 – WebViewGold for iOS 文档"
description: "调整安全区域并启用自定义底栏，让您的网页应用在带有主页横条的 iPhone 上完美显示。"
lang: "zh"
product: "WebViewGold for iOS"
platform: "iOS"
category: "应用设计"
slug: "safe-area"
canonical_url: "https://www.webviewgold.com/zh/docs/iOS/safe-area/"
keywords:
  - "修改安全区域"
  - "WebViewGold for iOS"
  - "将网站转换为应用"
  - "WebView 应用文档"
  - "iOS WebView SDK"
  - "PWA 转应用"
  - "HTML 转应用"
  - "JavaScript 桥接"
last_updated: "2026-10-09"
---

# 修改安全区域大小 – WebViewGold for iOS

> **摘要：** 调整安全区域并启用自定义底栏，让您的网页应用在带有主页横条的 iPhone 上完美显示。

[文档](../README.md) › [WebViewGold for iOS](README.md) › 修改安全区域

**平台：** iOS · **类别：** 应用设计 · **在线版本：** [www.webviewgold.com/zh/docs/iOS/safe-area/](https://www.webviewgold.com/zh/docs/iOS/safe-area/)

---

从 iPhone 8 到 iPhone X 及更高机型的跨越，通过移除 Home 按钮并引入 Home 条，极大地改变了移动行业的用户界面。根据您的 Web 应用设计，由于默认安全区域的变化，在带有 Home 条的设备上，底部菜单栏的位置可能会不正确（内容重叠）。\
好消息是，WebViewGold 提供了一项功能，允许您开启 **bottombar** 并选择其颜色以匹配您的应用主题。由于 Home 条与应用内容重叠的问题在 iPad 上可能不会出现（因为屏幕更大且布局可能不同），因此还提供了在 iPad 上禁用此功能的选项。\
要实现此功能，请在 **Config.swift** 中标题为“Custom Bottom Bar Design”的部分使用以下变量。请务必将 **bottombar** 设置为 **true**。\
![底部栏功能的 Config 变量](../../assets/ios/img/bottombar_config.webp)\
**高级：**除了使用 bottombar 功能外，您还可以在 **WebViewController.swift** 文件中搜索这段代码片段*（按 **CMD+F**，然后输入“*`switch UIDevice.current.userInterfaceIdiom`*”）*，在这里您可以将边框值 20 更改为任意所需的值，例如 10、30 等，如下所示：\
![调整 iPhone X/XS/XS Max WebView 应用上的安全区域大小](../../assets/ios/img/edgeinsets.webp)

---

## 继续阅读

- ← 上一页： [名称、图标和启动屏](app-name-icon-splash.md)
- 下一页 →： [地理定位 API](geolocation.md)
- 语言： [🇺🇸 English](../../ios/safe-area.md) · [🇩🇪 Deutsch](../../de/ios/safe-area.md) · [🇫🇷 Français](../../fr/ios/safe-area.md) · [🇪🇸 Español](../../es/ios/safe-area.md) · **🇨🇳 中文**

> [!TIP]
> **太忙了？我们替您搭建应用。** 我们的团队为您配置、构建并提交 WebViewGold 应用——全程代劳、交付迅速、德国制造。 [让我们搭建应用 →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **在浏览器中构建：** 无需 Mac、无需 IDE：**WebViewGold Cloud Builder** 在线为您配置、构建并上传应用。 [了解 Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
