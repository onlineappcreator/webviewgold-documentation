---
title: "HTML5 Geolocation API – WebViewGold for Android Documentation"
description: "Enable HTML5 geolocation in your Android WebView app and request location permissions properly."
lang: "en"
product: "WebViewGold for Android"
platform: "Android"
category: "APIs & Features"
slug: "geolocation"
canonical_url: "https://www.webviewgold.com/docs/android/geolocation/"
keywords:
  - "Geolocation API"
  - "WebViewGold for Android"
  - "convert website to app"
  - "WebView app documentation"
  - "Android WebView SDK"
  - "PWA to app"
  - "HTML to app"
  - "JavaScript bridge"
last_updated: "2026-10-09"
---

# HTML5 Geolocation API – WebViewGold for Android

> **Summary:** Enable HTML5 geolocation in your Android WebView app and request location permissions properly.

[Documentation](../README.md) › [WebViewGold for Android](README.md) › Geolocation API

**Platform:** Android · **Category:** APIs & Features · **Online version:** [www.webviewgold.com/docs/android/geolocation/](https://www.webviewgold.com/docs/android/geolocation/)

---

The HTML5 Geolocation API enables users to share their location with your app, enhancing features like location-based content. In WebViewGold, the Geolocation API is supported by default once integrated into your web content. Here is how to implement Geolocation tracking into your WebView-based Android app:

## Setting up HTML5 Geolocation

For basic Geolocation setup, refer to [Mozilla's Geolocation Guide](https://developer.mozilla.org/en-US/docs/Web/API/Geolocation_API) for details on how to implement this feature into your website or web app.

For a demonstration, visit this [W3Schools Geolocation Demo](https://www.w3schools.com/html/html5_geolocation.asp).

## Enabling Background Location Tracking (Android Only)

To enable background location tracking for your WebView-based Android app, follow these steps:

1. Set permissions in **Config.java**:
   - Set `requireBackgroundLocation` to `true` if background location tracking is needed.
   - Make sure `requireLocation` is also set to `true` to activate any location services.
2. Adjust permissions in **AndroidManifest.xml**:
   - Uncomment the permission blocks for `android.permission.FOREGROUND_SERVICE_LOCATION` and `GPSService`.
   - Search for these terms within the file to ensure the correct permissions are set.

## Toggling Background Location Tracking with URL Schemes

Use the following URL schemes to turn background location tracking on or off within your WebView-based Android app:

To turn on background location tracking, redirect the user to the following URL:

```html
<script>window.location.href = "backgroundlocationon://";  </script>
```

To turn off background location tracking, redirect the user to the following URL:

```html
<script>window.location.href = "backgroundlocationoff://";  </script>
```

**Note:** These URL schemes are specific to WebViewGold for Android and may not work in standard web browsers. To ensure these redirects are only applied for Android app users, consider detecting the User-Agent.

---

## Continue reading

- ← Previous: [Multi API Call](multi-api-call.md)
- Next →: [Push Notifications API](push-notifications.md)
- Same feature on other platforms: [iOS – Geolocation API](../ios/geolocation.md)
- Languages: **🇺🇸 English** · [🇩🇪 Deutsch](../de/android/geolocation.md) · [🇫🇷 Français](../fr/android/geolocation.md) · [🇪🇸 Español](../es/android/geolocation.md) · [🇨🇳 中文](../zh/android/geolocation.md)

> [!TIP]
> **Too busy? We set up your app for you.** Our team configures, builds & submits your WebViewGold app — done-for-you, fast turnaround, Made in Germany. [Get your app set up →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_android_doc_online)
>
> **Build in your browser:** No Mac, no IDE: the **WebViewGold Cloud Builder** configures, builds & uploads your app online. [Discover Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=android_docs)
