---
title: "Multi API Call (multiapicall://) – Documentation WebViewGold pour Android"
description: "Appelez plusieurs APIs de données WebViewGold en une seule affectation window.location.href — idéal pour les web apps multiplateformes qui utilisent aussi la version iOS."
lang: "fr"
product: "WebViewGold pour Android"
platform: "Android"
category: "API et fonctionnalités"
slug: "multi-api-call"
canonical_url: "https://www.webviewgold.com/fr/docs/android/multi-api-call/"
keywords:
  - "Multi API Call"
  - "WebViewGold pour Android"
  - "convertir un site web en app"
  - "documentation d’app WebView"
  - "SDK WebView Android"
  - "PWA en app"
  - "HTML en app"
  - "pont JavaScript"
last_updated: "2026-10-09"
---

# Multi API Call (multiapicall://) – WebViewGold pour Android

> **Résumé :** Appelez plusieurs APIs de données WebViewGold en une seule affectation window.location.href — idéal pour les web apps multiplateformes qui utilisent aussi la version iOS.

[Documentation](../README.md) › [WebViewGold pour Android](README.md) › Multi API Call

**Plateforme :** Android · **Catégorie :** API et fonctionnalités · **Version en ligne :** [www.webviewgold.com/fr/docs/android/multi-api-call/](https://www.webviewgold.com/fr/docs/android/multi-api-call/)

---

La **fonctionnalité Multi API Call** vous permet de déclencher **plusieurs APIs WebViewGold en une seule affectation *window.location.href***. C'est particulièrement utile pour les **applications web multiplateformes** : les navigateurs basés sur Apple traitent plusieurs redirections de page dans le même script différemment d'Android — appeler *window.location.href = "exampleAPItrigger"* plusieurs fois dans le même script fonctionne sur Android, mais pas sur iOS. Avec `multiapicall://`, le même code web fonctionne sur les deux plateformes.

## APIs prises en charge comme entrées

- [get-uuid](uuid.md)
- [getonesignalplayerid](push-notifications.md)
- [getappversion](app-version-check.md)
- [statusbarcolor](dynamic-ui.md) (suivi de trois entrées pour les valeurs RGB)
- [statusbartextcolor](dynamic-ui.md) (suivi d'une entrée : `black` ou `white`)
- [bottombarcolor](dynamic-ui.md) (suivi de trois entrées pour les valeurs RGB)
- [navbartextcolor](dynamic-ui.md) (suivi d'une entrée : `black` ou `white`)

## Comment l'utiliser

Séparez les noms des APIs (et leurs valeurs, le cas échéant) par des virgules (`,`) — **sans espaces** :

```html
<script>
// Exemple de combinaison : "getonesignalplayerid" et "getappversion"
window.location.href = "multiapicall://getonesignalplayerid,getappversion";
</script>
```

Voici comment passer des valeurs aux APIs Dynamic UI :

```html
<script>
// Mettre la barre d'état en rouge, son texte en blanc et récupérer l'UUID — le tout en un seul appel
window.location.href = "multiapicall://statusbarcolor,255,0,0,statusbartextcolor,white,get-uuid";
</script>
```

**Remarque :** Sur Android, appeler les APIs individuelles l'une après l'autre fonctionne également (p. ex. `window.location.href = "get-uuid://";` suivi de `window.location.href = "getappversion://";`). Utilisez `multiapicall://` si vous souhaitez partager un même code avec la [version iOS de WebViewGold](../ios/multi-api-call.md).

Cliquez [ici](https://webviewgoldtest.github.io/multiAPI.html) pour voir une page web de démonstration de cette fonctionnalité. Inspectez la page pour consulter le code d'exemple.

---

## Continuer la lecture

- ← Précédent : [API CSS et JS personnalisés](custom-css-js.md)
- Suivant → : [API de géolocalisation](geolocation.md)
- Même fonctionnalité sur les autres plateformes : [iOS – Fonction MultiAPICall](../ios/multi-api-call.md)
- Langues : [🇺🇸 English](../../android/multi-api-call.md) · [🇩🇪 Deutsch](../../de/android/multi-api-call.md) · **🇫🇷 Français** · [🇪🇸 Español](../../es/android/multi-api-call.md) · [🇨🇳 中文](../../zh/android/multi-api-call.md)

> [!TIP]
> **Trop occupé ? Nous configurons votre app pour vous.** Notre équipe configure, compile & soumet votre app WebViewGold — clé en main, délai rapide, Made in Germany. [Faire configurer mon app →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_android_doc_online)
>
> **Compilez dans votre navigateur :** Pas de Mac, pas d’IDE : le **WebViewGold Cloud Builder** configure, compile & met en ligne votre app. [Découvrir Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=android_docs)
