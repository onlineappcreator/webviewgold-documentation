---
title: "应用内购买 API – WebViewGold for iOS 文档"
description: "借助由 StoreKit 驱动的应用内购买，在您的 iOS WebView 应用中销售数字商品和订阅。"
lang: "zh"
product: "WebViewGold for iOS"
platform: "iOS"
category: "API 与功能"
slug: "in-app-purchases"
canonical_url: "https://www.webviewgold.com/zh/docs/iOS/in-app-purchases/"
keywords:
  - "应用内购买 API"
  - "WebViewGold for iOS"
  - "将网站转换为应用"
  - "WebView 应用文档"
  - "iOS WebView SDK"
  - "PWA 转应用"
  - "HTML 转应用"
  - "JavaScript 桥接"
last_updated: "2026-10-09"
---

# 应用内购买 API – WebViewGold for iOS

> **摘要：** 借助由 StoreKit 驱动的应用内购买，在您的 iOS WebView 应用中销售数字商品和订阅。

[文档](../README.md) › [WebViewGold for iOS](README.md) › 应用内购买 API

**平台：** iOS · **类别：** API 与功能 · **在线版本：** [www.webviewgold.com/zh/docs/iOS/in-app-purchases/](https://www.webviewgold.com/zh/docs/iOS/in-app-purchases/)

---

在某些应用中，您可以购买额外的内容或服务。这类购买称为"应用内购买"。对开发者而言，它们可以是一种颇具吸引力的收入来源；对客户而言也非常便利，因为可以直接使用现有账户和支付方式完成结算。WebViewGold 允许触发 App Store 应用内购买。如果您计划在最终产品中使用此功能，请确保拥有 WebViewGold 的[扩展许可证](credits.md)。需要升级？[在此了解如何升级](https://help.market.envato.com/hc/en-us/articles/115005593503-If-I-choose-the-wrong-license-or-need-to-upgrade-my-license-how-easy-is-it-to-change-to-the-correct-license)。

**方案 1（默认）：RevenueCat**\
创建您的免费 [RevenueCat 账户](https://tinyurl.com/register-revenuecat)开始使用。定价信息可在其网站上查看。然后按照其安装向导和文档设置 RevenueCat（定价详情可在其[网站](https://tinyurl.com/register-revenuecat)上查看）。之后，将您的详细信息添加到 **Config.swift** 中。此方案同样支持 Google Play 商店的 [15% Service Fee Tier Program](https://support.google.com/googleplay/android-developer/answer/112622?hl=en) 和 Apple 的 [Small Business Program](https://developer.apple.com/app-store/small-business-program/)。如果您参与了这些低费率计划，请通过 RevenueCat 的 [Apple Small Business Program](https://www.revenuecat.com/docs/platform-resources/apple-platform-resources/app-store-small-business-program) 或 [Google 15% reduced service fee](https://www.revenuecat.com/docs/platform-resources/google-platform-resources/15-reduced-service-fee) 页面告知 RevenueCat。Config.swift 中的设置如下所示：

```swift
static let kRevenueCatEnable = true //Set to true to activate RevenueCat
static let kRevenueCatShowDefaultOfferingPaywall = true //Set to true to show the default offering paywall on app launch
static let revenueCatAPIKey = "xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx" //Your RevenueCat API Key (sign up via tinyurl.com/register-revenuecat first, then follow tinyurl.com/api-key-revenuecat how to find it)
static let revenueCatProjectID = "xxxxxxxxx" //Your RevenueCat Project ID (sign up via tinyurl.com/register-revenuecat first, then follow tinyurl.com/project-id-revenuecat how to find it)
```

请确保 Xcode 与 App Store Connect 中的 Bundle ID 与 RevenueCat 中配置的项目一致。使用以下方式触发购买或订阅：

```
revenuecat://purchase?external_id=user_123&product=sub_30_days
```

`external_id` = 用户标识符，例如客户的邮箱地址或用户 ID。`product` = 显示在 RevenueCat 控制台中的 ID。

您还可以直接从 Web 应用展示原生的 **RevenueCat 付费墙**（在 RevenueCat 控制台中配置）——需要 iOS 15 或更高版本：

```
revenuecat://launchPaywall?external_id=user_123&offering=CustomOfferingOne
```

`external_id` = 用户标识符，例如客户的邮箱地址或用户 ID（必填）。`offering` = 可选的 RevenueCat offering 标识符，用于指定要展示付费墙的 offering；省略该参数则展示默认 offering 的付费墙。

## 方案 2：手动（不使用 RevenueCat）

首先，将 App Store Connect 中应用内购买"Shared Secret"的详细信息插入 **Config.swift** 文件。要在 App Store Connect 中查找您的"Shared Secret"，需要先登录您的 App Store Connect 账户。然后，前往"Users and Access"部分，并选择"Shared Secret"选项卡。您生成的"Shared Secret"将会列出，您可以将其复制并粘贴到 WebViewGold 中 Config.swift 相应的"IAPSharedSecret"字段。\
我们非常关心客户的成功，并会尽一切可能为他们提供支持：这就是我们希望在此提及 App Store Small Business Program 和 Google Play 商店 15% Service Fee Tier Program 的原因。根据这些计划，符合资格的开发者可获得 15% 的降低佣金比例，比标准的 30% 大幅降低。仅需几分钟即可填写申请表单，最多可为您节省 50% 的费用（**佣金比例从 30% 降至 15%**）。一旦获得批准，您将在相应商店的所有付费应用和应用内购买中享受降低后的佣金比例。要了解有关 Apple 计划的更多信息，请点击[**此处**](https://developer.apple.com/app-store/small-business-program/)；有关 Google Play 计划的更多信息，请点击[**此处**](https://support.google.com/googleplay/android-developer/answer/112622?hl=en)。\
设置完成后，对于**应用内购买产品**，只需链接到如下 URL：

```html
<a href="inapppurchase://?package=IN-APP_PURCHASE_PRODUCT_IDENTIFIER&disableadmob=true&successful_url=https://www.google.com">Buy In-App Purchase</a>
```

- "package" 是您想要销售的商品的产品标识符。
- "successful_url" 是购买完成后您希望应用加载的 URL。
  - *您可能希望在此页面保存一个 Cookie，以便您的 Web 应用记住已完成购买。*
- 如果您想在购买该产品后禁用 AdMob 广告，请包含 "disableadmob=true"。

对于**应用内订阅产品**，请使用此类 URL 方案：

```html
<a href="inappsubscription://?package=IN-APP_PURCHASE_PRODUCT_IDENTIFIER&expired_url=https://www.yahoo.com&successful_url=https://www.google.com">Start In-App Subscription</a>
```

- "package" 是您想要销售的订阅的产品标识符。
- "successful_url" 是购买完成后您希望应用加载的 URL。
  - *您可能希望在此页面保存一个 Cookie，以便您的 Web 应用记住已激活订阅。*
- "expired_url" 是订阅不再有效时您希望应用加载的 URL。
  - *您可能希望在此页面更新/删除一个 Cookie，以便您的 Web 应用记住订阅已被停用。*

有关应用内购买产品标识符的所有信息可在[此处](https://developer.apple.com/library/archive/qa/qa1329/_index.html)找到。\
您可以在服务器端识别用户。例如，站点 /buy_now.php 重定向到应用内购买 API，而该 API 重定向到 /thanks.php，您仍可以在服务器端访问用户/会话 Cookie，并识别刚刚完成该应用内购买的用户。在此用例中，请务必在 *Config.swift* 文件中停用 *deletecache* 选项，以保留应用内购买过程激活的 Cookie。

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

**恢复购买：**调用 `restoreinapppurchases://` 可使您的应用重新启用先前购买的内容。当用户点击带有此 URL 方案的链接时，应用会启动一个流程来重新验证并恢复应用内购买 — 适用于应用重新安装或更换设备等场景。只需添加类似以下的链接，即可让用户恢复其购买：

```html
<a href="restoreinapppurchases://">Restore Purchases</a>
```

**购买历史：**要在您的 Web 应用中显示用户的历史购买，请参阅[应用内购买历史 API](iap-history.md)（`getpurchasehistory://`）。

**取消订阅：**调用 `cancelinapppurchase://` 会将用户引导至 Apple 官方的订阅管理门户，让他们通过 Apple 的原生界面取消订阅。只需添加类似以下的链接，即可将用户引导至订阅管理页面：

```html
<a href="cancelinapppurchase://">Cancel Subscription</a>
```

**本地化定价 / 获取商店位置：** `getstorelocation://` URL 方案将 App Store 位置注入到 JavaScript 变量中。在调用/链接 `getstorelocation://` 后，WebViewGold 包装器会检索 App Store 的国家/地区代码（如果可用）。或者，您可以考虑在 Config.swift 中将 `autoInjectVariable` 设置为 `true`，以自动将此值（和其他值）注入到 JavaScript 中，而无需事先调用 URL。国家/地区代码随后会被注入到 JavaScript 变量 `storeLocation` 中，供您的 Web 应用进一步使用（**例如用于显示本地化定价**）。如果代码不可用，`storeLocation` 将被设置为 `null`：

- 成功时（示例：美利坚合众国）：`var storeLocation = 'US';`
- 如果未找到国家/地区代码：`var storeLocation = null;`

注意：使用我们的 API 向应用用户提供付费内容确实存在一定风险，即技术熟练的用户可能会在未付款的情况下访问该内容。这可能通过多种方式发生，例如直接检索并打开 Success URL 链接、卸载应用后取消订阅产品，或使用撤回权和信用卡退单流程。然而，必须指出的是，任何数字化方案都存在一定程度的风险。虽然我们将继续致力于降低这些风险，但最终由 WebViewGold 用户/开发者在使用建议方案时接受内容遭到未授权/未付费访问的风险，因为该 API 不提供任何保证。尽管如此，对大多数用户而言，使用我们的 API 的好处通常超过风险。为确保准确的收入报告并识别潜在差异，我们建议跟踪并比较 App Store Connect 的销售数据与应用内购买产品的服务器端激活数据。

---

## 继续阅读

- ← 上一页： [应用内评分对话框 API](in-app-rating.md)
- 下一页 →： [购买历史 API](iap-history.md)
- 其他平台上的相同功能： [Android – 应用内购买 API](../android/in-app-purchases.md) · [macOS – In-App Purchases API](../macos/in-app-purchases.md)
- 语言： [🇺🇸 English](../../ios/in-app-purchases.md) · [🇩🇪 Deutsch](../../de/ios/in-app-purchases.md) · [🇫🇷 Français](../../fr/ios/in-app-purchases.md) · [🇪🇸 Español](../../es/ios/in-app-purchases.md) · **🇨🇳 中文**

> [!TIP]
> **太忙了？我们替您搭建应用。** 我们的团队为您配置、构建并提交 WebViewGold 应用——全程代劳、交付迅速、德国制造。 [让我们搭建应用 →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **在浏览器中构建：** 无需 Mac、无需 IDE：**WebViewGold Cloud Builder** 在线为您配置、构建并上传应用。 [了解 Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
