---
title: "Configurer votre application web ou site web – Documentation WebViewGold pour iOS"
description: "Préparez votre site web, votre PWA ou vos fichiers HTML locaux pour votre application iOS : utilisez une URL distante, intégrez les fichiers hors ligne dans l'application ou combinez les deux avec une solution de repli hors ligne."
lang: "fr"
product: "WebViewGold pour iOS"
platform: "iOS"
category: "Prise en main"
slug: "setup-website"
canonical_url: "https://www.webviewgold.com/fr/docs/iOS/setup-website/"
keywords:
  - "Configurer l'application web"
  - "WebViewGold pour iOS"
  - "convertir un site web en app"
  - "documentation d’app WebView"
  - "SDK WebView iOS"
  - "PWA en app"
  - "HTML en app"
  - "pont JavaScript"
last_updated: "2026-10-09"
---

# Configurer votre application web ou site web – WebViewGold pour iOS

> **Résumé :** Préparez votre site web, votre PWA ou vos fichiers HTML locaux pour votre application iOS : utilisez une URL distante, intégrez les fichiers hors ligne dans l'application ou combinez les deux avec une solution de repli hors ligne.

[Documentation](../README.md) › [WebViewGold pour iOS](README.md) › Configurer l'application web

**Plateforme :** iOS · **Catégorie :** Prise en main · **Version en ligne :** [www.webviewgold.com/fr/docs/iOS/setup-website/](https://www.webviewgold.com/fr/docs/iOS/setup-website/)

---

## Option A) Utiliser une URL pour accéder à votre application web (= stocker les fichiers en ligne)

Créez un site web ou une application web optimisé(e) pour mobile et téléversez-le sur votre serveur web / espace web. WebViewGold pour iOS est compatible avec le HTML classique, PHP, WordPress, les Progressive Web Apps, les jeux HTML5, Wix, apprat.io, Bubble, jQuery Mobile, ainsi que les outils modernes d'IA / no-code tels que Lovable, Base44 et Bolt. Dans un flux de travail typique, vous construisez l'interface produit avec jQuery, Lovable, Base44, Bolt, React, Vue, Angular ou votre stack préféré(e), puis vous utilisez WebViewGold comme coque d'application iOS native qui ajoute le packaging App Store, les notifications push, les API d'appareil, la gestion des URL et d'autres capacités natives.

Pour obtenir les meilleurs résultats lors de la validation par l'App Store, concevez votre expérience web afin qu'elle paraisse pensée pour l'iPhone et l'iPad : mises en page responsives, grandes zones de tap, premier rendu rapide, états de chargement / vide / erreur clairs, et navigation qui donne l'impression d'être dans une application. Par défaut, WebViewGold pour iOS autorise à la fois le contenu HTTPS et le contenu HTTP. Pour un profil de sécurité plus proche de la production, restreignez le trafic à HTTPS en [modifiant le réglage iOS transport security](https://www.webviewgold.com/support-center/knowledgebase/how-to-prevent-non-https-connections-in-webviewgold-for-ios-removing-nsallowsarbitraryloadsinwebcontent-from-info-plist/) et envisagez l'option `blockfaultyandselfsignedhttpscerts`. Envisagez une revue professionnelle d'expérience utilisateur / UX sur [UXreviewer.io](https://www.uxreviewer.io) ou des services similaires pour améliorer votre préparation à la validation par le store et la rétention utilisateur à long terme.

## Option B) Utiliser un dossier HTML local pour accéder à votre application web (= stocker les fichiers dans l'application)

WebViewGold prend également en charge les applications web basées sur des dossiers HTML locaux : définissez **uselocalhtmlfolder** sur **true** (voir [étape suivante](setup.md)) et copiez vos fichiers HTML/CSS/JavaScript (y compris les sous-répertoires) dans le dossier « local-www » de votre projet Xcode. Pour cela, veillez à :

1. Supprimer les fichiers par défaut du dossier « local-www » en les sélectionnant dans la hiérarchie de fichiers Xcode, puis en faisant un clic droit sur « Delete », puis en cliquant sur « Move to Trash ».
2. Sélectionner tous les fichiers de votre site web local, puis les glisser-déposer dans la hiérarchie de fichiers Xcode sous le dossier « local-www ». Assurez-vous que « Create folder references » est coché et cliquez sur « Finish ».

Envisagez une revue professionnelle d'expérience utilisateur / UX sur [UXreviewer.io](https://www.uxreviewer.io) ou des services similaires pour de meilleurs résultats lors de la validation par l'App Store. Une telle revue UX vous aide également à obtenir globalement une meilleure fidélisation client pour votre produit grâce à des suggestions d'amélioration.

## Option C) Utiliser un dossier HTML si l'utilisateur est hors ligne, et utiliser une URL distante si l'utilisateur est en ligne (= stocker les fichiers en ligne + stocker des fichiers de secours / repli dans l'application)

Copiez vos fichiers HTML/CSS/JavaScript (y compris les sous-répertoires) dans le dossier « local-www » de votre projet Xcode. Pour cela, veillez à :

1. Supprimer les fichiers par défaut du dossier « local-www » en les sélectionnant dans la hiérarchie de fichiers Xcode, puis en faisant un clic droit sur « Delete », puis en cliquant sur « Move to Trash ».
2. Sélectionner tous les fichiers de votre site web local, puis les glisser-déposer dans la hiérarchie de fichiers Xcode sous le dossier « local-www ». Assurez-vous que « Create folder references » est coché et cliquez sur « Finish ».

Définissez **uselocalhtmlfolder** sur **false** (voir [étape suivante](setup.md)) et définissez **offlinelocalhtmlswitch** sur **true** (voir [étape suivante](setup.md)). Envisagez une revue professionnelle d'expérience utilisateur / UX sur [UXreviewer.io](https://www.uxreviewer.io) ou des services similaires pour de meilleurs résultats lors de la validation par l'App Store. Une telle revue UX vous aide également à obtenir globalement une meilleure fidélisation client pour votre produit grâce à des suggestions d'amélioration.

---

## Continuer la lecture

- ← Retour à : [Aperçu](README.md)
- Suivant → : [Configurer WebViewGold](setup.md)
- Même fonctionnalité sur les autres plateformes : [Android – Configurer l'application web](../android/setup-website.md) · [macOS – Configuration de votre application web](../macos/setup-website.md)
- Langues : [🇺🇸 English](../../ios/setup-website.md) · [🇩🇪 Deutsch](../../de/ios/setup-website.md) · **🇫🇷 Français** · [🇪🇸 Español](../../es/ios/setup-website.md) · [🇨🇳 中文](../../zh/ios/setup-website.md)

> [!TIP]
> **Trop occupé ? Nous configurons votre app pour vous.** Notre équipe configure, compile & soumet votre app WebViewGold — clé en main, délai rapide, Made in Germany. [Faire configurer mon app →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **Compilez dans votre navigateur :** Pas de Mac, pas d’IDE : le **WebViewGold Cloud Builder** configure, compile & met en ligne votre app. [Découvrir Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
