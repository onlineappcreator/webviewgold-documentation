---
title: "API scanner de QR codes – Documentation WebViewGold pour Android"
description: "Ouvrez un scanner de QR codes natif depuis votre application web et traitez les résultats via URL ou JavaScript."
lang: "fr"
product: "WebViewGold pour Android"
platform: "Android"
category: "API et fonctionnalités"
slug: "qr-code-scanner"
canonical_url: "https://www.webviewgold.com/fr/docs/android/qr-code-scanner/"
keywords:
  - "API scanner de QR codes"
  - "WebViewGold pour Android"
  - "convertir un site web en app"
  - "documentation d’app WebView"
  - "SDK WebView Android"
  - "PWA en app"
  - "HTML en app"
  - "pont JavaScript"
last_updated: "2026-10-09"
---

# API scanner de QR codes – WebViewGold pour Android

> **Résumé :** Ouvrez un scanner de QR codes natif depuis votre application web et traitez les résultats via URL ou JavaScript.

[Documentation](../README.md) › [WebViewGold pour Android](README.md) › API scanner de QR codes

**Plateforme :** Android · **Catégorie :** API et fonctionnalités · **Version en ligne :** [www.webviewgold.com/fr/docs/android/qr-code-scanner/](https://www.webviewgold.com/fr/docs/android/qr-code-scanner/)

---

Pour déclencher le scanner de QR code au sein de votre application Android basée sur WebView, utilisez le format de lien HTML suivant :

```html
<a href="qrcode://">Scan QR Code</a>
```

Un clic sur ce lien ouvre la caméra de l'appareil pour scanner un QR code, et toute URL encodée dans le QR code sera automatiquement chargée dans la WebView.

## Cas d'usage

- Faire le pont entre le contenu imprimé et numérique (par exemple, scanner un QR code d'un magazine pour ouvrir une page web).
- Accès rapide à des promotions, des informations produits ou des évènements.
- Relier les utilisateurs de manière sécurisée à des ressources internes de l'application ou à des pages d'atterrissage spécifiques.

---

## Continuer la lecture

- ← Précédent : [IAP History API](iap-history.md)
- Suivant → : [API mode de scan](scanning-mode.md)
- Même fonctionnalité sur les autres plateformes : [iOS – API de scanner de QR code](../ios/qr-code-scanner.md)
- Langues : [🇺🇸 English](../../android/qr-code-scanner.md) · [🇩🇪 Deutsch](../../de/android/qr-code-scanner.md) · **🇫🇷 Français** · [🇪🇸 Español](../../es/android/qr-code-scanner.md) · [🇨🇳 中文](../../zh/android/qr-code-scanner.md)

> [!TIP]
> **Trop occupé ? Nous configurons votre app pour vous.** Notre équipe configure, compile & soumet votre app WebViewGold — clé en main, délai rapide, Made in Germany. [Faire configurer mon app →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_android_doc_online)
>
> **Compilez dans votre navigateur :** Pas de Mac, pas d’IDE : le **WebViewGold Cloud Builder** configure, compile & met en ligne votre app. [Découvrir Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=android_docs)
