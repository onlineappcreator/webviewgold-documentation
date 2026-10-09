---
title: "AdMob Ads API – WebViewGold for Android Documentation"
description: "Monetize your Android app with Google AdMob banner and interstitial ads — configuration and JavaScript triggers."
lang: "en"
product: "WebViewGold for Android"
platform: "Android"
category: "APIs & Features"
slug: "admob"
canonical_url: "https://www.webviewgold.com/docs/android/admob/"
keywords:
  - "AdMob Ads API"
  - "WebViewGold for Android"
  - "convert website to app"
  - "WebView app documentation"
  - "Android WebView SDK"
  - "PWA to app"
  - "HTML to app"
  - "JavaScript bridge"
last_updated: "2026-10-09"
---

# AdMob Ads API – WebViewGold for Android

> **Summary:** Monetize your Android app with Google AdMob banner and interstitial ads — configuration and JavaScript triggers.

[Documentation](../README.md) › [WebViewGold for Android](README.md) › AdMob Ads API

**Platform:** Android · **Category:** APIs & Features · **Online version:** [www.webviewgold.com/docs/android/admob/](https://www.webviewgold.com/docs/android/admob/)

---

AdMob is a Google service for monetizing mobile apps on iOS and Android platforms. It allows developers to integrate banner, interstitial, and rewarded ads, which are paid by clicks (CPC, Cost-per-Click) or impressions (CPM, Cost-per-Mille). WebViewGold simplifies AdMob integration, enabling quick setup for displaying ads in your WebView-based Android application.

## Step 1: Open Config.java File

To begin, open your app's **Config.java** file to set ad preferences and activate AdMob functionality.

## Step 2: Monetize Your App with Native AdMob SDK

In **Config.java** you can:

- **Enable or disable** banner and/or interstitial ads by setting `SHOW_BANNER_AD` to true for banner ads and `SHOW_FULL_SCREEN_AD` to true for interstitial ads.
- **Define intervals** for displaying interstitial ads by changing `SHOW_AD_AFTER_X` to the desired number of website interactions before playing an interstitial ad.

**Note:** Before launching your app, ensure that your unique AdMob IDs are correctly added in the **strings.xml** file:\
![Enable specific AdMob ad blocs in your app](../assets/android/img/admobconfig.webp)

## Step 3: Enable Rewarded Ads

- Setting Up Rewarded Ads:
  - To enable rewarded ads, set `ENABLE_REWARDED_ADS` to `true`.
  - Use the following link to display a rewarded ad

    ```html
    <a href="displayrewardedad://">Display Rewarded Advertisement</a>
    ```

  - Once a user completes viewing the ad, WebViewGold triggers the JavaScript function `updateRewardedStatus('true');` for you to handle rewards within your app’s code.
- Rewarded Ads as Default:
  - If you prefer rewarded ads to display by default, set both `USE_REWARDED_ADS_WHERE_POSSIBLE` and `SHOW_FULL_SCREEN_AD` to `true`. This will prioritize rewarded ads over interstitial ads.

## Additional Resources

For more detailed options, refer to the [official AdMob SDK documentation](https://developers.google.com/admob/), but skip the setup instructions as WebViewGold already includes the necessary framework.

[![Watch the video: AdMob Ads API](https://img.youtube.com/vi/vq5FM7n0Syg/hqdefault.jpg)](https://www.youtube.com/watch?v=vq5FM7n0Syg)

You can also **dynamically** control the ad visibility for a user by calling the following custom URL schemes from your website or app:

- `enableads://` – Set ads to be shown again for the current user
- `disableads://` – Permanently disables ads for the current user

## <a id="appopenads"></a>Step 4: Enable App Open Ads

**App open ads** are fullscreen ads that appear when the user opens the app (cold start from the launcher splash) or returns to it from the background. To enable them:

- Set `SHOW_APP_OPEN_AD` to `true` in **Config.java**.
- Replace the `admob_app_open_id` value in **strings.xml** with your own AdMob app open ad unit ID (the template ships with the official AdMob test ID — replace it before release!).

**Note:** App open ads respect the Google consent management setting (`ASK_FOR_AD_CONSENT`) just like the other AdMob formats.

---

## Continue reading

- ← Previous: [Push Notifications API](push-notifications.md)
- Next →: [Facebook Ads API](facebook-ads.md)
- Same feature on other platforms: [iOS – AdMob Ads API](../ios/admob.md)
- Languages: **🇺🇸 English** · [🇩🇪 Deutsch](../de/android/admob.md) · [🇫🇷 Français](../fr/android/admob.md) · [🇪🇸 Español](../es/android/admob.md) · [🇨🇳 中文](../zh/android/admob.md)

> [!TIP]
> **Too busy? We set up your app for you.** Our team configures, builds & submits your WebViewGold app — done-for-you, fast turnaround, Made in Germany. [Get your app set up →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_android_doc_online)
>
> **Build in your browser:** No Mac, no IDE: the **WebViewGold Cloud Builder** configures, builds & uploads your app online. [Discover Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=android_docs)
