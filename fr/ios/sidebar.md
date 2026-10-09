---
title: "Navigation par barre latérale native – Documentation WebViewGold pour iOS"
description: "Activez un menu latéral coulissant natif avec des liens personnalisés et des icônes SF Symbols — configuré via Sidebar.json."
lang: "fr"
product: "WebViewGold pour iOS"
platform: "iOS"
category: "Extensions et plugins"
slug: "sidebar"
canonical_url: "https://www.webviewgold.com/fr/docs/iOS/sidebar/"
keywords:
  - "Barre latérale native"
  - "WebViewGold pour iOS"
  - "convertir un site web en app"
  - "documentation d’app WebView"
  - "SDK WebView iOS"
  - "PWA en app"
  - "HTML en app"
  - "pont JavaScript"
last_updated: "2026-10-09"
---

# Navigation par barre latérale native – WebViewGold pour iOS

> **Résumé :** Activez un menu latéral coulissant natif avec des liens personnalisés et des icônes SF Symbols — configuré via Sidebar.json.

[Documentation](../README.md) › [WebViewGold pour iOS](README.md) › Barre latérale native

**Plateforme :** iOS · **Catégorie :** Extensions et plugins · **Version en ligne :** [www.webviewgold.com/fr/docs/iOS/sidebar/](https://www.webviewgold.com/fr/docs/iOS/sidebar/)

---

En plus du [pied de navigation natif](navigation-footer.md), WebViewGold intègre une **barre latérale coulissante** native qui vous permet d'offrir une expérience de navigation digne d'une app sans toucher à votre site web. Un bouton de menu flottant ouvre une barre latérale avec vos liens — chaque entrée fait naviguer la WebView principale vers l'URL que vous lui associez.

## Activation

Définissez l'option suivante dans **Config.swift** :

```swift
var enableSidebar = true
```

## Configuration

Ouvrez **Sidebar.json** dans le projet Xcode et définissez le schéma de couleurs ainsi que les entrées du menu :

```json
{
   "colour":"dark",
   "layout":[
      {
         "redirection_link":"https://example.org/home",
         "sf_symbol":"house",
         "name": "Accueil"
      },
      {
         "redirection_link":"https://example.org/shop",
         "sf_symbol":"cart",
         "name": "Boutique"
      }
   ]
}
```

| Clé | Description |
| --- | --- |
| `colour` | Schéma de couleurs de la barre latérale : `dark` ou `light`. |
| `redirection_link` | URL chargée dans la WebView principale lorsque l'entrée est touchée. |
| `sf_symbol` | Nom de l'icône issue de la bibliothèque [SF Symbols](https://developer.apple.com/sf-symbols/) d'Apple (par ex. `house`, `cart`, `wrench.and.screwdriver`). |
| `name` | Libellé de l'entrée de la barre latérale. |

## Comportement

- Un bouton flottant ouvre et ferme la barre latérale par-dessus votre contenu web.
- Toucher une entrée charge l'URL associée dans la WebView principale — votre application web ne quitte donc jamais la coque de l'app.
- La barre latérale peut être combinée avec le [pied de navigation natif](navigation-footer.md) ou utilisée indépendamment.

---

## Continuer la lecture

- ← Précédent : [Pied de navigation natif](navigation-footer.md)
- Suivant → : [Détection de capture d'écran](screen-capture.md)
- Langues : [🇺🇸 English](../../ios/sidebar.md) · [🇩🇪 Deutsch](../../de/ios/sidebar.md) · **🇫🇷 Français** · [🇪🇸 Español](../../es/ios/sidebar.md) · [🇨🇳 中文](../../zh/ios/sidebar.md)

> [!TIP]
> **Trop occupé ? Nous configurons votre app pour vous.** Notre équipe configure, compile & soumet votre app WebViewGold — clé en main, délai rapide, Made in Germany. [Faire configurer mon app →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **Compilez dans votre navigateur :** Pas de Mac, pas d’IDE : le **WebViewGold Cloud Builder** configure, compile & met en ligne votre app. [Découvrir Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
