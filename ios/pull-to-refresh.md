---
title: "Pull-to-Refresh API – WebViewGold for iOS Documentation"
description: "Enable the native pull-to-refresh gesture in your iOS WebView app, customize its colors, and toggle it dynamically from your web app."
lang: "en"
product: "WebViewGold for iOS"
platform: "iOS"
category: "APIs & Features"
slug: "pull-to-refresh"
canonical_url: "https://www.webviewgold.com/docs/iOS/pull-to-refresh/"
keywords:
  - "Pull-to-Refresh API"
  - "WebViewGold for iOS"
  - "convert website to app"
  - "WebView app documentation"
  - "iOS WebView SDK"
  - "PWA to app"
  - "HTML to app"
  - "JavaScript bridge"
last_updated: "2026-10-09"
---

# Pull-to-Refresh API – WebViewGold for iOS

> **Summary:** Enable the native pull-to-refresh gesture in your iOS WebView app, customize its colors, and toggle it dynamically from your web app.

[Documentation](../README.md) › [WebViewGold for iOS](README.md) › Pull-to-Refresh API

**Platform:** iOS · **Category:** APIs & Features · **Online version:** [www.webviewgold.com/docs/iOS/pull-to-refresh/](https://www.webviewgold.com/docs/iOS/pull-to-refresh/)

---

The **Pull-to-Refresh API** adds the native iOS pull-to-refresh gesture to your WebView app: users drag the page down to reload the current URL — just like in native apps such as Mail or Safari.

## How to Enable

Open **Config.swift** and set:

```swift
var pulltorefresh = true
var preventoverscroll = false
```

- `pulltorefresh` activates the native refresh control.
- `preventoverscroll` must be set to `false` — the gesture needs the WebView bounce/overscroll animation to work.

## Customize the Colors

You can style the loading spinner and its background separately for Light and Dark Mode in **Config.swift**:

```swift
var pulltorefresh_loadingsigncolour_lightmode = #colorLiteral(...)
var pulltorefresh_backgroundcolour_lightmode = #colorLiteral(...)
var pulltorefresh_loadingsigncolour_darkmode = #colorLiteral(...)
var pulltorefresh_backgroundcolour_darkmode = #colorLiteral(...)
```

Tip: Click the color swatch next to each `#colorLiteral` in Xcode to pick a color visually. The Dark Mode variants require iOS 13 or higher.

## Toggle Dynamically from Your Web App

You can switch pull-to-refresh on or off at runtime — for example, to disable it on pages with their own swipe gestures (maps, sliders, games):

```html
<a href="enablepulltorefresh://">Enable pull to refresh</a>
<a href="disablepulltorefresh://">Disable pull to refresh</a>
```

Or via JavaScript:

```javascript
window.location.href = "disablepulltorefresh://";
```

Both commands are also supported inside a [MultiAPICall](multi-api-call.md) request.

## Good to Know

- The refresh control reloads the URL that is currently displayed in the WebView.
- If you use the [Dynamic UI API](dynamic-ui.md) to change the bottom bar color at runtime, the pull-to-refresh colors are adjusted automatically to match.

---

## Continue reading

- ← Previous: [Loading Sign API](loading-sign.md)
- Next →: [URL Handling API](url-handling.md)
- Languages: **🇺🇸 English** · [🇩🇪 Deutsch](../de/ios/pull-to-refresh.md) · [🇫🇷 Français](../fr/ios/pull-to-refresh.md) · [🇪🇸 Español](../es/ios/pull-to-refresh.md) · [🇨🇳 中文](../zh/ios/pull-to-refresh.md)

> [!TIP]
> **Too busy? We set up your app for you.** Our team configures, builds & submits your WebViewGold app — done-for-you, fast turnaround, Made in Germany. [Get your app set up →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **Build in your browser:** No Mac, no IDE: the **WebViewGold Cloud Builder** configures, builds & uploads your app online. [Discover Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
