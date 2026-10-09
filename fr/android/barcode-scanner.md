---
title: "API scanner de codes-barres – Documentation WebViewGold pour Android"
description: "Scannez les codes-barres EAN, UPC et autres nativement dans votre application Android WebView et transmettez les résultats à votre application web."
lang: "fr"
product: "WebViewGold pour Android"
platform: "Android"
category: "API et fonctionnalités"
slug: "barcode-scanner"
canonical_url: "https://www.webviewgold.com/fr/docs/android/barcode-scanner/"
keywords:
  - "API scanner de codes-barres"
  - "WebViewGold pour Android"
  - "convertir un site web en app"
  - "documentation d’app WebView"
  - "SDK WebView Android"
  - "PWA en app"
  - "HTML en app"
  - "pont JavaScript"
last_updated: "2026-10-09"
---

# API scanner de codes-barres – WebViewGold pour Android

> **Résumé :** Scannez les codes-barres EAN, UPC et autres nativement dans votre application Android WebView et transmettez les résultats à votre application web.

[Documentation](../README.md) › [WebViewGold pour Android](README.md) › API scanner de codes-barres

**Plateforme :** Android · **Catégorie :** API et fonctionnalités · **Version en ligne :** [www.webviewgold.com/fr/docs/android/barcode-scanner/](https://www.webviewgold.com/fr/docs/android/barcode-scanner/)

---

L'API Barcode Scanner de WebViewGold permet à votre application basée sur WebView d'activer la caméra de l'appareil pour scanner des codes-barres. Une fois un code-barres scanné avec succès, le résultat est automatiquement renvoyé dans votre contenu web.

## Cas d'usage

- Scanner les codes-barres de produits pour les systèmes de gestion des stocks
- Traiter des tickets ou des codes d'accès dans les applications de logistique ou d'événementiel
- Permettre une saisie rapide des données à partir de codes-barres imprimés

## Comment déclencher le scanner

Utilisez le code HTML suivant pour lancer le scanner de codes-barres natif :

```html
<a href="barcodescanner://">Start Barcode Scanner</a>
<a href="#" onClick="alert(barcodescanresult);">Show Scan Result</a>
```

- **Démarrer le scanner de codes-barres :** Ouvre la caméra de l'appareil pour détecter les formats de codes-barres pris en charge
- **Afficher le résultat du scan :** Affiche le contenu du code-barres scanné, stocké dans la variable JavaScript `barcodescanresult`

**Note technique :** Après le scan, la valeur décodée du code-barres est injectée dans la page actuelle via la variable JavaScript `barcodescanresult`. Vous pouvez utiliser cette variable pour préremplir des formulaires, déclencher une logique personnalisée ou effectuer des recherches à partir des données scannées.

**Autorisations :** Assurez-vous que l'application a accès à la caméra de l'appareil, car celle-ci est requise pour que le scan de codes-barres fonctionne correctement.

---

## Continuer la lecture

- ← Précédent : [API mode de scan](scanning-mode.md)
- Suivant → : [API de capture d'écran](take-screenshot.md)
- Même fonctionnalité sur les autres plateformes : [iOS – API de scanner de codes-barres](../ios/barcode-scanner.md)
- Langues : [🇺🇸 English](../../android/barcode-scanner.md) · [🇩🇪 Deutsch](../../de/android/barcode-scanner.md) · **🇫🇷 Français** · [🇪🇸 Español](../../es/android/barcode-scanner.md) · [🇨🇳 中文](../../zh/android/barcode-scanner.md)

> [!TIP]
> **Trop occupé ? Nous configurons votre app pour vous.** Notre équipe configure, compile & soumet votre app WebViewGold — clé en main, délai rapide, Made in Germany. [Faire configurer mon app →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_android_doc_online)
>
> **Compilez dans votre navigateur :** Pas de Mac, pas d’IDE : le **WebViewGold Cloud Builder** configure, compile & met en ligne votre app. [Découvrir Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=android_docs)
