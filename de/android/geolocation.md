---
title: "HTML5-Geolocation-API – WebViewGold für Android Dokumentation"
description: "Aktiviere HTML5-Geolocation in deiner Android-WebView-App und fordere Standortberechtigungen korrekt an."
lang: "de"
product: "WebViewGold für Android"
platform: "Android"
category: "APIs & Funktionen"
slug: "geolocation"
canonical_url: "https://www.webviewgold.com/de/docs/android/geolocation/"
keywords:
  - "Geolocation-API"
  - "WebViewGold für Android"
  - "Website in App umwandeln"
  - "WebView-App-Dokumentation"
  - "Android WebView SDK"
  - "PWA zu App"
  - "HTML zu App"
  - "JavaScript-Bridge"
last_updated: "2026-10-09"
---

# HTML5-Geolocation-API – WebViewGold für Android

> **Zusammenfassung:** Aktiviere HTML5-Geolocation in deiner Android-WebView-App und fordere Standortberechtigungen korrekt an.

[Dokumentation](../README.md) › [WebViewGold für Android](README.md) › Geolocation-API

**Plattform:** Android · **Kategorie:** APIs & Funktionen · **Online-Version:** [www.webviewgold.com/de/docs/android/geolocation/](https://www.webviewgold.com/de/docs/android/geolocation/)

---

Die HTML5 Geolocation API ermöglicht es Nutzern, ihren Standort mit deiner App zu teilen und Funktionen wie standortbasierte Inhalte zu verbessern. In WebViewGold wird die Geolocation API standardmäßig unterstützt, sobald sie in deine Webinhalte integriert ist. So implementierst du die Standortverfolgung in deine WebView-basierte Android-App:

## Einrichten der HTML5-Geolocation

Für die grundlegende Geolocation-Einrichtung findest du im [Geolocation-Leitfaden von Mozilla](https://developer.mozilla.org/en-US/docs/Web/API/Geolocation_API) Details dazu, wie du diese Funktion in deine Website oder Web-App implementierst.

Eine Demonstration findest du in dieser [W3Schools Geolocation Demo](https://www.w3schools.com/html/html5_geolocation.asp).

## Standortverfolgung im Hintergrund aktivieren (nur Android)

Um die Standortverfolgung im Hintergrund für deine WebView-basierte Android-App zu aktivieren, führe die folgenden Schritte aus:

1. Lege die Berechtigungen in **Config.java** fest:
   - Setze `requireBackgroundLocation` auf `true`, wenn die Standortverfolgung im Hintergrund benötigt wird.
   - Stelle sicher, dass auch `requireLocation` auf `true` gesetzt ist, um überhaupt Standortdienste zu aktivieren.
2. Passe die Berechtigungen in **AndroidManifest.xml** an:
   - Entferne die Kommentarzeichen bei den Berechtigungsblöcken für `android.permission.FOREGROUND_SERVICE_LOCATION` und `GPSService`.
   - Suche innerhalb der Datei nach diesen Begriffen, um sicherzustellen, dass die richtigen Berechtigungen gesetzt sind.

## Standortverfolgung im Hintergrund über URL-Schemata ein-/ausschalten

Verwende die folgenden URL-Schemata, um die Standortverfolgung im Hintergrund innerhalb deiner WebView-basierten Android-App ein- oder auszuschalten:

Um die Standortverfolgung im Hintergrund einzuschalten, leite den Nutzer auf die folgende URL um:

```html
<script>window.location.href = "backgroundlocationon://";  </script>
```

Um die Standortverfolgung im Hintergrund auszuschalten, leite den Nutzer auf die folgende URL um:

```html
<script>window.location.href = "backgroundlocationoff://";  </script>
```

**Hinweis:** Diese URL-Schemata sind spezifisch für WebViewGold für Android und funktionieren möglicherweise nicht in herkömmlichen Webbrowsern. Um sicherzustellen, dass diese Weiterleitungen nur für Android-App-Nutzer angewendet werden, solltest du den User-Agent erkennen.

---

## Weiterlesen

- ← Vorherige: [Multi API Call](multi-api-call.md)
- Weiter →: [Push-Benachrichtigungs-API](push-notifications.md)
- Dieselbe Funktion auf anderen Plattformen: [iOS – Geolocation-API](../ios/geolocation.md)
- Sprachen: [🇺🇸 English](../../android/geolocation.md) · **🇩🇪 Deutsch** · [🇫🇷 Français](../../fr/android/geolocation.md) · [🇪🇸 Español](../../es/android/geolocation.md) · [🇨🇳 中文](../../zh/android/geolocation.md)

> [!TIP]
> **Zu wenig Zeit? Wir richten deine App für dich ein.** Unser Team konfiguriert, erstellt & reicht deine WebViewGold-App ein – schlüsselfertig, mit schneller Bearbeitung, Made in Germany. [App einrichten lassen →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_android_doc_online)
>
> **Im Browser erstellen:** Kein Mac, keine IDE: Der **WebViewGold Cloud Builder** konfiguriert, erstellt & lädt deine App online hoch. [Cloud Builder entdecken →](https://www.webviewgold.com/cloud-builder?ref=android_docs)
