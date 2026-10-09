---
title: "URL 处理 API – WebViewGold for iOS 文档"
description: "决定哪些链接在应用内、应用内浏览器标签页或 Safari 中打开——为 iOS 提供完整的 URL 处理控制。"
lang: "zh"
product: "WebViewGold for iOS"
platform: "iOS"
category: "API 与功能"
slug: "url-handling"
canonical_url: "https://www.webviewgold.com/zh/docs/iOS/url-handling/"
keywords:
  - "URL 处理 API"
  - "WebViewGold for iOS"
  - "将网站转换为应用"
  - "WebView 应用文档"
  - "iOS WebView SDK"
  - "PWA 转应用"
  - "HTML 转应用"
  - "JavaScript 桥接"
last_updated: "2026-10-09"
---

# URL 处理 API – WebViewGold for iOS

> **摘要：** 决定哪些链接在应用内、应用内浏览器标签页或 Safari 中打开——为 iOS 提供完整的 URL 处理控制。

[文档](../README.md) › [WebViewGold for iOS](README.md) › URL 处理 API

**平台：** iOS · **类别：** API 与功能 · **在线版本：** [www.webviewgold.com/zh/docs/iOS/url-handling/](https://www.webviewgold.com/zh/docs/iOS/url-handling/)

---

为了提升用户体验，通常需要对应用如何处理不同类型的网络链接进行自定义。例如，社交媒体按钮可以配置为在系统浏览器或对应的应用中打开，而不是在您的应用内打开。WebViewGold 为基于 WebView 的 iOS 应用提供了灵活的 URL 处理设置。

## 链接类型

1. **外部链接：**指向与您应用**主域名不同**的域名的链接。
   - **示例：**若您应用的域名是 **mydomain.com**，则 **google.com** 就是一个外部链接。
2. **内部链接：**保持在与您应用**相同域名**下的链接。
   - **示例：**若您应用的域名是 **mydomain.com**，则 **mydomain.com/purchase** 就是一个内部链接。
3. **特殊链接：**包含特殊属性（例如 **target="_blank"**）的链接。

## 要配置 URL Handling API，请打开 Config.swift

1. 定义**外部链接**的默认行为：
   - 将 `externalLinkHandlingOptions` 设置为 `0`，默认在应用内打开外部链接；或设置为 `2`，始终在其他浏览器（Safari）中打开。

2. 定义**特殊链接**（例如 **target="_blank"**）的默认行为：
   - 将 `specialLinkHandlingOptions` 设置为 `0`，在应用内打开特殊链接；设置为 `1`，在新标签页（附加的应用内浏览器）中打开；或设置为 `2`，在其他浏览器（Safari）中打开。

3. 设置***始终*在 Safari 中打开**的域名（不受 `externalLinkHandlingOptions` 设置影响）：
   - 将目标域名添加到 `safariwhitelist` 列表。
   - 按此格式添加其他主机：["alwaysopeninsafari.com", "google.com", "m.facebook.com"]。
   - 请严格按照您在链接中使用的形式输入主机名（可含或不含 www，但一律不含 http/https）。

4. 设置***永远不*在 Safari 中打开**的域名（不受 `externalLinkHandlingOptions` 设置影响）：
   - 将目标域名添加到 `safariblacklist` 列表。
   - 按此格式添加其他主机：["alwaysopeninsafari.com", "google.com", "m.facebook.com"]。
   - 请严格按照您在链接中使用的形式输入主机名（可含或不含 www，但一律不含 http/https）。

5. 设置***始终***或***永远不*在应用内标签页中打开**的域名（不受 `externalLinkHandlingOptions` 设置影响）：
   - 将目标域名添加到 `alwaysOpenInInAppTab` 或 `neverOpenInInAppTab` 列表。

## 在标签页/附加的应用内浏览器中打开链接

有些链接（例如“条款与条件”页面）不至于重要到需要在外部系统浏览器中打开，但又对您应用的主 WebView 而言过于特殊。WebViewGold 为处理此类链接提供了一种巧妙的方案：**在主 WebView 上覆盖打开的应用内浏览器标签页**，从而提供一种应用与浏览器结合的混合体验。效果如下：

![在附加的应用内浏览器/标签页（SFSafariViewController）中打开链接](../../assets/ios/img/tabs.webp)

### 应用内浏览器标签页的主要特性

- 应用内浏览器标签页包含**地址栏**和**导航按钮**，相比主 WebView 提供更接近浏览器的体验。
- 非常适合需要便捷导航的内容，例如教程、知识库或包含特定信息的页面。

### 如何在基于 WebView 的 iOS 应用中使用应用内浏览器标签页

要在应用内浏览器标签页中打开链接，请将 `specialLinkHandlingOptions` 设置为 `1`，并按以下格式编写 HTML 中的 URL：

```html
<a href="https://www.example.com" target="_blank">Open link in an in-app tab</a>
```

简单来说，带有 “_blank” 目标属性的链接就被视为**特殊链接**。在普通浏览器中，这类链接会在新标签页中打开。而在 WebViewGold 应用中，您可以让它改为在应用内标签页中打开。

请注意，如果您使用的链接是外部链接（例如域名与您的网站不同，如 “www.google.com”），请同时确保 `externalLinkHandlingOptions` 设置为 `0`，否则“在其他浏览器中打开所有外部链接”的设置会覆盖特殊-外部链接的行为，使其改在 Safari 应用中打开。

**测试链接行为：**\
如需查看您的应用如何处理不同类型的链接，可在测试时将以下 URL 用作 WebView URL：\
测试链接：<https://www.webviewgold.com/demo/testlinks.php>\
**注意：**您也可以在桌面浏览器中打开同一域名，查看其源代码并复制链接格式用于您自己的链接。

---

## 继续阅读

- ← 上一页： [下拉刷新 API](pull-to-refresh.md)
- 下一页 →： [社交登录助手](social-login.md)
- 其他平台上的相同功能： [Android – URL 处理 API](../android/url-handling.md)
- 语言： [🇺🇸 English](../../ios/url-handling.md) · [🇩🇪 Deutsch](../../de/ios/url-handling.md) · [🇫🇷 Français](../../fr/ios/url-handling.md) · [🇪🇸 Español](../../es/ios/url-handling.md) · **🇨🇳 中文**

> [!TIP]
> **太忙了？我们替您搭建应用。** 我们的团队为您配置、构建并提交 WebViewGold 应用——全程代劳、交付迅速、德国制造。 [让我们搭建应用 →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **在浏览器中构建：** 无需 Mac、无需 IDE：**WebViewGold Cloud Builder** 在线为您配置、构建并上传应用。 [了解 Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
