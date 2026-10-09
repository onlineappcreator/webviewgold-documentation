---
title: "Pied de navigation natif – Documentation WebViewGold pour iOS"
description: "Activez une barre de navigation inférieure native avec des boutons précédent, suivant et personnalisés dans votre application iOS."
lang: "fr"
product: "WebViewGold pour iOS"
platform: "iOS"
category: "Extensions et plugins"
slug: "navigation-footer"
canonical_url: "https://www.webviewgold.com/fr/docs/iOS/navigation-footer/"
keywords:
  - "Pied de navigation natif"
  - "WebViewGold pour iOS"
  - "convertir un site web en app"
  - "documentation d’app WebView"
  - "SDK WebView iOS"
  - "PWA en app"
  - "HTML en app"
  - "pont JavaScript"
last_updated: "2026-10-09"
---

# Pied de navigation natif – WebViewGold pour iOS

> **Résumé :** Activez une barre de navigation inférieure native avec des boutons précédent, suivant et personnalisés dans votre application iOS.

[Documentation](../README.md) › [WebViewGold pour iOS](README.md) › Pied de navigation natif

**Plateforme :** iOS · **Catégorie :** Extensions et plugins · **Version en ligne :** [www.webviewgold.com/fr/docs/iOS/navigation-footer/](https://www.webviewgold.com/fr/docs/iOS/navigation-footer/)

---

Définissez `var showNavFooter = true` dans `Config.swift` pour activer la barre de navigation native en pied de page. Configurez les boutons et les liens dans `FooterBar.json`. Exemple :

```json
{
   "colour":"dark",
   "layout":[
      {
         "redirection_link":"https://webviewgoldtest.github.io/index.html",
         "sf_symbol":"house",
         "name": "Home"
      },
      {
         "redirection_link":"https://webviewgoldtest.github.io/appControls.html",
         "sf_symbol":"wrench.and.screwdriver",
         "name": "Controls"
      },
      {
         "redirection_link":"https://webviewgoldtest.github.io/NFCtesting.html",
         "sf_symbol":"wifi.square",
         "name": "NFC"
      },
      {
         "redirection_link":"https://webviewgoldtest.github.io/IAPtesting.html",
         "sf_symbol":"cart",
         "name": "Purchases"
      },
      {
         "redirection_link":"https://webviewgoldtest.github.io/permissions.html",
         "sf_symbol":"lock.open",
         "name": "Permissions"
      }
   ]
}
```

Chaque `sf_symbol` utilise un [SF Symbol](https://developer.apple.com/sf-symbols/) et ouvre le `redirection_link` dans la WebView principale.

---

## Continuer la lecture

- ← Précédent : [App Clip Extension](app-clip.md)
- Suivant → : [Barre latérale native](sidebar.md)
- Même fonctionnalité sur les autres plateformes : [Android – Navigation Drawer & Footer](../android/navigation-drawer.md)
- Langues : [🇺🇸 English](../../ios/navigation-footer.md) · [🇩🇪 Deutsch](../../de/ios/navigation-footer.md) · **🇫🇷 Français** · [🇪🇸 Español](../../es/ios/navigation-footer.md) · [🇨🇳 中文](../../zh/ios/navigation-footer.md)

> [!TIP]
> **Trop occupé ? Nous configurons votre app pour vous.** Notre équipe configure, compile & soumet votre app WebViewGold — clé en main, délai rapide, Made in Germany. [Faire configurer mon app →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **Compilez dans votre navigateur :** Pas de Mac, pas d’IDE : le **WebViewGold Cloud Builder** configure, compile & met en ligne votre app. [Découvrir Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
