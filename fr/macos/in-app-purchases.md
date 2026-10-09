---
title: "API In-App Purchase & In-App Subscription – WebViewGold pour macOS Documentation"
description: "Vendez des achats intégrés et abonnements du Mac App Store depuis votre app web : ajoutez l'ID produit dans Constants.h et déclenchez l'achat avec un lien inapppurchase://."
lang: "fr"
product: "WebViewGold pour macOS"
platform: "macOS"
category: "API et fonctionnalités"
slug: "in-app-purchases"
canonical_url: "https://www.webviewgold.com/fr/docs/mac/#inapppurchases"
keywords:
  - "API In-App Purchases"
  - "WebViewGold pour macOS"
  - "convertir un site web en app"
  - "documentation d’app WebView"
  - "SDK WebView macOS"
  - "PWA en app"
  - "HTML en app"
  - "pont JavaScript"
last_updated: "2026-10-09"
---

# API In-App Purchase & In-App Subscription – WebViewGold pour macOS

> **Résumé :** Vendez des achats intégrés et abonnements du Mac App Store depuis votre app web : ajoutez l'ID produit dans Constants.h et déclenchez l'achat avec un lien inapppurchase://.

[Documentation](../README.md) › [WebViewGold pour macOS](README.md) › API In-App Purchases

**Plateforme :** macOS · **Catégorie :** API et fonctionnalités · **Version en ligne :** [www.webviewgold.com/fr/docs/mac/#inapppurchases](https://www.webviewgold.com/fr/docs/mac/#inapppurchases)

---

Dans certaines applications macOS/Mac, vous pouvez acheter du contenu ou des services supplémentaires. Ce type d'achats est appelé « in-app purchases ». Ils peuvent constituer une source de revenus intéressante pour les développeurs et sont très pratiques pour les clients, car ils utilisent des comptes et des sources de paiement existants pour le règlement. WebViewGold permet de déclencher les In-App Purchases du Mac App Store. Ajoutez simplement votre In-App Purchase Product ID (obtenu depuis *App Store Connect*) dans le fichier *Constants.h* : \
![Mac App Store In-App Purchase Product ID dans le fichier Constants.h](../../assets/macos/img/inapppurchase.png)\
Créez ensuite un lien vers ce type d'URL :

```html
<a href="inapppurchase://?successful_url=https://www.google.com">Buy In-App Purchase</a>
```

Vous pouvez également utiliser ce type d'URL pour les produits d'abonnement :

```html
<a href="inappsubscription://?successful_url=https://www.google.com&expired_url=https://www.yahoo.com">Start In-App Subscription</a>
```

Dans cet exemple d'URL, https://www.google.com doit être appelé après l'activation réussie de l'abonnement, et https://www.yahoo.com doit être appelé dès que l'abonnement expire.

---

## Continuer la lecture

- ← Précédent : [Écran de démarrage](splash-screen.md)
- Suivant → : [API UUID](uuid.md)
- Même fonctionnalité sur les autres plateformes : [iOS – API d'achats intégrés](../ios/in-app-purchases.md) · [Android – API d'achats intégrés](../android/in-app-purchases.md)
- Langues : [🇺🇸 English](../../macos/in-app-purchases.md) · [🇩🇪 Deutsch](../../de/macos/in-app-purchases.md) · **🇫🇷 Français** · [🇪🇸 Español](../../es/macos/in-app-purchases.md) · [🇨🇳 中文](../../zh/macos/in-app-purchases.md)

