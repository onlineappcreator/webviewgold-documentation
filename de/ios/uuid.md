---
title: "UUID-API – WebViewGold für iOS Dokumentation"
description: "Identifiziere App-Installationen mit einer eindeutigen UUID, die an deine WebView-URL angehängt oder per JavaScript abgerufen wird."
lang: "de"
product: "WebViewGold für iOS"
platform: "iOS"
category: "APIs & Funktionen"
slug: "uuid"
canonical_url: "https://www.webviewgold.com/de/docs/iOS/uuid/"
keywords:
  - "UUID-API"
  - "WebViewGold für iOS"
  - "Website in App umwandeln"
  - "WebView-App-Dokumentation"
  - "iOS WebView SDK"
  - "PWA zu App"
  - "HTML zu App"
  - "JavaScript-Bridge"
last_updated: "2026-10-09"
---

# UUID-API – WebViewGold für iOS

> **Zusammenfassung:** Identifiziere App-Installationen mit einer eindeutigen UUID, die an deine WebView-URL angehängt oder per JavaScript abgerufen wird.

[Dokumentation](../README.md) › [WebViewGold für iOS](README.md) › UUID-API

**Plattform:** iOS · **Kategorie:** APIs & Funktionen · **Online-Version:** [www.webviewgold.com/de/docs/iOS/uuid/](https://www.webviewgold.com/de/docs/iOS/uuid/)

---

Die UUID-API von WebViewGold ermöglicht es dir, eine nicht-personenbezogene, eindeutige Geräte-ID (UUID – „Universally Unique Identifier“) abzurufen, mit der ein **iOS-Gerät eindeutig identifiziert** werden kann. Diese Funktion kann hilfreich sein für:

- Speichern nutzerspezifischer Einstellungen auf dem Server
- Aufrechterhaltung von Sitzungszuständen
- Abrufen gespeicherter Daten auf Client-Seite

**Datenschutzhinweis:** Stelle sicher, dass du bei der Nutzung dieser Funktion die geltenden lokalen und internationalen **Datenschutzgesetze** einhältst, da hierbei eine Geräteidentifikation erfolgt.

## So rufst du die UUID ab

Um die UUID aus deiner WebView-basierten App abzurufen, verwende den folgenden Code:

```html
<a href="get-uuid://">Get UUID</a>
<a href="#" onClick="alert(uuid);">Show UUID</a>
```

- **UUID abrufen:** Fordert die UUID von WebViewGold an.
- **UUID anzeigen:** Zeigt die UUID zum einfachen Testen per **alert** an.

## Alternative Methode: UUID an die WebView-URL anhängen

Wenn du die UUID lieber in den URL-Parametern übergeben möchtest, aktiviere die Option `enhanceUrlUUID` in **Config.swift**, indem du sie auf `true` setzt. Dadurch wird bei der ersten Anfrage automatisch `uuid=XYZ` an deine WebView-URL angehängt, sodass du die UUID direkt in deinem Web-Content nutzen kannst:

- **Beispiel:** Wenn deine WebView-URL `https://www.example.org` lautet, wird sie als `https://www.example.org?uuid=XYZ` aufgerufen.
- **Hinweis:** Nur die initiale URL-Anfrage enthält diesen GET-Parameter, daher solltest du ihn in einer Session oder einem Cookie speichern, falls du ihn später in der App wiederverwenden möchtest.

## UUID automatisch in JavaScript injizieren

Um die UUID (und weitere Variablen) automatisch auf allen Seiten in JavaScript verfügbar zu machen, ohne URLs zu verändern, setze `autoInjectVariable` in **Config.swift** auf `true`. Dadurch kannst du die UUID und andere Werte direkt in jeder Seite abrufen.

---

## Weiterlesen

- ← Vorherige: [Apple-Wallet-Pass-API](wallet-pass.md)
- Weiter →: [Taschenlampen-API](flashlight.md)
- Dieselbe Funktion auf anderen Plattformen: [Android – UUID-API](../android/uuid.md) · [macOS – UUID API](../macos/uuid.md)
- Sprachen: [🇺🇸 English](../../ios/uuid.md) · **🇩🇪 Deutsch** · [🇫🇷 Français](../../fr/ios/uuid.md) · [🇪🇸 Español](../../es/ios/uuid.md) · [🇨🇳 中文](../../zh/ios/uuid.md)

> [!TIP]
> **Zu wenig Zeit? Wir richten deine App für dich ein.** Unser Team konfiguriert, erstellt & reicht deine WebViewGold-App ein – schlüsselfertig, mit schneller Bearbeitung, Made in Germany. [App einrichten lassen →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **Im Browser erstellen:** Kein Mac, keine IDE: Der **WebViewGold Cloud Builder** konfiguriert, erstellt & lädt deine App online hoch. [Cloud Builder entdecken →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
