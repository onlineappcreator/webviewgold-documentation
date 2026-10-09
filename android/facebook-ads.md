---
title: "Facebook Audience Network Ads API – WebViewGold for Android Documentation"
description: "Show Facebook Audience Network banner and interstitial ads in your WebViewGold Android app."
lang: "en"
product: "WebViewGold for Android"
platform: "Android"
category: "APIs & Features"
slug: "facebook-ads"
canonical_url: "https://www.webviewgold.com/docs/android/facebook-ads/"
keywords:
  - "Facebook Ads API"
  - "WebViewGold for Android"
  - "convert website to app"
  - "WebView app documentation"
  - "Android WebView SDK"
  - "PWA to app"
  - "HTML to app"
  - "JavaScript bridge"
last_updated: "2026-10-09"
---

# Facebook Audience Network Ads API – WebViewGold for Android

> **Summary:** Show Facebook Audience Network banner and interstitial ads in your WebViewGold Android app.

[Documentation](../README.md) › [WebViewGold for Android](README.md) › Facebook Ads API

**Platform:** Android · **Category:** APIs & Features · **Online version:** [www.webviewgold.com/docs/android/facebook-ads/](https://www.webviewgold.com/docs/android/facebook-ads/)

---

The Facebook Audience Network allows mobile app developers to monetize iOS and Android applications by displaying ads. Through WebViewGold, you can easily incorporate Facebook ads into your WebView-based Android app to earn revenue through clicks (CPC) and impressions (CPM).

## Step 1: Open the Config.java File

- To begin, open your app's **Config.java** file to configure the Audience Network settings.

## Step 2: Enable Facebook Audience Network Ads

1. **Activate Necessary Configuration Variables:**
   - Set the following variables to `true` in Config.java:
     - `USE_FACEBOOK_ADS` sets the app to use Facebook Audience Network ads instead of AdMob ads.
     - `SHOW_BANNER_AD` turns on banner ads for your app.
     - `SHOW_FULLSCREEN_AD` turns on fullscreen, interstitial ads for your app.
   - Set `SHOW_AD_AFTER_X` to a desired number of website clicks to show an interstitial ad.

2. **Enter Your Facebook Ad IDs:**
   - Go to `strings.xml` and add your unique Facebook Ad IDs to the corresponding fields.

After configuring the above settings and confirming your Ad IDs, your app is now ready to launch with Facebook Audience Network ads enabled.

For further details, you may also refer to the [official Facebook Audience Network documentation](https://developers.facebook.com/docs/audience-network) for any additional setup or optimization tips specific to your ad strategy.

[![Watch the video: Facebook Audience Network Ads API](https://img.youtube.com/vi/81wCzuFttic/hqdefault.jpg)](https://www.youtube.com/watch?v=81wCzuFttic)

You can also **dynamically** control the ad visibility for a user by calling the following custom URL schemes from your website or app:

- `enableads://` – Set ads to be shown again for the current user
- `disableads://` – Permanently disables ads for the current user

```html
<a href="enableads://">Enable Ads</a>
<a href="disableads://">Disable Ads</a>
```

---

## Continue reading

- ← Previous: [AdMob Ads API](admob.md)
- Next →: [File Downloader API](file-downloader.md)
- Same feature on other platforms: [iOS – Facebook Ads API](../ios/facebook-ads.md)
- Languages: **🇺🇸 English** · [🇩🇪 Deutsch](../de/android/facebook-ads.md) · [🇫🇷 Français](../fr/android/facebook-ads.md) · [🇪🇸 Español](../es/android/facebook-ads.md) · [🇨🇳 中文](../zh/android/facebook-ads.md)

> [!TIP]
> **Too busy? We set up your app for you.** Our team configures, builds & submits your WebViewGold app — done-for-you, fast turnaround, Made in Germany. [Get your app set up →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_android_doc_online)
>
> **Build in your browser:** No Mac, no IDE: the **WebViewGold Cloud Builder** configures, builds & uploads your app online. [Discover Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=android_docs)
