---
title: "Dynamische-UI-API – WebViewGold für iOS Dokumentation"
description: "Ändere native UI-Elemente wie die Farben der Statusleiste oder der unteren Leiste dynamisch aus deiner Web-App."
lang: "de"
product: "WebViewGold für iOS"
platform: "iOS"
category: "APIs & Funktionen"
slug: "dynamic-ui"
canonical_url: "https://www.webviewgold.com/de/docs/iOS/dynamic-ui/"
keywords:
  - "Dynamische-UI-API"
  - "WebViewGold für iOS"
  - "Website in App umwandeln"
  - "WebView-App-Dokumentation"
  - "iOS WebView SDK"
  - "PWA zu App"
  - "HTML zu App"
  - "JavaScript-Bridge"
last_updated: "2026-10-09"
---

# Dynamische-UI-API – WebViewGold für iOS

> **Zusammenfassung:** Ändere native UI-Elemente wie die Farben der Statusleiste oder der unteren Leiste dynamisch aus deiner Web-App.

[Dokumentation](../README.md) › [WebViewGold für iOS](README.md) › Dynamische-UI-API

**Plattform:** iOS · **Kategorie:** APIs & Funktionen · **Online-Version:** [www.webviewgold.com/de/docs/iOS/dynamic-ui/](https://www.webviewgold.com/de/docs/iOS/dynamic-ui/)

---

Mit WebViewGold kannst du die UI-Elemente in deiner Web-App dynamisch anpassen. Zu diesen Elementen können die Statusleiste, die Bottom Bar (iOS), die Navigationsleiste (Android) und die Pull-to-Refresh-Funktion (iOS) gehören. WebViewGold enthält die folgenden Befehle zur dynamischen Anpassung dieser Elemente:

- **statusbarcolor://**
  - Der MASTER-BEFEHL, um die Farbe der Statusleiste und aller weiteren relevanten UI-Elemente automatisch zu ändern, wie zum Beispiel die Textfarbe der Statusleiste, die Farbe der Bottom Bar (iOS), die Farbe der Navigationsleiste (Android) usw.
- **statusbartextcolor://**
  - Ermöglicht dir, die Textfarbe der Statusleiste (iOS und Android) manuell zu ändern.
- **bottombarcolor://**
  - Falls ein UI-Element „Bottom Bar“ (iOS) oder „Navigationsleiste“ (Android) vorhanden ist, ermöglicht dir dieser Befehl, dessen Farbe manuell zu ändern.
- **hidebars://**
  - Ermöglicht dir, den Hintergrund der Statusleiste auszublenden, wobei der Text auf einem transparenten Hintergrund erhalten bleibt.

## Ändern der Farbe der Statusleiste (und weiterer UI-Elemente automatisch)

Diese Funktion unterstützt eine Farbeingabe im folgenden Format:

- RGB = {red, green, blue}

Wobei die Werte Ganzzahlen zwischen 0 (min) und 255 (max) sind.

Verwende JavaScript mit dieser Art von URL, um die Farbe der Statusleiste zu ändern:

```html
<script>
// Example: red
window.location.href = "statusbarcolor://255,0,0";
</script>
```

Wenn du die Farbe der Statusleiste änderst, wird der Text der Statusleiste automatisch in einer passenden Farbe (weiß oder schwarz) dargestellt, abhängig davon, wie dunkel die Farbe ist.\
Optionale UI-Funktionen wie *Pull To Refresh* (iOS), die *Bottom Bar* (iOS) und die *Navigationsleiste* (Android) erhalten ihre Farben ebenfalls automatisch angepasst.

## Ändern der Farbe des Statusleisten-Textes

Wenn du die Farbe des Statusleisten-Textes manuell wählen möchtest, kannst du dies mit dieser Option tun.

Diese Funktion unterstützt eine Texteingabe für die folgenden Optionen:

- "white"
- "black"

Verwende JavaScript mit dieser Art von URL, um die Farbe des Statusleisten-Textes zu ändern:

```html
<script>
// Example: white text
window.location.href = "statusbartextcolor://white";
// Example: black text
window.location.href = "statusbartextcolor://black";
</script>
```

## Ändern der Farbe der Bottom Bar

Diese Funktion unterstützt eine Farbeingabe im folgenden Format:

- RGB = {red, green, blue}

Wobei die Werte Ganzzahlen zwischen 0 (min) und 255 (max) sind.

Verwende JavaScript mit dieser Art von URL, um die Farbe der Statusleiste zu ändern:

```html
<script>
// Example: red
window.location.href = "bottombarcolor://255,0,0";
</script>
```

## Ausblenden der Statusleiste

Die hidebars-Funktionalität kann entweder **on** oder **off** sein.

Beachte: Der Text der Statusleiste, wie Uhrzeit und Batterieanzeige, bleibt für den Nutzer sichtbar,
der Hintergrund um den Text wird jedoch transparent, und die WebView dehnt sich aus, um den freiwerdenden Platz zu füllen.

Verwende JavaScript, um die Sichtbarkeit der Leiste zu ändern:

```html
<script>
// Example: hide the bars from view
window.location.href = "hidebars://on";
// Example: redisplay the bars after being hidden
window.location.href = "hidebars://off";
</script>
```

---

## Weiterlesen

- ← Vorherige: [App-Versionsprüfung-API](app-version-check.md)
- Weiter →: [Dynamisches-App-Icon-API](dynamic-app-icon.md)
- Dieselbe Funktion auf anderen Plattformen: [Android – Dynamische-UI-API](../android/dynamic-ui.md)
- Sprachen: [🇺🇸 English](../../ios/dynamic-ui.md) · **🇩🇪 Deutsch** · [🇫🇷 Français](../../fr/ios/dynamic-ui.md) · [🇪🇸 Español](../../es/ios/dynamic-ui.md) · [🇨🇳 中文](../../zh/ios/dynamic-ui.md)

> [!TIP]
> **Zu wenig Zeit? Wir richten deine App für dich ein.** Unser Team konfiguriert, erstellt & reicht deine WebViewGold-App ein – schlüsselfertig, mit schneller Bearbeitung, Made in Germany. [App einrichten lassen →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **Im Browser erstellen:** Kein Mac, keine IDE: Der **WebViewGold Cloud Builder** konfiguriert, erstellt & lädt deine App online hoch. [Cloud Builder entdecken →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
