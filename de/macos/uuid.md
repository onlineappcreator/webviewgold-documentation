---
title: "UUID API – WebViewGold für macOS Dokumentation"
description: "Übergib eine nicht personenbezogene, eindeutige Geräte-ID (UUID) per get-uuid:// an JavaScript, um Geräte zu erkennen und Einstellungen wiederherzustellen."
lang: "de"
product: "WebViewGold für macOS"
platform: "macOS"
category: "APIs & Funktionen"
slug: "uuid"
canonical_url: "https://www.webviewgold.com/de/docs/mac/#uuid"
keywords:
  - "UUID API"
  - "WebViewGold für macOS"
  - "Website in App umwandeln"
  - "WebView-App-Dokumentation"
  - "macOS WebView SDK"
  - "PWA zu App"
  - "HTML zu App"
  - "JavaScript-Bridge"
last_updated: "2026-10-09"
---

# UUID API – WebViewGold für macOS

> **Zusammenfassung:** Übergib eine nicht personenbezogene, eindeutige Geräte-ID (UUID) per get-uuid:// an JavaScript, um Geräte zu erkennen und Einstellungen wiederherzustellen.

[Dokumentation](../README.md) › [WebViewGold für macOS](README.md) › UUID API

**Plattform:** macOS · **Kategorie:** APIs & Funktionen · **Online-Version:** [www.webviewgold.com/de/docs/mac/#uuid](https://www.webviewgold.com/de/docs/mac/#uuid)

---

WebViewGold ermöglicht die Übergabe einer **nicht personenbezogenen, eindeutigen Geräte-ID** (UUID / „Universally Unique Identifier“) an JavaScript, die **zur eindeutigen Identifizierung von macOS-Geräten verwendet werden kann**. Diese API kann beispielsweise nützlich sein, um Einstellungen oder Werte serverseitig zu speichern und clientseitig wiederherzustellen. Bitte beachte lokale und internationale **Datenschutzbestimmungen**, wenn du diese API verwendest.

```html
<a href="get-uuid://">Get UDID</a>
<a href="#" onClick="alert(uuid);">Show UDID</a>
```

---

## Weiterlesen

- ← Vorherige: [In-App Purchases API](in-app-purchases.md)
- Weiter →: [Deeplinking API](deep-linking.md)
- Dieselbe Funktion auf anderen Plattformen: [iOS – UUID-API](../ios/uuid.md) · [Android – UUID-API](../android/uuid.md)
- Sprachen: [🇺🇸 English](../../macos/uuid.md) · **🇩🇪 Deutsch** · [🇫🇷 Français](../../fr/macos/uuid.md) · [🇪🇸 Español](../../es/macos/uuid.md) · [🇨🇳 中文](../../zh/macos/uuid.md)

