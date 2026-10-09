---
title: "Barcode-Scanner-API – WebViewGold für iOS Dokumentation"
description: "Scanne EAN-, UPC- und andere Barcodes nativ in deiner iOS-WebView-App und übergib die Ergebnisse an deine Web-App."
lang: "de"
product: "WebViewGold für iOS"
platform: "iOS"
category: "APIs & Funktionen"
slug: "barcode-scanner"
canonical_url: "https://www.webviewgold.com/de/docs/iOS/barcode-scanner/"
keywords:
  - "Barcode-Scanner-API"
  - "WebViewGold für iOS"
  - "Website in App umwandeln"
  - "WebView-App-Dokumentation"
  - "iOS WebView SDK"
  - "PWA zu App"
  - "HTML zu App"
  - "JavaScript-Bridge"
last_updated: "2026-10-09"
---

# Barcode-Scanner-API – WebViewGold für iOS

> **Zusammenfassung:** Scanne EAN-, UPC- und andere Barcodes nativ in deiner iOS-WebView-App und übergib die Ergebnisse an deine Web-App.

[Dokumentation](../README.md) › [WebViewGold für iOS](README.md) › Barcode-Scanner-API

**Plattform:** iOS · **Kategorie:** APIs & Funktionen · **Online-Version:** [www.webviewgold.com/de/docs/iOS/barcode-scanner/](https://www.webviewgold.com/de/docs/iOS/barcode-scanner/)

---

Die Barcode-Scanner-API von WebViewGold ermöglicht es deiner WebView-basierten App, die Kamera des Geräts zum Scannen von Barcodes zu aktivieren. Sobald ein Barcode erfolgreich gescannt wurde, wird das Ergebnis automatisch an deinen Web-Content zurückgegeben.

## Anwendungsfälle

- Scannen von Produkt-Barcodes für Bestandsführungssysteme
- Verarbeiten von Tickets oder Zugangscodes in Logistik- oder Event-Apps
- Schnelle Datenerfassung anhand gedruckter Barcodes

## So löst du den Scanner aus

Verwende das folgende HTML, um den nativen Barcode-Scanner zu starten:

```html
<a href="barcodescanner://">Start Barcode Scanner</a>
<a href="#" onClick="alert(barcodescanresult);">Show Scan Result</a>
```

- **Barcode-Scanner starten:** Öffnet die Kamera des Geräts, um unterstützte Barcode-Formate zu erkennen
- **Scan-Ergebnis anzeigen:** Zeigt den gescannten Barcode-Inhalt an, der in der JavaScript-Variable `barcodescanresult` gespeichert ist

**Technischer Hinweis:** Nach dem Scannen wird der dekodierte Barcode-Wert über die JavaScript-Variable `barcodescanresult` in die aktuelle Seite injiziert. Du kannst diese Variable nutzen, um Formulare automatisch auszufüllen, benutzerdefinierte Logik auszulösen oder Lookups auf Basis der gescannten Daten durchzuführen.

**Berechtigungen:** Stelle sicher, dass die App Zugriff auf die Kamera des Geräts hat, da dieser für das Barcode-Scanning erforderlich ist.

---

## Weiterlesen

- ← Vorherige: [QR-Code-Scanner-API](qr-code-scanner.md)
- Weiter →: [Scan-Modus-API](scanning-mode.md)
- Dieselbe Funktion auf anderen Plattformen: [Android – Barcode-Scanner-API](../android/barcode-scanner.md)
- Sprachen: [🇺🇸 English](../../ios/barcode-scanner.md) · **🇩🇪 Deutsch** · [🇫🇷 Français](../../fr/ios/barcode-scanner.md) · [🇪🇸 Español](../../es/ios/barcode-scanner.md) · [🇨🇳 中文](../../zh/ios/barcode-scanner.md)

> [!TIP]
> **Zu wenig Zeit? Wir richten deine App für dich ein.** Unser Team konfiguriert, erstellt & reicht deine WebViewGold-App ein – schlüsselfertig, mit schneller Bearbeitung, Made in Germany. [App einrichten lassen →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **Im Browser erstellen:** Kein Mac, keine IDE: Der **WebViewGold Cloud Builder** konfiguriert, erstellt & lädt deine App online hoch. [Cloud Builder entdecken →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
