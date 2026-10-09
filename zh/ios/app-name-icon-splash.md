---
title: "应用名称、图标和启动屏幕 – WebViewGold for iOS 文档"
description: "重命名您的 iOS 应用，添加自定义应用图标，并为您的 WebViewGold 应用设置个性化的启动屏幕图形。"
lang: "zh"
product: "WebViewGold for iOS"
platform: "iOS"
category: "应用设计"
slug: "app-name-icon-splash"
canonical_url: "https://www.webviewgold.com/zh/docs/iOS/app-name-icon-splash/"
keywords:
  - "名称、图标和启动屏"
  - "WebViewGold for iOS"
  - "将网站转换为应用"
  - "WebView 应用文档"
  - "iOS WebView SDK"
  - "PWA 转应用"
  - "HTML 转应用"
  - "JavaScript 桥接"
last_updated: "2026-10-09"
---

# 应用名称、图标和启动屏幕 – WebViewGold for iOS

> **摘要：** 重命名您的 iOS 应用，添加自定义应用图标，并为您的 WebViewGold 应用设置个性化的启动屏幕图形。

[文档](../README.md) › [WebViewGold for iOS](README.md) › 名称、图标和启动屏

**平台：** iOS · **类别：** 应用设计 · **在线版本：** [www.webviewgold.com/zh/docs/iOS/app-name-icon-splash/](https://www.webviewgold.com/zh/docs/iOS/app-name-icon-splash/)

---

## 更改显示的应用名称

按照截图所示，依次通过 **WebViewGold** → **WebViewGold** → **Build Settings** 导航至 **Product Name**，并按照下方截图所示更改名称：

- ***注意：***如果您的应用名称包含带重音符号的字母（例如 'à'），您需要将其替换为普通字母来设置 **Product Name**。**Product Name** 还会用于为应用中的文件命名，因此它不支持带重音符号的字母（否则应用会崩溃）。之后，为确保您的应用在 iOS 主屏幕上向用户显示正确的名称，请同时将 **Bundle Display Name**（位于 **Info.plist** 文件中）从 "$PRODUCT_NAME" 更改为带重音符号的应用名称。例如，如果您的应用名称为 "WebViewGold"，则 **Product Name** 应为 "WebViewGolda"，而 **Bundle Display Name** 应为 "WebViewGold"。

![更改您的 Web-View 应用的 iOS 名称](../../assets/ios/img/rename_xcode14.webp)

## 添加自定义应用图标

按照以下简单步骤，为您基于 WebView 的 iOS 应用添加自定义应用图标：\
**1. 定位应用图标设置**\
依次导航至 **WebViewGold** → **WebViewGold** → **General** → **App Icons and Launch Screen** → **App Icon Source**。\
![将您的 iOS 图标添加到项目空间中](../../assets/ios/img/screen6.webp)\
**2. 替换为您自己的图标**\
只需用您自己调整过尺寸的图像文件替换随附的图像文件即可。网上有一些免费工具可以帮助生成这些不同尺寸的图像，例如 [**App Icon Generator**](https://www.appicon.co/)（我们与该开发公司没有关联）。或者，您也可以搜索任何您喜欢的 "iOS App Icon Generator" 工具。

## 添加自定义启动屏幕

按照以下步骤，为您基于 WebView 的 iOS 应用添加自定义启动屏幕图形：

### 1. 启用启动屏幕

要为您的应用激活启动屏幕：

- 打开 **Config.swift** 文件并搜索 `splashScreenEnabled`。
- 确保此变量设置为 `true`。

### 2. 替换启动屏幕图像

要使用您自己的品牌形象作为启动屏幕：

- 用您自己的 GIF 文件替换 XCode 项目主文件夹中现有的 **splash.gif** 文件。
- **重要提示：**请确保您的图像文件为正方形（宽度 = 高度）以获得最佳显示效果。例如：
  - 128x128 像素
  - 512x512 像素
  - 1024x1024 像素

### 3. 调整显示超时时间

要控制启动屏幕的显示时长：

- 打开 **Config.swift** 文件并搜索 `splashTimeout`。
- 将超时设置修改为您期望的时长（以毫秒为单位）。

**示例：**设置为 `2000` 表示显示 2 秒。

如果您希望在页面成功加载完成之前一直显示启动屏幕，请将 `remainSplashOption` 选项（可在 **Config.swift** 文件中找到）设置为 `true`。否则，启动屏幕只会短暂显示，随后原生 iOS 加载指示器便会启动。\
使用 `splashscreencolor` 选项（可在 **Config.swift** 文件中找到）来修改启动屏幕的背景颜色。颜色选项可在[此处](https://developer.apple.com/documentation/uikit/uicolor/standard_colors)查看。

### 4. 为您的隐私政策 / 条款与条件添加可选的应用披露声明

如果您向用户提供（基于 WebViewGold 的）移动应用，您可以选择在您的隐私政策或条款与条件中加入以下声明（此声明仅供参考，不构成法律建议。我们对该文本的使用方式不承担任何责任。请咨询法律专业人士以获取针对个人情况的指导）：

> ```
> Our mobile apps (iOS/Android) are developed using WebViewGold by jocapps GmbH (Germany). These apps display the content of our website using a WebView framework and enrich it with selected native features to improve usability and performance. Accordingly, the same privacy policy and terms of service that apply to our website also apply to our mobile apps. For more information, please visit
> https://www.webviewgold.com/#convert-website-to-app-privacy, or contact us directly.
> ```

---

## 继续阅读

- ← 上一页： [配置 WebViewGold](setup.md)
- 下一页 →： [修改安全区域](safe-area.md)
- 其他平台上的相同功能： [Android – 应用图标](../android/app-icon.md) · [macOS – 应用图标](../macos/app-icon.md)
- 语言： [🇺🇸 English](../../ios/app-name-icon-splash.md) · [🇩🇪 Deutsch](../../de/ios/app-name-icon-splash.md) · [🇫🇷 Français](../../fr/ios/app-name-icon-splash.md) · [🇪🇸 Español](../../es/ios/app-name-icon-splash.md) · **🇨🇳 中文**

> [!TIP]
> **太忙了？我们替您搭建应用。** 我们的团队为您配置、构建并提交 WebViewGold 应用——全程代劳、交付迅速、德国制造。 [让我们搭建应用 →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **在浏览器中构建：** 无需 Mac、无需 IDE：**WebViewGold Cloud Builder** 在线为您配置、构建并上传应用。 [了解 Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
