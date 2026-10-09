---
title: "Splash Screen – WebViewGold für Android Dokumentation"
description: "Passe den Splash- bzw. Startbildschirm deiner Android-WebView-App mit deinen eigenen Grafiken an."
lang: "de"
product: "WebViewGold für Android"
platform: "Android"
category: "App-Design"
slug: "splash-screen"
canonical_url: "https://www.webviewgold.com/de/docs/android/splash-screen/"
keywords:
  - "Splash Screen"
  - "WebViewGold für Android"
  - "Website in App umwandeln"
  - "WebView-App-Dokumentation"
  - "Android WebView SDK"
  - "PWA zu App"
  - "HTML zu App"
  - "JavaScript-Bridge"
last_updated: "2026-10-09"
---

# Splash Screen – WebViewGold für Android

> **Zusammenfassung:** Passe den Splash- bzw. Startbildschirm deiner Android-WebView-App mit deinen eigenen Grafiken an.

[Dokumentation](../README.md) › [WebViewGold für Android](README.md) › Splash Screen

**Plattform:** Android · **Kategorie:** App-Design · **Online-Version:** [www.webviewgold.com/de/docs/android/splash-screen/](https://www.webviewgold.com/de/docs/android/splash-screen/)

---

Passe das Verhalten des Splash-Screens an, indem du die folgenden Variablen in `Config.java` konfigurierst:

| Option | Typ | Beschreibung |
| --- | --- | --- |
| SPLASH_SCREEN_ACTIVATED | **true** oder **false** | Auf *true* setzen, um den Splash-Screen zu aktivieren |
| SPLASH_TIMEOUT | Zahl (Millisekunden) | Verzögerung vor dem Anzeigen der Ladeanzeige, falls die Home-URL noch lädt |
| REMAIN_SPLASH_OPTION | **true** oder **false** | Bei *true* bleibt der Splash-Screen sichtbar, bis die Home-URL vollständig geladen ist (überschreibt `SPLASH_TIMEOUT`) |
| SPLASH_MIN_TIME | Zahl (Millisekunden) | Minimale Anzeigedauer, wenn `REMAIN_SPLASH_OPTION` auf *true* gesetzt ist; wird ignoriert, wenn die tatsächliche Ladezeit diesen Wert überschreitet |
| SPLASH_FADE_OUT | Zahl (Millisekunden) | Dauer der Ausblendanimation nach allen Timern; auf *0* setzen, um den Ausblendeffekt zu deaktivieren |
| SCALE_SPLASH_IMAGE | Prozentsatz [0–100] | Skaliert das Splash-Bild relativ zur kleinsten Bildschirmabmessung des Geräts; *0* blendet das Bild aus |

## Splash-Screen-Bild ersetzen

- Ersetze `splash.gif` in deinen Assets durch dein eigenes quadratisches GIF (z. B. 128×128, 512×512 oder 1024×1024 px)
- Stelle sicher, dass die Bildabmessungen gleich sind (Breite = Höhe), um die optimale Darstellung zu gewährleisten
- Lege die Hintergrundfarbe in `colors.xml` fest

Die Schritte zum Hinzufügen eines individuellen Splash-Screens zu deiner Android-App werden im folgenden Video gezeigt:

[![Video ansehen: Splash Screen](https://img.youtube.com/vi/x684JHvW8lI/hqdefault.jpg)](https://www.youtube.com/watch?v=x684JHvW8lI)

---

## Weiterlesen

- ← Vorherige: [App-Icon](app-icon.md)
- Weiter →: [Navigation Drawer & Footer](navigation-drawer.md)
- Dieselbe Funktion auf anderen Plattformen: [iOS – Name, Icon & Splash](../ios/app-name-icon-splash.md) · [macOS – Begrüßungsbildschirm](../macos/splash-screen.md)
- Sprachen: [🇺🇸 English](../../android/splash-screen.md) · **🇩🇪 Deutsch** · [🇫🇷 Français](../../fr/android/splash-screen.md) · [🇪🇸 Español](../../es/android/splash-screen.md) · [🇨🇳 中文](../../zh/android/splash-screen.md)

> [!TIP]
> **Zu wenig Zeit? Wir richten deine App für dich ein.** Unser Team konfiguriert, erstellt & reicht deine WebViewGold-App ein – schlüsselfertig, mit schneller Bearbeitung, Made in Germany. [App einrichten lassen →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_android_doc_online)
>
> **Im Browser erstellen:** Kein Mac, keine IDE: Der **WebViewGold Cloud Builder** konfiguriert, erstellt & lädt deine App online hoch. [Cloud Builder entdecken →](https://www.webviewgold.com/cloud-builder?ref=android_docs)
