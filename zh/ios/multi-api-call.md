---
title: "MultiAPICall 功能 – WebViewGold for iOS 文档"
description: "借助适用于 iOS 的 MultiAPICall 功能，在单个请求中串联多个 WebViewGold API 调用。"
lang: "zh"
product: "WebViewGold for iOS"
platform: "iOS"
category: "扩展与插件"
slug: "multi-api-call"
canonical_url: "https://www.webviewgold.com/zh/docs/iOS/multi-api-call/"
keywords:
  - "MultiAPICall 功能"
  - "WebViewGold for iOS"
  - "将网站转换为应用"
  - "WebView 应用文档"
  - "iOS WebView SDK"
  - "PWA 转应用"
  - "HTML 转应用"
  - "JavaScript 桥接"
last_updated: "2026-10-09"
---

# MultiAPICall 功能 – WebViewGold for iOS

> **摘要：** 借助适用于 iOS 的 MultiAPICall 功能，在单个请求中串联多个 WebViewGold API 调用。

[文档](../README.md) › [WebViewGold for iOS](README.md) › MultiAPICall 功能

**平台：** iOS · **类别：** 扩展与插件 · **在线版本：** [www.webviewgold.com/zh/docs/iOS/multi-api-call/](https://www.webviewgold.com/zh/docs/iOS/multi-api-call/)

---

这是一项 **iOS 的可选功能**，因为基于 Apple 的浏览器处理同一脚本上多次页面重新加载的方式与基于 Android 的浏览器不同。
这意味着在同一网页脚本中多次调用 *window.location.href = "exampleAPItrigger"* 在 iOS 上将无法正常工作，这与 Android 不同。\
MultiAPICall 功能**允许您在网页脚本末尾通过单次 *window.location.href* 赋值调用多个 API**。如果您希望从应用中预加载多个数据功能以便在页面上使用，此功能会非常有用。\
**MultiAPICall 支持以下数据采集 API 作为条目：**
"[get-uuid](uuid.md)", "[user-disable-tracking](user-tracking.md)", "[getonesignalplayerid](push-notifications.md#getonesignalid)", "[getappversion](app-version-check.md)", "[__haptics (light, medium, heavy, success, warning, error)](haptic-feedback.md)"\
使用 JavaScript 调用此类 URL 即可一次性调用多个 API（**请务必加入检测以确保仅在 iOS 平台上使用**）：

```html
<script>
// Example combination: "getonesignalplayerid" and "getappversion"

if (getMobileOperatingSystem() == "iOS") {
    // iOS: Use MultiAPICall feature, separate API names by commas (","), NO spaces
    window.location.href = "multiapicall://getonesignalplayerid,getappversion";
} else {
    // Android: Can handle multiple calls at once, use normal API call structure
    window.location.href = "getonesignalplayerid://";
    window.location.href = "getappversion://";
}
</script>
```

点击[此处](https://webviewgoldtest.github.io/multiAPI.html)查看此功能的演示网页。检查该页面即可查看示例代码。

---

## 继续阅读

- ← 上一页： [屏幕捕获检测](screen-capture.md)
- 下一页 →： [NFC 插件](nfc.md)
- 其他平台上的相同功能： [Android – Multi API Call](../android/multi-api-call.md)
- 语言： [🇺🇸 English](../../ios/multi-api-call.md) · [🇩🇪 Deutsch](../../de/ios/multi-api-call.md) · [🇫🇷 Français](../../fr/ios/multi-api-call.md) · [🇪🇸 Español](../../es/ios/multi-api-call.md) · **🇨🇳 中文**

> [!TIP]
> **太忙了？我们替您搭建应用。** 我们的团队为您配置、构建并提交 WebViewGold 应用——全程代劳、交付迅速、德国制造。 [让我们搭建应用 →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **在浏览器中构建：** 无需 Mac、无需 IDE：**WebViewGold Cloud Builder** 在线为您配置、构建并上传应用。 [了解 Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
