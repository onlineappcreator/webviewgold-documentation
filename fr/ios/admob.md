---
title: "API AdMob Ads – Documentation WebViewGold pour iOS"
description: "Monétisez votre application iOS avec les publicités bannière, interstitielles et récompensées de Google AdMob : configuration et déclencheurs JavaScript."
lang: "fr"
product: "WebViewGold pour iOS"
platform: "iOS"
category: "API et fonctionnalités"
slug: "admob"
canonical_url: "https://www.webviewgold.com/fr/docs/iOS/admob/"
keywords:
  - "API AdMob Ads"
  - "WebViewGold pour iOS"
  - "convertir un site web en app"
  - "documentation d’app WebView"
  - "SDK WebView iOS"
  - "PWA en app"
  - "HTML en app"
  - "pont JavaScript"
last_updated: "2026-10-09"
---

# API AdMob Ads – WebViewGold pour iOS

> **Résumé :** Monétisez votre application iOS avec les publicités bannière, interstitielles et récompensées de Google AdMob : configuration et déclencheurs JavaScript.

[Documentation](../README.md) › [WebViewGold pour iOS](README.md) › API AdMob Ads

**Plateforme :** iOS · **Catégorie :** API et fonctionnalités · **Version en ligne :** [www.webviewgold.com/fr/docs/iOS/admob/](https://www.webviewgold.com/fr/docs/iOS/admob/)

---

AdMob est un service Google permettant de monétiser les applications mobiles sur les plateformes iOS et Android. Il permet aux développeurs d'intégrer des annonces bannières, interstitielles et avec récompense, rémunérées au clic (CPC, coût par clic) ou à l'impression (CPM, coût pour mille). WebViewGold simplifie l'intégration d'AdMob et permet une configuration rapide pour afficher des annonces dans votre application iOS basée sur WebView.

[![Regarder la vidéo: API AdMob Ads](https://img.youtube.com/vi/7j7NW5CTwqo/hqdefault.jpg)](https://www.youtube.com/watch?v=7j7NW5CTwqo)

**Étape 1 :** Ouvrez le fichier **Info.plist** et renseignez l'identifiant de compte global AdMob dans le champ *GADApplicationIdentifier* :\
![Ajoutez l'identifiant de votre compte AdMob au projet](../../assets/ios/img/admobglobal.webp)

**Étape 2 :** Veuillez insérer vos identifiants AdMob dans le fichier **Config.swift** pour `AdmobBannerID`, `AdmobinterstitialID` et `AdmobRewardedID` :\
![Activez des blocs de bannières AdMob spécifiques dans votre application](../../assets/ios/img/admobconstants.webp)

**Étape 3 :** Dans **Config.swift**, vous pouvez :

- **Activer ou désactiver** les annonces bannières et/ou interstitielles en réglant `showBannerAd` sur `true` pour les bannières et `showFullScreenAd` sur `true` pour les interstitielles.
- **Définir des intervalles** pour l'affichage des annonces interstitielles en modifiant `showadAfterX` pour indiquer le nombre d'interactions avec le site web souhaité avant la diffusion d'une annonce interstitielle.

**Pour activer les annonces avec récompense** *(disponibles uniquement pour les versions iOS supérieures à 13.0)* **:** Réglez `enableRewardedAds` sur `true`.

Pour diffuser une annonce avec récompense, utilisez un appel à la fonctionnalité de notre API d'annonces avec récompense.

```html
<a href="displayrewardedad://>Display Rewarded Advertisement</a>
```

Une fois le visionnage complet d'une annonce terminé, votre site web recevra un appel à une fonction JavaScript, **updateRewardedStatus('true');**. C'est à vous d'implémenter cette fonction dans votre code JavaScript, tout comme c'est à vous de décider comment vous souhaitez récompenser l'utilisateur.

WebViewGold prend en charge l'affichage des annonces avec récompense comme option publicitaire par défaut, remplaçant les options interstitielles. Pour cela, réglez `useRewardedAdsWherePossible` et `showFullScreenAd` sur `true`.

**Astuce :** si vous affichez des annonces interstitielles après X touches (`incrementWithTaps` sur `true`), vous pouvez également augmenter le compteur de touches manuellement depuis votre application web en appelant `increasetapcounter://` — utile pour ne compter que certaines interactions dans l'intervalle publicitaire.

*Pour plus d'informations, veuillez également consulter la [documentation officielle du SDK AdMob](https://developers.google.com/admob/) (mais ignorez les parties concernant la configuration, car WebViewGold inclut déjà le framework).*

---

## Continuer la lecture

- ← Précédent : [API de notifications push](push-notifications.md)
- Suivant → : [API Facebook Ads](facebook-ads.md)
- Même fonctionnalité sur les autres plateformes : [Android – API AdMob](../android/admob.md)
- Langues : [🇺🇸 English](../../ios/admob.md) · [🇩🇪 Deutsch](../../de/ios/admob.md) · **🇫🇷 Français** · [🇪🇸 Español](../../es/ios/admob.md) · [🇨🇳 中文](../../zh/ios/admob.md)

> [!TIP]
> **Trop occupé ? Nous configurons votre app pour vous.** Notre équipe configure, compile & soumet votre app WebViewGold — clé en main, délai rapide, Made in Germany. [Faire configurer mon app →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **Compilez dans votre navigateur :** Pas de Mac, pas d’IDE : le **WebViewGold Cloud Builder** configure, compile & met en ligne votre app. [Découvrir Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
