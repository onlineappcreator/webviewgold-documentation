---
title: "Taschenlampen-API – WebViewGold für Android Dokumentation"
description: "Steuere die Taschenlampe des Geräts aus deiner Web-App mit einfachen JavaScript-Links in WebViewGold für Android."
lang: "de"
product: "WebViewGold für Android"
platform: "Android"
category: "APIs & Funktionen"
slug: "flashlight"
canonical_url: "https://www.webviewgold.com/de/docs/android/flashlight/"
keywords:
  - "Taschenlampen-API"
  - "WebViewGold für Android"
  - "Website in App umwandeln"
  - "WebView-App-Dokumentation"
  - "Android WebView SDK"
  - "PWA zu App"
  - "HTML zu App"
  - "JavaScript-Bridge"
last_updated: "2026-10-09"
---

# Taschenlampen-API – WebViewGold für Android

> **Zusammenfassung:** Steuere die Taschenlampe des Geräts aus deiner Web-App mit einfachen JavaScript-Links in WebViewGold für Android.

[Dokumentation](../README.md) › [WebViewGold für Android](README.md) › Taschenlampen-API

**Plattform:** Android · **Kategorie:** APIs & Funktionen · **Online-Version:** [www.webviewgold.com/de/docs/android/flashlight/](https://www.webviewgold.com/de/docs/android/flashlight/)

---

Die Flashlight API von WebViewGold ermöglicht es deiner Website, die Taschenlampe (Blitzlicht) des Geräts zu steuern. Diese Funktion kann nützlich sein für:

- Die Entwicklung von Dienstprogramm-Apps, die das Ein-/Ausschalten der Taschenlampe erfordern
- Die Verbesserung der Nutzererfahrung während der App-Nutzung durch Gamification
- Die Bereitstellung zusätzlicher Barrierefreiheitsfunktionen

## So verwendest du die Funktion

Du kannst die Taschenlampe direkt aus deinen HTML-Inhalten heraus mit den folgenden Links ein- oder ausschalten:

```html
<a href="enableflashlight://">Turn On Flashlight</a>
<a href="disableflashlight://">Turn Off Flashlight</a>
```

**Hinweis:** Stelle sicher, dass deine App über die erforderlichen Kameraberechtigungen in der AndroidManifest.xml verfügt, da die Taschenlampen-Funktionalität an die Kamera-Hardware des Geräts gebunden ist.

---

## Weiterlesen

- ← Vorherige: [UUID-API](uuid.md)
- Weiter →: [App Links / Deep Linking](app-links.md)
- Dieselbe Funktion auf anderen Plattformen: [iOS – Taschenlampen-API](../ios/flashlight.md)
- Sprachen: [🇺🇸 English](../../android/flashlight.md) · **🇩🇪 Deutsch** · [🇫🇷 Français](../../fr/android/flashlight.md) · [🇪🇸 Español](../../es/android/flashlight.md) · [🇨🇳 中文](../../zh/android/flashlight.md)

> [!TIP]
> **Zu wenig Zeit? Wir richten deine App für dich ein.** Unser Team konfiguriert, erstellt & reicht deine WebViewGold-App ein – schlüsselfertig, mit schneller Bearbeitung, Made in Germany. [App einrichten lassen →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_android_doc_online)
>
> **Im Browser erstellen:** Kein Mac, keine IDE: Der **WebViewGold Cloud Builder** konfiguriert, erstellt & lädt deine App online hoch. [Cloud Builder entdecken →](https://www.webviewgold.com/cloud-builder?ref=android_docs)
