---
title: "Set Up Your Web App or Website – WebViewGold for Android Documentation"
description: "Prepare your website, PWA, or local HTML files for your Android app: use a remote URL, bundle files offline in the app, or combine both with an offline fallback."
lang: "en"
product: "WebViewGold for Android"
platform: "Android"
category: "Get Started"
slug: "setup-website"
canonical_url: "https://www.webviewgold.com/docs/android/setup-website/"
keywords:
  - "Set up your web app"
  - "WebViewGold for Android"
  - "convert website to app"
  - "WebView app documentation"
  - "Android WebView SDK"
  - "PWA to app"
  - "HTML to app"
  - "JavaScript bridge"
last_updated: "2026-10-09"
---

# Set Up Your Web App or Website – WebViewGold for Android

> **Summary:** Prepare your website, PWA, or local HTML files for your Android app: use a remote URL, bundle files offline in the app, or combine both with an offline fallback.

[Documentation](../README.md) › [WebViewGold for Android](README.md) › Set up your web app

**Platform:** Android · **Category:** Get Started · **Online version:** [www.webviewgold.com/docs/android/setup-website/](https://www.webviewgold.com/docs/android/setup-website/)

---

## Option A) Use a URL for accessing your web application (= store files online)

Create a mobile-optimized website or web app and upload it to your webserver/webspace. WebViewGold for Android supports classic HTML, PHP, WordPress, Progressive Web Apps, HTML5 games, Wix, apprat.io, Bubble, jQuery Mobile, and modern AI/no-code builders such as Lovable, Base44, and Bolt. A common implementation pattern is to build the product UI in jQuery, Lovable, Base44, Bolt, React, Vue, Angular, or your preferred stack, then use WebViewGold as the native Android app shell that adds Google Play packaging, push notifications, device APIs, URL handling, and other native capabilities.

For best Google Play review results, optimize the website so it behaves like a polished Android app: responsive breakpoints, fast loading, clear offline/error states, accessible tap targets, and predictable back-button behavior. By default, WebViewGold for Android permits both HTTPS and HTTP content. For a more production-grade security profile, restrict traffic to HTTPS by [switching cleartext traffic off](https://www.webviewgold.com/support-center/knowledgebase/how-to-prevent-non-https-connections-in-webviewgold-for-android-switching-usescleartexttraffic-from-true-to-false/) and consider the `BLOCK_SELF_SIGNED_AND_FAULTY_SSL_CERTS` option. Please consider a professional User Experience/UX Review on [UXreviewer.io](https://www.uxreviewer.io) or similar services to improve approval readiness and long-term retention.

## Option B) Use a local HTML folder for accessing your web application (= store files within the app)

WebViewGold supports web apps based on local HTML folders, too: Copy your HTML/CSS/JavaScript files to the Android Studio project and set **USE_LOCAL_HTML_FOLDER** to **true** (see [next step](setup.md)). Please consider a professional User Experience/UX Review on [UXreviewer.io](https://www.uxreviewer.io) or similar services for best Play Store approval results. Such a UX review also helps you to achieve better customer retention in general for your product with suggestions for improvement.

[![Watch the video: Set Up Your Web App or Website](https://img.youtube.com/vi/CtyyZrNVcek/hqdefault.jpg)](https://www.youtube.com/watch?v=CtyyZrNVcek)

## Option C) Use an HTML folder if the user is offline, and use a remote URL if the user is online (= store files online + store backup/fallback files within the app)

Copy your HTML/CSS/JavaScript files to the Android Studio project, set **USE_LOCAL_HTML_FOLDER** to **false** (see [next step](setup.md)) and set **FALLBACK_USE_LOCAL_HTML_FOLDER_IF_OFFLINE** to **true** (see [next step](setup.md)). Please consider a professional User Experience/UX Review on [UXreviewer.io](https://www.uxreviewer.io) or similar services for best Play Store approval results. Such a UX review also helps you to achieve better customer retention in general for your product with suggestions for improvement.

[![Watch the video: Set Up Your Web App or Website](https://img.youtube.com/vi/W0NrpCKB7aU/hqdefault.jpg)](https://www.youtube.com/watch?v=W0NrpCKB7aU)

---

## Continue reading

- ← Back to: [Overview](README.md)
- Next →: [Configure WebViewGold](setup.md)
- Same feature on other platforms: [iOS – Set up your web app](../ios/setup-website.md) · [macOS – Setting up your web app](../macos/setup-website.md)
- Languages: **🇺🇸 English** · [🇩🇪 Deutsch](../de/android/setup-website.md) · [🇫🇷 Français](../fr/android/setup-website.md) · [🇪🇸 Español](../es/android/setup-website.md) · [🇨🇳 中文](../zh/android/setup-website.md)

> [!TIP]
> **Too busy? We set up your app for you.** Our team configures, builds & submits your WebViewGold app — done-for-you, fast turnaround, Made in Germany. [Get your app set up →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_android_doc_online)
>
> **Build in your browser:** No Mac, no IDE: the **WebViewGold Cloud Builder** configures, builds & uploads your app online. [Discover Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=android_docs)
