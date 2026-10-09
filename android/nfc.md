---
title: "NFC Plugin – WebViewGold for Android Documentation"
description: "Read NFC tags natively in your Android WebView app and pass tag data to your web app."
lang: "en"
product: "WebViewGold for Android"
platform: "Android"
category: "APIs & Features"
slug: "nfc"
canonical_url: "https://www.webviewgold.com/docs/android/nfc/"
keywords:
  - "NFC Plugin"
  - "WebViewGold for Android"
  - "convert website to app"
  - "WebView app documentation"
  - "Android WebView SDK"
  - "PWA to app"
  - "HTML to app"
  - "JavaScript bridge"
last_updated: "2026-10-09"
---

# NFC Plugin – WebViewGold for Android

> **Summary:** Read NFC tags natively in your Android WebView app and pass tag data to your web app.

[Documentation](../README.md) › [WebViewGold for Android](README.md) › NFC Plugin

**Platform:** Android · **Category:** APIs & Features · **Online version:** [www.webviewgold.com/docs/android/nfc/](https://www.webviewgold.com/docs/android/nfc/)

---

**Near-Field Communication (NFC)** enables two devices or a device and an NFC tag to communicate wirelessly when in close proximity. NFC is widely used on Android devices for reading and writing small amounts of data, making it an effective tool for sharing information via NFC-enabled cards or tags.

The **WebViewGold NFC API** lets your web app read and write NFC tags directly via a JavaScript bridge — from sharing contact information to embedding text snippets.

**Writing**\
To write a value to an NFC tag, send a command from your web app by loading the following URL: `writenfc://?value=data`\
Example:\
`<a href="writenfc://?value=WebViewGold.com"> Write to an NFC tag </a>`\
This puts your app into Write Mode and stores the value until a tag is scanned: as soon as the user holds an NFC tag to the device, the value is written to it.

**Writing a VCARD (contact card)**\
Use the same API as for writing plain text and format the text like this:

```
VCARD
FN:John Doe
Title:Developer
TEL;TYPE=CELL:0452641211
```

Separate the properties with an underscore (`_`), encode spaces as `%20`, and prefix the text with `VCARD_`. Example:

```
writenfc://?value=VCARD_FN:John%20Doe_Title:Developer_TEL;TYPE=CELL:0452641211
```

See <https://en.wikipedia.org/wiki/VCard#Properties> for a list of supported properties.

**Reading**\
To read an NFC tag, load `readnfc://`. This puts your app into Read Mode. When the user scans a tag, the app returns the stored information to your web app by calling the JavaScript function `readNFCResult(data)`, where `data` is the value stored on the tag. Define this JavaScript function in your web app to handle the value:

```html
<script>
window.location.href = "readnfc://";

function readNFCResult(data) {
    alert("NFC tag content: " + data);
}
</script>
```

## How to Test the API

1. Open the Config file of your app’s codebase.
2. Enter your purchase code.
3. Set the app’s URL to the NFC API Test Page: <https://webviewgoldtest.github.io/NFCtesting.html>
4. Run the app on a physical device with NFC support.
5. Press one of the Read or Write options to enable the corresponding mode. If writing, enter a value.
6. Bring the NFC tag to the device to complete the read or write operation. The test page and app will display the results.

**Need more?** If you require extended NFC functionality beyond this API (e.g., special tag types or custom data formats), we offer custom NFC plugin integrations on an individual basis. Please send us your requirements via an email to [webviewgold-nfc@onlineappcreator.com](mailto:webviewgold-nfc@onlineappcreator.com) for a free consultation and a non-binding quote.

---

## Continue reading

- ← Previous: [Haptic Feedback API](haptic-feedback.md)
- Next →: [Open App Settings API](open-app-settings.md)
- Same feature on other platforms: [iOS – NFC Plugin](../ios/nfc.md)
- Languages: **🇺🇸 English** · [🇩🇪 Deutsch](../de/android/nfc.md) · [🇫🇷 Français](../fr/android/nfc.md) · [🇪🇸 Español](../es/android/nfc.md) · [🇨🇳 中文](../zh/android/nfc.md)

> [!TIP]
> **Too busy? We set up your app for you.** Our team configures, builds & submits your WebViewGold app — done-for-you, fast turnaround, Made in Germany. [Get your app set up →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_android_doc_online)
>
> **Build in your browser:** No Mac, no IDE: the **WebViewGold Cloud Builder** configures, builds & uploads your app online. [Discover Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=android_docs)
