---
title: "Apple-Wallet-Pass-API – WebViewGold für iOS Dokumentation"
description: "Lass Nutzer .pkpass-Pässe (Tickets, Coupons, Mitgliedskarten) aus deiner Web-App zu Apple Wallet hinzufügen."
lang: "de"
product: "WebViewGold für iOS"
platform: "iOS"
category: "APIs & Funktionen"
slug: "wallet-pass"
canonical_url: "https://www.webviewgold.com/de/docs/iOS/wallet-pass/"
keywords:
  - "Apple-Wallet-Pass-API"
  - "WebViewGold für iOS"
  - "Website in App umwandeln"
  - "WebView-App-Dokumentation"
  - "iOS WebView SDK"
  - "PWA zu App"
  - "HTML zu App"
  - "JavaScript-Bridge"
last_updated: "2026-10-09"
---

# Apple-Wallet-Pass-API – WebViewGold für iOS

> **Zusammenfassung:** Lass Nutzer .pkpass-Pässe (Tickets, Coupons, Mitgliedskarten) aus deiner Web-App zu Apple Wallet hinzufügen.

[Dokumentation](../README.md) › [WebViewGold für iOS](README.md) › Apple-Wallet-Pass-API

**Plattform:** iOS · **Kategorie:** APIs & Funktionen · **Online-Version:** [www.webviewgold.com/de/docs/iOS/wallet-pass/](https://www.webviewgold.com/de/docs/iOS/wallet-pass/)

---

Mit der **Apple-Wallet-Pass-API** kann deine Web-App eine `.pkpass`-Datei (Event-Ticket, Bordkarte, Coupon, Kunden- oder Mitgliedskarte) an den Nutzer übergeben, damit er sie zu **Apple Wallet** hinzufügen kann.

## Verwendung

Verlinke deine `.pkpass`-Datei, ersetze dabei jedoch das `https://`-Präfix der Datei-URL durch `addpkpass://`:

```html
<a href="addpkpass://example.com/passes/ticket.pkpass">Ticket zu Apple Wallet hinzufügen</a>
```

## So funktioniert es

1. Die App wandelt den `addpkpass://`-Link zurück in eine `https://`-URL um.
2. Die Pass-URL wird in einem In-App-Browser-Tab geöffnet, der den `.pkpass`-Inhalt erkennt und die native **Zu Apple Wallet hinzufügen**-Vorschau anzeigt.
3. Der Nutzer bestätigt, und der Pass wird in der Wallet-App gespeichert.

**Hinweise:** Der Pass muss über HTTPS mit dem korrekten MIME-Type `application/vnd.apple.pkpass` ausgeliefert und mit einem gültigen Apple-Pass-Type-ID-Zertifikat signiert sein (siehe die [Apple-Wallet-Passes-Dokumentation](https://developer.apple.com/documentation/walletpasses) zur Erstellung von Pässen).

---

## Weiterlesen

- ← Vorherige: [iCal-Kalender-API](ical-calendar.md)
- Weiter →: [UUID-API](uuid.md)
- Sprachen: [🇺🇸 English](../../ios/wallet-pass.md) · **🇩🇪 Deutsch** · [🇫🇷 Français](../../fr/ios/wallet-pass.md) · [🇪🇸 Español](../../es/ios/wallet-pass.md) · [🇨🇳 中文](../../zh/ios/wallet-pass.md)

> [!TIP]
> **Zu wenig Zeit? Wir richten deine App für dich ein.** Unser Team konfiguriert, erstellt & reicht deine WebViewGold-App ein – schlüsselfertig, mit schneller Bearbeitung, Made in Germany. [App einrichten lassen →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **Im Browser erstellen:** Kein Mac, keine IDE: Der **WebViewGold Cloud Builder** konfiguriert, erstellt & lädt deine App online hoch. [Cloud Builder entdecken →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
