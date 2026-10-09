---
title: "In-App Purchase 与 In-App Subscription API – WebViewGold for macOS 文档"
description: "从您的 Web 应用销售 Mac App Store 应用内购买和订阅：在 Constants.h 中添加产品 ID，并通过 inapppurchase:// 链接触发购买。"
lang: "zh"
product: "WebViewGold for macOS"
platform: "macOS"
category: "API 与功能"
slug: "in-app-purchases"
canonical_url: "https://www.webviewgold.com/zh/docs/mac/#inapppurchases"
keywords:
  - "In-App Purchases API"
  - "WebViewGold for macOS"
  - "将网站转换为应用"
  - "WebView 应用文档"
  - "macOS WebView SDK"
  - "PWA 转应用"
  - "HTML 转应用"
  - "JavaScript 桥接"
last_updated: "2026-10-09"
---

# In-App Purchase 与 In-App Subscription API – WebViewGold for macOS

> **摘要：** 从您的 Web 应用销售 Mac App Store 应用内购买和订阅：在 Constants.h 中添加产品 ID，并通过 inapppurchase:// 链接触发购买。

[文档](../README.md) › [WebViewGold for macOS](README.md) › In-App Purchases API

**平台：** macOS · **类别：** API 与功能 · **在线版本：** [www.webviewgold.com/zh/docs/mac/#inapppurchases](https://www.webviewgold.com/zh/docs/mac/#inapppurchases)

---

在部分 macOS/Mac 应用中,您可以购买额外的内容或服务。这类购买被称为“in-app purchases”(应用内购买)。它们可以成为开发者极具吸引力的收入来源,对客户也非常方便,因为使用现有账户和支付方式即可完成结算。WebViewGold 允许触发 Mac App Store 的 In-App Purchases。只需在 *Constants.h* 文件中添加您从 *App Store Connect* 获得的 In-App Purchase Product ID: \
![Constants.h 文件中的 Mac App Store In-App Purchase Product ID](../../assets/macos/img/inapppurchase.png)\
随后,只需链接到如下 URL 即可:

```html
<a href="inapppurchase://?successful_url=https://www.google.com">Buy In-App Purchase</a>
```

对于订阅产品,也可以使用此类 URL:

```html
<a href="inappsubscription://?successful_url=https://www.google.com&expired_url=https://www.yahoo.com">Start In-App Subscription</a>
```

在此 URL 示例中,订阅成功激活后应调用 https://www.google.com,一旦订阅到期就应调用 https://www.yahoo.com。

---

## 继续阅读

- ← 上一页： [启动画面](splash-screen.md)
- 下一页 →： [UUID API](uuid.md)
- 其他平台上的相同功能： [iOS – 应用内购买 API](../ios/in-app-purchases.md) · [Android – 应用内购买 API](../android/in-app-purchases.md)
- 语言： [🇺🇸 English](../../macos/in-app-purchases.md) · [🇩🇪 Deutsch](../../de/macos/in-app-purchases.md) · [🇫🇷 Français](../../fr/macos/in-app-purchases.md) · [🇪🇸 Español](../../es/macos/in-app-purchases.md) · **🇨🇳 中文**

