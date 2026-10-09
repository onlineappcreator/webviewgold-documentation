---
title: "Siri-Plugin – WebViewGold für iOS Dokumentation"
description: "Füge deiner iOS-WebView-App Unterstützung für Siri Shortcuts hinzu und öffne App-Inhalte per Sprache."
lang: "de"
product: "WebViewGold für iOS"
platform: "iOS"
category: "Erweiterungen & Plugins"
slug: "siri"
canonical_url: "https://www.webviewgold.com/de/docs/iOS/siri/"
keywords:
  - "Siri-Plugin"
  - "WebViewGold für iOS"
  - "Website in App umwandeln"
  - "WebView-App-Dokumentation"
  - "iOS WebView SDK"
  - "PWA zu App"
  - "HTML zu App"
  - "JavaScript-Bridge"
last_updated: "2026-10-09"
---

# Siri-Plugin – WebViewGold für iOS

> **Zusammenfassung:** Füge deiner iOS-WebView-App Unterstützung für Siri Shortcuts hinzu und öffne App-Inhalte per Sprache.

[Dokumentation](../README.md) › [WebViewGold für iOS](README.md) › Siri-Plugin

**Plattform:** iOS · **Kategorie:** Erweiterungen & Plugins · **Online-Version:** [www.webviewgold.com/de/docs/iOS/siri/](https://www.webviewgold.com/de/docs/iOS/siri/)

---

Aktiviere die Siri-Integration, indem du deinen Plugin-Token in `static let siriEnabled` in `Config.swift` einträgst und die Siri-Capability zum WebViewGold-Target hinzufügst.\
Wende dich für weitere Informationen an [webviewgold-siri@onlineappcreator.com](mailto:webviewgold-siri@onlineappcreator.com).

## So implementierst du die Siri-Funktionalität

1. Erstelle eine JavaScript-Funktion, die Siri auslösen soll:

```javascript
function playRadio() {
   // Add desired functionality
}
```

2. Füge einen Button oder Link hinzu, um den Siri-Befehl zu registrieren (vermeide Formulierungen wie „Open“, die Siri verwirren könnten):

```html
<a href="addtosiri://?command=Play%20Radio&jsFunction=playRadio()">Add Play Radio to Siri</a>
```

Der Parameter `command` liefert die empfohlene Sprachphrase, während `jsFunction` die auszuführende JavaScript-Funktion angibt.

---

## Weiterlesen

- ← Vorherige: [NFC-Plugin](nfc.md)
- Weiter →: [HealthKit-Plugin](healthkit.md)
- Sprachen: [🇺🇸 English](../../ios/siri.md) · **🇩🇪 Deutsch** · [🇫🇷 Français](../../fr/ios/siri.md) · [🇪🇸 Español](../../es/ios/siri.md) · [🇨🇳 中文](../../zh/ios/siri.md)

> [!TIP]
> **Zu wenig Zeit? Wir richten deine App für dich ein.** Unser Team konfiguriert, erstellt & reicht deine WebViewGold-App ein – schlüsselfertig, mit schneller Bearbeitung, Made in Germany. [App einrichten lassen →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **Im Browser erstellen:** Kein Mac, keine IDE: Der **WebViewGold Cloud Builder** konfiguriert, erstellt & lädt deine App online hoch. [Cloud Builder entdecken →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
