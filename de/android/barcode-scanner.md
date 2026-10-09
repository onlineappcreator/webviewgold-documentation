---
title: "Barcode-Scanner-API – WebViewGold für Android Dokumentation"
description: "Scanne EAN-, UPC- und andere Barcodes nativ in deiner Android-WebView-App und übergib die Ergebnisse an deine Web-App."
lang: "de"
product: "WebViewGold für Android"
platform: "Android"
category: "APIs & Funktionen"
slug: "barcode-scanner"
canonical_url: "https://www.webviewgold.com/de/docs/android/barcode-scanner/"
keywords:
  - "Barcode-Scanner-API"
  - "WebViewGold für Android"
  - "Website in App umwandeln"
  - "WebView-App-Dokumentation"
  - "Android WebView SDK"
  - "PWA zu App"
  - "HTML zu App"
  - "JavaScript-Bridge"
last_updated: "2026-10-09"
---

# Barcode-Scanner-API – WebViewGold für Android

> **Zusammenfassung:** Scanne EAN-, UPC- und andere Barcodes nativ in deiner Android-WebView-App und übergib die Ergebnisse an deine Web-App.

[Dokumentation](../README.md) › [WebViewGold für Android](README.md) › Barcode-Scanner-API

**Plattform:** Android · **Kategorie:** APIs & Funktionen · **Online-Version:** [www.webviewgold.com/de/docs/android/barcode-scanner/](https://www.webviewgold.com/de/docs/android/barcode-scanner/)

---

Die WebViewGold Barcode Scanner API ermöglicht es deiner WebView-basierten App, die Gerätekamera zum Scannen von Barcodes zu aktivieren. Sobald ein Barcode erfolgreich gescannt wurde, wird das Ergebnis automatisch an deine Webinhalte zurückgegeben.

## Anwendungsfälle

- Scannen von Produkt-Barcodes für Inventarsysteme
- Verarbeiten von Tickets oder Zugangscodes in Logistik- oder Event-Apps
- Ermöglichen einer schnellen Datenerfassung aus gedruckten Barcodes

## So löst du den Scanner aus

Verwende das folgende HTML, um den nativen Barcode-Scanner zu starten:

```html
<a href="barcodescanner://">Start Barcode Scanner</a>
<a href="#" onClick="alert(barcodescanresult);">Show Scan Result</a>
```

- **Barcode-Scanner starten:** Öffnet die Gerätekamera, um unterstützte Barcode-Formate zu erkennen
- **Scan-Ergebnis anzeigen:** Zeigt den gescannten Barcode-Inhalt an, der in der JavaScript-Variablen `barcodescanresult` gespeichert ist

**Technischer Hinweis:** Nach dem Scannen wird der dekodierte Barcode-Wert über die JavaScript-Variable `barcodescanresult` in die aktuelle Seite eingefügt. Du kannst diese Variable verwenden, um Formulare automatisch auszufüllen, benutzerdefinierte Logik auszulösen oder Abfragen auf Basis der gescannten Daten durchzuführen.

**Berechtigungen:** Stelle sicher, dass die App Zugriff auf die Gerätekamera hat, da dieser für das ordnungsgemäße Funktionieren des Barcode-Scans erforderlich ist.

---

## Weiterlesen

- ← Vorherige: [Scan-Modus-API](scanning-mode.md)
- Weiter →: [Screenshot-API](take-screenshot.md)
- Dieselbe Funktion auf anderen Plattformen: [iOS – Barcode-Scanner-API](../ios/barcode-scanner.md)
- Sprachen: [🇺🇸 English](../../android/barcode-scanner.md) · **🇩🇪 Deutsch** · [🇫🇷 Français](../../fr/android/barcode-scanner.md) · [🇪🇸 Español](../../es/android/barcode-scanner.md) · [🇨🇳 中文](../../zh/android/barcode-scanner.md)

> [!TIP]
> **Zu wenig Zeit? Wir richten deine App für dich ein.** Unser Team konfiguriert, erstellt & reicht deine WebViewGold-App ein – schlüsselfertig, mit schneller Bearbeitung, Made in Germany. [App einrichten lassen →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_android_doc_online)
>
> **Im Browser erstellen:** Kein Mac, keine IDE: Der **WebViewGold Cloud Builder** konfiguriert, erstellt & lädt deine App online hoch. [Cloud Builder entdecken →](https://www.webviewgold.com/cloud-builder?ref=android_docs)
