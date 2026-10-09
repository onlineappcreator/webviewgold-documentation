---
title: "WebViewGold for Android Documentation – Convert Website to Android App"
description: "Official WebViewGold for Android documentation: convert your website to a native Android app in minutes — setup guide, 30+ APIs & features, and Google Play publishing."
lang: "en"
product: "WebViewGold for Android"
platform: "Android"
canonical_url: "https://www.webviewgold.com/docs/android/"
keywords:
  - "WebViewGold for Android"
  - "convert website to app"
  - "WebView app documentation"
  - "Android WebView SDK"
  - "PWA to app"
  - "HTML to app"
  - "JavaScript bridge"
last_updated: "2026-10-09"
---

# WebViewGold for Android Documentation

![WebViewGold for Android](../assets/android/img/header.webp)

> Official WebViewGold for Android documentation: convert your website to a native Android app in minutes — setup guide, 30+ APIs & features, and Google Play publishing.

[Documentation](../README.md) › WebViewGold for Android

Convert your website, PWA, SaaS dashboard, e-commerce storefront, or AI-generated web app into a native Android app in minutes. Use WebViewGold like a lightweight app SDK: configure your URL, enable native APIs, integrate JavaScript bridge commands, and publish a store-ready app without rebuilding your web product from scratch.

WebViewGold works with classic HTML/PHP sites, WordPress, jQuery Mobile projects, and modern web apps created with Lovable, Base44, Bolt, Bubble, React, Vue, Angular, or similar builders. The documentation below explains the setup flow, native feature APIs, security considerations, and publishing steps in a technical, implementation-focused format.

