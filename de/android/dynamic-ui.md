---
title: "Dynamische-UI-API – WebViewGold für Android Dokumentation"
description: "Ändere native UI-Elemente wie die Statusleistenfarbe dynamisch aus deiner Web-App unter Android."
lang: "de"
product: "WebViewGold für Android"
platform: "Android"
category: "APIs & Funktionen"
slug: "dynamic-ui"
canonical_url: "https://www.webviewgold.com/de/docs/android/dynamic-ui/"
keywords:
  - "Dynamische-UI-API"
  - "WebViewGold für Android"
  - "Website in App umwandeln"
  - "WebView-App-Dokumentation"
  - "Android WebView SDK"
  - "PWA zu App"
  - "HTML zu App"
  - "JavaScript-Bridge"
last_updated: "2026-10-09"
---

# Dynamische-UI-API – WebViewGold für Android

> **Zusammenfassung:** Ändere native UI-Elemente wie die Statusleistenfarbe dynamisch aus deiner Web-App unter Android.

[Dokumentation](../README.md) › [WebViewGold für Android](README.md) › Dynamische-UI-API

**Plattform:** Android · **Kategorie:** APIs & Funktionen · **Online-Version:** [www.webviewgold.com/de/docs/android/dynamic-ui/](https://www.webviewgold.com/de/docs/android/dynamic-ui/)

---

Mit WebViewGold kannst du die UI-Elemente in deiner Web-App dynamisch anpassen. Zu diesen Elementen können die Statusleiste, die untere Leiste (iOS), die Navigationsleiste (Android) und Pull-to-Refresh (iOS) gehören. WebViewGold umfasst die folgenden Befehle zur dynamischen Anpassung dieser Elemente:

- **statusbarcolor://**
  - Der MASTER-BEFEHL, um die Farbe der Statusleiste und automatisch aller anderen relevanten UI-Elemente zu ändern, wie z. B. die Textfarbe der Statusleiste, die Farbe der unteren Leiste (iOS), die Farbe der Navigationsleiste (Android) usw.
- **statusbartextcolor://**
  - Ermöglicht es dir, die Textfarbe der Statusleiste manuell zu ändern (iOS und Android).
- **bottombarcolor://**
  - Falls ein UI-Element für die untere Leiste (iOS) oder die Navigationsleiste (Android) vorhanden ist, ermöglicht es dir, dessen Farbe manuell zu ändern.
- **navbartextcolor://**
  - Ermöglicht es dir, die Textfarbe der Navigationsleiste unter Android manuell zu ändern. Unter iOS wird die Anfrage ignoriert (die untere Leiste unter iOS enthält keinen Text).
- **hidebars://**
  - Ermöglicht es dir, den Hintergrund der Status- und Navigationsleiste auszublenden.

## Ändern der Farbe der Statusleiste (und automatisch anderer UI-Elemente)

Diese Funktion unterstützt eine Farbeingabe im folgenden Format:

- RGB = {rot, grün, blau}

Dabei sind die Werte ganze Zahlen zwischen 0 (min) und 255 (max).

Verwende JavaScript mit einer solchen URL, um die Farbe der Statusleiste zu ändern:

```html
<script>
// Example: red
window.location.href = "statusbarcolor://255,0,0";
</script>
```

Wenn du die Farbe der Statusleiste änderst, wechselt der Text der Statusleiste automatisch zu einer passenden Farbe (weiß oder schwarz), abhängig davon, wie dunkel die Farbe ist.\
Bei optionalen UI-Funktionen wie *Pull To Refresh* (iOS), der *unteren Leiste* (iOS) und der *Navigationsleiste* (Android) werden die Farben ebenfalls automatisch angepasst.

## Ändern der Farbe des Statusleisten-Textes

Wenn du die Farbe des Statusleisten-Textes manuell auswählen möchtest, kannst du dies über diese Option tun.

Diese Funktion unterstützt eine Texteingabe für die folgenden Optionen:

- "white"
- "black"

Verwende JavaScript mit einer solchen URL, um die Farbe des Statusleisten-Textes zu ändern:

```html
<script>
// Example: white text
window.location.href = "statusbartextcolor://white";
// Example: black text
window.location.href = "statusbartextcolor://black";
</script>
```

## Ändern der Farbe der Navigationsleiste

Diese Funktion unterstützt eine Farbeingabe im folgenden Format:

- RGB = {rot, grün, blau}

Dabei sind die Werte ganze Zahlen zwischen 0 (min) und 255 (max).

Verwende JavaScript mit einer solchen URL, um die Farbe der Navigationsleiste zu ändern:

```html
<script>
// Example: red
window.location.href = "bottombarcolor://255,0,0";
</script>
```

## Ändern der Farbe des Navigationsleisten-Textes

Wenn du die Farbe des Navigationsleisten-Textes manuell auswählen möchtest, kannst du dies über diese Option tun. Bitte beachte, dass diese Anfrage unter iOS ignoriert wird.

Diese Funktion unterstützt eine Texteingabe für die folgenden Optionen:

- "white"
- "black"

Verwende JavaScript mit einer solchen URL, um die Farbe des Navigationsleisten-Textes zu ändern:

```html
<script>
// Example: white text
window.location.href = "navbartextcolor://white";
// Example: black text
window.location.href = "navbartextcolor://black";
</script>
```

## Ausblenden der Status- und unteren Leisten

Die hidebars-Funktionalität kann entweder **on** oder **off** sein.

Hinweis: Der Text der Statusleiste, wie z. B. die Uhrzeit und der Batterieprozentsatz, *bleibt nicht* für den Nutzer sichtbar.
Diese können jedoch durch ein Wischen des Nutzers vom oberen Rand wieder eingeblendet werden.

Verwende JavaScript, um den Sichtbarkeitsstatus der Status- und Navigationsleiste zu ändern:

```html
<script>
// Example: hide the bars from view
window.location.href = "hidebars://on";
// Example: redisplay the bars after being hidden
window.location.href = "hidebars://off";
</script>
```

---

## Dark Mode erkennen (JavaScript-Variable `isDarkMode`)

Um deine dynamischen UI-Farben an das Systemdesign des Nutzers anzupassen, injiziert WebViewGold nach dem Laden jeder Seite automatisch die JavaScript-Variable `isDarkMode` (`true` oder `false`). Beispiel:

```html
<script>
if (typeof isDarkMode !== "undefined" && isDarkMode) {
    // Dark Mode: z. B. dunkle Statusleiste setzen
    window.location.href = "statusbarcolor://0,0,0";
    window.location.href = "statusbartextcolor://white";
} else {
    // Light Mode
    window.location.href = "statusbarcolor://255,255,255";
    window.location.href = "statusbartextcolor://black";
}
</script>
```

**Hinweis:** Alternativ kannst du in deiner Web-App die Standard-CSS-Media-Query `prefers-color-scheme` verwenden. Die injizierte Variable `isDarkMode` ist praktisch, wenn du die oben beschriebenen WebViewGold-UI-APIs aus JavaScript auslösen möchtest.

---

## Weiterlesen

- ← Vorherige: [Kontakte-API](contacts.md)
- Weiter →: [Haptisches-Feedback-API](haptic-feedback.md)
- Dieselbe Funktion auf anderen Plattformen: [iOS – Dynamische-UI-API](../ios/dynamic-ui.md)
- Sprachen: [🇺🇸 English](../../android/dynamic-ui.md) · **🇩🇪 Deutsch** · [🇫🇷 Français](../../fr/android/dynamic-ui.md) · [🇪🇸 Español](../../es/android/dynamic-ui.md) · [🇨🇳 中文](../../zh/android/dynamic-ui.md)

> [!TIP]
> **Zu wenig Zeit? Wir richten deine App für dich ein.** Unser Team konfiguriert, erstellt & reicht deine WebViewGold-App ein – schlüsselfertig, mit schneller Bearbeitung, Made in Germany. [App einrichten lassen →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_android_doc_online)
>
> **Im Browser erstellen:** Kein Mac, keine IDE: Der **WebViewGold Cloud Builder** konfiguriert, erstellt & lädt deine App online hoch. [Cloud Builder entdecken →](https://www.webviewgold.com/cloud-builder?ref=android_docs)
