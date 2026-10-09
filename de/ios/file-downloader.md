---
title: "Datei-Downloader-API – WebViewGold für iOS Dokumentation"
description: "Lass Nutzer Bilder, PDFs und andere Dateien aus deiner Web-App direkt auf ihr iPhone oder iPad herunterladen."
lang: "de"
product: "WebViewGold für iOS"
platform: "iOS"
category: "APIs & Funktionen"
slug: "file-downloader"
canonical_url: "https://www.webviewgold.com/de/docs/iOS/file-downloader/"
keywords:
  - "Datei-Downloader-API"
  - "WebViewGold für iOS"
  - "Website in App umwandeln"
  - "WebView-App-Dokumentation"
  - "iOS WebView SDK"
  - "PWA zu App"
  - "HTML zu App"
  - "JavaScript-Bridge"
last_updated: "2026-10-09"
---

# Datei-Downloader-API – WebViewGold für iOS

> **Zusammenfassung:** Lass Nutzer Bilder, PDFs und andere Dateien aus deiner Web-App direkt auf ihr iPhone oder iPad herunterladen.

[Dokumentation](../README.md) › [WebViewGold für iOS](README.md) › Datei-Downloader-API

**Plattform:** iOS · **Kategorie:** APIs & Funktionen · **Online-Version:** [www.webviewgold.com/de/docs/iOS/file-downloader/](https://www.webviewgold.com/de/docs/iOS/file-downloader/)

---

Mit der Download-API von WebViewGold kannst du Dokument-, Bild- und Audio-Datei-Downloads in deiner WebView-App bereitstellen. Die folgenden Schritte zeigen, wie du die Downloader-Funktionalität aktivierst und anpasst:

## 1. Bilder herunterladen

Speichere Bilder in der Fotomediathek des Nutzers, indem du Links mit dem Präfix savethisimage://?url= aufrufst:

```html
<a href="savethisimage://?url=IMAGE URL HERE">Download Image</a>
```

## 2. Dateien herunterladen

Speichere Dateien, indem du Links mit einer entsprechenden Endung (z. B. .mp3) aufrufst:

```html
<a href="https://www.example.org/file.pdf">Link PDF</a>
<a href="https://www.example.org/file.mp3">Link mp3 Music</a>
<a href="https://www.example.org/file.mp4">Link mp4 Music</a>
<a href="https://www.example.org/file.wav">Link wav Music</a>
<a href="https://www.example.org/file.epub">Link epub eBook</a>
<a href="https://www.example.org/file.pkpass">Link Passbook / Apple Wallet</a>
<a href="https://www.example.org/file.docx">Link Word</a>
<a href="https://www.example.org/file.pptx">Link PowerPoint</a>
<a href="https://www.example.org/file.xlsx">Link Excel</a>
```

## 3. Unterstützte Dateitypen anpassen

Du kannst weitere Dateitypen hinzufügen, die die Datei-Downloader-Funktion auslösen sollen (z. B. .epub, .zip, ...). Dies erfolgt über die Listenvariable `extentionARY`, die du in der Datei **Config.swift** findest.

## 4. Automatische Datei-Downloads aktivieren

Ziehe in Betracht, die Option `autodownloader` in **Config.swift** zu setzen, um automatische Downloads für Dateien zu aktivieren, die mit Content-Disposition-HTTP-Headern gekennzeichnet sind – unabhängig von der Liste `extentionARY`. So wird sichergestellt, dass Dateien basierend auf den Serverkonfigurationen automatisch heruntergeladen werden.

[![Video ansehen: Datei-Downloader-API](https://img.youtube.com/vi/V0LnwnzJx6I/hqdefault.jpg)](https://www.youtube.com/watch?v=V0LnwnzJx6I)

---

## Weiterlesen

- ← Vorherige: [Native-Video-API](native-video.md)
- Weiter →: [Drucker-API](printer.md)
- Dieselbe Funktion auf anderen Plattformen: [Android – Datei-Downloader-API](../android/file-downloader.md)
- Sprachen: [🇺🇸 English](../../ios/file-downloader.md) · **🇩🇪 Deutsch** · [🇫🇷 Français](../../fr/ios/file-downloader.md) · [🇪🇸 Español](../../es/ios/file-downloader.md) · [🇨🇳 中文](../../zh/ios/file-downloader.md)

> [!TIP]
> **Zu wenig Zeit? Wir richten deine App für dich ein.** Unser Team konfiguriert, erstellt & reicht deine WebViewGold-App ein – schlüsselfertig, mit schneller Bearbeitung, Made in Germany. [App einrichten lassen →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **Im Browser erstellen:** Kein Mac, keine IDE: Der **WebViewGold Cloud Builder** konfiguriert, erstellt & lädt deine App online hoch. [Cloud Builder entdecken →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
