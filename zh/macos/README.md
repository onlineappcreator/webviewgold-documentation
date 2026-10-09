---
title: "WebViewGold for macOS 文档 – 将网站转换为 Mac 应用"
description: "WebViewGold for macOS 官方文档：将您的网站、PWA、SaaS 仪表板或 HTML 项目转换为原生 Mac 桌面应用，包含 Xcode 设置、配置选项、JavaScript API、发布指南以及 SDK 风格的实现说明。"
lang: "zh"
product: "WebViewGold for macOS"
platform: "macOS"
canonical_url: "https://www.webviewgold.com/zh/docs/mac/"
keywords:
  - "WebViewGold for macOS"
  - "将网站转换为应用"
  - "WebView 应用文档"
  - "macOS WebView SDK"
  - "PWA 转应用"
  - "HTML 转应用"
  - "JavaScript 桥接"
last_updated: "2026-10-09"
---

# WebViewGold for macOS 文档

![WebViewGold for macOS](../../assets/macos/img/header.png)

> WebViewGold for macOS 官方文档：将您的网站、PWA、SaaS 仪表板或 HTML 项目转换为原生 Mac 桌面应用，包含 Xcode 设置、配置选项、JavaScript API、发布指南以及 SDK 风格的实现说明。

[文档](../README.md) › WebViewGold for macOS

在几分钟内将您的网站、PWA、SaaS 仪表板、电商店面或 AI 生成的 Web 应用转换为原生 macOS 应用。像使用轻量级应用 SDK 一样使用 WebViewGold：配置 URL、启用原生 API、集成 JavaScript 桥接命令，无需从头重建 Web 产品即可发布可上架的应用。

WebViewGold 兼容经典的 HTML/PHP 网站、WordPress、jQuery Mobile 项目，以及使用 Lovable、Base44、Bolt、Bubble、React、Vue、Angular 或类似工具创建的现代 Web 应用。以下文档以技术性、注重实现的方式介绍配置流程、原生功能 API、安全注意事项和发布步骤。

**[开始教程 →](setup-website.md)** · [下载 WebViewGold](https://www.webviewgold.com/download/mac/)

## 快速上手

1. **[设置您的 Web 应用](setup-website.md)** — 使用远程 URL、打包本地 HTML 文件，或将两者结合并提供离线回退。
2. **[配置 WebViewGold](setup.md)** — 插入您的 URL，并在一个简单的配置文件中微调每个选项——无需编写代码。

## 所有主题、API 与功能

WebViewGold for macOS 的全部能力——每个主题独立成页：

### 快速开始

- **[设置您的 Web 应用](setup-website.md)** — 为 WebViewGold for macOS 准备您的网站、PWA 或 Web 应用：支持的技术（HTML、PHP、WordPress、PWA、Lovable、Base44、Bolt 等）以及打造原生桌面体验的建议。
- **[设置 WebViewGold](setup.md)** — 安装 Xcode，打开 WebViewGold for macOS 项目，在 index.html 中填写您的 URL 并配置 config.json——或打包您自己的本地 HTML 内容。

### 应用设计

- **[应用图标](app-icon.md)** — 用您自己调整好尺寸的图像文件替换 WebViewGold for macOS 桌面应用的图标。
- **[应用名称](app-name.md)** — 在 Xcode 中更改 WebViewGold for macOS 桌面应用的名称。
- **[离线界面文字](offline-screen.md)** — 在 Interface Builder 中编辑 OfflineOverlay.xib，自定义 Mac WebView 应用的离线界面文字。
- **[首次运行对话框](first-run-dialog.md)** — 在 FirstRunWindow.xib（Interface Builder）中编辑 Mac WebView 应用首次运行对话框的文字。
- **[启动画面](splash-screen.md)** — 在 SplashScreen.xib 中修改启动画面文字，并在 Preferences.m 中设置 WebViewGold for macOS 启动画面的最长时长。

### API 与功能

- **[In-App Purchases API](in-app-purchases.md)** — 从您的 Web 应用销售 Mac App Store 应用内购买和订阅：在 Constants.h 中添加产品 ID，并通过 inapppurchase:// 链接触发购买。
- **[UUID API](uuid.md)** — 通过 get-uuid:// 将非个人的唯一设备 ID（UUID）传递给 JavaScript，用于识别设备并恢复设置。
- **[Deeplinking API](deep-linking.md)** — 通过自定义 URL 协议启动 WebViewGold for macOS 应用并直接打开指定页面——分步讲解深度链接设置。

### 更多

- **[致谢与许可](credits.md)** — WebViewGold for macOS 的许可信息、商标说明及开源致谢（MacGap，MIT 许可）。
- **[为 WebViewGold 评分](rate.md)** — 喜欢 WebViewGold for macOS 吗？只需 10 秒即可在 CodeCanyon 上为其评分——这将激励我们持续更新。
- **[继续查看 iOS 与 Android](more-platforms.md)** — 在移动端复用您的 Web 应用：获取 WebViewGold for iOS 和 Android——以及 photos2webgallery for macOS。
- **[联系我们](support.md)** — 获取 WebViewGold for macOS 帮助：在支持中心查找快速解答，或直接联系团队。

## 一个 Web 应用，覆盖所有平台

使用 WebViewGold，将同一个网站复用于 iOS、Android & macOS 应用。

- [WebViewGold for iOS](../ios/README.md)
- [WebViewGold for Android](../android/README.md)

**语言：** [🇺🇸 English](../../macos/README.md) · [🇩🇪 Deutsch](../../de/macos/README.md) · [🇫🇷 Français](../../fr/macos/README.md) · [🇪🇸 Español](../../es/macos/README.md) · **🇨🇳 中文**

