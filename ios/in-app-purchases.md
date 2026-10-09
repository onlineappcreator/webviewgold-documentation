---
title: "In-App Purchases API – WebViewGold for iOS Documentation"
description: "Sell digital goods and subscriptions in your iOS WebView app with StoreKit-powered In-App Purchases."
lang: "en"
product: "WebViewGold for iOS"
platform: "iOS"
category: "APIs & Features"
slug: "in-app-purchases"
canonical_url: "https://www.webviewgold.com/docs/iOS/in-app-purchases/"
keywords:
  - "In-App Purchases API"
  - "WebViewGold for iOS"
  - "convert website to app"
  - "WebView app documentation"
  - "iOS WebView SDK"
  - "PWA to app"
  - "HTML to app"
  - "JavaScript bridge"
last_updated: "2026-10-09"
---

# In-App Purchases API – WebViewGold for iOS

> **Summary:** Sell digital goods and subscriptions in your iOS WebView app with StoreKit-powered In-App Purchases.

[Documentation](../README.md) › [WebViewGold for iOS](README.md) › In-App Purchases API

**Platform:** iOS · **Category:** APIs & Features · **Online version:** [www.webviewgold.com/docs/iOS/in-app-purchases/](https://www.webviewgold.com/docs/iOS/in-app-purchases/)

---

Within some apps, you can buy additional content or services. These kinds of purchases are called "in-app purchases". They can be an attractive source of revenue for developers and are very convenient for customers as they use existing accounts and payment sources for settlement. WebViewGold allows triggering App Store In-App Purchases. Make sure to own an [Extended License](credits.md) of WebViewGold if you plan to use this feature in an end product. Need to upgrade? [Learn how to upgrade here](https://help.market.envato.com/hc/en-us/articles/115005593503-If-I-choose-the-wrong-license-or-need-to-upgrade-my-license-how-easy-is-it-to-change-to-the-correct-license).

**Option 1 (Default): RevenueCat**\
Create your free [RevenueCat account](https://tinyurl.com/register-revenuecat) to get started. Pricing information is available on their website. Then set up RevenueCat by following their setup wizards and documentation (pricing details are available on their [website](https://tinyurl.com/register-revenuecat)). Afterwards, add your details to **Config.swift**. This approach also supports the [15% Service Fee Tier Program](https://support.google.com/googleplay/android-developer/answer/112622?hl=en) of the Google Play Store and Apple's [Small Business Program](https://developer.apple.com/app-store/small-business-program/). If you participate in these reduced-fee programs, inform RevenueCat via their [Apple Small Business Program](https://www.revenuecat.com/docs/platform-resources/apple-platform-resources/app-store-small-business-program) or [Google 15% reduced service fee](https://www.revenuecat.com/docs/platform-resources/google-platform-resources/15-reduced-service-fee) pages. This is how setup in Config.swift looks like:

```swift
static let kRevenueCatEnable = true //Set to true to activate RevenueCat
static let kRevenueCatShowDefaultOfferingPaywall = true //Set to true to show the default offering paywall on app launch
static let revenueCatAPIKey = "xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx" //Your RevenueCat API Key (sign up via tinyurl.com/register-revenuecat first, then follow tinyurl.com/api-key-revenuecat how to find it)
static let revenueCatProjectID = "xxxxxxxxx" //Your RevenueCat Project ID (sign up via tinyurl.com/register-revenuecat first, then follow tinyurl.com/project-id-revenuecat how to find it)
```

Ensure your Bundle ID in Xcode & App Store Connect matches the project configured in RevenueCat. Trigger a purchase or subscription using:

```
revenuecat://purchase?external_id=user_123&product=sub_30_days
```

`external_id` = User identifier, e.g., your customer email or user ID. `product` = ID displayed on the RevenueCat console.

You can also present a native **RevenueCat Paywall** (configured in the RevenueCat dashboard) straight from your web app — requires iOS 15 or higher:

```
revenuecat://launchPaywall?external_id=user_123&offering=CustomOfferingOne
```

`external_id` = User identifier, e.g., your customer email or user ID (required). `offering` = Optional identifier of the RevenueCat offering whose paywall should be shown; omit it to present the default offering paywall.

## Option 2: Manual (Non-RevenueCat)

In the first step, insert the App Store Connect details of your In-App Purchase "Shared Secret" in **Config.swift** file. To find your "Shared Secret" in App Store Connect, you need to first log into your App Store Connect account. Then, go to the "Users and Access" section, and select the "Shared Secret" tab. Your generated "Shared Secret" will be listed, and you can copy/paste it to the relevant "IAPSharedSecret" field in Config.swift of WebViewGold. \
We care about the success of our customers and are here to support them in any way we can: That’s why we want to mention the App Store Small Business Program and the Google Play Store 15% Service Fee Tier Program here. Under these programs, eligible developers can qualify for a reduced 15% commission down from the standard 30% commission. It only takes minutes to fill out their forms, and they can potentially save you 50% of fees (**reduction from 30% commission to 15%**). Once approved, you will receive the reduced commission rate for all paid apps and in-app purchases made by customers on the respective stores. Find more information on the Apple program [**here**](https://developer.apple.com/app-store/small-business-program/) and on the Google Play program [**here**](https://support.google.com/googleplay/android-developer/answer/112622?hl=en). \
After setup, for **in-app purchase products** just link to this kind of URL:

```html
<a href="inapppurchase://?package=IN-APP_PURCHASE_PRODUCT_IDENTIFIER&disableadmob=true&successful_url=https://www.google.com">Buy In-App Purchase</a>
```

- The "package" is the product identifier of the item you want to sell.
- The "successful_url" is the URL you want the app to load once the purchase is complete.
  - *You may want to save a cookie on this page so that your web app remembers that the purchase has been made.*
- Include "disableadmob=true" if you would like to disable AdMob ads after the purchase of the product.

For **in-app subscription products**, use this kind of URL scheme:

```html
<a href="inappsubscription://?package=IN-APP_PURCHASE_PRODUCT_IDENTIFIER&expired_url=https://www.yahoo.com&successful_url=https://www.google.com">Start In-App Subscription</a>
```

- The "package" is the product identifier of the subscription you want to sell.
- The "successful_url" is the URL you want the app to load once the purchase is complete.
  - *You may want to save a cookie on this page so that your web app remembers that the subscription has been activated.*
- The "expired_url" is the URL you want the app to load when the subscription is no longer valid.
  - *You may want to update/delete a cookie on this page so that your web app remembers that the subscription has been deactivated.*

All information about the In-App Purchase Product Identifier can be found [here](https://developer.apple.com/library/archive/qa/qa1329/_index.html).\
You can identify the user server-side. e.g., the site /buy_now.php redirects to In-App-Purchase API and that API redirects to /thanks.php, you can still access the user/session cookies server-sided and identify the user who just bought that In-App-Purchase. In this use case, please make sure that you deactivate the *deletecache* option in the *Config.swift* file in order to keep cookies activated by the In-App Purchase process.

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

**Restore Purchases:** A `restoreinapppurchases://` call allows your app to re-enable previously purchased content. When a user taps a link with this URL scheme, the app initiates a process to revalidate and restore in-app purchases—ideal for scenarios like app reinstallation or device change. Simply add a link like the following to let users restore their purchases:

```html
<a href="restoreinapppurchases://">Restore Purchases</a>
```

**Purchase History:** To display the user's previous purchases inside your web app, see the [In-App Purchase History API](iap-history.md) (`getpurchasehistory://`).

**Cancel Subscription:** A `cancelinapppurchase://` call directs users to the official Apple subscription management portal, allowing them to cancel their subscriptions through Apple's native interface. Simply add a link like the following to forward users to manage their subscriptions:

```html
<a href="cancelinapppurchase://">Cancel Subscription</a>
```

**Localized Pricing / Get Store Location:** The `getstorelocation://` URL scheme injects the App Store location into a JavaScript variable. After `getstorelocation://` is called/linked to, the WebViewGold wrapper retrieves the App Store's country code if available. Alternatively, consider turning `autoInjectVariable` to `true` in Config.swift to automatically inject this (and other) values into JavaScript without needing to call a URL upfront. The country code is then injected into a JavaScript variable `storeLocation` for further use by your web app (**e.g., for displaying localized pricing**). If the code is not available, `storeLocation` will be set to `null`:

- If successful (example United States of America): `var storeLocation = 'US';`
- If no country code is found: `var storeLocation = null;`

Note: Using our API for delivering paid content to app users does carry some risk of technically savvy users accessing the content without paying for it. This could occur through various methods, such as retrieving and opening the Success URL link directly, canceling subscription products after uninstalling the app, or using withdrawal rights and chargeback processes for credit cards. However, it is crucial to note that some level of risk is present with any digital approach. While we continue to work on ways to reduce these risks, it is ultimately up to the WebViewGold user/developer to accept the risk of unauthorized/unpaid access to content when using the suggested approach, as the API comes without a warranty. Despite this, the benefits of using our API generally outweigh the risks for most users. To ensure accurate revenue reporting and identify potential discrepancies, we recommend tracking and comparing the sales data of App Store Connect with server-side activations of in-app purchase products.

---

## Continue reading

- ← Previous: [In-App Rating Dialog API](in-app-rating.md)
- Next →: [IAP History API](iap-history.md)
- Same feature on other platforms: [Android – In-App Purchases API](../android/in-app-purchases.md) · [macOS – In-App Purchases API](../macos/in-app-purchases.md)
- Languages: **🇺🇸 English** · [🇩🇪 Deutsch](../de/ios/in-app-purchases.md) · [🇫🇷 Français](../fr/ios/in-app-purchases.md) · [🇪🇸 Español](../es/ios/in-app-purchases.md) · [🇨🇳 中文](../zh/ios/in-app-purchases.md)

> [!TIP]
> **Too busy? We set up your app for you.** Our team configures, builds & submits your WebViewGold app — done-for-you, fast turnaround, Made in Germany. [Get your app set up →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **Build in your browser:** No Mac, no IDE: the **WebViewGold Cloud Builder** configures, builds & uploads your app online. [Discover Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
