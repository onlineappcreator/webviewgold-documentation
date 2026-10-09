---
title: "UUID API – WebViewGold for Android 文档"
description: "通过附加到 WebView URL 或经由 JavaScript 获取的唯一 UUID 来识别应用安装。"
lang: "zh"
product: "WebViewGold for Android"
platform: "Android"
category: "API 与功能"
slug: "uuid"
canonical_url: "https://www.webviewgold.com/zh/docs/android/uuid/"
keywords:
  - "UUID API"
  - "WebViewGold for Android"
  - "将网站转换为应用"
  - "WebView 应用文档"
  - "Android WebView SDK"
  - "PWA 转应用"
  - "HTML 转应用"
  - "JavaScript 桥接"
last_updated: "2026-10-09"
---

# UUID API – WebViewGold for Android

> **摘要：** 通过附加到 WebView URL 或经由 JavaScript 获取的唯一 UUID 来识别应用安装。

[文档](../README.md) › [WebViewGold for Android](README.md) › UUID API

**平台：** Android · **类别：** API 与功能 · **在线版本：** [www.webviewgold.com/zh/docs/android/uuid/](https://www.webviewgold.com/zh/docs/android/uuid/)

---

WebViewGold UUID API 允许您通过 JavaScript 获取一个非个人化的唯一设备 ID（UUID，即 "Universally Unique Identifier"，通用唯一标识符），它可以唯一标识一台 Android 设备。此功能在以下场景中很有帮助：

- 在服务器上存储用户专属设置
- 维护会话状态
- 在客户端调用已保存的数据

**隐私注意事项：**由于此功能涉及设备识别，请确保在使用时遵守当地及国际的隐私法律法规。

## 如何获取 UUID

要从基于 WebView 的应用中获取 UUID，请使用以下代码：

```html
<a href="get-uuid://">Get UUID</a>
<a href="#" onClick="alert(uuid);">Show UUID</a>
```

- **Get UUID：**向 WebViewGold 请求 UUID。
- **Show UUID：**通过 **alert** 弹窗显示 UUID，便于测试。

## 备选方法：将 UUID 追加到 WebView URL 中

如果您希望将 UUID 包含在 URL 参数中，请在 **Config.java** 中将 `UUID_ENHANCE_WEBVIEW_URL` 选项设置为 `true`。这样，在首次请求时会自动将 `uuid=XYZ` 追加到您的 WebView URL 上，使您可以直接在网页内容中访问 UUID：

- **示例：**如果您的 WebView URL 为 `https://www.example.org`，则它将以 `https://www.example.org?uuid=XYZ` 的形式发起请求。
- **注意：**只有首次 URL 请求会包含此 GET 参数，因此如果您需要稍后在应用中引用它，请考虑将其保存到会话或 cookie 中。

## 自动将 UUID 注入 JavaScript

要在所有页面中自动使 UUID（以及其他变量）在 JavaScript 中可用，而无需修改 URL，请在 **Config.java** 中将 `AUTO_INJECT_VARIABLES` 设置为 `true`。这样您就可以在任何页面中直接访问 UUID 及其他值。

---

## 继续阅读

- ← 上一页： [剪贴板 API](clipboard.md)
- 下一页 →： [手电筒 API](flashlight.md)
- 其他平台上的相同功能： [iOS – UUID API](../ios/uuid.md) · [macOS – UUID API](../macos/uuid.md)
- 语言： [🇺🇸 English](../../android/uuid.md) · [🇩🇪 Deutsch](../../de/android/uuid.md) · [🇫🇷 Français](../../fr/android/uuid.md) · [🇪🇸 Español](../../es/android/uuid.md) · **🇨🇳 中文**

> [!TIP]
> **太忙了？我们替您搭建应用。** 我们的团队为您配置、构建并提交 WebViewGold 应用——全程代劳、交付迅速、德国制造。 [让我们搭建应用 →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_android_doc_online)
>
> **在浏览器中构建：** 无需 Mac、无需 IDE：**WebViewGold Cloud Builder** 在线为您配置、构建并上传应用。 [了解 Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=android_docs)
