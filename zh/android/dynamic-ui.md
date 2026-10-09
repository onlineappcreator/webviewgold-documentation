---
title: "动态 UI API – WebViewGold for Android 文档"
description: "从您的 Web 应用在 Android 上动态更改状态栏颜色等原生 UI 元素。"
lang: "zh"
product: "WebViewGold for Android"
platform: "Android"
category: "API 与功能"
slug: "dynamic-ui"
canonical_url: "https://www.webviewgold.com/zh/docs/android/dynamic-ui/"
keywords:
  - "动态 UI API"
  - "WebViewGold for Android"
  - "将网站转换为应用"
  - "WebView 应用文档"
  - "Android WebView SDK"
  - "PWA 转应用"
  - "HTML 转应用"
  - "JavaScript 桥接"
last_updated: "2026-10-09"
---

# 动态 UI API – WebViewGold for Android

> **摘要：** 从您的 Web 应用在 Android 上动态更改状态栏颜色等原生 UI 元素。

[文档](../README.md) › [WebViewGold for Android](README.md) › 动态 UI API

**平台：** Android · **类别：** API 与功能 · **在线版本：** [www.webviewgold.com/zh/docs/android/dynamic-ui/](https://www.webviewgold.com/zh/docs/android/dynamic-ui/)

---

WebViewGold 允许您在 Web 应用中动态定制 UI 元素。这些元素可能包括状态栏、底部栏（iOS）、导航栏（Android）和下拉刷新（iOS）。WebViewGold 包含以下命令来动态定制这些元素：

- **statusbarcolor://**
  - 用于自动更改状态栏及其他所有相关 UI 元素颜色的主命令，例如状态栏文字颜色、底部栏颜色（iOS）、导航栏颜色（Android）等。
- **statusbartextcolor://**
  - 允许您手动更改状态栏的文字颜色（iOS 和 Android）。
- **bottombarcolor://**
  - 如果存在底部栏（iOS）或导航栏（Android）UI 元素，则允许您手动更改其颜色。
- **navbartextcolor://**
  - 允许您手动更改 Android 上导航栏的文字颜色。iOS 上将忽略该请求（iOS 上的底部栏没有文字）。
- **hidebars://**
  - 允许您隐藏状态栏和导航栏的背景。

## 更改状态栏的颜色（并自动更改其他 UI 元素）

此功能支持以下格式的颜色输入：

- RGB = {red, green, blue}

其中数值为 0（最小）到 255（最大）之间的整数。

使用 JavaScript 跳转到此类 URL 以更改状态栏颜色：

```html
<script>
// Example: red
window.location.href = "statusbarcolor://255,0,0";
</script>
```

更改状态栏颜色时，状态栏文字会根据颜色的深浅自动切换为合适的颜色（白色或黑色）。\
可选的 UI 功能，如*下拉刷新*（iOS）、*底部栏*（iOS）和*导航栏*（Android）的颜色也会自动调整。

## 更改状态栏文字的颜色

如果您想手动选择状态栏文字的颜色，可以使用此选项。

此功能支持以下选项的文本输入：

- "white"
- "black"

使用 JavaScript 跳转到此类 URL 以更改状态栏文字的颜色：

```html
<script>
// Example: white text
window.location.href = "statusbartextcolor://white";
// Example: black text
window.location.href = "statusbartextcolor://black";
</script>
```

## 更改导航栏的颜色

此功能支持以下格式的颜色输入：

- RGB = {red, green, blue}

其中数值为 0（最小）到 255（最大）之间的整数。

使用 JavaScript 跳转到此类 URL 以更改导航栏颜色：

```html
<script>
// Example: red
window.location.href = "bottombarcolor://255,0,0";
</script>
```

## 更改导航栏文字的颜色

如果您想手动选择导航栏文字的颜色，可以使用此选项。请注意，此请求在 iOS 上将被忽略。

此功能支持以下选项的文本输入：

- "white"
- "black"

使用 JavaScript 跳转到此类 URL 以更改导航栏文字的颜色：

```html
<script>
// Example: white text
window.location.href = "navbartextcolor://white";
// Example: black text
window.location.href = "navbartextcolor://black";
</script>
```

## 隐藏状态栏和底部栏

hidebars 功能可以处于**开启**或**关闭**状态。

请注意，状态栏文字（如时间和电量百分比）*不会*保持对用户可见。
但是，可以通过用户从顶部滑动的手势重新显示这些内容。

使用 JavaScript 更改状态栏和导航栏的可见状态：

```html
<script>
// Example: hide the bars from view
window.location.href = "hidebars://on";
// Example: redisplay the bars after being hidden
window.location.href = "hidebars://off";
</script>
```

---

## 检测深色模式（JavaScript 变量 `isDarkMode`）

为了让动态 UI 颜色适配用户的系统主题，WebViewGold 会在每个页面加载完成后自动注入 JavaScript 变量 `isDarkMode`（`true` 或 `false`）。示例：

```html
<script>
if (typeof isDarkMode !== "undefined" && isDarkMode) {
    // 深色模式：例如设置深色状态栏
    window.location.href = "statusbarcolor://0,0,0";
    window.location.href = "statusbartextcolor://white";
} else {
    // 浅色模式
    window.location.href = "statusbarcolor://255,255,255";
    window.location.href = "statusbartextcolor://black";
}
</script>
```

**注意：**您也可以在 Web 应用中使用标准 CSS 媒体查询 `prefers-color-scheme`。当您想通过 JavaScript 触发上述 WebViewGold UI API 时，注入的 `isDarkMode` 变量非常方便。

---

## 继续阅读

- ← 上一页： [通讯录 API](contacts.md)
- 下一页 →： [触觉反馈 API](haptic-feedback.md)
- 其他平台上的相同功能： [iOS – 动态 UI API](../ios/dynamic-ui.md)
- 语言： [🇺🇸 English](../../android/dynamic-ui.md) · [🇩🇪 Deutsch](../../de/android/dynamic-ui.md) · [🇫🇷 Français](../../fr/android/dynamic-ui.md) · [🇪🇸 Español](../../es/android/dynamic-ui.md) · **🇨🇳 中文**

> [!TIP]
> **太忙了？我们替您搭建应用。** 我们的团队为您配置、构建并提交 WebViewGold 应用——全程代劳、交付迅速、德国制造。 [让我们搭建应用 →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_android_doc_online)
>
> **在浏览器中构建：** 无需 Mac、无需 IDE：**WebViewGold Cloud Builder** 在线为您配置、构建并上传应用。 [了解 Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=android_docs)