**[Start the guide →](setup-website.md)** · [Download WebViewGold](https://www.webviewgold.com/download/android) · [Cloud Builder](https://www.webviewgold.com/cloud-builder?ref=android_docs)

## Quick start

Three steps from website to published app:

1. **[Set up your web app](setup-website.md)** — Use a remote URL, bundle local HTML files, or combine both with an offline fallback.
2. **[Configure WebViewGold](setup.md)** — Insert your URL and fine-tune every option in one simple config file — no coding needed.
3. **[Build & publish](publish.md)** — Ship your app to the store — yourself, via Cloud Builder, or with our publishing service.

## What’s new

WebViewGold is updated regularly. See the full changelog [here](https://www.webviewgold.com/changelog/android/).

## All topics, APIs & features

Everything WebViewGold for Android can do — each topic on its own page:

### Get Started

- **[Set up your web app](setup-website.md)** — Prepare your website, PWA, or local HTML files for your Android app: use a remote URL, bundle files offline in the app, or combine both with an offline fallback.
- **[Configure WebViewGold](setup.md)** — Download the WebViewGold Android Studio template, insert your URL, and explore every built-in configuration option — no coding skills required.

### App Design

- **[App Icon](app-icon.md)** — Add your custom app icon to your WebViewGold Android app in Android Studio — step by step.
- **[Splash Screen](splash-screen.md)** — Customize the splash/launch screen of your Android WebView app with your own graphics.
- **[Navigation Drawer & Footer](navigation-drawer.md)** — Ship an app-like navigation experience with the built-in Material navigation drawer and Material 3 bottom navigation bar — no changes to your website required.

### APIs & Features

- **[URL Handling API](url-handling.md)** — Decide which links open inside your Android app, in Chrome Custom Tabs, or in the external browser.
- **[Custom CSS & JS API](custom-css-js.md)** — Inject custom CSS styles and JavaScript code into any page of your Android WebView app — perfect for app-only tweaks.
- **[Multi API Call](multi-api-call.md)** — Call several WebViewGold data APIs in one single window.location.href assignment — ideal for cross-platform web apps that also target the iOS version.
- **[Geolocation API](geolocation.md)** — Enable HTML5 geolocation in your Android WebView app and request location permissions properly.
- **[Push Notifications API](push-notifications.md)** — Send push notifications to your Android app users with OneSignal, Firebase, or Pushwoosh — setup, deep links, and per-user targeting explained.
- **[AdMob Ads API](admob.md)** — Monetize your Android app with Google AdMob banner and interstitial ads — configuration and JavaScript triggers.
- **[Facebook Ads API](facebook-ads.md)** — Show Facebook Audience Network banner and interstitial ads in your WebViewGold Android app.
- **[File Downloader API](file-downloader.md)** — Let users download images, PDFs, and other files from your web app to their Android device.
- **[Native Video (PiP) API](native-video.md)** — Play videos natively with Picture-in-Picture support in your Android WebView app.
- **[Reset App API](reset-app.md)** — Reset cache, cookies, and local storage of your Android WebView app with a single link or JavaScript call.
- **[Loading Sign API](loading-sign.md)** — Show or hide the native loading indicator on demand and customize the loading experience of your Android app.
- **[Clipboard API](clipboard.md)** — Copy text to the Android clipboard and read clipboard content from your web app via JavaScript.
- **[UUID API](uuid.md)** — Identify app installations with a unique UUID appended to your WebView URL or retrieved via JavaScript.
- **[Flashlight API](flashlight.md)** — Control the device flashlight from your web app with simple JavaScript links in WebViewGold for Android.
- **[App Links / Deep Linking](app-links.md)** — Open links to your domain directly in your Android app with App Links and custom URL scheme deep linking.
- **[ShareIntent API](share-intent.md)** — Receive content shared from other Android apps directly in your WebView app via Share Intents.
- **[App Sharing Dialog API](app-sharing-dialog.md)** — Trigger the native Android share dialog from your web app to let users share your app or any URL.
- **[In-App Rating API](in-app-rating.md)** — Ask your users for a Google Play review: trigger a native "Rate this app" dialog from your web app via rateapp:// or let WebViewGold show it automatically.
- **[In-App Purchases API](in-app-purchases.md)** — Sell digital goods and subscriptions in your Android WebView app with Google Play Billing.
- **[IAP History API](iap-history.md)** — Return the user's Google Play purchase history as window.purchaseHistory so your web app can list subscriptions or unlock premium content client-side.
- **[QR Code Scanner API](qr-code-scanner.md)** — Open a native QR code scanner from your web app and process scan results via URL or JavaScript.
- **[Scanning Mode API](scanning-mode.md)** — Fine-tune the camera scanning behavior of the QR and barcode scanner in WebViewGold for Android.
- **[Barcode Scanner API](barcode-scanner.md)** — Scan EAN, UPC, and other barcodes natively in your Android WebView app and hand results to your web app.
- **[Take Screenshot API](take-screenshot.md)** — Capture a screenshot of the current app screen programmatically and share or save it — via JavaScript.
- **[App Version Check API](app-version-check.md)** — Detect the installed app version from your web app and prompt users to update when needed.
- **[Contacts API](contacts.md)** — Access the device address book from your web app: read contacts with user permission in WebViewGold for Android.
- **[Dynamic UI API](dynamic-ui.md)** — Change native UI elements like the status bar color dynamically from your web app on Android.
- **[Haptic Feedback API](haptic-feedback.md)** — Trigger native vibration haptic feedback from your web app for a native app feeling on Android.
- **[NFC Plugin](nfc.md)** — Read NFC tags natively in your Android WebView app and pass tag data to your web app.
- **[Open App Settings API](open-app-settings.md)** — Send the user straight to the system App-info screen from your web app to manage permissions, notifications, storage, or force-stop your Android app.
- **[Reconnect API](reconnect.md)** — Reload the last online URL from your offline / fallback HTML page — the perfect "Try again" button for your custom offline screen.
- **[Read/Write Value API](read-write-value.md)** — Persist small strings on the device from JavaScript and read them back — for theme, language, session tokens, or onboarding state.
- **[Biometric Auth API](biometric-auth.md)** — Prompt fingerprint or face authentication with the native Android BiometricPrompt directly from your web app.
- **[Document Scanner](document-scanner.md)** — Add a Scan document option to the file upload dialog — the user scans up to 5 pages and your web app receives a PDF like any other upload.
- **[Printer API](printer.md)** — Send a remote image or PDF to the Android system print dialog — Wi-Fi printers, cloud print, or Save-as-PDF, straight from your web app.
- **[Health Connect API](health-connect.md)** — Read and write Android Health Connect records from JavaScript — mirrors the WebViewGold HealthKit API on iOS so one web app covers both platforms.

### Build & Publish

- **[Firebase Crashlytics](crashlytics.md)** — Ship crash reports and non-fatal events to your Firebase project, with runtime opt-in / opt-out from your web app.
- **[Build & Publish](publish.md)** — Publish your WebView app to the Google Play Store: full publishing service, manual process, and changing the package name.

### More

- **[Credits & Licenses](credits.md)** — License terms for WebViewGold for Android, when you need an Envato Extended License, and open source credits.
- **[Rate WebViewGold](rate.md)** — Enjoying WebViewGold? Rate it on CodeCanyon in seconds — it keeps updates coming.
- **[iOS & macOS versions](more-platforms.md)** — Ship your app on more platforms: get WebViewGold for iOS and macOS and reuse the same web app.
- **[Support & Contact](support.md)** — Get help fast: browse the WebViewGold Support Center, contact our team directly, or request professional custom app development made in Germany.

## One web app, every platform

Reuse the same website for iOS, Android & macOS apps with WebViewGold.

- [WebViewGold for iOS](../ios/README.md)
- [WebViewGold for macOS](../macos/README.md)

**Languages:** **🇺🇸 English** · [🇩🇪 Deutsch](../de/android/README.md) · [🇫🇷 Français](../fr/android/README.md) · [🇪🇸 Español](../es/android/README.md) · [🇨🇳 中文](../zh/android/README.md)

> [!TIP]
> **Too busy? We set up your app for you.** Our team configures, builds & submits your WebViewGold app — done-for-you, fast turnaround, Made in Germany. [Get your app set up →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_android_doc_online)
>
> **Build in your browser:** No Mac, no IDE: the **WebViewGold Cloud Builder** configures, builds & uploads your app online. [Discover Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=android_docs)
