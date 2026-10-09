---
title: "In-App-Rating-Dialog-API – WebViewGold für iOS Dokumentation"
description: "Bitte Nutzer im perfekten Moment um eine App-Store-Bewertung — löse den nativen iOS-Bewertungsdialog aus deiner Web-App aus."
lang: "de"
product: "WebViewGold für iOS"
platform: "iOS"
category: "APIs & Funktionen"
slug: "in-app-rating"
canonical_url: "https://www.webviewgold.com/de/docs/iOS/in-app-rating/"
keywords:
  - "In-App-Rating-Dialog-API"
  - "WebViewGold für iOS"
  - "Website in App umwandeln"
  - "WebView-App-Dokumentation"
  - "iOS WebView SDK"
  - "PWA zu App"
  - "HTML zu App"
  - "JavaScript-Bridge"
last_updated: "2026-10-09"
---

# In-App-Rating-Dialog-API – WebViewGold für iOS

> **Zusammenfassung:** Bitte Nutzer im perfekten Moment um eine App-Store-Bewertung — löse den nativen iOS-Bewertungsdialog aus deiner Web-App aus.

[Dokumentation](../README.md) › [WebViewGold für iOS](README.md) › In-App-Rating-Dialog-API

**Plattform:** iOS · **Kategorie:** APIs & Funktionen · **Online-Version:** [www.webviewgold.com/de/docs/iOS/in-app-rating/](https://www.webviewgold.com/de/docs/iOS/in-app-rating/)

---

Positive App-Store-Bewertungen sind einer der stärksten Wachstumstreiber für deine App. Mit der **In-App-Rating-Dialog-API** von WebViewGold bittest du deine Nutzer genau im richtigen Moment um eine Bewertung — zum Beispiel direkt nach einem erfolgreichen Kauf oder nachdem sie eine Aufgabe in deiner Web-App abgeschlossen haben.

## Option 1: Nativer iOS-Bewertungsdialog (Standard)

Rufe die folgende URL über einen HTML-Link oder per JavaScript auf, um den nativen **SKStoreReviewController**-Bewertungsdialog anzuzeigen:

```html
<a href="rateapp://">Gefällt dir die App? Bewerte uns!</a>
```

```javascript
window.location.href = "rateapp://";
```

**Hinweis:** Apple begrenzt, wie oft der native Bewertungsdialog angezeigt werden darf (etwa dreimal pro Jahr und Nutzer). Er erscheint daher möglicherweise nicht bei jedem Aufruf — das ist beabsichtigt und gilt auch während der Entwicklung.

## Option 2: Eigener Bewertungsdialog

Wenn du einen Dialog bevorzugst, der immer erscheint und den Nutzer stattdessen zu deiner App-Store-Seite führt, konfiguriere ihn in **Config.swift**:

- `showcustomrateappdialog` — auf `true` setzen, um beim Auslösen von `rateapp://` einen eigenen Bewertungsdialog anzuzeigen, anstatt den nativen Review-Aufruf zu versuchen.
- `ratemyappurl` — die App-Store-URL deiner App, z. B. `https://apps.apple.com/app/idXXXXXXXXX?action=write-review`.

## Typische Anwendungsfälle

- Bitte direkt nach einer positiven Interaktion um eine Bewertung (abgeschlossene Bestellung, Level-Aufstieg, erfolgreiche Buchung).
- Zeige zunächst deinen eigenen „Gefällt dir die App?“-Flow auf deiner Website und leite nur zufriedene Nutzer zu `rateapp://` weiter.

---

## Weiterlesen

- ← Vorherige: [App-Teilen-Dialog-API](app-sharing-dialog.md)
- Weiter →: [In-App-Käufe-API](in-app-purchases.md)
- Dieselbe Funktion auf anderen Plattformen: [Android – In-App-Rating-API](../android/in-app-rating.md)
- Sprachen: [🇺🇸 English](../../ios/in-app-rating.md) · **🇩🇪 Deutsch** · [🇫🇷 Français](../../fr/ios/in-app-rating.md) · [🇪🇸 Español](../../es/ios/in-app-rating.md) · [🇨🇳 中文](../../zh/ios/in-app-rating.md)

> [!TIP]
> **Zu wenig Zeit? Wir richten deine App für dich ein.** Unser Team konfiguriert, erstellt & reicht deine WebViewGold-App ein – schlüsselfertig, mit schneller Bearbeitung, Made in Germany. [App einrichten lassen →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **Im Browser erstellen:** Kein Mac, keine IDE: Der **WebViewGold Cloud Builder** konfiguriert, erstellt & lädt deine App online hoch. [Cloud Builder entdecken →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
