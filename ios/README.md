---
title: "WebViewGold for iOS Documentation – Convert Website to iOS App"
description: "Official WebViewGold for iOS documentation: convert your website to a native iOS app in minutes — setup guide, 40+ APIs & features, and App Store publishing."
lang: "en"
product: "WebViewGold for iOS"
platform: "iOS"
canonical_url: "https://www.webviewgold.com/docs/iOS/"
keywords:
  - "WebViewGold for iOS"
  - "convert website to app"
  - "WebView app documentation"
  - "iOS WebView SDK"
  - "PWA to app"
  - "HTML to app"
  - "JavaScript bridge"
last_updated: "2026-10-09"
---

# WebViewGold for iOS Documentation

![WebViewGold for iOS](../assets/ios/img/header.webp)

> Official WebViewGold for iOS documentation: convert your website to a native iOS app in minutes — setup guide, 40+ APIs & features, and App Store publishing.

[Documentation](../README.md) › WebViewGold for iOS

Convert your website, PWA, SaaS dashboard, e-commerce storefront, or AI-generated web app into a native iOS app in minutes. Use WebViewGold like a lightweight app SDK: configure your URL, enable native APIs, integrate JavaScript bridge commands, and publish a store-ready app without rebuilding your web product from scratch.

WebViewGold works with classic HTML/PHP sites, WordPress, jQuery Mobile projects, and modern web apps created with Lovable, Base44, Bolt, Bubble, React, Vue, Angular, or similar builders. The documentation below explains the setup flow, native feature APIs, security considerations, and publishing steps in a technical, implementation-focused format.

