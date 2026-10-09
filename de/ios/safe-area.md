---
title: "Größe der Safe Area anpassen – WebViewGold für iOS Dokumentation"
description: "Passe die Safe Area an und aktiviere die individuelle untere Leiste, damit deine Web-App auf iPhones mit Home-Leiste perfekt aussieht."
lang: "de"
product: "WebViewGold für iOS"
platform: "iOS"
category: "App-Design"
slug: "safe-area"
canonical_url: "https://www.webviewgold.com/de/docs/iOS/safe-area/"
keywords:
  - "Safe Area anpassen"
  - "WebViewGold für iOS"
  - "Website in App umwandeln"
  - "WebView-App-Dokumentation"
  - "iOS WebView SDK"
  - "PWA zu App"
  - "HTML zu App"
  - "JavaScript-Bridge"
last_updated: "2026-10-09"
---

# Größe der Safe Area anpassen – WebViewGold für iOS

> **Zusammenfassung:** Passe die Safe Area an und aktiviere die individuelle untere Leiste, damit deine Web-App auf iPhones mit Home-Leiste perfekt aussieht.

[Dokumentation](../README.md) › [WebViewGold für iOS](README.md) › Safe Area anpassen

**Plattform:** iOS · **Kategorie:** App-Design · **Online-Version:** [www.webviewgold.com/de/docs/iOS/safe-area/](https://www.webviewgold.com/de/docs/iOS/safe-area/)

---

Der Wechsel vom iPhone 8 zum iPhone X und darüber hinaus hat in der mobilen Branche in Bezug auf die Benutzeroberfläche vieles verändert: Der Home-Button wurde entfernt und die Home-Leiste eingeführt. Je nach Design deiner Web-App kann die untere Menüleiste auf Geräten mit Home-Leiste aufgrund der geänderten Standard-Safe-Area falsch positioniert sein (und Inhalte überlagern).\
Die gute Nachricht: WebViewGold bietet eine Funktion, mit der du eine **bottombar** aktivieren und deren Farbe an dein App-Design anpassen kannst. Da das Problem der Überlagerung von App-Inhalten durch die Home-Leiste auf iPads (aufgrund des größeren Bildschirms und eines möglicherweise anderen Layouts) möglicherweise nicht auftritt, gibt es zudem eine Option, die Funktion auf iPads zu deaktivieren.\
Um diese Funktion zu implementieren, verwende die folgenden Variablen in **Config.swift** unter der Überschrift „Custom Bottom Bar Design“. Stelle sicher, dass du **bottombar** auf **true** setzt.\
![Config-Variablen der Bottom-Bar-Funktion](../../assets/ios/img/bottombar_config.webp)\
**Erweitert:** Anstatt die Bottombar-Funktion zu verwenden, kannst du in der Datei **WebViewController.swift** nach diesem Code-Snippet-Abschnitt suchen *(drücke **CMD+F** und gib „*`switch UIDevice.current.userInterfaceIdiom`*“ ein)*, in dem du den Randwert 20 auf einen gewünschten Wert wie 10, 30 usw. ändern kannst, wie unten dargestellt:\
![Safe Area in WebView-Apps auf iPhone X/XS/XS Max anpassen](../../assets/ios/img/edgeinsets.webp)

---

## Weiterlesen

- ← Vorherige: [Name, Icon & Splash](app-name-icon-splash.md)
- Weiter →: [Geolocation-API](geolocation.md)
- Sprachen: [🇺🇸 English](../../ios/safe-area.md) · **🇩🇪 Deutsch** · [🇫🇷 Français](../../fr/ios/safe-area.md) · [🇪🇸 Español](../../es/ios/safe-area.md) · [🇨🇳 中文](../../zh/ios/safe-area.md)

> [!TIP]
> **Zu wenig Zeit? Wir richten deine App für dich ein.** Unser Team konfiguriert, erstellt & reicht deine WebViewGold-App ein – schlüsselfertig, mit schneller Bearbeitung, Made in Germany. [App einrichten lassen →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **Im Browser erstellen:** Kein Mac, keine IDE: Der **WebViewGold Cloud Builder** konfiguriert, erstellt & lädt deine App online hoch. [Cloud Builder entdecken →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
