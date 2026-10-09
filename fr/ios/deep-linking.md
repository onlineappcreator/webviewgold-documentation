---
title: "API de deep linking – Documentation WebViewGold pour iOS"
description: "Lancez votre application iOS via des schémas d'URL personnalisés et redirigez les utilisateurs par deep link vers des pages précises de votre application web."
lang: "fr"
product: "WebViewGold pour iOS"
platform: "iOS"
category: "API et fonctionnalités"
slug: "deep-linking"
canonical_url: "https://www.webviewgold.com/fr/docs/iOS/deep-linking/"
keywords:
  - "API de deep linking"
  - "WebViewGold pour iOS"
  - "convertir un site web en app"
  - "documentation d’app WebView"
  - "SDK WebView iOS"
  - "PWA en app"
  - "HTML en app"
  - "pont JavaScript"
last_updated: "2026-10-09"
---

# API de deep linking – WebViewGold pour iOS

> **Résumé :** Lancez votre application iOS via des schémas d'URL personnalisés et redirigez les utilisateurs par deep link vers des pages précises de votre application web.

[Documentation](../README.md) › [WebViewGold pour iOS](README.md) › API de deep linking

**Plateforme :** iOS · **Catégorie :** API et fonctionnalités · **Version en ligne :** [www.webviewgold.com/fr/docs/iOS/deep-linking/](https://www.webviewgold.com/fr/docs/iOS/deep-linking/)

---

L'**API Deep Linking** facilite l'orientation des utilisateurs vers un contenu spécifique au sein de votre application. WebViewGold vous permet de configurer un schéma d'URL personnalisé (par exemple `webviewgold://`) qui peut être déclenché depuis des applications comme **Mail, Safari et d'autres** pour ouvrir des liens directement dans votre application WebView.

**Remarque :** l'application doit d'abord être installée pour que cette fonctionnalité fonctionne.

**Vous pouvez également** utiliser notre [**API Universal Links**](universal-links.md). Bien qu'elle fonctionne de manière similaire, elle utilise une syntaxe différente, plus courante que celle de l'API Deep Linking. Pour la plupart des applications, il est judicieux de choisir l'une ou l'autre, mais pas les deux.

Pour configurer le **Deep Linking** dans votre application iOS, veuillez suivre les étapes ci-dessous :

1. **Ouvrez Config.swift :**
   - Réglez `ShowExternalLink` sur `true`.

![Configuration du Deep Linking](../../assets/ios/img/universallinks.webp)
2. **Ouvrez Info.plist :**
   - Remplacez le schéma d'URL par le nom de votre propre application (par exemple `your-app-name://` au lieu de `webviewgold://`).

![Info.plist est un emplacement puissant pour configurer le deep linking, qui peut également être déclenché depuis différentes applications](../../assets/ios/img/infoplist.webp)

**Terminé ! :)** L'exemple ci-dessous ouvrirait google.com dans l'application WebView :

```
WebViewGold://url?link=https://www.google.com
```

[![Regarder la vidéo: API de deep linking](https://img.youtube.com/vi/mW4H_gUKU28/hqdefault.jpg)](https://www.youtube.com/watch?v=mW4H_gUKU28)

---

## Continuer la lecture

- ← Précédent : [API Universal Links](universal-links.md)
- Suivant → : [API de partage d'app](app-sharing-dialog.md)
- Même fonctionnalité sur les autres plateformes : [macOS – API Deeplinking](../macos/deep-linking.md)
- Langues : [🇺🇸 English](../../ios/deep-linking.md) · [🇩🇪 Deutsch](../../de/ios/deep-linking.md) · **🇫🇷 Français** · [🇪🇸 Español](../../es/ios/deep-linking.md) · [🇨🇳 中文](../../zh/ios/deep-linking.md)

> [!TIP]
> **Trop occupé ? Nous configurons votre app pour vous.** Notre équipe configure, compile & soumet votre app WebViewGold — clé en main, délai rapide, Made in Germany. [Faire configurer mon app →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **Compilez dans votre navigateur :** Pas de Mac, pas d’IDE : le **WebViewGold Cloud Builder** configure, compile & met en ligne votre app. [Découvrir Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
