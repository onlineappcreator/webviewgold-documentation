---
title: "In-App-Purchase-History-API – WebViewGold für iOS Dokumentation"
description: "Lies die bisherigen In-App-Käufe des Nutzers als JSON aus deiner Web-App — perfekt für „Meine Käufe“-Seiten."
lang: "de"
product: "WebViewGold für iOS"
platform: "iOS"
category: "APIs & Funktionen"
slug: "iap-history"
canonical_url: "https://www.webviewgold.com/de/docs/iOS/iap-history/"
keywords:
  - "IAP-History-API"
  - "WebViewGold für iOS"
  - "Website in App umwandeln"
  - "WebView-App-Dokumentation"
  - "iOS WebView SDK"
  - "PWA zu App"
  - "HTML zu App"
  - "JavaScript-Bridge"
last_updated: "2026-10-09"
---

# In-App-Purchase-History-API – WebViewGold für iOS

> **Zusammenfassung:** Lies die bisherigen In-App-Käufe des Nutzers als JSON aus deiner Web-App — perfekt für „Meine Käufe“-Seiten.

[Dokumentation](../README.md) › [WebViewGold für iOS](README.md) › IAP-History-API

**Plattform:** iOS · **Kategorie:** APIs & Funktionen · **Online-Version:** [www.webviewgold.com/de/docs/iOS/iap-history/](https://www.webviewgold.com/de/docs/iOS/iap-history/)

---

Die **In-App-Purchase-History-API** liefert die Liste der bisherigen Käufe des Nutzers, die über die [In-App-Purchases-API](in-app-purchases.md) auf diesem Gerät getätigt wurden, und injiziert sie als `window.purchaseHistory` in deine Web-App. Stelle sicher, dass du eine [Extended License](credits.md) von WebViewGold besitzt, wenn du dieses Feature in einem Endprodukt verwenden möchtest.

## Verwendung

```html
<a href="getpurchasehistory://" onclick="setTimeout(renderHistory, 300)">Meine Käufe</a>

<script>
function renderHistory() {
  const data = window.purchaseHistory;
  if (!data) return;
  data.purchases.forEach(function (p) {
    console.log(p.productId, p.transactionId, p.purchaseDateMs);
  });
}
</script>
```

## Datenformat

```json
{
  "purchases": [
    {
      "productId": "com.example.premium",
      "transactionId": "2000000123456789",
      "purchaseDateMs": "1721600000000"
    }
  ]
}
```

`purchaseDateMs` ist der Kaufzeitpunkt in Unix-Millisekunden (als String).

## Typische Anwendungsfälle

- Eine Seite „Meine Abos“ oder „Meine Käufe“ innerhalb deiner Web-App anzeigen.
- Premium-Inhalte clientseitig auf Basis früherer Käufe freischalten, ohne dein Backend anzufragen.
- Debugging- und Kundensupport-Workflows.

**Hinweise:** Die Liste enthält Käufe, die innerhalb der App auf diesem Gerät getätigt wurden. Sie wird lokal gespeichert und nicht zwischen Geräten synchronisiert — für geräteübergreifende Berechtigungsprüfungen validiere Belege stattdessen auf deinem Server.

---

## Weiterlesen

- ← Vorherige: [In-App-Käufe-API](in-app-purchases.md)
- Weiter →: [QR-Code-Scanner-API](qr-code-scanner.md)
- Dieselbe Funktion auf anderen Plattformen: [Android – IAP History API](../android/iap-history.md)
- Sprachen: [🇺🇸 English](../../ios/iap-history.md) · **🇩🇪 Deutsch** · [🇫🇷 Français](../../fr/ios/iap-history.md) · [🇪🇸 Español](../../es/ios/iap-history.md) · [🇨🇳 中文](../../zh/ios/iap-history.md)

> [!TIP]
> **Zu wenig Zeit? Wir richten deine App für dich ein.** Unser Team konfiguriert, erstellt & reicht deine WebViewGold-App ein – schlüsselfertig, mit schneller Bearbeitung, Made in Germany. [App einrichten lassen →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **Im Browser erstellen:** Kein Mac, keine IDE: Der **WebViewGold Cloud Builder** konfiguriert, erstellt & lädt deine App online hoch. [Cloud Builder entdecken →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
