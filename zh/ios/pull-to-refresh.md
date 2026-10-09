---
title: "Pull-to-Refresh API（下拉刷新） – WebViewGold for iOS 文档"
description: "在您的 iOS WebView 应用中启用原生下拉刷新手势，自定义其颜色，并从您的 Web 应用动态开启或关闭。"
lang: "zh"
product: "WebViewGold for iOS"
platform: "iOS"
category: "API 与功能"
slug: "pull-to-refresh"
canonical_url: "https://www.webviewgold.com/zh/docs/iOS/pull-to-refresh/"
keywords:
  - "下拉刷新 API"
  - "WebViewGold for iOS"
  - "将网站转换为应用"
  - "WebView 应用文档"
  - "iOS WebView SDK"
  - "PWA 转应用"
  - "HTML 转应用"
  - "JavaScript 桥接"
last_updated: "2026-10-09"
---

# Pull-to-Refresh API（下拉刷新） – WebViewGold for iOS

> **摘要：** 在您的 iOS WebView 应用中启用原生下拉刷新手势，自定义其颜色，并从您的 Web 应用动态开启或关闭。

[文档](../README.md) › [WebViewGold for iOS](README.md) › 下拉刷新 API

**平台：** iOS · **类别：** API 与功能 · **在线版本：** [www.webviewgold.com/zh/docs/iOS/pull-to-refresh/](https://www.webviewgold.com/zh/docs/iOS/pull-to-refresh/)

---

**Pull-to-Refresh API**（下拉刷新）为您的 WebView 应用添加 iOS 原生的下拉刷新手势：用户向下拖动页面即可重新加载当前 URL——就像邮件或 Safari 等原生应用一样。

## 如何启用

打开 **Config.swift** 并设置：

```swift
var pulltorefresh = true
var preventoverscroll = false
```

- `pulltorefresh` 启用原生刷新控件。
- `preventoverscroll` 必须设置为 `false`——该手势需要 WebView 的回弹（overscroll）动画才能工作。

## 自定义颜色

您可以在 **Config.swift** 中分别为浅色模式和深色模式设置加载指示器及其背景的颜色：

```swift
var pulltorefresh_loadingsigncolour_lightmode = #colorLiteral(...)
var pulltorefresh_backgroundcolour_lightmode = #colorLiteral(...)
var pulltorefresh_loadingsigncolour_darkmode = #colorLiteral(...)
var pulltorefresh_backgroundcolour_darkmode = #colorLiteral(...)
```

提示：在 Xcode 中点击每个 `#colorLiteral` 旁边的色块即可直观地选择颜色。深色模式变体需要 iOS 13 或更高版本。

## 从您的 Web 应用动态切换

您可以在运行时开启或关闭下拉刷新——例如，在带有自己滑动手势的页面（地图、滑块、游戏）上将其禁用：

```html
<a href="enablepulltorefresh://">启用下拉刷新</a>
<a href="disablepulltorefresh://">禁用下拉刷新</a>
```

或通过 JavaScript：

```javascript
window.location.href = "disablepulltorefresh://";
```

这两个命令也可以在 [MultiAPICall](multi-api-call.md) 请求中使用。

## 值得了解

- 刷新控件会重新加载 WebView 中当前显示的 URL。
- 如果您使用 [Dynamic UI API](dynamic-ui.md) 在运行时更改底部栏颜色，下拉刷新的颜色会自动进行匹配调整。

---

## 继续阅读

- ← 上一页： [加载标志 API](loading-sign.md)
- 下一页 →： [URL 处理 API](url-handling.md)
- 语言： [🇺🇸 English](../../ios/pull-to-refresh.md) · [🇩🇪 Deutsch](../../de/ios/pull-to-refresh.md) · [🇫🇷 Français](../../fr/ios/pull-to-refresh.md) · [🇪🇸 Español](../../es/ios/pull-to-refresh.md) · **🇨🇳 中文**

> [!TIP]
> **太忙了？我们替您搭建应用。** 我们的团队为您配置、构建并提交 WebViewGold 应用——全程代劳、交付迅速、德国制造。 [让我们搭建应用 →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **在浏览器中构建：** 无需 Mac、无需 IDE：**WebViewGold Cloud Builder** 在线为您配置、构建并上传应用。 [了解 Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
