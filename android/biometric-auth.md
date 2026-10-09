---
title: "Biometric Authentication API – WebViewGold for Android Documentation"
description: "Prompt fingerprint or face authentication with the native Android BiometricPrompt directly from your web app."
lang: "en"
product: "WebViewGold for Android"
platform: "Android"
category: "APIs & Features"
slug: "biometric-auth"
canonical_url: "https://www.webviewgold.com/docs/android/biometric-auth/"
keywords:
  - "Biometric Auth API"
  - "WebViewGold for Android"
  - "convert website to app"
  - "WebView app documentation"
  - "Android WebView SDK"
  - "PWA to app"
  - "HTML to app"
  - "JavaScript bridge"
last_updated: "2026-10-09"
---

# Biometric Authentication API – WebViewGold for Android

> **Summary:** Prompt fingerprint or face authentication with the native Android BiometricPrompt directly from your web app.

[Documentation](../README.md) › [WebViewGold for Android](README.md) › Biometric Auth API

**Platform:** Android · **Category:** APIs & Features · **Online version:** [www.webviewgold.com/docs/android/biometric-auth/](https://www.webviewgold.com/docs/android/biometric-auth/)

---

The **Biometric Authentication API** prompts the user for fingerprint or face authentication using the device's native `BiometricPrompt`. If the OS is configured that way, it falls back to the device PIN or pattern.

## How to Use

Trigger the system dialog from an HTML link or from JavaScript:

```html
<a href="bioauth://">Unlock</a>
```

```javascript
window.location.href = "bioauth://";
```

## Typical Use Cases

- Gate access to a "wallet", "settings", or "orders" page inside your web app.
- Require re-authentication before a sensitive checkout step.

## Behavior

- The system dialog is drawn by the app — your web app does not need to render any UI.
- After a successful authentication the app resumes normally so your web app can react (e.g. by navigating to the protected page).
- On some devices without biometrics, the OS may show a PIN prompt instead.

## Related Config

`enableBioMetricAuth` in **Config.java** turns on the built-in **App Lock** flow that requires biometric auth on every app launch. `bioauth://` is independent of this flag and can be triggered at any time from JavaScript.

---

## Continue reading

- ← Previous: [Read/Write Value API](read-write-value.md)
- Next →: [Document Scanner](document-scanner.md)
- Same feature on other platforms: [iOS – Biometric Auth API](../ios/biometric-authentication.md)
- Languages: **🇺🇸 English** · [🇩🇪 Deutsch](../de/android/biometric-auth.md) · [🇫🇷 Français](../fr/android/biometric-auth.md) · [🇪🇸 Español](../es/android/biometric-auth.md) · [🇨🇳 中文](../zh/android/biometric-auth.md)

> [!TIP]
> **Too busy? We set up your app for you.** Our team configures, builds & submits your WebViewGold app — done-for-you, fast turnaround, Made in Germany. [Get your app set up →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_android_doc_online)
>
> **Build in your browser:** No Mac, no IDE: the **WebViewGold Cloud Builder** configures, builds & uploads your app online. [Discover Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=android_docs)
