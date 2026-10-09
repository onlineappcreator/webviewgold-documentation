---
title: "Taschenlampen-API – WebViewGold für iOS Dokumentation"
description: "Steuere die Taschenlampe des Geräts aus deiner Web-App mit einfachen JavaScript-Links in WebViewGold für iOS."
lang: "de"
product: "WebViewGold für iOS"
platform: "iOS"
category: "APIs & Funktionen"
slug: "flashlight"
canonical_url: "https://www.webviewgold.com/de/docs/iOS/flashlight/"
keywords:
  - "Taschenlampen-API"
  - "WebViewGold für iOS"
  - "Website in App umwandeln"
  - "WebView-App-Dokumentation"
  - "iOS WebView SDK"
  - "PWA zu App"
  - "HTML zu App"
  - "JavaScript-Bridge"
last_updated: "2026-10-09"
---

# Taschenlampen-API – WebViewGold für iOS

> **Zusammenfassung:** Steuere die Taschenlampe des Geräts aus deiner Web-App mit einfachen JavaScript-Links in WebViewGold für iOS.

[Dokumentation](../README.md) › [WebViewGold für iOS](README.md) › Taschenlampen-API

**Plattform:** iOS · **Kategorie:** APIs & Funktionen · **Online-Version:** [www.webviewgold.com/de/docs/iOS/flashlight/](https://www.webviewgold.com/de/docs/iOS/flashlight/)

---

Die Flashlight-API von WebViewGold ermöglicht es deiner Website, die Taschenlampe (Blitzlicht) des Geräts zu steuern. Diese Funktion kann nützlich sein für:

- Die Entwicklung von Utility-Apps, die eine Taschenlampen-Umschaltung erfordern
- Die Verbesserung des Nutzererlebnisses während der App-Nutzung durch Gamification
- Die Bereitstellung zusätzlicher Barrierefreiheitsfunktionen

## Verwendung

Du kannst die Taschenlampe direkt aus deinem HTML-Inhalt heraus mit den folgenden Links ein- oder ausschalten:

```html
<a href="enableflashlight://">Turn On Flashlight</a>
<a href="disableflashlight://">Turn Off Flashlight</a>
```

**Hinweis:** Stelle sicher, dass deine App über die erforderlichen Kamera-Berechtigungen in der Info.plist verfügt, da die Taschenlampen-Funktionalität an die Kamera-Hardware des Geräts gekoppelt ist.

---

## Weiterlesen

- ← Vorherige: [UUID-API](uuid.md)
- Weiter →: [App-Zurücksetzen-API](reset-app.md)
- Dieselbe Funktion auf anderen Plattformen: [Android – Taschenlampen-API](../android/flashlight.md)
- Sprachen: [🇺🇸 English](../../ios/flashlight.md) · **🇩🇪 Deutsch** · [🇫🇷 Français](../../fr/ios/flashlight.md) · [🇪🇸 Español](../../es/ios/flashlight.md) · [🇨🇳 中文](../../zh/ios/flashlight.md)

> [!TIP]
> **Zu wenig Zeit? Wir richten deine App für dich ein.** Unser Team konfiguriert, erstellt & reicht deine WebViewGold-App ein – schlüsselfertig, mit schneller Bearbeitung, Made in Germany. [App einrichten lassen →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **Im Browser erstellen:** Kein Mac, keine IDE: Der **WebViewGold Cloud Builder** konfiguriert, erstellt & lädt deine App online hoch. [Cloud Builder entdecken →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
