---
title: "App-Zurücksetzen-API – WebViewGold für iOS Dokumentation"
description: "Setze Cache, Cookies und lokalen Speicher deiner iOS-WebView-App mit einem einzigen Link oder JavaScript-Aufruf zurück."
lang: "de"
product: "WebViewGold für iOS"
platform: "iOS"
category: "APIs & Funktionen"
slug: "reset-app"
canonical_url: "https://www.webviewgold.com/de/docs/iOS/reset-app/"
keywords:
  - "App-Zurücksetzen-API"
  - "WebViewGold für iOS"
  - "Website in App umwandeln"
  - "WebView-App-Dokumentation"
  - "iOS WebView SDK"
  - "PWA zu App"
  - "HTML zu App"
  - "JavaScript-Bridge"
last_updated: "2026-10-09"
---

# App-Zurücksetzen-API – WebViewGold für iOS

> **Zusammenfassung:** Setze Cache, Cookies und lokalen Speicher deiner iOS-WebView-App mit einem einzigen Link oder JavaScript-Aufruf zurück.

[Dokumentation](../README.md) › [WebViewGold für iOS](README.md) › App-Zurücksetzen-API

**Plattform:** iOS · **Kategorie:** APIs & Funktionen · **Online-Version:** [www.webviewgold.com/de/docs/iOS/reset-app/](https://www.webviewgold.com/de/docs/iOS/reset-app/)

---

In bestimmten Fällen kann es notwendig sein, die App auf ihre Ausgangseinstellungen zurückzusetzen (durch Löschen von Cookies und Cache), um die optimale Leistung wiederherzustellen. Die **Reset-App-API** bietet eine unkomplizierte Möglichkeit, diesen Reset einzuleiten.

## Verwendung

Um die App-Daten zurückzusetzen, verwende einfach den folgenden Link in deiner App:

```html
<a href="reset://">Reset App Link</a>
```

Dieser Link wird:

- Alle Cookies löschen
- Zwischengespeicherte Daten löschen

## Test der Reset-Funktionalität

Um diese Funktion zu testen, füge die folgende Demo-URL zu deiner WebViewGold-App hinzu: <https://www.onlineappcreator.com/reset_test.html>

**Hinweis:** Verwende die Reset-Funktionalität mit Bedacht, da Nutzerdaten in Bezug auf Cookies und Cache gelöscht werden. Dies kann gespeicherte Einstellungen oder Sitzungsdaten beeinträchtigen und dazu führen, dass Nutzer aus aktiven Sitzungen abgemeldet werden.

---

## Weiterlesen

- ← Vorherige: [Taschenlampen-API](flashlight.md)
- Weiter →: [Nutzer-Tracking-Entscheidung-API](user-tracking.md)
- Dieselbe Funktion auf anderen Plattformen: [Android – App-Zurücksetzen-API](../android/reset-app.md)
- Sprachen: [🇺🇸 English](../../ios/reset-app.md) · **🇩🇪 Deutsch** · [🇫🇷 Français](../../fr/ios/reset-app.md) · [🇪🇸 Español](../../es/ios/reset-app.md) · [🇨🇳 中文](../../zh/ios/reset-app.md)

> [!TIP]
> **Zu wenig Zeit? Wir richten deine App für dich ein.** Unser Team konfiguriert, erstellt & reicht deine WebViewGold-App ein – schlüsselfertig, mit schneller Bearbeitung, Made in Germany. [App einrichten lassen →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **Im Browser erstellen:** Kein Mac, keine IDE: Der **WebViewGold Cloud Builder** konfiguriert, erstellt & lädt deine App online hoch. [Cloud Builder entdecken →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
