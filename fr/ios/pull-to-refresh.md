---
title: "API Pull-to-Refresh – Documentation WebViewGold pour iOS"
description: "Activez le geste natif « tirer pour actualiser » dans votre app WebView iOS, personnalisez ses couleurs et basculez-le dynamiquement depuis votre app web."
lang: "fr"
product: "WebViewGold pour iOS"
platform: "iOS"
category: "API et fonctionnalités"
slug: "pull-to-refresh"
canonical_url: "https://www.webviewgold.com/fr/docs/iOS/pull-to-refresh/"
keywords:
  - "API Pull-to-Refresh"
  - "WebViewGold pour iOS"
  - "convertir un site web en app"
  - "documentation d’app WebView"
  - "SDK WebView iOS"
  - "PWA en app"
  - "HTML en app"
  - "pont JavaScript"
last_updated: "2026-10-09"
---

# API Pull-to-Refresh – WebViewGold pour iOS

> **Résumé :** Activez le geste natif « tirer pour actualiser » dans votre app WebView iOS, personnalisez ses couleurs et basculez-le dynamiquement depuis votre app web.

[Documentation](../README.md) › [WebViewGold pour iOS](README.md) › API Pull-to-Refresh

**Plateforme :** iOS · **Catégorie :** API et fonctionnalités · **Version en ligne :** [www.webviewgold.com/fr/docs/iOS/pull-to-refresh/](https://www.webviewgold.com/fr/docs/iOS/pull-to-refresh/)

---

L'**API Pull-to-Refresh** ajoute le geste natif iOS « tirer pour actualiser » à votre app WebView : les utilisateurs tirent la page vers le bas pour recharger l'URL actuelle — exactement comme dans les apps natives telles que Mail ou Safari.

## Activation

Ouvrez **Config.swift** et définissez :

```swift
var pulltorefresh = true
var preventoverscroll = false
```

- `pulltorefresh` active le contrôle d'actualisation natif.
- `preventoverscroll` doit être défini sur `false` — le geste a besoin de l'animation de rebond (overscroll) de la WebView pour fonctionner.

## Personnaliser les couleurs

Vous pouvez styliser l'indicateur de chargement et son arrière-plan séparément pour les modes clair et sombre dans **Config.swift** :

```swift
var pulltorefresh_loadingsigncolour_lightmode = #colorLiteral(...)
var pulltorefresh_backgroundcolour_lightmode = #colorLiteral(...)
var pulltorefresh_loadingsigncolour_darkmode = #colorLiteral(...)
var pulltorefresh_backgroundcolour_darkmode = #colorLiteral(...)
```

Astuce : cliquez sur la pastille de couleur à côté de chaque `#colorLiteral` dans Xcode pour choisir une couleur visuellement. Les variantes du mode sombre nécessitent iOS 13 ou une version ultérieure.

## Basculer dynamiquement depuis votre app web

Vous pouvez activer ou désactiver le pull-to-refresh à l'exécution — par exemple pour le désactiver sur des pages avec leurs propres gestes de balayage (cartes, sliders, jeux) :

```html
<a href="enablepulltorefresh://">Activer le pull-to-refresh</a>
<a href="disablepulltorefresh://">Désactiver le pull-to-refresh</a>
```

Ou via JavaScript :

```javascript
window.location.href = "disablepulltorefresh://";
```

Les deux commandes sont également prises en charge dans une requête [MultiAPICall](multi-api-call.md).

## Bon à savoir

- Le contrôle d'actualisation recharge l'URL actuellement affichée dans la WebView.
- Si vous utilisez l'[API Dynamic UI](dynamic-ui.md) pour changer la couleur de la barre inférieure à l'exécution, les couleurs du pull-to-refresh sont ajustées automatiquement pour correspondre.

---

## Continuer la lecture

- ← Précédent : [API d'indicateur de chargement](loading-sign.md)
- Suivant → : [API de gestion des URL](url-handling.md)
- Langues : [🇺🇸 English](../../ios/pull-to-refresh.md) · [🇩🇪 Deutsch](../../de/ios/pull-to-refresh.md) · **🇫🇷 Français** · [🇪🇸 Español](../../es/ios/pull-to-refresh.md) · [🇨🇳 中文](../../zh/ios/pull-to-refresh.md)

> [!TIP]
> **Trop occupé ? Nous configurons votre app pour vous.** Notre équipe configure, compile & soumet votre app WebViewGold — clé en main, délai rapide, Made in Germany. [Faire configurer mon app →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **Compilez dans votre navigateur :** Pas de Mac, pas d’IDE : le **WebViewGold Cloud Builder** configure, compile & met en ligne votre app. [Découvrir Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
