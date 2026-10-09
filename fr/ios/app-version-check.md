---
title: "API de vérification de version de l'app – Documentation WebViewGold pour iOS"
description: "Détectez la version installée de l'app depuis votre application web et invitez les utilisateurs à la mettre à jour si nécessaire."
lang: "fr"
product: "WebViewGold pour iOS"
platform: "iOS"
category: "API et fonctionnalités"
slug: "app-version-check"
canonical_url: "https://www.webviewgold.com/fr/docs/iOS/app-version-check/"
keywords:
  - "API de vérification de version"
  - "WebViewGold pour iOS"
  - "convertir un site web en app"
  - "documentation d’app WebView"
  - "SDK WebView iOS"
  - "PWA en app"
  - "HTML en app"
  - "pont JavaScript"
last_updated: "2026-10-09"
---

# API de vérification de version de l'app – WebViewGold pour iOS

> **Résumé :** Détectez la version installée de l'app depuis votre application web et invitez les utilisateurs à la mettre à jour si nécessaire.

[Documentation](../README.md) › [WebViewGold pour iOS](README.md) › API de vérification de version

**Plateforme :** iOS · **Catégorie :** API et fonctionnalités · **Version en ligne :** [www.webviewgold.com/fr/docs/iOS/app-version-check/](https://www.webviewgold.com/fr/docs/iOS/app-version-check/)

---

Grâce à cette approche de l'API JavaScript de WebViewGold, votre site web / application web peut **récupérer la version de l'application iOS** utilisée par l'utilisateur de votre application. Cela est particulièrement utile si vous souhaitez inviter les utilisateurs d'une version plus ancienne à mettre à jour leur application. De plus, vous pouvez masquer les sections de l'application web qui nécessitent des fonctionnalités prises en charge par une version spécifique de l'application.\
Utilisez JavaScript avec ce type d'URL pour lire et afficher la version de l'application ainsi que son numéro de build :

```html
<script>
window.location.href = "getappversion://";
alert(versionNumber);
alert(bundleNumber);
</script>
```

**Vous pouvez également passer `autoInjectVariable` à `true` dans Config.swift afin d'injecter automatiquement cette valeur (et d'autres) dans JavaScript sans avoir à appeler une URL au préalable.**

---

## Continuer la lecture

- ← Précédent : [API de capture d'écran](take-screenshot.md)
- Suivant → : [API d'UI dynamique](dynamic-ui.md)
- Même fonctionnalité sur les autres plateformes : [Android – API de vérification de version](../android/app-version-check.md)
- Langues : [🇺🇸 English](../../ios/app-version-check.md) · [🇩🇪 Deutsch](../../de/ios/app-version-check.md) · **🇫🇷 Français** · [🇪🇸 Español](../../es/ios/app-version-check.md) · [🇨🇳 中文](../../zh/ios/app-version-check.md)

> [!TIP]
> **Trop occupé ? Nous configurons votre app pour vous.** Notre équipe configure, compile & soumet votre app WebViewGold — clé en main, délai rapide, Made in Germany. [Faire configurer mon app →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **Compilez dans votre navigateur :** Pas de Mac, pas d’IDE : le **WebViewGold Cloud Builder** configure, compile & met en ligne votre app. [Découvrir Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
