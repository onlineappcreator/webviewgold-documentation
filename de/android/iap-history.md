---
title: "In-App Purchase History API – WebViewGold für Android Dokumentation"
description: "Return the user's Google Play purchase history as window.purchaseHistory so your web app can list subscriptions or unlock premium content client-side."
lang: "de"
product: "WebViewGold für Android"
platform: "Android"
category: "APIs & Funktionen"
slug: "iap-history"
canonical_url: "https://www.webviewgold.com/de/docs/android/iap-history/"
keywords:
  - "IAP History API"
  - "WebViewGold für Android"
  - "Website in App umwandeln"
  - "WebView-App-Dokumentation"
  - "Android WebView SDK"
  - "PWA zu App"
  - "HTML zu App"
  - "JavaScript-Bridge"
last_updated: "2026-10-09"
---

# In-App Purchase History API – WebViewGold für Android

> **Zusammenfassung:** Return the user's Google Play purchase history as window.purchaseHistory so your web app can list subscriptions or unlock premium content client-side.

[Dokumentation](../README.md) › [WebViewGold für Android](README.md) › IAP History API

**Plattform:** Android · **Kategorie:** APIs & Funktionen · **Online-Version:** [www.webviewgold.com/de/docs/android/iap-history/](https://www.webviewgold.com/de/docs/android/iap-history/)

---

Die **In-App-Purchase-History-API** liefert die Liste bisheriger Käufe des Nutzers (Produkt-IDs, Zeitpunkte, Tokens) über Google Play Billing und injiziert sie in deine Web-App als `window.purchaseHistory`. Stelle sicher, dass du eine [Extended License](credits.md) von WebViewGold besitzt, wenn du diese Funktion in einem Endprodukt einsetzen möchtest.

## So verwendest du die Funktion

```html
<a href="getpurchasehistory://" onclick="setTimeout(renderHistory, 300)">My purchases</a>

<script>
function renderHistory() {
  const data = window.purchaseHistory;
  if (!data) return;
  data.purchases.forEach(function (p) {
    console.log(p.productId, p.purchaseTime, p.orderId);
  });
}
</script>
```

## Struktur der Antwort

```json
{
  "purchases": [
    {
      "productId": "com.example.premium",
      "purchaseTime": 1721600000000,
      "orderId": "GPA.xxxx-xxxx-xxxx",
      "purchaseToken": "..."
    }
  ]
}
```

Die genauen Felder hängen vom Store-Eintrag ab – behandle die Liste als JSON-Array.

## Typische Anwendungsfälle

- Seite „Meine Abonnements" oder „Meine Käufe" in der Web-App.
- Client-seitige Freischaltung von Premium-Inhalten anhand vergangener Käufe ohne Backend-Request.
- Debugging und Kundensupport.

**Hinweise:** Die Liste enthält nur Käufe des aktuell angemeldeten Google-Play-Kontos auf diesem Gerät.

---

## Weiterlesen

- ← Vorherige: [In-App-Käufe-API](in-app-purchases.md)
- Weiter →: [QR-Code-Scanner-API](qr-code-scanner.md)
- Dieselbe Funktion auf anderen Plattformen: [iOS – IAP-History-API](../ios/iap-history.md)
- Sprachen: [🇺🇸 English](../../android/iap-history.md) · **🇩🇪 Deutsch** · [🇫🇷 Français](../../fr/android/iap-history.md) · [🇪🇸 Español](../../es/android/iap-history.md) · [🇨🇳 中文](../../zh/android/iap-history.md)

> [!TIP]
> **Zu wenig Zeit? Wir richten deine App für dich ein.** Unser Team konfiguriert, erstellt & reicht deine WebViewGold-App ein – schlüsselfertig, mit schneller Bearbeitung, Made in Germany. [App einrichten lassen →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_android_doc_online)
>
> **Im Browser erstellen:** Kein Mac, keine IDE: Der **WebViewGold Cloud Builder** konfiguriert, erstellt & lädt deine App online hoch. [Cloud Builder entdecken →](https://www.webviewgold.com/cloud-builder?ref=android_docs)
