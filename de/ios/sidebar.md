---
title: "Native Sidebar-Navigation – WebViewGold für iOS Dokumentation"
description: "Aktiviere ein natives ausklappbares Sidebar-Menü mit eigenen Links und SF-Symbols-Icons — konfiguriert über Sidebar.json."
lang: "de"
product: "WebViewGold für iOS"
platform: "iOS"
category: "Erweiterungen & Plugins"
slug: "sidebar"
canonical_url: "https://www.webviewgold.com/de/docs/iOS/sidebar/"
keywords:
  - "Native Sidebar"
  - "WebViewGold für iOS"
  - "Website in App umwandeln"
  - "WebView-App-Dokumentation"
  - "iOS WebView SDK"
  - "PWA zu App"
  - "HTML zu App"
  - "JavaScript-Bridge"
last_updated: "2026-10-09"
---

# Native Sidebar-Navigation – WebViewGold für iOS

> **Zusammenfassung:** Aktiviere ein natives ausklappbares Sidebar-Menü mit eigenen Links und SF-Symbols-Icons — konfiguriert über Sidebar.json.

[Dokumentation](../README.md) › [WebViewGold für iOS](README.md) › Native Sidebar

**Plattform:** iOS · **Kategorie:** Erweiterungen & Plugins · **Online-Version:** [www.webviewgold.com/de/docs/iOS/sidebar/](https://www.webviewgold.com/de/docs/iOS/sidebar/)

---

Neben dem [nativen Navigation Footer](navigation-footer.md) bringt WebViewGold eine native **ausklappbare Sidebar** mit, mit der du eine App-typische Navigation anbieten kannst, ohne deine Website anzupassen. Ein schwebender Menü-Button öffnet eine Sidebar mit deinen Links — jeder Eintrag navigiert die Haupt-WebView zu der von dir hinterlegten URL.

## Aktivierung

Setze die folgende Option in **Config.swift**:

```swift
var enableSidebar = true
```

## Konfiguration

Öffne **Sidebar.json** im Xcode-Projekt und definiere das Farbschema sowie die Menüeinträge:

```json
{
   "colour":"dark",
   "layout":[
      {
         "redirection_link":"https://example.org/home",
         "sf_symbol":"house",
         "name": "Home"
      },
      {
         "redirection_link":"https://example.org/shop",
         "sf_symbol":"cart",
         "name": "Shop"
      }
   ]
}
```

| Schlüssel | Beschreibung |
| --- | --- |
| `colour` | Farbschema der Sidebar: `dark` oder `light`. |
| `redirection_link` | URL, die in der Haupt-WebView geladen wird, wenn der Eintrag angetippt wird. |
| `sf_symbol` | Icon-Name aus Apples [SF-Symbols](https://developer.apple.com/sf-symbols/)-Bibliothek (z. B. `house`, `cart`, `wrench.and.screwdriver`). |
| `name` | Beschriftung des Sidebar-Eintrags. |

## Verhalten

- Ein schwebender Button öffnet und schließt die Sidebar über deinem Web-Inhalt.
- Ein Tipp auf einen Eintrag lädt die zugehörige URL in der Haupt-WebView — deine Web-App verlässt also nie die App-Hülle.
- Die Sidebar lässt sich mit dem [nativen Navigation Footer](navigation-footer.md) kombinieren oder unabhängig davon nutzen.

---

## Weiterlesen

- ← Vorherige: [Native Navigationsleiste](navigation-footer.md)
- Weiter →: [Bildschirmaufnahme-Erkennung](screen-capture.md)
- Sprachen: [🇺🇸 English](../../ios/sidebar.md) · **🇩🇪 Deutsch** · [🇫🇷 Français](../../fr/ios/sidebar.md) · [🇪🇸 Español](../../es/ios/sidebar.md) · [🇨🇳 中文](../../zh/ios/sidebar.md)

> [!TIP]
> **Zu wenig Zeit? Wir richten deine App für dich ein.** Unser Team konfiguriert, erstellt & reicht deine WebViewGold-App ein – schlüsselfertig, mit schneller Bearbeitung, Made in Germany. [App einrichten lassen →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **Im Browser erstellen:** Kein Mac, keine IDE: Der **WebViewGold Cloud Builder** konfiguriert, erstellt & lädt deine App online hoch. [Cloud Builder entdecken →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
