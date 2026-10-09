---
title: "Configuration de votre site web / application web – WebViewGold pour macOS Documentation"
description: "Préparez votre site web, PWA ou app web pour WebViewGold pour macOS : technologies prises en charge (HTML, PHP, WordPress, PWA, Lovable, Base44, Bolt…) et conseils pour une expérience de bureau native."
lang: "fr"
product: "WebViewGold pour macOS"
platform: "macOS"
category: "Prise en main"
slug: "setup-website"
canonical_url: "https://www.webviewgold.com/fr/docs/mac/#setupwebsite"
keywords:
  - "Configuration de votre application web"
  - "WebViewGold pour macOS"
  - "convertir un site web en app"
  - "documentation d’app WebView"
  - "SDK WebView macOS"
  - "PWA en app"
  - "HTML en app"
  - "pont JavaScript"
last_updated: "2026-10-09"
---

# Configuration de votre site web / application web – WebViewGold pour macOS

> **Résumé :** Préparez votre site web, PWA ou app web pour WebViewGold pour macOS : technologies prises en charge (HTML, PHP, WordPress, PWA, Lovable, Base44, Bolt…) et conseils pour une expérience de bureau native.

[Documentation](../README.md) › [WebViewGold pour macOS](README.md) › Configuration de votre application web

**Plateforme :** macOS · **Catégorie :** Prise en main · **Version en ligne :** [www.webviewgold.com/fr/docs/mac/#setupwebsite](https://www.webviewgold.com/fr/docs/mac/#setupwebsite)

---

Créez un site web ou une application web optimisée pour le bureau et téléchargez-la sur votre espace web. WebViewGold pour macOS prend en charge le HTML classique, PHP, WordPress, les Progressive Web Apps, les jeux HTML5, Wix, Bubble, jQuery Mobile ainsi que les générateurs modernes d'IA/no-code tels que Lovable, Base44 et Bolt. Un flux de travail d'implémentation professionnel consiste à créer votre produit principal en jQuery, Lovable, Base44, Bolt, React, Vue, Angular ou une autre pile web, puis à utiliser WebViewGold comme conteneur d'application Mac natif qui ajoute le packaging Xcode, le comportement natif des fenêtres macOS, la gestion des URL, les intégrations de fichiers et les options de distribution de l'application.

Optimisez l'expérience comme une véritable application de bureau macOS : utilisez des mises en page réactives pour les fenêtres redimensionnables, une navigation adaptée au clavier, des états de chargement et d'erreur clairs, des points de terminaison HTTPS et des écrans de secours concis pour les situations hors ligne ou de maintenance. Vous pouvez par exemple désactiver le zoom par l'utilisateur si cela correspond à votre spécification d'interface utilisateur :

```html
<meta name="viewport" content="width=device-width, user-scalable=no" />
```

## Exemple d'implémentation de type SDK

Conservez votre site web comme source canonique de la logique métier et exposez de petits assistants JavaScript documentés pour les actions purement natives. Cela permet à la même application web de rester utilisable dans les navigateurs, tandis que WebViewGold pour macOS fournit l'enveloppe de bureau. Pour le référencement, maintenez indexables les titres de route, les méta-descriptions, les en-têtes et les contenus structurés sur votre site public ; pour les utilisateurs de l'application, laissez WebViewGold charger ces mêmes routes dans une expérience d'application Mac native.

---

## Continuer la lecture

- ← Retour à : [Aperçu](README.md)
- Suivant → : [Configuration de WebViewGold](setup.md)
- Même fonctionnalité sur les autres plateformes : [iOS – Configurer l'application web](../ios/setup-website.md) · [Android – Configurer l'application web](../android/setup-website.md)
- Langues : [🇺🇸 English](../../macos/setup-website.md) · [🇩🇪 Deutsch](../../de/macos/setup-website.md) · **🇫🇷 Français** · [🇪🇸 Español](../../es/macos/setup-website.md) · [🇨🇳 中文](../../zh/macos/setup-website.md)

