---
title: "UUID API – WebViewGold for macOS 文档"
description: "通过 get-uuid:// 将非个人的唯一设备 ID（UUID）传递给 JavaScript，用于识别设备并恢复设置。"
lang: "zh"
product: "WebViewGold for macOS"
platform: "macOS"
category: "API 与功能"
slug: "uuid"
canonical_url: "https://www.webviewgold.com/zh/docs/mac/#uuid"
keywords:
  - "UUID API"
  - "WebViewGold for macOS"
  - "将网站转换为应用"
  - "WebView 应用文档"
  - "macOS WebView SDK"
  - "PWA 转应用"
  - "HTML 转应用"
  - "JavaScript 桥接"
last_updated: "2026-10-09"
---

# UUID API – WebViewGold for macOS

> **摘要：** 通过 get-uuid:// 将非个人的唯一设备 ID（UUID）传递给 JavaScript，用于识别设备并恢复设置。

[文档](../README.md) › [WebViewGold for macOS](README.md) › UUID API

**平台：** macOS · **类别：** API 与功能 · **在线版本：** [www.webviewgold.com/zh/docs/mac/#uuid](https://www.webviewgold.com/zh/docs/mac/#uuid)

---

WebViewGold 允许将**非个人的、唯一的设备 ID**(UUID / “Universally Unique Identifier”)传递给 JavaScript,**可用于唯一识别 macOS 设备**。例如,该 API 可用于在服务器端保存设置或数值,并在客户端恢复它们。如果您使用此 API,请遵守当地及国际的**隐私法规**。

```html
<a href="get-uuid://">Get UDID</a>
<a href="#" onClick="alert(uuid);">Show UDID</a>
```

---

## 继续阅读

- ← 上一页： [In-App Purchases API](in-app-purchases.md)
- 下一页 →： [Deeplinking API](deep-linking.md)
- 其他平台上的相同功能： [iOS – UUID API](../ios/uuid.md) · [Android – UUID API](../android/uuid.md)
- 语言： [🇺🇸 English](../../macos/uuid.md) · [🇩🇪 Deutsch](../../de/macos/uuid.md) · [🇫🇷 Français](../../fr/macos/uuid.md) · [🇪🇸 Español](../../es/macos/uuid.md) · **🇨🇳 中文**

