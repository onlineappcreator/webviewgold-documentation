---
title: "API de cartes Apple Wallet – Documentation WebViewGold pour iOS"
description: "Permettez aux utilisateurs d'ajouter des cartes .pkpass (billets, coupons, cartes de membre) depuis votre application web à Apple Wallet."
lang: "fr"
product: "WebViewGold pour iOS"
platform: "iOS"
category: "API et fonctionnalités"
slug: "wallet-pass"
canonical_url: "https://www.webviewgold.com/fr/docs/iOS/wallet-pass/"
keywords:
  - "API de cartes Apple Wallet"
  - "WebViewGold pour iOS"
  - "convertir un site web en app"
  - "documentation d’app WebView"
  - "SDK WebView iOS"
  - "PWA en app"
  - "HTML en app"
  - "pont JavaScript"
last_updated: "2026-10-09"
---

# API de cartes Apple Wallet – WebViewGold pour iOS

> **Résumé :** Permettez aux utilisateurs d'ajouter des cartes .pkpass (billets, coupons, cartes de membre) depuis votre application web à Apple Wallet.

[Documentation](../README.md) › [WebViewGold pour iOS](README.md) › API de cartes Apple Wallet

**Plateforme :** iOS · **Catégorie :** API et fonctionnalités · **Version en ligne :** [www.webviewgold.com/fr/docs/iOS/wallet-pass/](https://www.webviewgold.com/fr/docs/iOS/wallet-pass/)

---

L'**API de cartes Apple Wallet** permet à votre application web de transmettre un fichier `.pkpass` (billet d'événement, carte d'embarquement, coupon, carte de fidélité ou d'adhésion) à l'utilisateur afin qu'il puisse l'ajouter à **Apple Wallet**.

## Utilisation

Créez un lien vers votre fichier `.pkpass`, mais remplacez le préfixe `https://` de l'URL du fichier par `addpkpass://` :

```html
<a href="addpkpass://example.com/passes/ticket.pkpass">Ajouter le billet à Apple Wallet</a>
```

## Fonctionnement

1. L'application reconvertit le lien `addpkpass://` en URL `https://`.
2. L'URL de la carte s'ouvre dans un onglet de navigateur intégré, qui reconnaît le contenu `.pkpass` et affiche l'aperçu natif **Ajouter à Apple Wallet**.
3. L'utilisateur confirme et la carte est enregistrée dans l'application Wallet.

**Remarques :** la carte doit être servie via HTTPS avec le type MIME correct `application/vnd.apple.pkpass` et signée avec un certificat Apple Pass Type ID valide (consultez la [documentation Apple Wallet Passes](https://developer.apple.com/documentation/walletpasses) pour savoir comment générer des cartes).

---

## Continuer la lecture

- ← Précédent : [API calendrier iCal](ical-calendar.md)
- Suivant → : [API UUID](uuid.md)
- Langues : [🇺🇸 English](../../ios/wallet-pass.md) · [🇩🇪 Deutsch](../../de/ios/wallet-pass.md) · **🇫🇷 Français** · [🇪🇸 Español](../../es/ios/wallet-pass.md) · [🇨🇳 中文](../../zh/ios/wallet-pass.md)

> [!TIP]
> **Trop occupé ? Nous configurons votre app pour vous.** Notre équipe configure, compile & soumet votre app WebViewGold — clé en main, délai rapide, Made in Germany. [Faire configurer mon app →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **Compilez dans votre navigateur :** Pas de Mac, pas d’IDE : le **WebViewGold Cloud Builder** configure, compile & met en ligne votre app. [Découvrir Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
