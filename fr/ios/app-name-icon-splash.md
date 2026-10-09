---
title: "Nom de l'app, icône et écran de démarrage – Documentation WebViewGold pour iOS"
description: "Renommez votre application iOS, ajoutez une icône d'app personnalisée et configurez des écrans de démarrage personnalisés pour votre application WebViewGold."
lang: "fr"
product: "WebViewGold pour iOS"
platform: "iOS"
category: "Design de l’app"
slug: "app-name-icon-splash"
canonical_url: "https://www.webviewgold.com/fr/docs/iOS/app-name-icon-splash/"
keywords:
  - "Nom, icône et splash"
  - "WebViewGold pour iOS"
  - "convertir un site web en app"
  - "documentation d’app WebView"
  - "SDK WebView iOS"
  - "PWA en app"
  - "HTML en app"
  - "pont JavaScript"
last_updated: "2026-10-09"
---

# Nom de l'app, icône et écran de démarrage – WebViewGold pour iOS

> **Résumé :** Renommez votre application iOS, ajoutez une icône d'app personnalisée et configurez des écrans de démarrage personnalisés pour votre application WebViewGold.

[Documentation](../README.md) › [WebViewGold pour iOS](README.md) › Nom, icône et splash

**Plateforme :** iOS · **Catégorie :** Design de l’app · **Version en ligne :** [www.webviewgold.com/fr/docs/iOS/app-name-icon-splash/](https://www.webviewgold.com/fr/docs/iOS/app-name-icon-splash/)

---

## Modifier le nom affiché de l'application

Naviguez comme indiqué dans la capture d'écran via **WebViewGold** → **WebViewGold** → **Build Settings** jusqu'à **Product Name** et modifiez le nom comme illustré ci-dessous :

- ***REMARQUE :*** Si le nom de votre application contient des lettres accentuées (comme « à », par exemple), vous devrez les remplacer par des lettres normales pour le **Product Name**. Le **Product Name** est également utilisé pour nommer les fichiers de votre application, il ne prend donc pas en charge les lettres accentuées (l'application planterait). Ensuite, pour vous assurer que votre application affiche le nom correct aux utilisateurs sur l'écran d'accueil iOS, veuillez également modifier le **Bundle Display Name** (situé dans le fichier **Info.plist**) de « $PRODUCT_NAME » vers le nom de votre application avec les lettres accentuées. Par exemple, si le nom de votre application est « WebViewGold », le **Product Name** doit être « WebViewGolda » et le **Bundle Display Name** doit être « WebViewGold ».

![Modifier le nom iOS de votre application Web-View](../../assets/ios/img/rename_xcode14.webp)

## Ajouter une icône d'application personnalisée

Suivez ces étapes simples pour ajouter une icône personnalisée à votre application iOS basée sur WebView :\
**1. Localiser les paramètres d'icône d'application**\
Naviguez vers **WebViewGold** → **WebViewGold** → **General** → **App Icons and Launch Screen** → **App Icon Source**.\
![Ajoutez votre icône iOS à l'espace de projet](../../assets/ios/img/screen6.webp)\
**2. Remplacez par votre icône**\
Il suffit de remplacer les fichiers image inclus par vos propres fichiers image redimensionnés. Il existe des outils en ligne gratuits pour vous aider à générer ces différentes tailles d'images, comme [**App Icon Generator**](https://www.appicon.co/), par exemple (nous ne sommes pas affiliés à l'entreprise du développeur). Vous pouvez également rechercher n'importe quel outil « iOS App Icon Generator » de votre choix.

## Ajouter un écran de démarrage personnalisé

Suivez ces étapes pour ajouter des graphismes d'écran de démarrage personnalisés à votre application iOS basée sur WebView :

### 1. Activer l'écran de démarrage

Pour activer l'écran de démarrage de votre application :

- Ouvrez le fichier **Config.swift** et recherchez `splashScreenEnabled`.
- Assurez-vous que cette variable est définie sur `true`.

### 2. Remplacer l'image de l'écran de démarrage

Pour utiliser votre propre identité visuelle comme écran de démarrage :

- Remplacez le fichier **splash.gif** existant dans le dossier principal du projet Xcode par votre propre fichier GIF.
- **Important :** assurez-vous que votre fichier image est carré (largeur = hauteur) pour un affichage optimal. Par exemple :
  - 128x128 px
  - 512x512 px
  - 1024x1024 px

### 3. Ajuster la durée d'affichage

Pour contrôler la durée d'affichage de l'écran de démarrage :

- Ouvrez le fichier **Config.swift** et recherchez `splashTimeout`.
- Modifiez le paramètre de délai à la durée souhaitée (en millisecondes).

**Exemple :** définissez sur `2000` pour un affichage de 2 secondes.

Définissez l'option `remainSplashOption` (elle se trouve dans le fichier **Config.swift**) sur `true` si vous souhaitez afficher l'écran de démarrage jusqu'à ce que votre page soit chargée avec succès. Dans le cas contraire, il ne s'affichera que brièvement, et l'indicateur de chargement natif iOS prendra le relais.\
Utilisez l'option `splashscreencolor` (elle se trouve dans le fichier **Config.swift**) pour modifier la couleur d'arrière-plan de l'écran de démarrage. Les options de couleurs sont disponibles [ici](https://developer.apple.com/documentation/uikit/uicolor/standard_colors).

**4. Divulgation facultative concernant l'application pour votre politique de confidentialité / vos conditions générales**

Si vous proposez des applications mobiles (basées sur WebViewGold) à vos utilisateurs, vous pouvez éventuellement inclure la déclaration suivante dans votre politique de confidentialité ou vos conditions générales (cette note est fournie à titre informatif uniquement et ne constitue pas un conseil juridique. Nous n'assumons aucune responsabilité quant à l'utilisation de ce texte. Veuillez consulter un professionnel du droit pour un accompagnement individuel) :

> ```
> Nos applications mobiles (iOS/Android) sont développées à l'aide de WebViewGold par jocapps GmbH (Allemagne). Ces applications affichent le contenu de notre site web via un framework WebView et l'enrichissent de fonctionnalités natives sélectionnées afin d'améliorer l'ergonomie et la performance. Par conséquent, la même politique de confidentialité et les mêmes conditions d'utilisation qui s'appliquent à notre site web s'appliquent également à nos applications mobiles. Pour plus d'informations, veuillez consulter
> https://www.webviewgold.com/#convert-website-to-app-privacy, ou contactez-nous directement.
> ```

---

## Continuer la lecture

- ← Précédent : [Configurer WebViewGold](setup.md)
- Suivant → : [Modifier la Safe Area](safe-area.md)
- Même fonctionnalité sur les autres plateformes : [Android – Icône de l'application](../android/app-icon.md) · [macOS – Icône de l'application](../macos/app-icon.md)
- Langues : [🇺🇸 English](../../ios/app-name-icon-splash.md) · [🇩🇪 Deutsch](../../de/ios/app-name-icon-splash.md) · **🇫🇷 Français** · [🇪🇸 Español](../../es/ios/app-name-icon-splash.md) · [🇨🇳 中文](../../zh/ios/app-name-icon-splash.md)

> [!TIP]
> **Trop occupé ? Nous configurons votre app pour vous.** Notre équipe configure, compile & soumet votre app WebViewGold — clé en main, délai rapide, Made in Germany. [Faire configurer mon app →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **Compilez dans votre navigateur :** Pas de Mac, pas d’IDE : le **WebViewGold Cloud Builder** configure, compile & met en ligne votre app. [Découvrir Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
