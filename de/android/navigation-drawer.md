---
title: "Navigation Drawer & Bottom Navigation Footer – WebViewGold für Android Dokumentation"
description: "Ship an app-like navigation experience with the built-in Material navigation drawer and Material 3 bottom navigation bar — no changes to your website required."
lang: "de"
product: "WebViewGold für Android"
platform: "Android"
category: "App-Design"
slug: "navigation-drawer"
canonical_url: "https://www.webviewgold.com/de/docs/android/navigation-drawer/"
keywords:
  - "Navigation Drawer & Footer"
  - "WebViewGold für Android"
  - "Website in App umwandeln"
  - "WebView-App-Dokumentation"
  - "Android WebView SDK"
  - "PWA zu App"
  - "HTML zu App"
  - "JavaScript-Bridge"
last_updated: "2026-10-09"
---

# Navigation Drawer & Bottom Navigation Footer – WebViewGold für Android

> **Zusammenfassung:** Ship an app-like navigation experience with the built-in Material navigation drawer and Material 3 bottom navigation bar — no changes to your website required.

[Dokumentation](../README.md) › [WebViewGold für Android](README.md) › Navigation Drawer & Footer

**Plattform:** Android · **Kategorie:** App-Design · **Online-Version:** [www.webviewgold.com/de/docs/android/navigation-drawer/](https://www.webviewgold.com/de/docs/android/navigation-drawer/)

---

WebViewGold liefert zwei eingebaute native Navigations-UIs, sodass du eine App-artige Navigation ausrollen kannst, ohne die Website anzufassen: einen seitlichen **Navigation-Drawer** und eine Material-3-**Bottom-Navigation**. Beide sind optional und können kombiniert oder einzeln genutzt werden.

## 1. Seitlicher Navigation-Drawer

Ein schwebender Menü-Button öffnet einen Material-Navigation-Drawer mit deinen Links. Aktiviere ihn in **Config.java**:

```java
static boolean ENABLE_NAVIGATION_DRAWER = true;
```

Konfiguriere die Einträge und Icons in:

```
app/src/main/res/menu/menu_drawer.xml
```

Jeder `<item>` wird zu einer Drawer-Zeile und navigiert beim Tippen den WebView zur zugehörigen URL.

## 2. Bottom-Navigation-Footer

Eine Material-3-Bottom-Navigation sitzt am unteren Bildschirmrand und wechselt zwischen den Top-Level-Bereichen. Aktiviere sie in **Config.java**:

```java
static boolean ENABLE_NAVIGATION_FOOTER = true;
```

Dieselbe Datei (`res/menu/menu_drawer.xml`) steuert die Einträge – wähle 3–5 Top-Level-Ziele.

## Verhalten

- Beide UIs respektieren automatisch den Dark-/Light-Modus des Geräts.
- Icons und Beschriftungen kommen aus deiner Menü-XML.
- Ein Tap auf einen Eintrag lädt die zugehörige URL im Haupt-WebView, sodass deine Web-App nicht die App-Hülle verlässt.

**Referenz:** [Material-3-Bottom-Navigation-Richtlinien](https://m3.material.io/components/navigation-bar/overview).

---

## Weiterlesen

- ← Vorherige: [Splash Screen](splash-screen.md)
- Weiter →: [URL-Handling-API](url-handling.md)
- Dieselbe Funktion auf anderen Plattformen: [iOS – Native Navigationsleiste](../ios/navigation-footer.md)
- Sprachen: [🇺🇸 English](../../android/navigation-drawer.md) · **🇩🇪 Deutsch** · [🇫🇷 Français](../../fr/android/navigation-drawer.md) · [🇪🇸 Español](../../es/android/navigation-drawer.md) · [🇨🇳 中文](../../zh/android/navigation-drawer.md)

> [!TIP]
> **Zu wenig Zeit? Wir richten deine App für dich ein.** Unser Team konfiguriert, erstellt & reicht deine WebViewGold-App ein – schlüsselfertig, mit schneller Bearbeitung, Made in Germany. [App einrichten lassen →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_android_doc_online)
>
> **Im Browser erstellen:** Kein Mac, keine IDE: Der **WebViewGold Cloud Builder** konfiguriert, erstellt & lädt deine App online hoch. [Cloud Builder entdecken →](https://www.webviewgold.com/cloud-builder?ref=android_docs)
