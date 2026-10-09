---
title: "App Links & Deep Linking API – WebViewGold for Android Documentation"
description: "Open links to your domain directly in your Android app with App Links and custom URL scheme deep linking."
lang: "en"
product: "WebViewGold for Android"
platform: "Android"
category: "APIs & Features"
slug: "app-links"
canonical_url: "https://www.webviewgold.com/docs/android/app-links/"
keywords:
  - "App Links / Deep Linking"
  - "WebViewGold for Android"
  - "convert website to app"
  - "WebView app documentation"
  - "Android WebView SDK"
  - "PWA to app"
  - "HTML to app"
  - "JavaScript bridge"
last_updated: "2026-10-09"
---

# App Links & Deep Linking API – WebViewGold for Android

> **Summary:** Open links to your domain directly in your Android app with App Links and custom URL scheme deep linking.

[Documentation](../README.md) › [WebViewGold for Android](README.md) › App Links / Deep Linking

**Platform:** Android · **Category:** APIs & Features · **Online version:** [www.webviewgold.com/docs/android/app-links/](https://www.webviewgold.com/docs/android/app-links/)

---

The WebViewGold App Links / Deeplinking API enables users to open specific pages in your app from external sources like email, social media, or messaging apps.

## WebViewGold for Android supports two deep linking methods

- **Standard URL-based Deep Links:** e.g. `https://www.example.org/subpages/example1`
- **Custom Scheme Deep Links:** e.g. `webviewgold://https://www.example.org/subpages/example2`

## Step 1: Configure Your Link Scheme in AndroidManifest.xml

To support standard deep linking, configure your **AndroidManifest.xml** to associate your domain with your app. Replace `www.webviewgold.com` with your actual domain (e.g., `www.example.org`):

![AndroidManifest.xml for App Link Configuration](../assets/android/img/applinks1.webp)

## Step 2: Enable Deep Linking in Config.java

In your **Config.java** file, enable deep linking features:

```java
// Enables standard deep linking (https:// links)
public static final boolean IS_DEEP_LINKING_ENABLED = true;

// Enables custom scheme deep linking (e.g., webviewgold://)
public static final boolean IS_CUSTOM_SCHEME_ENABLED = true;

// Set your desired scheme prefix (must match AndroidManifest.xml)
public static final String CUSTOM_DEEPLINK_SCHEME = "webviewgold";
```

![Config.java for App Link Configuration](../assets/android/img/applinks2.webp)

## Step 3: Verify Domain Ownership (for URL-based Deep Links)

To enable deep linking using HTTPS URLs, you must verify domain ownership with Google. Follow the [**Google Site Verification Guide**](https://developer.android.com/training/app-links/verify-android-applinks).

## Testing Your App Links

You can test both types of links via Android Studio or terminal:

- **Using Android Studio:** Open the **App Links Assistant** from the **Tools** menu for simulation and troubleshooting.
- **Using Terminal or Command Prompt:**
  1. Run the following command:

     ```bash
     adb shell am start -a android.intent.action.VIEW -d "webviewgold://https://www.example.org/subpages/example2" com.webviewgold.myappname
     ```

     - Replace `com.webviewgold.myappname` with your actual app package name.
     - You can also test with a URL link like `https://www.example.org/subpages/example1`.

Once everything is set up, users can open your app directly to any specific page using deep links like:

- `https://www.example.org/subpages/example1`
- `webviewgold://https://www.example.org/subpages/example2`

**Questions?** Ping us anytime!

---

## Continue reading

- ← Previous: [Flashlight API](flashlight.md)
- Next →: [ShareIntent API](share-intent.md)
- Same feature on other platforms: [iOS – Universal Links API](../ios/universal-links.md)
- Languages: **🇺🇸 English** · [🇩🇪 Deutsch](../de/android/app-links.md) · [🇫🇷 Français](../fr/android/app-links.md) · [🇪🇸 Español](../es/android/app-links.md) · [🇨🇳 中文](../zh/android/app-links.md)

> [!TIP]
> **Too busy? We set up your app for you.** Our team configures, builds & submits your WebViewGold app — done-for-you, fast turnaround, Made in Germany. [Get your app set up →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_android_doc_online)
>
> **Build in your browser:** No Mac, no IDE: the **WebViewGold Cloud Builder** configures, builds & uploads your app online. [Discover Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=android_docs)
