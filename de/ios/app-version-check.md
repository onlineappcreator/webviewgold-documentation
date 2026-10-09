---
title: "App-Versionsprüfung-API – WebViewGold für iOS Dokumentation"
description: "Erkenne die installierte App-Version aus deiner Web-App und fordere Nutzer bei Bedarf zum Aktualisieren auf."
lang: "de"
product: "WebViewGold für iOS"
platform: "iOS"
category: "APIs & Funktionen"
slug: "app-version-check"
canonical_url: "https://www.webviewgold.com/de/docs/iOS/app-version-check/"
keywords:
  - "App-Versionsprüfung-API"
  - "WebViewGold für iOS"
  - "Website in App umwandeln"
  - "WebView-App-Dokumentation"
  - "iOS WebView SDK"
  - "PWA zu App"
  - "HTML zu App"
  - "JavaScript-Bridge"
last_updated: "2026-10-09"
---

# App-Versionsprüfung-API – WebViewGold für iOS

> **Zusammenfassung:** Erkenne die installierte App-Version aus deiner Web-App und fordere Nutzer bei Bedarf zum Aktualisieren auf.

[Dokumentation](../README.md) › [WebViewGold für iOS](README.md) › App-Versionsprüfung-API

**Plattform:** iOS · **Kategorie:** APIs & Funktionen · **Online-Version:** [www.webviewgold.com/de/docs/iOS/app-version-check/](https://www.webviewgold.com/de/docs/iOS/app-version-check/)

---

Mit diesem WebViewGold-JavaScript-API-Ansatz kann deine Website/Web-App die **Version der verwendeten iOS-App** abrufen, die von deinem App-Benutzer genutzt wird. Dies ist besonders hilfreich, wenn du Benutzer einer älteren Version darauf hinweisen möchtest, ihre App zu aktualisieren. Darüber hinaus kannst du Bereiche der Web-App ausblenden, die App-Funktionen erfordern, welche erst ab einer bestimmten App-Version unterstützt werden.\
Verwende JavaScript mit dieser Art von URL, um die App-Version und die App-Bundle-Nummer auszulesen und anzuzeigen:

```html
<script>
window.location.href = "getappversion://";
alert(versionNumber);
alert(bundleNumber);
</script>
```

**Alternativ kannst du in Config.swift `autoInjectVariable` auf `true` setzen, um diesen (und andere) Werte automatisch in JavaScript einzufügen, ohne zuvor eine URL aufrufen zu müssen.**

---

## Weiterlesen

- ← Vorherige: [Screenshot-erstellen-API](take-screenshot.md)
- Weiter →: [Dynamische-UI-API](dynamic-ui.md)
- Dieselbe Funktion auf anderen Plattformen: [Android – App-Versionsprüfung-API](../android/app-version-check.md)
- Sprachen: [🇺🇸 English](../../ios/app-version-check.md) · **🇩🇪 Deutsch** · [🇫🇷 Français](../../fr/ios/app-version-check.md) · [🇪🇸 Español](../../es/ios/app-version-check.md) · [🇨🇳 中文](../../zh/ios/app-version-check.md)

> [!TIP]
> **Zu wenig Zeit? Wir richten deine App für dich ein.** Unser Team konfiguriert, erstellt & reicht deine WebViewGold-App ein – schlüsselfertig, mit schneller Bearbeitung, Made in Germany. [App einrichten lassen →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **Im Browser erstellen:** Kein Mac, keine IDE: Der **WebViewGold Cloud Builder** konfiguriert, erstellt & lädt deine App online hoch. [Cloud Builder entdecken →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
