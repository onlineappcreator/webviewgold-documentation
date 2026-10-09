---
title: "API Presse-papiers – Documentation WebViewGold pour Android"
description: "Copiez du texte dans le presse-papiers Android et lisez son contenu depuis votre application web via JavaScript."
lang: "fr"
product: "WebViewGold pour Android"
platform: "Android"
category: "API et fonctionnalités"
slug: "clipboard"
canonical_url: "https://www.webviewgold.com/fr/docs/android/clipboard/"
keywords:
  - "API Presse-papiers"
  - "WebViewGold pour Android"
  - "convertir un site web en app"
  - "documentation d’app WebView"
  - "SDK WebView Android"
  - "PWA en app"
  - "HTML en app"
  - "pont JavaScript"
last_updated: "2026-10-09"
---

# API Presse-papiers – WebViewGold pour Android

> **Résumé :** Copiez du texte dans le presse-papiers Android et lisez son contenu depuis votre application web via JavaScript.

[Documentation](../README.md) › [WebViewGold pour Android](README.md) › API Presse-papiers

**Plateforme :** Android · **Catégorie :** API et fonctionnalités · **Version en ligne :** [www.webviewgold.com/fr/docs/android/clipboard/](https://www.webviewgold.com/fr/docs/android/clipboard/)

---

L'API Clipboard de WebViewGold offre un moyen simple et sécurisé d'accéder au contenu du presse-papiers de l'appareil depuis votre application basée sur WebView. Elle constitue une alternative à l'accès au presse-papiers natif de la WebView et offre une plus grande fiabilité selon les plateformes et les mises à jour.

## Cas d'usage

- Préremplir des champs de formulaire avec des données copiées
- Améliorer les parcours utilisateurs dans les applications d'authentification, de prise de notes ou de partage
- Créer des fonctions de collage rapide ou des outils d'historique du presse-papiers

## Comment récupérer le contenu du presse-papiers

Pour accéder aux données du presse-papiers, utilisez l'appel suivant :

```html
<a href="getclipboard://">Get Clipboard Data</a>
<a href="#" onClick="alert(clipboarddata);">Show Clipboard Data</a>
```

- **Récupérer les données du presse-papiers :** Déclenche la fonctionnalité native de lecture du presse-papiers.
- **Afficher les données du presse-papiers :** Affiche le résultat stocké dans la variable JavaScript `clipboarddata`.

**Note technique :** Une fois `getclipboard://` déclenché, WebViewGold injecte automatiquement le contenu du presse-papiers dans la variable JavaScript `clipboarddata` de la page, la rendant accessible pour toute action ultérieure.

---

## Continuer la lecture

- ← Précédent : [API d'indicateur de chargement](loading-sign.md)
- Suivant → : [API UUID](uuid.md)
- Même fonctionnalité sur les autres plateformes : [iOS – API Presse-papiers](../ios/clipboard.md)
- Langues : [🇺🇸 English](../../android/clipboard.md) · [🇩🇪 Deutsch](../../de/android/clipboard.md) · **🇫🇷 Français** · [🇪🇸 Español](../../es/android/clipboard.md) · [🇨🇳 中文](../../zh/android/clipboard.md)

> [!TIP]
> **Trop occupé ? Nous configurons votre app pour vous.** Notre équipe configure, compile & soumet votre app WebViewGold — clé en main, délai rapide, Made in Germany. [Faire configurer mon app →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_android_doc_online)
>
> **Compilez dans votre navigateur :** Pas de Mac, pas d’IDE : le **WebViewGold Cloud Builder** configure, compile & met en ligne votre app. [Découvrir Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=android_docs)
