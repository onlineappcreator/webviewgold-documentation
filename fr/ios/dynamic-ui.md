---
title: "API d'UI dynamique – Documentation WebViewGold pour iOS"
description: "Modifiez dynamiquement des éléments d'UI natifs comme les couleurs de la barre d'état ou de la barre inférieure depuis votre application web."
lang: "fr"
product: "WebViewGold pour iOS"
platform: "iOS"
category: "API et fonctionnalités"
slug: "dynamic-ui"
canonical_url: "https://www.webviewgold.com/fr/docs/iOS/dynamic-ui/"
keywords:
  - "API d'UI dynamique"
  - "WebViewGold pour iOS"
  - "convertir un site web en app"
  - "documentation d’app WebView"
  - "SDK WebView iOS"
  - "PWA en app"
  - "HTML en app"
  - "pont JavaScript"
last_updated: "2026-10-09"
---

# API d'UI dynamique – WebViewGold pour iOS

> **Résumé :** Modifiez dynamiquement des éléments d'UI natifs comme les couleurs de la barre d'état ou de la barre inférieure depuis votre application web.

[Documentation](../README.md) › [WebViewGold pour iOS](README.md) › API d'UI dynamique

**Plateforme :** iOS · **Catégorie :** API et fonctionnalités · **Version en ligne :** [www.webviewgold.com/fr/docs/iOS/dynamic-ui/](https://www.webviewgold.com/fr/docs/iOS/dynamic-ui/)

---

WebViewGold vous permet de personnaliser dynamiquement les éléments d'interface utilisateur de votre application web. Ces éléments peuvent inclure la barre d'état, la barre inférieure (iOS), la barre de navigation (Android) et le geste « tirer pour actualiser » (iOS). WebViewGold inclut les commandes suivantes pour personnaliser dynamiquement ces éléments :

- **statusbarcolor://**
  - La COMMANDE MAÎTRESSE pour changer automatiquement la couleur de la barre d'état et de toutes les autres fonctionnalités d'interface concernées, telles que la couleur du texte de la barre d'état, la couleur de la barre inférieure (iOS), la couleur de la barre de navigation (Android), etc.
- **statusbartextcolor://**
  - Vous permet de modifier manuellement la couleur du texte de la barre d'état (iOS et Android).
- **bottombarcolor://**
  - Si un élément d'interface « barre inférieure » (iOS) ou « barre de navigation » (Android) existe, vous permet de modifier manuellement sa couleur.
- **hidebars://**
  - Vous permet de masquer l'arrière-plan de la barre d'état, dont le texte reste affiché sur un fond transparent.

## Changer la couleur de la barre d'état (et automatiquement des autres éléments d'interface)

Cette fonctionnalité prend en charge une entrée de couleur au format suivant :

- RGB = {rouge, vert, bleu}

Où les valeurs sont des entiers compris entre 0 (min) et 255 (max).

Utilisez JavaScript avec ce type d'URL pour changer la couleur de la barre d'état :

```html
<script>
// Exemple : rouge
window.location.href = "statusbarcolor://255,0,0";
</script>
```

Lorsque vous changez la couleur de la barre d'état, le texte de la barre d'état passe automatiquement à une couleur appropriée (blanc ou noir) en fonction du degré d'obscurité de la couleur.\
Les fonctionnalités d'interface optionnelles telles que *Pull To Refresh* (iOS), la *barre inférieure* (iOS) et la *barre de navigation* (Android) verront également leurs couleurs ajustées automatiquement.

## Changer la couleur du texte de la barre d'état

Si vous souhaitez choisir manuellement la couleur du texte de la barre d'état, vous pouvez le faire à l'aide de cette option.

Cette fonctionnalité prend en charge une entrée textuelle pour les options suivantes :

- « white »
- « black »

Utilisez JavaScript avec ce type d'URL pour changer la couleur du texte de la barre d'état :

```html
<script>
// Exemple : texte blanc
window.location.href = "statusbartextcolor://white";
// Exemple : texte noir
window.location.href = "statusbartextcolor://black";
</script>
```

## Changer la couleur de la barre inférieure

Cette fonctionnalité prend en charge une entrée de couleur au format suivant :

- RGB = {rouge, vert, bleu}

Où les valeurs sont des entiers compris entre 0 (min) et 255 (max).

Utilisez JavaScript avec ce type d'URL pour changer la couleur de la barre d'état :

```html
<script>
// Exemple : rouge
window.location.href = "bottombarcolor://255,0,0";
</script>
```

## Masquer la barre d'état

La fonctionnalité hidebars peut être **activée** ou **désactivée**.

Notez que le texte de la barre d'état, comme l'heure et le pourcentage de batterie, restent visibles pour l'utilisateur,
mais l'arrière-plan qui entoure le texte devient transparent et la WebView s'étend pour occuper l'espace libéré.

Utilisez JavaScript pour changer l'état de visibilité de la barre :

```html
<script>
// Exemple : masquer les barres
window.location.href = "hidebars://on";
// Exemple : réafficher les barres après avoir été masquées
window.location.href = "hidebars://off";
</script>
```

---

## Continuer la lecture

- ← Précédent : [API de vérification de version](app-version-check.md)
- Suivant → : [API d'icône d'app dynamique](dynamic-app-icon.md)
- Même fonctionnalité sur les autres plateformes : [Android – API d'interface dynamique](../android/dynamic-ui.md)
- Langues : [🇺🇸 English](../../ios/dynamic-ui.md) · [🇩🇪 Deutsch](../../de/ios/dynamic-ui.md) · **🇫🇷 Français** · [🇪🇸 Español](../../es/ios/dynamic-ui.md) · [🇨🇳 中文](../../zh/ios/dynamic-ui.md)

> [!TIP]
> **Trop occupé ? Nous configurons votre app pour vous.** Notre équipe configure, compile & soumet votre app WebViewGold — clé en main, délai rapide, Made in Germany. [Faire configurer mon app →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **Compilez dans votre navigateur :** Pas de Mac, pas d’IDE : le **WebViewGold Cloud Builder** configure, compile & met en ligne votre app. [Découvrir Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
