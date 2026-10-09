---
title: "Icône de l'application – Documentation WebViewGold pour Android"
description: "Ajoutez votre icône d'application personnalisée à votre application Android WebViewGold dans Android Studio — étape par étape."
lang: "fr"
product: "WebViewGold pour Android"
platform: "Android"
category: "Design de l’app"
slug: "app-icon"
canonical_url: "https://www.webviewgold.com/fr/docs/android/app-icon/"
keywords:
  - "Icône de l'application"
  - "WebViewGold pour Android"
  - "convertir un site web en app"
  - "documentation d’app WebView"
  - "SDK WebView Android"
  - "PWA en app"
  - "HTML en app"
  - "pont JavaScript"
last_updated: "2026-10-09"
---

# Icône de l'application – WebViewGold pour Android

> **Résumé :** Ajoutez votre icône d'application personnalisée à votre application Android WebViewGold dans Android Studio — étape par étape.

[Documentation](../README.md) › [WebViewGold pour Android](README.md) › Icône de l'application

**Plateforme :** Android · **Catégorie :** Design de l’app · **Version en ligne :** [www.webviewgold.com/fr/docs/android/app-icon/](https://www.webviewgold.com/fr/docs/android/app-icon/)

---

## Mention facultative concernant l'application pour votre politique de confidentialité / vos conditions générales

Si vous proposez des applications mobiles (basées sur WebViewGold) à vos utilisateurs, vous pouvez éventuellement inclure la mention suivante dans votre politique de confidentialité ou vos conditions générales (cette note est fournie à titre purement informatif et ne constitue pas un avis juridique. Nous déclinons toute responsabilité quant à l'utilisation de ce texte. Veuillez consulter un professionnel du droit pour un accompagnement individuel) :

> ```
> Our mobile apps (iOS/Android) are developed using WebViewGold by jocapps GmbH (Germany). These apps display the content of our website using a WebView framework and enrich it with selected native features to improve usability and performance. Accordingly, the same privacy policy and terms of service that apply to our website also apply to our mobile apps. For more information, please visit
> https://www.webviewgold.com/#convert-website-to-app-privacy, or contact us directly.
> ```

---

## 3) Ajouter une icône d'application personnalisée

![Icône d'application Android](../../assets/android/img/screenshot_Icon.webp)

Voici comment ajouter une icône personnalisée à votre application Android basée sur WebView :

### 1. Localiser les icônes d'application existantes

Pour commencer, repérez les fichiers d'icônes d'application existants :

- Faites un clic droit sur chaque fichier 'ic_launcher.png' de votre projet (tailles de hdpi à xxxhdpi).
- Sélectionnez Reveal in Finder (Mac) ou Reveal in Explorer (Windows).

### 2. Remplacer par votre icône

Remplacez chaque fichier ic_launcher.png par votre nouveau fichier d'icône, en veillant à ce que les nouvelles icônes respectent les exigences suivantes :

- Incluez des icônes pour chaque résolution : hdpi, xhdpi, xxhdpi et xxxhdpi.
- Utilisez une image de haute qualité (de préférence au format PNG).

**Astuce :** Vous pouvez également utiliser le [**Launcher Icon Generator**](https://jgilfelt.github.io/AndroidAssetStudio/icons-launcher.html) (remarque : WebViewGold n'est pas affilié au développeur de cet outil).

Les différents appareils affichent des icônes carrées ou rondes. Vous devez donc inclure :

- 'ic_launcher.png' : Utilisé sur les appareils affichant des icônes carrées.
- 'ic_launcher_round.png' et 'ic_launcher_foreground.png' : Utilisés sur les appareils affichant des icônes rondes.

![Icône Android ronde ou carrée](../../assets/android/img/roundvsboxicon.webp)

Placez les trois fichiers dans les dossiers mipmap correspondant à chaque résolution (mipmap-hdpi, mipmap-xhdpi, mipmap-xxhdpi et mipmap-xxxhdpi).

La vidéo explique en détail la procédure pour changer l'icône de votre nouvelle application, ainsi que quelques recommandations pour la créer.

[![Regarder la vidéo: Icône de l'application](https://img.youtube.com/vi/TDDH_yaZxoI/hqdefault.jpg)](https://www.youtube.com/watch?v=TDDH_yaZxoI)

---

## Continuer la lecture

- ← Précédent : [Configurer WebViewGold](setup.md)
- Suivant → : [Écran de démarrage](splash-screen.md)
- Même fonctionnalité sur les autres plateformes : [iOS – Nom, icône et splash](../ios/app-name-icon-splash.md) · [macOS – Icône de l'application](../macos/app-icon.md)
- Langues : [🇺🇸 English](../../android/app-icon.md) · [🇩🇪 Deutsch](../../de/android/app-icon.md) · **🇫🇷 Français** · [🇪🇸 Español](../../es/android/app-icon.md) · [🇨🇳 中文](../../zh/android/app-icon.md)

> [!TIP]
> **Trop occupé ? Nous configurons votre app pour vous.** Notre équipe configure, compile & soumet votre app WebViewGold — clé en main, délai rapide, Made in Germany. [Faire configurer mon app →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_android_doc_online)
>
> **Compilez dans votre navigateur :** Pas de Mac, pas d’IDE : le **WebViewGold Cloud Builder** configure, compile & met en ligne votre app. [Découvrir Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=android_docs)
