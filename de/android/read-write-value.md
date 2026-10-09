---
title: "Read/Write Value API – WebViewGold für Android Dokumentation"
description: "Persist small strings on the device from JavaScript and read them back — for theme, language, session tokens, or onboarding state."
lang: "de"
product: "WebViewGold für Android"
platform: "Android"
category: "APIs & Funktionen"
slug: "read-write-value"
canonical_url: "https://www.webviewgold.com/de/docs/android/read-write-value/"
keywords:
  - "Read/Write Value API"
  - "WebViewGold für Android"
  - "Website in App umwandeln"
  - "WebView-App-Dokumentation"
  - "Android WebView SDK"
  - "PWA zu App"
  - "HTML zu App"
  - "JavaScript-Bridge"
last_updated: "2026-10-09"
---

# Read/Write Value API – WebViewGold für Android

> **Zusammenfassung:** Persist small strings on the device from JavaScript and read them back — for theme, language, session tokens, or onboarding state.

[Dokumentation](../README.md) › [WebViewGold für Android](README.md) › Read/Write Value API

**Plattform:** Android · **Kategorie:** APIs & Funktionen · **Online-Version:** [www.webviewgold.com/de/docs/android/read-write-value/](https://www.webviewgold.com/de/docs/android/read-write-value/)

---

Die **Read/Write-Value-API** speichert einen beliebigen String dauerhaft auf dem Gerät (im privaten Speicher der App) und liest ihn in dein JavaScript zurück. Werte überleben App-Neustarts und Cache-Löschungen – außer das Betriebssystem löscht die App-Daten.

## Wert schreiben

Alles nach `writevalue://` wird als ein String gespeichert. Lege dein eigenes Format fest (Query-String, JSON, CSV – wie es zu deiner Web-App passt):

```html
<a href="writevalue://darkmode=on;user=42">Save</a>
```

## Wert lesen

Beim Aufruf von `readvalue://` injiziert die App den gespeicherten String zurück in den WebView, sodass dein JavaScript ihn lesen kann:

```html
<a href="readvalue://" onclick="setTimeout(showSettings, 200)">Load</a>
<script>
  function showSettings() {
    console.log(window.appSettings || "no settings yet");
  }
</script>
```

## Typische Anwendungsfälle

- Theme, Sprache oder Onboarding-Status offline merken.
- Session-Token puffern, wenn Cookies nicht zuverlässig sind.
- Kleine lokale Präferenzen ohne Backend-Roundtrip.

**Hinweise:** Werte sind pro Installation und pro Gerät – sie werden **nicht** über Geräte synchronisiert. Halte die Werte klein; die API ist für Einstellungen gedacht, nicht für Blob-Storage.

---

## Weiterlesen

- ← Vorherige: [Reconnect API](reconnect.md)
- Weiter →: [Biometric Auth API](biometric-auth.md)
- Dieselbe Funktion auf anderen Plattformen: [iOS – Read/Write-Value-API](../ios/read-write-value.md)
- Sprachen: [🇺🇸 English](../../android/read-write-value.md) · **🇩🇪 Deutsch** · [🇫🇷 Français](../../fr/android/read-write-value.md) · [🇪🇸 Español](../../es/android/read-write-value.md) · [🇨🇳 中文](../../zh/android/read-write-value.md)

> [!TIP]
> **Zu wenig Zeit? Wir richten deine App für dich ein.** Unser Team konfiguriert, erstellt & reicht deine WebViewGold-App ein – schlüsselfertig, mit schneller Bearbeitung, Made in Germany. [App einrichten lassen →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_android_doc_online)
>
> **Im Browser erstellen:** Kein Mac, keine IDE: Der **WebViewGold Cloud Builder** konfiguriert, erstellt & lädt deine App online hoch. [Cloud Builder entdecken →](https://www.webviewgold.com/cloud-builder?ref=android_docs)
