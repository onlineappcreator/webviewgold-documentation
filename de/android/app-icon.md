---
title: "App-Icon – WebViewGold für Android Dokumentation"
description: "Füge dein individuelles App-Icon Schritt für Schritt in Android Studio zu deiner WebViewGold-Android-App hinzu."
lang: "de"
product: "WebViewGold für Android"
platform: "Android"
category: "App-Design"
slug: "app-icon"
canonical_url: "https://www.webviewgold.com/de/docs/android/app-icon/"
keywords:
  - "App-Icon"
  - "WebViewGold für Android"
  - "Website in App umwandeln"
  - "WebView-App-Dokumentation"
  - "Android WebView SDK"
  - "PWA zu App"
  - "HTML zu App"
  - "JavaScript-Bridge"
last_updated: "2026-10-09"
---

# App-Icon – WebViewGold für Android

> **Zusammenfassung:** Füge dein individuelles App-Icon Schritt für Schritt in Android Studio zu deiner WebViewGold-Android-App hinzu.

[Dokumentation](../README.md) › [WebViewGold für Android](README.md) › App-Icon

**Plattform:** Android · **Kategorie:** App-Design · **Online-Version:** [www.webviewgold.com/de/docs/android/app-icon/](https://www.webviewgold.com/de/docs/android/app-icon/)

---

## Optionaler App-Hinweis für deine Datenschutzerklärung / Nutzungsbedingungen

Wenn du deinen Nutzern (WebViewGold-basierte) mobile Apps anbietest, kannst du optional die folgende Erklärung in deine Datenschutzerklärung oder deine Nutzungsbedingungen aufnehmen (dieser Hinweis dient ausschließlich zu Informationszwecken und stellt keine Rechtsberatung dar. Wir übernehmen keine Haftung für die Verwendung dieses Textes. Bitte konsultiere für eine individuelle Beratung einen Rechtsexperten):

> ```
> Our mobile apps (iOS/Android) are developed using WebViewGold by jocapps GmbH (Germany). These apps display the content of our website using a WebView framework and enrich it with selected native features to improve usability and performance. Accordingly, the same privacy policy and terms of service that apply to our website also apply to our mobile apps. For more information, please visit
> https://www.webviewgold.com/#convert-website-to-app-privacy, or contact us directly.
> ```

---

## 3) Ein individuelles App-Icon hinzufügen

![Android App-Icon](../../assets/android/img/screenshot_Icon.webp)

So fügst du deiner WebView-basierten Android-App ein individuelles App-Icon hinzu:

### 1. Vorhandene App-Icons finden

Suche zunächst die vorhandenen App-Icon-Dateien:

- Klicke mit der rechten Maustaste auf jede 'ic_launcher.png'-Datei in deinem Projekt (Größen von hdpi bis xxxhdpi).
- Wähle "Reveal in Finder" (Mac) oder "Reveal in Explorer" (Windows).

### 2. Durch dein Icon ersetzen

Ersetze jede ic_launcher.png-Datei durch deine neue Icon-Datei und stelle sicher, dass die neuen Icons die folgenden Anforderungen erfüllen:

- Füge Icons für jede Auflösung hinzu: hdpi, xhdpi, xxhdpi und xxxhdpi.
- Verwende ein hochwertiges Bild (vorzugsweise im PNG-Format).

**Tipp:** Du kannst auch den [**Launcher Icon Generator**](https://jgilfelt.github.io/AndroidAssetStudio/icons-launcher.html) verwenden (Hinweis: WebViewGold steht in keiner Verbindung zum Entwickler des Tools).

Verschiedene Geräte zeigen quadratische oder runde Icons an. Daher musst du Folgendes einschließen:

- 'ic_launcher.png': Wird auf Geräten mit quadratischen Icons verwendet.
- 'ic_launcher_round.png' und 'ic_launcher_foreground.png': Werden auf Geräten mit runden Icons verwendet.

![Android-Icon rund vs. eckig](../../assets/android/img/roundvsboxicon.webp)

Lege alle drei Dateien in die entsprechenden mipmap-Ordner für jede Auflösung (mipmap-hdpi, mipmap-xhdpi, mipmap-xxhdpi und mipmap-xxxhdpi).

Das Video erklärt ausführlich den Vorgang zum Ändern des Icons deiner neuen App sowie einige Empfehlungen zu dessen Erstellung.

[![Video ansehen: App-Icon](https://img.youtube.com/vi/TDDH_yaZxoI/hqdefault.jpg)](https://www.youtube.com/watch?v=TDDH_yaZxoI)

---

## Weiterlesen

- ← Vorherige: [WebViewGold konfigurieren](setup.md)
- Weiter →: [Splash Screen](splash-screen.md)
- Dieselbe Funktion auf anderen Plattformen: [iOS – Name, Icon & Splash](../ios/app-name-icon-splash.md) · [macOS – App-Symbol](../macos/app-icon.md)
- Sprachen: [🇺🇸 English](../../android/app-icon.md) · **🇩🇪 Deutsch** · [🇫🇷 Français](../../fr/android/app-icon.md) · [🇪🇸 Español](../../es/android/app-icon.md) · [🇨🇳 中文](../../zh/android/app-icon.md)

> [!TIP]
> **Zu wenig Zeit? Wir richten deine App für dich ein.** Unser Team konfiguriert, erstellt & reicht deine WebViewGold-App ein – schlüsselfertig, mit schneller Bearbeitung, Made in Germany. [App einrichten lassen →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_android_doc_online)
>
> **Im Browser erstellen:** Kein Mac, keine IDE: Der **WebViewGold Cloud Builder** konfiguriert, erstellt & lädt deine App online hoch. [Cloud Builder entdecken →](https://www.webviewgold.com/cloud-builder?ref=android_docs)
