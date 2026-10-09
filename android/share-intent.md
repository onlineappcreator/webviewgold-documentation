---
title: "ShareIntent API – WebViewGold for Android Documentation"
description: "Receive content shared from other Android apps directly in your WebView app via Share Intents."
lang: "en"
product: "WebViewGold for Android"
platform: "Android"
category: "APIs & Features"
slug: "share-intent"
canonical_url: "https://www.webviewgold.com/docs/android/share-intent/"
keywords:
  - "ShareIntent API"
  - "WebViewGold for Android"
  - "convert website to app"
  - "WebView app documentation"
  - "Android WebView SDK"
  - "PWA to app"
  - "HTML to app"
  - "JavaScript bridge"
last_updated: "2026-10-09"
---

# ShareIntent API – WebViewGold for Android

> **Summary:** Receive content shared from other Android apps directly in your WebView app via Share Intents.

[Documentation](../README.md) › [WebViewGold for Android](README.md) › ShareIntent API

**Platform:** Android · **Category:** APIs & Features · **Online version:** [www.webviewgold.com/docs/android/share-intent/](https://www.webviewgold.com/docs/android/share-intent/)

---

The WebViewGold **ShareIntent API** enables your app to appear as a target in Android’s native Share dialog. This allows users to share content such as text, URLs, or images (as base64 strings) from any other app directly into your WebView-based app.

## Use Cases

- Sharing links to user profiles, notes, or articles directly into your app
- Receiving content from messaging or browser apps
- Sending images from the gallery to your WebView interface (base64-encoded)

## Step 1: Enable Sharing Support in AndroidManifest.xml

To allow your app to receive shared data, uncomment the relevant intent filters in your **AndroidManifest.xml** file:

```html
<!-- Receive shared text (e.g., URLs or notes) -->
<intent-filter>
    <action android:name="android.intent.action.SEND" />
    <category android:name="android.intent.category.DEFAULT" />
    <data android:mimeType="text/plain" />
</intent-filter>

<!-- Receive a single shared image -->
<intent-filter>
    <action android:name="android.intent.action.SEND" />
    <category android:name="android.intent.category.DEFAULT" />
    <data android:mimeType="image/*" />
</intent-filter>

<!-- Receive multiple shared images -->
<intent-filter>
    <action android:name="android.intent.action.SEND_MULTIPLE" />
    <category android:name="android.intent.category.DEFAULT" />
    <data android:mimeType="image/*" />
</intent-filter>
```

Once these filters are active, your WebViewGold-based app icon will appear as a sharing target whenever users share content from another app.

## Step 2: Handle Shared Data in Your WebView

When a user shares content to your app, WebViewGold will automatically inject the shared content into a JavaScript variable named `sharedData`.

```html
<script>
    alert(sharedData); // Displays the shared content (text or base64 image)

</script>
```

- **Text or URL:** Will be passed as plain text into `sharedData`
- **Image:** Will be converted to a base64-encoded string and passed into `sharedData`

**Example Use:** Automatically populate a form or preview an image based on the received content:

```html
<script>
    if (sharedData) {
        document.getElementById("myInput").value = sharedData;
    }
</script>
```

**Note:** Ensure that your JavaScript is ready to handle both plain text and long base64 strings. You may also implement client-side checks to distinguish between different content types.

---

## Continue reading

- ← Previous: [App Links / Deep Linking](app-links.md)
- Next →: [App Sharing Dialog API](app-sharing-dialog.md)
- Same feature on other platforms: [iOS – Share Extension](../ios/share-extension.md)
- Languages: **🇺🇸 English** · [🇩🇪 Deutsch](../de/android/share-intent.md) · [🇫🇷 Français](../fr/android/share-intent.md) · [🇪🇸 Español](../es/android/share-intent.md) · [🇨🇳 中文](../zh/android/share-intent.md)

> [!TIP]
> **Too busy? We set up your app for you.** Our team configures, builds & submits your WebViewGold app — done-for-you, fast turnaround, Made in Germany. [Get your app set up →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_android_doc_online)
>
> **Build in your browser:** No Mac, no IDE: the **WebViewGold Cloud Builder** configures, builds & uploads your app online. [Discover Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=android_docs)
