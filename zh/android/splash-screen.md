---
title: "启动画面 – WebViewGold for Android 文档"
description: "使用您自己的图形自定义 Android WebView 应用的启动画面。"
lang: "zh"
product: "WebViewGold for Android"
platform: "Android"
category: "应用设计"
slug: "splash-screen"
canonical_url: "https://www.webviewgold.com/zh/docs/android/splash-screen/"
keywords:
  - "启动画面"
  - "WebViewGold for Android"
  - "将网站转换为应用"
  - "WebView 应用文档"
  - "Android WebView SDK"
  - "PWA 转应用"
  - "HTML 转应用"
  - "JavaScript 桥接"
last_updated: "2026-10-09"
---

# 启动画面 – WebViewGold for Android

> **摘要：** 使用您自己的图形自定义 Android WebView 应用的启动画面。

[文档](../README.md) › [WebViewGold for Android](README.md) › 启动画面

**平台：** Android · **类别：** 应用设计 · **在线版本：** [www.webviewgold.com/zh/docs/android/splash-screen/](https://www.webviewgold.com/zh/docs/android/splash-screen/)

---

通过在 `Config.java` 中配置以下变量来自定义启动屏行为：

| 选项 | 类型 | 说明 |
| --- | --- | --- |
| SPLASH_SCREEN_ACTIVATED | **true** 或 **false** | 设置为 *true* 以启用启动屏 |
| SPLASH_TIMEOUT | 数字（毫秒） | 如果主页 URL 仍在加载，则在显示加载指示器之前的延迟时间 |
| REMAIN_SPLASH_OPTION | **true** 或 **false** | 为 *true* 时，保持启动屏可见，直到主页 URL 完全加载完成（会覆盖 `SPLASH_TIMEOUT`） |
| SPLASH_MIN_TIME | 数字（毫秒） | 当 `REMAIN_SPLASH_OPTION` 为 *true* 时的最短显示时长；如果实际加载时间超过此值，则忽略此设置 |
| SPLASH_FADE_OUT | 数字（毫秒） | 所有计时器结束后的淡出动画时长；设置为 *0* 可禁用淡出效果 |
| SCALE_SPLASH_IMAGE | 百分比 [0–100] | 相对于设备最小尺寸缩放启动屏图片；*0* 表示隐藏图片 |

## 替换启动屏图片

- 用您自己的方形 GIF（例如 128×128、512×512 或 1024×1024 px）替换 assets 中的 `splash.gif`
- 确保图片尺寸相等（宽 = 高）以获得最佳显示效果
- 在 `colors.xml` 中设置背景颜色

下方视频展示了为您的 Android 应用添加自定义启动屏的步骤：

[![观看视频: 启动画面](https://img.youtube.com/vi/x684JHvW8lI/hqdefault.jpg)](https://www.youtube.com/watch?v=x684JHvW8lI)

---

## 继续阅读

- ← 上一页： [应用图标](app-icon.md)
- 下一页 →： [Navigation Drawer & Footer](navigation-drawer.md)
- 其他平台上的相同功能： [iOS – 名称、图标和启动屏](../ios/app-name-icon-splash.md) · [macOS – 启动画面](../macos/splash-screen.md)
- 语言： [🇺🇸 English](../../android/splash-screen.md) · [🇩🇪 Deutsch](../../de/android/splash-screen.md) · [🇫🇷 Français](../../fr/android/splash-screen.md) · [🇪🇸 Español](../../es/android/splash-screen.md) · **🇨🇳 中文**

> [!TIP]
> **太忙了？我们替您搭建应用。** 我们的团队为您配置、构建并提交 WebViewGold 应用——全程代劳、交付迅速、德国制造。 [让我们搭建应用 →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_android_doc_online)
>
> **在浏览器中构建：** 无需 Mac、无需 IDE：**WebViewGold Cloud Builder** 在线为您配置、构建并上传应用。 [了解 Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=android_docs)
