---
title: "App Links & Deep-Linking-API – WebViewGold für Android Dokumentation"
description: "Öffne Links zu deiner Domain direkt in deiner Android-App mit App Links und Deep Linking über ein eigenes URL-Schema."
lang: "de"
product: "WebViewGold für Android"
platform: "Android"
category: "APIs & Funktionen"
slug: "app-links"
canonical_url: "https://www.webviewgold.com/de/docs/android/app-links/"
keywords:
  - "App Links / Deep Linking"
  - "WebViewGold für Android"
  - "Website in App umwandeln"
  - "WebView-App-Dokumentation"
  - "Android WebView SDK"
  - "PWA zu App"
  - "HTML zu App"
  - "JavaScript-Bridge"
last_updated: "2026-10-09"
---

# App Links & Deep-Linking-API – WebViewGold für Android

> **Zusammenfassung:** Öffne Links zu deiner Domain direkt in deiner Android-App mit App Links und Deep Linking über ein eigenes URL-Schema.

[Dokumentation](../README.md) › [WebViewGold für Android](README.md) › App Links / Deep Linking

**Plattform:** Android · **Kategorie:** APIs & Funktionen · **Online-Version:** [www.webviewgold.com/de/docs/android/app-links/](https://www.webviewgold.com/de/docs/android/app-links/)

---

Die WebViewGold App Links / Deeplinking API ermöglicht es Nutzern, bestimmte Seiten in deiner App aus externen Quellen wie E-Mail, sozialen Medien oder Messaging-Apps zu öffnen.

## WebViewGold für Android unterstützt zwei Deep-Linking-Methoden

- **Standardmäßige URL-basierte Deep Links:** z. B. `https://www.example.org/subpages/example1`
- **Deep Links mit benutzerdefiniertem Schema:** z. B. `webviewgold://https://www.example.org/subpages/example2`

## Schritt 1: Konfiguriere dein Link-Schema in AndroidManifest.xml

Um standardmäßiges Deep Linking zu unterstützen, konfiguriere deine **AndroidManifest.xml**, um deine Domain mit deiner App zu verknüpfen. Ersetze `www.webviewgold.com` durch deine tatsächliche Domain (z. B. `www.example.org`):

![AndroidManifest.xml für die App-Link-Konfiguration](../../assets/android/img/applinks1.webp)

## Schritt 2: Deep Linking in Config.java aktivieren

Aktiviere in deiner **Config.java**-Datei die Deep-Linking-Funktionen:

```java
// Enables standard deep linking (https:// links)
public static final boolean IS_DEEP_LINKING_ENABLED = true;

// Enables custom scheme deep linking (e.g., webviewgold://)
public static final boolean IS_CUSTOM_SCHEME_ENABLED = true;

// Set your desired scheme prefix (must match AndroidManifest.xml)
public static final String CUSTOM_DEEPLINK_SCHEME = "webviewgold";
```

![Config.java für die App-Link-Konfiguration](../../assets/android/img/applinks2.webp)

## Schritt 3: Domain-Eigentümerschaft überprüfen (für URL-basierte Deep Links)

Um Deep Linking über HTTPS-URLs zu aktivieren, musst du die Domain-Eigentümerschaft bei Google überprüfen. Folge dem [**Google Site Verification Guide**](https://developer.android.com/training/app-links/verify-android-applinks).

## Deine App Links testen

Du kannst beide Arten von Links über Android Studio oder das Terminal testen:

- **Mit Android Studio:** Öffne den **App Links Assistant** aus dem Menü **Tools** für Simulation und Fehlerbehebung.
- **Mit Terminal oder Eingabeaufforderung:**
  1. Führe den folgenden Befehl aus:

     ```bash
     adb shell am start -a android.intent.action.VIEW -d "webviewgold://https://www.example.org/subpages/example2" com.webviewgold.myappname
     ```

     - Ersetze `com.webviewgold.myappname` durch den tatsächlichen Paketnamen deiner App.
     - Du kannst auch mit einem URL-Link wie `https://www.example.org/subpages/example1` testen.

Sobald alles eingerichtet ist, können Nutzer deine App über Deep Links wie die folgenden direkt auf einer bestimmten Seite öffnen:

- `https://www.example.org/subpages/example1`
- `webviewgold://https://www.example.org/subpages/example2`

**Fragen?** Melde dich jederzeit bei uns!

---

## Weiterlesen

- ← Vorherige: [Taschenlampen-API](flashlight.md)
- Weiter →: [ShareIntent-API](share-intent.md)
- Dieselbe Funktion auf anderen Plattformen: [iOS – Universal Links-API](../ios/universal-links.md)
- Sprachen: [🇺🇸 English](../../android/app-links.md) · **🇩🇪 Deutsch** · [🇫🇷 Français](../../fr/android/app-links.md) · [🇪🇸 Español](../../es/android/app-links.md) · [🇨🇳 中文](../../zh/android/app-links.md)

> [!TIP]
> **Zu wenig Zeit? Wir richten deine App für dich ein.** Unser Team konfiguriert, erstellt & reicht deine WebViewGold-App ein – schlüsselfertig, mit schneller Bearbeitung, Made in Germany. [App einrichten lassen →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_android_doc_online)
>
> **Im Browser erstellen:** Kein Mac, keine IDE: Der **WebViewGold Cloud Builder** konfiguriert, erstellt & lädt deine App online hoch. [Cloud Builder entdecken →](https://www.webviewgold.com/cloud-builder?ref=android_docs)
