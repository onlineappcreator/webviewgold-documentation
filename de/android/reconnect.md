---
title: "Reconnect API – WebViewGold für Android Dokumentation"
description: "Reload the last online URL from your offline / fallback HTML page — the perfect \"Try again\" button for your custom offline screen."
lang: "de"
product: "WebViewGold für Android"
platform: "Android"
category: "APIs & Funktionen"
slug: "reconnect"
canonical_url: "https://www.webviewgold.com/de/docs/android/reconnect/"
keywords:
  - "Reconnect API"
  - "WebViewGold für Android"
  - "Website in App umwandeln"
  - "WebView-App-Dokumentation"
  - "Android WebView SDK"
  - "PWA zu App"
  - "HTML zu App"
  - "JavaScript-Bridge"
last_updated: "2026-10-09"
---

# Reconnect API – WebViewGold für Android

> **Zusammenfassung:** Reload the last online URL from your offline / fallback HTML page — the perfect "Try again" button for your custom offline screen.

[Dokumentation](../README.md) › [WebViewGold für Android](README.md) › Reconnect API

**Plattform:** Android · **Kategorie:** APIs & Funktionen · **Online-Version:** [www.webviewgold.com/de/docs/android/reconnect/](https://www.webviewgold.com/de/docs/android/reconnect/)

---

Die **Reconnect-API** lädt die letzte Online-URL erneut, auf der sich der Nutzer befand, bevor die App auf die Offline-HTML-Seite ausgewichen ist. Ideal als „Erneut versuchen"-Button auf deiner eigenen Fallback-Seite.

## So verwendest du die Funktion

Baue den Trigger in deine Offline-Seite ein (typischerweise `local-html/index.html`):

```html
<button onclick="window.location.href='reconnect://'">Try to reconnect</button>
```

## Wie es funktioniert

Die App merkt sich die letzte erfolgreich geladene Nicht-Helper-URL. Wenn der Nutzer `reconnect://` auslöst, navigiert der WebView zurück zu dieser URL. Ist die Verbindung noch immer weg, erscheint wieder deine Fallback-Seite.

## Zugehörige Config

- `FALLBACK_USE_LOCAL_HTML_FOLDER_IF_OFFLINE` in **Config.java** muss `true` sein, und du brauchst eine `local-html/index.html`-Fallback-Seite, damit diese Funktion sinnvoll wirkt.

---

## Weiterlesen

- ← Vorherige: [Open App Settings API](open-app-settings.md)
- Weiter →: [Read/Write Value API](read-write-value.md)
- Dieselbe Funktion auf anderen Plattformen: [iOS – Reconnect-API](../ios/reconnect.md)
- Sprachen: [🇺🇸 English](../../android/reconnect.md) · **🇩🇪 Deutsch** · [🇫🇷 Français](../../fr/android/reconnect.md) · [🇪🇸 Español](../../es/android/reconnect.md) · [🇨🇳 中文](../../zh/android/reconnect.md)

> [!TIP]
> **Zu wenig Zeit? Wir richten deine App für dich ein.** Unser Team konfiguriert, erstellt & reicht deine WebViewGold-App ein – schlüsselfertig, mit schneller Bearbeitung, Made in Germany. [App einrichten lassen →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_android_doc_online)
>
> **Im Browser erstellen:** Kein Mac, keine IDE: Der **WebViewGold Cloud Builder** konfiguriert, erstellt & lädt deine App online hoch. [Cloud Builder entdecken →](https://www.webviewgold.com/cloud-builder?ref=android_docs)
