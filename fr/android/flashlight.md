---
title: "API Lampe torche – Documentation WebViewGold pour Android"
description: "Contrôlez la lampe torche de l'appareil depuis votre application web avec de simples liens JavaScript dans WebViewGold pour Android."
lang: "fr"
product: "WebViewGold pour Android"
platform: "Android"
category: "API et fonctionnalités"
slug: "flashlight"
canonical_url: "https://www.webviewgold.com/fr/docs/android/flashlight/"
keywords:
  - "API Lampe torche"
  - "WebViewGold pour Android"
  - "convertir un site web en app"
  - "documentation d’app WebView"
  - "SDK WebView Android"
  - "PWA en app"
  - "HTML en app"
  - "pont JavaScript"
last_updated: "2026-10-09"
---

# API Lampe torche – WebViewGold pour Android

> **Résumé :** Contrôlez la lampe torche de l'appareil depuis votre application web avec de simples liens JavaScript dans WebViewGold pour Android.

[Documentation](../README.md) › [WebViewGold pour Android](README.md) › API Lampe torche

**Plateforme :** Android · **Catégorie :** API et fonctionnalités · **Version en ligne :** [www.webviewgold.com/fr/docs/android/flashlight/](https://www.webviewgold.com/fr/docs/android/flashlight/)

---

L'API Flashlight de WebViewGold permet à votre site web de contrôler la lampe torche de l'appareil. Cette fonctionnalité peut être utile pour :

- Créer des applications utilitaires nécessitant l'activation de la lampe torche
- Améliorer l'expérience utilisateur pendant l'utilisation de l'application grâce à la gamification
- Fournir des fonctionnalités d'accessibilité supplémentaires

## Utilisation

Vous pouvez activer ou désactiver la lampe torche directement depuis votre contenu HTML à l'aide des liens suivants :

```html
<a href="enableflashlight://">Turn On Flashlight</a>
<a href="disableflashlight://">Turn Off Flashlight</a>
```

**Remarque :** Assurez-vous que votre application dispose des permissions caméra requises dans AndroidManifest.xml, car la fonctionnalité de lampe torche est liée au matériel caméra de l'appareil.

---

## Continuer la lecture

- ← Précédent : [API UUID](uuid.md)
- Suivant → : [App Links / Deep Linking](app-links.md)
- Même fonctionnalité sur les autres plateformes : [iOS – API lampe torche](../ios/flashlight.md)
- Langues : [🇺🇸 English](../../android/flashlight.md) · [🇩🇪 Deutsch](../../de/android/flashlight.md) · **🇫🇷 Français** · [🇪🇸 Español](../../es/android/flashlight.md) · [🇨🇳 中文](../../zh/android/flashlight.md)

> [!TIP]
> **Trop occupé ? Nous configurons votre app pour vous.** Notre équipe configure, compile & soumet votre app WebViewGold — clé en main, délai rapide, Made in Germany. [Faire configurer mon app →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_android_doc_online)
>
> **Compilez dans votre navigateur :** Pas de Mac, pas d’IDE : le **WebViewGold Cloud Builder** configure, compile & met en ligne votre app. [Découvrir Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=android_docs)
