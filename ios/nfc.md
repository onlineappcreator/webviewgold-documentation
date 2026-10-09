---
title: "NFC Plugin – WebViewGold for iOS Documentation"
description: "Read NFC tags natively in your iOS WebView app and pass tag data to your web app."
lang: "en"
product: "WebViewGold for iOS"
platform: "iOS"
category: "Extensions & Plugins"
slug: "nfc"
canonical_url: "https://www.webviewgold.com/docs/iOS/nfc/"
keywords:
  - "NFC Plugin"
  - "WebViewGold for iOS"
  - "convert website to app"
  - "WebView app documentation"
  - "iOS WebView SDK"
  - "PWA to app"
  - "HTML to app"
  - "JavaScript bridge"
last_updated: "2026-10-09"
---

# NFC Plugin – WebViewGold for iOS

> **Summary:** Read NFC tags natively in your iOS WebView app and pass tag data to your web app.

[Documentation](../README.md) › [WebViewGold for iOS](README.md) › NFC Plugin

**Platform:** iOS · **Category:** Extensions & Plugins · **Online version:** [www.webviewgold.com/docs/iOS/nfc/](https://www.webviewgold.com/docs/iOS/nfc/)

---

**Near-Field Communication (NFC)** technology is one of the latest technologies that has become very popular among mobile users. It enables two devices or a device and an NFC tag to communicate wirelessly when in close proximity. NFC is widely used on iOS devices for reading and writing small amounts of data, making it an effective tool for sharing information via NFC-enabled cards or tags.

The NFC API allows developers to read and write data to NFC tags directly from app code. This opens up new ways for apps to interact with users, from sharing contact information to embedding text snippets.

## WebViewGold NFC Plugin Integration

While NFC is not part of the general WebViewGold feature scope, we offer a custom, easy WebViewGold NFC plugin integration (via JavaScript) on an individual basis.

Please send us your requirements (e.g., writing/reading text snippets and/or contact card details to/from NFC tags) via an email to [webviewgold-nfc@onlineappcreator.com](mailto:webviewgold-nfc@onlineappcreator.com) for a free consultation and a non-binding quote.

**Writing**\
To write a value to an NFC tag, send a command from your web app by loading the following URL: `writenfc://?value=data`\
Example:\
`<a href="writenfc://?value=WebViewGold.com"> Write to an NFC tag </a>`\
This puts your app into Write Mode and stores the value until a tag is scanned.

**Writing to a VCARD**\
Use the same API as writing plaintext. Format the text like:

```
VCARD
FN:John Doe
Title:Developer
TEL;TYPE=CELL:0452641211
_
_
_
```

Separate properties with an underscore (`_`) and prefix the text with `VCARD_`. See <https://en.wikipedia.org/wiki/VCard#Properties> for a list of supported properties.

**Reading**\
To read an NFC tag, load `readnfc://`. The app will return the information to your web app by calling `readNFCResult(data, id, tag)` where `data` is the stored value, `id` the tag identifier and `tag` the tag type. Define this JavaScript function in your web app to handle the values.

## How to Test the API

1. Open the Config file of your app’s codebase.
2. Enter your purchase code.
3. Set the app’s URL to the NFC API Test Page: <https://webviewgoldtest.github.io/NFCtesting.html>
4. Run the app.
5. Press one of the Read or Write options to enable the corresponding mode. If writing, enter a value.
6. Bring the NFC tag to the device to complete the read or write operation. The test page and app will display the results.

---

## Continue reading

- ← Previous: [MultiAPICall Feature](multi-api-call.md)
- Next →: [Siri Plugin](siri.md)
- Same feature on other platforms: [Android – NFC Plugin](../android/nfc.md)
- Languages: **🇺🇸 English** · [🇩🇪 Deutsch](../de/ios/nfc.md) · [🇫🇷 Français](../fr/ios/nfc.md) · [🇪🇸 Español](../es/ios/nfc.md) · [🇨🇳 中文](../zh/ios/nfc.md)

> [!TIP]
> **Too busy? We set up your app for you.** Our team configures, builds & submits your WebViewGold app — done-for-you, fast turnaround, Made in Germany. [Get your app set up →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **Build in your browser:** No Mac, no IDE: the **WebViewGold Cloud Builder** configures, builds & uploads your app online. [Discover Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
