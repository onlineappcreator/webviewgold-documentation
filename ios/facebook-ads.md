---
title: "Facebook Audience Network Ads API – WebViewGold for iOS Documentation"
description: "Show Facebook Audience Network banner and interstitial ads in your WebViewGold iOS app."
lang: "en"
product: "WebViewGold for iOS"
platform: "iOS"
category: "APIs & Features"
slug: "facebook-ads"
canonical_url: "https://www.webviewgold.com/docs/iOS/facebook-ads/"
keywords:
  - "Facebook Ads API"
  - "WebViewGold for iOS"
  - "convert website to app"
  - "WebView app documentation"
  - "iOS WebView SDK"
  - "PWA to app"
  - "HTML to app"
  - "JavaScript bridge"
last_updated: "2026-10-09"
---

# Facebook Audience Network Ads API – WebViewGold for iOS

> **Summary:** Show Facebook Audience Network banner and interstitial ads in your WebViewGold iOS app.

[Documentation](../README.md) › [WebViewGold for iOS](README.md) › Facebook Ads API

**Platform:** iOS · **Category:** APIs & Features · **Online version:** [www.webviewgold.com/docs/iOS/facebook-ads/](https://www.webviewgold.com/docs/iOS/facebook-ads/)

---

The [Facebook Audience Network](https://www.facebook.com/audiencenetwork/) allows mobile app developers to monetize iOS and Android applications by displaying ads. Through WebViewGold, you can easily incorporate Facebook ads into your WebView-based iOS applications to earn revenue through clicks (CPC) and impressions (CPM).

## Step 1: Create a Facebook Audience Network Account

You must create a [Facebook Audience Network](https://www.facebook.com/audiencenetwork/) account and create a property under integration in the Monetization Manager. Then you must connect an iOS app (however, you do not need to link to a published iOS app for testing purposes).

Follow this guide for reference: <https://www.facebook.com/business/help/191133327919314>

## Step 2: Set the Necessary Configuration Variables

- Open **Config.swift** and set `useFacebookAds` to `true`.
- Enter your Facebook Placement ID at `facebookAdsID`.

![Facebook Ads configuration screenshot](../assets/ios/img/fbadsconfig.webp)

## Step 3: Configure Ad Settings

- To use timed ads, set `useTimedAds` to `true` and set `showFBAdsEveryNSeconds` to the desired time between ads.
- You can add URL trigger words to `fbadstriggerurls` to initialize ads on command.

## Further considerations

- A real iOS device must be used to test (not a simulator)
- The device must be added as a test device, see <https://developers.facebook.com/docs/audience-network/setting-up/testing/platform>
- Facebook must be installed and logged in on the device
- “Limit Ad Tracking” or any similar setting that may be released with upcoming iOS versions must be disabled.

---

## Continue reading

- ← Previous: [AdMob Ads API](admob.md)
- Next →: [HTML Audio API](html-audio.md)
- Same feature on other platforms: [Android – Facebook Ads API](../android/facebook-ads.md)
- Languages: **🇺🇸 English** · [🇩🇪 Deutsch](../de/ios/facebook-ads.md) · [🇫🇷 Français](../fr/ios/facebook-ads.md) · [🇪🇸 Español](../es/ios/facebook-ads.md) · [🇨🇳 中文](../zh/ios/facebook-ads.md)

> [!TIP]
> **Too busy? We set up your app for you.** Our team configures, builds & submits your WebViewGold app — done-for-you, fast turnaround, Made in Germany. [Get your app set up →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **Build in your browser:** No Mac, no IDE: the **WebViewGold Cloud Builder** configures, builds & uploads your app online. [Discover Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
