---
title: "AdMob 广告 API – WebViewGold for Android 文档"
description: "使用 Google AdMob 横幅广告和插页式广告让您的 Android 应用实现变现——配置与 JavaScript 触发器。"
lang: "zh"
product: "WebViewGold for Android"
platform: "Android"
category: "API 与功能"
slug: "admob"
canonical_url: "https://www.webviewgold.com/zh/docs/android/admob/"
keywords:
  - "AdMob 广告 API"
  - "WebViewGold for Android"
  - "将网站转换为应用"
  - "WebView 应用文档"
  - "Android WebView SDK"
  - "PWA 转应用"
  - "HTML 转应用"
  - "JavaScript 桥接"
last_updated: "2026-10-09"
---

# AdMob 广告 API – WebViewGold for Android

> **摘要：** 使用 Google AdMob 横幅广告和插页式广告让您的 Android 应用实现变现——配置与 JavaScript 触发器。

[文档](../README.md) › [WebViewGold for Android](README.md) › AdMob 广告 API

**平台：** Android · **类别：** API 与功能 · **在线版本：** [www.webviewgold.com/zh/docs/android/admob/](https://www.webviewgold.com/zh/docs/android/admob/)

---

AdMob 是一项 Google 服务，用于通过 iOS 和 Android 平台上的移动应用获利。它允许开发人员集成横幅广告、插页式广告和奖励广告，这些广告按点击次数（CPC，每次点击成本）或展示次数（CPM，每千次成本）付费。 WebViewGold 简化了 AdMob 集成，支持快速设置以在基于 WebView 的 Android 应用程序中显示广告。

## 第 1 步：打开 Config.java 文件

首先，打开您应用的 **Config.java** 文件以设置广告首选项并激活 AdMob 功能。

## 第 2 步：使用原生 AdMob SDK 通过您的应用获利

在 **Config.java** 中，您可以：

- **启用或禁用**横幅广告和/或插页式广告：将 `SHOW_BANNER_AD` 设置为 true 以启用横幅广告，将 `SHOW_FULL_SCREEN_AD` 设置为 true 以启用插页式广告。
- **定义展示间隔**：将 `SHOW_AD_AFTER_X` 更改为您希望的网站互动次数，达到该次数后即可播放插页式广告。

**注意：** 在启动您的应用之前，请确保您的唯一 AdMob ID 已正确添加到 **strings.xml** 文件：\
![Enable specific AdMob ad blocs in your app](../../assets/android/img/admobconfig.webp)

## 第 3 步：启用激励广告

- 设置奖励广告：
  - 要启用激励广告，请将 `ENABLE_REWARDED_ADS` 设置为 `true`。
  - 使用以下链接展示激励广告

    ```html
    <a href="displayrewardedad://">Display Rewarded Advertisement</a>
    ```

  - 一旦用户完成查看广告，WebViewGold 就会触发 JavaScript 函数 `updateRewardedStatus('true');` 以便您在应用程序代码中处理奖励。
- 默认奖励广告：
  - 如果您希望默认显示激励广告，请同时将 `USE_REWARDED_ADS_WHERE_POSSIBLE` 和 `SHOW_FULL_SCREEN_AD` 设置为 `true`。这将优先展示激励广告而非插页式广告。

## 其他资源

有关更详细的选项，请参阅 [官方 AdMob SDK 文档](https://developers.google.com/admob/)，但请跳过设置说明，因为 WebViewGold 已包含必要的框架。

[![观看视频: AdMob 广告 API](https://img.youtube.com/vi/vq5FM7n0Syg/hqdefault.jpg)](https://www.youtube.com/watch?v=vq5FM7n0Syg)

您还可以通过从您的网站或应用程序调用以下自定义 URL 方案来**动态**控制用户的广告可见性：

- `enableads://` – 设置为当前用户再次显示的广告
- `disableads://` – 永久禁用当前用户的广告

## <a id="appopenads"></a>第 4 步：启用 App Open 广告

**App Open 广告**是在用户打开应用（从启动器闪屏冷启动）或从后台返回应用时显示的全屏广告。启用方法：

- 在 **Config.java** 中将 `SHOW_APP_OPEN_AD` 设置为 `true`。
- 将 **strings.xml** 中的 `admob_app_open_id` 值替换为您自己的 AdMob App Open 广告单元 ID（模板中包含 AdMob 官方测试 ID — 请在发布前替换！）。

**注意：**App Open 广告与其他 AdMob 格式一样，遵循 Google 同意管理设置（`ASK_FOR_AD_CONSENT`）。

---

## 继续阅读

- ← 上一页： [推送通知 API](push-notifications.md)
- 下一页 →： [Facebook 广告 API](facebook-ads.md)
- 其他平台上的相同功能： [iOS – AdMob 广告 API](../ios/admob.md)
- 语言： [🇺🇸 English](../../android/admob.md) · [🇩🇪 Deutsch](../../de/android/admob.md) · [🇫🇷 Français](../../fr/android/admob.md) · [🇪🇸 Español](../../es/android/admob.md) · **🇨🇳 中文**

> [!TIP]
> **太忙了？我们替您搭建应用。** 我们的团队为您配置、构建并提交 WebViewGold 应用——全程代劳、交付迅速、德国制造。 [让我们搭建应用 →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_android_doc_online)
>
> **在浏览器中构建：** 无需 Mac、无需 IDE：**WebViewGold Cloud Builder** 在线为您配置、构建并上传应用。 [了解 Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=android_docs)
