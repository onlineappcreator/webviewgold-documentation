---
title: "API de décision de suivi utilisateur – Documentation WebViewGold pour iOS"
description: "Respectez l'App Tracking Transparency : lisez la décision de suivi de l'utilisateur et réagissez en conséquence dans votre application WebViewGold iOS."
lang: "fr"
product: "WebViewGold pour iOS"
platform: "iOS"
category: "API et fonctionnalités"
slug: "user-tracking"
canonical_url: "https://www.webviewgold.com/fr/docs/iOS/user-tracking/"
keywords:
  - "API de décision de suivi"
  - "WebViewGold pour iOS"
  - "convertir un site web en app"
  - "documentation d’app WebView"
  - "SDK WebView iOS"
  - "PWA en app"
  - "HTML en app"
  - "pont JavaScript"
last_updated: "2026-10-09"
---

# API de décision de suivi utilisateur – WebViewGold pour iOS

> **Résumé :** Respectez l'App Tracking Transparency : lisez la décision de suivi de l'utilisateur et réagissez en conséquence dans votre application WebViewGold iOS.

[Documentation](../README.md) › [WebViewGold pour iOS](README.md) › API de décision de suivi

**Plateforme :** iOS · **Catégorie :** API et fonctionnalités · **Version en ligne :** [www.webviewgold.com/fr/docs/iOS/user-tracking/](https://www.webviewgold.com/fr/docs/iOS/user-tracking/)

---

Sous iOS, les applications doivent demander l'autorisation de suivre les données utilisateur en s'appuyant sur le framework Apple AppTrackingTransparency. WebViewGold vous permet de connaître le choix effectué par l'utilisateur lors de l'installation de votre application afin d'agir en conséquence dans votre application web. La variable JavaScript **trackingDisabled** peut être définie par WebViewGold à true pour indiquer que le suivi a été bloqué, ou à false dans le cas contraire. Dans votre application web, vous pouvez facilement vérifier l'état JavaScript en récupérant d'abord la variable JavaScript, puis en l'affichant :

```html
<a href="user-disable-tracking://">Définir la variable JavaScript</a>
<a href="#" onClick="alert(trackingDisabled);">Afficher la décision de suivi</a>
```

---

## Continuer la lecture

- ← Précédent : [API de réinitialisation de l'app](reset-app.md)
- Suivant → : [API d'indicateur de chargement](loading-sign.md)
- Langues : [🇺🇸 English](../../ios/user-tracking.md) · [🇩🇪 Deutsch](../../de/ios/user-tracking.md) · **🇫🇷 Français** · [🇪🇸 Español](../../es/ios/user-tracking.md) · [🇨🇳 中文](../../zh/ios/user-tracking.md)

> [!TIP]
> **Trop occupé ? Nous configurons votre app pour vous.** Notre équipe configure, compile & soumet votre app WebViewGold — clé en main, délai rapide, Made in Germany. [Faire configurer mon app →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **Compilez dans votre navigateur :** Pas de Mac, pas d’IDE : le **WebViewGold Cloud Builder** configure, compile & met en ligne votre app. [Découvrir Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
