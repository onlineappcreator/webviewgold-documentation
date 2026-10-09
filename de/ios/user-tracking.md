---
title: "Nutzer-Tracking-Entscheidung-API – WebViewGold für iOS Dokumentation"
description: "Berücksichtige App Tracking Transparency: Lies die Tracking-Entscheidung des Nutzers aus und reagiere darauf in deiner WebViewGold-iOS-App."
lang: "de"
product: "WebViewGold für iOS"
platform: "iOS"
category: "APIs & Funktionen"
slug: "user-tracking"
canonical_url: "https://www.webviewgold.com/de/docs/iOS/user-tracking/"
keywords:
  - "Nutzer-Tracking-Entscheidung-API"
  - "WebViewGold für iOS"
  - "Website in App umwandeln"
  - "WebView-App-Dokumentation"
  - "iOS WebView SDK"
  - "PWA zu App"
  - "HTML zu App"
  - "JavaScript-Bridge"
last_updated: "2026-10-09"
---

# Nutzer-Tracking-Entscheidung-API – WebViewGold für iOS

> **Zusammenfassung:** Berücksichtige App Tracking Transparency: Lies die Tracking-Entscheidung des Nutzers aus und reagiere darauf in deiner WebViewGold-iOS-App.

[Dokumentation](../README.md) › [WebViewGold für iOS](README.md) › Nutzer-Tracking-Entscheidung-API

**Plattform:** iOS · **Kategorie:** APIs & Funktionen · **Online-Version:** [www.webviewgold.com/de/docs/iOS/user-tracking/](https://www.webviewgold.com/de/docs/iOS/user-tracking/)

---

In iOS müssen Apps auf Grundlage des Apple-AppTrackingTransparency-Frameworks um Erlaubnis für das Tracking von Nutzerdaten bitten. Mit WebViewGold kannst du erkennen, welche Auswahl der Nutzer bei der Installation deiner App getroffen hat, um in deiner Web-App entsprechend zu reagieren. Die JavaScript-Variable **trackingDisabled** kann von WebViewGold entweder auf true gesetzt werden, um darzustellen, dass das Tracking blockiert wurde, oder auf false, wenn dies nicht der Fall ist. In deiner Web-App kannst du den JavaScript-Status einfach überprüfen, indem du zunächst die JavaScript-Variable abrufst und anschließend anzeigst:

```html
<a href="user-disable-tracking://">Set JavaScript variable</a>
<a href="#" onClick="alert(trackingDisabled);">Show tracking decision</a>
```

---

## Weiterlesen

- ← Vorherige: [App-Zurücksetzen-API](reset-app.md)
- Weiter →: [Ladeanzeige-API](loading-sign.md)
- Sprachen: [🇺🇸 English](../../ios/user-tracking.md) · **🇩🇪 Deutsch** · [🇫🇷 Français](../../fr/ios/user-tracking.md) · [🇪🇸 Español](../../es/ios/user-tracking.md) · [🇨🇳 中文](../../zh/ios/user-tracking.md)

> [!TIP]
> **Zu wenig Zeit? Wir richten deine App für dich ein.** Unser Team konfiguriert, erstellt & reicht deine WebViewGold-App ein – schlüsselfertig, mit schneller Bearbeitung, Made in Germany. [App einrichten lassen →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **Im Browser erstellen:** Kein Mac, keine IDE: Der **WebViewGold Cloud Builder** konfiguriert, erstellt & lädt deine App online hoch. [Cloud Builder entdecken →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
