---
title: "Multi API Call (multiapicall://) – WebViewGold for Android 文档"
description: "在一次 window.location.href 赋值中调用多个 WebViewGold 数据 API — 非常适合同时使用 iOS 版本的跨平台 Web 应用。"
lang: "zh"
product: "WebViewGold for Android"
platform: "Android"
category: "API 与功能"
slug: "multi-api-call"
canonical_url: "https://www.webviewgold.com/zh/docs/android/multi-api-call/"
keywords:
  - "Multi API Call"
  - "WebViewGold for Android"
  - "将网站转换为应用"
  - "WebView 应用文档"
  - "Android WebView SDK"
  - "PWA 转应用"
  - "HTML 转应用"
  - "JavaScript 桥接"
last_updated: "2026-10-09"
---

# Multi API Call (multiapicall://) – WebViewGold for Android

> **摘要：** 在一次 window.location.href 赋值中调用多个 WebViewGold 数据 API — 非常适合同时使用 iOS 版本的跨平台 Web 应用。

[文档](../README.md) › [WebViewGold for Android](README.md) › Multi API Call

**平台：** Android · **类别：** API 与功能 · **在线版本：** [www.webviewgold.com/zh/docs/android/multi-api-call/](https://www.webviewgold.com/zh/docs/android/multi-api-call/)

---

**Multi API Call 功能**允许您**在一次 *window.location.href* 赋值中触发多个 WebViewGold API**。这对**跨平台 Web 应用**尤其有用：基于 Apple 的浏览器对同一脚本中的多次页面跳转的处理方式与 Android 不同 — 在同一脚本中多次调用 *window.location.href = "exampleAPItrigger"* 在 Android 上可行，但在 iOS 上不行。使用 `multiapicall://`，同一份 Web 代码可以在两个平台上运行。

## 支持作为条目的 API

- [get-uuid](uuid.md)
- [getonesignalplayerid](push-notifications.md)
- [getappversion](app-version-check.md)
- [statusbarcolor](dynamic-ui.md)（后跟三个 RGB 数值条目）
- [statusbartextcolor](dynamic-ui.md)（后跟一个条目：`black` 或 `white`）
- [bottombarcolor](dynamic-ui.md)（后跟三个 RGB 数值条目）
- [navbartextcolor](dynamic-ui.md)（后跟一个条目：`black` 或 `white`）

## 使用方法

用英文逗号（`,`）分隔 API 名称（以及它们的值，如有）— **不要有空格**：

```html
<script>
// 示例组合："getonesignalplayerid" 和 "getappversion"
window.location.href = "multiapicall://getonesignalplayerid,getappversion";
</script>
```

向 Dynamic UI API 传递值的方式如下：

```html
<script>
// 将状态栏设为红色、文字颜色设为白色并获取 UUID — 一次调用完成
window.location.href = "multiapicall://statusbarcolor,255,0,0,statusbartextcolor,white,get-uuid";
</script>
```

**注意：**在 Android 上，也可以依次调用各个 API（例如先调用 `window.location.href = "get-uuid://";`，再调用 `window.location.href = "getappversion://";`）。如果您想与 [WebViewGold iOS 版](../ios/multi-api-call.md)共享同一套代码，请使用 `multiapicall://`。

点击[这里](https://webviewgoldtest.github.io/multiAPI.html)查看该功能的演示网页。检查页面源代码即可查看示例代码。

---

## 继续阅读

- ← 上一页： [自定义 CSS 和 JS API](custom-css-js.md)
- 下一页 →： [地理定位 API](geolocation.md)
- 其他平台上的相同功能： [iOS – MultiAPICall 功能](../ios/multi-api-call.md)
- 语言： [🇺🇸 English](../../android/multi-api-call.md) · [🇩🇪 Deutsch](../../de/android/multi-api-call.md) · [🇫🇷 Français](../../fr/android/multi-api-call.md) · [🇪🇸 Español](../../es/android/multi-api-call.md) · **🇨🇳 中文**

> [!TIP]
> **太忙了？我们替您搭建应用。** 我们的团队为您配置、构建并提交 WebViewGold 应用——全程代劳、交付迅速、德国制造。 [让我们搭建应用 →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_android_doc_online)
>
> **在浏览器中构建：** 无需 Mac、无需 IDE：**WebViewGold Cloud Builder** 在线为您配置、构建并上传应用。 [了解 Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=android_docs)
