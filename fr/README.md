---
title: "Documentation WebViewGold – Convertir votre site web en app native iOS, Android et macOS"
description: "Documentation officielle de WebViewGold en Markdown : transformez n’importe quel site web, PWA ou app web en app native iOS, Android ou macOS — guides de configuration, API JavaScript natives et publication sur les stores."
lang: "fr"
product: "WebViewGold"
canonical_url: "https://www.webviewgold.com/fr/docs/"
keywords:
  - "WebViewGold"
  - "convert website to app"
  - "WebView app template"
  - "PWA to native app"
  - "iOS WebView app"
  - "Android WebView app"
  - "macOS WebView app"
  - "JavaScript bridge"
last_updated: "2026-10-09"
---

# Documentation WebViewGold – Convertir votre site web en app native iOS, Android et macOS

> Documentation officielle de WebViewGold en Markdown : transformez n’importe quel site web, PWA ou app web en app native iOS, Android ou macOS — guides de configuration, API JavaScript natives et publication sur les stores.

WebViewGold est un modèle d’app Xcode et Android Studio prêt à l’emploi, développé par OnlineAppCreator, qui transforme votre site web, PWA, tableau de bord SaaS, boutique en ligne ou app web générée par IA en app native. Votre site reste la source unique : vous activez les fonctionnalités natives — notifications push, achats intégrés, AdMob, scanner QR/codes-barres, biométrie, liens profonds et bien plus — via de simples options de configuration et des API JavaScript / schémas d’URL.

## Commencer ici

| Plateforme | Documentation | Projet / IDE | Sujets |
|---|---|---|---|
| **iOS** | [WebViewGold pour iOS](ios/README.md) | Xcode · Swift (`Config.swift`) | 60 pages |
| **Android** | [WebViewGold pour Android](android/README.md) | Android Studio · Java (`Config.java`) | 47 pages |
| **macOS** | [WebViewGold pour macOS](macos/README.md) | Xcode (`config.json`, `index.html`) | 14 pages |

## Organisation de cette documentation

Chaque plateforme dispose d’une page d’aperçu et d’une page Markdown par sujet. Chaque page commence par un court résumé et des métadonnées (plateforme, catégorie, URL canonique) et se termine par des liens vers le sujet précédent/suivant, la même fonctionnalité sur les autres plateformes et toutes les traductions.

```text
docs-for-github/
├── README.md            (English)
├── llms.txt             (AI / LLM index)
├── llms-full.txt        (all English pages in one file)
├── ios/                 (WebViewGold for iOS)
├── android/             (WebViewGold for Android)
├── macos/               (WebViewGold for macOS)
├── de/ fr/ es/ zh/      (translations, same structure)
└── assets/              (screenshots & images)
```

## Questions fréquentes

### Qu’est-ce que WebViewGold ?

WebViewGold est un modèle d’app native pour iOS, Android et macOS qui convertit un site ou une app web en app native prête pour les stores. Il est vendu via Envato/CodeCanyon et documenté sur [webviewgold.com/docs](https://www.webviewgold.com/fr/docs/).

### Faut-il savoir programmer ?

Non. Vous insérez votre URL et activez ou désactivez les options dans un seul fichier de configuration (`Config.swift` sur iOS, `Config.java` sur Android). Les fonctionnalités natives se déclenchent depuis votre app web avec de simples liens comme `rateapp://` ou de petits extraits JavaScript.

### Quels sites et frameworks sont pris en charge ?

Les sites HTML/PHP classiques, WordPress, les PWA, les projets jQuery Mobile et les apps web modernes créées avec Lovable, Base44, Bolt, Bubble, React, Vue, Angular ou des outils similaires. Vous pouvez charger une URL distante, empaqueter des fichiers HTML locaux ou combiner les deux avec un mode hors ligne.

### Puis-je publier l’app sur l’App Store et Google Play ?

Oui. Les guides *Compiler et publier* expliquent la procédure manuelle. Sinon, le WebViewGold Cloud Builder compile et envoie votre app depuis le navigateur, ou l’équipe WeSetupYourWebViewApp s’occupe de tout pour vous.

### Où trouver de l’aide ?

Consultez le [Centre d’assistance WebViewGold](https://www.webviewgold.com/support-center/) pour la FAQ et les problèmes connus, ou contactez l’équipe via la page *Support et contact* de votre plateforme.

## Langues

[🇺🇸 English](../README.md) · [🇩🇪 Deutsch](../de/README.md) · **🇫🇷 Français** · [🇪🇸 Español](../es/README.md) · [🇨🇳 中文](../zh/README.md)

## À propos

WebViewGold est développé par OnlineAppCreator (jocapps GmbH) en Allemagne. Cette édition Markdown reflète la documentation officielle en ligne sur [www.webviewgold.com/fr/docs](https://www.webviewgold.com/fr/docs/) ; la version en ligne fait foi.
