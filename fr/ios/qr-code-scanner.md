---
title: "API de scanner de QR code – Documentation WebViewGold pour iOS"
description: "Ouvrez un scanner de QR code natif depuis votre application web et traitez les résultats de scan via URL ou JavaScript."
lang: "fr"
product: "WebViewGold pour iOS"
platform: "iOS"
category: "API et fonctionnalités"
slug: "qr-code-scanner"
canonical_url: "https://www.webviewgold.com/fr/docs/iOS/qr-code-scanner/"
keywords:
  - "API de scanner de QR code"
  - "WebViewGold pour iOS"
  - "convertir un site web en app"
  - "documentation d’app WebView"
  - "SDK WebView iOS"
  - "PWA en app"
  - "HTML en app"
  - "pont JavaScript"
last_updated: "2026-10-09"
---

# API de scanner de QR code – WebViewGold pour iOS

> **Résumé :** Ouvrez un scanner de QR code natif depuis votre application web et traitez les résultats de scan via URL ou JavaScript.

[Documentation](../README.md) › [WebViewGold pour iOS](README.md) › API de scanner de QR code

**Plateforme :** iOS · **Catégorie :** API et fonctionnalités · **Version en ligne :** [www.webviewgold.com/fr/docs/iOS/qr-code-scanner/](https://www.webviewgold.com/fr/docs/iOS/qr-code-scanner/)

---

Pour déclencher le scanner de QR code au sein de votre application iOS basée sur WebView, utilisez le format de lien HTML suivant :

```html
<a href="qrcode://">Scanner un QR Code</a>
```

Cliquer sur ce lien ouvrira l'appareil photo du dispositif pour scanner un QR code, et toute URL encodée dans le QR code sera automatiquement chargée dans la WebView.

## Cas d'usage

- Faire le lien entre le contenu imprimé et le contenu numérique (par exemple, scanner un QR code depuis un magazine pour ouvrir une page web).
- Accès rapide aux promotions, informations produit ou événements.
- Diriger les utilisateurs en toute sécurité vers les ressources internes de l'application ou vers des pages de destination spécifiques.

---

## Continuer la lecture

- ← Précédent : [API d'historique des achats](iap-history.md)
- Suivant → : [API de scanner de codes-barres](barcode-scanner.md)
- Même fonctionnalité sur les autres plateformes : [Android – API scanner de QR codes](../android/qr-code-scanner.md)
- Langues : [🇺🇸 English](../../ios/qr-code-scanner.md) · [🇩🇪 Deutsch](../../de/ios/qr-code-scanner.md) · **🇫🇷 Français** · [🇪🇸 Español](../../es/ios/qr-code-scanner.md) · [🇨🇳 中文](../../zh/ios/qr-code-scanner.md)

> [!TIP]
> **Trop occupé ? Nous configurons votre app pour vous.** Notre équipe configure, compile & soumet votre app WebViewGold — clé en main, délai rapide, Made in Germany. [Faire configurer mon app →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **Compilez dans votre navigateur :** Pas de Mac, pas d’IDE : le **WebViewGold Cloud Builder** configure, compile & met en ligne votre app. [Découvrir Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
