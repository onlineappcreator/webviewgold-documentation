---
title: "应用内购买 API – WebViewGold for Android 文档"
description: "使用 Google Play Billing 在您的 Android WebView 应用中销售数字商品和订阅。"
lang: "zh"
product: "WebViewGold for Android"
platform: "Android"
category: "API 与功能"
slug: "in-app-purchases"
canonical_url: "https://www.webviewgold.com/zh/docs/android/in-app-purchases/"
keywords:
  - "应用内购买 API"
  - "WebViewGold for Android"
  - "将网站转换为应用"
  - "WebView 应用文档"
  - "Android WebView SDK"
  - "PWA 转应用"
  - "HTML 转应用"
  - "JavaScript 桥接"
last_updated: "2026-10-09"
---

# 应用内购买 API – WebViewGold for Android

> **摘要：** 使用 Google Play Billing 在您的 Android WebView 应用中销售数字商品和订阅。

[文档](../README.md) › [WebViewGold for Android](README.md) › 应用内购买 API

**平台：** Android · **类别：** API 与功能 · **在线版本：** [www.webviewgold.com/zh/docs/android/in-app-purchases/](https://www.webviewgold.com/zh/docs/android/in-app-purchases/)

---

在某些应用中，您可以购买额外的内容或服务。这类购买称为"应用内购买"。对开发者而言，它们可以是一种颇具吸引力的收入来源；对客户而言也非常便利，因为可以直接使用现有账户和支付方式完成结算。WebViewGold 允许触发 Google Play 应用内购买。如果您计划在最终产品中使用此功能，请确保拥有 WebViewGold 的[扩展许可证](credits.md)。需要升级？[在此了解如何升级](https://help.market.envato.com/hc/en-us/articles/115005593503-If-I-choose-the-wrong-license-or-need-to-upgrade-my-license-how-easy-is-it-to-change-to-the-correct-license)。

**方案 1（默认）：RevenueCat**\
创建您的免费 [RevenueCat 账户](https://tinyurl.com/register-revenuecat)开始使用。定价信息可在其网站上查看。然后按照其安装向导和文档设置 RevenueCat（定价详情可在其[网站](https://tinyurl.com/register-revenuecat)上查看）。之后，将您的详细信息添加到 **Config.java** 中。此方案同样支持 Google Play 商店的 [15% Service Fee Tier Program](https://support.google.com/googleplay/android-developer/answer/112622?hl=en) 和 Apple 的 [Small Business Program](https://developer.apple.com/app-store/small-business-program/)。如果您参与了这些低费率计划，请通过 RevenueCat 的 [Apple Small Business Program](https://www.revenuecat.com/docs/platform-resources/apple-platform-resources/app-store-small-business-program) 或 [Google 15% reduced service fee](https://www.revenuecat.com/docs/platform-resources/google-platform-resources/15-reduced-service-fee) 页面告知 RevenueCat。Config.java 中的设置如下所示：

```java
public static final String REVENUECAT_API_KEY = "xxxxxxxsxxxxxxxxxxxxxxxxxxxxxxxxxx"; //Your RevenueCat API Key (sign up via tinyurl.com/register-revenuecat first, then follow tinyurl.com/api-key-revenuecat how to find it)
public static final String REVENUECAT_PROJECT_ID = "xxxxxxx"; //Your RevenueCat Project ID (sign up via tinyurl.com/register-revenuecat first, then follow tinyurl.com/project-id-revenuecat how to find it)
```

请确保 APK 和 Google Play Console 中的包名与 RevenueCat 中配置的项目一致。使用以下方式触发购买或订阅：

```
revenuecat://purchase?external_id=user_123&product=sub_30_days
```

`external_id` = 用户标识符，例如客户的邮箱地址或用户 ID。`product` = 显示在 RevenueCat 控制台中的 ID。同时适用于 Android 和 iOS。

## 方案 2：手动（不使用 RevenueCat）

我们致力于帮助 WebViewGold 客户取得成功，并希望提请您注意 Google Play 商店的 15% Service Fee Tier Program 和 Apple 的 Small Business Program。这些计划允许符合资格的开发者获得 15% 的佣金比例，比标准的 30% 大幅降低。申请快速简便，通过**将 Google 和 Apple 的佣金比例从 30% 降至 15%**，有可能为您节省 50% 的费用。一旦获得批准，您将在相应商店的所有付费应用和应用内购买中享受降低后的佣金比例。要详细了解 Google Play 计划，请点击**[此处](https://support.google.com/googleplay/android-developer/answer/112622?hl=en)**；要了解 Apple 计划，请访问**[此处](https://developer.apple.com/app-store/small-business-program/)**。

设置完成后，对于**应用内购买产品**，只需链接到如下 URL：

```html
<a href="inapppurchase://?package=purchase_package_identifier_name_here&disableadmob=true&consumable=true&successful_url=https://www.google.com">Buy In-App Purchase</a>
```

- "package" 是您想要销售的商品的产品标识符。
- "successful_url" 是购买完成后您希望应用加载的 URL。
  - *您可能希望在此页面保存一个 Cookie，以便您的 Web 应用记住已完成购买。*
- 如果您想在购买该产品后禁用广告，请包含 "disableadmob=true"。
- 为使用户能够再次为同一应用内购买产品付费（如再次购买），请将 "consumable" 属性设置为 true。反之，如果您希望阻止用户再次为同一产品付费（如再次购买），请将 "consumable" 设置为 false 或完全省略（因为 false 是默认值）。请确保使用 WebViewGold for Android v12.5 或更新版本。

或者，对于**应用内订阅产品**，请使用此类 URL：

```html
<a href="inappsubscription://?package=purchase_package_identifier_name_here&expired_url=https://www.yahoo.com&successful_url=https://www.google.com">Start In-App Subscription</a>
```

- "package" 是您想要销售的订阅的产品标识符。
- "successful_url" 是购买完成后您希望应用加载的 URL。
  - *您可能希望在此页面保存一个 Cookie，以便您的 Web 应用记住已激活订阅。*
- "expired_url" 是订阅不再有效时您希望应用加载的 URL。
  - *您可能希望在此页面更新/删除一个 Cookie，以便您的 Web 应用记住订阅已被停用。*

在此 URL 示例中，订阅成功激活后应调用 https://www.google.com，订阅到期后应立即调用 https://www.yahoo.com。\
您可以在服务器端识别用户。例如，站点 /buy_now.php 重定向到应用内购买 API，而该 API 重定向到 /thanks.php，您仍可以在服务器端访问用户/会话 Cookie，并识别刚刚完成该应用内购买的用户。在此用例中，请务必在 Config.java 文件中停用 CLEAR_CACHE_ON_STARTUP，以保留应用内购买过程激活的 Cookie。

**管理/取消订阅：** WebViewGold for Android 可以直接链接到 Play 商店的订阅管理界面 — 只需将您的链接指向 `cancelinapppurchase://`：

```html
<script>
<a href="cancelinapppurchase://">Manage/cancel subscription in Google Play</a>
<script>
```

**恢复购买：** WebViewGold for Android 提供了一种简单的方法来恢复用户的应用内购买。例如，在用户重新安装应用或更换设备并需要重新获得已购内容访问权限的场景中非常有用：

```html
<script>
<a href="restoreinapppurchases://">Restore</a>
<script>
```

**服务器端验证：** 此外或作为替代方案，WebViewGold 还允许您在服务器端处理应用内购买或订阅数据。交易成功后，WebViewGold 将创建以下 JavaScript 变量并将其注入网页：\
**1. planID：**包含产品 ID\
**2. transactionIdentifier：**包含唯一的交易 ID\
**3. subreceipts：**包含用户订阅的唯一收据 ID\
这些变量可以直接在网页上访问，以便进行服务器端存储和验证。请注意，交易完成后，这些变量会直接注入全局 window 对象。请确保您的 JavaScript 在可访问这些变量的同一页面上执行。如果变量未在预期时间内可用，请添加适当的回退机制（如超时实现所示）。
将这些变量发送到您的服务器后，您可以使用 Apple 的收据验证 API 或您选择的其他方法安全地验证订阅和交易。以下是 JavaScript 实现示例：

```html
<script>
// Utility function to wait for a variable to be defined
function waitForVariable(variableName, callback, timeout = 5000) {
    const startTime = Date.now();

    (function checkVariable() {
        if (window[variableName] !== undefined) {
            callback(window[variableName]);
        } else if (Date.now() - startTime < timeout) {
            setTimeout(checkVariable, 100);
        } else {
            console.error(`Timeout: ${variableName} was not set within ${timeout} ms`);
        }
    })();
}

// Example: Handling In-App Purchase/Subscription variables
waitForVariable("planID", function(planID) {
    console.log("planID:", planID);
    // Send the Product ID to your server
    sendToServer("planID", planID);
});

waitForVariable("transactionIdentifier", function(transactionIdentifier) {
    console.log("transactionIdentifier:", transactionIdentifier);
    // Send the Transaction ID to your server
    sendToServer("transactionIdentifier", transactionIdentifier);
});

waitForVariable("subreceipts", function(subreceipts) {
    console.log("subreceipts:", subreceipts);
    // Send Subscription Receipt IDs to your server
    sendToServer("subreceipts", subreceipts);
});

// Function to send data to your server for validation
function sendToServer(key, value) {
    fetch("https://example.com/api/validate", {
        method: "POST",
        headers: {
            "Content-Type": "application/json"
        },
        body: JSON.stringify({ [key]: value })
    })
    .then(response => response.json())
    .then(data => console.log(`Server Response for ${key}:`, data))
    .catch(error => console.error(`Error sending ${key}:`, error));
}
</script>
```

**本地化定价 / 获取商店位置：** `getstorelocation://` URL 方案将 Play 商店的位置注入到 JavaScript 变量中。当调用/链接 `getstorelocation://` 时，WebViewGold 包装器会检索 Play 商店的国家/地区代码（如果可用）。或者，您可以考虑在配置文件中将 `autoInjectVariable` 设置为 `true`，以自动将此值（和其他值）注入到 JavaScript 中，而无需 URL 调用。国家/地区代码随后会被注入到 JavaScript 变量 `storeLocation` 中，供您的 Web 应用进一步使用（**例如用于显示本地化定价**）。如果代码不可用，`storeLocation` 将被设置为 `null`：

- 成功时（示例：美国）：`var storeLocation = 'US';`
- 如果未找到国家/地区代码：`var storeLocation = null;`

注意：与任何技术一样，必须指出的是，即使使用我们的 API，也存在一些（技术熟练的）用户能够在未付款的情况下访问受限内容的风险。例如，这可能通过直接检索并打开 Success URL 链接，通过卸载应用后取消订阅产品使 Expiration URL 永远不被调用（为了最大限度地降低此风险，您可以定期请求重新授权），或通过使用撤回权和/或信用卡退单流程来实现。但值得注意的是，任何数字化方案都存在一定风险。总体而言，我们的 API 是一种向应用用户提供付费内容的实用且易于集成的方案，我们将继续致力于进一步降低风险。使用我们的 API 仍需自担风险，且不提供任何保证，但总体而言，虽然必须意识到内容遭到未授权/未付费访问的风险，但对大多数用户而言，使用我们的 API 的好处远远超过风险。建议跟踪并比较 Google Play Store Developer Console 的销售数据与应用内购买产品的服务器端激活数据，以确保准确的收入报告并识别任何潜在差异。

---

## 继续阅读

- ← 上一页： [应用内评分 API](in-app-rating.md)
- 下一页 →： [IAP History API](iap-history.md)
- 其他平台上的相同功能： [iOS – 应用内购买 API](../ios/in-app-purchases.md) · [macOS – In-App Purchases API](../macos/in-app-purchases.md)
- 语言： [🇺🇸 English](../../android/in-app-purchases.md) · [🇩🇪 Deutsch](../../de/android/in-app-purchases.md) · [🇫🇷 Français](../../fr/android/in-app-purchases.md) · [🇪🇸 Español](../../es/android/in-app-purchases.md) · **🇨🇳 中文**

> [!TIP]
> **太忙了？我们替您搭建应用。** 我们的团队为您配置、构建并提交 WebViewGold 应用——全程代劳、交付迅速、德国制造。 [让我们搭建应用 →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_android_doc_online)
>
> **在浏览器中构建：** 无需 Mac、无需 IDE：**WebViewGold Cloud Builder** 在线为您配置、构建并上传应用。 [了解 Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=android_docs)
