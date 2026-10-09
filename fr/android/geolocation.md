---
title: "API de géolocalisation HTML5 – Documentation WebViewGold pour Android"
description: "Activez la géolocalisation HTML5 dans votre application Android WebView et demandez correctement les autorisations de localisation."
lang: "fr"
product: "WebViewGold pour Android"
platform: "Android"
category: "API et fonctionnalités"
slug: "geolocation"
canonical_url: "https://www.webviewgold.com/fr/docs/android/geolocation/"
keywords:
  - "API de géolocalisation"
  - "WebViewGold pour Android"
  - "convertir un site web en app"
  - "documentation d’app WebView"
  - "SDK WebView Android"
  - "PWA en app"
  - "HTML en app"
  - "pont JavaScript"
last_updated: "2026-10-09"
---

# API de géolocalisation HTML5 – WebViewGold pour Android

> **Résumé :** Activez la géolocalisation HTML5 dans votre application Android WebView et demandez correctement les autorisations de localisation.

[Documentation](../README.md) › [WebViewGold pour Android](README.md) › API de géolocalisation

**Plateforme :** Android · **Catégorie :** API et fonctionnalités · **Version en ligne :** [www.webviewgold.com/fr/docs/android/geolocation/](https://www.webviewgold.com/fr/docs/android/geolocation/)

---

L'API de géolocalisation HTML5 permet aux utilisateurs de partager leur position avec votre application, améliorant ainsi les fonctionnalités telles que le contenu géolocalisé. Dans WebViewGold, l'API de géolocalisation est prise en charge par défaut une fois intégrée à votre contenu web. Voici comment implémenter le suivi de géolocalisation dans votre application Android basée sur WebView :

## Configuration de la géolocalisation HTML5

Pour la configuration de base de la géolocalisation, consultez le [guide de géolocalisation de Mozilla](https://developer.mozilla.org/en-US/docs/Web/API/Geolocation_API) pour plus de détails sur la mise en œuvre de cette fonctionnalité dans votre site web ou application web.

Pour une démonstration, consultez cette [démo de géolocalisation W3Schools](https://www.w3schools.com/html/html5_geolocation.asp).

## Activer le suivi de localisation en arrière-plan (Android uniquement)

Pour activer le suivi de localisation en arrière-plan pour votre application Android basée sur WebView, suivez ces étapes :

1. Définissez les permissions dans **Config.java** :
   - Réglez `requireBackgroundLocation` sur `true` si le suivi de localisation en arrière-plan est nécessaire.
   - Assurez-vous que `requireLocation` est également réglé sur `true` pour activer les services de localisation.
2. Ajustez les permissions dans **AndroidManifest.xml** :
   - Décommentez les blocs de permission pour `android.permission.FOREGROUND_SERVICE_LOCATION` et `GPSService`.
   - Recherchez ces termes dans le fichier pour vous assurer que les permissions correctes sont définies.

## Activer/désactiver le suivi de localisation en arrière-plan avec des schémas d'URL

Utilisez les schémas d'URL suivants pour activer ou désactiver le suivi de localisation en arrière-plan au sein de votre application Android basée sur WebView :

Pour activer le suivi de localisation en arrière-plan, redirigez l'utilisateur vers l'URL suivante :

```html
<script>window.location.href = "backgroundlocationon://";  </script>
```

Pour désactiver le suivi de localisation en arrière-plan, redirigez l'utilisateur vers l'URL suivante :

```html
<script>window.location.href = "backgroundlocationoff://";  </script>
```

**Remarque :** Ces schémas d'URL sont spécifiques à WebViewGold pour Android et peuvent ne pas fonctionner dans les navigateurs web standard. Pour vous assurer que ces redirections ne sont appliquées qu'aux utilisateurs de l'application Android, envisagez de détecter le User-Agent.

---

## Continuer la lecture

- ← Précédent : [Multi API Call](multi-api-call.md)
- Suivant → : [API de notifications push](push-notifications.md)
- Même fonctionnalité sur les autres plateformes : [iOS – API de géolocalisation](../ios/geolocation.md)
- Langues : [🇺🇸 English](../../android/geolocation.md) · [🇩🇪 Deutsch](../../de/android/geolocation.md) · **🇫🇷 Français** · [🇪🇸 Español](../../es/android/geolocation.md) · [🇨🇳 中文](../../zh/android/geolocation.md)

> [!TIP]
> **Trop occupé ? Nous configurons votre app pour vous.** Notre équipe configure, compile & soumet votre app WebViewGold — clé en main, délai rapide, Made in Germany. [Faire configurer mon app →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_android_doc_online)
>
> **Compilez dans votre navigateur :** Pas de Mac, pas d’IDE : le **WebViewGold Cloud Builder** configure, compile & met en ligne votre app. [Découvrir Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=android_docs)
