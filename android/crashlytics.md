---
title: "Firebase Crashlytics – WebViewGold for Android Documentation"
description: "Ship crash reports and non-fatal events to your Firebase project, with runtime opt-in / opt-out from your web app."
lang: "en"
product: "WebViewGold for Android"
platform: "Android"
category: "Build & Publish"
slug: "crashlytics"
canonical_url: "https://www.webviewgold.com/docs/android/crashlytics/"
keywords:
  - "Firebase Crashlytics"
  - "WebViewGold for Android"
  - "convert website to app"
  - "WebView app documentation"
  - "Android WebView SDK"
  - "PWA to app"
  - "HTML to app"
  - "JavaScript bridge"
last_updated: "2026-10-09"
---

# Firebase Crashlytics – WebViewGold for Android

> **Summary:** Ship crash reports and non-fatal events to your Firebase project, with runtime opt-in / opt-out from your web app.

[Documentation](../README.md) › [WebViewGold for Android](README.md) › Firebase Crashlytics

**Platform:** Android · **Category:** Build & Publish · **Online version:** [www.webviewgold.com/docs/android/crashlytics/](https://www.webviewgold.com/docs/android/crashlytics/)

---

**Firebase Crashlytics** integration sends anonymous crash reports and non-fatal events to your Firebase project, so you can spot stability issues in production.

## How to Enable

1. Set up Firebase for your app and drop `google-services.json` into `AndroidStudioSourceCode/app/`.
2. In **Config.java**, turn tracking on:

   ```java
   public static final boolean TRACKING_EVENT = true;
   ```

`TRACKING_EVENT = false` disables all tracking-related features, including Crashlytics event logging and the `starttracking://` / `endtracking://` triggers.

## Runtime Opt-In / Opt-Out from Your Web App

WebViewGold respects a per-user tracking flag that is persisted on the device. Use the standard tracking triggers to change it at runtime:

```html
<a href="starttracking://">Enable analytics & crash reports</a>
<a href="endtracking://">Disable analytics & crash reports</a>
```

When the user is opted out, Crashlytics collection is turned off — nothing is uploaded.

## What Is Reported

- Unhandled crashes (stack traces, device model, OS version).
- Non-fatal exceptions logged internally by the app shell.
- No personal user data is attached by default.

**Where to View the Reports:** Open your **Firebase Console → Crashlytics** dashboard. Reports usually appear within a few minutes of a crash.

**Notes:** Crashlytics initialization is best-effort — if Firebase is misconfigured, the app still runs normally. Consider adding a consent screen (GDPR / CCPA) before calling `starttracking://` for the first time.

---

## Continue reading

- ← Previous: [Health Connect API](health-connect.md)
- Next →: [Build & Publish](publish.md)
- Languages: **🇺🇸 English** · [🇩🇪 Deutsch](../de/android/crashlytics.md) · [🇫🇷 Français](../fr/android/crashlytics.md) · [🇪🇸 Español](../es/android/crashlytics.md) · [🇨🇳 中文](../zh/android/crashlytics.md)

> [!TIP]
> **Too busy? We set up your app for you.** Our team configures, builds & submits your WebViewGold app — done-for-you, fast turnaround, Made in Germany. [Get your app set up →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_android_doc_online)
>
> **Build in your browser:** No Mac, no IDE: the **WebViewGold Cloud Builder** configures, builds & uploads your app online. [Discover Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=android_docs)
