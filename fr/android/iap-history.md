---
title: "In-App Purchase History API – Documentation WebViewGold pour Android"
description: "Return the user's Google Play purchase history as window.purchaseHistory so your web app can list subscriptions or unlock premium content client-side."
lang: "fr"
product: "WebViewGold pour Android"
platform: "Android"
category: "API et fonctionnalités"
slug: "iap-history"
canonical_url: "https://www.webviewgold.com/fr/docs/android/iap-history/"
keywords:
  - "IAP History API"
  - "WebViewGold pour Android"
  - "convertir un site web en app"
  - "documentation d’app WebView"
  - "SDK WebView Android"
  - "PWA en app"
  - "HTML en app"
  - "pont JavaScript"
last_updated: "2026-10-09"
---

# In-App Purchase History API – WebViewGold pour Android

> **Résumé :** Return the user's Google Play purchase history as window.purchaseHistory so your web app can list subscriptions or unlock premium content client-side.

[Documentation](../README.md) › [WebViewGold pour Android](README.md) › IAP History API

**Plateforme :** Android · **Catégorie :** API et fonctionnalités · **Version en ligne :** [www.webviewgold.com/fr/docs/android/iap-history/](https://www.webviewgold.com/fr/docs/android/iap-history/)

---

L'**API d'historique des achats intégrés** renvoie la liste des achats antérieurs de l'utilisateur (identifiants de produit, horodatages, tokens) effectués via Google Play Billing et l'injecte dans votre application web sous la forme `window.purchaseHistory`. Assurez-vous de disposer d'une [licence étendue](credits.md) de WebViewGold si vous prévoyez d'utiliser cette fonctionnalité dans un produit final.

## Utilisation

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

## Structure du payload

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

Les champs exacts dépendent de l'enregistrement du store — traitez la valeur comme un tableau JSON à parcourir.

## Cas d'usage typiques

- Afficher une page « Mes abonnements » ou « Mes achats » dans votre application web.
- Déverrouiller côté client du contenu premium en fonction d'achats antérieurs sans solliciter votre backend.
- Débogage et flux de support client.

**Remarques :** La liste ne contient que les achats effectués sous le compte Google Play actuellement connecté sur cet appareil.

---

## Continuer la lecture

- ← Précédent : [API d'achats intégrés](in-app-purchases.md)
- Suivant → : [API scanner de QR codes](qr-code-scanner.md)
- Même fonctionnalité sur les autres plateformes : [iOS – API d'historique des achats](../ios/iap-history.md)
- Langues : [🇺🇸 English](../../android/iap-history.md) · [🇩🇪 Deutsch](../../de/android/iap-history.md) · **🇫🇷 Français** · [🇪🇸 Español](../../es/android/iap-history.md) · [🇨🇳 中文](../../zh/android/iap-history.md)

> [!TIP]
> **Trop occupé ? Nous configurons votre app pour vous.** Notre équipe configure, compile & soumet votre app WebViewGold — clé en main, délai rapide, Made in Germany. [Faire configurer mon app →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_android_doc_online)
>
> **Compilez dans votre navigateur :** Pas de Mac, pas d’IDE : le **WebViewGold Cloud Builder** configure, compile & met en ligne votre app. [Découvrir Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=android_docs)
