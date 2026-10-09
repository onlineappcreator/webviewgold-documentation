---
title: "Contacts API – WebViewGold for Android Documentation"
description: "Access the device address book from your web app: read contacts with user permission in WebViewGold for Android."
lang: "en"
product: "WebViewGold for Android"
platform: "Android"
category: "APIs & Features"
slug: "contacts"
canonical_url: "https://www.webviewgold.com/docs/android/contacts/"
keywords:
  - "Contacts API"
  - "WebViewGold for Android"
  - "convert website to app"
  - "WebView app documentation"
  - "Android WebView SDK"
  - "PWA to app"
  - "HTML to app"
  - "JavaScript bridge"
last_updated: "2026-10-09"
---

# Contacts API – WebViewGold for Android

> **Summary:** Access the device address book from your web app: read contacts with user permission in WebViewGold for Android.

[Documentation](../README.md) › [WebViewGold for Android](README.md) › Contacts API

**Platform:** Android · **Category:** APIs & Features · **Online version:** [www.webviewgold.com/docs/android/contacts/](https://www.webviewgold.com/docs/android/contacts/)

---

WebViewGold allows for the export of contacts into a JavaScript variable, in the format below via the **readcontacts://** API. The JSON object is stored in the `contacts` variable. In order to access this, your app must first gain permission through the **requestcontactpermission://** API, which will prompt your user to enable contact permissions. Without completing this step, the **readcontacts://** will populate the `contacts` variable with a null value.\
Example output stored in JS `contacts` variable:

```json
 {
   "John Appleseed":[
      "888-555-5512",
      "888-555-1212"
   ],
   "Daniel Higgins":[
      "555-478-7672",
      "(408) 555-5270",
      "(408) 555-3514"
   ],
   "David Taylor":[
      "555-610-6679"
   ],
   "Hank Zakroff":[
      "(555) 766-4823",
      "(707) 555-1854"
   ]
}
```

In order to add this contact functionality, the `android.permission.READ_CONTACTS` permission needs to be added to the *AndroidManifest.xml* file so the permission can be granted by users.

---

## Continue reading

- ← Previous: [App Version Check API](app-version-check.md)
- Next →: [Dynamic UI API](dynamic-ui.md)
- Same feature on other platforms: [iOS – Contacts API](../ios/contacts.md)
- Languages: **🇺🇸 English** · [🇩🇪 Deutsch](../de/android/contacts.md) · [🇫🇷 Français](../fr/android/contacts.md) · [🇪🇸 Español](../es/android/contacts.md) · [🇨🇳 中文](../zh/android/contacts.md)

> [!TIP]
> **Too busy? We set up your app for you.** Our team configures, builds & submits your WebViewGold app — done-for-you, fast turnaround, Made in Germany. [Get your app set up →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_android_doc_online)
>
> **Build in your browser:** No Mac, no IDE: the **WebViewGold Cloud Builder** configures, builds & uploads your app online. [Discover Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=android_docs)
