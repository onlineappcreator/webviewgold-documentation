---
title: "Haptisches-Feedback-API – WebViewGold für iOS Dokumentation"
description: "Löse natives haptisches Feedback (Vibrationen) aus deiner Web-App aus, für ein echtes natives App-Gefühl auf iOS."
lang: "de"
product: "WebViewGold für iOS"
platform: "iOS"
category: "APIs & Funktionen"
slug: "haptic-feedback"
canonical_url: "https://www.webviewgold.com/de/docs/iOS/haptic-feedback/"
keywords:
  - "Haptisches-Feedback-API"
  - "WebViewGold für iOS"
  - "Website in App umwandeln"
  - "WebView-App-Dokumentation"
  - "iOS WebView SDK"
  - "PWA zu App"
  - "HTML zu App"
  - "JavaScript-Bridge"
last_updated: "2026-10-09"
---

# Haptisches-Feedback-API – WebViewGold für iOS

> **Zusammenfassung:** Löse natives haptisches Feedback (Vibrationen) aus deiner Web-App aus, für ein echtes natives App-Gefühl auf iOS.

[Dokumentation](../README.md) › [WebViewGold für iOS](README.md) › Haptisches-Feedback-API

**Plattform:** iOS · **Kategorie:** APIs & Funktionen · **Online-Version:** [www.webviewgold.com/de/docs/iOS/haptic-feedback/](https://www.webviewgold.com/de/docs/iOS/haptic-feedback/)

---

**WebViewGold** ermöglicht die Implementierung nativer iOS-Haptik-Steuerung in deiner Web-App.
Mit unserer API kannst du die folgenden Aktionen ausführen:

| Name | URL-Schema | Beschreibung |
| --- | --- | --- |
| Leichter Impuls | lighthaptic:// | Wird bei einer Kollision zwischen kleinen, leichten UI-Elementen verwendet |
| Mittlerer Impuls | mediumhaptic:// | Wird bei einer Kollision zwischen mittelgroßen UI-Elementen verwendet |
| Starker Impuls | heavyhaptic:// | Wird bei einer Kollision zwischen großen, schweren UI-Elementen verwendet |
| Erfolgs-Benachrichtigung | successhaptic:// | Zeigt an, dass eine Aufgabe oder Aktion erfolgreich abgeschlossen wurde |
| Warnungs-Benachrichtigung | warninghaptic:// | Zeigt an, dass eine Aufgabe oder Aktion eine Warnung ausgelöst hat |
| Fehler-Benachrichtigung | errorhaptic:// | Zeigt an, dass ein Fehler aufgetreten ist |

Wir empfehlen, dir vor der Integration dieser Funktionen in deine Anwendung Apples [Best Practices](https://developer.apple.com/design/human-interface-guidelines/playing-haptics) anzusehen.
Ein Beispiel für die Verwendung dieser API siehst du unten, mit einem Anchor-Tag und einer benutzerdefinierten JavaScript-Funktion, die mit unserer Haptik-API interagieren.

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

Klicke [hier](https://webviewgoldtest.github.io/hapticFeedback.html), um eine Demo-Webseite für diese Funktion aufzurufen. Untersuche die Seite, um den Beispielcode einzusehen.

---

## Weiterlesen

- ← Vorherige: [Biometrische-Auth-API](biometric-authentication.md)
- Weiter →: [Shortcut-API](shortcut.md)
- Dieselbe Funktion auf anderen Plattformen: [Android – Haptisches-Feedback-API](../android/haptic-feedback.md)
- Sprachen: [🇺🇸 English](../../ios/haptic-feedback.md) · **🇩🇪 Deutsch** · [🇫🇷 Français](../../fr/ios/haptic-feedback.md) · [🇪🇸 Español](../../es/ios/haptic-feedback.md) · [🇨🇳 中文](../../zh/ios/haptic-feedback.md)

> [!TIP]
> **Zu wenig Zeit? Wir richten deine App für dich ein.** Unser Team konfiguriert, erstellt & reicht deine WebViewGold-App ein – schlüsselfertig, mit schneller Bearbeitung, Made in Germany. [App einrichten lassen →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **Im Browser erstellen:** Kein Mac, keine IDE: Der **WebViewGold Cloud Builder** konfiguriert, erstellt & lädt deine App online hoch. [Cloud Builder entdecken →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
