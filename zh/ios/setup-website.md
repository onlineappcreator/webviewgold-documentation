---
title: "设置您的网页应用或网站 – WebViewGold for iOS 文档"
description: "为您的 iOS 应用准备网站、PWA 或本地 HTML 文件：使用远程 URL、将文件离线打包到应用中，或将两者结合并提供离线回退方案。"
lang: "zh"
product: "WebViewGold for iOS"
platform: "iOS"
category: "快速开始"
slug: "setup-website"
canonical_url: "https://www.webviewgold.com/zh/docs/iOS/setup-website/"
keywords:
  - "设置网页应用"
  - "WebViewGold for iOS"
  - "将网站转换为应用"
  - "WebView 应用文档"
  - "iOS WebView SDK"
  - "PWA 转应用"
  - "HTML 转应用"
  - "JavaScript 桥接"
last_updated: "2026-10-09"
---

# 设置您的网页应用或网站 – WebViewGold for iOS

> **摘要：** 为您的 iOS 应用准备网站、PWA 或本地 HTML 文件：使用远程 URL、将文件离线打包到应用中，或将两者结合并提供离线回退方案。

[文档](../README.md) › [WebViewGold for iOS](README.md) › 设置网页应用

**平台：** iOS · **类别：** 快速开始 · **在线版本：** [www.webviewgold.com/zh/docs/iOS/setup-website/](https://www.webviewgold.com/zh/docs/iOS/setup-website/)

---

## 方案 A) 使用 URL 访问您的 Web 应用（= 文件存储在线）

创建一个针对移动端优化的网站或 Web 应用，并将其上传至您的 Web 服务器/主机空间。WebViewGold for iOS 兼容传统 HTML、PHP、WordPress、渐进式 Web 应用 (PWA)、HTML5 游戏、Wix、apprat.io、Bubble、jQuery Mobile，以及现代的 AI/无代码构建工具如 Lovable、Base44 和 Bolt。在典型的工作流程中，您可以在 jQuery、Lovable、Base44、Bolt、React、Vue、Angular 或您喜欢的技术栈中构建产品 UI，然后使用 WebViewGold 作为原生 iOS 应用外壳，添加 App Store 打包、推送通知、设备 API、URL 处理和其他原生功能。

为了获得最佳的 App Store 审核效果，请让您的 Web 体验在 iPhone 和 iPad 上感觉更“有意为之”：响应式布局、大尺寸的点按区域、快速的首屏渲染、清晰的加载/空/错误状态，以及类原生应用的导航。默认情况下，WebViewGold for iOS 同时允许 HTTPS 内容和 HTTP 内容。若要获得更符合生产环境标准的安全配置，可通过[修改 iOS 传输安全设置](https://www.webviewgold.com/support-center/knowledgebase/how-to-prevent-non-https-connections-in-webviewgold-for-ios-removing-nsallowsarbitraryloadsinwebcontent-from-info-plist/)将流量限制为仅使用 HTTPS，并可考虑 `blockfaultyandselfsignedhttpscerts` 选项。建议您在 [UXreviewer.io](https://www.uxreviewer.io) 或类似服务上进行专业的用户体验/UX 审查，以提升商店审核通过率和长期的用户留存。

## 方案 B) 使用本地 HTML 文件夹访问您的 Web 应用（= 文件存储在应用内）

WebViewGold 也支持基于本地 HTML 文件夹的 Web 应用：将 **uselocalhtmlfolder** 设置为 **true**（参见[下一步](setup.md)），并将您的 HTML/CSS/JavaScript 文件（含子目录）复制到 Xcode 项目中的 “local-www” 文件夹。为此，请执行以下步骤：

1. 在 Xcode 文件层级中选中 “local-www” 文件夹里的默认文件，右键选择 “Delete”，然后点击 “Move to Trash” 删除。
2. 选中您本地网站的所有文件，将其拖放至 Xcode 文件层级中的 “local-www” 文件夹下。请确保勾选 “Create folder references”，然后点击 “Finish”。

建议您在 [UXreviewer.io](https://www.uxreviewer.io) 或类似服务上进行专业的用户体验/UX 审查，以获得最佳的 App Store 审核结果。这样的 UX 审查还能通过改进建议帮助您整体上获得更好的客户留存效果。

## 方案 C) 用户离线时使用 HTML 文件夹，用户在线时使用远程 URL（= 文件在线存储 + 应用内保留备份/回退文件）

将您的 HTML/CSS/JavaScript 文件（含子目录）复制到 Xcode 项目中的 “local-www” 文件夹。为此，请执行以下步骤：

1. 在 Xcode 文件层级中选中 “local-www” 文件夹里的默认文件，右键选择 “Delete”，然后点击 “Move to Trash” 删除。
2. 选中您本地网站的所有文件，将其拖放至 Xcode 文件层级中的 “local-www” 文件夹下。请确保勾选 “Create folder references”，然后点击 “Finish”。

将 **uselocalhtmlfolder** 设置为 **false**（参见[下一步](setup.md)），并将 **offlinelocalhtmlswitch** 设置为 **true**（参见[下一步](setup.md)）。建议您在 [UXreviewer.io](https://www.uxreviewer.io) 或类似服务上进行专业的用户体验/UX 审查，以获得最佳的 App Store 审核结果。这样的 UX 审查还能通过改进建议帮助您整体上获得更好的客户留存效果。

---

## 继续阅读

- ← 返回： [概览](README.md)
- 下一页 →： [配置 WebViewGold](setup.md)
- 其他平台上的相同功能： [Android – 设置 Web 应用](../android/setup-website.md) · [macOS – 设置您的 Web 应用](../macos/setup-website.md)
- 语言： [🇺🇸 English](../../ios/setup-website.md) · [🇩🇪 Deutsch](../../de/ios/setup-website.md) · [🇫🇷 Français](../../fr/ios/setup-website.md) · [🇪🇸 Español](../../es/ios/setup-website.md) · **🇨🇳 中文**

> [!TIP]
> **太忙了？我们替您搭建应用。** 我们的团队为您配置、构建并提交 WebViewGold 应用——全程代劳、交付迅速、德国制造。 [让我们搭建应用 →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **在浏览器中构建：** 无需 Mac、无需 IDE：**WebViewGold Cloud Builder** 在线为您配置、构建并上传应用。 [了解 Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
