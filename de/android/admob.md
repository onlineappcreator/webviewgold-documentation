---
title: "AdMob-Ads-API – WebViewGold für Android Dokumentation"
description: "Monetarisiere deine Android-App mit Google-AdMob-Banner- und Interstitial-Anzeigen — Konfiguration und JavaScript-Trigger."
lang: "de"
product: "WebViewGold für Android"
platform: "Android"
category: "APIs & Funktionen"
slug: "admob"
canonical_url: "https://www.webviewgold.com/de/docs/android/admob/"
keywords:
  - "AdMob-Ads-API"
  - "WebViewGold für Android"
  - "Website in App umwandeln"
  - "WebView-App-Dokumentation"
  - "Android WebView SDK"
  - "PWA zu App"
  - "HTML zu App"
  - "JavaScript-Bridge"
last_updated: "2026-10-09"
---

# AdMob-Ads-API – WebViewGold für Android

> **Zusammenfassung:** Monetarisiere deine Android-App mit Google-AdMob-Banner- und Interstitial-Anzeigen — Konfiguration und JavaScript-Trigger.

[Dokumentation](../README.md) › [WebViewGold für Android](README.md) › AdMob-Ads-API

**Plattform:** Android · **Kategorie:** APIs & Funktionen · **Online-Version:** [www.webviewgold.com/de/docs/android/admob/](https://www.webviewgold.com/de/docs/android/admob/)

---

AdMob ist ein Google-Dienst zur Monetarisierung mobiler Apps auf den Plattformen iOS und Android. Er ermöglicht Entwicklern die Integration von Banner-, Interstitial- und Rewarded-Anzeigen, die nach Klicks (CPC, Cost-per-Click) oder Impressionen (CPM, Cost-per-Mille) vergütet werden. WebViewGold vereinfacht die AdMob-Integration und ermöglicht eine schnelle Einrichtung zur Anzeige von Werbung in deiner WebView-basierten Android-Anwendung.

## Schritt 1: Config.java-Datei öffnen

Öffne zunächst die **Config.java**-Datei deiner App, um die Werbeeinstellungen festzulegen und die AdMob-Funktionalität zu aktivieren.

## Schritt 2: Monetarisiere deine App mit dem nativen AdMob SDK

In **Config.java** kannst du:

- Banner- und/oder Interstitial-Anzeigen **aktivieren oder deaktivieren**, indem du `SHOW_BANNER_AD` für Banner-Anzeigen auf true und `SHOW_FULL_SCREEN_AD` für Interstitial-Anzeigen auf true setzt.
- **Intervalle festlegen** für die Anzeige von Interstitial-Anzeigen, indem du `SHOW_AD_AFTER_X` auf die gewünschte Anzahl von Website-Interaktionen änderst, bevor eine Interstitial-Anzeige abgespielt wird.

**Hinweis:** Stelle vor der Veröffentlichung deiner App sicher, dass deine eindeutigen AdMob-IDs korrekt in der **strings.xml**-Datei eingetragen sind:\
![Bestimmte AdMob-Werbeblöcke in deiner App aktivieren](../../assets/android/img/admobconfig.webp)

## Schritt 3: Rewarded-Anzeigen aktivieren

- Rewarded-Anzeigen einrichten:
  - Um Rewarded-Anzeigen zu aktivieren, setze `ENABLE_REWARDED_ADS` auf `true`.
  - Verwende den folgenden Link, um eine Rewarded-Anzeige anzuzeigen

    ```html
    <a href="displayrewardedad://">Display Rewarded Advertisement</a>
    ```

  - Sobald ein Nutzer die Anzeige vollständig angesehen hat, löst WebViewGold die JavaScript-Funktion `updateRewardedStatus('true');` aus, damit du Belohnungen im Code deiner App verarbeiten kannst.
- Rewarded-Anzeigen als Standard:
  - Wenn du möchtest, dass standardmäßig Rewarded-Anzeigen angezeigt werden, setze sowohl `USE_REWARDED_ADS_WHERE_POSSIBLE` als auch `SHOW_FULL_SCREEN_AD` auf `true`. Dadurch werden Rewarded-Anzeigen gegenüber Interstitial-Anzeigen priorisiert.

## Weitere Ressourcen

Ausführlichere Optionen findest du in der [offiziellen AdMob-SDK-Dokumentation](https://developers.google.com/admob/), überspringe jedoch die Einrichtungsanweisungen, da WebViewGold das erforderliche Framework bereits enthält.

[![Video ansehen: AdMob-Ads-API](https://img.youtube.com/vi/vq5FM7n0Syg/hqdefault.jpg)](https://www.youtube.com/watch?v=vq5FM7n0Syg)

Du kannst die Sichtbarkeit der Anzeigen für einen Nutzer auch **dynamisch** steuern, indem du die folgenden benutzerdefinierten URL-Schemata von deiner Website oder App aus aufrufst:

- `enableads://` – Legt fest, dass dem aktuellen Nutzer wieder Anzeigen angezeigt werden
- `disableads://` – Deaktiviert Anzeigen dauerhaft für den aktuellen Nutzer

## <a id="appopenads"></a>Schritt 4: App Open Ads aktivieren

**App Open Ads** sind Vollbild-Anzeigen, die erscheinen, wenn der Nutzer die App öffnet (Kaltstart über den Launcher-Splash) oder aus dem Hintergrund zu ihr zurückkehrt. So aktivierst du sie:

- Setze `SHOW_APP_OPEN_AD` in **Config.java** auf `true`.
- Ersetze den Wert `admob_app_open_id` in **strings.xml** durch deine eigene AdMob-App-Open-Anzeigenblock-ID (das Template enthält die offizielle AdMob-Test-ID – ersetze sie vor der Veröffentlichung!).

**Hinweis:** App Open Ads berücksichtigen die Google-Consent-Verwaltung (`ASK_FOR_AD_CONSENT`) genauso wie die anderen AdMob-Formate.

---

## Weiterlesen

- ← Vorherige: [Push-Benachrichtigungs-API](push-notifications.md)
- Weiter →: [Facebook-Ads-API](facebook-ads.md)
- Dieselbe Funktion auf anderen Plattformen: [iOS – AdMob-Ads-API](../ios/admob.md)
- Sprachen: [🇺🇸 English](../../android/admob.md) · **🇩🇪 Deutsch** · [🇫🇷 Français](../../fr/android/admob.md) · [🇪🇸 Español](../../es/android/admob.md) · [🇨🇳 中文](../../zh/android/admob.md)

> [!TIP]
> **Zu wenig Zeit? Wir richten deine App für dich ein.** Unser Team konfiguriert, erstellt & reicht deine WebViewGold-App ein – schlüsselfertig, mit schneller Bearbeitung, Made in Germany. [App einrichten lassen →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_android_doc_online)
>
> **Im Browser erstellen:** Kein Mac, keine IDE: Der **WebViewGold Cloud Builder** konfiguriert, erstellt & lädt deine App online hoch. [Cloud Builder entdecken →](https://www.webviewgold.com/cloud-builder?ref=android_docs)
