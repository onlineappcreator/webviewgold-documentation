---
title: "AdMob Ads API – WebViewGold for iOS Documentation"
description: "Monetize your iOS app with Google AdMob banner, interstitial, and rewarded ads — configuration and JavaScript triggers."
lang: "en"
product: "WebViewGold for iOS"
platform: "iOS"
category: "APIs & Features"
slug: "admob"
canonical_url: "https://www.webviewgold.com/docs/iOS/admob/"
keywords:
  - "AdMob Ads API"
  - "WebViewGold for iOS"
  - "convert website to app"
  - "WebView app documentation"
  - "iOS WebView SDK"
  - "PWA to app"
  - "HTML to app"
  - "JavaScript bridge"
last_updated: "2026-10-09"
---

# AdMob Ads API – WebViewGold for iOS

> **Summary:** Monetize your iOS app with Google AdMob banner, interstitial, and rewarded ads — configuration and JavaScript triggers.

[Documentation](../README.md) › [WebViewGold for iOS](README.md) › AdMob Ads API

**Platform:** iOS · **Category:** APIs & Features · **Online version:** [www.webviewgold.com/docs/iOS/admob/](https://www.webviewgold.com/docs/iOS/admob/)

---

AdMob is a Google service for monetizing mobile apps on iOS and Android platforms. It allows developers to integrate banner, interstitial, and rewarded ads, which are paid by clicks (CPC, Cost-per-Click) or impressions (CPM, Cost-per-Mille). WebViewGold simplifies AdMob integration, enabling quick setup for displaying ads in your WebView-based iOS application.

[![Watch the video: AdMob Ads API](https://img.youtube.com/vi/7j7NW5CTwqo/hqdefault.jpg)](https://www.youtube.com/watch?v=7j7NW5CTwqo)

**Step 1:** Open **Info.plist** file and set your AdMob global account ID in the *GADApplicationIdentifier* field:\
![Add your AdMob Account ID to the project](../assets/ios/img/admobglobal.webp)

**Step 2:** Please insert your AdMob IDs in the **Config.swift** for `AdmobBannerID`, `AdmobinterstitialID`, and `AdmobRewardedID`:\
![Activate specific AdMob banner blocs into your application](../assets/ios/img/admobconstants.webp)

**Step 3:** Within **Config.swift** you can:

- **Enable or disable** banner and/or interstitial ads by setting `showBannerAd` to `true` for banner ads and `showFullScreenAd` to `true` for interstitial ads.
- **Define intervals** for displaying interstitial ads by changing `showadAfterX` to the desired number of website interactions before playing an interstitial ad.

**To enable rewarded ads** *(only available for iOS versions greater than 13.0)***:** Set `enableRewardedAds` to `true`.

To play a rewarded ad, use a call to our rewarded ad API functionality.

```html
<a href="displayrewardedad://>Display Rewarded Advertisement</a>
```

Upon completion of full viewing of an advertisement, your website will be sent a call to a JavaScript function, **updateRewardedStatus('true');**. This function is up to you to implement in your JavaScript code, as it is up to you to decide how you want to reward the user.

WebViewGold supports displaying rewarded ads as the default advertisement option, overwriting the interstitial options. For this to occur, set `useRewardedAdsWherePossible` and `showFullScreenAd` to `true`.

**Tip:** If you display interstitial ads after X taps (`incrementWithTaps` set to `true`), you can also increase the tap counter manually from your web app by calling `increasetapcounter://` — useful for counting only specific interactions towards the ad interval.

*For more information, please consider the [official AdMob SDK documentation](https://developers.google.com/admob/) as well (but skip the setup parts as WebViewGold already includes the framework).*

---

## Continue reading

- ← Previous: [Push Notifications API](push-notifications.md)
- Next →: [Facebook Ads API](facebook-ads.md)
- Same feature on other platforms: [Android – AdMob Ads API](../android/admob.md)
- Languages: **🇺🇸 English** · [🇩🇪 Deutsch](../de/ios/admob.md) · [🇫🇷 Français](../fr/ios/admob.md) · [🇪🇸 Español](../es/ios/admob.md) · [🇨🇳 中文](../zh/ios/admob.md)

> [!TIP]
> **Too busy? We set up your app for you.** Our team configures, builds & submits your WebViewGold app — done-for-you, fast turnaround, Made in Germany. [Get your app set up →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **Build in your browser:** No Mac, no IDE: the **WebViewGold Cloud Builder** configures, builds & uploads your app online. [Discover Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
