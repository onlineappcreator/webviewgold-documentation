---
title: "原生导航底栏 – WebViewGold for iOS 文档"
description: "在您的 iOS 应用中启用带有后退、前进和自定义按钮的原生底部导航栏。"
lang: "zh"
product: "WebViewGold for iOS"
platform: "iOS"
category: "扩展与插件"
slug: "navigation-footer"
canonical_url: "https://www.webviewgold.com/zh/docs/iOS/navigation-footer/"
keywords:
  - "原生导航底栏"
  - "WebViewGold for iOS"
  - "将网站转换为应用"
  - "WebView 应用文档"
  - "iOS WebView SDK"
  - "PWA 转应用"
  - "HTML 转应用"
  - "JavaScript 桥接"
last_updated: "2026-10-09"
---

# 原生导航底栏 – WebViewGold for iOS

> **摘要：** 在您的 iOS 应用中启用带有后退、前进和自定义按钮的原生底部导航栏。

[文档](../README.md) › [WebViewGold for iOS](README.md) › 原生导航底栏

**平台：** iOS · **类别：** 扩展与插件 · **在线版本：** [www.webviewgold.com/zh/docs/iOS/navigation-footer/](https://www.webviewgold.com/zh/docs/iOS/navigation-footer/)

---

在 `Config.swift` 中设置 `var showNavFooter = true` 以启用原生导航页脚栏。在 `FooterBar.json` 中配置按钮和链接。示例：

```json
{
   "colour":"dark",
   "layout":[
      {
         "redirection_link":"https://webviewgoldtest.github.io/index.html",
         "sf_symbol":"house",
         "name": "Home"
      },
      {
         "redirection_link":"https://webviewgoldtest.github.io/appControls.html",
         "sf_symbol":"wrench.and.screwdriver",
         "name": "Controls"
      },
      {
         "redirection_link":"https://webviewgoldtest.github.io/NFCtesting.html",
         "sf_symbol":"wifi.square",
         "name": "NFC"
      },
      {
         "redirection_link":"https://webviewgoldtest.github.io/IAPtesting.html",
         "sf_symbol":"cart",
         "name": "Purchases"
      },
      {
         "redirection_link":"https://webviewgoldtest.github.io/permissions.html",
         "sf_symbol":"lock.open",
         "name": "Permissions"
      }
   ]
}
```

每个 `sf_symbol` 都使用一个 [SF Symbol](https://developer.apple.com/sf-symbols/)，并在主 WebView 中打开对应的 `redirection_link`。

---

## 继续阅读

- ← 上一页： [App Clip Extension](app-clip.md)
- 下一页 →： [原生侧边栏](sidebar.md)
- 其他平台上的相同功能： [Android – Navigation Drawer & Footer](../android/navigation-drawer.md)
- 语言： [🇺🇸 English](../../ios/navigation-footer.md) · [🇩🇪 Deutsch](../../de/ios/navigation-footer.md) · [🇫🇷 Français](../../fr/ios/navigation-footer.md) · [🇪🇸 Español](../../es/ios/navigation-footer.md) · **🇨🇳 中文**

> [!TIP]
> **太忙了？我们替您搭建应用。** 我们的团队为您配置、构建并提交 WebViewGold 应用——全程代劳、交付迅速、德国制造。 [让我们搭建应用 →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **在浏览器中构建：** 无需 Mac、无需 IDE：**WebViewGold Cloud Builder** 在线为您配置、构建并上传应用。 [了解 Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
