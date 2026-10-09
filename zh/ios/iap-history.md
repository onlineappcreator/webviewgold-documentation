---
title: "应用内购买历史 API – WebViewGold for iOS 文档"
description: "以 JSON 形式从您的 Web 应用读取用户的历史应用内购买——非常适合“我的购买”页面。"
lang: "zh"
product: "WebViewGold for iOS"
platform: "iOS"
category: "API 与功能"
slug: "iap-history"
canonical_url: "https://www.webviewgold.com/zh/docs/iOS/iap-history/"
keywords:
  - "购买历史 API"
  - "WebViewGold for iOS"
  - "将网站转换为应用"
  - "WebView 应用文档"
  - "iOS WebView SDK"
  - "PWA 转应用"
  - "HTML 转应用"
  - "JavaScript 桥接"
last_updated: "2026-10-09"
---

# 应用内购买历史 API – WebViewGold for iOS

> **摘要：** 以 JSON 形式从您的 Web 应用读取用户的历史应用内购买——非常适合“我的购买”页面。

[文档](../README.md) › [WebViewGold for iOS](README.md) › 购买历史 API

**平台：** iOS · **类别：** API 与功能 · **在线版本：** [www.webviewgold.com/zh/docs/iOS/iap-history/](https://www.webviewgold.com/zh/docs/iOS/iap-history/)

---

**应用内购买历史 API** 返回用户在此设备上通过[应用内购买 API](in-app-purchases.md) 完成的历史购买列表，并将其作为 `window.purchaseHistory` 注入到您的 Web 应用中。如果您计划在最终产品中使用此功能，请确保拥有 WebViewGold 的 [Extended License](credits.md)。

## 使用方法

```html
<a href="getpurchasehistory://" onclick="setTimeout(renderHistory, 300)">我的购买</a>

<script>
function renderHistory() {
  const data = window.purchaseHistory;
  if (!data) return;
  data.purchases.forEach(function (p) {
    console.log(p.productId, p.transactionId, p.purchaseDateMs);
  });
}
</script>
```

## 数据格式

```json
{
  "purchases": [
    {
      "productId": "com.example.premium",
      "transactionId": "2000000123456789",
      "purchaseDateMs": "1721600000000"
    }
  ]
}
```

`purchaseDateMs` 是购买时间的 Unix 毫秒时间戳（字符串形式）。

## 典型使用场景

- 在您的 Web 应用中显示“我的订阅”或“我的购买”页面。
- 基于历史购买在客户端解锁高级内容，无需请求您的后端。
- 调试和客户支持工作流。

**注意：**该列表包含在此设备上于应用内完成的购买。数据存储在本地，不会跨设备同步——如需跨设备的权益校验，请改为在您的服务器上验证收据。

---

## 继续阅读

- ← 上一页： [应用内购买 API](in-app-purchases.md)
- 下一页 →： [QR 码扫描 API](qr-code-scanner.md)
- 其他平台上的相同功能： [Android – IAP History API](../android/iap-history.md)
- 语言： [🇺🇸 English](../../ios/iap-history.md) · [🇩🇪 Deutsch](../../de/ios/iap-history.md) · [🇫🇷 Français](../../fr/ios/iap-history.md) · [🇪🇸 Español](../../es/ios/iap-history.md) · **🇨🇳 中文**

> [!TIP]
> **太忙了？我们替您搭建应用。** 我们的团队为您配置、构建并提交 WebViewGold 应用——全程代劳、交付迅速、德国制造。 [让我们搭建应用 →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **在浏览器中构建：** 无需 Mac、无需 IDE：**WebViewGold Cloud Builder** 在线为您配置、构建并上传应用。 [了解 Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
