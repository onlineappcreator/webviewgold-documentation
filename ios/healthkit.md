---
title: "HealthKit Plugin – WebViewGold for iOS Documentation"
description: "Connect your web app to Apple HealthKit and read health data with user permission on iOS."
lang: "en"
product: "WebViewGold for iOS"
platform: "iOS"
category: "Extensions & Plugins"
slug: "healthkit"
canonical_url: "https://www.webviewgold.com/docs/iOS/healthkit/"
keywords:
  - "HealthKit Plugin"
  - "WebViewGold for iOS"
  - "convert website to app"
  - "WebView app documentation"
  - "iOS WebView SDK"
  - "PWA to app"
  - "HTML to app"
  - "JavaScript bridge"
last_updated: "2026-10-09"
---

# HealthKit Plugin – WebViewGold for iOS

> **Summary:** Connect your web app to Apple HealthKit and read health data with user permission on iOS.

[Documentation](../README.md) › [WebViewGold for iOS](README.md) › HealthKit Plugin

**Platform:** iOS · **Category:** Extensions & Plugins · **Online version:** [www.webviewgold.com/docs/iOS/healthkit/](https://www.webviewgold.com/docs/iOS/healthkit/)

---

Activate HealthKit features by setting `static let HealthKitEnabled` in `Config.swift` to your plugin token and adding the HealthKit capability.\
Contact [webviewgold-healthkit@onlineappcreator.com](mailto:webviewgold-healthkit@onlineappcreator.com) for details.

## API Usage (once activated)

**Read** a HealthKit value by calling `readhealthkit://` followed by a [HealthKit identifier](https://developer.apple.com/documentation/healthkit/hkquantitytypeidentifier). The result is injected into your web app as a JavaScript variable named after the identifier (containing value and unit as a string):

```html
<a href="readhealthkit://HKQuantityTypeIdentifierStepCount" onclick="setTimeout(function(){ alert(HKQuantityTypeIdentifierStepCount); }, 500)">Read step count</a>
```

**Write** a HealthKit value using the `writehealthkit://Identifier//Value` syntax:

```html
<a href="writehealthkit://HKQuantityTypeIdentifierStepCount//100">Save 100 steps</a>
```

**Note:** Requires the HealthKit capability and the *Privacy - Health Share Usage Description* / *Privacy - Health Update Usage Description* entries in **Info.plist**.

---

## Continue reading

- ← Previous: [Siri Plugin](siri.md)
- Next →: [Build & Publish](publish.md)
- Same feature on other platforms: [Android – Health Connect API](../android/health-connect.md)
- Languages: **🇺🇸 English** · [🇩🇪 Deutsch](../de/ios/healthkit.md) · [🇫🇷 Français](../fr/ios/healthkit.md) · [🇪🇸 Español](../es/ios/healthkit.md) · [🇨🇳 中文](../zh/ios/healthkit.md)

> [!TIP]
> **Too busy? We set up your app for you.** Our team configures, builds & submits your WebViewGold app — done-for-you, fast turnaround, Made in Germany. [Get your app set up →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **Build in your browser:** No Mac, no IDE: the **WebViewGold Cloud Builder** configures, builds & uploads your app online. [Discover Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
