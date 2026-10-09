---
title: "Native Navigationsleiste – WebViewGold für iOS Dokumentation"
description: "Aktiviere eine native untere Navigationsleiste mit Zurück-, Vorwärts- und individuellen Schaltflächen in deiner iOS-App."
lang: "de"
product: "WebViewGold für iOS"
platform: "iOS"
category: "Erweiterungen & Plugins"
slug: "navigation-footer"
canonical_url: "https://www.webviewgold.com/de/docs/iOS/navigation-footer/"
keywords:
  - "Native Navigationsleiste"
  - "WebViewGold für iOS"
  - "Website in App umwandeln"
  - "WebView-App-Dokumentation"
  - "iOS WebView SDK"
  - "PWA zu App"
  - "HTML zu App"
  - "JavaScript-Bridge"
last_updated: "2026-10-09"
---

# Native Navigationsleiste – WebViewGold für iOS

> **Zusammenfassung:** Aktiviere eine native untere Navigationsleiste mit Zurück-, Vorwärts- und individuellen Schaltflächen in deiner iOS-App.

[Dokumentation](../README.md) › [WebViewGold für iOS](README.md) › Native Navigationsleiste

**Plattform:** iOS · **Kategorie:** Erweiterungen & Plugins · **Online-Version:** [www.webviewgold.com/de/docs/iOS/navigation-footer/](https://www.webviewgold.com/de/docs/iOS/navigation-footer/)

---

Setze `var showNavFooter = true` in `Config.swift`, um die native Navigations-Fußleiste zu aktivieren. Konfiguriere Buttons und Links in `FooterBar.json`. Beispiel:

```json
{
   "colour":"dark",
   "layout":[
      {
         "redirection_link":"https://webviewgoldtest.github.io/index.html",
         "sf_symbol":"house",
         "name": "Home"
      },
      {
         "redirection_link":"https://webviewgoldtest.github.io/appControls.html",
         "sf_symbol":"wrench.and.screwdriver",
         "name": "Controls"
      },
      {
         "redirection_link":"https://webviewgoldtest.github.io/NFCtesting.html",
         "sf_symbol":"wifi.square",
         "name": "NFC"
      },
      {
         "redirection_link":"https://webviewgoldtest.github.io/IAPtesting.html",
         "sf_symbol":"cart",
         "name": "Purchases"
      },
      {
         "redirection_link":"https://webviewgoldtest.github.io/permissions.html",
         "sf_symbol":"lock.open",
         "name": "Permissions"
      }
   ]
}
```

Jedes `sf_symbol` verwendet ein [SF Symbol](https://developer.apple.com/sf-symbols/) und öffnet den `redirection_link` in der Haupt-WebView.

---

## Weiterlesen

- ← Vorherige: [App Clip Extension](app-clip.md)
- Weiter →: [Native Sidebar](sidebar.md)
- Dieselbe Funktion auf anderen Plattformen: [Android – Navigation Drawer & Footer](../android/navigation-drawer.md)
- Sprachen: [🇺🇸 English](../../ios/navigation-footer.md) · **🇩🇪 Deutsch** · [🇫🇷 Français](../../fr/ios/navigation-footer.md) · [🇪🇸 Español](../../es/ios/navigation-footer.md) · [🇨🇳 中文](../../zh/ios/navigation-footer.md)

> [!TIP]
> **Zu wenig Zeit? Wir richten deine App für dich ein.** Unser Team konfiguriert, erstellt & reicht deine WebViewGold-App ein – schlüsselfertig, mit schneller Bearbeitung, Made in Germany. [App einrichten lassen →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **Im Browser erstellen:** Kein Mac, keine IDE: Der **WebViewGold Cloud Builder** konfiguriert, erstellt & lädt deine App online hoch. [Cloud Builder entdecken →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
