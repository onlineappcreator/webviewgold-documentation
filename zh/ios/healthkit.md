---
title: "HealthKit 插件 – WebViewGold for iOS 文档"
description: "将您的网页应用连接到 Apple HealthKit，并在 iOS 上经用户授权读取健康数据。"
lang: "zh"
product: "WebViewGold for iOS"
platform: "iOS"
category: "扩展与插件"
slug: "healthkit"
canonical_url: "https://www.webviewgold.com/zh/docs/iOS/healthkit/"
keywords:
  - "HealthKit 插件"
  - "WebViewGold for iOS"
  - "将网站转换为应用"
  - "WebView 应用文档"
  - "iOS WebView SDK"
  - "PWA 转应用"
  - "HTML 转应用"
  - "JavaScript 桥接"
last_updated: "2026-10-09"
---

# HealthKit 插件 – WebViewGold for iOS

> **摘要：** 将您的网页应用连接到 Apple HealthKit，并在 iOS 上经用户授权读取健康数据。

[文档](../README.md) › [WebViewGold for iOS](README.md) › HealthKit 插件

**平台：** iOS · **类别：** 扩展与插件 · **在线版本：** [www.webviewgold.com/zh/docs/iOS/healthkit/](https://www.webviewgold.com/zh/docs/iOS/healthkit/)

---

通过在 `Config.swift` 中的 `static let HealthKitEnabled` 设置您的插件令牌，并添加 HealthKit 功能，以激活 HealthKit 相关功能。\
如需详细信息，请联系 [webviewgold-healthkit@onlineappcreator.com](mailto:webviewgold-healthkit@onlineappcreator.com)。

## API 用法（激活后）

通过调用 `readhealthkit://` 加上 [HealthKit 标识符](https://developer.apple.com/documentation/healthkit/hkquantitytypeidentifier)来**读取** HealthKit 数值。结果会以该标识符命名的 JavaScript 变量注入到您的 Web 应用中（值和单位为字符串）：

```html
<a href="readhealthkit://HKQuantityTypeIdentifierStepCount" onclick="setTimeout(function(){ alert(HKQuantityTypeIdentifierStepCount); }, 500)">读取步数</a>
```

使用 `writehealthkit://标识符//数值` 语法**写入** HealthKit 数值：

```html
<a href="writehealthkit://HKQuantityTypeIdentifierStepCount//100">保存 100 步</a>
```

**注意：**需要 HealthKit 功能以及 **Info.plist** 中的 *Privacy - Health Share Usage Description* / *Privacy - Health Update Usage Description* 条目。

---

## 继续阅读

- ← 上一页： [Siri 插件](siri.md)
- 下一页 →： [构建与发布](publish.md)
- 其他平台上的相同功能： [Android – Health Connect API](../android/health-connect.md)
- 语言： [🇺🇸 English](../../ios/healthkit.md) · [🇩🇪 Deutsch](../../de/ios/healthkit.md) · [🇫🇷 Français](../../fr/ios/healthkit.md) · [🇪🇸 Español](../../es/ios/healthkit.md) · **🇨🇳 中文**

> [!TIP]
> **太忙了？我们替您搭建应用。** 我们的团队为您配置、构建并提交 WebViewGold 应用——全程代劳、交付迅速、德国制造。 [让我们搭建应用 →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **在浏览器中构建：** 无需 Mac、无需 IDE：**WebViewGold Cloud Builder** 在线为您配置、构建并上传应用。 [了解 Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
