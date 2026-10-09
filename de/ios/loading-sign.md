---
title: "Ladeanzeige-API – WebViewGold für iOS Dokumentation"
description: "Blende die native Ladeanzeige bei Bedarf ein oder aus und passe das Ladeerlebnis deiner iOS-App an."
lang: "de"
product: "WebViewGold für iOS"
platform: "iOS"
category: "APIs & Funktionen"
slug: "loading-sign"
canonical_url: "https://www.webviewgold.com/de/docs/iOS/loading-sign/"
keywords:
  - "Ladeanzeige-API"
  - "WebViewGold für iOS"
  - "Website in App umwandeln"
  - "WebView-App-Dokumentation"
  - "iOS WebView SDK"
  - "PWA zu App"
  - "HTML zu App"
  - "JavaScript-Bridge"
last_updated: "2026-10-09"
---

# Ladeanzeige-API – WebViewGold für iOS

> **Zusammenfassung:** Blende die native Ladeanzeige bei Bedarf ein oder aus und passe das Ladeerlebnis deiner iOS-App an.

[Dokumentation](../README.md) › [WebViewGold für iOS](README.md) › Ladeanzeige-API

**Plattform:** iOS · **Kategorie:** APIs & Funktionen · **Online-Version:** [www.webviewgold.com/de/docs/iOS/loading-sign/](https://www.webviewgold.com/de/docs/iOS/loading-sign/)

---

Der native iOS-Ladeindikator von WebViewGold **erscheint automatisch**, wenn Seiten geladen werden oder das Laden abgeschlossen ist. Du kannst den Ladeindikator jedoch auch manuell für Szenarien außerhalb der Standard-Seitenladeereignisse steuern. Dies ist besonders nützlich für Prozesse, bei denen der Nutzer über den Ladevorgang informiert werden soll, wie zum Beispiel:

- Warten in einer Live-Chat-Warteschlange
- Ausführen eines Hintergrundprozesses auf einem Cloud-Server
- Visualisieren eines beliebigen anderen längeren Prozesses zur Information des Nutzers

## Verwendung

Verwende die folgenden Links, um den Ladeindikator in deiner WebView-App manuell zu steuern:

```html
<a href="spinneron://">Show the loading spinner</a>
<a href="spinneroff://">Hide the loading spinner</a>
```

---

## Weiterlesen

- ← Vorherige: [Nutzer-Tracking-Entscheidung-API](user-tracking.md)
- Weiter →: [Pull-to-Refresh-API](pull-to-refresh.md)
- Dieselbe Funktion auf anderen Plattformen: [Android – Ladeanzeige-API](../android/loading-sign.md)
- Sprachen: [🇺🇸 English](../../ios/loading-sign.md) · **🇩🇪 Deutsch** · [🇫🇷 Français](../../fr/ios/loading-sign.md) · [🇪🇸 Español](../../es/ios/loading-sign.md) · [🇨🇳 中文](../../zh/ios/loading-sign.md)

> [!TIP]
> **Zu wenig Zeit? Wir richten deine App für dich ein.** Unser Team konfiguriert, erstellt & reicht deine WebViewGold-App ein – schlüsselfertig, mit schneller Bearbeitung, Made in Germany. [App einrichten lassen →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **Im Browser erstellen:** Kein Mac, keine IDE: Der **WebViewGold Cloud Builder** konfiguriert, erstellt & lädt deine App online hoch. [Cloud Builder entdecken →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
