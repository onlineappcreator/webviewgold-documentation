---
title: "API de mode de scan – Documentation WebViewGold pour iOS"
description: "Affinez le comportement de scan de la caméra du scanner de QR codes et de codes-barres dans WebViewGold pour iOS."
lang: "fr"
product: "WebViewGold pour iOS"
platform: "iOS"
category: "API et fonctionnalités"
slug: "scanning-mode"
canonical_url: "https://www.webviewgold.com/fr/docs/iOS/scanning-mode/"
keywords:
  - "API de mode de scan"
  - "WebViewGold pour iOS"
  - "convertir un site web en app"
  - "documentation d’app WebView"
  - "SDK WebView iOS"
  - "PWA en app"
  - "HTML en app"
  - "pont JavaScript"
last_updated: "2026-10-09"
---

# API de mode de scan – WebViewGold pour iOS

> **Résumé :** Affinez le comportement de scan de la caméra du scanner de QR codes et de codes-barres dans WebViewGold pour iOS.

[Documentation](../README.md) › [WebViewGold pour iOS](README.md) › API de mode de scan

**Plateforme :** iOS · **Catégorie :** API et fonctionnalités · **Version en ligne :** [www.webviewgold.com/fr/docs/iOS/scanning-mode/](https://www.webviewgold.com/fr/docs/iOS/scanning-mode/)

---

Si votre application web affiche à l'écran des informations destinées à être scannées (par exemple, un QR code), il peut être utile de régler la luminosité de l'écran à 100 % et d'empêcher l'écran de se mettre en veille. WebViewGold fournit l'API Scanning Mode pour activer dynamiquement ces conditions de numérisation optimales.\
Cette API comprend 3 commandes :

- « auto » = active le mode de numérisation et le désactive automatiquement lors d'une redirection de page.
- « on » = active le mode de numérisation, il reste activé après les redirections de page.
- « off » = désactive le mode de numérisation.

Liez ce type d'URL pour utiliser l'API Scanning Mode :

```html
<a href="scanningmode://auto">Activer le mode de numérisation ; sera automatiquement désactivé lors d'une redirection de page</a>
<a href="scanningmode://on">Activer le mode de numérisation ; restera actif jusqu'à désactivation manuelle</a>
<a href="scanningmode://off">Désactiver le mode de numérisation</a>
```

---

## Continuer la lecture

- ← Précédent : [API de scanner de codes-barres](barcode-scanner.md)
- Suivant → : [Scanner de documents](document-scanner.md)
- Même fonctionnalité sur les autres plateformes : [Android – API mode de scan](../android/scanning-mode.md)
- Langues : [🇺🇸 English](../../ios/scanning-mode.md) · [🇩🇪 Deutsch](../../de/ios/scanning-mode.md) · **🇫🇷 Français** · [🇪🇸 Español](../../es/ios/scanning-mode.md) · [🇨🇳 中文](../../zh/ios/scanning-mode.md)

> [!TIP]
> **Trop occupé ? Nous configurons votre app pour vous.** Notre équipe configure, compile & soumet votre app WebViewGold — clé en main, délai rapide, Made in Germany. [Faire configurer mon app →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **Compilez dans votre navigateur :** Pas de Mac, pas d’IDE : le **WebViewGold Cloud Builder** configure, compile & met en ligne votre app. [Découvrir Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
