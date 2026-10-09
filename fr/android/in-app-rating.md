---
title: "API de dialogue de notation In-App – Documentation WebViewGold pour Android"
description: "Demandez un avis Google Play à vos utilisateurs : déclenchez le dialogue natif « Noter cette app » via rateapp:// depuis votre web app ou laissez WebViewGold le proposer automatiquement."
lang: "fr"
product: "WebViewGold pour Android"
platform: "Android"
category: "API et fonctionnalités"
slug: "in-app-rating"
canonical_url: "https://www.webviewgold.com/fr/docs/android/in-app-rating/"
keywords:
  - "API de notation In-App"
  - "WebViewGold pour Android"
  - "convertir un site web en app"
  - "documentation d’app WebView"
  - "SDK WebView Android"
  - "PWA en app"
  - "HTML en app"
  - "pont JavaScript"
last_updated: "2026-10-09"
---

# API de dialogue de notation In-App – WebViewGold pour Android

> **Résumé :** Demandez un avis Google Play à vos utilisateurs : déclenchez le dialogue natif « Noter cette app » via rateapp:// depuis votre web app ou laissez WebViewGold le proposer automatiquement.

[Documentation](../README.md) › [WebViewGold pour Android](README.md) › API de notation In-App

**Plateforme :** Android · **Catégorie :** API et fonctionnalités · **Version en ligne :** [www.webviewgold.com/fr/docs/android/in-app-rating/](https://www.webviewgold.com/fr/docs/android/in-app-rating/)

---

Les avis positifs sur Google Play sont l'un des leviers de croissance les plus puissants pour votre application. L'**API de dialogue de notation In-App** de WebViewGold vous permet de demander une note à vos utilisateurs au moment idéal — par exemple juste après un achat réussi ou après qu'ils ont accompli une tâche dans votre web app.

## Option 1 : Déclencher manuellement le dialogue de notation depuis votre web app

Appelez l'URL suivante depuis un lien HTML ou depuis JavaScript pour afficher un dialogue natif « Noter cette app » :

```html
<a href="rateapp://">Vous aimez l'app ? Notez-nous !</a>
```

```javascript
window.location.href = "rateapp://";
```

Si l'utilisateur confirme le dialogue, la page Google Play de votre application s'ouvre pour qu'il puisse laisser un avis. Pour que cela fonctionne, définissez `RATE_MY_APP_URL` dans **Config.java** avec l'URL Google Play de votre application :

```java
public static final String RATE_MY_APP_URL = "https://play.google.com/store/apps/details?id=com.yourcompany.yourapp";
```

**Remarque :** Si `RATE_MY_APP_URL` est vide, les appels à `rateapp://` sont ignorés. Le titre et le message du dialogue peuvent être personnalisés via les entrées `rate_title` et `rate_message` dans **strings.xml**.

## Option 2 : Laisser WebViewGold demander automatiquement

WebViewGold peut également afficher automatiquement l'invite « Noter cette app » après que l'utilisateur a utilisé votre application pendant un certain temps. Configurez ce comportement dans **Config.java** :

- `SHOW_RATE_DIALOG` — définissez-le sur `true` pour activer l'invite de notation automatique (ou sur `false` pour la désactiver).
- `RATE_DAYS_UNTIL_PROMPT` — nombre minimum de jours après l'installation avant l'affichage de l'invite.
- `RATE_LAUNCHES_UNTIL_PROMPT` — nombre minimum de lancements de l'application avant l'affichage de l'invite.

## Cas d'usage typiques

- Demander un avis juste après une interaction positive (commande finalisée, passage de niveau, réservation réussie).
- Afficher d'abord votre propre parcours « Aimez-vous l'app ? » sur votre site web et n'envoyer que les utilisateurs satisfaits vers `rateapp://`.

---

## Continuer la lecture

- ← Précédent : [API de dialogue de partage](app-sharing-dialog.md)
- Suivant → : [API d'achats intégrés](in-app-purchases.md)
- Même fonctionnalité sur les autres plateformes : [iOS – API de notation In-App](../ios/in-app-rating.md)
- Langues : [🇺🇸 English](../../android/in-app-rating.md) · [🇩🇪 Deutsch](../../de/android/in-app-rating.md) · **🇫🇷 Français** · [🇪🇸 Español](../../es/android/in-app-rating.md) · [🇨🇳 中文](../../zh/android/in-app-rating.md)

> [!TIP]
> **Trop occupé ? Nous configurons votre app pour vous.** Notre équipe configure, compile & soumet votre app WebViewGold — clé en main, délai rapide, Made in Germany. [Faire configurer mon app →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_android_doc_online)
>
> **Compilez dans votre navigateur :** Pas de Mac, pas d’IDE : le **WebViewGold Cloud Builder** configure, compile & met en ligne votre app. [Découvrir Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=android_docs)
