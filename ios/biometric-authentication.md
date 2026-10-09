---
title: "Biometric Authentication API (Face ID / Touch ID) – WebViewGold for iOS Documentation"
description: "Protect your iOS app with Face ID or Touch ID and verify users biometrically from your web app."
lang: "en"
product: "WebViewGold for iOS"
platform: "iOS"
category: "APIs & Features"
slug: "biometric-authentication"
canonical_url: "https://www.webviewgold.com/docs/iOS/biometric-authentication/"
keywords:
  - "Biometric Auth API"
  - "WebViewGold for iOS"
  - "convert website to app"
  - "WebView app documentation"
  - "iOS WebView SDK"
  - "PWA to app"
  - "HTML to app"
  - "JavaScript bridge"
last_updated: "2026-10-09"
---

# Biometric Authentication API (Face ID / Touch ID) – WebViewGold for iOS

> **Summary:** Protect your iOS app with Face ID or Touch ID and verify users biometrically from your web app.

[Documentation](../README.md) › [WebViewGold for iOS](README.md) › Biometric Auth API

**Platform:** iOS · **Category:** APIs & Features · **Online version:** [www.webviewgold.com/docs/iOS/biometric-authentication/](https://www.webviewgold.com/docs/iOS/biometric-authentication/)

---

**This is an independent, more powerful, yet more complicated alternative to our simple Config.swift-based *enableBioMetricAuth* option.** This API allows you to use biometric authentication in your app and return result via JavaScript to your website. Biometric authentication includes Face ID (in newer iPhone designs) and Touch ID (in older iPhone designs) with code as fallback. By calling the "bioauth://" URL command, you can trigger the biometric authentication natively in your app. Once the process is complete, WebViewGold will report the results back to your web app by calling one of the following functions:

- **onBioAuthSuccess()**
  - Called when the authentication process was successful.
- **onBioAuthFailure(errorCode, errorMessage)**
  - Called when the authentication process fails and provides error information.
- **onBioAuthUnavailable()**
  - Called when biometric authentication is found to be unavailable on the device.

To use this API, first, you must add the privacy key for Face ID biometric authentication in your **Info.plist** file. This is done by opening **Info.plist**, hovering over an exisiting key, clicking the (+) symbol to add a new key below your currently selected one and selecting the "**Privacy - Face ID Usage Description**" key option. Without this key, the app will not support Face ID. The value for this key is a description that is presented to the user the first time your app attempts to use Face ID. This description should clearly explain why your app needs to use Face ID. See below for an example description for this key:

![Example of the Face ID privacy key in Info.plist.](../assets/ios/img/faceID_key.webp)\
Next, you must define the following functions (in JavaScript) in your web app to handle the results of a biometric authentication:

```html
<script>

function onBioAuthSuccess() {
    alert("Bio Authentication Succeeded");
}

function onBioAuthFailure(errorCode, errorMessage) {
    // errorCode = Int, errorMessage = String
    alert(`Bio Authentication Failed, ${errorMessage} (code ${errorCode})`);
}

function onBioAuthUnavailable() {
    alert("Bio Authentication Unavailable");
}

</script>
```

Then, load this kind of URL to trigger the biometric authentication process in your web app:

```html
<script>

window.location.href = "bioauth://";

</script>
```

**Security Notice:** It should be noted that malicious users may be able to cause the onBioAuthSuccess() function to be called without completing the authentication process. Since authentication is a sensitive process, it is recommended to add an extra layer of security in your web app, such as a cookie or geolocation check, to help ensure the integrity of the authentication. Please consult your website cybersecurity expert for tailored guidance for your web app's needs.

---

## Continue reading

- ← Previous: [Contacts API](contacts.md)
- Next →: [Haptic Feedback API](haptic-feedback.md)
- Same feature on other platforms: [Android – Biometric Auth API](../android/biometric-auth.md)
- Languages: **🇺🇸 English** · [🇩🇪 Deutsch](../de/ios/biometric-authentication.md) · [🇫🇷 Français](../fr/ios/biometric-authentication.md) · [🇪🇸 Español](../es/ios/biometric-authentication.md) · [🇨🇳 中文](../zh/ios/biometric-authentication.md)

> [!TIP]
> **Too busy? We set up your app for you.** Our team configures, builds & submits your WebViewGold app — done-for-you, fast turnaround, Made in Germany. [Get your app set up →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **Build in your browser:** No Mac, no IDE: the **WebViewGold Cloud Builder** configures, builds & uploads your app online. [Discover Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
