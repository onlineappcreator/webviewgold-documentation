---
title: "API App Links et Deep Linking – Documentation WebViewGold pour Android"
description: "Ouvrez les liens vers votre domaine directement dans votre application Android grâce aux App Links et au deep linking par schéma d'URL personnalisé."
lang: "fr"
product: "WebViewGold pour Android"
platform: "Android"
category: "API et fonctionnalités"
slug: "app-links"
canonical_url: "https://www.webviewgold.com/fr/docs/android/app-links/"
keywords:
  - "App Links / Deep Linking"
  - "WebViewGold pour Android"
  - "convertir un site web en app"
  - "documentation d’app WebView"
  - "SDK WebView Android"
  - "PWA en app"
  - "HTML en app"
  - "pont JavaScript"
last_updated: "2026-10-09"
---

# API App Links et Deep Linking – WebViewGold pour Android

> **Résumé :** Ouvrez les liens vers votre domaine directement dans votre application Android grâce aux App Links et au deep linking par schéma d'URL personnalisé.

[Documentation](../README.md) › [WebViewGold pour Android](README.md) › App Links / Deep Linking

**Plateforme :** Android · **Catégorie :** API et fonctionnalités · **Version en ligne :** [www.webviewgold.com/fr/docs/android/app-links/](https://www.webviewgold.com/fr/docs/android/app-links/)

---

L'API App Links / Deeplinking de WebViewGold permet aux utilisateurs d'ouvrir des pages spécifiques de votre application depuis des sources externes telles que les e-mails, les réseaux sociaux ou les applications de messagerie.

## WebViewGold pour Android prend en charge deux méthodes de deep linking

- **Deep links standard basés sur une URL :** par exemple `https://www.example.org/subpages/example1`
- **Deep links à schéma personnalisé :** par exemple `webviewgold://https://www.example.org/subpages/example2`

## Étape 1 : Configurer votre schéma de lien dans AndroidManifest.xml

Pour prendre en charge le deep linking standard, configurez votre fichier **AndroidManifest.xml** afin d'associer votre domaine à votre application. Remplacez `www.webviewgold.com` par votre domaine réel (par exemple `www.example.org`) :

![AndroidManifest.xml pour la configuration des App Links](../../assets/android/img/applinks1.webp)

## Étape 2 : Activer le deep linking dans Config.java

Dans votre fichier **Config.java**, activez les fonctionnalités de deep linking :

```java
// Enables standard deep linking (https:// links)
public static final boolean IS_DEEP_LINKING_ENABLED = true;

// Enables custom scheme deep linking (e.g., webviewgold://)
public static final boolean IS_CUSTOM_SCHEME_ENABLED = true;

// Set your desired scheme prefix (must match AndroidManifest.xml)
public static final String CUSTOM_DEEPLINK_SCHEME = "webviewgold";
```

![Config.java pour la configuration des App Links](../../assets/android/img/applinks2.webp)

## Étape 3 : Vérifier la propriété du domaine (pour les deep links basés sur une URL)

Pour activer le deep linking à l'aide d'URL HTTPS, vous devez vérifier la propriété du domaine auprès de Google. Suivez le [**guide de vérification de site Google**](https://developer.android.com/training/app-links/verify-android-applinks).

## Tester vos App Links

Vous pouvez tester les deux types de liens via Android Studio ou le terminal :

- **Avec Android Studio :** Ouvrez l'**App Links Assistant** depuis le menu **Tools** pour la simulation et le dépannage.
- **Avec le terminal ou l'invite de commande :**
  1. Exécutez la commande suivante :

     ```bash
     adb shell am start -a android.intent.action.VIEW -d "webviewgold://https://www.example.org/subpages/example2" com.webviewgold.myappname
     ```

     - Remplacez `com.webviewgold.myappname` par le nom de package réel de votre application.
     - Vous pouvez également tester avec un lien URL comme `https://www.example.org/subpages/example1`.

Une fois tout configuré, les utilisateurs peuvent ouvrir votre application directement sur n'importe quelle page spécifique à l'aide de deep links comme :

- `https://www.example.org/subpages/example1`
- `webviewgold://https://www.example.org/subpages/example2`

**Des questions ?** Contactez-nous à tout moment !

---

## Continuer la lecture

- ← Précédent : [API Lampe torche](flashlight.md)
- Suivant → : [API ShareIntent](share-intent.md)
- Même fonctionnalité sur les autres plateformes : [iOS – API Universal Links](../ios/universal-links.md)
- Langues : [🇺🇸 English](../../android/app-links.md) · [🇩🇪 Deutsch](../../de/android/app-links.md) · **🇫🇷 Français** · [🇪🇸 Español](../../es/android/app-links.md) · [🇨🇳 中文](../../zh/android/app-links.md)

> [!TIP]
> **Trop occupé ? Nous configurons votre app pour vous.** Notre équipe configure, compile & soumet votre app WebViewGold — clé en main, délai rapide, Made in Germany. [Faire configurer mon app →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_android_doc_online)
>
> **Compilez dans votre navigateur :** Pas de Mac, pas d’IDE : le **WebViewGold Cloud Builder** configure, compile & met en ligne votre app. [Découvrir Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=android_docs)
