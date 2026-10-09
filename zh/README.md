---
title: "WebViewGold 文档 – 将网站转换为原生 iOS、Android 和 macOS 应用"
description: "WebViewGold 官方 Markdown 文档：将任何网站、PWA 或 Web 应用转换为原生 iOS、Android 或 macOS 应用——包含设置指南、原生 JavaScript API 以及应用商店发布说明。"
lang: "zh"
product: "WebViewGold"
canonical_url: "https://www.webviewgold.com/zh/docs/"
keywords:
  - "WebViewGold"
  - "convert website to app"
  - "WebView app template"
  - "PWA to native app"
  - "iOS WebView app"
  - "Android WebView app"
  - "macOS WebView app"
  - "JavaScript bridge"
last_updated: "2026-10-09"
---

# WebViewGold 文档 – 将网站转换为原生 iOS、Android 和 macOS 应用

> WebViewGold 官方 Markdown 文档：将任何网站、PWA 或 Web 应用转换为原生 iOS、Android 或 macOS 应用——包含设置指南、原生 JavaScript API 以及应用商店发布说明。

WebViewGold 是由 OnlineAppCreator 开发的开箱即用的 Xcode 和 Android Studio 应用模板，可将您的网站、PWA、SaaS 仪表板、网店或 AI 生成的 Web 应用封装为原生应用。您的网站始终是唯一的内容来源；推送通知、应用内购买、AdMob、二维码/条形码扫描、生物识别、深度链接等原生功能，只需通过简单的配置选项和 JavaScript/URL 协议 API 即可启用。

## 从这里开始

| 平台 | 文档 | 项目 / IDE | 主题 |
|---|---|---|---|
| **iOS** | [WebViewGold for iOS](ios/README.md) | Xcode · Swift (`Config.swift`) | 60 页 |
| **Android** | [WebViewGold for Android](android/README.md) | Android Studio · Java (`Config.java`) | 47 页 |
| **macOS** | [WebViewGold for macOS](macos/README.md) | Xcode (`config.json`, `index.html`) | 14 页 |

## 本文档的结构

每个平台都有一个概览页，并为每个主题提供单独的 Markdown 页面。每页以简短摘要和元数据（平台、类别、规范 URL）开头，并以指向上一个/下一个主题、其他平台上相同功能以及所有译文的链接结尾。

```text
docs-for-github/
├── README.md            (English)
├── llms.txt             (AI / LLM index)
├── llms-full.txt        (all English pages in one file)
├── ios/                 (WebViewGold for iOS)
├── android/             (WebViewGold for Android)
├── macos/               (WebViewGold for macOS)
├── de/ fr/ es/ zh/      (translations, same structure)
└── assets/              (screenshots & images)
```

## 常见问题

### 什么是 WebViewGold？

WebViewGold 是适用于 iOS、Android 和 macOS 的原生应用模板，可将网站或 Web 应用转换为可上架的原生应用。它通过 Envato/CodeCanyon 销售，文档位于 [webviewgold.com/docs](https://www.webviewgold.com/zh/docs/)。

### 我需要编程技能吗？

不需要。您只需插入 URL，并在一个配置文件（iOS 为 `Config.swift`，Android 为 `Config.java`）中开启或关闭选项。原生功能可通过 `rateapp://` 等简单链接或少量 JavaScript 代码从 Web 应用中触发。

### 支持哪些网站和框架？

支持传统 HTML/PHP 网站、WordPress、PWA、jQuery Mobile 项目，以及使用 Lovable、Base44、Bolt、Bubble、React、Vue、Angular 或类似工具构建的现代 Web 应用。您可以加载远程 URL、打包本地 HTML 文件，或将两者结合并提供离线回退。

### 可以将应用发布到 App Store 和 Google Play 吗？

可以。“构建与发布”指南介绍了手动流程。此外，WebViewGold Cloud Builder 可在浏览器中构建并上传您的应用，WeSetupYourWebViewApp 团队也可以为您完成全部设置。

### 在哪里可以获得帮助？

请访问 [WebViewGold 支持中心](https://www.webviewgold.com/support-center/) 查看常见问题和已知问题，或通过您所用平台的“支持与联系”页面联系团队。

## 语言

[🇺🇸 English](../README.md) · [🇩🇪 Deutsch](../de/README.md) · [🇫🇷 Français](../fr/README.md) · [🇪🇸 Español](../es/README.md) · **🇨🇳 中文**

## 关于

WebViewGold 由德国的 OnlineAppCreator（jocapps GmbH）开发。此 Markdown 版本与 [www.webviewgold.com/zh/docs](https://www.webviewgold.com/zh/docs/) 上的官方在线文档保持一致；在线版本为规范来源。
