---
title: "API UUID – Documentation WebViewGold pour Android"
description: "Identifiez les installations de l'application grâce à un UUID unique ajouté à votre URL WebView ou récupéré via JavaScript."
lang: "fr"
product: "WebViewGold pour Android"
platform: "Android"
category: "API et fonctionnalités"
slug: "uuid"
canonical_url: "https://www.webviewgold.com/fr/docs/android/uuid/"
keywords:
  - "API UUID"
  - "WebViewGold pour Android"
  - "convertir un site web en app"
  - "documentation d’app WebView"
  - "SDK WebView Android"
  - "PWA en app"
  - "HTML en app"
  - "pont JavaScript"
last_updated: "2026-10-09"
---

# API UUID – WebViewGold pour Android

> **Résumé :** Identifiez les installations de l'application grâce à un UUID unique ajouté à votre URL WebView ou récupéré via JavaScript.

[Documentation](../README.md) › [WebViewGold pour Android](README.md) › API UUID

**Plateforme :** Android · **Catégorie :** API et fonctionnalités · **Version en ligne :** [www.webviewgold.com/fr/docs/android/uuid/](https://www.webviewgold.com/fr/docs/android/uuid/)

---

L'API UUID de WebViewGold vous permet de récupérer un identifiant unique d'appareil non personnel (UUID - « Universally Unique Identifier ») via JavaScript, capable d'identifier de manière unique un appareil Android. Cette fonctionnalité peut être utile pour :

- Stocker des paramètres spécifiques à l'utilisateur sur le serveur
- Maintenir les états de session
- Rappeler les données enregistrées côté client

**Remarque sur la confidentialité :** Veillez à respecter les lois locales et internationales en matière de confidentialité lorsque vous utilisez cette fonctionnalité, car elle implique l'identification de l'appareil.

## Comment récupérer l'UUID

Pour récupérer l'UUID depuis votre application basée sur WebView, utilisez le code suivant :

```html
<a href="get-uuid://">Get UUID</a>
<a href="#" onClick="alert(uuid);">Show UUID</a>
```

- **Get UUID :** Demande l'UUID à WebViewGold.
- **Show UUID :** Affiche l'UUID via une **alert** pour faciliter les tests.

## Méthode alternative : ajouter l'UUID à l'URL de la WebView

Si vous préférez inclure l'UUID dans les paramètres d'URL, activez l'option `UUID_ENHANCE_WEBVIEW_URL` dans **Config.java** en la réglant sur `true`. Cela ajoutera automatiquement `uuid=XYZ` à votre URL de WebView lors de la première requête, ce qui vous permettra d'accéder à l'UUID directement depuis votre contenu web :

- **Exemple :** Si votre URL de WebView est `https://www.example.org`, elle sera requêtée comme `https://www.example.org?uuid=XYZ`.
- **Remarque :** Seule la requête d'URL initiale inclura ce paramètre GET, envisagez donc de l'enregistrer dans une session ou un cookie si vous devez y faire référence plus tard dans l'application.

## Injecter automatiquement l'UUID dans JavaScript

Pour rendre automatiquement l'UUID (et d'autres variables) disponible en JavaScript sur toutes les pages sans modifier les URL, réglez `AUTO_INJECT_VARIABLES` sur `true` dans **Config.java**. Cela vous permet d'accéder à l'UUID et à d'autres valeurs directement depuis n'importe quelle page.

---

## Continuer la lecture

- ← Précédent : [API Presse-papiers](clipboard.md)
- Suivant → : [API Lampe torche](flashlight.md)
- Même fonctionnalité sur les autres plateformes : [iOS – API UUID](../ios/uuid.md) · [macOS – API UUID](../macos/uuid.md)
- Langues : [🇺🇸 English](../../android/uuid.md) · [🇩🇪 Deutsch](../../de/android/uuid.md) · **🇫🇷 Français** · [🇪🇸 Español](../../es/android/uuid.md) · [🇨🇳 中文](../../zh/android/uuid.md)

> [!TIP]
> **Trop occupé ? Nous configurons votre app pour vous.** Notre équipe configure, compile & soumet votre app WebViewGold — clé en main, délai rapide, Made in Germany. [Faire configurer mon app →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_android_doc_online)
>
> **Compilez dans votre navigateur :** Pas de Mac, pas d’IDE : le **WebViewGold Cloud Builder** configure, compile & met en ligne votre app. [Découvrir Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=android_docs)
