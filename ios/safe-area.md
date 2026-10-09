---
title: "Modify the Safe Area Size – WebViewGold for iOS Documentation"
description: "Adjust the safe area and enable the custom bottom bar so your web app looks perfect on iPhones with a Home bar."
lang: "en"
product: "WebViewGold for iOS"
platform: "iOS"
category: "App Design"
slug: "safe-area"
canonical_url: "https://www.webviewgold.com/docs/iOS/safe-area/"
keywords:
  - "Modify Safe Area"
  - "WebViewGold for iOS"
  - "convert website to app"
  - "WebView app documentation"
  - "iOS WebView SDK"
  - "PWA to app"
  - "HTML to app"
  - "JavaScript bridge"
last_updated: "2026-10-09"
---

# Modify the Safe Area Size – WebViewGold for iOS

> **Summary:** Adjust the safe area and enable the custom bottom bar so your web app looks perfect on iPhones with a Home bar.

[Documentation](../README.md) › [WebViewGold for iOS](README.md) › Modify Safe Area

**Platform:** iOS · **Category:** App Design · **Online version:** [www.webviewgold.com/docs/iOS/safe-area/](https://www.webviewgold.com/docs/iOS/safe-area/)

---

The jump from iPhone 8 to iPhone X and beyond changed a lot in terms of User Interface in the mobile industry by removing the Home button and introducing the Home bar. Depending on your web app design, the lower menu bar may be positioned incorrectly on devices (overlapping content) with the Home bar due to the change in the default safe area.\
The good news is that WebViewGold has a feature that allows you to turn on a **bottombar** and choose its color to match your app theme. Since the issue of the Home bar overlapping app content may not appear in iPads (due to the larger screen and possible different layout), there is also an option to disable the feature in iPads.\
To implement this feature, use the following variables in **Config.swift** under the heading "Custom Bottom Bar Design". Make sure to set **bottombar** to **true**.\
![Bottom bar feature Config variables](../assets/ios/img/bottombar_config.webp)\
**Advanced:** Instead of using the bottombar feature, you can search for this code snippet part *(Press **CMD+F** then enter "*`switch UIDevice.current.userInterfaceIdiom`*")* in the **WebViewController.swift** file where you can change the border value 20 to any desired value like 10, 30, etc as shown below:\
![Resize the Safe Area on iPhone X/XS/XS Max WebView apps](../assets/ios/img/edgeinsets.webp)

---

## Continue reading

- ← Previous: [Name, Icon & Splash](app-name-icon-splash.md)
- Next →: [Geolocation API](geolocation.md)
- Languages: **🇺🇸 English** · [🇩🇪 Deutsch](../de/ios/safe-area.md) · [🇫🇷 Français](../fr/ios/safe-area.md) · [🇪🇸 Español](../es/ios/safe-area.md) · [🇨🇳 中文](../zh/ios/safe-area.md)

> [!TIP]
> **Too busy? We set up your app for you.** Our team configures, builds & submits your WebViewGold app — done-for-you, fast turnaround, Made in Germany. [Get your app set up →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **Build in your browser:** No Mac, no IDE: the **WebViewGold Cloud Builder** configures, builds & uploads your app online. [Discover Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
