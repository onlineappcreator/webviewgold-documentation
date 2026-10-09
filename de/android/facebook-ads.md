---
title: "Facebook Audience Network Ads-API – WebViewGold für Android Dokumentation"
description: "Zeige Banner- und Interstitial-Anzeigen des Facebook Audience Network in deiner WebViewGold-Android-App an."
lang: "de"
product: "WebViewGold für Android"
platform: "Android"
category: "APIs & Funktionen"
slug: "facebook-ads"
canonical_url: "https://www.webviewgold.com/de/docs/android/facebook-ads/"
keywords:
  - "Facebook-Ads-API"
  - "WebViewGold für Android"
  - "Website in App umwandeln"
  - "WebView-App-Dokumentation"
  - "Android WebView SDK"
  - "PWA zu App"
  - "HTML zu App"
  - "JavaScript-Bridge"
last_updated: "2026-10-09"
---

# Facebook Audience Network Ads-API – WebViewGold für Android

> **Zusammenfassung:** Zeige Banner- und Interstitial-Anzeigen des Facebook Audience Network in deiner WebViewGold-Android-App an.

[Dokumentation](../README.md) › [WebViewGold für Android](README.md) › Facebook-Ads-API

**Plattform:** Android · **Kategorie:** APIs & Funktionen · **Online-Version:** [www.webviewgold.com/de/docs/android/facebook-ads/](https://www.webviewgold.com/de/docs/android/facebook-ads/)

---

Das Facebook Audience Network ermöglicht es Entwicklern mobiler Apps, iOS- und Android-Anwendungen durch die Anzeige von Werbung zu monetarisieren. Über WebViewGold kannst du Facebook-Anzeigen problemlos in deine WebView-basierte Android-App einbinden, um durch Klicks (CPC) und Impressionen (CPM) Einnahmen zu erzielen.

## Schritt 1: Öffne die Config.java-Datei

- Öffne zunächst die **Config.java**-Datei deiner App, um die Audience-Network-Einstellungen zu konfigurieren.

## Schritt 2: Facebook-Audience-Network-Anzeigen aktivieren

1. **Erforderliche Konfigurationsvariablen aktivieren:**
   - Setze die folgenden Variablen in Config.java auf `true`:
     - `USE_FACEBOOK_ADS` stellt die App so ein, dass sie Facebook-Audience-Network-Anzeigen anstelle von AdMob-Anzeigen verwendet.
     - `SHOW_BANNER_AD` aktiviert Banner-Anzeigen für deine App.
     - `SHOW_FULLSCREEN_AD` aktiviert Vollbild-Interstitial-Anzeigen für deine App.
   - Setze `SHOW_AD_AFTER_X` auf die gewünschte Anzahl von Website-Klicks, nach der eine Interstitial-Anzeige angezeigt werden soll.

2. **Gib deine Facebook-Anzeigen-IDs ein:**
   - Gehe zu `strings.xml` und füge deine eindeutigen Facebook-Anzeigen-IDs in die entsprechenden Felder ein.

Nachdem du die oben genannten Einstellungen konfiguriert und deine Anzeigen-IDs bestätigt hast, ist deine App nun bereit für die Veröffentlichung mit aktivierten Facebook-Audience-Network-Anzeigen.

Weitere Einzelheiten findest du auch in der [offiziellen Facebook-Audience-Network-Dokumentation](https://developers.facebook.com/docs/audience-network) für zusätzliche Einrichtungs- oder Optimierungstipps, die speziell auf deine Werbestrategie zugeschnitten sind.

[![Video ansehen: Facebook Audience Network Ads-API](https://img.youtube.com/vi/81wCzuFttic/hqdefault.jpg)](https://www.youtube.com/watch?v=81wCzuFttic)

Du kannst die Sichtbarkeit der Anzeigen für einen Nutzer auch **dynamisch** steuern, indem du die folgenden benutzerdefinierten URL-Schemata von deiner Website oder App aus aufrufst:

- `enableads://` – Legt fest, dass dem aktuellen Nutzer wieder Anzeigen angezeigt werden
- `disableads://` – Deaktiviert Anzeigen dauerhaft für den aktuellen Nutzer

```html
<a href="enableads://">Enable Ads</a>
<a href="disableads://">Disable Ads</a>
```

---

## Weiterlesen

- ← Vorherige: [AdMob-Ads-API](admob.md)
- Weiter →: [Datei-Downloader-API](file-downloader.md)
- Dieselbe Funktion auf anderen Plattformen: [iOS – Facebook-Ads-API](../ios/facebook-ads.md)
- Sprachen: [🇺🇸 English](../../android/facebook-ads.md) · **🇩🇪 Deutsch** · [🇫🇷 Français](../../fr/android/facebook-ads.md) · [🇪🇸 Español](../../es/android/facebook-ads.md) · [🇨🇳 中文](../../zh/android/facebook-ads.md)

> [!TIP]
> **Zu wenig Zeit? Wir richten deine App für dich ein.** Unser Team konfiguriert, erstellt & reicht deine WebViewGold-App ein – schlüsselfertig, mit schneller Bearbeitung, Made in Germany. [App einrichten lassen →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_android_doc_online)
>
> **Im Browser erstellen:** Kein Mac, keine IDE: Der **WebViewGold Cloud Builder** konfiguriert, erstellt & lädt deine App online hoch. [Cloud Builder entdecken →](https://www.webviewgold.com/cloud-builder?ref=android_docs)
