---
title: "Open App Settings API – Documentation WebViewGold pour Android"
description: "Send the user straight to the system App-info screen from your web app to manage permissions, notifications, storage, or force-stop your Android app."
lang: "fr"
product: "WebViewGold pour Android"
platform: "Android"
category: "API et fonctionnalités"
slug: "open-app-settings"
canonical_url: "https://www.webviewgold.com/fr/docs/android/open-app-settings/"
keywords:
  - "Open App Settings API"
  - "WebViewGold pour Android"
  - "convertir un site web en app"
  - "documentation d’app WebView"
  - "SDK WebView Android"
  - "PWA en app"
  - "HTML en app"
  - "pont JavaScript"
last_updated: "2026-10-09"
---

# Open App Settings API – WebViewGold pour Android

> **Résumé :** Send the user straight to the system App-info screen from your web app to manage permissions, notifications, storage, or force-stop your Android app.

[Documentation](../README.md) › [WebViewGold pour Android](README.md) › Open App Settings API

**Plateforme :** Android · **Catégorie :** API et fonctionnalités · **Version en ligne :** [www.webviewgold.com/fr/docs/android/open-app-settings/](https://www.webviewgold.com/fr/docs/android/open-app-settings/)

---

L'**API Open App Settings** de WebViewGold envoie directement l'utilisateur vers l'écran système **Informations sur l'application** de votre application. À partir de là, il peut gérer les permissions, les notifications, le stockage, ou forcer l'arrêt de l'application — sans quitter votre application web pour chercher dans les paramètres Android.

## Utilisation

Déclenchez cet écran depuis un lien HTML ou depuis JavaScript :

```html
<a href="settingsapp://">Open app settings</a>
```

```javascript
window.location.href = "settingsapp://";
```

## Cas d'usage typiques

- L'utilisateur a refusé une permission (caméra, microphone, localisation, notifications) — envoyez-le directement à l'écran système pour la réactiver.
- Guider l'utilisateur pour désactiver l'optimisation de la batterie ou vider le cache depuis le système d'exploitation.

**Remarques :** Aucun paramètre. Toute URL commençant par `settingsapp://` déclenche le même écran. Fonctionne sur toutes les versions Android prises en charge.

---

## Continuer la lecture

- ← Précédent : [Plugin NFC](nfc.md)
- Suivant → : [Reconnect API](reconnect.md)
- Même fonctionnalité sur les autres plateformes : [iOS – API d'ouverture des réglages](../ios/open-app-settings.md)
- Langues : [🇺🇸 English](../../android/open-app-settings.md) · [🇩🇪 Deutsch](../../de/android/open-app-settings.md) · **🇫🇷 Français** · [🇪🇸 Español](../../es/android/open-app-settings.md) · [🇨🇳 中文](../../zh/android/open-app-settings.md)

> [!TIP]
> **Trop occupé ? Nous configurons votre app pour vous.** Notre équipe configure, compile & soumet votre app WebViewGold — clé en main, délai rapide, Made in Germany. [Faire configurer mon app →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_android_doc_online)
>
> **Compilez dans votre navigateur :** Pas de Mac, pas d’IDE : le **WebViewGold Cloud Builder** configure, compile & met en ligne votre app. [Découvrir Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=android_docs)
