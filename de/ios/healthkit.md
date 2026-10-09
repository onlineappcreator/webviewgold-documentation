---
title: "HealthKit-Plugin – WebViewGold für iOS Dokumentation"
description: "Verbinde deine Web-App mit Apple HealthKit und lies Gesundheitsdaten mit Nutzerberechtigung auf iOS."
lang: "de"
product: "WebViewGold für iOS"
platform: "iOS"
category: "Erweiterungen & Plugins"
slug: "healthkit"
canonical_url: "https://www.webviewgold.com/de/docs/iOS/healthkit/"
keywords:
  - "HealthKit-Plugin"
  - "WebViewGold für iOS"
  - "Website in App umwandeln"
  - "WebView-App-Dokumentation"
  - "iOS WebView SDK"
  - "PWA zu App"
  - "HTML zu App"
  - "JavaScript-Bridge"
last_updated: "2026-10-09"
---

# HealthKit-Plugin – WebViewGold für iOS

> **Zusammenfassung:** Verbinde deine Web-App mit Apple HealthKit und lies Gesundheitsdaten mit Nutzerberechtigung auf iOS.

[Dokumentation](../README.md) › [WebViewGold für iOS](README.md) › HealthKit-Plugin

**Plattform:** iOS · **Kategorie:** Erweiterungen & Plugins · **Online-Version:** [www.webviewgold.com/de/docs/iOS/healthkit/](https://www.webviewgold.com/de/docs/iOS/healthkit/)

---

Aktiviere die HealthKit-Funktionen, indem du `static let HealthKitEnabled` in `Config.swift` auf deinen Plugin-Token setzt und die HealthKit-Capability hinzufügst.\
Wende dich für Details an [webviewgold-healthkit@onlineappcreator.com](mailto:webviewgold-healthkit@onlineappcreator.com).

## API-Verwendung (nach Aktivierung)

**Lies** einen HealthKit-Wert, indem du `readhealthkit://` gefolgt von einem [HealthKit-Identifier](https://developer.apple.com/documentation/healthkit/hkquantitytypeidentifier) aufrufst. Das Ergebnis wird als JavaScript-Variable mit dem Namen des Identifiers in deine Web-App injiziert (Wert und Einheit als String):

```html
<a href="readhealthkit://HKQuantityTypeIdentifierStepCount" onclick="setTimeout(function(){ alert(HKQuantityTypeIdentifierStepCount); }, 500)">Schrittzahl lesen</a>
```

**Schreibe** einen HealthKit-Wert mit der Syntax `writehealthkit://Identifier//Wert`:

```html
<a href="writehealthkit://HKQuantityTypeIdentifierStepCount//100">100 Schritte speichern</a>
```

**Hinweis:** Erfordert die HealthKit-Capability sowie die Einträge *Privacy - Health Share Usage Description* / *Privacy - Health Update Usage Description* in der **Info.plist**.

---

## Weiterlesen

- ← Vorherige: [Siri-Plugin](siri.md)
- Weiter →: [Erstellen & Veröffentlichen](publish.md)
- Dieselbe Funktion auf anderen Plattformen: [Android – Health Connect API](../android/health-connect.md)
- Sprachen: [🇺🇸 English](../../ios/healthkit.md) · **🇩🇪 Deutsch** · [🇫🇷 Français](../../fr/ios/healthkit.md) · [🇪🇸 Español](../../es/ios/healthkit.md) · [🇨🇳 中文](../../zh/ios/healthkit.md)

> [!TIP]
> **Zu wenig Zeit? Wir richten deine App für dich ein.** Unser Team konfiguriert, erstellt & reicht deine WebViewGold-App ein – schlüsselfertig, mit schneller Bearbeitung, Made in Germany. [App einrichten lassen →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **Im Browser erstellen:** Kein Mac, keine IDE: Der **WebViewGold Cloud Builder** konfiguriert, erstellt & lädt deine App online hoch. [Cloud Builder entdecken →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
