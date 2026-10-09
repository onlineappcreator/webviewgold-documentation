---
title: "In-App Purchases API – WebViewGold for Android Documentation"
description: "Sell digital goods and subscriptions in your Android WebView app with Google Play Billing."
lang: "en"
product: "WebViewGold for Android"
platform: "Android"
category: "APIs & Features"
slug: "in-app-purchases"
canonical_url: "https://www.webviewgold.com/docs/android/in-app-purchases/"
keywords:
  - "In-App Purchases API"
  - "WebViewGold for Android"
  - "convert website to app"
  - "WebView app documentation"
  - "Android WebView SDK"
  - "PWA to app"
  - "HTML to app"
  - "JavaScript bridge"
last_updated: "2026-10-09"
---

# In-App Purchases API – WebViewGold for Android

> **Summary:** Sell digital goods and subscriptions in your Android WebView app with Google Play Billing.

[Documentation](../README.md) › [WebViewGold for Android](README.md) › In-App Purchases API

**Platform:** Android · **Category:** APIs & Features · **Online version:** [www.webviewgold.com/docs/android/in-app-purchases/](https://www.webviewgold.com/docs/android/in-app-purchases/)

---

Within some apps, you can buy additional content or services. These kinds of purchases are called "in-app purchases". They can be an attractive source of revenue for developers and are very convenient for customers as they use existing accounts and payment sources for settlement. WebViewGold allows triggering Google Play In-App Purchases. Make sure to own an [Extended License](credits.md) of WebViewGold if you plan to use this feature in an end product. Need to upgrade? [Learn how to upgrade here](https://help.market.envato.com/hc/en-us/articles/115005593503-If-I-choose-the-wrong-license-or-need-to-upgrade-my-license-how-easy-is-it-to-change-to-the-correct-license).

**Option 1 (Default): RevenueCat**\
Create your free [RevenueCat account](https://tinyurl.com/register-revenuecat) to get started. Pricing information is available on their website. Then set up RevenueCat by following their setup wizards and documentation (pricing details are available on their [website](https://tinyurl.com/register-revenuecat)). Afterwards, add your details to **Config.java**. This approach also supports the [15% Service Fee Tier Program](https://support.google.com/googleplay/android-developer/answer/112622?hl=en) of the Google Play Store and Apple's [Small Business Program](https://developer.apple.com/app-store/small-business-program/). If you participate in these reduced-fee programs, inform RevenueCat via their [Apple Small Business Program](https://www.revenuecat.com/docs/platform-resources/apple-platform-resources/app-store-small-business-program) or [Google 15% reduced service fee](https://www.revenuecat.com/docs/platform-resources/google-platform-resources/15-reduced-service-fee) pages. This is how setup in Config.java looks like:

```java
public static final String REVENUECAT_API_KEY = "xxxxxxxsxxxxxxxxxxxxxxxxxxxxxxxxxx"; //Your RevenueCat API Key (sign up via tinyurl.com/register-revenuecat first, then follow tinyurl.com/api-key-revenuecat how to find it)
public static final String REVENUECAT_PROJECT_ID = "xxxxxxx"; //Your RevenueCat Project ID (sign up via tinyurl.com/register-revenuecat first, then follow tinyurl.com/project-id-revenuecat how to find it)
```

Ensure your package name on the APK and Google Play Console matches the project configured in RevenueCat. Trigger a purchase or subscription using:

```
revenuecat://purchase?external_id=user_123&product=sub_30_days
```

`external_id` = User identifier, e.g., your customer email or user ID. `product` = ID displayed on the RevenueCat console. It works for both Android & iOS.

## Option 2: Manual (Non-RevenueCat)

We are committed to helping our WebViewGold customers achieve success, and we want to bring your attention to the 15% Service Fee Tier Program of the Google Play Store and Apple's Small Business Program. These programs allow eligible developers to qualify for a 15% commission, a significant reduction from the standard 30%. It's quick and easy to apply, and can potentially save you 50% in fees by **reducing the Google and Apple commission rates from 30% to 15%**. Once approved, you'll receive the reduced commission rate for all paid apps and in-app purchases made by customers on the respective stores. To learn more about the Google Play program, click **[here](https://support.google.com/googleplay/android-developer/answer/112622?hl=en)**, and for the Apple program, visit **[here](https://developer.apple.com/app-store/small-business-program/)**.

After setup, for **in-app purchase products** just link to this kind of URL:

```html
<a href="inapppurchase://?package=purchase_package_identifier_name_here&disableadmob=true&consumable=true&successful_url=https://www.google.com">Buy In-App Purchase</a>
```

- The "package" is the product identifier of the item you want to sell.
- The "successful_url" is the URL you want the app to load once the purchase is complete.
  - *You may want to save a cookie on this page so that your web app remembers that the purchase has been made.*
- Include "disableadmob=true" if you would like to disable ads after the purchase of the product.
- To enable the user to be charged again for the same in-app purchase product (if bought another time), set the attribute "consumable" to true. On the other hand, if you want to prevent the user from being charged again for the same product (if bought another time), set "consumable" to false or omit it altogether (since false is the default value). Make sure to use WebViewGold for Android v12.5 or newer.

Alternatively, use this kind of URL for **in-app subscription products**:

```html
<a href="inappsubscription://?package=purchase_package_identifier_name_here&expired_url=https://www.yahoo.com&successful_url=https://www.google.com">Start In-App Subscription</a>
```

- The "package" is the product identifier of the subscription you want to sell.
- The "successful_url" is the URL you want the app to load once the purchase is complete.
  - *You may want to save a cookie on this page so that your web app remembers that the subscription has been activated.*
- The "expired_url" is the URL you want the app to load when the subscription is no longer valid.
  - *You may want to update/delete a cookie on this page so that your web app remembers that the subscription has been deactivated.*

In this URL example, https://www.google.com should be called after the successful subscription activation, and https://www.yahoo.com should be called as soon as the subscription is expired.\
You can identify the user server-side. e.g., the site /buy_now.php redirects to In-App-Purchase API and that API redirects to /thanks.php, you can still access the user/session cookies server-sided and identify the user who just bought that In-App-Purchase. In this use case, please make sure that you deactivate the CLEAR_CACHE_ON_STARTUP in the Config.java file in order to keep cookies activated by the In-App Purchase process.

**Managing/canceling subscriptions:** WebViewGold for Android can link directly to the Play Store’s subscriptions management screen – just point your link to `cancelinapppurchase://`:

```html
<script>
<a href="cancelinapppurchase://">Manage/cancel subscription in Google Play</a>
<script>
```

**Restoring purchases:** WebViewGold for Android provides a simple way to restore in-app purchases made by users. E.g., useful for scenarios where users reinstall the app or switch devices and need to regain access to their purchased content:

```html
<script>
<a href="restoreinapppurchases://">Restore</a>
<script>
```

**Server-Side Verification:** Additionally or alternatively, WebViewGold also allows you to handle In-App Purchase or Subscription data from a server-side. After a successful transaction, the following JavaScript variables are created and injected into the webpage by WebViewGold: \
**1. planID:** Contains the Product ID\
**2. transactionIdentifier:** Contains the unique Transaction ID\
**3. subreceipts:** Contains unique receipt IDs for the user’s subscriptions\
These variables can be accessed directly on the webpage for server-side storage and validation. Note that these variables are injected directly into the global window object after a transaction. Make sure your JavaScript is executed on the same page where the variables are accessible. Add appropriate fallback mechanisms if the variables are not available within the expected time frame (as shown in the timeout implementation).
Sending these variables to your server allows you to validate subscriptions and transactions securely using Apple’s receipt validation API or your chosen method. Here’s an example JavaScript implementation:

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

**Localized Pricing / Get Store Location:** The `getstorelocation://` URL scheme injects the Play Store location into a JavaScript variable. When `getstorelocation://` is called/linked, the WebViewGold wrapper retrieves the Play Store's country code, if available. Alternatively, consider setting `autoInjectVariable` to `true` in the configuration file to automatically inject this (and other) values into JavaScript without needing a URL call. The country code is then injected into a JavaScript variable `storeLocation` for further use by your web app (**e.g., for displaying localized pricing**). If the code is not available, `storeLocation` will be set to `null`:

- If successful (example United States): `var storeLocation = 'US';`
- If no country code is found: `var storeLocation = null;`

Note: As with any technology, it is essential to mention that also while using our API, there is a risk that some (technically savvy) users may be able to access the restricted content without paying for it. This could, for example, occur through retrieving and opening the Success URL link directly, by uninstalling the app while afterward canceling subscription products so that the Expiration URL never gets called (to minimize this risk, you can, therefore, occasionally request reauthorizations) or by using withdrawal rights and/or chargeback processes of credit cards. However, it is worth noting that some kind of risk is present with any sort of digital approach. In general, our API is a practical and easy-to-integrate approach for delivering paid content to app users, and we continue to work on ways to reduce risks further. The use of our API is still at your own risk and without warranty, but overall, while it is essential to be aware of the risk of unauthorized/unpaid access to content, the benefits of using our API far outweigh the risks for most users. It is recommended to track and compare the sales data of the Google Play Store Developer Console with server-side activations of in-app purchase products to ensure accurate revenue reporting and identify any potential discrepancies.

---

## Continue reading

- ← Previous: [In-App Rating API](in-app-rating.md)
- Next →: [IAP History API](iap-history.md)
- Same feature on other platforms: [iOS – In-App Purchases API](../ios/in-app-purchases.md) · [macOS – In-App Purchases API](../macos/in-app-purchases.md)
- Languages: **🇺🇸 English** · [🇩🇪 Deutsch](../de/android/in-app-purchases.md) · [🇫🇷 Français](../fr/android/in-app-purchases.md) · [🇪🇸 Español](../es/android/in-app-purchases.md) · [🇨🇳 中文](../zh/android/in-app-purchases.md)

> [!TIP]
> **Too busy? We set up your app for you.** Our team configures, builds & submits your WebViewGold app — done-for-you, fast turnaround, Made in Germany. [Get your app set up →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_android_doc_online)
>
> **Build in your browser:** No Mac, no IDE: the **WebViewGold Cloud Builder** configures, builds & uploads your app online. [Discover Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=android_docs)
