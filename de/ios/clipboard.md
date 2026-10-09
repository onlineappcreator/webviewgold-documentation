---
title: "Zwischenablage-API – WebViewGold für iOS Dokumentation"
description: "Kopiere Text in die iOS-Zwischenablage und lies den Inhalt der Zwischenablage aus deiner Web-App per JavaScript."
lang: "de"
product: "WebViewGold für iOS"
platform: "iOS"
category: "APIs & Funktionen"
slug: "clipboard"
canonical_url: "https://www.webviewgold.com/de/docs/iOS/clipboard/"
keywords:
  - "Zwischenablage-API"
  - "WebViewGold für iOS"
  - "Website in App umwandeln"
  - "WebView-App-Dokumentation"
  - "iOS WebView SDK"
  - "PWA zu App"
  - "HTML zu App"
  - "JavaScript-Bridge"
last_updated: "2026-10-09"
---

# Zwischenablage-API – WebViewGold für iOS

> **Zusammenfassung:** Kopiere Text in die iOS-Zwischenablage und lies den Inhalt der Zwischenablage aus deiner Web-App per JavaScript.

[Dokumentation](../README.md) › [WebViewGold für iOS](README.md) › Zwischenablage-API

**Plattform:** iOS · **Kategorie:** APIs & Funktionen · **Online-Version:** [www.webviewgold.com/de/docs/iOS/clipboard/](https://www.webviewgold.com/de/docs/iOS/clipboard/)

---

Rufe `getclipboard://` auf, um den aktuellen Inhalt der Zwischenablage in die JavaScript-Variable `clipboarddata` zu übertragen.

```html
<a href="getclipboard://">Read Clipboard</a>
<script>
function showClipboard() {
    console.log(clipboarddata);
}
</script>
```

---

## Weiterlesen

- ← Vorherige: [Shortcut-API](shortcut.md)
- Weiter →: [Read/Write-Value-API](read-write-value.md)
- Dieselbe Funktion auf anderen Plattformen: [Android – Zwischenablage-API](../android/clipboard.md)
- Sprachen: [🇺🇸 English](../../ios/clipboard.md) · **🇩🇪 Deutsch** · [🇫🇷 Français](../../fr/ios/clipboard.md) · [🇪🇸 Español](../../es/ios/clipboard.md) · [🇨🇳 中文](../../zh/ios/clipboard.md)

> [!TIP]
> **Zu wenig Zeit? Wir richten deine App für dich ein.** Unser Team konfiguriert, erstellt & reicht deine WebViewGold-App ein – schlüsselfertig, mit schneller Bearbeitung, Made in Germany. [App einrichten lassen →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **Im Browser erstellen:** Kein Mac, keine IDE: Der **WebViewGold Cloud Builder** konfiguriert, erstellt & lädt deine App online hoch. [Cloud Builder entdecken →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
