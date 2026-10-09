---
title: "Health Connect API – WebViewGold for Android Documentation"
description: "Read and write Android Health Connect records from JavaScript — mirrors the WebViewGold HealthKit API on iOS so one web app covers both platforms."
lang: "en"
product: "WebViewGold for Android"
platform: "Android"
category: "APIs & Features"
slug: "health-connect"
canonical_url: "https://www.webviewgold.com/docs/android/health-connect/"
keywords:
  - "Health Connect API"
  - "WebViewGold for Android"
  - "convert website to app"
  - "WebView app documentation"
  - "Android WebView SDK"
  - "PWA to app"
  - "HTML to app"
  - "JavaScript bridge"
last_updated: "2026-10-09"
---

# Health Connect API – WebViewGold for Android

> **Summary:** Read and write Android Health Connect records from JavaScript — mirrors the WebViewGold HealthKit API on iOS so one web app covers both platforms.

[Documentation](../README.md) › [WebViewGold for Android](README.md) › Health Connect API

**Platform:** Android · **Category:** APIs & Features · **Online version:** [www.webviewgold.com/docs/android/health-connect/](https://www.webviewgold.com/docs/android/health-connect/)

---

The **Health Connect API** reads and writes health records via [Android Health Connect](https://health.google/health-connect-android/). It mirrors the iOS HealthKit functionality of WebViewGold, so you can ship one web app that talks to health data on both platforms. Reads always return **today's totals** for the requested record type.

## Reading a Record

```html
<a href="readhealthkit://StepsRecord" onclick="setTimeout(show, 300)">
  My steps today
</a>

<script>
function show() {
  // Injected variable name matches the sanitized record name.
  alert(StepsRecord); // e.g. "8421.0 steps"
}
</script>
```

## Writing a Record

Format: `writehealthkit://<RecordName>//<value>`

```html
<a href="writehealthkit://StepsRecord//1000">Log 1000 steps</a>
```

On success the app injects `<RecordName> = "WRITE_SUCCESS"`. On failure it injects the error text.

**Supported Records:** Any Health Connect record type your app has requested permission for. Common ones:

- `StepsRecord`
- `HeartRateRecord`
- `WeightRecord`
- `SleepSessionRecord`
- `HydrationRecord`
- `ActiveCaloriesBurnedRecord`
- `DistanceRecord`

## Setup

1. Install **Health Connect** on the device (pre-installed on Android 14+).
2. On first use the app opens the Health Connect permission dialog; the user grants read and/or write for the requested record types.
3. If Health Connect is not supported, the injected value falls back to the string `"Health Connect not supported"`.

**Notes:** Values are returned as `"<number> <unit>"` (e.g. `"75.4 kg"`). Requires Android 8.0 (API 26) or higher.

---

## Continue reading

- ← Previous: [Printer API](printer.md)
- Next →: [Firebase Crashlytics](crashlytics.md)
- Same feature on other platforms: [iOS – HealthKit Plugin](../ios/healthkit.md)
- Languages: **🇺🇸 English** · [🇩🇪 Deutsch](../de/android/health-connect.md) · [🇫🇷 Français](../fr/android/health-connect.md) · [🇪🇸 Español](../es/android/health-connect.md) · [🇨🇳 中文](../zh/android/health-connect.md)

> [!TIP]
> **Too busy? We set up your app for you.** Our team configures, builds & submits your WebViewGold app — done-for-you, fast turnaround, Made in Germany. [Get your app set up →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_android_doc_online)
>
> **Build in your browser:** No Mac, no IDE: the **WebViewGold Cloud Builder** configures, builds & uploads your app online. [Discover Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=android_docs)
