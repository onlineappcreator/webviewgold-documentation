---
title: "HTML5-Geolocation-API – WebViewGold für iOS Dokumentation"
description: "Aktiviere die HTML5-Geolokalisierung in deiner iOS-WebView-App und fordere präzise Standortberechtigungen auf die richtige Weise an."
lang: "de"
product: "WebViewGold für iOS"
platform: "iOS"
category: "APIs & Funktionen"
slug: "geolocation"
canonical_url: "https://www.webviewgold.com/de/docs/iOS/geolocation/"
keywords:
  - "Geolocation-API"
  - "WebViewGold für iOS"
  - "Website in App umwandeln"
  - "WebView-App-Dokumentation"
  - "iOS WebView SDK"
  - "PWA zu App"
  - "HTML zu App"
  - "JavaScript-Bridge"
last_updated: "2026-10-09"
---

# HTML5-Geolocation-API – WebViewGold für iOS

> **Zusammenfassung:** Aktiviere die HTML5-Geolokalisierung in deiner iOS-WebView-App und fordere präzise Standortberechtigungen auf die richtige Weise an.

[Dokumentation](../README.md) › [WebViewGold für iOS](README.md) › Geolocation-API

**Plattform:** iOS · **Kategorie:** APIs & Funktionen · **Online-Version:** [www.webviewgold.com/de/docs/iOS/geolocation/](https://www.webviewgold.com/de/docs/iOS/geolocation/)

---

Die HTML5-Geolocation-API ermöglicht es Nutzern, ihren Standort mit deiner App zu teilen, und erweitert Funktionen wie standortbezogene Inhalte. In WebViewGold wird die Geolocation-API standardmäßig unterstützt, sobald sie in deinen Web-Content integriert ist. So implementierst du das Geolocation-Tracking in deiner WebView-basierten iOS-App:

## HTML5-Geolocation einrichten

Für die grundlegende Geolocation-Einrichtung findest du in [Mozillas Geolocation-Guide](https://developer.mozilla.org/en-US/docs/Web/API/Geolocation_API) Details dazu, wie du diese Funktion in deine Website oder Web-App integrieren kannst.

Zur Demonstration besuche diese [W3Schools-Geolocation-Demo](https://www.w3schools.com/html/html5_geolocation.asp).

Seit iOS 10 ist Geolocation nur noch auf HTTPS-Seiten verfügbar. Stelle daher sicher, dass du bei Standortabfragen eine Web-App-URL verwendest, die mit `https://` statt `http://` beginnt.

## Standortzugriff im Hintergrund

Standardmäßig funktionieren Standortabfragen nur, während die App im Vordergrund ist. Wenn deine Web-App auch im Hintergrund weiter Standort-Updates erhalten soll (z. B. für Tracking- oder Geofencing-Anwendungsfälle), aktiviere die Hintergrund-Standort-Option in **Config.swift**:

```swift
static let backgroundlocation = true
```

- Füge in den Xcode-Projekteinstellungen dem WebViewGold-Target die Capability **Background Modes** hinzu und aktiviere **Location updates**.
- Je nach Web-App musst du zusätzlich **Background Processing** aktivieren. Füge in diesem Fall außerdem ein Array mit dem Schlüssel `Permitted background task scheduler identifiers` in deine **Info.plist** ein und hinterlege darin einen String mit deiner App-Bundle-ID (z. B. `com.yourcompany.yourapp`).
- Beachte, dass Standortzugriff im Hintergrund im App-Store-Review eine klare Begründung erfordert – beschreibe den Nutzen für die Anwender in deinen Review-Notizen.

---

## Weiterlesen

- ← Vorherige: [Safe Area anpassen](safe-area.md)
- Weiter →: [Push-Benachrichtigungen-API](push-notifications.md)
- Dieselbe Funktion auf anderen Plattformen: [Android – Geolocation-API](../android/geolocation.md)
- Sprachen: [🇺🇸 English](../../ios/geolocation.md) · **🇩🇪 Deutsch** · [🇫🇷 Français](../../fr/ios/geolocation.md) · [🇪🇸 Español](../../es/ios/geolocation.md) · [🇨🇳 中文](../../zh/ios/geolocation.md)

> [!TIP]
> **Zu wenig Zeit? Wir richten deine App für dich ein.** Unser Team konfiguriert, erstellt & reicht deine WebViewGold-App ein – schlüsselfertig, mit schneller Bearbeitung, Made in Germany. [App einrichten lassen →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **Im Browser erstellen:** Kein Mac, keine IDE: Der **WebViewGold Cloud Builder** konfiguriert, erstellt & lädt deine App online hoch. [Cloud Builder entdecken →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
