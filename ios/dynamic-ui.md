---
title: "Dynamic UI API – WebViewGold for iOS Documentation"
description: "Change native UI elements like the status bar or bottom bar colors dynamically from your web app."
lang: "en"
product: "WebViewGold for iOS"
platform: "iOS"
category: "APIs & Features"
slug: "dynamic-ui"
canonical_url: "https://www.webviewgold.com/docs/iOS/dynamic-ui/"
keywords:
  - "Dynamic UI API"
  - "WebViewGold for iOS"
  - "convert website to app"
  - "WebView app documentation"
  - "iOS WebView SDK"
  - "PWA to app"
  - "HTML to app"
  - "JavaScript bridge"
last_updated: "2026-10-09"
---

# Dynamic UI API – WebViewGold for iOS

> **Summary:** Change native UI elements like the status bar or bottom bar colors dynamically from your web app.

[Documentation](../README.md) › [WebViewGold for iOS](README.md) › Dynamic UI API

**Platform:** iOS · **Category:** APIs & Features · **Online version:** [www.webviewgold.com/docs/iOS/dynamic-ui/](https://www.webviewgold.com/docs/iOS/dynamic-ui/)

---

WebViewGold allows you to dynamically customise the UI elements in your web app. These elements may consist of the status bar, bottom bar (iOS), navigation bar (Android) and pull to refresh (iOS). WebViewGold includes the following commands to dynamically customise these elements:

- **statusbarcolor://**
  - The MASTER COMMAND to change the color of the status bar and any other relevant UI features automatically, such as the status bar text color, the bottom bar color (iOS), navigation bar color (Android), etc.
- **statusbartextcolor://**
  - Allows you to manually change the text color of the status bar (iOS and Android).
- **bottombarcolor://**
  - If a bottom bar (iOS) or navigation bar (Android) UI element exists, allows you to manually change its color.
- **hidebars://**
  - Allows you to hide the background of the status bar, whos text remains on a transparent background.

## Changing the color of the Status Bar (and other UI elements automatically)

This feature supports a color input in the following format:

- RGB = {red, green, blue}

Where the values are integers between 0 (min) and 255 (max).

Use JavaScript to this kind of URL to change the color of the status bar:

```html
<script>
// Example: red
window.location.href = "statusbarcolor://255,0,0";
</script>
```

When you change the status bar color, the status bar text will automatically change to a suitable color (white or black) depending on how dark the color is.\
Optional UI features like *Pull To Refresh* (iOS), the *Bottom Bar* (iOS) and the *Navigation Bar* (Android) will also have their colors automatically adjusted.

## Changing the color of the Status Bar text

If you would like to manually choose the color of the status bar text, you can do so using this option.

This feature supports a text input for the following options:

- "white"
- "black"

Use JavaScript to this kind of URL to change the color of the status bar text:

```html
<script>
// Example: white text
window.location.href = "statusbartextcolor://white";
// Example: black text
window.location.href = "statusbartextcolor://black";
</script>
```

## Changing the color of the Bottom Bar

This feature supports a color input in the following format:

- RGB = {red, green, blue}

Where the values are integers between 0 (min) and 255 (max).

Use JavaScript to this kind of URL to change the color of the status bar:

```html
<script>
// Example: red
window.location.href = "bottombarcolor://255,0,0";
</script>
```

## Hiding the status bar

The hidebars functionality can either be **on** or **off**.

Note, the status bar text, such as the time and battery percentage remain visible to the user,
but the background surrounding the text becomes transparent and the WebView expands to fill the room left.

Use JavaScript to change the visibility status of the bar:

```html
<script>
// Example: hide the bars from view
window.location.href = "hidebars://on";
// Example: redisplay the bars after being hidden
window.location.href = "hidebars://off";
</script>
```

---

## Continue reading

- ← Previous: [App Version Check API](app-version-check.md)
- Next →: [Dynamic App Icon API](dynamic-app-icon.md)
- Same feature on other platforms: [Android – Dynamic UI API](../android/dynamic-ui.md)
- Languages: **🇺🇸 English** · [🇩🇪 Deutsch](../de/ios/dynamic-ui.md) · [🇫🇷 Français](../fr/ios/dynamic-ui.md) · [🇪🇸 Español](../es/ios/dynamic-ui.md) · [🇨🇳 中文](../zh/ios/dynamic-ui.md)

> [!TIP]
> **Too busy? We set up your app for you.** Our team configures, builds & submits your WebViewGold app — done-for-you, fast turnaround, Made in Germany. [Get your app set up →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **Build in your browser:** No Mac, no IDE: the **WebViewGold Cloud Builder** configures, builds & uploads your app online. [Discover Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
