---
title: "Open App Settings API – WebViewGold für Android Dokumentation"
description: "Send the user straight to the system App-info screen from your web app to manage permissions, notifications, storage, or force-stop your Android app."
lang: "de"
product: "WebViewGold für Android"
platform: "Android"
category: "APIs & Funktionen"
slug: "open-app-settings"
canonical_url: "https://www.webviewgold.com/de/docs/android/open-app-settings/"
keywords:
  - "Open App Settings API"
  - "WebViewGold für Android"
  - "Website in App umwandeln"
  - "WebView-App-Dokumentation"
  - "Android WebView SDK"
  - "PWA zu App"
  - "HTML zu App"
  - "JavaScript-Bridge"
last_updated: "2026-10-09"
---

# Open App Settings API – WebViewGold für Android

> **Zusammenfassung:** Send the user straight to the system App-info screen from your web app to manage permissions, notifications, storage, or force-stop your Android app.

[Dokumentation](../README.md) › [WebViewGold für Android](README.md) › Open App Settings API

**Plattform:** Android · **Kategorie:** APIs & Funktionen · **Online-Version:** [www.webviewgold.com/de/docs/android/open-app-settings/](https://www.webviewgold.com/de/docs/android/open-app-settings/)

---

Die **Open-App-Settings-API** von WebViewGold schickt den Nutzer direkt in den System-Bildschirm **App-Info** deiner App. Von dort aus lassen sich Berechtigungen, Benachrichtigungen und Speicher verwalten oder die App per Force-Stop beenden – ohne die Web-App zu verlassen und die Android-Einstellungen selbst zu durchsuchen.

## So verwendest du die Funktion

Öffne den Bildschirm über einen HTML-Link oder aus JavaScript:

```html
<a href="settingsapp://">Open app settings</a>
```

```javascript
window.location.href = "settingsapp://";
```

## Typische Anwendungsfälle

- Der Nutzer hat eine Berechtigung (Kamera, Mikrofon, Standort, Push) abgelehnt – direkter Weg zum System-Dialog, um sie wieder zu aktivieren.
- Nutzer anleiten, die Akku-Optimierung zu deaktivieren oder den Cache aus der System-Ebene zu leeren.

**Hinweise:** Keine Parameter. Jede URL, die mit `settingsapp://` beginnt, öffnet denselben Bildschirm. Funktioniert auf allen unterstützten Android-Versionen.

---

## Weiterlesen

- ← Vorherige: [NFC-Plugin](nfc.md)
- Weiter →: [Reconnect API](reconnect.md)
- Dieselbe Funktion auf anderen Plattformen: [iOS – Open-App-Settings-API](../ios/open-app-settings.md)
- Sprachen: [🇺🇸 English](../../android/open-app-settings.md) · **🇩🇪 Deutsch** · [🇫🇷 Français](../../fr/android/open-app-settings.md) · [🇪🇸 Español](../../es/android/open-app-settings.md) · [🇨🇳 中文](../../zh/android/open-app-settings.md)

> [!TIP]
> **Zu wenig Zeit? Wir richten deine App für dich ein.** Unser Team konfiguriert, erstellt & reicht deine WebViewGold-App ein – schlüsselfertig, mit schneller Bearbeitung, Made in Germany. [App einrichten lassen →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_android_doc_online)
>
> **Im Browser erstellen:** Kein Mac, keine IDE: Der **WebViewGold Cloud Builder** konfiguriert, erstellt & lädt deine App online hoch. [Cloud Builder entdecken →](https://www.webviewgold.com/cloud-builder?ref=android_docs)
