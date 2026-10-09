---
title: "Share Extension – WebViewGold für iOS Dokumentation"
description: "Lass Nutzer Inhalte aus anderen Apps mit einer Share Extension direkt in deine iOS-WebView-App teilen."
lang: "de"
product: "WebViewGold für iOS"
platform: "iOS"
category: "Erweiterungen & Plugins"
slug: "share-extension"
canonical_url: "https://www.webviewgold.com/de/docs/iOS/share-extension/"
keywords:
  - "Share Extension"
  - "WebViewGold für iOS"
  - "Website in App umwandeln"
  - "WebView-App-Dokumentation"
  - "iOS WebView SDK"
  - "PWA zu App"
  - "HTML zu App"
  - "JavaScript-Bridge"
last_updated: "2026-10-09"
---

# Share Extension – WebViewGold für iOS

> **Zusammenfassung:** Lass Nutzer Inhalte aus anderen Apps mit einer Share Extension direkt in deine iOS-WebView-App teilen.

[Dokumentation](../README.md) › [WebViewGold für iOS](README.md) › Share Extension

**Plattform:** iOS · **Kategorie:** Erweiterungen & Plugins · **Online-Version:** [www.webviewgold.com/de/docs/iOS/share-extension/](https://www.webviewgold.com/de/docs/iOS/share-extension/)

---

Wenn Benutzer Texte oder Bilder aus Apps wie Fotos oder Safari an deine App weitergeben, stehen die Daten in der JavaScript-Variable `sharedData` zur Verfügung. Geteilte Bilder werden als Base64-Strings bereitgestellt.

```html
<script>
if (typeof sharedData !== 'undefined') {
    console.log(sharedData);
}
</script>
```

---

## Weiterlesen

- ← Vorherige: [Open-App-Settings-API](open-app-settings.md)
- Weiter →: [Widget Extension](widget-extension.md)
- Dieselbe Funktion auf anderen Plattformen: [Android – ShareIntent-API](../android/share-intent.md)
- Sprachen: [🇺🇸 English](../../ios/share-extension.md) · **🇩🇪 Deutsch** · [🇫🇷 Français](../../fr/ios/share-extension.md) · [🇪🇸 Español](../../es/ios/share-extension.md) · [🇨🇳 中文](../../zh/ios/share-extension.md)

> [!TIP]
> **Zu wenig Zeit? Wir richten deine App für dich ein.** Unser Team konfiguriert, erstellt & reicht deine WebViewGold-App ein – schlüsselfertig, mit schneller Bearbeitung, Made in Germany. [App einrichten lassen →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **Im Browser erstellen:** Kein Mac, keine IDE: Der **WebViewGold Cloud Builder** konfiguriert, erstellt & lädt deine App online hoch. [Cloud Builder entdecken →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
