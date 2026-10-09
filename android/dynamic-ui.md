---
title: "Dynamic UI API – WebViewGold for Android Documentation"
description: "Change native UI elements like the status bar color dynamically from your web app on Android."
lang: "en"
product: "WebViewGold for Android"
platform: "Android"
category: "APIs & Features"
slug: "dynamic-ui"
canonical_url: "https://www.webviewgold.com/docs/android/dynamic-ui/"
keywords:
  - "Dynamic UI API"
  - "WebViewGold for Android"
  - "convert website to app"
  - "WebView app documentation"
  - "Android WebView SDK"
  - "PWA to app"
  - "HTML to app"
  - "JavaScript bridge"
last_updated: "2026-10-09"
---

# Dynamic UI API – WebViewGold for Android

> **Summary:** Change native UI elements like the status bar color dynamically from your web app on Android.

[Documentation](../README.md) › [WebViewGold for Android](README.md) › Dynamic UI API

**Platform:** Android · **Category:** APIs & Features · **Online version:** [www.webviewgold.com/docs/android/dynamic-ui/](https://www.webviewgold.com/docs/android/dynamic-ui/)

---

WebViewGold allows you to dynamically customise the UI elements in your web app. These elements may consist of the status bar, bottom bar (iOS), navigation bar (Android) and pull to refresh (iOS). WebViewGold includes the following commands to dynamically customise these elements:

- **statusbarcolor://**
  - The MASTER COMMAND to change the color of the status bar and any other relevant UI features automatically, such as the status bar text color, the bottom bar color (iOS), navigation bar color (Android), etc.
- **statusbartextcolor://**
  - Allows you to manually change the text color of the status bar (iOS and Android).
- **bottombarcolor://**
  - If a bottom bar (iOS) or navigation bar (Android) UI element exists, allows you to manually change its color.
- **navbartextcolor://**
  - Allows you to manually change the text color of the navigation bar on Android. Request will be ignored on iOS (the bottom bar on iOS does not have text).
- **hidebars://**
  - Allows you to hide the background of the status and navigation bar.

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

## Changing the color of the Navigation Bar

This feature supports a color input in the following format:

- RGB = {red, green, blue}

Where the values are integers between 0 (min) and 255 (max).

Use JavaScript to this kind of URL to change the color of the navigation bar:

```html
<script>
// Example: red
window.location.href = "bottombarcolor://255,0,0";
</script>
```

## Changing the color of the Navigation Bar text

If you would like to manually choose the color of the navigation bar text, you can do so using this option. Please note that this request will be ignored on iOS.

This feature supports a text input for the following options:

- "white"
- "black"

Use JavaScript to this kind of URL to change the color of the navigation bar text:

```html
<script>
// Example: white text
window.location.href = "navbartextcolor://white";
// Example: black text
window.location.href = "navbartextcolor://black";
</script>
```

## Hiding the status and bottom bars

The hidebars functionality can either be **on** or **off**.

Note, the status bar text, such as the time and battery percentage *do not* remain visibile to the user.
However, these can be brought back to view with a user swipe from the top.

Use JavaScript to change the visibility status of the status and navigation bar:

```html
<script>
// Example: hide the bars from view
window.location.href = "hidebars://on";
// Example: redisplay the bars after being hidden
window.location.href = "hidebars://off";
</script>
```

---

## Detect Dark Mode (`isDarkMode` JavaScript variable)

To adapt your dynamic UI colors to the user's system theme, WebViewGold automatically injects the JavaScript variable `isDarkMode` (`true` or `false`) into every page once it has finished loading. Example:

```html
<script>
if (typeof isDarkMode !== "undefined" && isDarkMode) {
    // Dark mode: e.g., set a dark status bar
    window.location.href = "statusbarcolor://0,0,0";
    window.location.href = "statusbartextcolor://white";
} else {
    // Light mode
    window.location.href = "statusbarcolor://255,255,255";
    window.location.href = "statusbartextcolor://black";
}
</script>
```

**Note:** Alternatively, you can use the standard CSS media query `prefers-color-scheme` in your web app. The injected `isDarkMode` variable is handy when you want to trigger the WebViewGold UI APIs above from JavaScript.

---

## Continue reading

- ← Previous: [Contacts API](contacts.md)
- Next →: [Haptic Feedback API](haptic-feedback.md)
- Same feature on other platforms: [iOS – Dynamic UI API](../ios/dynamic-ui.md)
- Languages: **🇺🇸 English** · [🇩🇪 Deutsch](../de/android/dynamic-ui.md) · [🇫🇷 Français](../fr/android/dynamic-ui.md) · [🇪🇸 Español](../es/android/dynamic-ui.md) · [🇨🇳 中文](../zh/android/dynamic-ui.md)

> [!TIP]
> **Too busy? We set up your app for you.** Our team configures, builds & submits your WebViewGold app — done-for-you, fast turnaround, Made in Germany. [Get your app set up →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_android_doc_online)
>
> **Build in your browser:** No Mac, no IDE: the **WebViewGold Cloud Builder** configures, builds & uploads your app online. [Discover Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=android_docs)
