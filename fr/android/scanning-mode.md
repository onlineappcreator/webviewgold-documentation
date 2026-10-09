---
title: "API mode de scan – Documentation WebViewGold pour Android"
description: "Ajustez finement le comportement de scan de la caméra du scanner de QR codes et de codes-barres dans WebViewGold pour Android."
lang: "fr"
product: "WebViewGold pour Android"
platform: "Android"
category: "API et fonctionnalités"
slug: "scanning-mode"
canonical_url: "https://www.webviewgold.com/fr/docs/android/scanning-mode/"
keywords:
  - "API mode de scan"
  - "WebViewGold pour Android"
  - "convertir un site web en app"
  - "documentation d’app WebView"
  - "SDK WebView Android"
  - "PWA en app"
  - "HTML en app"
  - "pont JavaScript"
last_updated: "2026-10-09"
---

# API mode de scan – WebViewGold pour Android

> **Résumé :** Ajustez finement le comportement de scan de la caméra du scanner de QR codes et de codes-barres dans WebViewGold pour Android.

[Documentation](../README.md) › [WebViewGold pour Android](README.md) › API mode de scan

**Plateforme :** Android · **Catégorie :** API et fonctionnalités · **Version en ligne :** [www.webviewgold.com/fr/docs/android/scanning-mode/](https://www.webviewgold.com/fr/docs/android/scanning-mode/)

---

Si votre application web affiche des informations à l'écran destinées à être scannées (par exemple, un QR code), il peut être utile d'augmenter la luminosité de l'écran à 100 % et d'empêcher la mise en veille de l'écran. WebViewGold fournit l'API Scanning Mode pour activer dynamiquement ces conditions de scan optimales.\
Cette API inclut 3 commandes :

- « auto » = active le mode scan et le désactive automatiquement lors d'une redirection de page.
- « on » = active le mode scan, qui reste actif après les redirections de page.
- « off » = désactive le mode scan.

Faites un lien vers ce type d'URL pour utiliser l'API Scanning Mode :

```html
<a href="scanningmode://auto">Enable Scanning Mode; will automatically disable on page redirect.</a>
<a href="scanningmode://on">Enable Scanning Mode; will persist until manually disabled.</a>
<a href="scanningmode://off">Disable Scanning Mode.</a>
```

---

## Continuer la lecture

- ← Précédent : [API scanner de QR codes](qr-code-scanner.md)
- Suivant → : [API scanner de codes-barres](barcode-scanner.md)
- Même fonctionnalité sur les autres plateformes : [iOS – API de mode de scan](../ios/scanning-mode.md)
- Langues : [🇺🇸 English](../../android/scanning-mode.md) · [🇩🇪 Deutsch](../../de/android/scanning-mode.md) · **🇫🇷 Français** · [🇪🇸 Español](../../es/android/scanning-mode.md) · [🇨🇳 中文](../../zh/android/scanning-mode.md)

> [!TIP]
> **Trop occupé ? Nous configurons votre app pour vous.** Notre équipe configure, compile & soumet votre app WebViewGold — clé en main, délai rapide, Made in Germany. [Faire configurer mon app →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_android_doc_online)
>
> **Compilez dans votre navigateur :** Pas de Mac, pas d’IDE : le **WebViewGold Cloud Builder** configure, compile & met en ligne votre app. [Découvrir Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=android_docs)
