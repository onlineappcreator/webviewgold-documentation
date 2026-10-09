---
title: "应用内评分对话框 API – WebViewGold for Android 文档"
description: "请求用户在 Google Play 上评分：通过 rateapp:// 从您的 Web 应用触发原生“为此应用评分”对话框，或让 WebViewGold 自动询问。"
lang: "zh"
product: "WebViewGold for Android"
platform: "Android"
category: "API 与功能"
slug: "in-app-rating"
canonical_url: "https://www.webviewgold.com/zh/docs/android/in-app-rating/"
keywords:
  - "应用内评分 API"
  - "WebViewGold for Android"
  - "将网站转换为应用"
  - "WebView 应用文档"
  - "Android WebView SDK"
  - "PWA 转应用"
  - "HTML 转应用"
  - "JavaScript 桥接"
last_updated: "2026-10-09"
---

# 应用内评分对话框 API – WebViewGold for Android

> **摘要：** 请求用户在 Google Play 上评分：通过 rateapp:// 从您的 Web 应用触发原生“为此应用评分”对话框，或让 WebViewGold 自动询问。

[文档](../README.md) › [WebViewGold for Android](README.md) › 应用内评分 API

**平台：** Android · **类别：** API 与功能 · **在线版本：** [www.webviewgold.com/zh/docs/android/in-app-rating/](https://www.webviewgold.com/zh/docs/android/in-app-rating/)

---

Google Play 上的好评是应用增长最有力的推动因素之一。借助 WebViewGold 的**应用内评分对话框 API**，您可以在恰当的时机请求用户评分 — 例如在成功购买后，或用户在您的 Web 应用中完成某项任务之后。

## 方式 1：从 Web 应用手动触发评分对话框

通过 HTML 链接或 JavaScript 调用以下 URL，即可显示原生的"为此应用评分"对话框：

```html
<a href="rateapp://">喜欢这个应用吗？给我们评分吧！</a>
```

```javascript
window.location.href = "rateapp://";
```

用户确认对话框后，会打开您应用的 Google Play 页面，以便留下评价。要使其生效，请在 **Config.java** 中将 `RATE_MY_APP_URL` 设置为您应用的 Google Play URL：

```java
public static final String RATE_MY_APP_URL = "https://play.google.com/store/apps/details?id=com.yourcompany.yourapp";
```

**注意：**如果 `RATE_MY_APP_URL` 为空，`rateapp://` 调用将被忽略。对话框的标题和文字可以通过 **strings.xml** 中的 `rate_title` 和 `rate_message` 条目自定义。

## 方式 2：让 WebViewGold 自动询问

WebViewGold 也可以在用户使用应用一段时间后自动显示"为此应用评分"的提示。请在 **Config.java** 中配置此行为：

- `SHOW_RATE_DIALOG` — 设置为 `true` 启用自动评分提示（设置为 `false` 则禁用）。
- `RATE_DAYS_UNTIL_PROMPT` — 安装后至少经过多少天才显示提示。
- `RATE_LAUNCHES_UNTIL_PROMPT` — 至少启动应用多少次后才显示提示。

## 典型使用场景

- 在积极的互动之后立即请求评价（完成订单、升级、预订成功）。
- 先在您的网站上展示自己的"喜欢这个应用吗？"流程，只将满意的用户引导至 `rateapp://`。

---

## 继续阅读

- ← 上一页： [应用分享对话框 API](app-sharing-dialog.md)
- 下一页 →： [应用内购买 API](in-app-purchases.md)
- 其他平台上的相同功能： [iOS – 应用内评分对话框 API](../ios/in-app-rating.md)
- 语言： [🇺🇸 English](../../android/in-app-rating.md) · [🇩🇪 Deutsch](../../de/android/in-app-rating.md) · [🇫🇷 Français](../../fr/android/in-app-rating.md) · [🇪🇸 Español](../../es/android/in-app-rating.md) · **🇨🇳 中文**

> [!TIP]
> **太忙了？我们替您搭建应用。** 我们的团队为您配置、构建并提交 WebViewGold 应用——全程代劳、交付迅速、德国制造。 [让我们搭建应用 →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_android_doc_online)
>
> **在浏览器中构建：** 无需 Mac、无需 IDE：**WebViewGold Cloud Builder** 在线为您配置、构建并上传应用。 [了解 Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=android_docs)
