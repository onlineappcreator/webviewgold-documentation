---
title: "快捷方式 API – WebViewGold for iOS 文档"
description: "为您的 iOS 应用添加主屏幕快速操作快捷方式，深度链接到特定页面。"
lang: "zh"
product: "WebViewGold for iOS"
platform: "iOS"
category: "API 与功能"
slug: "shortcut"
canonical_url: "https://www.webviewgold.com/zh/docs/iOS/shortcut/"
keywords:
  - "快捷方式 API"
  - "WebViewGold for iOS"
  - "将网站转换为应用"
  - "WebView 应用文档"
  - "iOS WebView SDK"
  - "PWA 转应用"
  - "HTML 转应用"
  - "JavaScript 桥接"
last_updated: "2026-10-09"
---

# 快捷方式 API – WebViewGold for iOS

> **摘要：** 为您的 iOS 应用添加主屏幕快速操作快捷方式，深度链接到特定页面。

[文档](../README.md) › [WebViewGold for iOS](README.md) › 快捷方式 API

**平台：** iOS · **类别：** API 与功能 · **在线版本：** [www.webviewgold.com/zh/docs/iOS/shortcut/](https://www.webviewgold.com/zh/docs/iOS/shortcut/)

---

在 `Config.swift` 中启用 `var useShortcuts = true`，即可注册在 `Shortcuts.json` 中定义的动态快捷方式。每个快捷方式都可以打开一个 URL、注入 JavaScript，并显示一个 SF Symbol 图标。示例：

```json
{
    "shortcuts": [
        {
            "title": "Open Google",
            "redirection_link": "https://google.com",
            "injection": "",
            "symbol": "wrench.and.screwdriver"
        },
        {
            "title": "Open & Inject",
            "redirection_link": "https://apple.com",
            "injection": "(function() { console.log('Injected and executed!'); })();",
            "symbol": "lock.open"
        }
    ]
}
```

用户可通过长按应用图标访问这些快捷方式。

---

## 继续阅读

- ← 上一页： [触觉反馈 API](haptic-feedback.md)
- 下一页 →： [剪贴板 API](clipboard.md)
- 语言： [🇺🇸 English](../../ios/shortcut.md) · [🇩🇪 Deutsch](../../de/ios/shortcut.md) · [🇫🇷 Français](../../fr/ios/shortcut.md) · [🇪🇸 Español](../../es/ios/shortcut.md) · **🇨🇳 中文**

> [!TIP]
> **太忙了？我们替您搭建应用。** 我们的团队为您配置、构建并提交 WebViewGold 应用——全程代劳、交付迅速、德国制造。 [让我们搭建应用 →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **在浏览器中构建：** 无需 Mac、无需 IDE：**WebViewGold Cloud Builder** 在线为您配置、构建并上传应用。 [了解 Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
