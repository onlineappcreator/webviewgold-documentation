---
title: "Native Sidebar Navigation – WebViewGold for iOS Documentation"
description: "Enable a native sliding sidebar menu with custom links and SF Symbols icons — configured via Sidebar.json."
lang: "en"
product: "WebViewGold for iOS"
platform: "iOS"
category: "Extensions & Plugins"
slug: "sidebar"
canonical_url: "https://www.webviewgold.com/docs/iOS/sidebar/"
keywords:
  - "Native Sidebar"
  - "WebViewGold for iOS"
  - "convert website to app"
  - "WebView app documentation"
  - "iOS WebView SDK"
  - "PWA to app"
  - "HTML to app"
  - "JavaScript bridge"
last_updated: "2026-10-09"
---

# Native Sidebar Navigation – WebViewGold for iOS

> **Summary:** Enable a native sliding sidebar menu with custom links and SF Symbols icons — configured via Sidebar.json.

[Documentation](../README.md) › [WebViewGold for iOS](README.md) › Native Sidebar

**Platform:** iOS · **Category:** Extensions & Plugins · **Online version:** [www.webviewgold.com/docs/iOS/sidebar/](https://www.webviewgold.com/docs/iOS/sidebar/)

---

Besides the [Native Navigation Footer](navigation-footer.md), WebViewGold ships a native **sliding sidebar** so you can offer an app-like navigation experience without touching your website. A floating menu button opens a sidebar with your links — each entry navigates the main WebView to the URL you associate with it.

## How to Enable

Set the following option in **Config.swift**:

```swift
var enableSidebar = true
```

## How to Configure

Open **Sidebar.json** in the Xcode project and define the color scheme and the menu entries:

```json
{
   "colour":"dark",
   "layout":[
      {
         "redirection_link":"https://example.org/home",
         "sf_symbol":"house",
         "name": "Home"
      },
      {
         "redirection_link":"https://example.org/shop",
         "sf_symbol":"cart",
         "name": "Shop"
      }
   ]
}
```

| Key | Description |
| --- | --- |
| `colour` | Color scheme of the sidebar: `dark` or `light`. |
| `redirection_link` | URL loaded in the main WebView when the entry is tapped. |
| `sf_symbol` | Icon name from Apple's [SF Symbols](https://developer.apple.com/sf-symbols/) library (e.g., `house`, `cart`, `wrench.and.screwdriver`). |
| `name` | Label of the sidebar entry. |

## Behavior

- A floating button opens and closes the sidebar over your web content.
- Tapping an entry loads the associated URL in the main WebView, so your web app never leaves the app shell.
- The sidebar can be combined with the [Native Navigation Footer](navigation-footer.md) or used independently.

---

## Continue reading

- ← Previous: [Native Navigation Footer](navigation-footer.md)
- Next →: [Screen Capture Detection](screen-capture.md)
- Languages: **🇺🇸 English** · [🇩🇪 Deutsch](../de/ios/sidebar.md) · [🇫🇷 Français](../fr/ios/sidebar.md) · [🇪🇸 Español](../es/ios/sidebar.md) · [🇨🇳 中文](../zh/ios/sidebar.md)

> [!TIP]
> **Too busy? We set up your app for you.** Our team configures, builds & submits your WebViewGold app — done-for-you, fast turnaround, Made in Germany. [Get your app set up →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **Build in your browser:** No Mac, no IDE: the **WebViewGold Cloud Builder** configures, builds & uploads your app online. [Discover Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
