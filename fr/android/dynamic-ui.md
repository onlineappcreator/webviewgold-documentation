---
title: "API d'interface dynamique – Documentation WebViewGold pour Android"
description: "Modifiez dynamiquement les éléments d'interface natifs, comme la couleur de la barre d'état, depuis votre application web sous Android."
lang: "fr"
product: "WebViewGold pour Android"
platform: "Android"
category: "API et fonctionnalités"
slug: "dynamic-ui"
canonical_url: "https://www.webviewgold.com/fr/docs/android/dynamic-ui/"
keywords:
  - "API d'interface dynamique"
  - "WebViewGold pour Android"
  - "convertir un site web en app"
  - "documentation d’app WebView"
  - "SDK WebView Android"
  - "PWA en app"
  - "HTML en app"
  - "pont JavaScript"
last_updated: "2026-10-09"
---

# API d'interface dynamique – WebViewGold pour Android

> **Résumé :** Modifiez dynamiquement les éléments d'interface natifs, comme la couleur de la barre d'état, depuis votre application web sous Android.

[Documentation](../README.md) › [WebViewGold pour Android](README.md) › API d'interface dynamique

**Plateforme :** Android · **Catégorie :** API et fonctionnalités · **Version en ligne :** [www.webviewgold.com/fr/docs/android/dynamic-ui/](https://www.webviewgold.com/fr/docs/android/dynamic-ui/)

---

WebViewGold vous permet de personnaliser dynamiquement les éléments d'interface de votre application web. Ces éléments peuvent comprendre la barre d'état, la barre inférieure (iOS), la barre de navigation (Android) et le pull to refresh (iOS). WebViewGold inclut les commandes suivantes pour personnaliser dynamiquement ces éléments :

- **statusbarcolor://**
  - La COMMANDE MAÎTRE pour modifier la couleur de la barre d'état et automatiquement toute autre fonctionnalité d'interface pertinente, telle que la couleur du texte de la barre d'état, la couleur de la barre inférieure (iOS), la couleur de la barre de navigation (Android), etc.
- **statusbartextcolor://**
  - Vous permet de modifier manuellement la couleur du texte de la barre d'état (iOS et Android).
- **bottombarcolor://**
  - Si un élément d'interface de barre inférieure (iOS) ou de barre de navigation (Android) existe, vous permet de modifier manuellement sa couleur.
- **navbartextcolor://**
  - Vous permet de modifier manuellement la couleur du texte de la barre de navigation sur Android. La demande sera ignorée sur iOS (la barre inférieure iOS ne contient pas de texte).
- **hidebars://**
  - Vous permet de masquer l'arrière-plan des barres d'état et de navigation.

## Modifier la couleur de la barre d'état (et automatiquement d'autres éléments d'interface)

Cette fonctionnalité accepte une entrée de couleur au format suivant :

- RGB = {rouge, vert, bleu}

Où les valeurs sont des entiers compris entre 0 (min) et 255 (max).

Utilisez JavaScript avec ce type d'URL pour modifier la couleur de la barre d'état :

```html
<script>
// Example: red
window.location.href = "statusbarcolor://255,0,0";
</script>
```

Lorsque vous modifiez la couleur de la barre d'état, le texte de la barre d'état change automatiquement vers une couleur adaptée (blanc ou noir) selon le degré d'obscurité de la couleur.\
Les fonctionnalités d'interface facultatives telles que le *Pull To Refresh* (iOS), la *barre inférieure* (iOS) et la *barre de navigation* (Android) verront également leurs couleurs ajustées automatiquement.

## Modifier la couleur du texte de la barre d'état

Si vous souhaitez choisir manuellement la couleur du texte de la barre d'état, vous pouvez le faire à l'aide de cette option.

Cette fonctionnalité accepte une entrée textuelle pour les options suivantes :

- « white »
- « black »

Utilisez JavaScript avec ce type d'URL pour modifier la couleur du texte de la barre d'état :

```html
<script>
// Example: white text
window.location.href = "statusbartextcolor://white";
// Example: black text
window.location.href = "statusbartextcolor://black";
</script>
```

## Modifier la couleur de la barre de navigation

Cette fonctionnalité accepte une entrée de couleur au format suivant :

- RGB = {rouge, vert, bleu}

Où les valeurs sont des entiers compris entre 0 (min) et 255 (max).

Utilisez JavaScript avec ce type d'URL pour modifier la couleur de la barre de navigation :

```html
<script>
// Example: red
window.location.href = "bottombarcolor://255,0,0";
</script>
```

## Modifier la couleur du texte de la barre de navigation

Si vous souhaitez choisir manuellement la couleur du texte de la barre de navigation, vous pouvez le faire à l'aide de cette option. Notez que cette demande sera ignorée sur iOS.

Cette fonctionnalité accepte une entrée textuelle pour les options suivantes :

- « white »
- « black »

Utilisez JavaScript avec ce type d'URL pour modifier la couleur du texte de la barre de navigation :

```html
<script>
// Example: white text
window.location.href = "navbartextcolor://white";
// Example: black text
window.location.href = "navbartextcolor://black";
</script>
```

## Masquer les barres d'état et inférieure

La fonctionnalité hidebars peut être **on** ou **off**.

Notez que le texte de la barre d'état, tel que l'heure et le pourcentage de batterie, *ne reste pas* visible pour l'utilisateur.
Cependant, il peut être ramené à la vue par un balayage de l'utilisateur depuis le haut.

Utilisez JavaScript pour modifier l'état de visibilité de la barre d'état et de la barre de navigation :

```html
<script>
// Example: hide the bars from view
window.location.href = "hidebars://on";
// Example: redisplay the bars after being hidden
window.location.href = "hidebars://off";
</script>
```

---

## Détecter le mode sombre (variable JavaScript `isDarkMode`)

Pour adapter vos couleurs d'interface dynamiques au thème système de l'utilisateur, WebViewGold injecte automatiquement la variable JavaScript `isDarkMode` (`true` ou `false`) dans chaque page une fois son chargement terminé. Exemple :

```html
<script>
if (typeof isDarkMode !== "undefined" && isDarkMode) {
    // Mode sombre : p. ex. définir une barre d'état sombre
    window.location.href = "statusbarcolor://0,0,0";
    window.location.href = "statusbartextcolor://white";
} else {
    // Mode clair
    window.location.href = "statusbarcolor://255,255,255";
    window.location.href = "statusbartextcolor://black";
}
</script>
```

**Remarque :** Vous pouvez également utiliser la media query CSS standard `prefers-color-scheme` dans votre web app. La variable injectée `isDarkMode` est pratique lorsque vous souhaitez déclencher les APIs d'interface WebViewGold ci-dessus depuis JavaScript.

---

## Continuer la lecture

- ← Précédent : [API Contacts](contacts.md)
- Suivant → : [API de retour haptique](haptic-feedback.md)
- Même fonctionnalité sur les autres plateformes : [iOS – API d'UI dynamique](../ios/dynamic-ui.md)
- Langues : [🇺🇸 English](../../android/dynamic-ui.md) · [🇩🇪 Deutsch](../../de/android/dynamic-ui.md) · **🇫🇷 Français** · [🇪🇸 Español](../../es/android/dynamic-ui.md) · [🇨🇳 中文](../../zh/android/dynamic-ui.md)

> [!TIP]
> **Trop occupé ? Nous configurons votre app pour vous.** Notre équipe configure, compile & soumet votre app WebViewGold — clé en main, délai rapide, Made in Germany. [Faire configurer mon app →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_android_doc_online)
>
> **Compilez dans votre navigateur :** Pas de Mac, pas d’IDE : le **WebViewGold Cloud Builder** configure, compile & met en ligne votre app. [Découvrir Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=android_docs)
