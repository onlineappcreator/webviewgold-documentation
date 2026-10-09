---
title: "社交媒体登录助手（Google、Facebook 与 Apple） – WebViewGold for iOS 文档"
description: "借助内置的社交登录助手，让 Google、Facebook 和 Apple 的 OAuth 登录在您的 iOS WebView 应用中可靠运行。"
lang: "zh"
product: "WebViewGold for iOS"
platform: "iOS"
category: "API 与功能"
slug: "social-login"
canonical_url: "https://www.webviewgold.com/zh/docs/iOS/social-login/"
keywords:
  - "社交登录助手"
  - "WebViewGold for iOS"
  - "将网站转换为应用"
  - "WebView 应用文档"
  - "iOS WebView SDK"
  - "PWA 转应用"
  - "HTML 转应用"
  - "JavaScript 桥接"
last_updated: "2026-10-09"
---

# 社交媒体登录助手（Google、Facebook 与 Apple） – WebViewGold for iOS

> **摘要：** 借助内置的社交登录助手，让 Google、Facebook 和 Apple 的 OAuth 登录在您的 iOS WebView 应用中可靠运行。

[文档](../README.md) › [WebViewGold for iOS](README.md) › 社交登录助手

**平台：** iOS · **类别：** API 与功能 · **在线版本：** [www.webviewgold.com/zh/docs/iOS/social-login/](https://www.webviewgold.com/zh/docs/iOS/social-login/)

---

Google、Facebook 及其他 OAuth 提供商会限制在内嵌 WebView 中登录（例如 Google 的 *"disallowed_useragent"* 错误）。WebViewGold 内置的 **Social Login Helper**（社交登录助手）让这些登录能够在您的 iOS 应用中可靠运行——无需更改网站的登录流程。

## 工作原理

您需要定义在 Web 应用登录流程中出现的 URL 前缀。一旦其中某个触发 URL 开始加载，WebViewGold 就会在一个专用的弹出登录窗口中打开登录页面，并使用 OAuth 提供商可接受的调整后 User Agent。登录成功后，流程会自动返回您的 Web 应用。「通过 Apple 登录」（`appleid.apple.com`）会被自动检测和处理——无需任何配置。

## 配置

打开 **Config.swift** 并为您的登录流程定义触发 URL 前缀：

```javascript
var google_login_helper_triggers: [String] = ["https://accounts.google.com", "https://accounts.youtube.com"]
var facebook_login_helper_triggers: [String] = ["https://m.facebook.com", "https://www.facebook.com"]
```

- `google_login_helper_triggers`——在您的网站上进行 Google 登录时加载的 URL 前缀。
- `facebook_login_helper_triggers`——在您的网站上进行 Facebook 登录时加载的 URL 前缀。

要找到正确的触发 URL，请在桌面浏览器中启动网站的登录流程，并记录 OAuth 重定向经过了哪些 URL。

## 在外部浏览器中打开认证 URL

作为替代方案，您也可以将登录 URL 显式交给系统浏览器处理（此时会话保存在浏览器中，而不是应用内）：

```javascript
window.location.href = "googlelogin://" + encodeURIComponent("https://accounts.google.com/o/oauth2/v2/auth?...");
```

WebViewGold 会解码 `googlelogin://` 前缀之后的 URL 并在外部打开它。

## 何时使用此助手

请先尝试更简单的方案——它们通常已能解决登录问题：

- 通过 [URL Handling API](url-handling.md) 在应用内浏览器标签页或外部浏览器中打开登录域名（例如 `specialLinkHandlingOptions`、`safariblacklist`）。
- 设置[自定义 User Agent](setup.md)（`useragent_iphone` / `useragent_ipad`）。

如果应用内登录仍然失败，推荐使用 Social Login Helper 触发器来解决。

---

## 继续阅读

- ← 上一页： [URL 处理 API](url-handling.md)
- 下一页 →： [重新连接 API](reconnect.md)
- 语言： [🇺🇸 English](../../ios/social-login.md) · [🇩🇪 Deutsch](../../de/ios/social-login.md) · [🇫🇷 Français](../../fr/ios/social-login.md) · [🇪🇸 Español](../../es/ios/social-login.md) · **🇨🇳 中文**

> [!TIP]
> **太忙了？我们替您搭建应用。** 我们的团队为您配置、构建并提交 WebViewGold 应用——全程代劳、交付迅速、德国制造。 [让我们搭建应用 →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **在浏览器中构建：** 无需 Mac、无需 IDE：**WebViewGold Cloud Builder** 在线为您配置、构建并上传应用。 [了解 Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
