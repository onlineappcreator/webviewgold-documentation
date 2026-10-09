---
title: "Shortcut-API – WebViewGold für iOS Dokumentation"
description: "Füge deiner iOS-App Schnellaktion-Shortcuts für den Home-Bildschirm hinzu, die per Deep Link zu bestimmten Seiten führen."
lang: "de"
product: "WebViewGold für iOS"
platform: "iOS"
category: "APIs & Funktionen"
slug: "shortcut"
canonical_url: "https://www.webviewgold.com/de/docs/iOS/shortcut/"
keywords:
  - "Shortcut-API"
  - "WebViewGold für iOS"
  - "Website in App umwandeln"
  - "WebView-App-Dokumentation"
  - "iOS WebView SDK"
  - "PWA zu App"
  - "HTML zu App"
  - "JavaScript-Bridge"
last_updated: "2026-10-09"
---

# Shortcut-API – WebViewGold für iOS

> **Zusammenfassung:** Füge deiner iOS-App Schnellaktion-Shortcuts für den Home-Bildschirm hinzu, die per Deep Link zu bestimmten Seiten führen.

[Dokumentation](../README.md) › [WebViewGold für iOS](README.md) › Shortcut-API

**Plattform:** iOS · **Kategorie:** APIs & Funktionen · **Online-Version:** [www.webviewgold.com/de/docs/iOS/shortcut/](https://www.webviewgold.com/de/docs/iOS/shortcut/)

---

Aktiviere `var useShortcuts = true` in `Config.swift`, um dynamische Shortcuts zu registrieren, die in `Shortcuts.json` definiert sind. Jeder Shortcut kann eine URL öffnen, JavaScript injizieren und ein SF Symbol anzeigen. Beispiel:

```json
{
    "shortcuts": [
        {
            "title": "Open Google",
            "redirection_link": "https://google.com",
            "injection": "",
            "symbol": "wrench.and.screwdriver"
        },
        {
            "title": "Open & Inject",
            "redirection_link": "https://apple.com",
            "injection": "(function() { console.log('Injected and executed!'); })();",
            "symbol": "lock.open"
        }
    ]
}
```

Nutzer können auf die Shortcuts zugreifen, indem sie das App-Icon lange gedrückt halten.

---

## Weiterlesen

- ← Vorherige: [Haptisches-Feedback-API](haptic-feedback.md)
- Weiter →: [Zwischenablage-API](clipboard.md)
- Sprachen: [🇺🇸 English](../../ios/shortcut.md) · **🇩🇪 Deutsch** · [🇫🇷 Français](../../fr/ios/shortcut.md) · [🇪🇸 Español](../../es/ios/shortcut.md) · [🇨🇳 中文](../../zh/ios/shortcut.md)

> [!TIP]
> **Zu wenig Zeit? Wir richten deine App für dich ein.** Unser Team konfiguriert, erstellt & reicht deine WebViewGold-App ein – schlüsselfertig, mit schneller Bearbeitung, Made in Germany. [App einrichten lassen →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **Im Browser erstellen:** Kein Mac, keine IDE: Der **WebViewGold Cloud Builder** konfiguriert, erstellt & lädt deine App online hoch. [Cloud Builder entdecken →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
