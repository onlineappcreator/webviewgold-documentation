---
title: "Zwischenablage-API – WebViewGold für Android Dokumentation"
description: "Kopiere Text in die Android-Zwischenablage und lies deren Inhalt aus deiner Web-App per JavaScript aus."
lang: "de"
product: "WebViewGold für Android"
platform: "Android"
category: "APIs & Funktionen"
slug: "clipboard"
canonical_url: "https://www.webviewgold.com/de/docs/android/clipboard/"
keywords:
  - "Zwischenablage-API"
  - "WebViewGold für Android"
  - "Website in App umwandeln"
  - "WebView-App-Dokumentation"
  - "Android WebView SDK"
  - "PWA zu App"
  - "HTML zu App"
  - "JavaScript-Bridge"
last_updated: "2026-10-09"
---

# Zwischenablage-API – WebViewGold für Android

> **Zusammenfassung:** Kopiere Text in die Android-Zwischenablage und lies deren Inhalt aus deiner Web-App per JavaScript aus.

[Dokumentation](../README.md) › [WebViewGold für Android](README.md) › Zwischenablage-API

**Plattform:** Android · **Kategorie:** APIs & Funktionen · **Online-Version:** [www.webviewgold.com/de/docs/android/clipboard/](https://www.webviewgold.com/de/docs/android/clipboard/)

---

Die WebViewGold Clipboard API bietet eine einfache und sichere Möglichkeit, aus deiner WebView-basierten App heraus auf den Inhalt der Zwischenablage des Geräts zuzugreifen. Sie dient als Alternative zum nativen Zugriff auf die WebView-Zwischenablage und bietet mehr Zuverlässigkeit über verschiedene Plattformen und Updates hinweg.

## Anwendungsfälle

- Vorausfüllen von Formularfeldern mit kopierten Daten
- Verbessern von Nutzerabläufen in Apps für Authentifizierung, Notizen oder Teilen
- Erstellen von Schnelleinfüge-Funktionen oder Tools für den Verlauf der Zwischenablage

## So rufst du den Inhalt der Zwischenablage ab

Um auf die Daten der Zwischenablage zuzugreifen, verwende den folgenden Aufruf:

```html
<a href="getclipboard://">Get Clipboard Data</a>
<a href="#" onClick="alert(clipboarddata);">Show Clipboard Data</a>
```

- **Zwischenablage abrufen:** Löst die native Lesefunktion der Zwischenablage aus.
- **Zwischenablage-Daten anzeigen:** Zeigt das Ergebnis an, das in der JavaScript-Variablen `clipboarddata` gespeichert ist.

**Technischer Hinweis:** Sobald `getclipboard://` ausgelöst wird, fügt WebViewGold den Inhalt der Zwischenablage automatisch in die JavaScript-Variable `clipboarddata` auf der Seite ein, wodurch er für alle weiteren Aktionen verfügbar ist.

---

## Weiterlesen

- ← Vorherige: [Ladeanzeige-API](loading-sign.md)
- Weiter →: [UUID-API](uuid.md)
- Dieselbe Funktion auf anderen Plattformen: [iOS – Zwischenablage-API](../ios/clipboard.md)
- Sprachen: [🇺🇸 English](../../android/clipboard.md) · **🇩🇪 Deutsch** · [🇫🇷 Français](../../fr/android/clipboard.md) · [🇪🇸 Español](../../es/android/clipboard.md) · [🇨🇳 中文](../../zh/android/clipboard.md)

> [!TIP]
> **Zu wenig Zeit? Wir richten deine App für dich ein.** Unser Team konfiguriert, erstellt & reicht deine WebViewGold-App ein – schlüsselfertig, mit schneller Bearbeitung, Made in Germany. [App einrichten lassen →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_android_doc_online)
>
> **Im Browser erstellen:** Kein Mac, keine IDE: Der **WebViewGold Cloud Builder** konfiguriert, erstellt & lädt deine App online hoch. [Cloud Builder entdecken →](https://www.webviewgold.com/cloud-builder?ref=android_docs)
