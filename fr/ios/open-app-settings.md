---
title: "API d'ouverture des réglages de l'application – Documentation WebViewGold pour iOS"
description: "Envoyez les utilisateurs directement vers la page de votre application dans les Réglages d'iOS pour gérer autorisations et notifications."
lang: "fr"
product: "WebViewGold pour iOS"
platform: "iOS"
category: "API et fonctionnalités"
slug: "open-app-settings"
canonical_url: "https://www.webviewgold.com/fr/docs/iOS/open-app-settings/"
keywords:
  - "API d'ouverture des réglages"
  - "WebViewGold pour iOS"
  - "convertir un site web en app"
  - "documentation d’app WebView"
  - "SDK WebView iOS"
  - "PWA en app"
  - "HTML en app"
  - "pont JavaScript"
last_updated: "2026-10-09"
---

# API d'ouverture des réglages de l'application – WebViewGold pour iOS

> **Résumé :** Envoyez les utilisateurs directement vers la page de votre application dans les Réglages d'iOS pour gérer autorisations et notifications.

[Documentation](../README.md) › [WebViewGold pour iOS](README.md) › API d'ouverture des réglages

**Plateforme :** iOS · **Catégorie :** API et fonctionnalités · **Version en ligne :** [www.webviewgold.com/fr/docs/iOS/open-app-settings/](https://www.webviewgold.com/fr/docs/iOS/open-app-settings/)

---

L'**API d'ouverture des réglages de l'application** de WebViewGold envoie l'utilisateur directement vers la page de votre application dans l'app native **Réglages** d'iOS. Il peut y gérer les autorisations (appareil photo, position, notifications…), la langue et d'autres réglages de l'application — sans quitter votre application web pour chercher dans les Réglages d'iOS.

## Utilisation

Déclenchez l'écran depuis un lien HTML ou depuis JavaScript :

```html
<a href="settingsapp://">Ouvrir les réglages de l'application</a>
```

```javascript
window.location.href = "settingsapp://";
```

## Cas d'utilisation typiques

- L'utilisateur a refusé une autorisation (appareil photo, micro, position, notifications) — envoyez-le directement vers l'écran système pour la réactiver.
- Guider l'utilisateur vers les réglages de notifications de votre application, par ex. en combinaison avec l'appel `checkNativePushPermissions://` de l'[API de notifications push](push-notifications.md).

**Remarques :** aucun paramètre. Toute URL commençant par `settingsapp://` ouvre le même écran.

---

## Continuer la lecture

- ← Précédent : [API de lecture/écriture de valeur](read-write-value.md)
- Suivant → : [Share Extension](share-extension.md)
- Même fonctionnalité sur les autres plateformes : [Android – Open App Settings API](../android/open-app-settings.md)
- Langues : [🇺🇸 English](../../ios/open-app-settings.md) · [🇩🇪 Deutsch](../../de/ios/open-app-settings.md) · **🇫🇷 Français** · [🇪🇸 Español](../../es/ios/open-app-settings.md) · [🇨🇳 中文](../../zh/ios/open-app-settings.md)

> [!TIP]
> **Trop occupé ? Nous configurons votre app pour vous.** Notre équipe configure, compile & soumet votre app WebViewGold — clé en main, délai rapide, Made in Germany. [Faire configurer mon app →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **Compilez dans votre navigateur :** Pas de Mac, pas d’IDE : le **WebViewGold Cloud Builder** configure, compile & met en ligne votre app. [Découvrir Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
