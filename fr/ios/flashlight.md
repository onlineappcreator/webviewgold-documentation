---
title: "API lampe torche – Documentation WebViewGold pour iOS"
description: "Contrôlez la lampe torche de l'appareil depuis votre application web avec de simples liens JavaScript dans WebViewGold pour iOS."
lang: "fr"
product: "WebViewGold pour iOS"
platform: "iOS"
category: "API et fonctionnalités"
slug: "flashlight"
canonical_url: "https://www.webviewgold.com/fr/docs/iOS/flashlight/"
keywords:
  - "API lampe torche"
  - "WebViewGold pour iOS"
  - "convertir un site web en app"
  - "documentation d’app WebView"
  - "SDK WebView iOS"
  - "PWA en app"
  - "HTML en app"
  - "pont JavaScript"
last_updated: "2026-10-09"
---

# API lampe torche – WebViewGold pour iOS

> **Résumé :** Contrôlez la lampe torche de l'appareil depuis votre application web avec de simples liens JavaScript dans WebViewGold pour iOS.

[Documentation](../README.md) › [WebViewGold pour iOS](README.md) › API lampe torche

**Plateforme :** iOS · **Catégorie :** API et fonctionnalités · **Version en ligne :** [www.webviewgold.com/fr/docs/iOS/flashlight/](https://www.webviewgold.com/fr/docs/iOS/flashlight/)

---

L'API Flashlight de WebViewGold permet à votre site web de contrôler la lampe de poche (torche) de l'appareil. Cette fonctionnalité peut être utile pour :

- Créer des applications utilitaires nécessitant l'activation de la lampe de poche
- Améliorer l'expérience utilisateur pendant l'utilisation de l'application grâce à la ludification
- Proposer des fonctionnalités d'accessibilité supplémentaires

## Comment l'utiliser

Vous pouvez activer ou désactiver la lampe de poche directement depuis votre contenu HTML à l'aide des liens suivants :

```html
<a href="enableflashlight://">Activer la lampe de poche</a>
<a href="disableflashlight://">Désactiver la lampe de poche</a>
```

**Remarque :** assurez-vous que votre application dispose des autorisations d'accès à la caméra requises dans Info.plist, car la fonctionnalité de lampe de poche est liée au matériel de la caméra de l'appareil.

---

## Continuer la lecture

- ← Précédent : [API UUID](uuid.md)
- Suivant → : [API de réinitialisation de l'app](reset-app.md)
- Même fonctionnalité sur les autres plateformes : [Android – API Lampe torche](../android/flashlight.md)
- Langues : [🇺🇸 English](../../ios/flashlight.md) · [🇩🇪 Deutsch](../../de/ios/flashlight.md) · **🇫🇷 Français** · [🇪🇸 Español](../../es/ios/flashlight.md) · [🇨🇳 中文](../../zh/ios/flashlight.md)

> [!TIP]
> **Trop occupé ? Nous configurons votre app pour vous.** Notre équipe configure, compile & soumet votre app WebViewGold — clé en main, délai rapide, Made in Germany. [Faire configurer mon app →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **Compilez dans votre navigateur :** Pas de Mac, pas d’IDE : le **WebViewGold Cloud Builder** configure, compile & met en ligne votre app. [Découvrir Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
