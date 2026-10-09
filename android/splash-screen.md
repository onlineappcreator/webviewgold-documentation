---
title: "Splash Screen – WebViewGold for Android Documentation"
description: "Customize the splash/launch screen of your Android WebView app with your own graphics."
lang: "en"
product: "WebViewGold for Android"
platform: "Android"
category: "App Design"
slug: "splash-screen"
canonical_url: "https://www.webviewgold.com/docs/android/splash-screen/"
keywords:
  - "Splash Screen"
  - "WebViewGold for Android"
  - "convert website to app"
  - "WebView app documentation"
  - "Android WebView SDK"
  - "PWA to app"
  - "HTML to app"
  - "JavaScript bridge"
last_updated: "2026-10-09"
---

# Splash Screen – WebViewGold for Android

> **Summary:** Customize the splash/launch screen of your Android WebView app with your own graphics.

[Documentation](../README.md) › [WebViewGold for Android](README.md) › Splash Screen

**Platform:** Android · **Category:** App Design · **Online version:** [www.webviewgold.com/docs/android/splash-screen/](https://www.webviewgold.com/docs/android/splash-screen/)

---

Customize the splash screen behavior by configuring the following variables in `Config.java`:

| Option | Type | Description |
| --- | --- | --- |
| SPLASH_SCREEN_ACTIVATED | **true** or **false** | Set to *true* to activate the splash screen |
| SPLASH_TIMEOUT | number (milliseconds) | Delay before showing the loading indicator if the home URL is still loading |
| REMAIN_SPLASH_OPTION | **true** or **false** | When *true*, keeps the splash screen visible until the home URL has fully loaded (overrides `SPLASH_TIMEOUT`) |
| SPLASH_MIN_TIME | number (milliseconds) | Minimum display duration when `REMAIN_SPLASH_OPTION` is *true*; ignored if the actual load time exceeds this value |
| SPLASH_FADE_OUT | number (milliseconds) | Fade-out animation duration after all timers; set to *0* to disable the fade effect |
| SCALE_SPLASH_IMAGE | percentage [0–100] | Scale the splash image relative to the device's smallest dimension; *0* hides the image |

## Replacing the Splash Screen Image

- Replace `splash.gif` in your assets with your own square GIF (e.g., 128×128, 512×512, or 1024×1024 px)
- Ensure the image dimensions are equal (width = height) for optimal display
- Set the background color in `colors.xml`

The steps to add a custom splash screen to your android app are shown in the video below:

[![Watch the video: Splash Screen](https://img.youtube.com/vi/x684JHvW8lI/hqdefault.jpg)](https://www.youtube.com/watch?v=x684JHvW8lI)

---

## Continue reading

- ← Previous: [App Icon](app-icon.md)
- Next →: [Navigation Drawer & Footer](navigation-drawer.md)
- Same feature on other platforms: [iOS – Name, Icon & Splash](../ios/app-name-icon-splash.md) · [macOS – Splash Screen](../macos/splash-screen.md)
- Languages: **🇺🇸 English** · [🇩🇪 Deutsch](../de/android/splash-screen.md) · [🇫🇷 Français](../fr/android/splash-screen.md) · [🇪🇸 Español](../es/android/splash-screen.md) · [🇨🇳 中文](../zh/android/splash-screen.md)

> [!TIP]
> **Too busy? We set up your app for you.** Our team configures, builds & submits your WebViewGold app — done-for-you, fast turnaround, Made in Germany. [Get your app set up →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_android_doc_online)
>
> **Build in your browser:** No Mac, no IDE: the **WebViewGold Cloud Builder** configures, builds & uploads your app online. [Discover Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=android_docs)
