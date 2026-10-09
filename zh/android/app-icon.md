---
title: "应用图标 – WebViewGold for Android 文档"
description: "在 Android Studio 中为您的 WebViewGold Android 应用添加自定义应用图标——分步指南。"
lang: "zh"
product: "WebViewGold for Android"
platform: "Android"
category: "应用设计"
slug: "app-icon"
canonical_url: "https://www.webviewgold.com/zh/docs/android/app-icon/"
keywords:
  - "应用图标"
  - "WebViewGold for Android"
  - "将网站转换为应用"
  - "WebView 应用文档"
  - "Android WebView SDK"
  - "PWA 转应用"
  - "HTML 转应用"
  - "JavaScript 桥接"
last_updated: "2026-10-09"
---

# 应用图标 – WebViewGold for Android

> **摘要：** 在 Android Studio 中为您的 WebViewGold Android 应用添加自定义应用图标——分步指南。

[文档](../README.md) › [WebViewGold for Android](README.md) › 应用图标

**平台：** Android · **类别：** 应用设计 · **在线版本：** [www.webviewgold.com/zh/docs/android/app-icon/](https://www.webviewgold.com/zh/docs/android/app-icon/)

---

## 可选的应用声明，适用于您的隐私政策/条款和条件

如果您向用户提供（基于 WebViewGold 的）移动应用程序，您可以选择在您的隐私政策或条款和条件中包含以下声明（本说明仅供参考，并不构成法律建议。我们对该文本的使用方式不承担任何责任。请咨询法律专业人士以获取个人指导）：

> ```
> Our mobile apps (iOS/Android) are developed using WebViewGold by jocapps GmbH (Germany). These apps display the content of our website using a WebView framework and enrich it with selected native features to improve usability and performance. Accordingly, the same privacy policy and terms of service that apply to our website also apply to our mobile apps. For more information, please visit
> https://www.webviewgold.com/#convert-website-to-app-privacy, or contact us directly.
> ```

---

## 3) 添加自定义应用程序图标

![Android App Icon](../../assets/android/img/screenshot_Icon.webp)

以下是将自定义应用程序图标添加到基于 WebView 的 Android 应用程序的方法：

### 1. 找到现有的应用程序图标

首先，找到现有的应用程序图标文件：

- 右键单击项目中的每个 'ic_launcher.png' 文件（大小从 hdpi 到 xxxhdpi）。
- 选择在 Finder 中显示（Mac）或在资源管理器中显示（Windows）。

### 2. 替换为您的图标

将每个 ic_launcher.png 文件替换为新图标文件，确保新图标满足以下要求：

- 包括每个分辨率的图标：hdpi、xhdpi、xxhdpi 和 xxxhdpi。
- 使用高质量图像（最好是 PNG 格式）。

**提示：** 您还可以使用 [**启动器图标生成器**](https://jgilfelt.github.io/AndroidAssetStudio/icons-launcher.html) （注意：WebViewGold 不隶属于该工具的开发人员）。

不同的设备会显示方形或圆形图标。因此，您必须包括：

- 'ic_launcher.png'：用于带有方形图标的设备。
- 'ic_launcher_round.png' 和 'ic_launcher_foreground.png'：用于带有圆形图标的设备。

![Android Icon Round vs. Box](../../assets/android/img/roundvsboxicon.webp)

将所有三个文件放入每个分辨率的相应 mipmap 文件夹中（mipmap-hdpi、mipmap-xhdpi、mipmap-xxhdpi 和 mipmap-xxxhdpi）。

该视频详细解释了更改新应用程序图标的过程，以及创建它的一些建议。

[![观看视频: 应用图标](https://img.youtube.com/vi/TDDH_yaZxoI/hqdefault.jpg)](https://www.youtube.com/watch?v=TDDH_yaZxoI)

---

## 继续阅读

- ← 上一页： [配置 WebViewGold](setup.md)
- 下一页 →： [启动画面](splash-screen.md)
- 其他平台上的相同功能： [iOS – 名称、图标和启动屏](../ios/app-name-icon-splash.md) · [macOS – 应用图标](../macos/app-icon.md)
- 语言： [🇺🇸 English](../../android/app-icon.md) · [🇩🇪 Deutsch](../../de/android/app-icon.md) · [🇫🇷 Français](../../fr/android/app-icon.md) · [🇪🇸 Español](../../es/android/app-icon.md) · **🇨🇳 中文**

> [!TIP]
> **太忙了？我们替您搭建应用。** 我们的团队为您配置、构建并提交 WebViewGold 应用——全程代劳、交付迅速、德国制造。 [让我们搭建应用 →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_android_doc_online)
>
> **在浏览器中构建：** 无需 Mac、无需 IDE：**WebViewGold Cloud Builder** 在线为您配置、构建并上传应用。 [了解 Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=android_docs)
