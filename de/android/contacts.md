---
title: "Kontakte-API – WebViewGold für Android Dokumentation"
description: "Greife aus deiner Web-App auf das Adressbuch des Geräts zu: Lies Kontakte mit Nutzerberechtigung in WebViewGold für Android."
lang: "de"
product: "WebViewGold für Android"
platform: "Android"
category: "APIs & Funktionen"
slug: "contacts"
canonical_url: "https://www.webviewgold.com/de/docs/android/contacts/"
keywords:
  - "Kontakte-API"
  - "WebViewGold für Android"
  - "Website in App umwandeln"
  - "WebView-App-Dokumentation"
  - "Android WebView SDK"
  - "PWA zu App"
  - "HTML zu App"
  - "JavaScript-Bridge"
last_updated: "2026-10-09"
---

# Kontakte-API – WebViewGold für Android

> **Zusammenfassung:** Greife aus deiner Web-App auf das Adressbuch des Geräts zu: Lies Kontakte mit Nutzerberechtigung in WebViewGold für Android.

[Dokumentation](../README.md) › [WebViewGold für Android](README.md) › Kontakte-API

**Plattform:** Android · **Kategorie:** APIs & Funktionen · **Online-Version:** [www.webviewgold.com/de/docs/android/contacts/](https://www.webviewgold.com/de/docs/android/contacts/)

---

WebViewGold ermöglicht den Export von Kontakten in eine JavaScript-Variable, im unten stehenden Format über die **readcontacts://** API. Das JSON-Objekt wird in der Variablen `contacts` gespeichert. Um darauf zuzugreifen, muss deine App zunächst über die **requestcontactpermission://** API eine Berechtigung einholen, die deinen Nutzer auffordert, die Kontaktberechtigungen zu aktivieren. Ohne diesen Schritt füllt **readcontacts://** die Variable `contacts` mit einem Null-Wert.\
Beispielausgabe, gespeichert in der JS-Variablen `contacts`:

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

Um diese Kontaktfunktionalität hinzuzufügen, muss die Berechtigung `android.permission.READ_CONTACTS` zur Datei *AndroidManifest.xml* hinzugefügt werden, damit die Berechtigung von den Nutzern erteilt werden kann.

---

## Weiterlesen

- ← Vorherige: [App-Versionsprüfung-API](app-version-check.md)
- Weiter →: [Dynamische-UI-API](dynamic-ui.md)
- Dieselbe Funktion auf anderen Plattformen: [iOS – Kontakte-API](../ios/contacts.md)
- Sprachen: [🇺🇸 English](../../android/contacts.md) · **🇩🇪 Deutsch** · [🇫🇷 Français](../../fr/android/contacts.md) · [🇪🇸 Español](../../es/android/contacts.md) · [🇨🇳 中文](../../zh/android/contacts.md)

> [!TIP]
> **Zu wenig Zeit? Wir richten deine App für dich ein.** Unser Team konfiguriert, erstellt & reicht deine WebViewGold-App ein – schlüsselfertig, mit schneller Bearbeitung, Made in Germany. [App einrichten lassen →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_android_doc_online)
>
> **Im Browser erstellen:** Kein Mac, keine IDE: Der **WebViewGold Cloud Builder** konfiguriert, erstellt & lädt deine App online hoch. [Cloud Builder entdecken →](https://www.webviewgold.com/cloud-builder?ref=android_docs)
