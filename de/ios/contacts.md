---
title: "Kontakte-API – WebViewGold für iOS Dokumentation"
description: "Greife aus deiner Web-App auf das Adressbuch des Geräts zu: Lies Kontakte mit Nutzerberechtigung in WebViewGold für iOS."
lang: "de"
product: "WebViewGold für iOS"
platform: "iOS"
category: "APIs & Funktionen"
slug: "contacts"
canonical_url: "https://www.webviewgold.com/de/docs/iOS/contacts/"
keywords:
  - "Kontakte-API"
  - "WebViewGold für iOS"
  - "Website in App umwandeln"
  - "WebView-App-Dokumentation"
  - "iOS WebView SDK"
  - "PWA zu App"
  - "HTML zu App"
  - "JavaScript-Bridge"
last_updated: "2026-10-09"
---

# Kontakte-API – WebViewGold für iOS

> **Zusammenfassung:** Greife aus deiner Web-App auf das Adressbuch des Geräts zu: Lies Kontakte mit Nutzerberechtigung in WebViewGold für iOS.

[Dokumentation](../README.md) › [WebViewGold für iOS](README.md) › Kontakte-API

**Plattform:** iOS · **Kategorie:** APIs & Funktionen · **Online-Version:** [www.webviewgold.com/de/docs/iOS/contacts/](https://www.webviewgold.com/de/docs/iOS/contacts/)

---

WebViewGold ermöglicht den Export von Kontakten in eine JavaScript-Variable im untenstehenden Format über die **readcontacts://**-API. Das JSON-Objekt wird in der Variable `contacts` gespeichert. Um darauf zugreifen zu können, muss deine App zunächst über die **requestcontactpermission://**-API die Berechtigung erhalten, wodurch der Nutzer aufgefordert wird, den Zugriff auf Kontakte zu erlauben. Ohne diesen Schritt wird die **readcontacts://**-API die Variable `contacts` mit einem Nullwert füllen.\
Beispiel-Ausgabe, gespeichert in der JS-Variable `contacts`:

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

---

## Weiterlesen

- ← Vorherige: [Dynamisches-App-Icon-API](dynamic-app-icon.md)
- Weiter →: [Biometrische-Auth-API](biometric-authentication.md)
- Dieselbe Funktion auf anderen Plattformen: [Android – Kontakte-API](../android/contacts.md)
- Sprachen: [🇺🇸 English](../../ios/contacts.md) · **🇩🇪 Deutsch** · [🇫🇷 Français](../../fr/ios/contacts.md) · [🇪🇸 Español](../../es/ios/contacts.md) · [🇨🇳 中文](../../zh/ios/contacts.md)

> [!TIP]
> **Zu wenig Zeit? Wir richten deine App für dich ein.** Unser Team konfiguriert, erstellt & reicht deine WebViewGold-App ein – schlüsselfertig, mit schneller Bearbeitung, Made in Germany. [App einrichten lassen →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **Im Browser erstellen:** Kein Mac, keine IDE: Der **WebViewGold Cloud Builder** konfiguriert, erstellt & lädt deine App online hoch. [Cloud Builder entdecken →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
