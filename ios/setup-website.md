---
title: "Set Up Your Web App or Website – WebViewGold for iOS Documentation"
description: "Prepare your website, PWA, or local HTML files for your iOS app: use a remote URL, bundle files offline in the app, or combine both with an offline fallback."
lang: "en"
product: "WebViewGold for iOS"
platform: "iOS"
category: "Get Started"
slug: "setup-website"
canonical_url: "https://www.webviewgold.com/docs/iOS/setup-website/"
keywords:
  - "Set up your web app"
  - "WebViewGold for iOS"
  - "convert website to app"
  - "WebView app documentation"
  - "iOS WebView SDK"
  - "PWA to app"
  - "HTML to app"
  - "JavaScript bridge"
last_updated: "2026-10-09"
---

# Set Up Your Web App or Website – WebViewGold for iOS

> **Summary:** Prepare your website, PWA, or local HTML files for your iOS app: use a remote URL, bundle files offline in the app, or combine both with an offline fallback.

[Documentation](../README.md) › [WebViewGold for iOS](README.md) › Set up your web app

**Platform:** iOS · **Category:** Get Started · **Online version:** [www.webviewgold.com/docs/iOS/setup-website/](https://www.webviewgold.com/docs/iOS/setup-website/)

---

## Option A) Use a URL for accessing your web application (= store files online)

Create a mobile-optimized website or web app and upload it to your webserver/webspace. WebViewGold for iOS is compatible with classic HTML, PHP, WordPress, Progressive Web Apps, HTML5 games, Wix, apprat.io, Bubble, jQuery Mobile, and modern AI/no-code builders such as Lovable, Base44, and Bolt. In a typical workflow, you build the product UI in jQuery, Lovable, Base44, Bolt, React, Vue, Angular, or your preferred stack, then use WebViewGold as the native iOS app shell that adds App Store packaging, push notifications, device APIs, URL handling, and other native capabilities.

For the best App Store review results, design your web experience to feel intentional on iPhone and iPad: responsive layouts, large tap targets, fast first paint, clear loading/empty/error states, and app-like navigation. By default, WebViewGold for iOS permits both HTTPS content and HTTP content. For a more production-grade security profile, restrict traffic to HTTPS by [modifying the iOS transport security setting](https://www.webviewgold.com/support-center/knowledgebase/how-to-prevent-non-https-connections-in-webviewgold-for-ios-removing-nsallowsarbitraryloadsinwebcontent-from-info-plist/) and consider the `blockfaultyandselfsignedhttpscerts` option. Please consider a professional User Experience/UX Review on [UXreviewer.io](https://www.uxreviewer.io) or similar services to improve store approval readiness and long-term user retention.

## Option B) Use a local HTML folder for accessing your web application (= store files within the app)

WebViewGold supports web apps based on local HTML folders, too: Set **uselocalhtmlfolder** to **true** (see [next step](setup.md)) and copy your HTML/CSS/JavaScript files (including subdirectories) to the "local-www" folder in your Xcode project. To do this, make sure to:

1. Delete the default files in the "local-www" folder by selecting them in the Xcode file hierarchy, then right-click to press "Delete", then press "Move to Trash".
2. Select all the files for your local website, then drag and drop them into the Xcode file hierarchy under the "local-www" folder. Make sure "Create folder references" is checked and press "Finish".

Please consider a professional User Experience/UX Review on [UXreviewer.io](https://www.uxreviewer.io) or similar services for best App Store approval results. Such a UX review also helps you to achieve better customer retention in general for your product with suggestions for improvement.

## Option C) Use an HTML folder if the user is offline, and use a remote URL if the user is online (= store files online + store backup/fallback files within the app)

Copy your HTML/CSS/JavaScript files (including subdirectories) to the "local-www" folder in your Xcode project. To do this, make sure to:

1. Delete the default files in the "local-www" folder by selecting them in the Xcode file hierarchy, then right-click to press "Delete", then press "Move to Trash".
2. Select all the files for your local website, then drag and drop them into the Xcode file hierarchy under the "local-www" folder. Make sure "Create folder references" is checked and press "Finish".

Set **uselocalhtmlfolder** to **false** (see [next step](setup.md)) and set **offlinelocalhtmlswitch** to **true** (see [next step](setup.md)). Please consider a professional User Experience/UX Review on [UXreviewer.io](https://www.uxreviewer.io) or similar services for best App Store approval results. Such a UX review also helps you to achieve better customer retention in general for your product with suggestions for improvement.

---

## Continue reading

- ← Back to: [Overview](README.md)
- Next →: [Configure WebViewGold](setup.md)
- Same feature on other platforms: [Android – Set up your web app](../android/setup-website.md) · [macOS – Setting up your web app](../macos/setup-website.md)
- Languages: **🇺🇸 English** · [🇩🇪 Deutsch](../de/ios/setup-website.md) · [🇫🇷 Français](../fr/ios/setup-website.md) · [🇪🇸 Español](../es/ios/setup-website.md) · [🇨🇳 中文](../zh/ios/setup-website.md)

> [!TIP]
> **Too busy? We set up your app for you.** Our team configures, builds & submits your WebViewGold app — done-for-you, fast turnaround, Made in Germany. [Get your app set up →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **Build in your browser:** No Mac, no IDE: the **WebViewGold Cloud Builder** configures, builds & uploads your app online. [Discover Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
