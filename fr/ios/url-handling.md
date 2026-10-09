---
title: "API de gestion des URL – Documentation WebViewGold pour iOS"
description: "Décidez quels liens s'ouvrent dans votre app, dans un onglet de navigateur intégré ou dans Safari : un contrôle total de la gestion des URL pour iOS."
lang: "fr"
product: "WebViewGold pour iOS"
platform: "iOS"
category: "API et fonctionnalités"
slug: "url-handling"
canonical_url: "https://www.webviewgold.com/fr/docs/iOS/url-handling/"
keywords:
  - "API de gestion des URL"
  - "WebViewGold pour iOS"
  - "convertir un site web en app"
  - "documentation d’app WebView"
  - "SDK WebView iOS"
  - "PWA en app"
  - "HTML en app"
  - "pont JavaScript"
last_updated: "2026-10-09"
---

# API de gestion des URL – WebViewGold pour iOS

> **Résumé :** Décidez quels liens s'ouvrent dans votre app, dans un onglet de navigateur intégré ou dans Safari : un contrôle total de la gestion des URL pour iOS.

[Documentation](../README.md) › [WebViewGold pour iOS](README.md) › API de gestion des URL

**Plateforme :** iOS · **Catégorie :** API et fonctionnalités · **Version en ligne :** [www.webviewgold.com/fr/docs/iOS/url-handling/](https://www.webviewgold.com/fr/docs/iOS/url-handling/)

---

Pour améliorer l'expérience utilisateur, il est souvent judicieux de personnaliser la façon dont votre application gère les différents types de liens web. Par exemple, les boutons de réseaux sociaux peuvent être configurés pour s'ouvrir dans le navigateur système ou dans l'application correspondante, plutôt que dans votre application. WebViewGold propose des paramètres flexibles pour personnaliser la gestion des URL de votre application iOS basée sur WebView.

## Types de liens

1. **Liens externes :** liens qui mènent vers un **domaine différent** du domaine principal de votre application.
   - **Exemple :** si le domaine de votre application est **mydomain.com**, un lien externe serait **google.com**.
2. **Liens internes :** liens qui restent dans le **même domaine** que votre application.
   - **Exemple :** si le domaine de votre application est **mydomain.com**, un lien interne serait **mydomain.com/purchase**.
3. **Liens spéciaux :** liens comportant des attributs particuliers, tels que **target="_blank"**.

## Pour configurer l'API URL Handling, ouvrez Config.swift

1. Pour définir le comportement par défaut des **liens externes** :
   - Définissez `externalLinkHandlingOptions` sur `0` pour ouvrir les liens externes dans l'application par défaut, ou sur `2` pour TOUJOURS les ouvrir dans un autre navigateur (Safari).

2. Pour définir le comportement par défaut des **liens spéciaux** (par ex. **target="_blank"**) :
   - Définissez `specialLinkHandlingOptions` sur `0` pour ouvrir les liens spéciaux dans l'application, sur `1` pour les ouvrir dans un nouvel onglet (un navigateur intégré supplémentaire), ou sur `2` pour les ouvrir dans un autre navigateur (Safari).

3. Pour définir les domaines qui s'ouvrent ***toujours* dans Safari** (indépendamment du paramètre `externalLinkHandlingOptions`) :
   - Ajoutez les domaines souhaités à la liste `safariwhitelist`.
   - Insérez un autre hôte comme ceci : ["alwaysopeninsafari.com", "google.com", "m.facebook.com"].
   - Veuillez saisir l'hôte exactement comme vous établissez le lien vers celui-ci (avec ou sans www, mais toujours sans http/https).

4. Pour définir les domaines qui ne s'ouvrent ***jamais* dans Safari** (indépendamment du paramètre `externalLinkHandlingOptions`) :
   - Ajoutez les domaines souhaités à la liste `safariblacklist`.
   - Insérez un autre hôte comme ceci : ["alwaysopeninsafari.com", "google.com", "m.facebook.com"].
   - Veuillez saisir l'hôte exactement comme vous établissez le lien vers celui-ci (avec ou sans www, mais toujours sans http/https).

5. Pour définir les domaines qui s'ouvrent ***toujours*** ou ***jamais* dans un onglet intégré** (indépendamment du paramètre `externalLinkHandlingOptions`) :
   - Ajoutez les domaines souhaités à la liste `alwaysOpenInInAppTab` ou `neverOpenInInAppTab`.

## Ouvrir les liens dans un onglet / navigateur intégré supplémentaire

Certains liens, comme une page de conditions générales, peuvent ne pas être assez importants pour s'ouvrir dans un navigateur système externe, tout en étant trop spécifiques pour la WebView principale de votre application. WebViewGold propose une solution créative pour gérer ces liens : **un onglet de navigateur intégré** qui s'ouvre par-dessus la WebView principale, offrant une expérience hybride entre l'application et le navigateur. Voici à quoi cela ressemble :

![Ouvrir un lien dans un onglet / navigateur intégré supplémentaire SFSafariViewController](../../assets/ios/img/tabs.webp)

### Principales caractéristiques de l'onglet de navigateur intégré

- L'onglet de navigateur intégré comprend une **barre d'adresse** et des **boutons de navigation**, offrant une expérience plus proche d'un navigateur que la WebView principale.
- Idéal pour les contenus nécessitant une navigation facile, tels que les tutoriels, les bases de connaissances ou les pages contenant des informations spécifiques.

### Comment utiliser l'onglet de navigateur intégré dans votre application iOS basée sur WebView

Pour ouvrir un lien dans l'onglet de navigateur intégré, définissez `specialLinkHandlingOptions` sur `1` et formatez l'URL dans votre HTML comme suit :

```html
<a href="https://www.example.com" target="_blank">Ouvrir le lien dans un onglet intégré</a>
```

En résumé, un **lien spécial** est classé comme un lien portant l'attribut de cible « _blank ». Dans un navigateur classique, cela ferait en sorte que le lien s'ouvre dans un nouvel onglet. Dans une application WebViewGold, vous pouvez faire en sorte qu'il s'ouvre dans l'onglet intégré à la place.

Veuillez noter que si le lien que vous utilisez est externe (il a un domaine différent de celui de votre site, comme « www.google.com », par exemple), assurez-vous également que `externalLinkHandlingOptions` est défini sur `0`, sans quoi l'ouverture de tous les liens externes dans un autre navigateur prendra le dessus et le lien spécial externe s'ouvrira dans l'application Safari.

**Tester le comportement des liens :**\
Pour voir comment votre application gérera les différents types de liens, utilisez l'URL suivante comme URL de la WebView pendant les tests :\
Lien de test : <https://www.webviewgold.com/demo/testlinks.php>\
**Remarque :** vous pouvez également ouvrir le même domaine dans votre navigateur de bureau pour consulter le code source et copier le format pour vos liens.

---

## Continuer la lecture

- ← Précédent : [API Pull-to-Refresh](pull-to-refresh.md)
- Suivant → : [Social Login Helper](social-login.md)
- Même fonctionnalité sur les autres plateformes : [Android – API de gestion des URL](../android/url-handling.md)
- Langues : [🇺🇸 English](../../ios/url-handling.md) · [🇩🇪 Deutsch](../../de/ios/url-handling.md) · **🇫🇷 Français** · [🇪🇸 Español](../../es/ios/url-handling.md) · [🇨🇳 中文](../../zh/ios/url-handling.md)

> [!TIP]
> **Trop occupé ? Nous configurons votre app pour vous.** Notre équipe configure, compile & soumet votre app WebViewGold — clé en main, délai rapide, Made in Germany. [Faire configurer mon app →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **Compilez dans votre navigateur :** Pas de Mac, pas d’IDE : le **WebViewGold Cloud Builder** configure, compile & met en ligne votre app. [Découvrir Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
