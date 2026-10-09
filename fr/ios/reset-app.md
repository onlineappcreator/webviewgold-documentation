---
title: "API de réinitialisation de l'app – Documentation WebViewGold pour iOS"
description: "Réinitialisez le cache, les cookies et le stockage local de votre application WebView iOS avec un simple lien ou appel JavaScript."
lang: "fr"
product: "WebViewGold pour iOS"
platform: "iOS"
category: "API et fonctionnalités"
slug: "reset-app"
canonical_url: "https://www.webviewgold.com/fr/docs/iOS/reset-app/"
keywords:
  - "API de réinitialisation de l'app"
  - "WebViewGold pour iOS"
  - "convertir un site web en app"
  - "documentation d’app WebView"
  - "SDK WebView iOS"
  - "PWA en app"
  - "HTML en app"
  - "pont JavaScript"
last_updated: "2026-10-09"
---

# API de réinitialisation de l'app – WebViewGold pour iOS

> **Résumé :** Réinitialisez le cache, les cookies et le stockage local de votre application WebView iOS avec un simple lien ou appel JavaScript.

[Documentation](../README.md) › [WebViewGold pour iOS](README.md) › API de réinitialisation de l'app

**Plateforme :** iOS · **Catégorie :** API et fonctionnalités · **Version en ligne :** [www.webviewgold.com/fr/docs/iOS/reset-app/](https://www.webviewgold.com/fr/docs/iOS/reset-app/)

---

Dans certains cas, la réinitialisation de l'application à ses paramètres initiaux (par effacement des cookies et du cache) peut être nécessaire pour rétablir des performances optimales. L'**API Reset App** offre un moyen simple d'initier cette réinitialisation.

## Utilisation

Pour réinitialiser les données de l'application, utilisez simplement le lien suivant dans votre application :

```html
<a href="reset://">Lien de réinitialisation de l'application</a>
```

Ce lien va :

- Effacer tous les cookies
- Effacer les données mises en cache

## Tester la fonctionnalité de réinitialisation

Pour tester cette fonctionnalité, ajoutez l'URL de démonstration suivante à votre application WebViewGold : <https://www.onlineappcreator.com/reset_test.html>

**Remarque :** utilisez la fonctionnalité de réinitialisation avec discernement, car elle effacera les données utilisateur liées aux cookies et au cache, ce qui pourrait affecter les paramètres enregistrés ou les données de session, y compris la déconnexion des utilisateurs des sessions actives.

---

## Continuer la lecture

- ← Précédent : [API lampe torche](flashlight.md)
- Suivant → : [API de décision de suivi](user-tracking.md)
- Même fonctionnalité sur les autres plateformes : [Android – API de réinitialisation](../android/reset-app.md)
- Langues : [🇺🇸 English](../../ios/reset-app.md) · [🇩🇪 Deutsch](../../de/ios/reset-app.md) · **🇫🇷 Français** · [🇪🇸 Español](../../es/ios/reset-app.md) · [🇨🇳 中文](../../zh/ios/reset-app.md)

> [!TIP]
> **Trop occupé ? Nous configurons votre app pour vous.** Notre équipe configure, compile & soumet votre app WebViewGold — clé en main, délai rapide, Made in Germany. [Faire configurer mon app →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **Compilez dans votre navigateur :** Pas de Mac, pas d’IDE : le **WebViewGold Cloud Builder** configure, compile & met en ligne votre app. [Découvrir Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
