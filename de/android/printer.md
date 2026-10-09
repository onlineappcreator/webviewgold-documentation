---
title: "Printer API – WebViewGold für Android Dokumentation"
description: "Send a remote image or PDF to the Android system print dialog — Wi-Fi printers, cloud print, or Save-as-PDF, straight from your web app."
lang: "de"
product: "WebViewGold für Android"
platform: "Android"
category: "APIs & Funktionen"
slug: "printer"
canonical_url: "https://www.webviewgold.com/de/docs/android/printer/"
keywords:
  - "Printer API"
  - "WebViewGold für Android"
  - "Website in App umwandeln"
  - "WebView-App-Dokumentation"
  - "Android WebView SDK"
  - "PWA zu App"
  - "HTML zu App"
  - "JavaScript-Bridge"
last_updated: "2026-10-09"
---

# Printer API – WebViewGold für Android

> **Zusammenfassung:** Send a remote image or PDF to the Android system print dialog — Wi-Fi printers, cloud print, or Save-as-PDF, straight from your web app.

[Dokumentation](../README.md) › [WebViewGold für Android](README.md) › Printer API

**Plattform:** Android · **Kategorie:** APIs & Funktionen · **Online-Version:** [www.webviewgold.com/de/docs/android/printer/](https://www.webviewgold.com/de/docs/android/printer/)

---

Die **Printer-API** sendet eine Remote-Datei (Bild oder PDF) an den Android-System-Druckdialog, sodass der Nutzer sie auf jedem konfigurierten Drucker ausgeben kann – WLAN, Cloud-Print oder „Als PDF speichern".

## So verwendest du die Funktion

```html
<a href="printitem://?jobName=Invoice%20%23123&printItem=https://example.com/invoice.pdf">
  Print invoice
</a>
```

## Query-Parameter

| Name | Pflicht | Beschreibung |
| --- | --- | --- |
| `printItem` | ja | Vollständige URL der zu druckenden Datei (PDF, JPG, PNG, WebP…). |
| `jobName` | nein | Anzeigename des Druckauftrags im Druckdialog. Standard: `Print Job`. |

## Wie es funktioniert

1. Die App lädt die Datei von `printItem` in einen temporären Cache.
2. Bei einem Bild wird über `PrintHelper` gedruckt (skaliert auf Passung).
3. Bei einem PDF (oder anderem Dokumentformat) wird über den Android `PrintManager` mit passendem Document-Adapter gedruckt.
4. Die temporäre Datei wird nach Absetzen des Jobs gelöscht.

**Hinweise:** Die Ziel-URL muss vom Gerät aus öffentlich erreichbar sein. Nutzer können im Druckdialog **Als PDF speichern** wählen, um eine Kopie zu exportieren.

---

## Weiterlesen

- ← Vorherige: [Document Scanner](document-scanner.md)
- Weiter →: [Health Connect API](health-connect.md)
- Dieselbe Funktion auf anderen Plattformen: [iOS – Drucker-API](../ios/printer.md)
- Sprachen: [🇺🇸 English](../../android/printer.md) · **🇩🇪 Deutsch** · [🇫🇷 Français](../../fr/android/printer.md) · [🇪🇸 Español](../../es/android/printer.md) · [🇨🇳 中文](../../zh/android/printer.md)

> [!TIP]
> **Zu wenig Zeit? Wir richten deine App für dich ein.** Unser Team konfiguriert, erstellt & reicht deine WebViewGold-App ein – schlüsselfertig, mit schneller Bearbeitung, Made in Germany. [App einrichten lassen →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_android_doc_online)
>
> **Im Browser erstellen:** Kein Mac, keine IDE: Der **WebViewGold Cloud Builder** konfiguriert, erstellt & lädt deine App online hoch. [Cloud Builder entdecken →](https://www.webviewgold.com/cloud-builder?ref=android_docs)
