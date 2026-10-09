---
title: "API Facebook Audience Network Ads – Documentation WebViewGold pour Android"
description: "Affichez des annonces bannière et interstitielles du Facebook Audience Network dans votre application Android WebViewGold."
lang: "fr"
product: "WebViewGold pour Android"
platform: "Android"
category: "API et fonctionnalités"
slug: "facebook-ads"
canonical_url: "https://www.webviewgold.com/fr/docs/android/facebook-ads/"
keywords:
  - "API Facebook Ads"
  - "WebViewGold pour Android"
  - "convertir un site web en app"
  - "documentation d’app WebView"
  - "SDK WebView Android"
  - "PWA en app"
  - "HTML en app"
  - "pont JavaScript"
last_updated: "2026-10-09"
---

# API Facebook Audience Network Ads – WebViewGold pour Android

> **Résumé :** Affichez des annonces bannière et interstitielles du Facebook Audience Network dans votre application Android WebViewGold.

[Documentation](../README.md) › [WebViewGold pour Android](README.md) › API Facebook Ads

**Plateforme :** Android · **Catégorie :** API et fonctionnalités · **Version en ligne :** [www.webviewgold.com/fr/docs/android/facebook-ads/](https://www.webviewgold.com/fr/docs/android/facebook-ads/)

---

Le Facebook Audience Network permet aux développeurs d'applications mobiles de monétiser leurs applications iOS et Android en affichant des publicités. Grâce à WebViewGold, vous pouvez facilement intégrer des publicités Facebook dans votre application Android basée sur WebView afin de générer des revenus via les clics (CPC) et les impressions (CPM).

## Étape 1 : Ouvrir le fichier Config.java

- Pour commencer, ouvrez le fichier **Config.java** de votre application pour configurer les paramètres de l'Audience Network.

## Étape 2 : Activer les publicités Facebook Audience Network

1. **Activez les variables de configuration nécessaires :**
   - Réglez les variables suivantes sur `true` dans Config.java :
     - `USE_FACEBOOK_ADS` configure l'application pour utiliser les publicités Facebook Audience Network au lieu des publicités AdMob.
     - `SHOW_BANNER_AD` active les publicités bannière pour votre application.
     - `SHOW_FULLSCREEN_AD` active les publicités interstitielles plein écran pour votre application.
   - Réglez `SHOW_AD_AFTER_X` sur le nombre souhaité de clics sur le site web pour afficher une publicité interstitielle.

2. **Saisissez vos identifiants publicitaires Facebook :**
   - Rendez-vous dans `strings.xml` et ajoutez vos identifiants publicitaires Facebook uniques dans les champs correspondants.

Après avoir configuré les paramètres ci-dessus et confirmé vos identifiants publicitaires, votre application est prête à être lancée avec les publicités Facebook Audience Network activées.

Pour plus de détails, vous pouvez également consulter la [documentation officielle du Facebook Audience Network](https://developers.facebook.com/docs/audience-network) pour toute configuration supplémentaire ou astuce d'optimisation spécifique à votre stratégie publicitaire.

[![Regarder la vidéo: API Facebook Audience Network Ads](https://img.youtube.com/vi/81wCzuFttic/hqdefault.jpg)](https://www.youtube.com/watch?v=81wCzuFttic)

Vous pouvez également contrôler **dynamiquement** la visibilité des publicités pour un utilisateur en appelant les schémas d'URL personnalisés suivants depuis votre site web ou votre application :

- `enableads://` – Réactive l'affichage des publicités pour l'utilisateur actuel
- `disableads://` – Désactive définitivement les publicités pour l'utilisateur actuel

```html
<a href="enableads://">Enable Ads</a>
<a href="disableads://">Disable Ads</a>
```

---

## Continuer la lecture

- ← Précédent : [API AdMob](admob.md)
- Suivant → : [API de téléchargement de fichiers](file-downloader.md)
- Même fonctionnalité sur les autres plateformes : [iOS – API Facebook Ads](../ios/facebook-ads.md)
- Langues : [🇺🇸 English](../../android/facebook-ads.md) · [🇩🇪 Deutsch](../../de/android/facebook-ads.md) · **🇫🇷 Français** · [🇪🇸 Español](../../es/android/facebook-ads.md) · [🇨🇳 中文](../../zh/android/facebook-ads.md)

> [!TIP]
> **Trop occupé ? Nous configurons votre app pour vous.** Notre équipe configure, compile & soumet votre app WebViewGold — clé en main, délai rapide, Made in Germany. [Faire configurer mon app →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_android_doc_online)
>
> **Compilez dans votre navigateur :** Pas de Mac, pas d’IDE : le **WebViewGold Cloud Builder** configure, compile & met en ligne votre app. [Découvrir Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=android_docs)
