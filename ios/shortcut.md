---
title: "Shortcut API – WebViewGold for iOS Documentation"
description: "Add Home Screen quick action shortcuts to your iOS app that deep link into specific pages."
lang: "en"
product: "WebViewGold for iOS"
platform: "iOS"
category: "APIs & Features"
slug: "shortcut"
canonical_url: "https://www.webviewgold.com/docs/iOS/shortcut/"
keywords:
  - "Shortcut API"
  - "WebViewGold for iOS"
  - "convert website to app"
  - "WebView app documentation"
  - "iOS WebView SDK"
  - "PWA to app"
  - "HTML to app"
  - "JavaScript bridge"
last_updated: "2026-10-09"
---

# Shortcut API – WebViewGold for iOS

> **Summary:** Add Home Screen quick action shortcuts to your iOS app that deep link into specific pages.

[Documentation](../README.md) › [WebViewGold for iOS](README.md) › Shortcut API

**Platform:** iOS · **Category:** APIs & Features · **Online version:** [www.webviewgold.com/docs/iOS/shortcut/](https://www.webviewgold.com/docs/iOS/shortcut/)

---

Enable `var useShortcuts = true` in `Config.swift` to register dynamic shortcuts defined in `Shortcuts.json`. Each shortcut can open a URL, inject JavaScript, and display an SF Symbol. Example:

```json
{
    "shortcuts": [
        {
            "title": "Open Google",
            "redirection_link": "https://google.com",
            "injection": "",
            "symbol": "wrench.and.screwdriver"
        },
        {
            "title": "Open & Inject",
            "redirection_link": "https://apple.com",
            "injection": "(function() { console.log('Injected and executed!'); })();",
            "symbol": "lock.open"
        }
    ]
}
```

Users can access the shortcuts by long-pressing the app icon.

---

## Continue reading

- ← Previous: [Haptic Feedback API](haptic-feedback.md)
- Next →: [Clipboard API](clipboard.md)
- Languages: **🇺🇸 English** · [🇩🇪 Deutsch](../de/ios/shortcut.md) · [🇫🇷 Français](../fr/ios/shortcut.md) · [🇪🇸 Español](../es/ios/shortcut.md) · [🇨🇳 中文](../zh/ios/shortcut.md)

> [!TIP]
> **Too busy? We set up your app for you.** Our team configures, builds & submits your WebViewGold app — done-for-you, fast turnaround, Made in Germany. [Get your app set up →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **Build in your browser:** No Mac, no IDE: the **WebViewGold Cloud Builder** configures, builds & uploads your app online. [Discover Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
