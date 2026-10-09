---
title: "URL Handling API – WebViewGold for Android Documentation"
description: "Decide which links open inside your Android app, in Chrome Custom Tabs, or in the external browser."
lang: "en"
product: "WebViewGold for Android"
platform: "Android"
category: "APIs & Features"
slug: "url-handling"
canonical_url: "https://www.webviewgold.com/docs/android/url-handling/"
keywords:
  - "URL Handling API"
  - "WebViewGold for Android"
  - "convert website to app"
  - "WebView app documentation"
  - "Android WebView SDK"
  - "PWA to app"
  - "HTML to app"
  - "JavaScript bridge"
last_updated: "2026-10-09"
---

# URL Handling API – WebViewGold for Android

> **Summary:** Decide which links open inside your Android app, in Chrome Custom Tabs, or in the external browser.

[Documentation](../README.md) › [WebViewGold for Android](README.md) › URL Handling API

**Platform:** Android · **Category:** APIs & Features · **Online version:** [www.webviewgold.com/docs/android/url-handling/](https://www.webviewgold.com/docs/android/url-handling/)

---

To improve user experience, it's often beneficial to customize how your app handles different types of web links. For example, social media buttons can be configured to open in the system browser or respective app, rather than within your app. WebViewGold provides flexible settings to customize URL handling for your WebView-based Android app:

## Types of Links

1. **External Links:** Links that lead to a **different domain** from your app's primary domain.
   - **Example:** If your app's domain is **mydomain.com**, an external link would be **google.com**.
2. **Internal Links:** Links that stay within the **same domain** as your app.
   - **Example:** If your app's domain is **mydomain.com**, an internal link would be **mydomain.com/purchase**.
3. **Special Links:** Links that include special attributes, such as **target="_blank"** or links ending with **#**.

## Link Handling Options

You can configure link behavior by modifying settings in the **Config.java** file as shown below.

## External Link Handling

- **Default Option (0):** To open external links in the main WebView (the same as internal links), set `EXTERNAL_LINK_HANDLING_OPTIONS` to `0`.
- **Option 1:** To open external links in a new in-app tab, set `EXTERNAL_LINK_HANDLING_OPTIONS` to `1`.
- **Option 2:** To open external links in the device's default system browser (e.g. Chrome, Safari), set `EXTERNAL_LINK_HANDLING_OPTIONS` to `2`.

## Special Link Handling

- **Option 0:** To open special links in the app's main WebView, set `SPECIAL_LINK_HANDLING_OPTIONS` to `0`.
- **Option 1:** To open special links in a new in-app tab, set `SPECIAL_LINK_HANDLING_OPTIONS` to `1`.
- **Option 2:** To open special links in the device's default system browser (e.g. Chrome, Safari), set `SPECIAL_LINK_HANDLING_OPTIONS` to `2`.

Note: This setting with override `EXTERNAL_LINK_HANDLING_OPTIONS` for links that are both external and special.

## Customizing Link Access: Whitelist and Blacklist

To create exceptions for specific sites or pages, open **Config.java** and add the domain to one of the following arrays:

- **BROWSER_WHITELIST:** Lists specific domains to open within the app's WebView.
- **BROWSER_BLACKLIST:** Lists specific domains to open in the external browser.

For detailed guidance on link configuration for your Android app, watch the video tutorial provided below:

[![Watch the video: URL Handling API](https://img.youtube.com/vi/lq7jgaB6TxY/hqdefault.jpg)](https://www.youtube.com/watch?v=lq7jgaB6TxY)

---

## URL Handling – Using the In-App Browser for Specific Links

Some links, like a Terms and Conditions page, may not be significant enough to open in an external system browser yet too specific for your app's primary WebView. WebViewGold provides a creative solution for handling these links: **an in-app browser tab** that opens over the main WebView, providing a hybrid app and browser experience. Here's what it will look like:\
![Open a link in an additional in-app-browser/tab in Android WebView apps](../assets/android/img/tabs.webp)

### Key Features of the In-App Browser Tab

- The in-app browser tab includes an **address bar** and **navigation buttons**, offering a more browser-like experience than the primary WebView.
- Ideal for content that requires easy navigation, such as tutorials, knowledge bases, or pages with specific information.

### How to Use the In-App Browser Tab in Your WebView-Based Android App

To open a link in the in-app browser tab, format the URL in your HTML as follows:

```html
<a href='#' onClick="top.location.href='https://www.example.com';">Open Example Page</a>
```

**Example:** To open Google, use:

```html
<a href='#' onClick="top.location.href='https://www.google.com';">Open Google</a>
```

**Testing Link Behavior:**\
To see how your app will handle different types of links, use the following URL as the WebView URL during testing:\
Test Link: <https://www.webviewgold.com/demo/testlinks.php>\
**Note:** You can also open the same domain in your desktop browser to view the source code and copy the format for your links.

---

## Force a Specific Link into the In-App Tab or Browser (`newtab:` prefix)

Sometimes you want a **single, specific link** to open in the in-app browser tab (or in the external browser) — regardless of your global link handling configuration. Simply prefix the URL with `newtab:`:

```html
<a href="newtab:https://www.example.com">Open Example Page</a>
```

The prefixed link is then treated like a special link: with `SPECIAL_LINK_HANDLING_OPTIONS` set to `1` it opens in the in-app browser tab, with `2` it opens in the external system browser. This requires `SPECIAL_LINK_HANDLING_OPTIONS` to be set to a value other than `0` in **Config.java**.

## Open an Authentication URL in a Chrome Custom Tab (`googlelogin://`)

Some login providers (especially **Google Sign-In**) block authentication inside plain WebViews. If the [Social Media Login Helper Tool](setup.md) does not fit your flow, you can open the authentication URL in a secure **Chrome Custom Tab** instead by prefixing it with `googlelogin://`:

```javascript
window.location.href = "googlelogin://" + encodeURIComponent("https://accounts.google.com/o/oauth2/v2/auth?...");
```

The URL after the prefix is decoded and opened in an in-app Chrome Custom Tab, where the login can be completed. Afterwards, redirect the user back to your web app (e.g., via your OAuth redirect URL).

---

## Continue reading

- ← Previous: [Navigation Drawer & Footer](navigation-drawer.md)
- Next →: [Custom CSS & JS API](custom-css-js.md)
- Same feature on other platforms: [iOS – URL Handling API](../ios/url-handling.md)
- Languages: **🇺🇸 English** · [🇩🇪 Deutsch](../de/android/url-handling.md) · [🇫🇷 Français](../fr/android/url-handling.md) · [🇪🇸 Español](../es/android/url-handling.md) · [🇨🇳 中文](../zh/android/url-handling.md)

> [!TIP]
> **Too busy? We set up your app for you.** Our team configures, builds & submits your WebViewGold app — done-for-you, fast turnaround, Made in Germany. [Get your app set up →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_android_doc_online)
>
> **Build in your browser:** No Mac, no IDE: the **WebViewGold Cloud Builder** configures, builds & uploads your app online. [Discover Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=android_docs)
