---
title: "Configuration de WebViewGold pour les applications de bureau macOS – WebViewGold pour macOS Documentation"
description: "Installez Xcode, ouvrez le projet WebViewGold pour macOS, saisissez votre URL dans index.html et configurez config.json — ou intégrez votre propre contenu HTML local."
lang: "fr"
product: "WebViewGold pour macOS"
platform: "macOS"
category: "Prise en main"
slug: "setup"
canonical_url: "https://www.webviewgold.com/fr/docs/mac/#setup"
keywords:
  - "Configuration de WebViewGold"
  - "WebViewGold pour macOS"
  - "convertir un site web en app"
  - "documentation d’app WebView"
  - "SDK WebView macOS"
  - "PWA en app"
  - "HTML en app"
  - "pont JavaScript"
last_updated: "2026-10-09"
---

# Configuration de WebViewGold pour les applications de bureau macOS – WebViewGold pour macOS

> **Résumé :** Installez Xcode, ouvrez le projet WebViewGold pour macOS, saisissez votre URL dans index.html et configurez config.json — ou intégrez votre propre contenu HTML local.

[Documentation](../README.md) › [WebViewGold pour macOS](README.md) › Configuration de WebViewGold

**Plateforme :** macOS · **Catégorie :** Prise en main · **Version en ligne :** [www.webviewgold.com/fr/docs/mac/#setup](https://www.webviewgold.com/fr/docs/mac/#setup)

---

Xcode est requis pour configurer des applications à l'aide de WebViewGold pour macOS. Xcode est un environnement de développement intégré (IDE) puissant utilisé pour créer des applications pour les appareils Apple tels que les iPhones, iPads et Macs. Il est important de noter que Xcode est un programme volumineux qui peut occuper un espace de stockage important sur votre Mac. En outre, Xcode n'est disponible que pour les Mac et n'est pas compatible avec Windows ou Linux. Voici un guide étape par étape pour télécharger et installer Xcode sur votre Mac :

- Cliquez ici : [**Télécharger Xcode dans le Mac App Store**](https://apps.apple.com/us/app/xcode/id497799835)
- Cliquez sur le bouton « Obtenir » ou « Télécharger » pour lancer le téléchargement.
- Une fois le téléchargement terminé, l'installateur Xcode se lance automatiquement.
- Suivez les instructions de l'installateur pour terminer le processus d'installation.
- Une fois l'installation terminée, ouvrez Xcode depuis le dossier Applications ou la recherche Spotlight.
- Lors de la première ouverture de Xcode, vous serez peut-être invité à installer des composants supplémentaires ou à accepter les conditions d'utilisation. Suivez les instructions pour terminer la configuration.

À l'étape suivante, **[téléchargez WebViewGold pour macOS](https://www.webviewgold.com/download/mac/)** afin de créer des applications de bureau macOS. Ouvrez ensuite le **fichier de projet Xcode** :\
![Fichier principal du projet Xcode](../../assets/macos/img/xcodefile.jpg)

Choisissez le **dossier public** et configurez le fichier **config.json** :\
![Fichier de configuration de WebViewGold pour macOS](../../assets/macos/img/config1.png)

Ouvrez le fichier **index.html** pour modifier l'URL :\
![Insérez l'URL de votre application web dans le fichier index.html](../../assets/macos/img/config2.png)

Si vous souhaitez utiliser du **contenu HTML local** (au lieu d'une URL distante), remplacez simplement le fichier index.html par votre propre contenu.

---

## Continuer la lecture

- ← Précédent : [Configuration de votre application web](setup-website.md)
- Suivant → : [Icône de l'application](app-icon.md)
- Même fonctionnalité sur les autres plateformes : [iOS – Configurer WebViewGold](../ios/setup.md) · [Android – Configurer WebViewGold](../android/setup.md)
- Langues : [🇺🇸 English](../../macos/setup.md) · [🇩🇪 Deutsch](../../de/macos/setup.md) · **🇫🇷 Français** · [🇪🇸 Español](../../es/macos/setup.md) · [🇨🇳 中文](../../zh/macos/setup.md)

