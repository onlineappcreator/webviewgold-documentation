---
title: "In-App Purchase History API – WebViewGold for Android 文档"
description: "Return the user's Google Play purchase history as window.purchaseHistory so your web app can list subscriptions or unlock premium content client-side."
lang: "zh"
product: "WebViewGold for Android"
platform: "Android"
category: "API 与功能"
slug: "iap-history"
canonical_url: "https://www.webviewgold.com/zh/docs/android/iap-history/"
keywords:
  - "IAP History API"
  - "WebViewGold for Android"
  - "将网站转换为应用"
  - "WebView 应用文档"
  - "Android WebView SDK"
  - "PWA 转应用"
  - "HTML 转应用"
  - "JavaScript 桥接"
last_updated: "2026-10-09"
---

# In-App Purchase History API – WebViewGold for Android

> **摘要：** Return the user's Google Play purchase history as window.purchaseHistory so your web app can list subscriptions or unlock premium content client-side.

[文档](../README.md) › [WebViewGold for Android](README.md) › IAP History API

**平台：** Android · **类别：** API 与功能 · **在线版本：** [www.webviewgold.com/zh/docs/android/iap-history/](https://www.webviewgold.com/zh/docs/android/iap-history/)

---

**应用内购买历史 API** 返回用户之前通过 Google Play Billing 进行的购买记录列表（产品 ID、时间戳、令牌），并将其作为 `window.purchaseHistory` 注入到您的 Web 应用中。如果您打算在最终产品中使用此功能，请确保拥有 WebViewGold 的[扩展许可证](credits.md)。

## 使用方法

```html
<a href="getpurchasehistory://" onclick="setTimeout(renderHistory, 300)">My purchases</a>

<script>
function renderHistory() {
  const data = window.purchaseHistory;
  if (!data) return;
  data.purchases.forEach(function (p) {
    console.log(p.productId, p.purchaseTime, p.orderId);
  });
}
</script>
```

## 载荷结构

```json
{
  "purchases": [
    {
      "productId": "com.example.premium",
      "purchaseTime": 1721600000000,
      "orderId": "GPA.xxxx-xxxx-xxxx",
      "purchaseToken": "..."
    }
  ]
}
```

确切的字段取决于商店记录 — 请将该值视为可迭代的 JSON 数组。

## 典型用例

- 在您的 Web 应用内显示"我的订阅"或"我的购买"页面。
- 基于过往购买记录在客户端解锁高级内容，而无需请求您的后端。
- 调试和客户支持工作流程。

**说明：** 列表仅包含在此设备上当前登录的 Google Play 账户下进行的购买。

---

## 继续阅读

- ← 上一页： [应用内购买 API](in-app-purchases.md)
- 下一页 →： [QR 码扫描 API](qr-code-scanner.md)
- 其他平台上的相同功能： [iOS – 购买历史 API](../ios/iap-history.md)
- 语言： [🇺🇸 English](../../android/iap-history.md) · [🇩🇪 Deutsch](../../de/android/iap-history.md) · [🇫🇷 Français](../../fr/android/iap-history.md) · [🇪🇸 Español](../../es/android/iap-history.md) · **🇨🇳 中文**

> [!TIP]
> **太忙了？我们替您搭建应用。** 我们的团队为您配置、构建并提交 WebViewGold 应用——全程代劳、交付迅速、德国制造。 [让我们搭建应用 →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_android_doc_online)
>
> **在浏览器中构建：** 无需 Mac、无需 IDE：**WebViewGold Cloud Builder** 在线为您配置、构建并上传应用。 [了解 Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=android_docs)
