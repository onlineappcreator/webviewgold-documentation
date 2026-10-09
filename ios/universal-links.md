---
title: "Universal Links API – WebViewGold for iOS Documentation"
description: "Open links to your domain directly in your iOS app with Apple Universal Links — setup, AASA file, and troubleshooting."
lang: "en"
product: "WebViewGold for iOS"
platform: "iOS"
category: "APIs & Features"
slug: "universal-links"
canonical_url: "https://www.webviewgold.com/docs/iOS/universal-links/"
keywords:
  - "Universal Links API"
  - "WebViewGold for iOS"
  - "convert website to app"
  - "WebView app documentation"
  - "iOS WebView SDK"
  - "PWA to app"
  - "HTML to app"
  - "JavaScript bridge"
last_updated: "2026-10-09"
---

# Universal Links API – WebViewGold for iOS

> **Summary:** Open links to your domain directly in your iOS app with Apple Universal Links — setup, AASA file, and troubleshooting.

[Documentation](../README.md) › [WebViewGold for iOS](README.md) › Universal Links API

**Platform:** iOS · **Category:** APIs & Features · **Online version:** [www.webviewgold.com/docs/iOS/universal-links/](https://www.webviewgold.com/docs/iOS/universal-links/)

---

The **Universal Links API** simplifies linking to content within your app, providing a more seamless and native user experience. WebViewGold enables you to configure your domain so that links from apps like **Mail, Safari, and others** automatically open within your WebViewGold-based app—without requiring additional prompts.

**Note:** the app must be installed on the user's device first for this feature to work.

**Alternatively**, it is possible to use our [**Deep Linking API**](deep-linking.md). While it operates in a similar manner, it uses a different syntax. However, it's worth noting that the syntax of the [**Universal Links API**](universal-links.md) is more common than the syntax of the Deep Linking API. For most apps, it's wise to choose either one, but not both.

To set up **Universal Links** in your iOS app, please follow the steps below:

1. **Apple Developer Center Setup:**

1. Log in to your account on the [Apple Developer Center](https://developer.apple.com/account/).
2. Click on 'Certificates, Identifiers & Profiles'.
3. Under 'Identifiers', select 'App IDs' and then choose your app's ID from the list.
4. Under the 'App Services' section, check the 'Associated Domains' option and save your changes.

2. **Xcode Setup:**

1. Open your app project in Xcode.
2. Select the target (in most cases "WebViewGold"). In the 'Signing & Capabilities' tab, navigate to the 'Associated Domains' section. Click on '+' to add a domain. Your domain should be prefixed with 'applinks:', like this: `applinks:example.org` & `applinks:www.example.org`:\
   ![Associated Domains in Xcode](../assets/ios/img/associateddomains.webp)
3. In Config.swift, turn **ShowExternalLink** to **true**.
4. Be mindful of subdomains. There's a distinction between "www.\*" and non-"www" domains (consider adding both). Ensure that you have the correct provisioning profile with the 'Associated Domains' capability. If not, Xcode should prompt you to fix it.

3. **Server Setup:**

1. On your website server, you need to host an Apple App Site Association (AASA) file at the root level of your server or using the `/.well-known/` prefix. E.g., `https://example.org/.well-known/apple-app-site-association`
2. The AASA file should contain details about the app and the associated domains. Refer to the [official documentation](https://developer.apple.com/documentation/safariservices/supporting_associated_domains) for the exact structure. Ensure that the apple-app-site-association file is hosted on a server that supports HTTPS, not just HTTP.

**Done! :-)** Testing in the Simulator isn't as effective as on a real device. For best results, use an actual iPhone or iPad.

---

## Continue reading

- ← Previous: [Custom CSS & JS API](custom-css-js.md)
- Next →: [Deep Linking API](deep-linking.md)
- Same feature on other platforms: [Android – App Links / Deep Linking](../android/app-links.md)
- Languages: **🇺🇸 English** · [🇩🇪 Deutsch](../de/ios/universal-links.md) · [🇫🇷 Français](../fr/ios/universal-links.md) · [🇪🇸 Español](../es/ios/universal-links.md) · [🇨🇳 中文](../zh/ios/universal-links.md)

> [!TIP]
> **Too busy? We set up your app for you.** Our team configures, builds & submits your WebViewGold app — done-for-you, fast turnaround, Made in Germany. [Get your app set up →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **Build in your browser:** No Mac, no IDE: the **WebViewGold Cloud Builder** configures, builds & uploads your app online. [Discover Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
