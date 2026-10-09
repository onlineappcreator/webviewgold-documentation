---
title: "App-Teilen-Dialog-API – WebViewGold für iOS Dokumentation"
description: "Löse das native iOS-Teilen-Menü aus deiner Web-App aus, damit Nutzer deine App oder eine beliebige URL teilen können."
lang: "de"
product: "WebViewGold für iOS"
platform: "iOS"
category: "APIs & Funktionen"
slug: "app-sharing-dialog"
canonical_url: "https://www.webviewgold.com/de/docs/iOS/app-sharing-dialog/"
keywords:
  - "App-Teilen-Dialog-API"
  - "WebViewGold für iOS"
  - "Website in App umwandeln"
  - "WebView-App-Dokumentation"
  - "iOS WebView SDK"
  - "PWA zu App"
  - "HTML zu App"
  - "JavaScript-Bridge"
last_updated: "2026-10-09"
---

# App-Teilen-Dialog-API – WebViewGold für iOS

> **Zusammenfassung:** Löse das native iOS-Teilen-Menü aus deiner Web-App aus, damit Nutzer deine App oder eine beliebige URL teilen können.

[Dokumentation](../README.md) › [WebViewGold für iOS](README.md) › App-Teilen-Dialog-API

**Plattform:** iOS · **Kategorie:** APIs & Funktionen · **Online-Version:** [www.webviewgold.com/de/docs/iOS/app-sharing-dialog/](https://www.webviewgold.com/de/docs/iOS/app-sharing-dialog/)

---

Die App-Sharing-Dialog-API in WebViewGold ermöglicht es deinen Benutzern, Inhalte aus deiner App – etwa den Download-Link oder individuelle Nachrichten – über ihre bevorzugten Apps (z. B. WhatsApp, SMS, E-Mail) mit Freunden und Familie zu teilen. Dies kann eine wirkungsvolle Methode sein, um die Sichtbarkeit deiner App zu erhöhen und deine Nutzerbasis zu vergrößern.

## So verwendest du den App-Sharing-Dialog in deiner WebView-basierten iOS-App

Du kannst einen nativen Teilen-Dialog über das URL-Schema `shareapp://` mit anpassbaren Nachrichten- und URL-Parametern auslösen.

Nachfolgend findest du Beispiele für die verschiedenen Möglichkeiten, diese Funktion zu implementieren:

```html
<a href="shareapp://message?=Check out this cool thing!&url=https://www.webviewgold.com">Share (message, link)</a>

<a href="shareapp://message?=&url=https://www.webviewgold.com">Share (no message, link)</a>

<a href="shareapp://message?=Check out this cool thing!">Share (message, no link)</a>
```

![Beispiel für den App-Sharing-Dialog](../../assets/ios/img/sharedialog.webp)\
![Beispiel für eine App-Sharing-Nachricht](../../assets/ios/img/sharemessage.webp)

---

## Weiterlesen

- ← Vorherige: [Deep-Linking-API](deep-linking.md)
- Weiter →: [In-App-Rating-Dialog-API](in-app-rating.md)
- Dieselbe Funktion auf anderen Plattformen: [Android – App-Teilen-Dialog-API](../android/app-sharing-dialog.md)
- Sprachen: [🇺🇸 English](../../ios/app-sharing-dialog.md) · **🇩🇪 Deutsch** · [🇫🇷 Français](../../fr/ios/app-sharing-dialog.md) · [🇪🇸 Español](../../es/ios/app-sharing-dialog.md) · [🇨🇳 中文](../../zh/ios/app-sharing-dialog.md)

> [!TIP]
> **Zu wenig Zeit? Wir richten deine App für dich ein.** Unser Team konfiguriert, erstellt & reicht deine WebViewGold-App ein – schlüsselfertig, mit schneller Bearbeitung, Made in Germany. [App einrichten lassen →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **Im Browser erstellen:** Kein Mac, keine IDE: Der **WebViewGold Cloud Builder** konfiguriert, erstellt & lädt deine App online hoch. [Cloud Builder entdecken →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
