---
title: "Universal Links API – WebViewGold for iOS 文档"
description: "借助 Apple Universal Links，将指向您域名的链接直接在 iOS 应用中打开——设置、AASA 文件与故障排除。"
lang: "zh"
product: "WebViewGold for iOS"
platform: "iOS"
category: "API 与功能"
slug: "universal-links"
canonical_url: "https://www.webviewgold.com/zh/docs/iOS/universal-links/"
keywords:
  - "Universal Links API"
  - "WebViewGold for iOS"
  - "将网站转换为应用"
  - "WebView 应用文档"
  - "iOS WebView SDK"
  - "PWA 转应用"
  - "HTML 转应用"
  - "JavaScript 桥接"
last_updated: "2026-10-09"
---

# Universal Links API – WebViewGold for iOS

> **摘要：** 借助 Apple Universal Links，将指向您域名的链接直接在 iOS 应用中打开——设置、AASA 文件与故障排除。

[文档](../README.md) › [WebViewGold for iOS](README.md) › Universal Links API

**平台：** iOS · **类别：** API 与功能 · **在线版本：** [www.webviewgold.com/zh/docs/iOS/universal-links/](https://www.webviewgold.com/zh/docs/iOS/universal-links/)

---

**Universal Links API** 可简化跳转至应用内特定内容的过程，为用户提供更无缝、更原生的体验。WebViewGold 允许您配置自己的域名，让来自 **Mail、Safari 等应用**的链接自动在基于 WebViewGold 的应用中打开——无需额外的确认弹窗。

**注意：**此功能生效的前提是用户设备上已经安装了该应用。

**另外**，也可以使用我们的 [**Deep Linking API**](deep-linking.md)。两者的工作方式类似，但使用不同的语法。不过值得注意的是，[**Universal Links API**](universal-links.md) 的语法比 Deep Linking API 更为常见。对于大多数应用来说，建议在两者中选择其一，而不要同时使用。

要在您的 iOS 应用中设置 **Universal Links**，请按以下步骤操作：

1. **Apple Developer Center 设置：**

1. 登录您的 [Apple Developer Center](https://developer.apple.com/account/) 账户。
2. 点击 “Certificates, Identifiers & Profiles”。
3. 在 “Identifiers” 中，选择 “App IDs”，然后从列表中选择您应用的 ID。
4. 在 “App Services” 部分下，勾选 “Associated Domains” 选项，并保存更改。

2. **Xcode 设置：**

1. 在 Xcode 中打开您的应用工程。
2. 选择对应的 target（多数情况下为 “WebViewGold”）。在 “Signing & Capabilities” 选项卡中，进入 “Associated Domains” 部分。点击 “+” 添加一个域名。您的域名前需加上 “applinks:” 前缀，例如：`applinks:example.org` 和 `applinks:www.example.org`：\
   ![Xcode 中的 Associated Domains](../../assets/ios/img/associateddomains.webp)
3. 在 Config.swift 中，将 **ShowExternalLink** 设置为 **true**。
4. 请注意子域名的区分。“www.\*” 与非 “www” 域名之间存在差异（建议同时添加两者）。请确保您的 provisioning profile 已包含 “Associated Domains” 功能。如果没有，Xcode 应会提示您进行修复。

3. **服务器端设置：**

1. 在您的网站服务器上，需要将 Apple App Site Association（AASA）文件托管在服务器根目录下，或使用 `/.well-known/` 前缀。例如：`https://example.org/.well-known/apple-app-site-association`
2. AASA 文件应包含关于应用及其关联域名的详细信息。请参阅[官方文档](https://developer.apple.com/documentation/safariservices/supporting_associated_domains)了解具体结构。请确保 apple-app-site-association 文件托管在支持 HTTPS 的服务器上，而不仅仅是 HTTP。

**完成！:-)** 在模拟器中测试的效果不如在真机上明显。为获得最佳效果，请使用实体 iPhone 或 iPad 测试。

---

## 继续阅读

- ← 上一页： [自定义 CSS 和 JS API](custom-css-js.md)
- 下一页 →： [深度链接 API](deep-linking.md)
- 其他平台上的相同功能： [Android – App Links / 深度链接](../android/app-links.md)
- 语言： [🇺🇸 English](../../ios/universal-links.md) · [🇩🇪 Deutsch](../../de/ios/universal-links.md) · [🇫🇷 Français](../../fr/ios/universal-links.md) · [🇪🇸 Español](../../es/ios/universal-links.md) · **🇨🇳 中文**

> [!TIP]
> **太忙了？我们替您搭建应用。** 我们的团队为您配置、构建并提交 WebViewGold 应用——全程代劳、交付迅速、德国制造。 [让我们搭建应用 →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **在浏览器中构建：** 无需 Mac、无需 IDE：**WebViewGold Cloud Builder** 在线为您配置、构建并上传应用。 [了解 Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
