---
title: "AdMob-Ads-API – WebViewGold für iOS Dokumentation"
description: "Monetarisiere deine iOS-App mit Google-AdMob-Banner-, Interstitial- und Rewarded-Anzeigen – Konfiguration und JavaScript-Trigger."
lang: "de"
product: "WebViewGold für iOS"
platform: "iOS"
category: "APIs & Funktionen"
slug: "admob"
canonical_url: "https://www.webviewgold.com/de/docs/iOS/admob/"
keywords:
  - "AdMob-Ads-API"
  - "WebViewGold für iOS"
  - "Website in App umwandeln"
  - "WebView-App-Dokumentation"
  - "iOS WebView SDK"
  - "PWA zu App"
  - "HTML zu App"
  - "JavaScript-Bridge"
last_updated: "2026-10-09"
---

# AdMob-Ads-API – WebViewGold für iOS

> **Zusammenfassung:** Monetarisiere deine iOS-App mit Google-AdMob-Banner-, Interstitial- und Rewarded-Anzeigen – Konfiguration und JavaScript-Trigger.

[Dokumentation](../README.md) › [WebViewGold für iOS](README.md) › AdMob-Ads-API

**Plattform:** iOS · **Kategorie:** APIs & Funktionen · **Online-Version:** [www.webviewgold.com/de/docs/iOS/admob/](https://www.webviewgold.com/de/docs/iOS/admob/)

---

AdMob ist ein Google-Dienst zur Monetarisierung mobiler Apps auf iOS- und Android-Plattformen. Er ermöglicht Entwicklern die Integration von Banner-, Interstitial- und belohnten Anzeigen, die pro Klick (CPC, Cost-per-Click) oder pro Impression (CPM, Cost-per-Mille) vergütet werden. WebViewGold vereinfacht die AdMob-Integration und ermöglicht eine schnelle Einrichtung für die Anzeige von Werbung in deiner WebView-basierten iOS-Anwendung.

[![Video ansehen: AdMob-Ads-API](https://img.youtube.com/vi/7j7NW5CTwqo/hqdefault.jpg)](https://www.youtube.com/watch?v=7j7NW5CTwqo)

**Schritt 1:** Öffne die Datei **Info.plist** und trage deine globale AdMob-Konto-ID im Feld *GADApplicationIdentifier* ein:\
![Füge deine AdMob-Konto-ID zum Projekt hinzu](../../assets/ios/img/admobglobal.webp)

**Schritt 2:** Bitte füge deine AdMob-IDs in der **Config.swift** für `AdmobBannerID`, `AdmobinterstitialID` und `AdmobRewardedID` ein:\
![Aktiviere bestimmte AdMob-Bannerblöcke in deiner Anwendung](../../assets/ios/img/admobconstants.webp)

**Schritt 3:** In der **Config.swift** kannst du:

- **Aktiviere oder deaktiviere** Banner- und/oder Interstitial-Anzeigen, indem du `showBannerAd` für Banneranzeigen auf `true` und `showFullScreenAd` für Interstitial-Anzeigen auf `true` setzt.
- **Definiere Intervalle** für die Anzeige von Interstitial-Anzeigen, indem du `showadAfterX` auf die gewünschte Anzahl von Website-Interaktionen änderst, bevor eine Interstitial-Anzeige abgespielt wird.

**So aktivierst du belohnte Anzeigen** *(nur verfügbar für iOS-Versionen höher als 13.0)***:** Setze `enableRewardedAds` auf `true`.

Um eine belohnte Anzeige abzuspielen, rufe unsere API-Funktion für belohnte Anzeigen auf.

```html
<a href="displayrewardedad://>Display Rewarded Advertisement</a>
```

Nach dem vollständigen Ansehen einer Anzeige wird an deine Website ein Aufruf der JavaScript-Funktion **updateRewardedStatus('true');** gesendet. Diese Funktion musst du selbst in deinem JavaScript-Code implementieren, da es dir überlassen bleibt, wie du den Benutzer belohnen möchtest.

WebViewGold unterstützt die Anzeige belohnter Anzeigen als Standard-Werbeoption und überschreibt damit die Interstitial-Optionen. Damit dies geschieht, setze `useRewardedAdsWherePossible` und `showFullScreenAd` auf `true`.

**Tipp:** Wenn du Interstitial-Anzeigen nach X Taps anzeigst (`incrementWithTaps` auf `true`), kannst du den Tap-Zähler auch manuell aus deiner Web-App erhöhen, indem du `increasetapcounter://` aufrufst — nützlich, um nur bestimmte Interaktionen für das Anzeigenintervall zu zählen.

*Weitere Informationen findest du auch in der [offiziellen AdMob-SDK-Dokumentation](https://developers.google.com/admob/) (überspringe jedoch die Einrichtungsschritte, da WebViewGold das Framework bereits enthält).*

---

## Weiterlesen

- ← Vorherige: [Push-Benachrichtigungen-API](push-notifications.md)
- Weiter →: [Facebook-Ads-API](facebook-ads.md)
- Dieselbe Funktion auf anderen Plattformen: [Android – AdMob-Ads-API](../android/admob.md)
- Sprachen: [🇺🇸 English](../../ios/admob.md) · **🇩🇪 Deutsch** · [🇫🇷 Français](../../fr/ios/admob.md) · [🇪🇸 Español](../../es/ios/admob.md) · [🇨🇳 中文](../../zh/ios/admob.md)

> [!TIP]
> **Zu wenig Zeit? Wir richten deine App für dich ein.** Unser Team konfiguriert, erstellt & reicht deine WebViewGold-App ein – schlüsselfertig, mit schneller Bearbeitung, Made in Germany. [App einrichten lassen →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **Im Browser erstellen:** Kein Mac, keine IDE: Der **WebViewGold Cloud Builder** konfiguriert, erstellt & lädt deine App online hoch. [Cloud Builder entdecken →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
