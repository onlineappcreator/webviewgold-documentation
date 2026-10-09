---
title: "Facebook Audience Network 广告 API – WebViewGold for iOS 文档"
description: "在您的 WebViewGold iOS 应用中展示 Facebook Audience Network 横幅和插屏广告。"
lang: "zh"
product: "WebViewGold for iOS"
platform: "iOS"
category: "API 与功能"
slug: "facebook-ads"
canonical_url: "https://www.webviewgold.com/zh/docs/iOS/facebook-ads/"
keywords:
  - "Facebook 广告 API"
  - "WebViewGold for iOS"
  - "将网站转换为应用"
  - "WebView 应用文档"
  - "iOS WebView SDK"
  - "PWA 转应用"
  - "HTML 转应用"
  - "JavaScript 桥接"
last_updated: "2026-10-09"
---

# Facebook Audience Network 广告 API – WebViewGold for iOS

> **摘要：** 在您的 WebViewGold iOS 应用中展示 Facebook Audience Network 横幅和插屏广告。

[文档](../README.md) › [WebViewGold for iOS](README.md) › Facebook 广告 API

**平台：** iOS · **类别：** API 与功能 · **在线版本：** [www.webviewgold.com/zh/docs/iOS/facebook-ads/](https://www.webviewgold.com/zh/docs/iOS/facebook-ads/)

---

[Facebook Audience Network](https://www.facebook.com/audiencenetwork/) 允许移动应用开发者通过展示广告来变现 iOS 和 Android 应用。借助 WebViewGold，您可以轻松地将 Facebook 广告整合到基于 WebView 的 iOS 应用中，通过点击（CPC）和曝光（CPM）获得收益。

## 步骤 1：创建 Facebook Audience Network 账户

您必须先创建一个 [Facebook Audience Network](https://www.facebook.com/audiencenetwork/) 账户，并在 Monetization Manager 的 Integration 下创建一个 property。然后关联一个 iOS 应用（不过用于测试时，无需关联到已发布的 iOS 应用）。

请参考此指南：<https://www.facebook.com/business/help/191133327919314>

## 步骤 2：设置必要的配置变量

- 打开 **Config.swift**，将 `useFacebookAds` 设置为 `true`。
- 在 `facebookAdsID` 中输入您的 Facebook Placement ID。

![Facebook Ads 配置截图](../../assets/ios/img/fbadsconfig.webp)

## 步骤 3：配置广告设置

- 要使用定时广告，请将 `useTimedAds` 设置为 `true`，并将 `showFBAdsEveryNSeconds` 设置为广告之间所需的时间间隔。
- 您可以将 URL 触发词添加到 `fbadstriggerurls`，以便按需初始化广告。

## 其他注意事项

- 必须使用真实的 iOS 设备进行测试（不能使用模拟器）
- 该设备必须添加为测试设备，请参见 <https://developers.facebook.com/docs/audience-network/setting-up/testing/platform>
- 设备上必须已安装并登录 Facebook
- 必须禁用「限制广告跟踪」或未来 iOS 版本中可能推出的任何类似设置。

---

## 继续阅读

- ← 上一页： [AdMob 广告 API](admob.md)
- 下一页 →： [HTML 音频 API](html-audio.md)
- 其他平台上的相同功能： [Android – Facebook 广告 API](../android/facebook-ads.md)
- 语言： [🇺🇸 English](../../ios/facebook-ads.md) · [🇩🇪 Deutsch](../../de/ios/facebook-ads.md) · [🇫🇷 Français](../../fr/ios/facebook-ads.md) · [🇪🇸 Español](../../es/ios/facebook-ads.md) · **🇨🇳 中文**

> [!TIP]
> **太忙了？我们替您搭建应用。** 我们的团队为您配置、构建并提交 WebViewGold 应用——全程代劳、交付迅速、德国制造。 [让我们搭建应用 →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **在浏览器中构建：** 无需 Mac、无需 IDE：**WebViewGold Cloud Builder** 在线为您配置、构建并上传应用。 [了解 Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
