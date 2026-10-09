---
title: "Native Navigation Footer – WebViewGold for iOS Documentation"
description: "Enable a native bottom navigation bar with back, forward, and custom buttons in your iOS app."
lang: "en"
product: "WebViewGold for iOS"
platform: "iOS"
category: "Extensions & Plugins"
slug: "navigation-footer"
canonical_url: "https://www.webviewgold.com/docs/iOS/navigation-footer/"
keywords:
  - "Native Navigation Footer"
  - "WebViewGold for iOS"
  - "convert website to app"
  - "WebView app documentation"
  - "iOS WebView SDK"
  - "PWA to app"
  - "HTML to app"
  - "JavaScript bridge"
last_updated: "2026-10-09"
---

# Native Navigation Footer – WebViewGold for iOS

> **Summary:** Enable a native bottom navigation bar with back, forward, and custom buttons in your iOS app.

[Documentation](../README.md) › [WebViewGold for iOS](README.md) › Native Navigation Footer

**Platform:** iOS · **Category:** Extensions & Plugins · **Online version:** [www.webviewgold.com/docs/iOS/navigation-footer/](https://www.webviewgold.com/docs/iOS/navigation-footer/)

---

Set `var showNavFooter = true` in `Config.swift` to enable the native navigation footer bar. Configure buttons and links in `FooterBar.json`. Example:

```json
{
   "colour":"dark",
   "layout":[
      {
         "redirection_link":"https://webviewgoldtest.github.io/index.html",
         "sf_symbol":"house",
         "name": "Home"
      },
      {
         "redirection_link":"https://webviewgoldtest.github.io/appControls.html",
         "sf_symbol":"wrench.and.screwdriver",
         "name": "Controls"
      },
      {
         "redirection_link":"https://webviewgoldtest.github.io/NFCtesting.html",
         "sf_symbol":"wifi.square",
         "name": "NFC"
      },
      {
         "redirection_link":"https://webviewgoldtest.github.io/IAPtesting.html",
         "sf_symbol":"cart",
         "name": "Purchases"
      },
      {
         "redirection_link":"https://webviewgoldtest.github.io/permissions.html",
         "sf_symbol":"lock.open",
         "name": "Permissions"
      }
   ]
}
```

Each `sf_symbol` uses an [SF Symbol](https://developer.apple.com/sf-symbols/) and opens the `redirection_link` in the main WebView.

---

## Continue reading

- ← Previous: [App Clip Extension](app-clip.md)
- Next →: [Native Sidebar](sidebar.md)
- Same feature on other platforms: [Android – Navigation Drawer & Footer](../android/navigation-drawer.md)
- Languages: **🇺🇸 English** · [🇩🇪 Deutsch](../de/ios/navigation-footer.md) · [🇫🇷 Français](../fr/ios/navigation-footer.md) · [🇪🇸 Español](../es/ios/navigation-footer.md) · [🇨🇳 中文](../zh/ios/navigation-footer.md)

> [!TIP]
> **Too busy? We set up your app for you.** Our team configures, builds & submits your WebViewGold app — done-for-you, fast turnaround, Made in Germany. [Get your app set up →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **Build in your browser:** No Mac, no IDE: the **WebViewGold Cloud Builder** configures, builds & uploads your app online. [Discover Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
