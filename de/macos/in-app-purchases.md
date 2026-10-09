---
title: "In-App Purchase & In-App Subscription API – WebViewGold für macOS Dokumentation"
description: "Verkaufe In-App-Käufe und Abonnements im Mac App Store direkt aus deiner Web-App: Produkt-ID in Constants.h eintragen und Käufe per inapppurchase://-Link auslösen."
lang: "de"
product: "WebViewGold für macOS"
platform: "macOS"
category: "APIs & Funktionen"
slug: "in-app-purchases"
canonical_url: "https://www.webviewgold.com/de/docs/mac/#inapppurchases"
keywords:
  - "In-App Purchases API"
  - "WebViewGold für macOS"
  - "Website in App umwandeln"
  - "WebView-App-Dokumentation"
  - "macOS WebView SDK"
  - "PWA zu App"
  - "HTML zu App"
  - "JavaScript-Bridge"
last_updated: "2026-10-09"
---

# In-App Purchase & In-App Subscription API – WebViewGold für macOS

> **Zusammenfassung:** Verkaufe In-App-Käufe und Abonnements im Mac App Store direkt aus deiner Web-App: Produkt-ID in Constants.h eintragen und Käufe per inapppurchase://-Link auslösen.

[Dokumentation](../README.md) › [WebViewGold für macOS](README.md) › In-App Purchases API

**Plattform:** macOS · **Kategorie:** APIs & Funktionen · **Online-Version:** [www.webviewgold.com/de/docs/mac/#inapppurchases](https://www.webviewgold.com/de/docs/mac/#inapppurchases)

---

In einigen macOS-/Mac-Apps kannst du zusätzliche Inhalte oder Dienste kaufen. Diese Art von Käufen wird als „in-app purchases“ bezeichnet. Sie können eine attraktive Einnahmequelle für Entwickler sein und sind für Kunden sehr praktisch, da für die Abwicklung vorhandene Konten und Zahlungsquellen verwendet werden. WebViewGold ermöglicht das Auslösen von Mac App Store In-App Purchases. Füge einfach deine In-App Purchase Product ID (aus *App Store Connect*) in die Datei *Constants.h* ein: \
![Mac App Store In-App Purchase Product ID in der Datei Constants.h](../../assets/macos/img/inapppurchase.png)\
Verlinke anschließend einfach auf eine solche URL:

```html
<a href="inapppurchase://?successful_url=https://www.google.com">Buy In-App Purchase</a>
```

Alternativ kannst du für Abonnementprodukte eine solche URL verwenden:

```html
<a href="inappsubscription://?successful_url=https://www.google.com&expired_url=https://www.yahoo.com">Start In-App Subscription</a>
```

In diesem URL-Beispiel sollte https://www.google.com nach der erfolgreichen Aktivierung des Abonnements aufgerufen werden, und https://www.yahoo.com sollte aufgerufen werden, sobald das Abonnement abgelaufen ist.

---

## Weiterlesen

- ← Vorherige: [Begrüßungsbildschirm](splash-screen.md)
- Weiter →: [UUID API](uuid.md)
- Dieselbe Funktion auf anderen Plattformen: [iOS – In-App-Käufe-API](../ios/in-app-purchases.md) · [Android – In-App-Käufe-API](../android/in-app-purchases.md)
- Sprachen: [🇺🇸 English](../../macos/in-app-purchases.md) · **🇩🇪 Deutsch** · [🇫🇷 Français](../../fr/macos/in-app-purchases.md) · [🇪🇸 Español](../../es/macos/in-app-purchases.md) · [🇨🇳 中文](../../zh/macos/in-app-purchases.md)

