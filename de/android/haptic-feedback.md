---
title: "Haptisches-Feedback-API – WebViewGold für Android Dokumentation"
description: "Löse natives Vibrations-Feedback aus deiner Web-App aus — für ein natives App-Gefühl unter Android."
lang: "de"
product: "WebViewGold für Android"
platform: "Android"
category: "APIs & Funktionen"
slug: "haptic-feedback"
canonical_url: "https://www.webviewgold.com/de/docs/android/haptic-feedback/"
keywords:
  - "Haptisches-Feedback-API"
  - "WebViewGold für Android"
  - "Website in App umwandeln"
  - "WebView-App-Dokumentation"
  - "Android WebView SDK"
  - "PWA zu App"
  - "HTML zu App"
  - "JavaScript-Bridge"
last_updated: "2026-10-09"
---

# Haptisches-Feedback-API – WebViewGold für Android

> **Zusammenfassung:** Löse natives Vibrations-Feedback aus deiner Web-App aus — für ein natives App-Gefühl unter Android.

[Dokumentation](../README.md) › [WebViewGold für Android](README.md) › Haptisches-Feedback-API

**Plattform:** Android · **Kategorie:** APIs & Funktionen · **Online-Version:** [www.webviewgold.com/de/docs/android/haptic-feedback/](https://www.webviewgold.com/de/docs/android/haptic-feedback/)

---

**WebViewGold** ermöglicht die Implementierung der nativen Android-Haptik-Steuerung innerhalb deiner Web-App.
Mit unserer API kannst du die folgenden Aktionen ausführen:

| Name | URL-Schema | Beschreibung |
| --- | --- | --- |
| Leichter Impuls | lighthaptic:// | Wird für eine Kollision zwischen kleinen, leichten UI-Elementen verwendet |
| Starker Impuls | heavyhaptic:// | Wird für eine Kollision zwischen großen, schweren UI-Elementen verwendet |
| Erfolgsbenachrichtigung | successhaptic:// | Zeigt an, dass eine Aufgabe oder Aktion erfolgreich abgeschlossen wurde |
| Warnbenachrichtigung | warninghaptic:// | Zeigt an, dass eine Aufgabe oder Aktion eine Art Warnung ausgelöst hat |
| Fehlerbenachrichtigung | errorhaptic:// | Zeigt an, dass ein Fehler aufgetreten ist |

Ein Beispiel für die Verwendung dieser API siehst du unten, mit einem Anker-Tag und einer benutzerdefinierten JavaScript-Funktion, die mit unserer Haptik-API interagieren.

```html
<a onclick="lightHaptic('index.html')">Navigation Link with Haptics</a>

<script>
function lightHaptic(url) {
  if (isWebViewBrowser) {
    window.location.href = url;
    loadInnerHref("lighthaptic://");
  } else {
    window.location.href = url;
  }
}

function loadInnerHref(url) {
  iFrame = document.createElement("iframe");
  iFrame.setAttribute("src", url);
  document.body.appendChild(iFrame);
  iFrame.parentNode.removeChild(iFrame);
  iFrame = null;
}
</script>
```

Klicke [hier](https://webviewgoldtest.github.io/hapticFeedback.html), um eine Demonstrationswebseite für diese Funktion anzuzeigen. Untersuche die Seite, um den Beispielcode anzuzeigen.

---

## Weiterlesen

- ← Vorherige: [Dynamische-UI-API](dynamic-ui.md)
- Weiter →: [NFC-Plugin](nfc.md)
- Dieselbe Funktion auf anderen Plattformen: [iOS – Haptisches-Feedback-API](../ios/haptic-feedback.md)
- Sprachen: [🇺🇸 English](../../android/haptic-feedback.md) · **🇩🇪 Deutsch** · [🇫🇷 Français](../../fr/android/haptic-feedback.md) · [🇪🇸 Español](../../es/android/haptic-feedback.md) · [🇨🇳 中文](../../zh/android/haptic-feedback.md)

> [!TIP]
> **Zu wenig Zeit? Wir richten deine App für dich ein.** Unser Team konfiguriert, erstellt & reicht deine WebViewGold-App ein – schlüsselfertig, mit schneller Bearbeitung, Made in Germany. [App einrichten lassen →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_android_doc_online)
>
> **Im Browser erstellen:** Kein Mac, keine IDE: Der **WebViewGold Cloud Builder** konfiguriert, erstellt & lädt deine App online hoch. [Cloud Builder entdecken →](https://www.webviewgold.com/cloud-builder?ref=android_docs)
