---
title: "URL Handling API – WebViewGold for iOS Documentation"
description: "Decide which links open inside your app, in an in-app browser tab, or in Safari — full URL handling control for iOS."
lang: "en"
product: "WebViewGold for iOS"
platform: "iOS"
category: "APIs & Features"
slug: "url-handling"
canonical_url: "https://www.webviewgold.com/docs/iOS/url-handling/"
keywords:
  - "URL Handling API"
  - "WebViewGold for iOS"
  - "convert website to app"
  - "WebView app documentation"
  - "iOS WebView SDK"
  - "PWA to app"
  - "HTML to app"
  - "JavaScript bridge"
last_updated: "2026-10-09"
---

# URL Handling API – WebViewGold for iOS

> **Summary:** Decide which links open inside your app, in an in-app browser tab, or in Safari — full URL handling control for iOS.

[Documentation](../README.md) › [WebViewGold for iOS](README.md) › URL Handling API

**Platform:** iOS · **Category:** APIs & Features · **Online version:** [www.webviewgold.com/docs/iOS/url-handling/](https://www.webviewgold.com/docs/iOS/url-handling/)

---

To improve user experience, it's often beneficial to customize how your app handles different types of web links. For example, social media buttons can be configured to open in the system browser or respective app, rather than within your app. WebViewGold provides flexible settings to customize URL handling for your WebView-based iOS app.

## Types of Links

1. **External Links:** Links that lead to a **different domain** from your app's primary domain.
   - **Example:** If your app's domain is **mydomain.com**, an external link would be **google.com**.
2. **Internal Links:** Links that stay within the **same domain** as your app.
   - **Example:** If your app's domain is **mydomain.com**, an internal link would be **mydomain.com/purchase**.
3. **Special Links:** Links that include special attributes, such as **target="_blank"**.

## To configure the URL Handling API, open Config.swift

1. To define the default behavior for **external links**:
   - Set `externalLinkHandlingOptions` to `0` to open external links in-app by default, or to `2` to ALWAYS open them in another browser (Safari).

2. To define the default behavior for **special links** (e.g., **target="_blank"**):
   - Set `specialLinkHandlingOptions` to `0` to open special links in-app, `1` to open them in a new tab (an additional in-app browser), or `2` to open them in another browser (Safari).

3. To set domains which ***always* open in Safari** (regardless of the `externalLinkHandlingOptions` setting):
   - Add the desired domains to the `safariwhitelist` list.
   - Insert another host like so: ["alwaysopeninsafari.com", "google.com", "m.facebook.com"].
   - Please enter the host exactly how you link to it (with or without www, but always without http/https).

4. To set domains which ***never* open in Safari** (regardless of the `externalLinkHandlingOptions` setting):
   - Add the desired domains to the `safariblacklist` list.
   - Insert another host like so: ["alwaysopeninsafari.com", "google.com", "m.facebook.com"].
   - Please enter the host exactly how you link to it (with or without www, but always without http/https).

5. To set domains which ***always*** or ***never* open in an in-app tab** (regardless of the `externalLinkHandlingOptions` setting):
   - Add the desired domains to the `alwaysOpenInInAppTab` or `neverOpenInInAppTab` list.

## Open links in a tab/additional In-App-Browser

Some links, like a Terms and Conditions page, may not be significant enough to open in an external system browser yet too specific for your app's primary WebView. WebViewGold provides a creative solution for handling these links: **an in-app browser tab** that opens over the main WebView, providing a hybrid app and browser experience. Here's what it will look like:

![Open a link in an additional in-app-browser/tab SFSafariViewController](../assets/ios/img/tabs.webp)

### Key Features of the In-App Browser Tab

- The in-app browser tab includes an **address bar** and **navigation buttons**, offering a more browser-like experience than the primary WebView.
- Ideal for content that requires easy navigation, such as tutorials, knowledge bases, or pages with specific information.

### How to Use the In-App Browser Tab in Your WebView-Based iOS App

To open a link in the in-app browser tab, set `specialLinkHandlingOptions` to `1` and format the URL in your HTML as follows:

```html
<a href="https://www.example.com" target="_blank">Open link in an in-app tab</a>
```

Simply, a **special link** is classified as a link that has the "_blank" target attached. In a normal browser, this would make the link open in a new tab. In WebViewGold app, you can make it open in the in-app tab instead.

Please note that if the link you are using is external (has a different domain to your website like "www.google.com", for example) please also make sure that `externalLinkHandlingOptions` is set to `0`, as opening all external links in another browser would override the special-external link to open in the Safari app instead.

**Testing Link Behavior:**\
To see how your app will handle different types of links, use the following URL as the WebView URL during testing:\
Test Link: <https://www.webviewgold.com/demo/testlinks.php>\
**Note:** You can also open the same domain in your desktop browser to view the source code and copy the format for your links.

---

## Continue reading

- ← Previous: [Pull-to-Refresh API](pull-to-refresh.md)
- Next →: [Social Login Helper](social-login.md)
- Same feature on other platforms: [Android – URL Handling API](../android/url-handling.md)
- Languages: **🇺🇸 English** · [🇩🇪 Deutsch](../de/ios/url-handling.md) · [🇫🇷 Français](../fr/ios/url-handling.md) · [🇪🇸 Español](../es/ios/url-handling.md) · [🇨🇳 中文](../zh/ios/url-handling.md)

> [!TIP]
> **Too busy? We set up your app for you.** Our team configures, builds & submits your WebViewGold app — done-for-you, fast turnaround, Made in Germany. [Get your app set up →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **Build in your browser:** No Mac, no IDE: the **WebViewGold Cloud Builder** configures, builds & uploads your app online. [Discover Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
