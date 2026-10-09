---
title: "QR-Code-Scanner-API – WebViewGold für iOS Dokumentation"
description: "Öffne einen nativen QR-Code-Scanner aus deiner Web-App und verarbeite die Scan-Ergebnisse per URL oder JavaScript."
lang: "de"
product: "WebViewGold für iOS"
platform: "iOS"
category: "APIs & Funktionen"
slug: "qr-code-scanner"
canonical_url: "https://www.webviewgold.com/de/docs/iOS/qr-code-scanner/"
keywords:
  - "QR-Code-Scanner-API"
  - "WebViewGold für iOS"
  - "Website in App umwandeln"
  - "WebView-App-Dokumentation"
  - "iOS WebView SDK"
  - "PWA zu App"
  - "HTML zu App"
  - "JavaScript-Bridge"
last_updated: "2026-10-09"
---

# QR-Code-Scanner-API – WebViewGold für iOS

> **Zusammenfassung:** Öffne einen nativen QR-Code-Scanner aus deiner Web-App und verarbeite die Scan-Ergebnisse per URL oder JavaScript.

[Dokumentation](../README.md) › [WebViewGold für iOS](README.md) › QR-Code-Scanner-API

**Plattform:** iOS · **Kategorie:** APIs & Funktionen · **Online-Version:** [www.webviewgold.com/de/docs/iOS/qr-code-scanner/](https://www.webviewgold.com/de/docs/iOS/qr-code-scanner/)

---

Um den QR-Code-Scanner in deiner WebView-basierten iOS-App auszulösen, verwende das folgende HTML-Link-Format:

```html
<a href="qrcode://">Scan QR Code</a>
```

Ein Klick auf diesen Link öffnet die Kamera des Geräts, um einen QR-Code zu scannen. Jede im QR-Code kodierte URL wird automatisch in der WebView geladen.

## Anwendungsfälle

- Verknüpfung von Print- und Digitalinhalten (z. B. Scannen eines QR-Codes aus einem Magazin, um eine Webseite zu öffnen).
- Schneller Zugriff auf Aktionen, Produktinformationen oder Veranstaltungen.
- Sichere Verlinkung von Nutzern zu internen App-Ressourcen oder bestimmten Landingpages.

---

## Weiterlesen

- ← Vorherige: [IAP-History-API](iap-history.md)
- Weiter →: [Barcode-Scanner-API](barcode-scanner.md)
- Dieselbe Funktion auf anderen Plattformen: [Android – QR-Code-Scanner-API](../android/qr-code-scanner.md)
- Sprachen: [🇺🇸 English](../../ios/qr-code-scanner.md) · **🇩🇪 Deutsch** · [🇫🇷 Français](../../fr/ios/qr-code-scanner.md) · [🇪🇸 Español](../../es/ios/qr-code-scanner.md) · [🇨🇳 中文](../../zh/ios/qr-code-scanner.md)

> [!TIP]
> **Zu wenig Zeit? Wir richten deine App für dich ein.** Unser Team konfiguriert, erstellt & reicht deine WebViewGold-App ein – schlüsselfertig, mit schneller Bearbeitung, Made in Germany. [App einrichten lassen →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **Im Browser erstellen:** Kein Mac, keine IDE: Der **WebViewGold Cloud Builder** konfiguriert, erstellt & lädt deine App online hoch. [Cloud Builder entdecken →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
