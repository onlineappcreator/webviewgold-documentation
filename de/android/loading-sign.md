---
title: "Ladeanzeige-API – WebViewGold für Android Dokumentation"
description: "Blende die native Ladeanzeige bei Bedarf ein oder aus und passe das Ladeerlebnis deiner Android-App an."
lang: "de"
product: "WebViewGold für Android"
platform: "Android"
category: "APIs & Funktionen"
slug: "loading-sign"
canonical_url: "https://www.webviewgold.com/de/docs/android/loading-sign/"
keywords:
  - "Ladeanzeige-API"
  - "WebViewGold für Android"
  - "Website in App umwandeln"
  - "WebView-App-Dokumentation"
  - "Android WebView SDK"
  - "PWA zu App"
  - "HTML zu App"
  - "JavaScript-Bridge"
last_updated: "2026-10-09"
---

# Ladeanzeige-API – WebViewGold für Android

> **Zusammenfassung:** Blende die native Ladeanzeige bei Bedarf ein oder aus und passe das Ladeerlebnis deiner Android-App an.

[Dokumentation](../README.md) › [WebViewGold für Android](README.md) › Ladeanzeige-API

**Plattform:** Android · **Kategorie:** APIs & Funktionen · **Online-Version:** [www.webviewgold.com/de/docs/android/loading-sign/](https://www.webviewgold.com/de/docs/android/loading-sign/)

---

Die native Android-Ladeanzeige von WebViewGold erscheint automatisch, wenn Seiten geladen werden oder ihr Laden abgeschlossen ist. Du kannst die Ladeanzeige jedoch auch manuell für Szenarien außerhalb der Standard-Seitenladeereignisse steuern. Dies ist besonders nützlich für Prozesse, bei denen der Nutzer über einen Ladevorgang informiert werden muss, wie zum Beispiel:

- Warten in einer Live-Chat-Warteschlange
- Ausführung eines Hintergrundprozesses auf einem Cloud-Server
- Visualisierung eines beliebigen anderen längeren Vorgangs zur Information des Nutzers

## Verwendung

Um die Ladeanzeige deiner WebView-App manuell zu steuern, verwende die folgenden Links:

```html
<a href="spinneron://">Show the loading spinner</a>
<a href="spinneroff://">Hide the loading spinner</a>
```

---

## Weiterlesen

- ← Vorherige: [App-Zurücksetzen-API](reset-app.md)
- Weiter →: [Zwischenablage-API](clipboard.md)
- Dieselbe Funktion auf anderen Plattformen: [iOS – Ladeanzeige-API](../ios/loading-sign.md)
- Sprachen: [🇺🇸 English](../../android/loading-sign.md) · **🇩🇪 Deutsch** · [🇫🇷 Français](../../fr/android/loading-sign.md) · [🇪🇸 Español](../../es/android/loading-sign.md) · [🇨🇳 中文](../../zh/android/loading-sign.md)

> [!TIP]
> **Zu wenig Zeit? Wir richten deine App für dich ein.** Unser Team konfiguriert, erstellt & reicht deine WebViewGold-App ein – schlüsselfertig, mit schneller Bearbeitung, Made in Germany. [App einrichten lassen →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_android_doc_online)
>
> **Im Browser erstellen:** Kein Mac, keine IDE: Der **WebViewGold Cloud Builder** konfiguriert, erstellt & lädt deine App online hoch. [Cloud Builder entdecken →](https://www.webviewgold.com/cloud-builder?ref=android_docs)
