---
title: "API de géolocalisation HTML5 – Documentation WebViewGold pour iOS"
description: "Activez la géolocalisation HTML5 dans votre application WebView iOS et demandez les autorisations de localisation précise de la bonne manière."
lang: "fr"
product: "WebViewGold pour iOS"
platform: "iOS"
category: "API et fonctionnalités"
slug: "geolocation"
canonical_url: "https://www.webviewgold.com/fr/docs/iOS/geolocation/"
keywords:
  - "API de géolocalisation"
  - "WebViewGold pour iOS"
  - "convertir un site web en app"
  - "documentation d’app WebView"
  - "SDK WebView iOS"
  - "PWA en app"
  - "HTML en app"
  - "pont JavaScript"
last_updated: "2026-10-09"
---

# API de géolocalisation HTML5 – WebViewGold pour iOS

> **Résumé :** Activez la géolocalisation HTML5 dans votre application WebView iOS et demandez les autorisations de localisation précise de la bonne manière.

[Documentation](../README.md) › [WebViewGold pour iOS](README.md) › API de géolocalisation

**Plateforme :** iOS · **Catégorie :** API et fonctionnalités · **Version en ligne :** [www.webviewgold.com/fr/docs/iOS/geolocation/](https://www.webviewgold.com/fr/docs/iOS/geolocation/)

---

L'API de géolocalisation HTML5 permet aux utilisateurs de partager leur position avec votre application, enrichissant des fonctionnalités telles que le contenu basé sur la localisation. Dans WebViewGold, l'API de géolocalisation est prise en charge par défaut une fois intégrée à votre contenu web. Voici comment implémenter le suivi de géolocalisation dans votre application iOS basée sur WebView :

## Configurer la géolocalisation HTML5

Pour une configuration de base de la géolocalisation, consultez le [guide de géolocalisation de Mozilla](https://developer.mozilla.org/en-US/docs/Web/API/Geolocation_API) pour savoir comment implémenter cette fonctionnalité dans votre site web ou votre application web.

Pour une démonstration, visitez cette [démo de géolocalisation W3Schools](https://www.w3schools.com/html/html5_geolocation.asp).

Depuis iOS 10, la géolocalisation n'est disponible que pour les sites en https ; veillez donc à utiliser une URL d'application web commençant par `https://` au lieu de `http://` lorsque vous effectuez des requêtes de localisation.

## Accès à la localisation en arrière-plan

Par défaut, les requêtes de localisation ne fonctionnent que lorsque l'app est au premier plan. Si votre app web doit continuer à recevoir des mises à jour de position lorsque l'app est en arrière-plan (p. ex. pour des cas d'usage de suivi ou de géorepérage), activez l'option de localisation en arrière-plan dans **Config.swift** :

```swift
static let backgroundlocation = true
```

- Dans les réglages du projet Xcode, ajoutez la capacité **Background Modes** à la cible WebViewGold et cochez **Location updates**.
- Selon votre app web, vous devrez peut-être aussi activer **Background Processing**. Dans ce cas, ajoutez également un tableau avec la clé `Permitted background task scheduler identifiers` à votre **Info.plist** et incluez-y une chaîne avec l'identifiant de bundle de votre app (p. ex. `com.yourcompany.yourapp`).
- Gardez à l'esprit que l'accès à la localisation en arrière-plan exige une justification claire lors de la revue App Store — décrivez le bénéfice pour l'utilisateur dans vos notes de revue.

---

## Continuer la lecture

- ← Précédent : [Modifier la Safe Area](safe-area.md)
- Suivant → : [API de notifications push](push-notifications.md)
- Même fonctionnalité sur les autres plateformes : [Android – API de géolocalisation](../android/geolocation.md)
- Langues : [🇺🇸 English](../../ios/geolocation.md) · [🇩🇪 Deutsch](../../de/ios/geolocation.md) · **🇫🇷 Français** · [🇪🇸 Español](../../es/ios/geolocation.md) · [🇨🇳 中文](../../zh/ios/geolocation.md)

> [!TIP]
> **Trop occupé ? Nous configurons votre app pour vous.** Notre équipe configure, compile & soumet votre app WebViewGold — clé en main, délai rapide, Made in Germany. [Faire configurer mon app →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **Compilez dans votre navigateur :** Pas de Mac, pas d’IDE : le **WebViewGold Cloud Builder** configure, compile & met en ligne votre app. [Découvrir Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
