---
title: "Open-App-Settings-API – WebViewGold für iOS Dokumentation"
description: "Führe Nutzer direkt zur Seite deiner App in der iOS-Einstellungen-App, um Berechtigungen und Mitteilungen zu verwalten."
lang: "de"
product: "WebViewGold für iOS"
platform: "iOS"
category: "APIs & Funktionen"
slug: "open-app-settings"
canonical_url: "https://www.webviewgold.com/de/docs/iOS/open-app-settings/"
keywords:
  - "Open-App-Settings-API"
  - "WebViewGold für iOS"
  - "Website in App umwandeln"
  - "WebView-App-Dokumentation"
  - "iOS WebView SDK"
  - "PWA zu App"
  - "HTML zu App"
  - "JavaScript-Bridge"
last_updated: "2026-10-09"
---

# Open-App-Settings-API – WebViewGold für iOS

> **Zusammenfassung:** Führe Nutzer direkt zur Seite deiner App in der iOS-Einstellungen-App, um Berechtigungen und Mitteilungen zu verwalten.

[Dokumentation](../README.md) › [WebViewGold für iOS](README.md) › Open-App-Settings-API

**Plattform:** iOS · **Kategorie:** APIs & Funktionen · **Online-Version:** [www.webviewgold.com/de/docs/iOS/open-app-settings/](https://www.webviewgold.com/de/docs/iOS/open-app-settings/)

---

Die **Open-App-Settings-API** von WebViewGold führt den Nutzer direkt zur Seite deiner App in der nativen iOS-**Einstellungen**-App. Dort kann er Berechtigungen (Kamera, Standort, Mitteilungen…), Sprache und weitere App-Einstellungen verwalten — ohne deine Web-App zu verlassen und sich durch die iOS-Einstellungen zu suchen.

## Verwendung

Löse den Bildschirm über einen HTML-Link oder per JavaScript aus:

```html
<a href="settingsapp://">App-Einstellungen öffnen</a>
```

```javascript
window.location.href = "settingsapp://";
```

## Typische Anwendungsfälle

- Der Nutzer hat eine Berechtigung verweigert (Kamera, Mikrofon, Standort, Mitteilungen) — schicke ihn direkt zum System-Bildschirm, um sie wieder zu aktivieren.
- Führe den Nutzer zu den Mitteilungseinstellungen deiner App, z. B. in Kombination mit dem `checkNativePushPermissions://`-Aufruf der [Push-Notifications-API](push-notifications.md).

**Hinweise:** Keine Parameter. Jede URL, die mit `settingsapp://` beginnt, öffnet denselben Bildschirm.

---

## Weiterlesen

- ← Vorherige: [Read/Write-Value-API](read-write-value.md)
- Weiter →: [Share Extension](share-extension.md)
- Dieselbe Funktion auf anderen Plattformen: [Android – Open App Settings API](../android/open-app-settings.md)
- Sprachen: [🇺🇸 English](../../ios/open-app-settings.md) · **🇩🇪 Deutsch** · [🇫🇷 Français](../../fr/ios/open-app-settings.md) · [🇪🇸 Español](../../es/ios/open-app-settings.md) · [🇨🇳 中文](../../zh/ios/open-app-settings.md)

> [!TIP]
> **Zu wenig Zeit? Wir richten deine App für dich ein.** Unser Team konfiguriert, erstellt & reicht deine WebViewGold-App ein – schlüsselfertig, mit schneller Bearbeitung, Made in Germany. [App einrichten lassen →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **Im Browser erstellen:** Kein Mac, keine IDE: Der **WebViewGold Cloud Builder** konfiguriert, erstellt & lädt deine App online hoch. [Cloud Builder entdecken →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
