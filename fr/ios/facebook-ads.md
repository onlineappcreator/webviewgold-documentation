---
title: "API Facebook Audience Network Ads – Documentation WebViewGold pour iOS"
description: "Affichez des publicités bannière et interstitielles Facebook Audience Network dans votre application WebViewGold iOS."
lang: "fr"
product: "WebViewGold pour iOS"
platform: "iOS"
category: "API et fonctionnalités"
slug: "facebook-ads"
canonical_url: "https://www.webviewgold.com/fr/docs/iOS/facebook-ads/"
keywords:
  - "API Facebook Ads"
  - "WebViewGold pour iOS"
  - "convertir un site web en app"
  - "documentation d’app WebView"
  - "SDK WebView iOS"
  - "PWA en app"
  - "HTML en app"
  - "pont JavaScript"
last_updated: "2026-10-09"
---

# API Facebook Audience Network Ads – WebViewGold pour iOS

> **Résumé :** Affichez des publicités bannière et interstitielles Facebook Audience Network dans votre application WebViewGold iOS.

[Documentation](../README.md) › [WebViewGold pour iOS](README.md) › API Facebook Ads

**Plateforme :** iOS · **Catégorie :** API et fonctionnalités · **Version en ligne :** [www.webviewgold.com/fr/docs/iOS/facebook-ads/](https://www.webviewgold.com/fr/docs/iOS/facebook-ads/)

---

Le [Facebook Audience Network](https://www.facebook.com/audiencenetwork/) permet aux développeurs d'applications mobiles de monétiser leurs applications iOS et Android en affichant des annonces. Grâce à WebViewGold, vous pouvez facilement intégrer des annonces Facebook dans vos applications iOS basées sur WebView afin de générer des revenus grâce aux clics (CPC) et aux impressions (CPM).

## Étape 1 : créez un compte Facebook Audience Network

Vous devez créer un compte [Facebook Audience Network](https://www.facebook.com/audiencenetwork/) et créer une propriété dans la section Integration du Monetization Manager. Vous devez ensuite connecter une application iOS (vous n'avez toutefois pas besoin d'associer une application iOS publiée à des fins de test).

Suivez ce guide pour référence : <https://www.facebook.com/business/help/191133327919314>

## Étape 2 : définissez les variables de configuration nécessaires

- Ouvrez **Config.swift** et réglez `useFacebookAds` sur `true`.
- Saisissez votre identifiant d'emplacement Facebook (Placement ID) dans `facebookAdsID`.

![Capture d'écran de la configuration de Facebook Ads](../../assets/ios/img/fbadsconfig.webp)

## Étape 3 : configurez les paramètres des annonces

- Pour utiliser des annonces programmées, réglez `useTimedAds` sur `true` et définissez `showFBAdsEveryNSeconds` sur l'intervalle de temps souhaité entre les annonces.
- Vous pouvez ajouter des mots-déclencheurs d'URL à `fbadstriggerurls` pour initialiser les annonces à la demande.

## Autres considérations

- Un appareil iOS réel doit être utilisé pour les tests (et non un simulateur)
- L'appareil doit être ajouté comme appareil de test, voir <https://developers.facebook.com/docs/audience-network/setting-up/testing/platform>
- Facebook doit être installé et connecté sur l'appareil
- L'option “Limit Ad Tracking” ou tout paramètre similaire susceptible d'être introduit dans les futures versions d'iOS doit être désactivée.

---

## Continuer la lecture

- ← Précédent : [API AdMob Ads](admob.md)
- Suivant → : [API audio HTML](html-audio.md)
- Même fonctionnalité sur les autres plateformes : [Android – API Facebook Ads](../android/facebook-ads.md)
- Langues : [🇺🇸 English](../../ios/facebook-ads.md) · [🇩🇪 Deutsch](../../de/ios/facebook-ads.md) · **🇫🇷 Français** · [🇪🇸 Español](../../es/ios/facebook-ads.md) · [🇨🇳 中文](../../zh/ios/facebook-ads.md)

> [!TIP]
> **Trop occupé ? Nous configurons votre app pour vous.** Notre équipe configure, compile & soumet votre app WebViewGold — clé en main, délai rapide, Made in Germany. [Faire configurer mon app →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **Compilez dans votre navigateur :** Pas de Mac, pas d’IDE : le **WebViewGold Cloud Builder** configure, compile & met en ligne votre app. [Découvrir Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
