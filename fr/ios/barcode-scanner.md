---
title: "API de scanner de codes-barres – Documentation WebViewGold pour iOS"
description: "Scannez des codes-barres EAN, UPC et autres nativement dans votre application WebView iOS et transmettez les résultats à votre application web."
lang: "fr"
product: "WebViewGold pour iOS"
platform: "iOS"
category: "API et fonctionnalités"
slug: "barcode-scanner"
canonical_url: "https://www.webviewgold.com/fr/docs/iOS/barcode-scanner/"
keywords:
  - "API de scanner de codes-barres"
  - "WebViewGold pour iOS"
  - "convertir un site web en app"
  - "documentation d’app WebView"
  - "SDK WebView iOS"
  - "PWA en app"
  - "HTML en app"
  - "pont JavaScript"
last_updated: "2026-10-09"
---

# API de scanner de codes-barres – WebViewGold pour iOS

> **Résumé :** Scannez des codes-barres EAN, UPC et autres nativement dans votre application WebView iOS et transmettez les résultats à votre application web.

[Documentation](../README.md) › [WebViewGold pour iOS](README.md) › API de scanner de codes-barres

**Plateforme :** iOS · **Catégorie :** API et fonctionnalités · **Version en ligne :** [www.webviewgold.com/fr/docs/iOS/barcode-scanner/](https://www.webviewgold.com/fr/docs/iOS/barcode-scanner/)

---

L'API Barcode Scanner de WebViewGold permet à votre application basée sur WebView d'activer la caméra de l'appareil pour scanner des codes-barres. Une fois qu'un code-barres est scanné avec succès, le résultat est automatiquement renvoyé dans votre contenu web.

## Cas d'usage

- Scanner les codes-barres de produits pour les systèmes d'inventaire
- Traiter des billets ou des codes d'accès dans des applications de logistique ou d'événementiel
- Permettre une saisie rapide des données à partir de codes-barres imprimés

## Comment déclencher le scanner

Utilisez le code HTML suivant pour démarrer le scanner de codes-barres natif :

```html
<a href="barcodescanner://">Start Barcode Scanner</a>
<a href="#" onClick="alert(barcodescanresult);">Show Scan Result</a>
```

- **Start Barcode Scanner :** ouvre la caméra de l'appareil pour détecter les formats de codes-barres pris en charge
- **Show Scan Result :** affiche le contenu du code-barres scanné, stocké dans la variable JavaScript `barcodescanresult`

**Note technique :** après la lecture, la valeur décodée du code-barres est injectée dans la page actuelle via la variable JavaScript `barcodescanresult`. Vous pouvez utiliser cette variable pour préremplir des formulaires, déclencher une logique personnalisée ou effectuer des recherches basées sur les données scannées.

**Autorisations :** assurez-vous que l'application a accès à la caméra de l'appareil, car celle-ci est nécessaire au bon fonctionnement de la lecture des codes-barres.

---

## Continuer la lecture

- ← Précédent : [API de scanner de QR code](qr-code-scanner.md)
- Suivant → : [API de mode de scan](scanning-mode.md)
- Même fonctionnalité sur les autres plateformes : [Android – API scanner de codes-barres](../android/barcode-scanner.md)
- Langues : [🇺🇸 English](../../ios/barcode-scanner.md) · [🇩🇪 Deutsch](../../de/ios/barcode-scanner.md) · **🇫🇷 Français** · [🇪🇸 Español](../../es/ios/barcode-scanner.md) · [🇨🇳 中文](../../zh/ios/barcode-scanner.md)

> [!TIP]
> **Trop occupé ? Nous configurons votre app pour vous.** Notre équipe configure, compile & soumet votre app WebViewGold — clé en main, délai rapide, Made in Germany. [Faire configurer mon app →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **Compilez dans votre navigateur :** Pas de Mac, pas d’IDE : le **WebViewGold Cloud Builder** configure, compile & met en ligne votre app. [Découvrir Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
