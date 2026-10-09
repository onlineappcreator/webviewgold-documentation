---
title: "动态 UI API – WebViewGold for iOS 文档"
description: "从您的网页应用动态更改原生 UI 元素，例如状态栏或底栏的颜色。"
lang: "zh"
product: "WebViewGold for iOS"
platform: "iOS"
category: "API 与功能"
slug: "dynamic-ui"
canonical_url: "https://www.webviewgold.com/zh/docs/iOS/dynamic-ui/"
keywords:
  - "动态 UI API"
  - "WebViewGold for iOS"
  - "将网站转换为应用"
  - "WebView 应用文档"
  - "iOS WebView SDK"
  - "PWA 转应用"
  - "HTML 转应用"
  - "JavaScript 桥接"
last_updated: "2026-10-09"
---

# 动态 UI API – WebViewGold for iOS

> **摘要：** 从您的网页应用动态更改原生 UI 元素，例如状态栏或底栏的颜色。

[文档](../README.md) › [WebViewGold for iOS](README.md) › 动态 UI API

**平台：** iOS · **类别：** API 与功能 · **在线版本：** [www.webviewgold.com/zh/docs/iOS/dynamic-ui/](https://www.webviewgold.com/zh/docs/iOS/dynamic-ui/)

---

WebViewGold 允许您在 Web 应用中动态自定义 UI 元素。这些元素可以包括状态栏、底部栏（iOS）、导航栏（Android）以及下拉刷新（iOS）。WebViewGold 提供以下命令用于动态自定义这些元素：

- **statusbarcolor://**
  - 用于自动更改状态栏及其他相关 UI 元素颜色的主命令，例如状态栏文字颜色、底部栏颜色（iOS）、导航栏颜色（Android）等。
- **statusbartextcolor://**
  - 允许您手动更改状态栏文字颜色（iOS 和 Android）。
- **bottombarcolor://**
  - 若存在底部栏（iOS）或导航栏（Android）UI 元素，允许您手动更改其颜色。
- **hidebars://**
  - 允许您隐藏状态栏背景，其上的文字仍显示在透明背景之上。

## 更改状态栏颜色（并自动更改其他 UI 元素颜色）

此功能支持以下格式的颜色输入：

- RGB = {red, green, blue}

其中各数值均为 0（最小）到 255（最大）之间的整数。

使用如下 JavaScript URL 即可更改状态栏颜色：

```html
<script>
// Example: red
window.location.href = "statusbarcolor://255,0,0";
</script>
```

更改状态栏颜色后，状态栏文字会根据颜色深浅自动切换为合适的颜色（白色或黑色）。\
可选的 UI 元素如*下拉刷新*（iOS）、*底部栏*（iOS）以及*导航栏*（Android）的颜色也会随之自动调整。

## 更改状态栏文字颜色

如果您希望手动指定状态栏文字颜色，可以使用此选项。

此功能支持以下文本输入选项：

- "white"
- "black"

使用如下 JavaScript URL 即可更改状态栏文字颜色：

```html
<script>
// Example: white text
window.location.href = "statusbartextcolor://white";
// Example: black text
window.location.href = "statusbartextcolor://black";
</script>
```

## 更改底部栏颜色

此功能支持以下格式的颜色输入：

- RGB = {red, green, blue}

其中各数值均为 0（最小）到 255（最大）之间的整数。

使用如下 JavaScript URL 即可更改状态栏颜色：

```html
<script>
// Example: red
window.location.href = "bottombarcolor://255,0,0";
</script>
```

## 隐藏状态栏

hidebars 功能可为**开启**或**关闭**两种状态。

需要说明的是，状态栏的文字（例如时间和电量百分比）仍会对用户可见，
但其周围的背景会变为透明，且 WebView 会扩展以填充腾出的空间。

使用如下 JavaScript 更改状态栏的可见状态：

```html
<script>
// Example: hide the bars from view
window.location.href = "hidebars://on";
// Example: redisplay the bars after being hidden
window.location.href = "hidebars://off";
</script>
```

---

## 继续阅读

- ← 上一页： [应用版本检查 API](app-version-check.md)
- 下一页 →： [动态应用图标 API](dynamic-app-icon.md)
- 其他平台上的相同功能： [Android – 动态 UI API](../android/dynamic-ui.md)
- 语言： [🇺🇸 English](../../ios/dynamic-ui.md) · [🇩🇪 Deutsch](../../de/ios/dynamic-ui.md) · [🇫🇷 Français](../../fr/ios/dynamic-ui.md) · [🇪🇸 Español](../../es/ios/dynamic-ui.md) · **🇨🇳 中文**

> [!TIP]
> **太忙了？我们替您搭建应用。** 我们的团队为您配置、构建并提交 WebViewGold 应用——全程代劳、交付迅速、德国制造。 [让我们搭建应用 →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **在浏览器中构建：** 无需 Mac、无需 IDE：**WebViewGold Cloud Builder** 在线为您配置、构建并上传应用。 [了解 Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
