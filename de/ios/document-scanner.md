---
title: "VisionKit-Dokumentenscanner – WebViewGold für iOS Dokumentation"
description: "Lass Nutzer Papierdokumente mit der Kamera scannen und über den Datei-Upload deiner Web-App hochladen — auf Basis von Apple VisionKit."
lang: "de"
product: "WebViewGold für iOS"
platform: "iOS"
category: "APIs & Funktionen"
slug: "document-scanner"
canonical_url: "https://www.webviewgold.com/de/docs/iOS/document-scanner/"
keywords:
  - "Dokumentenscanner"
  - "WebViewGold für iOS"
  - "Website in App umwandeln"
  - "WebView-App-Dokumentation"
  - "iOS WebView SDK"
  - "PWA zu App"
  - "HTML zu App"
  - "JavaScript-Bridge"
last_updated: "2026-10-09"
---

# VisionKit-Dokumentenscanner – WebViewGold für iOS

> **Zusammenfassung:** Lass Nutzer Papierdokumente mit der Kamera scannen und über den Datei-Upload deiner Web-App hochladen — auf Basis von Apple VisionKit.

[Dokumentation](../README.md) › [WebViewGold für iOS](README.md) › Dokumentenscanner

**Plattform:** iOS · **Kategorie:** APIs & Funktionen · **Online-Version:** [www.webviewgold.com/de/docs/iOS/document-scanner/](https://www.webviewgold.com/de/docs/iOS/document-scanner/)

---

Das **Dokumentenscanner**-Feature ergänzt den Standard-Dateiupload-Dialog deiner App um die Option **Dokument scannen**. Der Nutzer kann eine oder mehrere Seiten mit der Kamera scannen; die App erzeugt einen Dokumentenscan und lädt ihn über den standardmäßigen `<input type="file">`-Flow deiner Web-App hoch. Es basiert auf Apples **VisionKit**-Framework (`VNDocumentCameraViewController`) — mit automatischer Kantenerkennung, Zuschnitt und Optimierung.

## Aktivierung

Schalte das Feature in **Config.swift** ein:

```swift
var kVisionKitEnable = true
```

Setze die Option auf `false`, um den Eintrag **Dokument scannen** auszublenden.

## Nutzererlebnis

1. Auf deiner Webseite tippt der Nutzer auf ein `<input type="file">`.
2. Die App zeigt einen Upload-Dialog mit Einträgen wie *Dokument scannen*, *Kamera* und *Fotomediathek*.
3. Ein Tipp auf **Dokument scannen** startet den VisionKit-Scanner: Er erkennt Kanten, schneidet zu, optimiert jede Seite und erlaubt das Hinzufügen weiterer Seiten.
4. Der fertige Scan wird in das `<input type="file">` zurückgegeben — deine Web-App erhält ihn genau wie jede andere hochgeladene Datei.

**Hinweise:** Erfordert iOS 18.4 oder höher und ein Gerät, das die VisionKit-Dokumentenkamera unterstützt. Auf nicht unterstützten Geräten wird der Eintrag **Dokument scannen** automatisch ausgeblendet.

---

## Weiterlesen

- ← Vorherige: [Scan-Modus-API](scanning-mode.md)
- Weiter →: [Screenshot-erstellen-API](take-screenshot.md)
- Dieselbe Funktion auf anderen Plattformen: [Android – Document Scanner](../android/document-scanner.md)
- Sprachen: [🇺🇸 English](../../ios/document-scanner.md) · **🇩🇪 Deutsch** · [🇫🇷 Français](../../fr/ios/document-scanner.md) · [🇪🇸 Español](../../es/ios/document-scanner.md) · [🇨🇳 中文](../../zh/ios/document-scanner.md)

> [!TIP]
> **Zu wenig Zeit? Wir richten deine App für dich ein.** Unser Team konfiguriert, erstellt & reicht deine WebViewGold-App ein – schlüsselfertig, mit schneller Bearbeitung, Made in Germany. [App einrichten lassen →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **Im Browser erstellen:** Kein Mac, keine IDE: Der **WebViewGold Cloud Builder** konfiguriert, erstellt & lädt deine App online hoch. [Cloud Builder entdecken →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
