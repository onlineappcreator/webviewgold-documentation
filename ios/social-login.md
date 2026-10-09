---
title: "Social Media Login Helper (Google, Facebook & Apple) – WebViewGold for iOS Documentation"
description: "Make Google, Facebook, and Apple OAuth logins work reliably inside your iOS WebView app with the built-in social login helpers."
lang: "en"
product: "WebViewGold for iOS"
platform: "iOS"
category: "APIs & Features"
slug: "social-login"
canonical_url: "https://www.webviewgold.com/docs/iOS/social-login/"
keywords:
  - "Social Login Helper"
  - "WebViewGold for iOS"
  - "convert website to app"
  - "WebView app documentation"
  - "iOS WebView SDK"
  - "PWA to app"
  - "HTML to app"
  - "JavaScript bridge"
last_updated: "2026-10-09"
---

# Social Media Login Helper (Google, Facebook & Apple) – WebViewGold for iOS

> **Summary:** Make Google, Facebook, and Apple OAuth logins work reliably inside your iOS WebView app with the built-in social login helpers.

[Documentation](../README.md) › [WebViewGold for iOS](README.md) › Social Login Helper

**Platform:** iOS · **Category:** APIs & Features · **Online version:** [www.webviewgold.com/docs/iOS/social-login/](https://www.webviewgold.com/docs/iOS/social-login/)

---

Google, Facebook, and other OAuth providers restrict logins from embedded WebViews (e.g., Google's *"disallowed_useragent"* error). The **Social Login Helper** built into WebViewGold makes these logins work reliably inside your iOS app — without changing your website's login flow.

## How It Works

You define URL prefixes that appear during the login flow of your web app. As soon as one of these trigger URLs loads, WebViewGold opens the login in a dedicated popup login window with an adjusted user agent that the OAuth provider accepts. After a successful login, the flow returns to your web app automatically. Sign in with Apple (`appleid.apple.com`) is detected and handled automatically — no configuration needed.

## Configuration

Open **Config.swift** and define the trigger URL prefixes for your login flow:

```javascript
var google_login_helper_triggers: [String] = ["https://accounts.google.com", "https://accounts.youtube.com"]
var facebook_login_helper_triggers: [String] = ["https://m.facebook.com", "https://www.facebook.com"]
```

- `google_login_helper_triggers` — URL prefixes that load during a Google login on your website.
- `facebook_login_helper_triggers` — URL prefixes that load during a Facebook login on your website.

To find the right trigger URLs, start your website's login flow in a desktop browser and note which URLs the OAuth redirect goes through.

## Open an Auth URL in the External Browser

As an alternative approach, you can hand over a login URL to the system browser explicitly (the session then lives in the browser, not in the app):

```javascript
window.location.href = "googlelogin://" + encodeURIComponent("https://accounts.google.com/o/oauth2/v2/auth?...");
```

WebViewGold decodes the URL after the `googlelogin://` prefix and opens it externally.

## When to Use the Helper

Try the simpler options first — in many cases they already solve login issues:

- Open the login domain in an in-app browser tab or external browser via the [URL Handling API](url-handling.md) (e.g., `specialLinkHandlingOptions`, `safariblacklist`).
- Set a [Custom User Agent](setup.md) (`useragent_iphone` / `useragent_ipad`).

If the login still fails in-app, the Social Login Helper triggers are the recommended solution.

---

## Continue reading

- ← Previous: [URL Handling API](url-handling.md)
- Next →: [Reconnect API](reconnect.md)
- Languages: **🇺🇸 English** · [🇩🇪 Deutsch](../de/ios/social-login.md) · [🇫🇷 Français](../fr/ios/social-login.md) · [🇪🇸 Español](../es/ios/social-login.md) · [🇨🇳 中文](../zh/ios/social-login.md)

> [!TIP]
> **Too busy? We set up your app for you.** Our team configures, builds & submits your WebViewGold app — done-for-you, fast turnaround, Made in Germany. [Get your app set up →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **Build in your browser:** No Mac, no IDE: the **WebViewGold Cloud Builder** configures, builds & uploads your app online. [Discover Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
