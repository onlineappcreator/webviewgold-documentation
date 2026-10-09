---
title: "API d'historique des achats In-App – Documentation WebViewGold pour iOS"
description: "Lisez les achats In-App précédents de l'utilisateur depuis votre application web au format JSON — parfait pour les pages « Mes achats »."
lang: "fr"
product: "WebViewGold pour iOS"
platform: "iOS"
category: "API et fonctionnalités"
slug: "iap-history"
canonical_url: "https://www.webviewgold.com/fr/docs/iOS/iap-history/"
keywords:
  - "API d'historique des achats"
  - "WebViewGold pour iOS"
  - "convertir un site web en app"
  - "documentation d’app WebView"
  - "SDK WebView iOS"
  - "PWA en app"
  - "HTML en app"
  - "pont JavaScript"
last_updated: "2026-10-09"
---

# API d'historique des achats In-App – WebViewGold pour iOS

> **Résumé :** Lisez les achats In-App précédents de l'utilisateur depuis votre application web au format JSON — parfait pour les pages « Mes achats ».

[Documentation](../README.md) › [WebViewGold pour iOS](README.md) › API d'historique des achats

**Plateforme :** iOS · **Catégorie :** API et fonctionnalités · **Version en ligne :** [www.webviewgold.com/fr/docs/iOS/iap-history/](https://www.webviewgold.com/fr/docs/iOS/iap-history/)

---

L'**API d'historique des achats In-App** renvoie la liste des achats précédents de l'utilisateur effectués via l'[API d'achats In-App](in-app-purchases.md) sur cet appareil et l'injecte dans votre application web sous la forme de `window.purchaseHistory`. Assurez-vous de posséder une [Extended License](credits.md) de WebViewGold si vous prévoyez d'utiliser cette fonctionnalité dans un produit final.

## Utilisation

```html
<a href="getpurchasehistory://" onclick="setTimeout(renderHistory, 300)">Mes achats</a>

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

## Format des données

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

`purchaseDateMs` est l'horodatage de l'achat en millisecondes Unix (sous forme de chaîne).

## Cas d'utilisation typiques

- Afficher une page « Mes abonnements » ou « Mes achats » dans votre application web.
- Déverrouiller du contenu premium côté client sur la base d'achats passés, sans solliciter votre backend.
- Flux de débogage et de support client.

**Remarques :** la liste contient les achats effectués dans l'application sur cet appareil. Elle est stockée localement et n'est donc pas synchronisée entre appareils — pour des vérifications de droits multi-appareils, validez plutôt les reçus sur votre serveur.

---

## Continuer la lecture

- ← Précédent : [API d'achats intégrés](in-app-purchases.md)
- Suivant → : [API de scanner de QR code](qr-code-scanner.md)
- Même fonctionnalité sur les autres plateformes : [Android – IAP History API](../android/iap-history.md)
- Langues : [🇺🇸 English](../../ios/iap-history.md) · [🇩🇪 Deutsch](../../de/ios/iap-history.md) · **🇫🇷 Français** · [🇪🇸 Español](../../es/ios/iap-history.md) · [🇨🇳 中文](../../zh/ios/iap-history.md)

> [!TIP]
> **Trop occupé ? Nous configurons votre app pour vous.** Notre équipe configure, compile & soumet votre app WebViewGold — clé en main, délai rapide, Made in Germany. [Faire configurer mon app →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **Compilez dans votre navigateur :** Pas de Mac, pas d’IDE : le **WebViewGold Cloud Builder** configure, compile & met en ligne votre app. [Découvrir Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
