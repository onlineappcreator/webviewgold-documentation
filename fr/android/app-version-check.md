---
title: "API de vérification de version de l'application – Documentation WebViewGold pour Android"
description: "Détectez la version installée de l'application depuis votre application web et invitez les utilisateurs à effectuer la mise à jour si nécessaire."
lang: "fr"
product: "WebViewGold pour Android"
platform: "Android"
category: "API et fonctionnalités"
slug: "app-version-check"
canonical_url: "https://www.webviewgold.com/fr/docs/android/app-version-check/"
keywords:
  - "API de vérification de version"
  - "WebViewGold pour Android"
  - "convertir un site web en app"
  - "documentation d’app WebView"
  - "SDK WebView Android"
  - "PWA en app"
  - "HTML en app"
  - "pont JavaScript"
last_updated: "2026-10-09"
---

# API de vérification de version de l'application – WebViewGold pour Android

> **Résumé :** Détectez la version installée de l'application depuis votre application web et invitez les utilisateurs à effectuer la mise à jour si nécessaire.

[Documentation](../README.md) › [WebViewGold pour Android](README.md) › API de vérification de version

**Plateforme :** Android · **Catégorie :** API et fonctionnalités · **Version en ligne :** [www.webviewgold.com/fr/docs/android/app-version-check/](https://www.webviewgold.com/fr/docs/android/app-version-check/)

---

Grâce à cette API App Version Check de WebViewGold, votre site web/application web peut **récupérer la version de l'application Android** utilisée par l'utilisateur de votre application Android. Cette API est particulièrement utile si vous souhaitez informer les utilisateurs d'une version antérieure qu'ils doivent mettre à jour leur application. De plus, vous pouvez masquer les sections de l'application web qui nécessitent des fonctionnalités prises en charge par une version spécifique de l'application.\
Utilisez du JavaScript vers ce type d'URL pour lire et afficher la version de l'application et le numéro de build :

```html
<script>
window.location.href = "getappversion://";
alert(versionNumber);
alert(bundleNumber);
</script>
```

**Vous pouvez aussi régler  `AUTO_INJECT_VARIABLES`  sur `true` dans Config.java afin d'injecter automatiquement cette valeur (et d'autres) dans le JavaScript sans avoir à appeler une URL au préalable.**

---

## Continuer la lecture

- ← Précédent : [API de capture d'écran](take-screenshot.md)
- Suivant → : [API Contacts](contacts.md)
- Même fonctionnalité sur les autres plateformes : [iOS – API de vérification de version](../ios/app-version-check.md)
- Langues : [🇺🇸 English](../../android/app-version-check.md) · [🇩🇪 Deutsch](../../de/android/app-version-check.md) · **🇫🇷 Français** · [🇪🇸 Español](../../es/android/app-version-check.md) · [🇨🇳 中文](../../zh/android/app-version-check.md)

> [!TIP]
> **Trop occupé ? Nous configurons votre app pour vous.** Notre équipe configure, compile & soumet votre app WebViewGold — clé en main, délai rapide, Made in Germany. [Faire configurer mon app →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_android_doc_online)
>
> **Compilez dans votre navigateur :** Pas de Mac, pas d’IDE : le **WebViewGold Cloud Builder** configure, compile & met en ligne votre app. [Découvrir Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=android_docs)
