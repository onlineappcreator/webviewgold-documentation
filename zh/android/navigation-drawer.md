---
title: "Navigation Drawer & Bottom Navigation Footer – WebViewGold for Android 文档"
description: "Ship an app-like navigation experience with the built-in Material navigation drawer and Material 3 bottom navigation bar — no changes to your website required."
lang: "zh"
product: "WebViewGold for Android"
platform: "Android"
category: "应用设计"
slug: "navigation-drawer"
canonical_url: "https://www.webviewgold.com/zh/docs/android/navigation-drawer/"
keywords:
  - "Navigation Drawer & Footer"
  - "WebViewGold for Android"
  - "将网站转换为应用"
  - "WebView 应用文档"
  - "Android WebView SDK"
  - "PWA 转应用"
  - "HTML 转应用"
  - "JavaScript 桥接"
last_updated: "2026-10-09"
---

# Navigation Drawer & Bottom Navigation Footer – WebViewGold for Android

> **摘要：** Ship an app-like navigation experience with the built-in Material navigation drawer and Material 3 bottom navigation bar — no changes to your website required.

[文档](../README.md) › [WebViewGold for Android](README.md) › Navigation Drawer & Footer

**平台：** Android · **类别：** 应用设计 · **在线版本：** [www.webviewgold.com/zh/docs/android/navigation-drawer/](https://www.webviewgold.com/zh/docs/android/navigation-drawer/)

---

WebViewGold 附带两个内置的原生导航 UI，让您无需修改网站即可提供类原生应用的导航体验：侧边**导航抽屉**和 Material 3 **底部导航栏**。两者均为可选，可以组合使用或独立使用。

## 1. 侧边导航抽屉

一个浮动菜单按钮会打开一个包含您的链接的 Material 导航抽屉。在 **Config.java** 中启用：

```java
static boolean ENABLE_NAVIGATION_DRAWER = true;
```

在以下位置配置条目和图标：

```
app/src/main/res/menu/menu_drawer.xml
```

每个 `<item>` 都会成为抽屉中的一行，被点击时会将 WebView 导航到与其关联的 URL。

## 2. 底部导航栏

一个 Material 3 底部导航栏位于屏幕底部，用于在您的顶层部分之间切换。在 **Config.java** 中启用：

```java
static boolean ENABLE_NAVIGATION_FOOTER = true;
```

同一文件（`res/menu/menu_drawer.xml`）驱动这些条目 — 请选择 3–5 个顶层目标。

## 行为

- 两个 UI 都会自动适配设备的深色/浅色模式。
- 图标和标签来自您的菜单 XML。
- 点击一个条目会在主 WebView 中加载关联的 URL，因此您的 Web 应用永远不会离开应用外壳。

**参考：** [Material 3 导航栏指南](https://m3.material.io/components/navigation-bar/overview)。

---

## 继续阅读

- ← 上一页： [启动画面](splash-screen.md)
- 下一页 →： [URL 处理 API](url-handling.md)
- 其他平台上的相同功能： [iOS – 原生导航底栏](../ios/navigation-footer.md)
- 语言： [🇺🇸 English](../../android/navigation-drawer.md) · [🇩🇪 Deutsch](../../de/android/navigation-drawer.md) · [🇫🇷 Français](../../fr/android/navigation-drawer.md) · [🇪🇸 Español](../../es/android/navigation-drawer.md) · **🇨🇳 中文**

> [!TIP]
> **太忙了？我们替您搭建应用。** 我们的团队为您配置、构建并提交 WebViewGold 应用——全程代劳、交付迅速、德国制造。 [让我们搭建应用 →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_android_doc_online)
>
> **在浏览器中构建：** 无需 Mac、无需 IDE：**WebViewGold Cloud Builder** 在线为您配置、构建并上传应用。 [了解 Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=android_docs)
