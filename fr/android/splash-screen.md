---
title: "Écran de démarrage – Documentation WebViewGold pour Android"
description: "Personnalisez l'écran de démarrage de votre application Android WebView avec vos propres graphismes."
lang: "fr"
product: "WebViewGold pour Android"
platform: "Android"
category: "Design de l’app"
slug: "splash-screen"
canonical_url: "https://www.webviewgold.com/fr/docs/android/splash-screen/"
keywords:
  - "Écran de démarrage"
  - "WebViewGold pour Android"
  - "convertir un site web en app"
  - "documentation d’app WebView"
  - "SDK WebView Android"
  - "PWA en app"
  - "HTML en app"
  - "pont JavaScript"
last_updated: "2026-10-09"
---

# Écran de démarrage – WebViewGold pour Android

> **Résumé :** Personnalisez l'écran de démarrage de votre application Android WebView avec vos propres graphismes.

[Documentation](../README.md) › [WebViewGold pour Android](README.md) › Écran de démarrage

**Plateforme :** Android · **Catégorie :** Design de l’app · **Version en ligne :** [www.webviewgold.com/fr/docs/android/splash-screen/](https://www.webviewgold.com/fr/docs/android/splash-screen/)

---

Personnalisez le comportement de l'écran de démarrage en configurant les variables suivantes dans `Config.java` :

| Option | Type | Description |
| --- | --- | --- |
| SPLASH_SCREEN_ACTIVATED | **true** ou **false** | Réglez sur *true* pour activer l'écran de démarrage |
| SPLASH_TIMEOUT | nombre (millisecondes) | Délai avant l'affichage de l'indicateur de chargement si l'URL d'accueil est toujours en cours de chargement |
| REMAIN_SPLASH_OPTION | **true** ou **false** | Lorsque *true*, garde l'écran de démarrage visible jusqu'à ce que l'URL d'accueil soit entièrement chargée (a priorité sur `SPLASH_TIMEOUT`) |
| SPLASH_MIN_TIME | nombre (millisecondes) | Durée d'affichage minimale lorsque `REMAIN_SPLASH_OPTION` est *true* ; ignorée si le temps de chargement réel dépasse cette valeur |
| SPLASH_FADE_OUT | nombre (millisecondes) | Durée de l'animation de fondu en sortie après tous les délais ; réglez sur *0* pour désactiver l'effet de fondu |
| SCALE_SPLASH_IMAGE | pourcentage [0–100] | Met à l'échelle l'image de démarrage par rapport à la plus petite dimension de l'appareil ; *0* masque l'image |

## Remplacer l'image de l'écran de démarrage

- Remplacez `splash.gif` dans vos assets par votre propre GIF carré (par exemple 128×128, 512×512 ou 1024×1024 px)
- Assurez-vous que les dimensions de l'image sont égales (largeur = hauteur) pour un affichage optimal
- Définissez la couleur d'arrière-plan dans `colors.xml`

Les étapes pour ajouter un écran de démarrage personnalisé à votre application Android sont présentées dans la vidéo ci-dessous :

[![Regarder la vidéo: Écran de démarrage](https://img.youtube.com/vi/x684JHvW8lI/hqdefault.jpg)](https://www.youtube.com/watch?v=x684JHvW8lI)

---

## Continuer la lecture

- ← Précédent : [Icône de l'application](app-icon.md)
- Suivant → : [Navigation Drawer & Footer](navigation-drawer.md)
- Même fonctionnalité sur les autres plateformes : [iOS – Nom, icône et splash](../ios/app-name-icon-splash.md) · [macOS – Écran de démarrage](../macos/splash-screen.md)
- Langues : [🇺🇸 English](../../android/splash-screen.md) · [🇩🇪 Deutsch](../../de/android/splash-screen.md) · **🇫🇷 Français** · [🇪🇸 Español](../../es/android/splash-screen.md) · [🇨🇳 中文](../../zh/android/splash-screen.md)

> [!TIP]
> **Trop occupé ? Nous configurons votre app pour vous.** Notre équipe configure, compile & soumet votre app WebViewGold — clé en main, délai rapide, Made in Germany. [Faire configurer mon app →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_android_doc_online)
>
> **Compilez dans votre navigateur :** Pas de Mac, pas d’IDE : le **WebViewGold Cloud Builder** configure, compile & met en ligne votre app. [Découvrir Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=android_docs)
