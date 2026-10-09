---
title: "App-Versionsprüfung-API – WebViewGold für Android Dokumentation"
description: "Erkenne die installierte App-Version aus deiner Web-App und fordere Nutzer bei Bedarf zum Update auf."
lang: "de"
product: "WebViewGold für Android"
platform: "Android"
category: "APIs & Funktionen"
slug: "app-version-check"
canonical_url: "https://www.webviewgold.com/de/docs/android/app-version-check/"
keywords:
  - "App-Versionsprüfung-API"
  - "WebViewGold für Android"
  - "Website in App umwandeln"
  - "WebView-App-Dokumentation"
  - "Android WebView SDK"
  - "PWA zu App"
  - "HTML zu App"
  - "JavaScript-Bridge"
last_updated: "2026-10-09"
---

# App-Versionsprüfung-API – WebViewGold für Android

> **Zusammenfassung:** Erkenne die installierte App-Version aus deiner Web-App und fordere Nutzer bei Bedarf zum Update auf.

[Dokumentation](../README.md) › [WebViewGold für Android](README.md) › App-Versionsprüfung-API

**Plattform:** Android · **Kategorie:** APIs & Funktionen · **Online-Version:** [www.webviewgold.com/de/docs/android/app-version-check/](https://www.webviewgold.com/de/docs/android/app-version-check/)

---

Mit dieser WebViewGold App Version Check API kann deine Website/Web-App **die Version der Android-App abrufen**, die von deinem Android-App-Nutzer verwendet wird. Diese API ist besonders hilfreich, wenn du Nutzer einer älteren Version darüber informieren möchtest, ihre App zu aktualisieren. Darüber hinaus kannst du Bereiche der Web-App ausblenden, die App-Funktionen erfordern, welche erst ab einer bestimmten App-Version unterstützt werden.\
Verwende JavaScript mit einer solchen URL, um die App-Version und die App-Bundle-Nummer auszulesen und per Alert anzuzeigen:

```html
<script>
window.location.href = "getappversion://";
alert(versionNumber);
alert(bundleNumber);
</script>
```

**Alternativ kannst du  `AUTO_INJECT_VARIABLES`  in Config.java auf `true` setzen, um diesen (und andere) Werte automatisch in JavaScript einzufügen, ohne zuvor eine URL aufrufen zu müssen.**

---

## Weiterlesen

- ← Vorherige: [Screenshot-API](take-screenshot.md)
- Weiter →: [Kontakte-API](contacts.md)
- Dieselbe Funktion auf anderen Plattformen: [iOS – App-Versionsprüfung-API](../ios/app-version-check.md)
- Sprachen: [🇺🇸 English](../../android/app-version-check.md) · **🇩🇪 Deutsch** · [🇫🇷 Français](../../fr/android/app-version-check.md) · [🇪🇸 Español](../../es/android/app-version-check.md) · [🇨🇳 中文](../../zh/android/app-version-check.md)

> [!TIP]
> **Zu wenig Zeit? Wir richten deine App für dich ein.** Unser Team konfiguriert, erstellt & reicht deine WebViewGold-App ein – schlüsselfertig, mit schneller Bearbeitung, Made in Germany. [App einrichten lassen →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_android_doc_online)
>
> **Im Browser erstellen:** Kein Mac, keine IDE: Der **WebViewGold Cloud Builder** konfiguriert, erstellt & lädt deine App online hoch. [Cloud Builder entdecken →](https://www.webviewgold.com/cloud-builder?ref=android_docs)
