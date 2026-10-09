---
title: "API de dialogue de partage d'app – Documentation WebViewGold pour iOS"
description: "Déclenchez la feuille de partage iOS native depuis votre application web pour permettre aux utilisateurs de partager votre app ou n'importe quelle URL."
lang: "fr"
product: "WebViewGold pour iOS"
platform: "iOS"
category: "API et fonctionnalités"
slug: "app-sharing-dialog"
canonical_url: "https://www.webviewgold.com/fr/docs/iOS/app-sharing-dialog/"
keywords:
  - "API de partage d'app"
  - "WebViewGold pour iOS"
  - "convertir un site web en app"
  - "documentation d’app WebView"
  - "SDK WebView iOS"
  - "PWA en app"
  - "HTML en app"
  - "pont JavaScript"
last_updated: "2026-10-09"
---

# API de dialogue de partage d'app – WebViewGold pour iOS

> **Résumé :** Déclenchez la feuille de partage iOS native depuis votre application web pour permettre aux utilisateurs de partager votre app ou n'importe quelle URL.

[Documentation](../README.md) › [WebViewGold pour iOS](README.md) › API de partage d'app

**Plateforme :** iOS · **Catégorie :** API et fonctionnalités · **Version en ligne :** [www.webviewgold.com/fr/docs/iOS/app-sharing-dialog/](https://www.webviewgold.com/fr/docs/iOS/app-sharing-dialog/)

---

L'API App Sharing Dialog de WebViewGold permet à vos utilisateurs de partager du contenu depuis votre application, comme le lien de téléchargement ou des messages personnalisés, avec leurs amis et leur famille via leurs applications préférées (par exemple WhatsApp, SMS, e-mail). C'est un moyen efficace d'accroître la visibilité de votre application et d'élargir votre base d'utilisateurs.

## Comment utiliser l'App Sharing Dialog dans votre application iOS basée sur WebView

Vous pouvez déclencher une boîte de dialogue de partage native à l'aide du schéma d'URL `shareapp://` avec des paramètres de message et d'URL personnalisables.

Voici des exemples des différentes manières d'implémenter cette fonctionnalité :

```html
<a href="shareapp://message?=Check out this cool thing!&url=https://www.webviewgold.com">Share (message, link)</a>

<a href="shareapp://message?=&url=https://www.webviewgold.com">Share (no message, link)</a>

<a href="shareapp://message?=Check out this cool thing!">Share (message, no link)</a>
```

![Exemple de boîte de dialogue de partage d'application](../../assets/ios/img/sharedialog.webp)\
![Exemple de message de partage d'application](../../assets/ios/img/sharemessage.webp)

---

## Continuer la lecture

- ← Précédent : [API de deep linking](deep-linking.md)
- Suivant → : [API de notation In-App](in-app-rating.md)
- Même fonctionnalité sur les autres plateformes : [Android – API de dialogue de partage](../android/app-sharing-dialog.md)
- Langues : [🇺🇸 English](../../ios/app-sharing-dialog.md) · [🇩🇪 Deutsch](../../de/ios/app-sharing-dialog.md) · **🇫🇷 Français** · [🇪🇸 Español](../../es/ios/app-sharing-dialog.md) · [🇨🇳 中文](../../zh/ios/app-sharing-dialog.md)

> [!TIP]
> **Trop occupé ? Nous configurons votre app pour vous.** Notre équipe configure, compile & soumet votre app WebViewGold — clé en main, délai rapide, Made in Germany. [Faire configurer mon app →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **Compilez dans votre navigateur :** Pas de Mac, pas d’IDE : le **WebViewGold Cloud Builder** configure, compile & met en ligne votre app. [Découvrir Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
