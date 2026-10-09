---
title: "更改启动画面的文字/时长（可选） – WebViewGold for macOS 文档"
description: "在 SplashScreen.xib 中修改启动画面文字，并在 Preferences.m 中设置 WebViewGold for macOS 启动画面的最长时长。"
lang: "zh"
product: "WebViewGold for macOS"
platform: "macOS"
category: "应用设计"
slug: "splash-screen"
canonical_url: "https://www.webviewgold.com/zh/docs/mac/#splash"
keywords:
  - "启动画面"
  - "WebViewGold for macOS"
  - "将网站转换为应用"
  - "WebView 应用文档"
  - "macOS WebView SDK"
  - "PWA 转应用"
  - "HTML 转应用"
  - "JavaScript 桥接"
last_updated: "2026-10-09"
---

# 更改启动画面的文字/时长（可选） – WebViewGold for macOS

> **摘要：** 在 SplashScreen.xib 中修改启动画面文字，并在 Preferences.m 中设置 WebViewGold for macOS 启动画面的最长时长。

[文档](../README.md) › [WebViewGold for macOS](README.md) › 启动画面

**平台：** macOS · **类别：** 应用设计 · **在线版本：** [www.webviewgold.com/zh/docs/mac/#splash](https://www.webviewgold.com/zh/docs/mac/#splash)

---

请在 *Interface Builder* 子文件夹中打开 **SplashScreen.xib** 文件。随后,双击文本即可进行编辑: \
![在 Mac WebView 应用中修改启动画面的行为](../../assets/macos/img/splash.jpg)\
如果您想修改启动画面的最长显示时间,请打开 *Generic* 子文件夹中的 **Preferences.m** 文件,修改超时时间(以秒为单位):\
![在 macOS WebView 应用中编辑启动画面的最长超时时间](../../assets/macos/img/splash2.jpg)

---

## 继续阅读

- ← 上一页： [首次运行对话框](first-run-dialog.md)
- 下一页 →： [In-App Purchases API](in-app-purchases.md)
- 其他平台上的相同功能： [iOS – 名称、图标和启动屏](../ios/app-name-icon-splash.md) · [Android – 启动画面](../android/splash-screen.md)
- 语言： [🇺🇸 English](../../macos/splash-screen.md) · [🇩🇪 Deutsch](../../de/macos/splash-screen.md) · [🇫🇷 Français](../../fr/macos/splash-screen.md) · [🇪🇸 Español](../../es/macos/splash-screen.md) · **🇨🇳 中文**

