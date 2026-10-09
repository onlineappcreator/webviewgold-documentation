---
title: "Drucker-API – WebViewGold für iOS Dokumentation"
description: "Drucke Bilder und PDFs aus deiner Web-App per AirPrint: Sende Dateien mit einem einzigen Link an den nativen iOS-Druckdialog."
lang: "de"
product: "WebViewGold für iOS"
platform: "iOS"
category: "APIs & Funktionen"
slug: "printer"
canonical_url: "https://www.webviewgold.com/de/docs/iOS/printer/"
keywords:
  - "Drucker-API"
  - "WebViewGold für iOS"
  - "Website in App umwandeln"
  - "WebView-App-Dokumentation"
  - "iOS WebView SDK"
  - "PWA zu App"
  - "HTML zu App"
  - "JavaScript-Bridge"
last_updated: "2026-10-09"
---

# Drucker-API – WebViewGold für iOS

> **Zusammenfassung:** Drucke Bilder und PDFs aus deiner Web-App per AirPrint: Sende Dateien mit einem einzigen Link an den nativen iOS-Druckdialog.

[Dokumentation](../README.md) › [WebViewGold für iOS](README.md) › Drucker-API

**Plattform:** iOS · **Kategorie:** APIs & Funktionen · **Online-Version:** [www.webviewgold.com/de/docs/iOS/printer/](https://www.webviewgold.com/de/docs/iOS/printer/)

---

Die **Drucker-API** übergibt eine entfernte Datei (Bild oder PDF) an den nativen iOS-Druckdialog (**AirPrint**), sodass der Nutzer sie auf jedem konfigurierten Drucker ausdrucken oder als PDF speichern kann.

## Verwendung

```html
<a href="printitem://?jobName=Rechnung%20%23123&printItem=https://example.com/invoice.pdf">
  Rechnung drucken
</a>
```

## Query-Parameter

| Name | Erforderlich | Beschreibung |
| --- | --- | --- |
| `printItem` | ja | Vollständige URL der zu druckenden Datei (PDF, JPG, PNG, WebP…). |
| `jobName` | nein | Gut lesbarer Auftragsname, der im Druckdialog angezeigt wird. |

## So funktioniert es

1. Die App lädt die Datei von `printItem` in einen temporären Cache herunter.
2. Die Datei wird an den nativen `UIPrintInteractionController` übergeben, der den iOS-Druckdialog anzeigt.
3. Der Nutzer wählt einen AirPrint-Drucker (oder **Als PDF sichern** über die Teilen-Optionen) und bestätigt.

**Hinweise:** Die Zieldatei muss vom Gerät aus öffentlich erreichbar sein (die URL muss auflösbar sein). Kodiere Sonderzeichen im `jobName`-Parameter als URL (z. B. `%20` für Leerzeichen).

---

## Weiterlesen

- ← Vorherige: [Datei-Downloader-API](file-downloader.md)
- Weiter →: [iCal-Kalender-API](ical-calendar.md)
- Dieselbe Funktion auf anderen Plattformen: [Android – Printer API](../android/printer.md)
- Sprachen: [🇺🇸 English](../../ios/printer.md) · **🇩🇪 Deutsch** · [🇫🇷 Français](../../fr/ios/printer.md) · [🇪🇸 Español](../../es/ios/printer.md) · [🇨🇳 中文](../../zh/ios/printer.md)

> [!TIP]
> **Zu wenig Zeit? Wir richten deine App für dich ein.** Unser Team konfiguriert, erstellt & reicht deine WebViewGold-App ein – schlüsselfertig, mit schneller Bearbeitung, Made in Germany. [App einrichten lassen →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **Im Browser erstellen:** Kein Mac, keine IDE: Der **WebViewGold Cloud Builder** konfiguriert, erstellt & lädt deine App online hoch. [Cloud Builder entdecken →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
