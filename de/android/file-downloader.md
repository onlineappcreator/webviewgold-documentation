---
title: "Datei-Downloader-API – WebViewGold für Android Dokumentation"
description: "Lass Nutzer Bilder, PDFs und andere Dateien aus deiner Web-App auf ihr Android-Gerät herunterladen."
lang: "de"
product: "WebViewGold für Android"
platform: "Android"
category: "APIs & Funktionen"
slug: "file-downloader"
canonical_url: "https://www.webviewgold.com/de/docs/android/file-downloader/"
keywords:
  - "Datei-Downloader-API"
  - "WebViewGold für Android"
  - "Website in App umwandeln"
  - "WebView-App-Dokumentation"
  - "Android WebView SDK"
  - "PWA zu App"
  - "HTML zu App"
  - "JavaScript-Bridge"
last_updated: "2026-10-09"
---

# Datei-Downloader-API – WebViewGold für Android

> **Zusammenfassung:** Lass Nutzer Bilder, PDFs und andere Dateien aus deiner Web-App auf ihr Android-Gerät herunterladen.

[Dokumentation](../README.md) › [WebViewGold für Android](README.md) › Datei-Downloader-API

**Plattform:** Android · **Kategorie:** APIs & Funktionen · **Online-Version:** [www.webviewgold.com/de/docs/android/file-downloader/](https://www.webviewgold.com/de/docs/android/file-downloader/)

---

Die Download API von WebViewGold ermöglicht es dir, Downloads von Dokument-, Bild- und Audiodateien in deiner WebView-App bereitzustellen. Die folgenden Schritte beschreiben, wie du die Downloader-Funktionalität aktivierst und anpasst:

## 1. Bilder herunterladen

Speichere Bilder in der Fotogalerie des Nutzers, indem du Links mit dem Präfix savethisimage://?url= aufrufst:

```html
<a href="savethisimage://?url=IMAGE URL HERE">Download Image</a>
```

## 2. PDF-Dateien herunterladen

Speichere PDF-Dateien, indem du Links mit der Endung .pdf aufrufst:

```html
<a href="https://www.example.org/file.pdf">Download PDF</a>
```

## 3. Musikdateien herunterladen

Speichere Musikdateien, indem du einfach Links mit der Endung .mp3, .mp4 oder .wav aufrufst:

```html
<a href="https://www.example.org/file.mp3">Download MP3</a>
<a href="https://www.example.org/file.mp4">Download MP4</a>
<a href="https://www.example.org/file.wav">Download WAV</a>
```

## 4. Unterstützte Dateitypen anpassen

Um dem Downloader weitere Dateiformate hinzuzufügen, trage diese in die Liste `downloadableExtension` in **Config.java** ein.

## 5. Automatische Datei-Downloads aktivieren

Erwäge, die Option `AUTO_DOWNLOAD_FILES` in **Config.java** zu setzen, um automatische Downloads für Dateien zu aktivieren, die mit Content-Disposition-HTTP-Headern gekennzeichnet sind, unabhängig von der Liste `downloadableExtension`. Dadurch wird sichergestellt, dass Dateien basierend auf den Serverkonfigurationen automatisch heruntergeladen werden.

---

## Weiterlesen

- ← Vorherige: [Facebook-Ads-API](facebook-ads.md)
- Weiter →: [Natives Video (PiP) API](native-video.md)
- Dieselbe Funktion auf anderen Plattformen: [iOS – Datei-Downloader-API](../ios/file-downloader.md)
- Sprachen: [🇺🇸 English](../../android/file-downloader.md) · **🇩🇪 Deutsch** · [🇫🇷 Français](../../fr/android/file-downloader.md) · [🇪🇸 Español](../../es/android/file-downloader.md) · [🇨🇳 中文](../../zh/android/file-downloader.md)

> [!TIP]
> **Zu wenig Zeit? Wir richten deine App für dich ein.** Unser Team konfiguriert, erstellt & reicht deine WebViewGold-App ein – schlüsselfertig, mit schneller Bearbeitung, Made in Germany. [App einrichten lassen →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_android_doc_online)
>
> **Im Browser erstellen:** Kein Mac, keine IDE: Der **WebViewGold Cloud Builder** konfiguriert, erstellt & lädt deine App online hoch. [Cloud Builder entdecken →](https://www.webviewgold.com/cloud-builder?ref=android_docs)
