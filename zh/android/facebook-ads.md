---
title: "Facebook Audience Network 广告 API – WebViewGold for Android 文档"
description: "在您的 WebViewGold Android 应用中展示 Facebook Audience Network 横幅广告和插页式广告。"
lang: "zh"
product: "WebViewGold for Android"
platform: "Android"
category: "API 与功能"
slug: "facebook-ads"
canonical_url: "https://www.webviewgold.com/zh/docs/android/facebook-ads/"
keywords:
  - "Facebook 广告 API"
  - "WebViewGold for Android"
  - "将网站转换为应用"
  - "WebView 应用文档"
  - "Android WebView SDK"
  - "PWA 转应用"
  - "HTML 转应用"
  - "JavaScript 桥接"
last_updated: "2026-10-09"
---

# Facebook Audience Network 广告 API – WebViewGold for Android

> **摘要：** 在您的 WebViewGold Android 应用中展示 Facebook Audience Network 横幅广告和插页式广告。

[文档](../README.md) › [WebViewGold for Android](README.md) › Facebook 广告 API

**平台：** Android · **类别：** API 与功能 · **在线版本：** [www.webviewgold.com/zh/docs/android/facebook-ads/](https://www.webviewgold.com/zh/docs/android/facebook-ads/)

---

Facebook Audience Network 允许移动应用开发者通过展示广告来通过 iOS 和 Android 应用获利。借助 WebViewGold，您可以轻松地将 Facebook 广告集成到基于 WebView 的 Android 应用中，通过点击（CPC）和展示（CPM）赚取收入。

## 第 1 步：打开 Config.java 文件

- 首先，打开应用的 **Config.java** 文件以配置 Audience Network 设置。

## 第 2 步：启用 Facebook Audience Network 广告

1. **激活必要的配置变量：**
   - 在 Config.java 中将以下变量设置为 `true`：
     - `USE_FACEBOOK_ADS` 让应用使用 Facebook Audience Network 广告而非 AdMob 广告。
     - `SHOW_BANNER_AD` 为您的应用开启横幅广告。
     - `SHOW_FULLSCREEN_AD` 为您的应用开启全屏插页式广告。
   - 将 `SHOW_AD_AFTER_X` 设置为达到目标数量的网站点击后展示插页式广告。

2. **输入您的 Facebook 广告 ID：**
   - 前往 `strings.xml`，将您的唯一 Facebook 广告 ID 添加到相应字段中。

配置上述设置并确认您的广告 ID 后，您的应用现已可以启用 Facebook Audience Network 广告并发布。

如需更多详情，您还可以参阅 [官方 Facebook Audience Network 文档](https://developers.facebook.com/docs/audience-network)，获取针对您广告策略的任何额外设置或优化提示。

[![观看视频: Facebook Audience Network 广告 API](https://img.youtube.com/vi/81wCzuFttic/hqdefault.jpg)](https://www.youtube.com/watch?v=81wCzuFttic)

您还可以通过从您的网站或应用调用以下自定义 URL 方案来**动态**控制用户的广告可见性：

- `enableads://` – 设置为当前用户再次显示广告
- `disableads://` – 永久禁用当前用户的广告

```html
<a href="enableads://">Enable Ads</a>
<a href="disableads://">Disable Ads</a>
```

---

## 继续阅读

- ← 上一页： [AdMob 广告 API](admob.md)
- 下一页 →： [文件下载 API](file-downloader.md)
- 其他平台上的相同功能： [iOS – Facebook 广告 API](../ios/facebook-ads.md)
- 语言： [🇺🇸 English](../../android/facebook-ads.md) · [🇩🇪 Deutsch](../../de/android/facebook-ads.md) · [🇫🇷 Français](../../fr/android/facebook-ads.md) · [🇪🇸 Español](../../es/android/facebook-ads.md) · **🇨🇳 中文**

> [!TIP]
> **太忙了？我们替您搭建应用。** 我们的团队为您配置、构建并提交 WebViewGold 应用——全程代劳、交付迅速、德国制造。 [让我们搭建应用 →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_android_doc_online)
>
> **在浏览器中构建：** 无需 Mac、无需 IDE：**WebViewGold Cloud Builder** 在线为您配置、构建并上传应用。 [了解 Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=android_docs)
