---
title: "URL 处理 API – WebViewGold for Android 文档"
description: "决定哪些链接在您的 Android 应用内、Chrome Custom Tabs 中或外部浏览器中打开。"
lang: "zh"
product: "WebViewGold for Android"
platform: "Android"
category: "API 与功能"
slug: "url-handling"
canonical_url: "https://www.webviewgold.com/zh/docs/android/url-handling/"
keywords:
  - "URL 处理 API"
  - "WebViewGold for Android"
  - "将网站转换为应用"
  - "WebView 应用文档"
  - "Android WebView SDK"
  - "PWA 转应用"
  - "HTML 转应用"
  - "JavaScript 桥接"
last_updated: "2026-10-09"
---

# URL 处理 API – WebViewGold for Android

> **摘要：** 决定哪些链接在您的 Android 应用内、Chrome Custom Tabs 中或外部浏览器中打开。

[文档](../README.md) › [WebViewGold for Android](README.md) › URL 处理 API

**平台：** Android · **类别：** API 与功能 · **在线版本：** [www.webviewgold.com/zh/docs/android/url-handling/](https://www.webviewgold.com/zh/docs/android/url-handling/)

---

为了提升用户体验，自定义应用处理不同类型网页链接的方式通常很有帮助。例如，可以将社交媒体按钮配置为在系统浏览器或相应的应用中打开，而不是在您的应用内打开。WebViewGold 提供了灵活的设置，可自定义基于 WebView 的 Android 应用的 URL 处理方式：

## 链接类型

1. **外部链接：** 指向与您应用主域名**不同的域名**的链接。
   - **示例：** 如果您应用的域名是 **mydomain.com**，那么外部链接就是 **google.com**。
2. **内部链接：** 与您应用处于**相同域名**下的链接。
   - **示例：** 如果您应用的域名是 **mydomain.com**，那么内部链接就是 **mydomain.com/purchase**。
3. **特殊链接：** 包含特殊属性的链接，例如 **target="_blank"**，或以 **#** 结尾的链接。

## 链接处理选项

您可以按如下所示，通过修改 **Config.java** 文件中的设置来配置链接行为。

## 外部链接处理

- **默认选项 (0)：** 若要在主 WebView 中打开外部链接（与内部链接相同），请将 `EXTERNAL_LINK_HANDLING_OPTIONS` 设置为 `0`。
- **选项 1：** 若要在新的应用内标签页中打开外部链接，请将 `EXTERNAL_LINK_HANDLING_OPTIONS` 设置为 `1`。
- **选项 2：** 若要在设备的默认系统浏览器（例如 Chrome、Safari）中打开外部链接，请将 `EXTERNAL_LINK_HANDLING_OPTIONS` 设置为 `2`。

## 特殊链接处理

- **选项 0：** 若要在应用的主 WebView 中打开特殊链接，请将 `SPECIAL_LINK_HANDLING_OPTIONS` 设置为 `0`。
- **选项 1：** 若要在新的应用内标签页中打开特殊链接，请将 `SPECIAL_LINK_HANDLING_OPTIONS` 设置为 `1`。
- **选项 2：** 若要在设备的默认系统浏览器（例如 Chrome、Safari）中打开特殊链接，请将 `SPECIAL_LINK_HANDLING_OPTIONS` 设置为 `2`。

注意：对于既是外部又是特殊的链接，此设置将覆盖 `EXTERNAL_LINK_HANDLING_OPTIONS`。

## 自定义链接访问：白名单与黑名单

若要为特定网站或页面创建例外，请打开 **Config.java** 并将该域名添加到以下某个数组中：

- **BROWSER_WHITELIST:** 列出要在应用的 WebView 内打开的特定域名。
- **BROWSER_BLACKLIST:** 列出要在外部浏览器中打开的特定域名。

有关为您的 Android 应用配置链接的详细指导，请观看下方提供的视频教程：

[![观看视频: URL 处理 API](https://img.youtube.com/vi/lq7jgaB6TxY/hqdefault.jpg)](https://www.youtube.com/watch?v=lq7jgaB6TxY)

---

## URL 处理 – 为特定链接使用应用内浏览器

有些链接（例如条款与条件页面）可能重要性不足以在外部系统浏览器中打开，但又过于特定而不适合放在应用的主 WebView 中。WebViewGold 为处理这类链接提供了一种巧妙的解决方案：**一个应用内浏览器标签页**，它在主 WebView 上层打开，提供应用与浏览器相结合的混合体验。其外观如下所示：\
![在 Android WebView 应用中于额外的应用内浏览器/标签页中打开链接](../../assets/android/img/tabs.webp)

### 应用内浏览器标签页的主要功能

- 应用内浏览器标签页包含**地址栏**和**导航按钮**，相比主 WebView 提供了更接近浏览器的体验。
- 非常适合需要便捷导航的内容，例如教程、知识库或包含特定信息的页面。

### 如何在基于 WebView 的 Android 应用中使用应用内浏览器标签页

若要在应用内浏览器标签页中打开链接，请按如下方式在 HTML 中设置 URL 的格式：

```html
<a href='#' onClick="top.location.href='https://www.example.com';">Open Example Page</a>
```

**示例：** 若要打开 Google，请使用：

```html
<a href='#' onClick="top.location.href='https://www.google.com';">Open Google</a>
```

**测试链接行为：**\
若要查看您的应用将如何处理不同类型的链接，请在测试期间将以下 URL 用作 WebView 的 URL：\
测试链接：<https://www.webviewgold.com/demo/testlinks.php>\
**注意：** 您也可以在桌面浏览器中打开同一域名，以查看源代码并复制链接的格式。

---

## 强制特定链接在应用内标签页或浏览器中打开（`newtab:` 前缀）

有时您希望**某个特定链接**在应用内浏览器标签页（或外部浏览器）中打开 — 而不受全局链接处理配置的影响。只需在 URL 前加上 `newtab:` 前缀：

```html
<a href="newtab:https://www.example.com">打开示例页面</a>
```

带前缀的链接会被作为特殊链接处理：当 `SPECIAL_LINK_HANDLING_OPTIONS` 为 `1` 时在应用内浏览器标签页中打开，为 `2` 时在外部系统浏览器中打开。这要求 **Config.java** 中的 `SPECIAL_LINK_HANDLING_OPTIONS` 设置为非 `0` 的值。

## 在 Chrome Custom Tab 中打开身份验证 URL（`googlelogin://`）

某些登录提供商（尤其是 **Google 登录**）会阻止在普通 WebView 中进行身份验证。如果[社交媒体登录辅助工具](setup.md)不适合您的流程，您可以改为在安全的 **Chrome Custom Tab** 中打开身份验证 URL，方法是加上 `googlelogin://` 前缀：

```javascript
window.location.href = "googlelogin://" + encodeURIComponent("https://accounts.google.com/o/oauth2/v2/auth?...");
```

前缀之后的 URL 会被解码并在应用内的 Chrome Custom Tab 中打开，用户可在其中完成登录。之后请将用户重定向回您的 Web 应用（例如通过您的 OAuth 重定向 URL）。

---

## 继续阅读

- ← 上一页： [Navigation Drawer & Footer](navigation-drawer.md)
- 下一页 →： [自定义 CSS 和 JS API](custom-css-js.md)
- 其他平台上的相同功能： [iOS – URL 处理 API](../ios/url-handling.md)
- 语言： [🇺🇸 English](../../android/url-handling.md) · [🇩🇪 Deutsch](../../de/android/url-handling.md) · [🇫🇷 Français](../../fr/android/url-handling.md) · [🇪🇸 Español](../../es/android/url-handling.md) · **🇨🇳 中文**

> [!TIP]
> **太忙了？我们替您搭建应用。** 我们的团队为您配置、构建并提交 WebViewGold 应用——全程代劳、交付迅速、德国制造。 [让我们搭建应用 →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_android_doc_online)
>
> **在浏览器中构建：** 无需 Mac、无需 IDE：**WebViewGold Cloud Builder** 在线为您配置、构建并上传应用。 [了解 Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=android_docs)
