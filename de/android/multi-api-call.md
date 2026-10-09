---
title: "Multi API Call (multiapicall://) – WebViewGold für Android Dokumentation"
description: "Rufe mehrere WebViewGold-Daten-APIs in einer einzigen window.location.href-Zuweisung auf – ideal für plattformübergreifende Web-Apps, die auch die iOS-Version nutzen."
lang: "de"
product: "WebViewGold für Android"
platform: "Android"
category: "APIs & Funktionen"
slug: "multi-api-call"
canonical_url: "https://www.webviewgold.com/de/docs/android/multi-api-call/"
keywords:
  - "Multi API Call"
  - "WebViewGold für Android"
  - "Website in App umwandeln"
  - "WebView-App-Dokumentation"
  - "Android WebView SDK"
  - "PWA zu App"
  - "HTML zu App"
  - "JavaScript-Bridge"
last_updated: "2026-10-09"
---

# Multi API Call (multiapicall://) – WebViewGold für Android

> **Zusammenfassung:** Rufe mehrere WebViewGold-Daten-APIs in einer einzigen window.location.href-Zuweisung auf – ideal für plattformübergreifende Web-Apps, die auch die iOS-Version nutzen.

[Dokumentation](../README.md) › [WebViewGold für Android](README.md) › Multi API Call

**Plattform:** Android · **Kategorie:** APIs & Funktionen · **Online-Version:** [www.webviewgold.com/de/docs/android/multi-api-call/](https://www.webviewgold.com/de/docs/android/multi-api-call/)

---

Mit dem **Multi-API-Call-Feature** löst du **mehrere WebViewGold-APIs in einer einzigen *window.location.href*-Zuweisung** aus. Das ist besonders für **plattformübergreifende Web-Apps** nützlich: Apple-basierte Browser verarbeiten mehrere Seiten-Redirects im selben Script anders als Android – *window.location.href = "exampleAPItrigger"* mehrfach im selben Script aufzurufen funktioniert auf Android, aber nicht auf iOS. Mit `multiapicall://` läuft derselbe Web-Code auf beiden Plattformen.

## Unterstützte APIs als Einträge

- [get-uuid](uuid.md)
- [getonesignalplayerid](push-notifications.md)
- [getappversion](app-version-check.md)
- [statusbarcolor](dynamic-ui.md) (gefolgt von drei Einträgen für die RGB-Werte)
- [statusbartextcolor](dynamic-ui.md) (gefolgt von einem Eintrag: `black` oder `white`)
- [bottombarcolor](dynamic-ui.md) (gefolgt von drei Einträgen für die RGB-Werte)
- [navbartextcolor](dynamic-ui.md) (gefolgt von einem Eintrag: `black` oder `white`)

## So verwendest du die Funktion

Trenne die API-Namen (und ggf. deren Werte) durch Kommas (`,`) – **ohne Leerzeichen**:

```html
<script>
// Beispielkombination: "getonesignalplayerid" und "getappversion"
window.location.href = "multiapicall://getonesignalplayerid,getappversion";
</script>
```

Werte an die Dynamic-UI-APIs übergibst du so:

```html
<script>
// Statusleiste rot färben, Textfarbe auf Weiß setzen und die UUID abrufen – alles in einem Aufruf
window.location.href = "multiapicall://statusbarcolor,255,0,0,statusbartextcolor,white,get-uuid";
</script>
```

**Hinweis:** Auf Android funktioniert es auch, die einzelnen APIs nacheinander aufzurufen (z. B. `window.location.href = "get-uuid://";` gefolgt von `window.location.href = "getappversion://";`). Verwende `multiapicall://`, wenn du einen gemeinsamen Code-Pfad mit der [iOS-Version von WebViewGold](../ios/multi-api-call.md) teilen möchtest.

Klicke [hier](https://webviewgoldtest.github.io/multiAPI.html), um eine Demo-Webseite für dieses Feature zu sehen. Untersuche die Seite, um den Beispielcode einzusehen.

---

## Weiterlesen

- ← Vorherige: [Eigene CSS- & JS-API](custom-css-js.md)
- Weiter →: [Geolocation-API](geolocation.md)
- Dieselbe Funktion auf anderen Plattformen: [iOS – MultiAPICall-Funktion](../ios/multi-api-call.md)
- Sprachen: [🇺🇸 English](../../android/multi-api-call.md) · **🇩🇪 Deutsch** · [🇫🇷 Français](../../fr/android/multi-api-call.md) · [🇪🇸 Español](../../es/android/multi-api-call.md) · [🇨🇳 中文](../../zh/android/multi-api-call.md)

> [!TIP]
> **Zu wenig Zeit? Wir richten deine App für dich ein.** Unser Team konfiguriert, erstellt & reicht deine WebViewGold-App ein – schlüsselfertig, mit schneller Bearbeitung, Made in Germany. [App einrichten lassen →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_android_doc_online)
>
> **Im Browser erstellen:** Kein Mac, keine IDE: Der **WebViewGold Cloud Builder** konfiguriert, erstellt & lädt deine App online hoch. [Cloud Builder entdecken →](https://www.webviewgold.com/cloud-builder?ref=android_docs)
