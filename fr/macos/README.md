---
title: "Documentation WebViewGold pour macOS – Convertir un site web en app Mac"
description: "Documentation officielle WebViewGold pour macOS : convertissez votre site web, PWA, tableau de bord SaaS ou projet HTML en une app de bureau Mac native, avec configuration Xcode, options de configuration, API JavaScript, conseils de publication et notes d’implémentation façon SDK."
lang: "fr"
product: "WebViewGold pour macOS"
platform: "macOS"
canonical_url: "https://www.webviewgold.com/fr/docs/mac/"
keywords:
  - "WebViewGold pour macOS"
  - "convertir un site web en app"
  - "documentation d’app WebView"
  - "SDK WebView macOS"
  - "PWA en app"
  - "HTML en app"
  - "pont JavaScript"
last_updated: "2026-10-09"
---

# Documentation WebViewGold pour macOS

![WebViewGold pour macOS](../../assets/macos/img/header.png)

> Documentation officielle WebViewGold pour macOS : convertissez votre site web, PWA, tableau de bord SaaS ou projet HTML en une app de bureau Mac native, avec configuration Xcode, options de configuration, API JavaScript, conseils de publication et notes d’implémentation façon SDK.

[Documentation](../README.md) › WebViewGold pour macOS

Convertissez votre site web, PWA, tableau de bord SaaS, boutique e-commerce ou app web générée par IA en une app macOS native en quelques minutes. Utilisez WebViewGold comme un SDK d’application léger : configurez votre URL, activez des API natives, intégrez des commandes du pont JavaScript et publiez une app prête pour le store sans reconstruire votre produit web de zéro.

WebViewGold fonctionne avec les sites HTML/PHP classiques, WordPress, les projets jQuery Mobile et les apps web modernes créées avec Lovable, Base44, Bolt, Bubble, React, Vue, Angular ou des outils similaires. La documentation ci-dessous explique le flux de configuration, les API de fonctionnalités natives, les considérations de sécurité et les étapes de publication dans un format technique axé sur l’implémentation.

**[Démarrer le guide →](setup-website.md)** · [Télécharger WebViewGold](https://www.webviewgold.com/download/mac/)

## Démarrage rapide

1. **[Configurez votre app web](setup-website.md)** — Utilisez une URL distante, empaquetez des fichiers HTML locaux, ou combinez les deux avec une solution de repli hors ligne.
2. **[Configurez WebViewGold](setup.md)** — Insérez votre URL et affinez chaque option dans un simple fichier de config — sans coder.

## Tous les sujets, API & fonctionnalités

Tout ce que WebViewGold pour macOS peut faire — chaque sujet sur sa propre page :

### Prise en main

- **[Configuration de votre application web](setup-website.md)** — Préparez votre site web, PWA ou app web pour WebViewGold pour macOS : technologies prises en charge (HTML, PHP, WordPress, PWA, Lovable, Base44, Bolt…) et conseils pour une expérience de bureau native.
- **[Configuration de WebViewGold](setup.md)** — Installez Xcode, ouvrez le projet WebViewGold pour macOS, saisissez votre URL dans index.html et configurez config.json — ou intégrez votre propre contenu HTML local.

### Design de l’app

- **[Icône de l'application](app-icon.md)** — Remplacez l'icône de votre app de bureau WebViewGold pour macOS par vos propres fichiers d'image redimensionnés.
- **[Nom de l'application](app-name.md)** — Modifiez le nom de votre app de bureau WebViewGold pour macOS dans Xcode.
- **[Texte de l'écran hors ligne](offline-screen.md)** — Personnalisez le texte de l'écran hors ligne de votre app WebView Mac en modifiant OfflineOverlay.xib dans Interface Builder.
- **[Boîte de dialogue de premier lancement](first-run-dialog.md)** — Modifiez le texte de la boîte de dialogue de premier lancement de votre app WebView Mac dans FirstRunWindow.xib (Interface Builder).
- **[Écran de démarrage](splash-screen.md)** — Modifiez le texte de l'écran de démarrage dans SplashScreen.xib et sa durée maximale dans Preferences.m de WebViewGold pour macOS.

### API et fonctionnalités

- **[API In-App Purchases](in-app-purchases.md)** — Vendez des achats intégrés et abonnements du Mac App Store depuis votre app web : ajoutez l'ID produit dans Constants.h et déclenchez l'achat avec un lien inapppurchase://.
- **[API UUID](uuid.md)** — Transmettez un identifiant d'appareil unique et non personnel (UUID) à JavaScript via get-uuid:// pour reconnaître les appareils et restaurer les réglages.
- **[API Deeplinking](deep-linking.md)** — Lancez votre app WebViewGold pour macOS via un schéma d'URL personnalisé et ouvrez directement une page précise — le deeplinking expliqué étape par étape.

### Plus

- **[Crédits & licences](credits.md)** — Informations de licence, marques déposées et crédits open source (MacGap, licence MIT) de WebViewGold pour macOS.
- **[Évaluer WebViewGold](rate.md)** — Vous aimez WebViewGold pour macOS ? Évaluez-le sur CodeCanyon en 10 secondes — cela fait vivre les mises à jour.
- **[Continuer avec iOS & Android](more-platforms.md)** — Réutilisez votre app web sur mobile : obtenez WebViewGold pour iOS et Android — ainsi que photos2webgallery pour macOS.
- **[Nous contacter](support.md)** — Obtenez de l'aide pour WebViewGold pour macOS : consultez le Centre d'assistance ou contactez directement l'équipe.

## Une app web, toutes les plateformes

Réutilisez le même site web pour des apps iOS, Android & macOS avec WebViewGold.

- [WebViewGold pour iOS](../ios/README.md)
- [WebViewGold pour Android](../android/README.md)

**Langues :** [🇺🇸 English](../../macos/README.md) · [🇩🇪 Deutsch](../../de/macos/README.md) · **🇫🇷 Français** · [🇪🇸 Español](../../es/macos/README.md) · [🇨🇳 中文](../../zh/macos/README.md)

