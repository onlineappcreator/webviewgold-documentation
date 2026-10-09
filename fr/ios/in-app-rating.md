---
title: "API de boîte de dialogue de notation In-App – Documentation WebViewGold pour iOS"
description: "Demandez une note App Store à vos utilisateurs au moment idéal — déclenchez la boîte de dialogue de notation native d'iOS depuis votre application web."
lang: "fr"
product: "WebViewGold pour iOS"
platform: "iOS"
category: "API et fonctionnalités"
slug: "in-app-rating"
canonical_url: "https://www.webviewgold.com/fr/docs/iOS/in-app-rating/"
keywords:
  - "API de notation In-App"
  - "WebViewGold pour iOS"
  - "convertir un site web en app"
  - "documentation d’app WebView"
  - "SDK WebView iOS"
  - "PWA en app"
  - "HTML en app"
  - "pont JavaScript"
last_updated: "2026-10-09"
---

# API de boîte de dialogue de notation In-App – WebViewGold pour iOS

> **Résumé :** Demandez une note App Store à vos utilisateurs au moment idéal — déclenchez la boîte de dialogue de notation native d'iOS depuis votre application web.

[Documentation](../README.md) › [WebViewGold pour iOS](README.md) › API de notation In-App

**Plateforme :** iOS · **Catégorie :** API et fonctionnalités · **Version en ligne :** [www.webviewgold.com/fr/docs/iOS/in-app-rating/](https://www.webviewgold.com/fr/docs/iOS/in-app-rating/)

---

Les avis positifs sur l'App Store sont l'un des leviers de croissance les plus puissants pour votre application. L'**API de boîte de dialogue de notation In-App** de WebViewGold vous permet de demander une note à vos utilisateurs exactement au bon moment — par exemple juste après un achat réussi ou après qu'ils ont accompli une tâche dans votre application web.

## Option 1 : boîte de dialogue de notation native iOS (par défaut)

Appelez l'URL suivante depuis un lien HTML ou depuis JavaScript pour afficher la boîte de dialogue de notation native **SKStoreReviewController** :

```html
<a href="rateapp://">Vous aimez l'app ? Notez-nous !</a>
```

```javascript
window.location.href = "rateapp://";
```

**Remarque :** Apple limite la fréquence d'affichage de la boîte de dialogue de notation native (environ trois fois par an et par utilisateur) ; elle peut donc ne pas apparaître à chaque appel — c'est voulu et cela s'applique aussi pendant le développement.

## Option 2 : boîte de dialogue de notation personnalisée

Si vous préférez une boîte de dialogue qui apparaît toujours et envoie l'utilisateur vers votre page App Store, configurez-la dans **Config.swift** :

- `showcustomrateappdialog` — définissez sur `true` pour afficher une boîte de dialogue personnalisée lors du déclenchement de `rateapp://` au lieu de tenter l'appel d'avis natif.
- `ratemyappurl` — définissez l'URL App Store de votre application, par ex. `https://apps.apple.com/app/idXXXXXXXXX?action=write-review`.

## Cas d'utilisation typiques

- Demander un avis juste après une interaction positive (commande finalisée, passage de niveau, réservation réussie).
- Afficher d'abord votre propre parcours « Aimez-vous l'app ? » sur votre site web et n'envoyer que les utilisateurs satisfaits vers `rateapp://`.

---

## Continuer la lecture

- ← Précédent : [API de partage d'app](app-sharing-dialog.md)
- Suivant → : [API d'achats intégrés](in-app-purchases.md)
- Même fonctionnalité sur les autres plateformes : [Android – API de notation In-App](../android/in-app-rating.md)
- Langues : [🇺🇸 English](../../ios/in-app-rating.md) · [🇩🇪 Deutsch](../../de/ios/in-app-rating.md) · **🇫🇷 Français** · [🇪🇸 Español](../../es/ios/in-app-rating.md) · [🇨🇳 中文](../../zh/ios/in-app-rating.md)

> [!TIP]
> **Trop occupé ? Nous configurons votre app pour vous.** Notre équipe configure, compile & soumet votre app WebViewGold — clé en main, délai rapide, Made in Germany. [Faire configurer mon app →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **Compilez dans votre navigateur :** Pas de Mac, pas d’IDE : le **WebViewGold Cloud Builder** configure, compile & met en ligne votre app. [Découvrir Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
