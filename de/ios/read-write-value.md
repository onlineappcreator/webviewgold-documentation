---
title: "Read/Write-Value-API – WebViewGold für iOS Dokumentation"
description: "Speichere einen String-Wert dauerhaft auf dem Gerät und lies ihn zurück in das JavaScript deiner Web-App."
lang: "de"
product: "WebViewGold für iOS"
platform: "iOS"
category: "APIs & Funktionen"
slug: "read-write-value"
canonical_url: "https://www.webviewgold.com/de/docs/iOS/read-write-value/"
keywords:
  - "Read/Write-Value-API"
  - "WebViewGold für iOS"
  - "Website in App umwandeln"
  - "WebView-App-Dokumentation"
  - "iOS WebView SDK"
  - "PWA zu App"
  - "HTML zu App"
  - "JavaScript-Bridge"
last_updated: "2026-10-09"
---

# Read/Write-Value-API – WebViewGold für iOS

> **Zusammenfassung:** Speichere einen String-Wert dauerhaft auf dem Gerät und lies ihn zurück in das JavaScript deiner Web-App.

[Dokumentation](../README.md) › [WebViewGold für iOS](README.md) › Read/Write-Value-API

**Plattform:** iOS · **Kategorie:** APIs & Funktionen · **Online-Version:** [www.webviewgold.com/de/docs/iOS/read-write-value/](https://www.webviewgold.com/de/docs/iOS/read-write-value/)

---

Die **Read/Write-Value-API** speichert dauerhaft einen beliebigen String auf dem Gerät (im privaten Speicher der App) und liest ihn zurück in dein JavaScript. Werte überstehen App-Neustarts und Cache-Löschungen — solange die App nicht deinstalliert wird.

## Wert schreiben

Alles nach `writevalue://` wird unverändert als ein String gespeichert. Definiere dein eigenes Format (Query-String, JSON, CSV — was zu deiner Web-App passt):

```html
<a href="writevalue://darkmode=on;user=42">Speichern</a>
```

## Wert lesen

Wird `readvalue://` ausgelöst, injiziert die App den gespeicherten String als `window.storedValues` zurück in die WebView, sodass dein JavaScript ihn lesen kann:

```html
<a href="readvalue://" onclick="setTimeout(showSettings, 200)">Laden</a>
<script>
  function showSettings() {
    console.log(window.storedValues || "noch keine Einstellungen");
  }
</script>
```

## Typische Anwendungsfälle

- Theme, Sprache oder Onboarding-Status eines Nutzers offline speichern.
- Ein Sitzungstoken zwischenspeichern, wenn du dich nicht auf Cookies verlassen kannst.
- Eine kleine lokale Einstellung ohne Backend-Roundtrip persistieren.

**Hinweise:** Werte gelten pro App-Installation und pro Gerät — sie werden **nicht** zwischen Geräten synchronisiert. Halte die Werte klein; diese API ist für Einstellungen gedacht, nicht als Blob-Speicher.

---

## Weiterlesen

- ← Vorherige: [Zwischenablage-API](clipboard.md)
- Weiter →: [Open-App-Settings-API](open-app-settings.md)
- Dieselbe Funktion auf anderen Plattformen: [Android – Read/Write Value API](../android/read-write-value.md)
- Sprachen: [🇺🇸 English](../../ios/read-write-value.md) · **🇩🇪 Deutsch** · [🇫🇷 Français](../../fr/ios/read-write-value.md) · [🇪🇸 Español](../../es/ios/read-write-value.md) · [🇨🇳 中文](../../zh/ios/read-write-value.md)

> [!TIP]
> **Zu wenig Zeit? Wir richten deine App für dich ein.** Unser Team konfiguriert, erstellt & reicht deine WebViewGold-App ein – schlüsselfertig, mit schneller Bearbeitung, Made in Germany. [App einrichten lassen →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **Im Browser erstellen:** Kein Mac, keine IDE: Der **WebViewGold Cloud Builder** konfiguriert, erstellt & lädt deine App online hoch. [Cloud Builder entdecken →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
