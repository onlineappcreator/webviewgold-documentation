---
title: "Biometric Authentication API – WebViewGold für Android Dokumentation"
description: "Prompt fingerprint or face authentication with the native Android BiometricPrompt directly from your web app."
lang: "de"
product: "WebViewGold für Android"
platform: "Android"
category: "APIs & Funktionen"
slug: "biometric-auth"
canonical_url: "https://www.webviewgold.com/de/docs/android/biometric-auth/"
keywords:
  - "Biometric Auth API"
  - "WebViewGold für Android"
  - "Website in App umwandeln"
  - "WebView-App-Dokumentation"
  - "Android WebView SDK"
  - "PWA zu App"
  - "HTML zu App"
  - "JavaScript-Bridge"
last_updated: "2026-10-09"
---

# Biometric Authentication API – WebViewGold für Android

> **Zusammenfassung:** Prompt fingerprint or face authentication with the native Android BiometricPrompt directly from your web app.

[Dokumentation](../README.md) › [WebViewGold für Android](README.md) › Biometric Auth API

**Plattform:** Android · **Kategorie:** APIs & Funktionen · **Online-Version:** [www.webviewgold.com/de/docs/android/biometric-auth/](https://www.webviewgold.com/de/docs/android/biometric-auth/)

---

Die **Biometric-Authentication-API** fordert eine Authentifizierung per Fingerabdruck oder Gesicht über den nativen `BiometricPrompt` des Geräts an. Ist das OS entsprechend konfiguriert, wird auf die Geräte-PIN oder das Muster zurückgegriffen.

## So verwendest du die Funktion

Löse den System-Dialog über einen HTML-Link oder aus JavaScript aus:

```html
<a href="bioauth://">Unlock</a>
```

```javascript
window.location.href = "bioauth://";
```

## Typische Anwendungsfälle

- Zugang zu einer „Wallet"-, „Einstellungen"- oder „Bestellungen"-Seite in deiner Web-App schützen.
- Erneute Authentifizierung vor einem sensiblen Checkout-Schritt erzwingen.

## Verhalten

- Der System-Dialog wird von der App gezeichnet – deine Web-App muss keine UI rendern.
- Nach erfolgreicher Authentifizierung läuft die App normal weiter, sodass deine Web-App reagieren kann (z. B. zur geschützten Seite navigieren).
- Auf Geräten ohne Biometrie kann das OS stattdessen einen PIN-Dialog anzeigen.

## Zugehörige Config

`enableBioMetricAuth` in **Config.java** aktiviert den eingebauten **App-Lock**-Flow, der bei jedem App-Start eine biometrische Auth verlangt. `bioauth://` ist davon unabhängig und kann jederzeit aus JavaScript ausgelöst werden.

---

## Weiterlesen

- ← Vorherige: [Read/Write Value API](read-write-value.md)
- Weiter →: [Document Scanner](document-scanner.md)
- Dieselbe Funktion auf anderen Plattformen: [iOS – Biometrische-Auth-API](../ios/biometric-authentication.md)
- Sprachen: [🇺🇸 English](../../android/biometric-auth.md) · **🇩🇪 Deutsch** · [🇫🇷 Français](../../fr/android/biometric-auth.md) · [🇪🇸 Español](../../es/android/biometric-auth.md) · [🇨🇳 中文](../../zh/android/biometric-auth.md)

> [!TIP]
> **Zu wenig Zeit? Wir richten deine App für dich ein.** Unser Team konfiguriert, erstellt & reicht deine WebViewGold-App ein – schlüsselfertig, mit schneller Bearbeitung, Made in Germany. [App einrichten lassen →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_android_doc_online)
>
> **Im Browser erstellen:** Kein Mac, keine IDE: Der **WebViewGold Cloud Builder** konfiguriert, erstellt & lädt deine App online hoch. [Cloud Builder entdecken →](https://www.webviewgold.com/cloud-builder?ref=android_docs)
