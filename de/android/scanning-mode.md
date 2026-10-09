---
title: "Scan-Modus-API – WebViewGold für Android Dokumentation"
description: "Optimiere das Kamera-Scanverhalten des QR- und Barcode-Scanners in WebViewGold für Android."
lang: "de"
product: "WebViewGold für Android"
platform: "Android"
category: "APIs & Funktionen"
slug: "scanning-mode"
canonical_url: "https://www.webviewgold.com/de/docs/android/scanning-mode/"
keywords:
  - "Scan-Modus-API"
  - "WebViewGold für Android"
  - "Website in App umwandeln"
  - "WebView-App-Dokumentation"
  - "Android WebView SDK"
  - "PWA zu App"
  - "HTML zu App"
  - "JavaScript-Bridge"
last_updated: "2026-10-09"
---

# Scan-Modus-API – WebViewGold für Android

> **Zusammenfassung:** Optimiere das Kamera-Scanverhalten des QR- und Barcode-Scanners in WebViewGold für Android.

[Dokumentation](../README.md) › [WebViewGold für Android](README.md) › Scan-Modus-API

**Plattform:** Android · **Kategorie:** APIs & Funktionen · **Online-Version:** [www.webviewgold.com/de/docs/android/scanning-mode/](https://www.webviewgold.com/de/docs/android/scanning-mode/)

---

Wenn deine Web-App Informationen zum Scannen auf dem Bildschirm anzeigt (zum Beispiel einen QR-Code), kann es hilfreich sein, die Bildschirmhelligkeit auf 100 % zu erhöhen und zu verhindern, dass der Bildschirm in den Ruhezustand wechselt. WebViewGold stellt die Scanning-Mode-API bereit, um diese optimalen Scan-Bedingungen dynamisch zu aktivieren.\
Diese API umfasst 3 Befehle:

- "auto" = aktiviert den Scan-Modus und schaltet ihn beim Seitenwechsel automatisch wieder aus.
- "on" = aktiviert den Scan-Modus, der auch nach Seitenwechseln aktiv bleibt.
- "off" = deaktiviert den Scan-Modus.

Verlinke diese Art von URLs, um die Scanning-Mode-API zu nutzen:

```html
<a href="scanningmode://auto">Enable Scanning Mode; will automatically disable on page redirect.</a>
<a href="scanningmode://on">Enable Scanning Mode; will persist until manually disabled.</a>
<a href="scanningmode://off">Disable Scanning Mode.</a>
```

---

## Weiterlesen

- ← Vorherige: [QR-Code-Scanner-API](qr-code-scanner.md)
- Weiter →: [Barcode-Scanner-API](barcode-scanner.md)
- Dieselbe Funktion auf anderen Plattformen: [iOS – Scan-Modus-API](../ios/scanning-mode.md)
- Sprachen: [🇺🇸 English](../../android/scanning-mode.md) · **🇩🇪 Deutsch** · [🇫🇷 Français](../../fr/android/scanning-mode.md) · [🇪🇸 Español](../../es/android/scanning-mode.md) · [🇨🇳 中文](../../zh/android/scanning-mode.md)

> [!TIP]
> **Zu wenig Zeit? Wir richten deine App für dich ein.** Unser Team konfiguriert, erstellt & reicht deine WebViewGold-App ein – schlüsselfertig, mit schneller Bearbeitung, Made in Germany. [App einrichten lassen →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_android_doc_online)
>
> **Im Browser erstellen:** Kein Mac, keine IDE: Der **WebViewGold Cloud Builder** konfiguriert, erstellt & lädt deine App online hoch. [Cloud Builder entdecken →](https://www.webviewgold.com/cloud-builder?ref=android_docs)
