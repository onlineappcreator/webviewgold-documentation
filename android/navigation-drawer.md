---
title: "Navigation Drawer & Bottom Navigation Footer – WebViewGold for Android Documentation"
description: "Ship an app-like navigation experience with the built-in Material navigation drawer and Material 3 bottom navigation bar — no changes to your website required."
lang: "en"
product: "WebViewGold for Android"
platform: "Android"
category: "App Design"
slug: "navigation-drawer"
canonical_url: "https://www.webviewgold.com/docs/android/navigation-drawer/"
keywords:
  - "Navigation Drawer & Footer"
  - "WebViewGold for Android"
  - "convert website to app"
  - "WebView app documentation"
  - "Android WebView SDK"
  - "PWA to app"
  - "HTML to app"
  - "JavaScript bridge"
last_updated: "2026-10-09"
---

# Navigation Drawer & Bottom Navigation Footer – WebViewGold for Android

> **Summary:** Ship an app-like navigation experience with the built-in Material navigation drawer and Material 3 bottom navigation bar — no changes to your website required.

[Documentation](../README.md) › [WebViewGold for Android](README.md) › Navigation Drawer & Footer

**Platform:** Android · **Category:** App Design · **Online version:** [www.webviewgold.com/docs/android/navigation-drawer/](https://www.webviewgold.com/docs/android/navigation-drawer/)

---

WebViewGold ships two built-in native navigation UIs so you can offer an app-like navigation experience without touching your website: a side **Navigation Drawer** and a Material 3 **Bottom Navigation Footer**. Both are optional and can be combined or used independently.

## 1. Side Navigation Drawer

A floating menu button opens a Material navigation drawer with your links. Enable it in **Config.java**:

```java
static boolean ENABLE_NAVIGATION_DRAWER = true;
```

Configure the entries and icons in:

```
app/src/main/res/menu/menu_drawer.xml
```

Each `<item>` becomes a drawer row and, when tapped, navigates the WebView to the URL you associate with it.

## 2. Bottom Navigation Footer

A Material 3 bottom-navigation bar sits at the bottom of the screen and switches between your top-level sections. Enable it in **Config.java**:

```java
static boolean ENABLE_NAVIGATION_FOOTER = true;
```

The same file (`res/menu/menu_drawer.xml`) drives the entries — pick 3–5 top-level destinations.

## Behavior

- Both UIs respect the device's dark/light mode automatically.
- Icons and labels come from your menu XML.
- Tapping an entry loads the associated URL in the main WebView, so your web app never leaves the app shell.

**Reference:** [Material 3 navigation bar guidelines](https://m3.material.io/components/navigation-bar/overview).

---

## Continue reading

- ← Previous: [Splash Screen](splash-screen.md)
- Next →: [URL Handling API](url-handling.md)
- Same feature on other platforms: [iOS – Native Navigation Footer](../ios/navigation-footer.md)
- Languages: **🇺🇸 English** · [🇩🇪 Deutsch](../de/android/navigation-drawer.md) · [🇫🇷 Français](../fr/android/navigation-drawer.md) · [🇪🇸 Español](../es/android/navigation-drawer.md) · [🇨🇳 中文](../zh/android/navigation-drawer.md)

> [!TIP]
> **Too busy? We set up your app for you.** Our team configures, builds & submits your WebViewGold app — done-for-you, fast turnaround, Made in Germany. [Get your app set up →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_android_doc_online)
>
> **Build in your browser:** No Mac, no IDE: the **WebViewGold Cloud Builder** configures, builds & uploads your app online. [Discover Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=android_docs)
