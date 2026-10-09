---
title: "QR-Code-Scanner-API – WebViewGold für Android Dokumentation"
description: "Öffne einen nativen QR-Code-Scanner aus deiner Web-App und verarbeite die Scan-Ergebnisse per URL oder JavaScript."
lang: "de"
product: "WebViewGold für Android"
platform: "Android"
category: "APIs & Funktionen"
slug: "qr-code-scanner"
canonical_url: "https://www.webviewgold.com/de/docs/android/qr-code-scanner/"
keywords:
  - "QR-Code-Scanner-API"
  - "WebViewGold für Android"
  - "Website in App umwandeln"
  - "WebView-App-Dokumentation"
  - "Android WebView SDK"
  - "PWA zu App"
  - "HTML zu App"
  - "JavaScript-Bridge"
last_updated: "2026-10-09"
---

# QR-Code-Scanner-API – WebViewGold für Android

> **Zusammenfassung:** Öffne einen nativen QR-Code-Scanner aus deiner Web-App und verarbeite die Scan-Ergebnisse per URL oder JavaScript.

[Dokumentation](../README.md) › [WebViewGold für Android](README.md) › QR-Code-Scanner-API

**Plattform:** Android · **Kategorie:** APIs & Funktionen · **Online-Version:** [www.webviewgold.com/de/docs/android/qr-code-scanner/](https://www.webviewgold.com/de/docs/android/qr-code-scanner/)

---

Um den QR-Code-Scanner in deiner WebView-basierten Android-App auszulösen, verwende das folgende HTML-Link-Format:

```html
<a href="qrcode://">Scan QR Code</a>
```

Ein Klick auf diesen Link öffnet die Kamera des Geräts, um einen QR-Code zu scannen, und jede im QR-Code codierte URL wird automatisch innerhalb der WebView geladen.

## Anwendungsfälle

- Verbindung von Print- und digitalen Inhalten (z. B. Scannen eines QR-Codes aus einem Magazin, um eine Webseite zu öffnen).
- Schneller Zugriff auf Aktionen, Produktinformationen oder Veranstaltungen.
- Sichere Weiterleitung von Nutzern zu internen App-Ressourcen oder bestimmten Landingpages.

---

## Weiterlesen

- ← Vorherige: [IAP History API](iap-history.md)
- Weiter →: [Scan-Modus-API](scanning-mode.md)
- Dieselbe Funktion auf anderen Plattformen: [iOS – QR-Code-Scanner-API](../ios/qr-code-scanner.md)
- Sprachen: [🇺🇸 English](../../android/qr-code-scanner.md) · **🇩🇪 Deutsch** · [🇫🇷 Français](../../fr/android/qr-code-scanner.md) · [🇪🇸 Español](../../es/android/qr-code-scanner.md) · [🇨🇳 中文](../../zh/android/qr-code-scanner.md)

> [!TIP]
> **Zu wenig Zeit? Wir richten deine App für dich ein.** Unser Team konfiguriert, erstellt & reicht deine WebViewGold-App ein – schlüsselfertig, mit schneller Bearbeitung, Made in Germany. [App einrichten lassen →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_android_doc_online)
>
> **Im Browser erstellen:** Kein Mac, keine IDE: Der **WebViewGold Cloud Builder** konfiguriert, erstellt & lädt deine App online hoch. [Cloud Builder entdecken →](https://www.webviewgold.com/cloud-builder?ref=android_docs)
