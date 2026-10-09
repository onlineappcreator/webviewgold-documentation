---
title: "Configurer votre application web ou site web – Documentation WebViewGold pour Android"
description: "Préparez votre site web, PWA ou fichiers HTML locaux pour votre application Android : utilisez une URL distante, intégrez des fichiers hors ligne dans l'application ou combinez les deux avec un repli hors ligne."
lang: "fr"
product: "WebViewGold pour Android"
platform: "Android"
category: "Prise en main"
slug: "setup-website"
canonical_url: "https://www.webviewgold.com/fr/docs/android/setup-website/"
keywords:
  - "Configurer l'application web"
  - "WebViewGold pour Android"
  - "convertir un site web en app"
  - "documentation d’app WebView"
  - "SDK WebView Android"
  - "PWA en app"
  - "HTML en app"
  - "pont JavaScript"
last_updated: "2026-10-09"
---

# Configurer votre application web ou site web – WebViewGold pour Android

> **Résumé :** Préparez votre site web, PWA ou fichiers HTML locaux pour votre application Android : utilisez une URL distante, intégrez des fichiers hors ligne dans l'application ou combinez les deux avec un repli hors ligne.

[Documentation](../README.md) › [WebViewGold pour Android](README.md) › Configurer l'application web

**Plateforme :** Android · **Catégorie :** Prise en main · **Version en ligne :** [www.webviewgold.com/fr/docs/android/setup-website/](https://www.webviewgold.com/fr/docs/android/setup-website/)

---

## Option A) Utiliser une URL pour accéder à votre application web (= stocker les fichiers en ligne)

Créez un site web ou une application web optimisée pour mobile et téléversez-la sur votre serveur/hébergement web. WebViewGold pour Android prend en charge le HTML classique, PHP, WordPress, les Progressive Web Apps, les jeux HTML5, Wix, apprat.io, Bubble, jQuery Mobile, ainsi que les constructeurs modernes basés sur l'IA/le no-code tels que Lovable, Base44 et Bolt. Un modèle d'implémentation courant consiste à concevoir l'interface produit en jQuery, Lovable, Base44, Bolt, React, Vue, Angular ou votre pile préférée, puis à utiliser WebViewGold comme coque d'application Android native qui ajoute l'empaquetage Google Play, les notifications push, les API d'appareil, la gestion des URL et d'autres capacités natives.

Pour obtenir les meilleurs résultats lors de la revue Google Play, optimisez le site web afin qu'il se comporte comme une application Android soignée : points de rupture responsive, chargement rapide, états hors ligne/erreur clairs, cibles tactiles accessibles et comportement prévisible du bouton retour. Par défaut, WebViewGold pour Android autorise à la fois le contenu HTTPS et HTTP. Pour un profil de sécurité de niveau production, restreignez le trafic au HTTPS en [désactivant le trafic en clair](https://www.webviewgold.com/support-center/knowledgebase/how-to-prevent-non-https-connections-in-webviewgold-for-android-switching-usescleartexttraffic-from-true-to-false/) et envisagez l'option `BLOCK_SELF_SIGNED_AND_FAULTY_SSL_CERTS`. Envisagez une revue professionnelle d'expérience utilisateur/UX sur [UXreviewer.io](https://www.uxreviewer.io) ou des services similaires pour améliorer la préparation à l'approbation et la fidélisation à long terme.

## Option B) Utiliser un dossier HTML local pour accéder à votre application web (= stocker les fichiers dans l'application)

WebViewGold prend également en charge les applications web basées sur des dossiers HTML locaux : copiez vos fichiers HTML/CSS/JavaScript dans le projet Android Studio et réglez **USE_LOCAL_HTML_FOLDER** sur **true** (voir [étape suivante](setup.md)). Envisagez une revue professionnelle d'expérience utilisateur/UX sur [UXreviewer.io](https://www.uxreviewer.io) ou des services similaires pour obtenir les meilleurs résultats d'approbation Play Store. Une telle revue UX vous aide également à obtenir une meilleure fidélisation client en général pour votre produit grâce à des suggestions d'amélioration.

[![Regarder la vidéo: Configurer votre application web ou site web](https://img.youtube.com/vi/CtyyZrNVcek/hqdefault.jpg)](https://www.youtube.com/watch?v=CtyyZrNVcek)

## Option C) Utiliser un dossier HTML si l'utilisateur est hors ligne, et une URL distante s'il est en ligne (= stocker les fichiers en ligne + stocker des fichiers de sauvegarde/repli dans l'application)

Copiez vos fichiers HTML/CSS/JavaScript dans le projet Android Studio, réglez **USE_LOCAL_HTML_FOLDER** sur **false** (voir [étape suivante](setup.md)) et réglez **FALLBACK_USE_LOCAL_HTML_FOLDER_IF_OFFLINE** sur **true** (voir [étape suivante](setup.md)). Envisagez une revue professionnelle d'expérience utilisateur/UX sur [UXreviewer.io](https://www.uxreviewer.io) ou des services similaires pour obtenir les meilleurs résultats d'approbation Play Store. Une telle revue UX vous aide également à obtenir une meilleure fidélisation client en général pour votre produit grâce à des suggestions d'amélioration.

[![Regarder la vidéo: Configurer votre application web ou site web](https://img.youtube.com/vi/W0NrpCKB7aU/hqdefault.jpg)](https://www.youtube.com/watch?v=W0NrpCKB7aU)

---

## Continuer la lecture

- ← Retour à : [Aperçu](README.md)
- Suivant → : [Configurer WebViewGold](setup.md)
- Même fonctionnalité sur les autres plateformes : [iOS – Configurer l'application web](../ios/setup-website.md) · [macOS – Configuration de votre application web](../macos/setup-website.md)
- Langues : [🇺🇸 English](../../android/setup-website.md) · [🇩🇪 Deutsch](../../de/android/setup-website.md) · **🇫🇷 Français** · [🇪🇸 Español](../../es/android/setup-website.md) · [🇨🇳 中文](../../zh/android/setup-website.md)

> [!TIP]
> **Trop occupé ? Nous configurons votre app pour vous.** Notre équipe configure, compile & soumet votre app WebViewGold — clé en main, délai rapide, Made in Germany. [Faire configurer mon app →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_android_doc_online)
>
> **Compilez dans votre navigateur :** Pas de Mac, pas d’IDE : le **WebViewGold Cloud Builder** configure, compile & met en ligne votre app. [Découvrir Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=android_docs)
