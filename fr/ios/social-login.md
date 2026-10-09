---
title: "Assistant de connexion sociale (Google, Facebook & Apple) – Documentation WebViewGold pour iOS"
description: "Faites fonctionner les connexions OAuth Google, Facebook et Apple de manière fiable dans votre app WebView iOS grâce aux assistants de connexion intégrés."
lang: "fr"
product: "WebViewGold pour iOS"
platform: "iOS"
category: "API et fonctionnalités"
slug: "social-login"
canonical_url: "https://www.webviewgold.com/fr/docs/iOS/social-login/"
keywords:
  - "Social Login Helper"
  - "WebViewGold pour iOS"
  - "convertir un site web en app"
  - "documentation d’app WebView"
  - "SDK WebView iOS"
  - "PWA en app"
  - "HTML en app"
  - "pont JavaScript"
last_updated: "2026-10-09"
---

# Assistant de connexion sociale (Google, Facebook & Apple) – WebViewGold pour iOS

> **Résumé :** Faites fonctionner les connexions OAuth Google, Facebook et Apple de manière fiable dans votre app WebView iOS grâce aux assistants de connexion intégrés.

[Documentation](../README.md) › [WebViewGold pour iOS](README.md) › Social Login Helper

**Plateforme :** iOS · **Catégorie :** API et fonctionnalités · **Version en ligne :** [www.webviewgold.com/fr/docs/iOS/social-login/](https://www.webviewgold.com/fr/docs/iOS/social-login/)

---

Google, Facebook et d'autres fournisseurs OAuth restreignent les connexions depuis des WebViews intégrées (p. ex. l'erreur *« disallowed_useragent »* de Google). Le **Social Login Helper** intégré à WebViewGold permet à ces connexions de fonctionner de manière fiable dans votre app iOS — sans modifier le flux de connexion de votre site web.

## Fonctionnement

Vous définissez des préfixes d'URL qui apparaissent pendant le flux de connexion de votre app web. Dès que l'une de ces URL déclencheuses se charge, WebViewGold ouvre la connexion dans une fenêtre de connexion popup dédiée avec un user agent ajusté que le fournisseur OAuth accepte. Après une connexion réussie, le flux revient automatiquement à votre app web. « Sign in with Apple » (`appleid.apple.com`) est détecté et géré automatiquement — aucune configuration nécessaire.

## Configuration

Ouvrez **Config.swift** et définissez les préfixes d'URL déclencheurs de votre flux de connexion :

```javascript
var google_login_helper_triggers: [String] = ["https://accounts.google.com", "https://accounts.youtube.com"]
var facebook_login_helper_triggers: [String] = ["https://m.facebook.com", "https://www.facebook.com"]
```

- `google_login_helper_triggers` — préfixes d'URL chargés pendant une connexion Google sur votre site web.
- `facebook_login_helper_triggers` — préfixes d'URL chargés pendant une connexion Facebook sur votre site web.

Pour trouver les bonnes URL déclencheuses, lancez le flux de connexion de votre site web dans un navigateur de bureau et notez par quelles URL passe la redirection OAuth.

## Ouvrir une URL d'authentification dans le navigateur externe

En alternative, vous pouvez transmettre explicitement une URL de connexion au navigateur système (la session vit alors dans le navigateur, pas dans l'app) :

```javascript
window.location.href = "googlelogin://" + encodeURIComponent("https://accounts.google.com/o/oauth2/v2/auth?...");
```

WebViewGold décode l'URL après le préfixe `googlelogin://` et l'ouvre en externe.

## Quand utiliser le helper

Essayez d'abord les options plus simples — elles résolvent déjà de nombreux problèmes de connexion :

- Ouvrez le domaine de connexion dans un onglet de navigateur in-app ou dans le navigateur externe via l'[API URL Handling](url-handling.md) (p. ex. `specialLinkHandlingOptions`, `safariblacklist`).
- Définissez un [user agent personnalisé](setup.md) (`useragent_iphone` / `useragent_ipad`).

Si la connexion échoue toujours dans l'app, les déclencheurs du Social Login Helper sont la solution recommandée.

---

## Continuer la lecture

- ← Précédent : [API de gestion des URL](url-handling.md)
- Suivant → : [API de reconnexion](reconnect.md)
- Langues : [🇺🇸 English](../../ios/social-login.md) · [🇩🇪 Deutsch](../../de/ios/social-login.md) · **🇫🇷 Français** · [🇪🇸 Español](../../es/ios/social-login.md) · [🇨🇳 中文](../../zh/ios/social-login.md)

> [!TIP]
> **Trop occupé ? Nous configurons votre app pour vous.** Notre équipe configure, compile & soumet votre app WebViewGold — clé en main, délai rapide, Made in Germany. [Faire configurer mon app →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **Compilez dans votre navigateur :** Pas de Mac, pas d’IDE : le **WebViewGold Cloud Builder** configure, compile & met en ligne votre app. [Découvrir Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
