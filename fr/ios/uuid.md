---
title: "API UUID – Documentation WebViewGold pour iOS"
description: "Identifiez les installations de l'app avec un UUID unique ajouté à votre URL WebView ou récupéré via JavaScript."
lang: "fr"
product: "WebViewGold pour iOS"
platform: "iOS"
category: "API et fonctionnalités"
slug: "uuid"
canonical_url: "https://www.webviewgold.com/fr/docs/iOS/uuid/"
keywords:
  - "API UUID"
  - "WebViewGold pour iOS"
  - "convertir un site web en app"
  - "documentation d’app WebView"
  - "SDK WebView iOS"
  - "PWA en app"
  - "HTML en app"
  - "pont JavaScript"
last_updated: "2026-10-09"
---

# API UUID – WebViewGold pour iOS

> **Résumé :** Identifiez les installations de l'app avec un UUID unique ajouté à votre URL WebView ou récupéré via JavaScript.

[Documentation](../README.md) › [WebViewGold pour iOS](README.md) › API UUID

**Plateforme :** iOS · **Catégorie :** API et fonctionnalités · **Version en ligne :** [www.webviewgold.com/fr/docs/iOS/uuid/](https://www.webviewgold.com/fr/docs/iOS/uuid/)

---

L'API UUID de WebViewGold vous permet de récupérer un identifiant d'appareil unique et non personnel (UUID - « Universally Unique Identifier »), capable d'**identifier de manière unique un appareil iOS**. Cette fonctionnalité peut être utile pour :

- Stocker sur le serveur des paramètres spécifiques à l'utilisateur
- Maintenir les états de session
- Retrouver les données enregistrées côté client

**Note sur la confidentialité :** veillez à respecter les **lois locales et internationales sur la protection de la vie privée** lors de l'utilisation de cette fonctionnalité, car elle implique l'identification de l'appareil.

## Comment récupérer l'UUID

Pour récupérer l'UUID depuis votre application basée sur WebView, utilisez le code suivant :

```html
<a href="get-uuid://">Obtenir l'UUID</a>
<a href="#" onClick="alert(uuid);">Afficher l'UUID</a>
```

- **Obtenir l'UUID :** demande l'UUID à WebViewGold.
- **Afficher l'UUID :** affiche l'UUID via une **alerte** pour un test facile.

## Méthode alternative : ajouter l'UUID à l'URL de la WebView

Si vous préférez inclure l'UUID dans les paramètres de l'URL, activez l'option `enhanceUrlUUID` dans **Config.swift** en la définissant sur `true`. Cela ajoutera automatiquement `uuid=XYZ` à l'URL de votre WebView lors de la première requête, vous permettant d'accéder à l'UUID directement dans votre contenu web :

- **Exemple :** si l'URL de votre WebView est `https://www.example.org`, elle sera requêtée sous la forme `https://www.example.org?uuid=XYZ`.
- **Remarque :** seule la requête d'URL initiale inclura ce paramètre GET, pensez donc à l'enregistrer dans une session ou un cookie si vous devez y faire référence plus tard dans l'application.

## Injecter automatiquement l'UUID dans JavaScript

Pour rendre automatiquement l'UUID (et d'autres variables) disponibles en JavaScript sur toutes les pages sans modifier les URL, définissez `autoInjectVariable` sur `true` dans **Config.swift**. Cela vous permet d'accéder directement à l'UUID et à d'autres valeurs depuis n'importe quelle page.

---

## Continuer la lecture

- ← Précédent : [API de cartes Apple Wallet](wallet-pass.md)
- Suivant → : [API lampe torche](flashlight.md)
- Même fonctionnalité sur les autres plateformes : [Android – API UUID](../android/uuid.md) · [macOS – API UUID](../macos/uuid.md)
- Langues : [🇺🇸 English](../../ios/uuid.md) · [🇩🇪 Deutsch](../../de/ios/uuid.md) · **🇫🇷 Français** · [🇪🇸 Español](../../es/ios/uuid.md) · [🇨🇳 中文](../../zh/ios/uuid.md)

> [!TIP]
> **Trop occupé ? Nous configurons votre app pour vous.** Notre équipe configure, compile & soumet votre app WebViewGold — clé en main, délai rapide, Made in Germany. [Faire configurer mon app →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **Compilez dans votre navigateur :** Pas de Mac, pas d’IDE : le **WebViewGold Cloud Builder** configure, compile & met en ligne votre app. [Découvrir Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
