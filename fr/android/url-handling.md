---
title: "API de gestion des URL – Documentation WebViewGold pour Android"
description: "Décidez quels liens s'ouvrent dans votre application Android, dans les Chrome Custom Tabs ou dans le navigateur externe."
lang: "fr"
product: "WebViewGold pour Android"
platform: "Android"
category: "API et fonctionnalités"
slug: "url-handling"
canonical_url: "https://www.webviewgold.com/fr/docs/android/url-handling/"
keywords:
  - "API de gestion des URL"
  - "WebViewGold pour Android"
  - "convertir un site web en app"
  - "documentation d’app WebView"
  - "SDK WebView Android"
  - "PWA en app"
  - "HTML en app"
  - "pont JavaScript"
last_updated: "2026-10-09"
---

# API de gestion des URL – WebViewGold pour Android

> **Résumé :** Décidez quels liens s'ouvrent dans votre application Android, dans les Chrome Custom Tabs ou dans le navigateur externe.

[Documentation](../README.md) › [WebViewGold pour Android](README.md) › API de gestion des URL

**Plateforme :** Android · **Catégorie :** API et fonctionnalités · **Version en ligne :** [www.webviewgold.com/fr/docs/android/url-handling/](https://www.webviewgold.com/fr/docs/android/url-handling/)

---

Pour améliorer l'expérience utilisateur, il est souvent judicieux de personnaliser la façon dont votre application gère différents types de liens web. Par exemple, les boutons des réseaux sociaux peuvent être configurés pour s'ouvrir dans le navigateur système ou dans l'application correspondante, plutôt que dans votre application. WebViewGold propose des paramètres flexibles pour personnaliser la gestion des URL de votre application Android basée sur WebView :

## Types de liens

1. **Liens externes :** liens qui mènent vers un **domaine différent** du domaine principal de votre application.
   - **Exemple :** si le domaine de votre application est **mydomain.com**, un lien externe serait **google.com**.
2. **Liens internes :** liens qui restent au sein du **même domaine** que votre application.
   - **Exemple :** si le domaine de votre application est **mydomain.com**, un lien interne serait **mydomain.com/purchase**.
3. **Liens spéciaux :** liens qui comportent des attributs spéciaux, comme **target="_blank"** ou des liens se terminant par **#**.

## Options de gestion des liens

Vous pouvez configurer le comportement des liens en modifiant les paramètres du fichier **Config.java** comme indiqué ci-dessous.

## Gestion des liens externes

- **Option par défaut (0) :** pour ouvrir les liens externes dans le WebView principal (comme les liens internes), réglez `EXTERNAL_LINK_HANDLING_OPTIONS` sur `0`.
- **Option 1 :** pour ouvrir les liens externes dans un nouvel onglet in-app, réglez `EXTERNAL_LINK_HANDLING_OPTIONS` sur `1`.
- **Option 2 :** pour ouvrir les liens externes dans le navigateur système par défaut de l'appareil (par ex. Chrome, Safari), réglez `EXTERNAL_LINK_HANDLING_OPTIONS` sur `2`.

## Gestion des liens spéciaux

- **Option 0 :** pour ouvrir les liens spéciaux dans le WebView principal de l'application, réglez `SPECIAL_LINK_HANDLING_OPTIONS` sur `0`.
- **Option 1 :** pour ouvrir les liens spéciaux dans un nouvel onglet in-app, réglez `SPECIAL_LINK_HANDLING_OPTIONS` sur `1`.
- **Option 2 :** pour ouvrir les liens spéciaux dans le navigateur système par défaut de l'appareil (par ex. Chrome, Safari), réglez `SPECIAL_LINK_HANDLING_OPTIONS` sur `2`.

Remarque : ce paramètre remplace `EXTERNAL_LINK_HANDLING_OPTIONS` pour les liens qui sont à la fois externes et spéciaux.

## Personnalisation de l'accès aux liens : liste blanche et liste noire

Pour créer des exceptions pour des sites ou pages spécifiques, ouvrez **Config.java** et ajoutez le domaine à l'un des tableaux suivants :

- **BROWSER_WHITELIST :** répertorie les domaines spécifiques à ouvrir dans le WebView de l'application.
- **BROWSER_BLACKLIST :** répertorie les domaines spécifiques à ouvrir dans le navigateur externe.

Pour des instructions détaillées sur la configuration des liens dans votre application Android, regardez le tutoriel vidéo ci-dessous :

[![Regarder la vidéo: API de gestion des URL](https://img.youtube.com/vi/lq7jgaB6TxY/hqdefault.jpg)](https://www.youtube.com/watch?v=lq7jgaB6TxY)

---

## Gestion des URL – Utiliser le navigateur in-app pour des liens spécifiques

Certains liens, comme une page de Conditions générales, peuvent ne pas être assez importants pour être ouverts dans un navigateur système externe, mais rester trop spécifiques pour le WebView principal de votre application. WebViewGold propose une solution créative pour gérer ces liens : **un onglet de navigateur in-app** qui s'ouvre par-dessus le WebView principal, offrant une expérience hybride entre application et navigateur. Voici à quoi cela ressemble :\
![Ouvrir un lien dans un navigateur/onglet in-app supplémentaire dans les applications Android basées sur WebView](../../assets/android/img/tabs.webp)

### Principales caractéristiques de l'onglet du navigateur in-app

- L'onglet du navigateur in-app comprend une **barre d'adresse** et des **boutons de navigation**, offrant une expérience plus proche d'un navigateur que le WebView principal.
- Idéal pour les contenus qui nécessitent une navigation aisée, comme des tutoriels, des bases de connaissances ou des pages contenant des informations spécifiques.

### Comment utiliser l'onglet du navigateur in-app dans votre application Android basée sur WebView

Pour ouvrir un lien dans l'onglet du navigateur in-app, formatez l'URL dans votre HTML comme suit :

```html
<a href='#' onClick="top.location.href='https://www.example.com';">Open Example Page</a>
```

**Exemple :** pour ouvrir Google, utilisez :

```html
<a href='#' onClick="top.location.href='https://www.google.com';">Open Google</a>
```

**Tester le comportement des liens :**\
Pour voir comment votre application gérera les différents types de liens, utilisez l'URL suivante comme URL du WebView pendant les tests :\
Lien de test : <https://www.webviewgold.com/demo/testlinks.php>\
**Remarque :** vous pouvez également ouvrir le même domaine dans votre navigateur de bureau pour visualiser le code source et copier le format pour vos liens.

---

## Forcer un lien précis à s'ouvrir dans l'onglet in-app ou le navigateur (préfixe `newtab:`)

Parfois, vous souhaitez qu'**un seul lien précis** s'ouvre dans l'onglet de navigateur in-app (ou dans le navigateur externe) — indépendamment de votre configuration globale de gestion des liens. Il suffit de préfixer l'URL avec `newtab:` :

```html
<a href="newtab:https://www.example.com">Ouvrir la page d'exemple</a>
```

Le lien préfixé est alors traité comme un lien spécial : avec `SPECIAL_LINK_HANDLING_OPTIONS` défini sur `1`, il s'ouvre dans l'onglet de navigateur in-app, avec `2` dans le navigateur système externe. Cela nécessite que `SPECIAL_LINK_HANDLING_OPTIONS` soit défini sur une valeur autre que `0` dans **Config.java**.

## Ouvrir une URL d'authentification dans un Chrome Custom Tab (`googlelogin://`)

Certains fournisseurs de connexion (notamment **Google Sign-In**) bloquent l'authentification dans les WebViews classiques. Si l'[outil Social Media Login Helper](setup.md) ne convient pas à votre parcours, vous pouvez ouvrir l'URL d'authentification dans un **Chrome Custom Tab** sécurisé en la préfixant avec `googlelogin://` :

```javascript
window.location.href = "googlelogin://" + encodeURIComponent("https://accounts.google.com/o/oauth2/v2/auth?...");
```

L'URL après le préfixe est décodée et ouverte dans un Chrome Custom Tab intégré à l'application, où la connexion peut être finalisée. Redirigez ensuite l'utilisateur vers votre web app (p. ex. via votre URL de redirection OAuth).

---

## Continuer la lecture

- ← Précédent : [Navigation Drawer & Footer](navigation-drawer.md)
- Suivant → : [API CSS et JS personnalisés](custom-css-js.md)
- Même fonctionnalité sur les autres plateformes : [iOS – API de gestion des URL](../ios/url-handling.md)
- Langues : [🇺🇸 English](../../android/url-handling.md) · [🇩🇪 Deutsch](../../de/android/url-handling.md) · **🇫🇷 Français** · [🇪🇸 Español](../../es/android/url-handling.md) · [🇨🇳 中文](../../zh/android/url-handling.md)

> [!TIP]
> **Trop occupé ? Nous configurons votre app pour vous.** Notre équipe configure, compile & soumet votre app WebViewGold — clé en main, délai rapide, Made in Germany. [Faire configurer mon app →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_android_doc_online)
>
> **Compilez dans votre navigateur :** Pas de Mac, pas d’IDE : le **WebViewGold Cloud Builder** configure, compile & met en ligne votre app. [Découvrir Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=android_docs)
