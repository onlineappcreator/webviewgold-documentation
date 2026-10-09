---
title: "App-Zurücksetzen-API – WebViewGold für Android Dokumentation"
description: "Setze Cache, Cookies und lokalen Speicher deiner Android-WebView-App mit einem einzigen Link oder JavaScript-Aufruf zurück."
lang: "de"
product: "WebViewGold für Android"
platform: "Android"
category: "APIs & Funktionen"
slug: "reset-app"
canonical_url: "https://www.webviewgold.com/de/docs/android/reset-app/"
keywords:
  - "App-Zurücksetzen-API"
  - "WebViewGold für Android"
  - "Website in App umwandeln"
  - "WebView-App-Dokumentation"
  - "Android WebView SDK"
  - "PWA zu App"
  - "HTML zu App"
  - "JavaScript-Bridge"
last_updated: "2026-10-09"
---

# App-Zurücksetzen-API – WebViewGold für Android

> **Zusammenfassung:** Setze Cache, Cookies und lokalen Speicher deiner Android-WebView-App mit einem einzigen Link oder JavaScript-Aufruf zurück.

[Dokumentation](../README.md) › [WebViewGold für Android](README.md) › App-Zurücksetzen-API

**Plattform:** Android · **Kategorie:** APIs & Funktionen · **Online-Version:** [www.webviewgold.com/de/docs/android/reset-app/](https://www.webviewgold.com/de/docs/android/reset-app/)

---

In bestimmten Fällen kann das Zurücksetzen der App auf ihre Ausgangseinstellungen (durch Löschen von Cookies und Cache) erforderlich sein, um die optimale Leistung wiederherzustellen. Die **Reset-App-API** bietet eine unkomplizierte Möglichkeit, diesen Reset auszulösen.

## Verwendung

Um die App-Daten zurückzusetzen, verwende einfach den folgenden Link in deiner App:

```html
<a href="reset://">Reset App Link</a>
```

Dieser Link wird:

- Alle Cookies löschen
- Zwischengespeicherte Daten löschen

## Testen der Reset-Funktionalität

Um diese Funktion zu testen, füge die folgende Demo-URL zu deiner WebViewGold-App hinzu: <https://www.onlineappcreator.com/reset_test.html>

**Hinweis:** Verwende die Reset-Funktion mit Bedacht, da sie Nutzerdaten in Bezug auf Cookies und Cache löscht. Dies kann sich auf gespeicherte Einstellungen oder Sitzungsdaten auswirken und Nutzer aus aktiven Sitzungen abmelden.

---

## Weiterlesen

- ← Vorherige: [Natives Video (PiP) API](native-video.md)
- Weiter →: [Ladeanzeige-API](loading-sign.md)
- Dieselbe Funktion auf anderen Plattformen: [iOS – App-Zurücksetzen-API](../ios/reset-app.md)
- Sprachen: [🇺🇸 English](../../android/reset-app.md) · **🇩🇪 Deutsch** · [🇫🇷 Français](../../fr/android/reset-app.md) · [🇪🇸 Español](../../es/android/reset-app.md) · [🇨🇳 中文](../../zh/android/reset-app.md)

> [!TIP]
> **Zu wenig Zeit? Wir richten deine App für dich ein.** Unser Team konfiguriert, erstellt & reicht deine WebViewGold-App ein – schlüsselfertig, mit schneller Bearbeitung, Made in Germany. [App einrichten lassen →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_android_doc_online)
>
> **Im Browser erstellen:** Kein Mac, keine IDE: Der **WebViewGold Cloud Builder** konfiguriert, erstellt & lädt deine App online hoch. [Cloud Builder entdecken →](https://www.webviewgold.com/cloud-builder?ref=android_docs)
