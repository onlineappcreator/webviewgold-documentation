---
title: "In-App Rating Dialog API – WebViewGold for Android Documentation"
description: "Ask your users for a Google Play review: trigger a native \"Rate this app\" dialog from your web app via rateapp:// or let WebViewGold show it automatically."
lang: "en"
product: "WebViewGold for Android"
platform: "Android"
category: "APIs & Features"
slug: "in-app-rating"
canonical_url: "https://www.webviewgold.com/docs/android/in-app-rating/"
keywords:
  - "In-App Rating API"
  - "WebViewGold for Android"
  - "convert website to app"
  - "WebView app documentation"
  - "Android WebView SDK"
  - "PWA to app"
  - "HTML to app"
  - "JavaScript bridge"
last_updated: "2026-10-09"
---

# In-App Rating Dialog API – WebViewGold for Android

> **Summary:** Ask your users for a Google Play review: trigger a native "Rate this app" dialog from your web app via rateapp:// or let WebViewGold show it automatically.

[Documentation](../README.md) › [WebViewGold for Android](README.md) › In-App Rating API

**Platform:** Android · **Category:** APIs & Features · **Online version:** [www.webviewgold.com/docs/android/in-app-rating/](https://www.webviewgold.com/docs/android/in-app-rating/)

---

Positive Google Play reviews are one of the most powerful growth drivers for your app. The **In-App Rating Dialog API** of WebViewGold lets you ask your users for a rating at exactly the right moment — for example, right after a successful purchase or after they completed a task in your web app.

## Option 1: Trigger the rating dialog manually from your web app

Call the following URL from an HTML link or from JavaScript to show a native "Rate this app" dialog:

```html
<a href="rateapp://">Enjoying the app? Rate us!</a>
```

```javascript
window.location.href = "rateapp://";
```

If the user confirms the dialog, the Google Play page of your app opens so they can leave a review. For this to work, set `RATE_MY_APP_URL` in **Config.java** to the Google Play URL of your app:

```java
public static final String RATE_MY_APP_URL = "https://play.google.com/store/apps/details?id=com.yourcompany.yourapp";
```

**Note:** If `RATE_MY_APP_URL` is empty, `rateapp://` calls are ignored. The title and message of the dialog can be customized via the `rate_title` and `rate_message` entries in **strings.xml**.

## Option 2: Let WebViewGold ask automatically

WebViewGold can also show a "Rate this app" prompt automatically after the user has used your app for a while. Configure this behavior in **Config.java**:

- `SHOW_RATE_DIALOG` — set to `true` to enable the automatic rating prompt (or `false` to disable it).
- `RATE_DAYS_UNTIL_PROMPT` — minimum number of days after installation before the prompt is displayed.
- `RATE_LAUNCHES_UNTIL_PROMPT` — minimum number of app launches before the prompt is displayed.

## Typical Use Cases

- Ask for a review right after a positive interaction (completed order, level up, successful booking).
- Show your own custom "Do you like the app?" flow on your website first, and only send happy users to `rateapp://`.

---

## Continue reading

- ← Previous: [App Sharing Dialog API](app-sharing-dialog.md)
- Next →: [In-App Purchases API](in-app-purchases.md)
- Same feature on other platforms: [iOS – In-App Rating Dialog API](../ios/in-app-rating.md)
- Languages: **🇺🇸 English** · [🇩🇪 Deutsch](../de/android/in-app-rating.md) · [🇫🇷 Français](../fr/android/in-app-rating.md) · [🇪🇸 Español](../es/android/in-app-rating.md) · [🇨🇳 中文](../zh/android/in-app-rating.md)

> [!TIP]
> **Too busy? We set up your app for you.** Our team configures, builds & submits your WebViewGold app — done-for-you, fast turnaround, Made in Germany. [Get your app set up →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_android_doc_online)
>
> **Build in your browser:** No Mac, no IDE: the **WebViewGold Cloud Builder** configures, builds & uploads your app online. [Discover Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=android_docs)
