---
title: "Bildschirmaufnahme-Erkennung – WebViewGold für iOS Dokumentation"
description: "Erkenne Screenshots und Bildschirmaufnahmen in deiner iOS-App und reagiere aus deiner Web-App darauf."
lang: "de"
product: "WebViewGold für iOS"
platform: "iOS"
category: "Erweiterungen & Plugins"
slug: "screen-capture"
canonical_url: "https://www.webviewgold.com/de/docs/iOS/screen-capture/"
keywords:
  - "Bildschirmaufnahme-Erkennung"
  - "WebViewGold für iOS"
  - "Website in App umwandeln"
  - "WebView-App-Dokumentation"
  - "iOS WebView SDK"
  - "PWA zu App"
  - "HTML zu App"
  - "JavaScript-Bridge"
last_updated: "2026-10-09"
---

# Bildschirmaufnahme-Erkennung – WebViewGold für iOS

> **Zusammenfassung:** Erkenne Screenshots und Bildschirmaufnahmen in deiner iOS-App und reagiere aus deiner Web-App darauf.

[Dokumentation](../README.md) › [WebViewGold für iOS](README.md) › Bildschirmaufnahme-Erkennung

**Plattform:** iOS · **Kategorie:** Erweiterungen & Plugins · **Online-Version:** [www.webviewgold.com/de/docs/iOS/screen-capture/](https://www.webviewgold.com/de/docs/iOS/screen-capture/)

---

Setze `let preventScreenCapture = true` in `Config.swift`, um Screenshots oder Bildschirmaufzeichnungen zu erkennen und automatisch die JavaScript-Funktion `onScreenCaptureAttempt` aufzurufen.

```html
<script>
function onScreenCaptureAttempt() {
    alert('Screen capture detected');
}
</script>
```

---

## Weiterlesen

- ← Vorherige: [Native Sidebar](sidebar.md)
- Weiter →: [MultiAPICall-Funktion](multi-api-call.md)
- Sprachen: [🇺🇸 English](../../ios/screen-capture.md) · **🇩🇪 Deutsch** · [🇫🇷 Français](../../fr/ios/screen-capture.md) · [🇪🇸 Español](../../es/ios/screen-capture.md) · [🇨🇳 中文](../../zh/ios/screen-capture.md)

> [!TIP]
> **Zu wenig Zeit? Wir richten deine App für dich ein.** Unser Team konfiguriert, erstellt & reicht deine WebViewGold-App ein – schlüsselfertig, mit schneller Bearbeitung, Made in Germany. [App einrichten lassen →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **Im Browser erstellen:** Kein Mac, keine IDE: Der **WebViewGold Cloud Builder** konfiguriert, erstellt & lädt deine App online hoch. [Cloud Builder entdecken →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
