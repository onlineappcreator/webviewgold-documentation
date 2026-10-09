---
title: "Reconnect-API – WebViewGold für iOS Dokumentation"
description: "Füge deiner Offline-Fallback-Seite einen „Erneut versuchen“-Button hinzu, der die letzte Online-URL deiner iOS-App neu lädt."
lang: "de"
product: "WebViewGold für iOS"
platform: "iOS"
category: "APIs & Funktionen"
slug: "reconnect"
canonical_url: "https://www.webviewgold.com/de/docs/iOS/reconnect/"
keywords:
  - "Reconnect-API"
  - "WebViewGold für iOS"
  - "Website in App umwandeln"
  - "WebView-App-Dokumentation"
  - "iOS WebView SDK"
  - "PWA zu App"
  - "HTML zu App"
  - "JavaScript-Bridge"
last_updated: "2026-10-09"
---

# Reconnect-API – WebViewGold für iOS

> **Zusammenfassung:** Füge deiner Offline-Fallback-Seite einen „Erneut versuchen“-Button hinzu, der die letzte Online-URL deiner iOS-App neu lädt.

[Dokumentation](../README.md) › [WebViewGold für iOS](README.md) › Reconnect-API

**Plattform:** iOS · **Kategorie:** APIs & Funktionen · **Online-Version:** [www.webviewgold.com/de/docs/iOS/reconnect/](https://www.webviewgold.com/de/docs/iOS/reconnect/)

---

Die **Reconnect-API** lädt die letzte Online-URL neu, auf der sich der Nutzer befand, bevor deine App auf die Offline-HTML-Seite zurückgefallen ist. Sie ist als „Erneut versuchen“-Button auf deinem eigenen Offline-/Fallback-Screen gedacht.

## Verwendung

Füge den Trigger auf deiner Offline-Seite ein (typischerweise `local-html/index.html`):

```html
<button onclick="window.location.href='reconnect://'">Erneut verbinden</button>
```

## So funktioniert es

Die App merkt sich die zuletzt erfolgreich geladene URL. Tippt der Nutzer auf `reconnect://`, navigiert die WebView zurück zu dieser URL. Besteht weiterhin keine Verbindung, wird erneut deine Fallback-Seite angezeigt.

## Zugehörige Konfiguration

- `offlinelocalhtmlswitch` in **Config.swift** muss auf `true` gesetzt sein, und du benötigst eine `local-html/index.html`-Fallback-Seite, damit dieses Feature sinnvoll ist. Details zum Offline-Fallback-Modus findest du unter [Web-App einrichten](setup-website.md).

---

## Weiterlesen

- ← Vorherige: [Social Login Helper](social-login.md)
- Weiter →: [Eigenes CSS & JS API](custom-css-js.md)
- Dieselbe Funktion auf anderen Plattformen: [Android – Reconnect API](../android/reconnect.md)
- Sprachen: [🇺🇸 English](../../ios/reconnect.md) · **🇩🇪 Deutsch** · [🇫🇷 Français](../../fr/ios/reconnect.md) · [🇪🇸 Español](../../es/ios/reconnect.md) · [🇨🇳 中文](../../zh/ios/reconnect.md)

> [!TIP]
> **Zu wenig Zeit? Wir richten deine App für dich ein.** Unser Team konfiguriert, erstellt & reicht deine WebViewGold-App ein – schlüsselfertig, mit schneller Bearbeitung, Made in Germany. [App einrichten lassen →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **Im Browser erstellen:** Kein Mac, keine IDE: Der **WebViewGold Cloud Builder** konfiguriert, erstellt & lädt deine App online hoch. [Cloud Builder entdecken →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
