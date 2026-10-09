---
title: "UUID API – WebViewGold for iOS 文档"
description: "通过附加到 WebView URL 或经由 JavaScript 获取的唯一 UUID 来识别应用安装。"
lang: "zh"
product: "WebViewGold for iOS"
platform: "iOS"
category: "API 与功能"
slug: "uuid"
canonical_url: "https://www.webviewgold.com/zh/docs/iOS/uuid/"
keywords:
  - "UUID API"
  - "WebViewGold for iOS"
  - "将网站转换为应用"
  - "WebView 应用文档"
  - "iOS WebView SDK"
  - "PWA 转应用"
  - "HTML 转应用"
  - "JavaScript 桥接"
last_updated: "2026-10-09"
---

# UUID API – WebViewGold for iOS

> **摘要：** 通过附加到 WebView URL 或经由 JavaScript 获取的唯一 UUID 来识别应用安装。

[文档](../README.md) › [WebViewGold for iOS](README.md) › UUID API

**平台：** iOS · **类别：** API 与功能 · **在线版本：** [www.webviewgold.com/zh/docs/iOS/uuid/](https://www.webviewgold.com/zh/docs/iOS/uuid/)

---

WebViewGold UUID API 允许您获取一个非个人化的唯一设备 ID（UUID，即 “Universally Unique Identifier”，通用唯一标识符），可用于**唯一标识一台 iOS 设备**。此功能适用的场景包括：

- 在服务器端存储用户特定设置
- 维护会话状态
- 在客户端读取已保存的数据

**隐私提示：**使用此功能时，请确保遵守当地及国际的**隐私法律法规**，因为它涉及设备识别。

## 如何获取 UUID

如需在基于 WebView 的应用中获取 UUID，请使用以下代码：

```html
<a href="get-uuid://">Get UUID</a>
<a href="#" onClick="alert(uuid);">Show UUID</a>
```

- **Get UUID：**向 WebViewGold 请求 UUID。
- **Show UUID：**通过 **alert** 弹窗显示 UUID，方便测试。

## 替代方式：将 UUID 追加到 WebView URL

如果您希望将 UUID 包含在 URL 参数中，请在 **Config.swift** 中启用 `enhanceUrlUUID` 选项，并将其设置为 `true`。这样，在首次请求时会自动向 WebView URL 追加 `uuid=XYZ`，让您可以直接在 Web 内容中获取 UUID：

- **示例：**如果您的 WebView URL 为 `https://www.example.org`，则实际请求将变为 `https://www.example.org?uuid=XYZ`。
- **注意：**仅首次 URL 请求会包含此 GET 参数，因此如果您需要在应用中稍后再引用它，请考虑将其保存到会话或 Cookie 中。

## 自动将 UUID 注入到 JavaScript

要在所有页面中自动使 UUID（以及其他变量）在 JavaScript 中可用，而无需修改 URL，请在 **Config.swift** 中将 `autoInjectVariable` 设置为 `true`。这样，您就可以在任何页面中直接访问 UUID 及其他值。

---

## 继续阅读

- ← 上一页： [Apple Wallet 凭证 API](wallet-pass.md)
- 下一页 →： [手电筒 API](flashlight.md)
- 其他平台上的相同功能： [Android – UUID API](../android/uuid.md) · [macOS – UUID API](../macos/uuid.md)
- 语言： [🇺🇸 English](../../ios/uuid.md) · [🇩🇪 Deutsch](../../de/ios/uuid.md) · [🇫🇷 Français](../../fr/ios/uuid.md) · [🇪🇸 Español](../../es/ios/uuid.md) · **🇨🇳 中文**

> [!TIP]
> **太忙了？我们替您搭建应用。** 我们的团队为您配置、构建并提交 WebViewGold 应用——全程代劳、交付迅速、德国制造。 [让我们搭建应用 →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **在浏览器中构建：** 无需 Mac、无需 IDE：**WebViewGold Cloud Builder** 在线为您配置、构建并上传应用。 [了解 Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
