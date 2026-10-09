---
title: "原生侧边栏导航 – WebViewGold for iOS 文档"
description: "启用带有自定义链接和 SF Symbols 图标的原生滑动侧边栏菜单——通过 Sidebar.json 配置。"
lang: "zh"
product: "WebViewGold for iOS"
platform: "iOS"
category: "扩展与插件"
slug: "sidebar"
canonical_url: "https://www.webviewgold.com/zh/docs/iOS/sidebar/"
keywords:
  - "原生侧边栏"
  - "WebViewGold for iOS"
  - "将网站转换为应用"
  - "WebView 应用文档"
  - "iOS WebView SDK"
  - "PWA 转应用"
  - "HTML 转应用"
  - "JavaScript 桥接"
last_updated: "2026-10-09"
---

# 原生侧边栏导航 – WebViewGold for iOS

> **摘要：** 启用带有自定义链接和 SF Symbols 图标的原生滑动侧边栏菜单——通过 Sidebar.json 配置。

[文档](../README.md) › [WebViewGold for iOS](README.md) › 原生侧边栏

**平台：** iOS · **类别：** 扩展与插件 · **在线版本：** [www.webviewgold.com/zh/docs/iOS/sidebar/](https://www.webviewgold.com/zh/docs/iOS/sidebar/)

---

除了[原生导航页脚](navigation-footer.md)之外，WebViewGold 还提供原生的**滑动侧边栏**，让您无需修改网站即可提供类似原生应用的导航体验。一个浮动菜单按钮会打开包含您的链接的侧边栏——每个条目都会让主 WebView 导航到您为其关联的 URL。

## 启用方法

在 **Config.swift** 中设置以下选项：

```swift
var enableSidebar = true
```

## 配置方法

在 Xcode 项目中打开 **Sidebar.json**，定义配色方案和菜单条目：

```json
{
   "colour":"dark",
   "layout":[
      {
         "redirection_link":"https://example.org/home",
         "sf_symbol":"house",
         "name": "首页"
      },
      {
         "redirection_link":"https://example.org/shop",
         "sf_symbol":"cart",
         "name": "商店"
      }
   ]
}
```

| 键 | 说明 |
| --- | --- |
| `colour` | 侧边栏的配色方案：`dark` 或 `light`。 |
| `redirection_link` | 点按条目时在主 WebView 中加载的 URL。 |
| `sf_symbol` | 来自 Apple [SF Symbols](https://developer.apple.com/sf-symbols/) 库的图标名称（例如 `house`、`cart`、`wrench.and.screwdriver`）。 |
| `name` | 侧边栏条目的标签。 |

## 行为

- 浮动按钮在您的 Web 内容上方打开和关闭侧边栏。
- 点按条目会在主 WebView 中加载关联的 URL，因此您的 Web 应用永远不会离开应用外壳。
- 侧边栏可以与[原生导航页脚](navigation-footer.md)组合使用，也可以独立使用。

---

## 继续阅读

- ← 上一页： [原生导航底栏](navigation-footer.md)
- 下一页 →： [屏幕捕获检测](screen-capture.md)
- 语言： [🇺🇸 English](../../ios/sidebar.md) · [🇩🇪 Deutsch](../../de/ios/sidebar.md) · [🇫🇷 Français](../../fr/ios/sidebar.md) · [🇪🇸 Español](../../es/ios/sidebar.md) · **🇨🇳 中文**

> [!TIP]
> **太忙了？我们替您搭建应用。** 我们的团队为您配置、构建并提交 WebViewGold 应用——全程代劳、交付迅速、德国制造。 [让我们搭建应用 →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **在浏览器中构建：** 无需 Mac、无需 IDE：**WebViewGold Cloud Builder** 在线为您配置、构建并上传应用。 [了解 Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
