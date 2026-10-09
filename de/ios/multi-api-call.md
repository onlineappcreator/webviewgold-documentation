---
title: "MultiAPICall-Funktion – WebViewGold für iOS Dokumentation"
description: "Verkette mehrere WebViewGold-API-Aufrufe in einer einzigen Anfrage mit der MultiAPICall-Funktion für iOS."
lang: "de"
product: "WebViewGold für iOS"
platform: "iOS"
category: "Erweiterungen & Plugins"
slug: "multi-api-call"
canonical_url: "https://www.webviewgold.com/de/docs/iOS/multi-api-call/"
keywords:
  - "MultiAPICall-Funktion"
  - "WebViewGold für iOS"
  - "Website in App umwandeln"
  - "WebView-App-Dokumentation"
  - "iOS WebView SDK"
  - "PWA zu App"
  - "HTML zu App"
  - "JavaScript-Bridge"
last_updated: "2026-10-09"
---

# MultiAPICall-Funktion – WebViewGold für iOS

> **Zusammenfassung:** Verkette mehrere WebViewGold-API-Aufrufe in einer einzigen Anfrage mit der MultiAPICall-Funktion für iOS.

[Dokumentation](../README.md) › [WebViewGold für iOS](README.md) › MultiAPICall-Funktion

**Plattform:** iOS · **Kategorie:** Erweiterungen & Plugins · **Online-Version:** [www.webviewgold.com/de/docs/iOS/multi-api-call/](https://www.webviewgold.com/de/docs/iOS/multi-api-call/)

---

Dies ist eine **optionale Funktion für iOS**, da Apple-basierte Browser mehrere Seiten-Reloads desselben Skripts anders verarbeiten als Android-basierte Browser.
Das bedeutet, dass ein mehrfacher Aufruf von *window.location.href = "exampleAPItrigger"* im selben Webseiten-Skript auf iOS – anders als auf Android – nicht funktioniert.\
Die MultiAPICall-Funktion **ermöglicht es dir, mehrere APIs in einer einzigen *window.location.href*-Zuweisung aufzurufen**, und zwar am Ende deines Webseiten-Skripts. Das kann nützlich sein, wenn du mehr als eine Datenfunktion aus der App vorladen möchtest, um sie auf einer Seite bereitzuhalten.\
**MultiAPICall unterstützt die folgenden Datenerfassungs-APIs als Einträge:**
"[get-uuid](uuid.md)", "[user-disable-tracking](user-tracking.md)", "[getonesignalplayerid](push-notifications.md#getonesignalid)", "[getappversion](app-version-check.md)", "[__haptics (light, medium, heavy, success, warning, error)](haptic-feedback.md)"\
Verwende JavaScript mit dieser Art von URL, um mehrere APIs gleichzeitig aufzurufen (**stelle sicher, dass eine Prüfung enthalten ist, damit die Funktion nur auf der iOS-Plattform verwendet wird**):

```html
<script>
// Example combination: "getonesignalplayerid" and "getappversion"

if (getMobileOperatingSystem() == "iOS") {
    // iOS: Use MultiAPICall feature, separate API names by commas (","), NO spaces
    window.location.href = "multiapicall://getonesignalplayerid,getappversion";
} else {
    // Android: Can handle multiple calls at once, use normal API call structure
    window.location.href = "getonesignalplayerid://";
    window.location.href = "getappversion://";
}
</script>
```

Klicke [hier](https://webviewgoldtest.github.io/multiAPI.html), um eine Demonstrations-Webseite für diese Funktion anzusehen. Untersuche die Seite, um den Beispielcode einzusehen.

---

## Weiterlesen

- ← Vorherige: [Bildschirmaufnahme-Erkennung](screen-capture.md)
- Weiter →: [NFC-Plugin](nfc.md)
- Dieselbe Funktion auf anderen Plattformen: [Android – Multi API Call](../android/multi-api-call.md)
- Sprachen: [🇺🇸 English](../../ios/multi-api-call.md) · **🇩🇪 Deutsch** · [🇫🇷 Français](../../fr/ios/multi-api-call.md) · [🇪🇸 Español](../../es/ios/multi-api-call.md) · [🇨🇳 中文](../../zh/ios/multi-api-call.md)

> [!TIP]
> **Zu wenig Zeit? Wir richten deine App für dich ein.** Unser Team konfiguriert, erstellt & reicht deine WebViewGold-App ein – schlüsselfertig, mit schneller Bearbeitung, Made in Germany. [App einrichten lassen →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **Im Browser erstellen:** Kein Mac, keine IDE: Der **WebViewGold Cloud Builder** konfiguriert, erstellt & lädt deine App online hoch. [Cloud Builder entdecken →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
