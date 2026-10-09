---
title: "UUID-API – WebViewGold für Android Dokumentation"
description: "Identifiziere App-Installationen mit einer eindeutigen UUID, die an deine WebView-URL angehängt oder per JavaScript abgerufen wird."
lang: "de"
product: "WebViewGold für Android"
platform: "Android"
category: "APIs & Funktionen"
slug: "uuid"
canonical_url: "https://www.webviewgold.com/de/docs/android/uuid/"
keywords:
  - "UUID-API"
  - "WebViewGold für Android"
  - "Website in App umwandeln"
  - "WebView-App-Dokumentation"
  - "Android WebView SDK"
  - "PWA zu App"
  - "HTML zu App"
  - "JavaScript-Bridge"
last_updated: "2026-10-09"
---

# UUID-API – WebViewGold für Android

> **Zusammenfassung:** Identifiziere App-Installationen mit einer eindeutigen UUID, die an deine WebView-URL angehängt oder per JavaScript abgerufen wird.

[Dokumentation](../README.md) › [WebViewGold für Android](README.md) › UUID-API

**Plattform:** Android · **Kategorie:** APIs & Funktionen · **Online-Version:** [www.webviewgold.com/de/docs/android/uuid/](https://www.webviewgold.com/de/docs/android/uuid/)

---

Die WebViewGold UUID-API ermöglicht es dir, eine nicht-personenbezogene, eindeutige Geräte-ID (UUID - "Universally Unique Identifier") über JavaScript abzurufen, mit der ein Android-Gerät eindeutig identifiziert werden kann. Diese Funktion kann hilfreich sein für:

- Speichern nutzerspezifischer Einstellungen auf dem Server
- Aufrechterhaltung von Sitzungsstatus
- Abrufen gespeicherter Daten auf der Client-Seite

**Datenschutzhinweis:** Stelle sicher, dass du bei der Nutzung dieser Funktion die lokalen und internationalen Datenschutzgesetze einhältst, da eine Geräteidentifizierung erfolgt.

## So rufst du die UUID ab

Um die UUID aus deiner WebView-basierten App abzurufen, verwende den folgenden Code:

```html
<a href="get-uuid://">Get UUID</a>
<a href="#" onClick="alert(uuid);">Show UUID</a>
```

- **UUID abrufen:** Fordert die UUID von WebViewGold an.
- **UUID anzeigen:** Zeigt die UUID über eine **alert**-Meldung zum einfachen Testen an.

## Alternative Methode: UUID an die WebView-URL anhängen

Wenn du die UUID lieber in die URL-Parameter aufnehmen möchtest, aktiviere die Option `UUID_ENHANCE_WEBVIEW_URL` in **Config.java**, indem du sie auf `true` setzt. Dadurch wird `uuid=XYZ` beim ersten Aufruf automatisch an deine WebView-URL angehängt, sodass du direkt in deinem Web-Inhalt auf die UUID zugreifen kannst:

- **Beispiel:** Wenn deine WebView-URL `https://www.example.org` lautet, wird sie als `https://www.example.org?uuid=XYZ` aufgerufen.
- **Hinweis:** Nur die erste URL-Anfrage enthält diesen GET-Parameter. Erwäge daher, ihn in einer Sitzung oder einem Cookie zu speichern, falls du später in der App darauf zugreifen möchtest.

## UUID automatisch in JavaScript einfügen

Um die UUID (und andere Variablen) automatisch in JavaScript auf allen Seiten verfügbar zu machen, ohne URLs zu ändern, setze `AUTO_INJECT_VARIABLES` in **Config.java** auf `true`. So kannst du direkt auf jeder Seite auf die UUID und andere Werte zugreifen.

---

## Weiterlesen

- ← Vorherige: [Zwischenablage-API](clipboard.md)
- Weiter →: [Taschenlampen-API](flashlight.md)
- Dieselbe Funktion auf anderen Plattformen: [iOS – UUID-API](../ios/uuid.md) · [macOS – UUID API](../macos/uuid.md)
- Sprachen: [🇺🇸 English](../../android/uuid.md) · **🇩🇪 Deutsch** · [🇫🇷 Français](../../fr/android/uuid.md) · [🇪🇸 Español](../../es/android/uuid.md) · [🇨🇳 中文](../../zh/android/uuid.md)

> [!TIP]
> **Zu wenig Zeit? Wir richten deine App für dich ein.** Unser Team konfiguriert, erstellt & reicht deine WebViewGold-App ein – schlüsselfertig, mit schneller Bearbeitung, Made in Germany. [App einrichten lassen →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_android_doc_online)
>
> **Im Browser erstellen:** Kein Mac, keine IDE: Der **WebViewGold Cloud Builder** konfiguriert, erstellt & lädt deine App online hoch. [Cloud Builder entdecken →](https://www.webviewgold.com/cloud-builder?ref=android_docs)
