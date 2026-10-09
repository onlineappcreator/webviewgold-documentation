---
title: "Native-Video-Player-API – WebViewGold für iOS Dokumentation"
description: "Spiele Videostreams im nativen iOS-Videoplayer mit Bild-in-Bild-Unterstützung ab — direkt aus deiner Web-App ausgelöst."
lang: "de"
product: "WebViewGold für iOS"
platform: "iOS"
category: "APIs & Funktionen"
slug: "native-video"
canonical_url: "https://www.webviewgold.com/de/docs/iOS/native-video/"
keywords:
  - "Native-Video-API"
  - "WebViewGold für iOS"
  - "Website in App umwandeln"
  - "WebView-App-Dokumentation"
  - "iOS WebView SDK"
  - "PWA zu App"
  - "HTML zu App"
  - "JavaScript-Bridge"
last_updated: "2026-10-09"
---

# Native-Video-Player-API – WebViewGold für iOS

> **Zusammenfassung:** Spiele Videostreams im nativen iOS-Videoplayer mit Bild-in-Bild-Unterstützung ab — direkt aus deiner Web-App ausgelöst.

[Dokumentation](../README.md) › [WebViewGold für iOS](README.md) › Native-Video-API

**Plattform:** iOS · **Kategorie:** APIs & Funktionen · **Online-Version:** [www.webviewgold.com/de/docs/iOS/native-video/](https://www.webviewgold.com/de/docs/iOS/native-video/)

---

Die **Native-Video-Player-API** ermöglicht es deiner Website, einen Videostream im nativen iOS-Videoplayer mit **Bild-in-Bild-Unterstützung** (Picture-in-Picture) zu starten. Löse die native Wiedergabe aus, indem du einen Link mit dem Präfix `startnativevideo://videostreamurl=` öffnest:

```html
<a href="startnativevideo://videostreamurl=YOUR_VIDEO_STREAM_URL">Video im System-Videoplayer mit PiP-Unterstützung abspielen</a>
```

Der Nutzer kann das Video in einem schwebenden Bild-in-Bild-Fenster weiterschauen, während er in deiner Web-App oder sogar in anderen Apps navigiert.

## Typische Anwendungsfälle

- Livestreams, die weiterlaufen sollen, während der Nutzer deine Web-App durchstöbert.
- Videokurse oder Tutorials mit systemweiten Wiedergabesteuerungen.
- Jedes Video, das von AirPlay, Vollbild und Bild-in-Bild-Unterstützung des nativen Players profitiert.

**Hinweis:** Verwende eine direkte Videostream-URL (z. B. eine .mp4-Datei oder einen HLS-.m3u8-Stream) — nicht die URL einer HTML-Seite, die das Video einbettet.

---

## Weiterlesen

- ← Vorherige: [HTML-Audio-API](html-audio.md)
- Weiter →: [Datei-Downloader-API](file-downloader.md)
- Dieselbe Funktion auf anderen Plattformen: [Android – Natives Video (PiP) API](../android/native-video.md)
- Sprachen: [🇺🇸 English](../../ios/native-video.md) · **🇩🇪 Deutsch** · [🇫🇷 Français](../../fr/ios/native-video.md) · [🇪🇸 Español](../../es/ios/native-video.md) · [🇨🇳 中文](../../zh/ios/native-video.md)

> [!TIP]
> **Zu wenig Zeit? Wir richten deine App für dich ein.** Unser Team konfiguriert, erstellt & reicht deine WebViewGold-App ein – schlüsselfertig, mit schneller Bearbeitung, Made in Germany. [App einrichten lassen →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **Im Browser erstellen:** Kein Mac, keine IDE: Der **WebViewGold Cloud Builder** konfiguriert, erstellt & lädt deine App online hoch. [Cloud Builder entdecken →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