**[Start the guide →](setup-website.md)** · [Download WebViewGold](https://www.webviewgold.com/download/ios) · [Cloud Builder](https://www.webviewgold.com/cloud-builder?ref=ios_docs)

## Quick start

Three steps from website to published app:

1. **[Set up your web app](setup-website.md)** — Use a remote URL, bundle local HTML files, or combine both with an offline fallback.
2. **[Configure WebViewGold](setup.md)** — Insert your URL and fine-tune every option in one simple config file — no coding needed.
3. **[Build & publish](publish.md)** — Ship your app to the store — yourself, via Cloud Builder, or with our publishing service.

## What’s new

WebViewGold is updated regularly. See the full changelog [here](https://www.webviewgold.com/changelog/ios/).

## All topics, APIs & features

Everything WebViewGold for iOS can do — each topic on its own page:

### Get Started

- **[Set up your web app](setup-website.md)** — Prepare your website, PWA, or local HTML files for your iOS app: use a remote URL, bundle files offline in the app, or combine both with an offline fallback.
- **[Configure WebViewGold](setup.md)** — Download the WebViewGold Xcode template, insert your URL in Config.swift, and explore every built-in configuration option — no coding skills required.

### App Design

- **[Name, Icon & Splash](app-name-icon-splash.md)** — Rename your iOS app, add a custom app icon, and set up personalized splash screen graphics for your WebViewGold app.
- **[Modify Safe Area](safe-area.md)** — Adjust the safe area and enable the custom bottom bar so your web app looks perfect on iPhones with a Home bar.

### APIs & Features

- **[Geolocation API](geolocation.md)** — Enable HTML5 geolocation in your iOS WebView app and request precise location permissions the right way.
- **[Push Notifications API](push-notifications.md)** — Send push notifications to your iOS app users with OneSignal, Firebase, or Pushwoosh — setup, deep links, and per-user targeting explained.
- **[AdMob Ads API](admob.md)** — Monetize your iOS app with Google AdMob banner, interstitial, and rewarded ads — configuration and JavaScript triggers.
- **[Facebook Ads API](facebook-ads.md)** — Show Facebook Audience Network banner and interstitial ads in your WebViewGold iOS app.
- **[HTML Audio API](html-audio.md)** — Keep HTML audio playing in the background of your iOS WebView app — even when the screen is locked.
- **[Native Video API](native-video.md)** — Play video streams in the native iOS video player with Picture-in-Picture support — triggered straight from your web app.
- **[File Downloader API](file-downloader.md)** — Let users download images, PDFs, and other files from your web app straight to their iPhone or iPad.
- **[Printer API](printer.md)** — Print images and PDFs from your web app via AirPrint: send files to the native iOS print dialog with a single link.
- **[iCal Calendar API](ical-calendar.md)** — Add calendar events from your web app to the native iOS calendar using the iCal Calendar API.
- **[Apple Wallet Pass API](wallet-pass.md)** — Let users add .pkpass passes (tickets, coupons, membership cards) from your web app to Apple Wallet.
- **[UUID API](uuid.md)** — Identify app installations with a unique UUID appended to your WebView URL or retrieved via JavaScript.
- **[Flashlight API](flashlight.md)** — Control the device flashlight from your web app with simple JavaScript links in WebViewGold for iOS.
- **[Reset App API](reset-app.md)** — Reset cache, cookies, and local storage of your iOS WebView app with a single link or JavaScript call.
- **[User Tracking Decision API](user-tracking.md)** — Respect App Tracking Transparency: read and react to the user's tracking decision inside your WebViewGold iOS app.
- **[Loading Sign API](loading-sign.md)** — Show or hide the native loading indicator on demand and customize the loading experience of your iOS app.
- **[Pull-to-Refresh API](pull-to-refresh.md)** — Enable the native pull-to-refresh gesture in your iOS WebView app, customize its colors, and toggle it dynamically from your web app.
- **[URL Handling API](url-handling.md)** — Decide which links open inside your app, in an in-app browser tab, or in Safari — full URL handling control for iOS.
- **[Social Login Helper](social-login.md)** — Make Google, Facebook, and Apple OAuth logins work reliably inside your iOS WebView app with the built-in social login helpers.
- **[Reconnect API](reconnect.md)** — Add a "Try again" button to your offline fallback page that reloads the last online URL of your iOS app.
- **[Custom CSS & JS API](custom-css-js.md)** — Inject custom CSS styles and JavaScript code into any page of your iOS WebView app — perfect for app-only tweaks.
- **[Universal Links API](universal-links.md)** — Open links to your domain directly in your iOS app with Apple Universal Links — setup, AASA file, and troubleshooting.
- **[Deep Linking API](deep-linking.md)** — Launch your iOS app via custom URL schemes and deep link users to specific pages of your web app.
- **[App Sharing Dialog API](app-sharing-dialog.md)** — Trigger the native iOS share sheet from your web app to let users share your app or any URL.
- **[In-App Rating Dialog API](in-app-rating.md)** — Ask users for an App Store rating at the perfect moment — trigger the native iOS rating dialog from your web app.
- **[In-App Purchases API](in-app-purchases.md)** — Sell digital goods and subscriptions in your iOS WebView app with StoreKit-powered In-App Purchases.
- **[IAP History API](iap-history.md)** — Read the user's previous in-app purchases from your web app as JSON — perfect for "My purchases" pages.
- **[QR Code Scanner API](qr-code-scanner.md)** — Open a native QR code scanner from your web app and process scan results via URL or JavaScript.
- **[Barcode Scanner API](barcode-scanner.md)** — Scan EAN, UPC, and other barcodes natively in your iOS WebView app and hand results to your web app.
- **[Scanning Mode API](scanning-mode.md)** — Fine-tune the camera scanning behavior of the QR and barcode scanner in WebViewGold for iOS.
- **[Document Scanner](document-scanner.md)** — Let users scan paper documents with the camera and upload them through your web app's file upload — powered by Apple VisionKit.
- **[Take Screenshot API](take-screenshot.md)** — Capture a screenshot of the current app screen programmatically and share or save it — via JavaScript.
- **[App Version Check API](app-version-check.md)** — Detect the installed app version from your web app and prompt users to update when needed.
- **[Dynamic UI API](dynamic-ui.md)** — Change native UI elements like the status bar or bottom bar colors dynamically from your web app.
- **[Dynamic App Icon API](dynamic-app-icon.md)** — Switch between alternative app icons at runtime in your iOS WebView app — triggered from your web app.
- **[Contacts API](contacts.md)** — Access the device address book from your web app: read contacts with user permission in WebViewGold for iOS.
- **[Biometric Auth API](biometric-authentication.md)** — Protect your iOS app with Face ID or Touch ID and verify users biometrically from your web app.
- **[Haptic Feedback API](haptic-feedback.md)** — Trigger native haptic feedback (vibrations) from your web app for a truly native app feeling on iOS.
- **[Shortcut API](shortcut.md)** — Add Home Screen quick action shortcuts to your iOS app that deep link into specific pages.
- **[Clipboard API](clipboard.md)** — Copy text to the iOS clipboard and read clipboard content from your web app via JavaScript.
- **[Read/Write Value API](read-write-value.md)** — Persistently store a string value on the device and read it back into your web app's JavaScript.
- **[Open App Settings API](open-app-settings.md)** — Send users straight to your app's page in the iOS Settings app to manage permissions and notifications.

### Extensions & Plugins

- **[Share Extension](share-extension.md)** — Let users share content from other apps directly into your iOS WebView app with a Share Extension.
- **[Widget Extension](widget-extension.md)** — Add a Home Screen widget to your iOS WebView app that links users straight into your web app.
- **[App Clip Extension](app-clip.md)** — Offer a lightweight App Clip version of your iOS app that opens instantly without installation.
- **[Native Navigation Footer](navigation-footer.md)** — Enable a native bottom navigation bar with back, forward, and custom buttons in your iOS app.
- **[Native Sidebar](sidebar.md)** — Enable a native sliding sidebar menu with custom links and SF Symbols icons — configured via Sidebar.json.
- **[Screen Capture Detection](screen-capture.md)** — Detect screenshots and screen recordings in your iOS app and react from your web app.
- **[MultiAPICall Feature](multi-api-call.md)** — Chain multiple WebViewGold API calls in a single request with the MultiAPICall feature for iOS.
- **[NFC Plugin](nfc.md)** — Read NFC tags natively in your iOS WebView app and pass tag data to your web app.
- **[Siri Plugin](siri.md)** — Add Siri Shortcuts support to your iOS WebView app and open app content by voice.
- **[HealthKit Plugin](healthkit.md)** — Connect your web app to Apple HealthKit and read health data with user permission on iOS.

### Build & Publish

- **[Build & Publish](publish.md)** — Publish your WebView app to the Apple App Store: full publishing service, manual process, and changing the bundle identifier.

### More

- **[Credits & Licenses](credits.md)** — License terms for WebViewGold for iOS, when you need an Envato Extended License, and open source credits.
- **[Rate WebViewGold](rate.md)** — Enjoying WebViewGold? Rate it on CodeCanyon in seconds — it keeps updates coming.
- **[Android & macOS versions](more-platforms.md)** — Ship your app on more platforms: get WebViewGold for Android and macOS and reuse the same web app.
- **[Support & Contact](support.md)** — Get help fast: browse the WebViewGold Support Center, contact our team directly, or request professional custom app development made in Germany.

## One web app, every platform

Reuse the same website for iOS, Android & macOS apps with WebViewGold.

- [WebViewGold for Android](../android/README.md)
- [WebViewGold for macOS](../macos/README.md)

**Languages:** **🇺🇸 English** · [🇩🇪 Deutsch](../de/ios/README.md) · [🇫🇷 Français](../fr/ios/README.md) · [🇪🇸 Español](../es/ios/README.md) · [🇨🇳 中文](../zh/ios/README.md)

> [!TIP]
> **Too busy? We set up your app for you.** Our team configures, builds & submits your WebViewGold app — done-for-you, fast turnaround, Made in Germany. [Get your app set up →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **Build in your browser:** No Mac, no IDE: the **WebViewGold Cloud Builder** configures, builds & uploads your app online. [Discover Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
