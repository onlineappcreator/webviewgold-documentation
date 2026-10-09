---
title: "API de dialogue de partage de l'application – Documentation WebViewGold pour Android"
description: "Déclenchez le dialogue de partage natif d'Android depuis votre application web pour permettre aux utilisateurs de partager votre application ou n'importe quelle URL."
lang: "fr"
product: "WebViewGold pour Android"
platform: "Android"
category: "API et fonctionnalités"
slug: "app-sharing-dialog"
canonical_url: "https://www.webviewgold.com/fr/docs/android/app-sharing-dialog/"
keywords:
  - "API de dialogue de partage"
  - "WebViewGold pour Android"
  - "convertir un site web en app"
  - "documentation d’app WebView"
  - "SDK WebView Android"
  - "PWA en app"
  - "HTML en app"
  - "pont JavaScript"
last_updated: "2026-10-09"
---

# API de dialogue de partage de l'application – WebViewGold pour Android

> **Résumé :** Déclenchez le dialogue de partage natif d'Android depuis votre application web pour permettre aux utilisateurs de partager votre application ou n'importe quelle URL.

[Documentation](../README.md) › [WebViewGold pour Android](README.md) › API de dialogue de partage

**Plateforme :** Android · **Catégorie :** API et fonctionnalités · **Version en ligne :** [www.webviewgold.com/fr/docs/android/app-sharing-dialog/](https://www.webviewgold.com/fr/docs/android/app-sharing-dialog/)

---

L'API App Sharing Dialog de WebViewGold permet à vos utilisateurs de partager du contenu de votre application, comme le lien de téléchargement ou des messages personnalisés, avec leurs amis et leur famille via leurs applications préférées (par exemple WhatsApp, SMS, e-mail). C'est un moyen efficace d'accroître la visibilité de votre application et d'élargir votre base d'utilisateurs.

## Comment utiliser l'App Sharing Dialog dans votre application Android basée sur WebView

Vous pouvez déclencher une boîte de dialogue de partage native en utilisant le schéma d'URL `shareapp://` avec des paramètres de message et d'URL personnalisables.

Voici des exemples des différentes façons d'implémenter cette fonctionnalité :

```html
<a href="shareapp://message?=Check out this cool thing!&url=https://www.webviewgold.com">Share (message, link)</a>

<a href="shareapp://message?=&url=https://www.webviewgold.com">Share (no message, link)</a>

<a href="shareapp://message?=Check out this cool thing!">Share (message, no link)</a>
```

![Exemple d'App Sharing Dialog](../../assets/android/img/appshare.webp)

---

## Continuer la lecture

- ← Précédent : [API ShareIntent](share-intent.md)
- Suivant → : [API de notation In-App](in-app-rating.md)
- Même fonctionnalité sur les autres plateformes : [iOS – API de partage d'app](../ios/app-sharing-dialog.md)
- Langues : [🇺🇸 English](../../android/app-sharing-dialog.md) · [🇩🇪 Deutsch](../../de/android/app-sharing-dialog.md) · **🇫🇷 Français** · [🇪🇸 Español](../../es/android/app-sharing-dialog.md) · [🇨🇳 中文](../../zh/android/app-sharing-dialog.md)

> [!TIP]
> **Trop occupé ? Nous configurons votre app pour vous.** Notre équipe configure, compile & soumet votre app WebViewGold — clé en main, délai rapide, Made in Germany. [Faire configurer mon app →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_android_doc_online)
>
> **Compilez dans votre navigateur :** Pas de Mac, pas d’IDE : le **WebViewGold Cloud Builder** configure, compile & met en ligne votre app. [Découvrir Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=android_docs)
