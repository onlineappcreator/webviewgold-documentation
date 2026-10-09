---
title: "API de reconnexion – Documentation WebViewGold pour iOS"
description: "Ajoutez un bouton « Réessayer » à votre page de secours hors ligne qui recharge la dernière URL en ligne de votre application iOS."
lang: "fr"
product: "WebViewGold pour iOS"
platform: "iOS"
category: "API et fonctionnalités"
slug: "reconnect"
canonical_url: "https://www.webviewgold.com/fr/docs/iOS/reconnect/"
keywords:
  - "API de reconnexion"
  - "WebViewGold pour iOS"
  - "convertir un site web en app"
  - "documentation d’app WebView"
  - "SDK WebView iOS"
  - "PWA en app"
  - "HTML en app"
  - "pont JavaScript"
last_updated: "2026-10-09"
---

# API de reconnexion – WebViewGold pour iOS

> **Résumé :** Ajoutez un bouton « Réessayer » à votre page de secours hors ligne qui recharge la dernière URL en ligne de votre application iOS.

[Documentation](../README.md) › [WebViewGold pour iOS](README.md) › API de reconnexion

**Plateforme :** iOS · **Catégorie :** API et fonctionnalités · **Version en ligne :** [www.webviewgold.com/fr/docs/iOS/reconnect/](https://www.webviewgold.com/fr/docs/iOS/reconnect/)

---

L'**API de reconnexion** recharge la dernière URL en ligne sur laquelle se trouvait l'utilisateur avant que votre application ne bascule vers la page HTML hors ligne. Elle est conçue comme bouton « Réessayer » sur votre propre écran de secours hors ligne.

## Utilisation

Ajoutez le déclencheur à votre page hors ligne (généralement `local-html/index.html`) :

```html
<button onclick="window.location.href='reconnect://'">Essayer de se reconnecter</button>
```

## Fonctionnement

L'application mémorise la dernière URL chargée avec succès. Lorsque l'utilisateur touche `reconnect://`, la WebView revient à cette URL. Si la connexion est toujours interrompue, votre page de secours s'affiche à nouveau.

## Configuration associée

- `offlinelocalhtmlswitch` dans **Config.swift** doit être défini sur `true`, et vous avez besoin d'une page de secours `local-html/index.html` pour que cette fonctionnalité ait un sens. Consultez [Configurer votre application web](setup-website.md) pour les détails du mode de secours hors ligne.

---

## Continuer la lecture

- ← Précédent : [Social Login Helper](social-login.md)
- Suivant → : [API CSS et JS personnalisés](custom-css-js.md)
- Même fonctionnalité sur les autres plateformes : [Android – Reconnect API](../android/reconnect.md)
- Langues : [🇺🇸 English](../../ios/reconnect.md) · [🇩🇪 Deutsch](../../de/ios/reconnect.md) · **🇫🇷 Français** · [🇪🇸 Español](../../es/ios/reconnect.md) · [🇨🇳 中文](../../zh/ios/reconnect.md)

> [!TIP]
> **Trop occupé ? Nous configurons votre app pour vous.** Notre équipe configure, compile & soumet votre app WebViewGold — clé en main, délai rapide, Made in Germany. [Faire configurer mon app →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **Compilez dans votre navigateur :** Pas de Mac, pas d’IDE : le **WebViewGold Cloud Builder** configure, compile & met en ligne votre app. [Découvrir Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
