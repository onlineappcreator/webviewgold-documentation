---
title: "API de réinitialisation de l'application – Documentation WebViewGold pour Android"
description: "Réinitialisez le cache, les cookies et le stockage local de votre application Android WebView d'un simple lien ou appel JavaScript."
lang: "fr"
product: "WebViewGold pour Android"
platform: "Android"
category: "API et fonctionnalités"
slug: "reset-app"
canonical_url: "https://www.webviewgold.com/fr/docs/android/reset-app/"
keywords:
  - "API de réinitialisation"
  - "WebViewGold pour Android"
  - "convertir un site web en app"
  - "documentation d’app WebView"
  - "SDK WebView Android"
  - "PWA en app"
  - "HTML en app"
  - "pont JavaScript"
last_updated: "2026-10-09"
---

# API de réinitialisation de l'application – WebViewGold pour Android

> **Résumé :** Réinitialisez le cache, les cookies et le stockage local de votre application Android WebView d'un simple lien ou appel JavaScript.

[Documentation](../README.md) › [WebViewGold pour Android](README.md) › API de réinitialisation

**Plateforme :** Android · **Catégorie :** API et fonctionnalités · **Version en ligne :** [www.webviewgold.com/fr/docs/android/reset-app/](https://www.webviewgold.com/fr/docs/android/reset-app/)

---

Dans certains cas, réinitialiser l'application à ses paramètres initiaux (en effaçant les cookies et le cache) peut être nécessaire pour restaurer des performances optimales. L'**API Reset App** offre un moyen simple d'initier cette réinitialisation.

## Utilisation

Pour réinitialiser les données de l'application, utilisez simplement le lien suivant dans votre application :

```html
<a href="reset://">Reset App Link</a>
```

Ce lien va :

- Effacer tous les cookies
- Effacer les données mises en cache

## Tester la fonctionnalité de réinitialisation

Pour tester cette fonctionnalité, ajoutez l'URL de démonstration suivante à votre application WebViewGold : <https://www.onlineappcreator.com/reset_test.html>

**Remarque :** Utilisez la fonctionnalité de réinitialisation de manière raisonnée, car elle effacera les données utilisateur liées aux cookies et au cache, ce qui pourrait affecter les paramètres enregistrés ou les données de session, y compris la déconnexion des utilisateurs des sessions actives.

---

## Continuer la lecture

- ← Précédent : [API vidéo native (PiP)](native-video.md)
- Suivant → : [API d'indicateur de chargement](loading-sign.md)
- Même fonctionnalité sur les autres plateformes : [iOS – API de réinitialisation de l'app](../ios/reset-app.md)
- Langues : [🇺🇸 English](../../android/reset-app.md) · [🇩🇪 Deutsch](../../de/android/reset-app.md) · **🇫🇷 Français** · [🇪🇸 Español](../../es/android/reset-app.md) · [🇨🇳 中文](../../zh/android/reset-app.md)

> [!TIP]
> **Trop occupé ? Nous configurons votre app pour vous.** Notre équipe configure, compile & soumet votre app WebViewGold — clé en main, délai rapide, Made in Germany. [Faire configurer mon app →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_android_doc_online)
>
> **Compilez dans votre navigateur :** Pas de Mac, pas d’IDE : le **WebViewGold Cloud Builder** configure, compile & met en ligne votre app. [Découvrir Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=android_docs)
