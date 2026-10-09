---
title: "Scan-Modus-API – WebViewGold für iOS Dokumentation"
description: "Optimiere das Kamera-Scan-Verhalten des QR- und Barcode-Scanners in WebViewGold für iOS."
lang: "de"
product: "WebViewGold für iOS"
platform: "iOS"
category: "APIs & Funktionen"
slug: "scanning-mode"
canonical_url: "https://www.webviewgold.com/de/docs/iOS/scanning-mode/"
keywords:
  - "Scan-Modus-API"
  - "WebViewGold für iOS"
  - "Website in App umwandeln"
  - "WebView-App-Dokumentation"
  - "iOS WebView SDK"
  - "PWA zu App"
  - "HTML zu App"
  - "JavaScript-Bridge"
last_updated: "2026-10-09"
---

# Scan-Modus-API – WebViewGold für iOS

> **Zusammenfassung:** Optimiere das Kamera-Scan-Verhalten des QR- und Barcode-Scanners in WebViewGold für iOS.

[Dokumentation](../README.md) › [WebViewGold für iOS](README.md) › Scan-Modus-API

**Plattform:** iOS · **Kategorie:** APIs & Funktionen · **Online-Version:** [www.webviewgold.com/de/docs/iOS/scanning-mode/](https://www.webviewgold.com/de/docs/iOS/scanning-mode/)

---

Wenn deine Web-App Informationen zum Scannen auf dem Bildschirm darstellt (zum Beispiel einen QR-Code), kann es hilfreich sein, die Bildschirmhelligkeit auf 100 % zu erhöhen und das Einschlafen des Bildschirms zu verhindern. WebViewGold bietet die Scanning-Mode-API, um diese optimalen Scan-Bedingungen dynamisch zu aktivieren.\
Diese API umfasst 3 Befehle:

- "auto" = schaltet den Scan-Modus ein und deaktiviert ihn automatisch bei einer Seitenweiterleitung.
- "on" = schaltet den Scan-Modus ein, bleibt auch nach Seitenweiterleitungen aktiv.
- "off" = schaltet den Scan-Modus aus.

Verlinke auf diese Art von URLs, um die Scanning-Mode-API zu nutzen:

```html
<a href="scanningmode://auto">Enable Scanning Mode; will automatically disable on page redirect</a>
<a href="scanningmode://on">Enable Scanning Mode; will persist until manually disabled</a>
<a href="scanningmode://off">Disable Scanning Mode</a>
```

---

## Weiterlesen

- ← Vorherige: [Barcode-Scanner-API](barcode-scanner.md)
- Weiter →: [Dokumentenscanner](document-scanner.md)
- Dieselbe Funktion auf anderen Plattformen: [Android – Scan-Modus-API](../android/scanning-mode.md)
- Sprachen: [🇺🇸 English](../../ios/scanning-mode.md) · **🇩🇪 Deutsch** · [🇫🇷 Français](../../fr/ios/scanning-mode.md) · [🇪🇸 Español](../../es/ios/scanning-mode.md) · [🇨🇳 中文](../../zh/ios/scanning-mode.md)

> [!TIP]
> **Zu wenig Zeit? Wir richten deine App für dich ein.** Unser Team konfiguriert, erstellt & reicht deine WebViewGold-App ein – schlüsselfertig, mit schneller Bearbeitung, Made in Germany. [App einrichten lassen →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **Im Browser erstellen:** Kein Mac, keine IDE: Der **WebViewGold Cloud Builder** konfiguriert, erstellt & lädt deine App online hoch. [Cloud Builder entdecken →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
