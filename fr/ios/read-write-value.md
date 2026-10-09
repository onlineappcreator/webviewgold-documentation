---
title: "API de lecture/écriture de valeur – Documentation WebViewGold pour iOS"
description: "Stockez durablement une valeur de chaîne sur l'appareil et relisez-la dans le JavaScript de votre application web."
lang: "fr"
product: "WebViewGold pour iOS"
platform: "iOS"
category: "API et fonctionnalités"
slug: "read-write-value"
canonical_url: "https://www.webviewgold.com/fr/docs/iOS/read-write-value/"
keywords:
  - "API de lecture/écriture de valeur"
  - "WebViewGold pour iOS"
  - "convertir un site web en app"
  - "documentation d’app WebView"
  - "SDK WebView iOS"
  - "PWA en app"
  - "HTML en app"
  - "pont JavaScript"
last_updated: "2026-10-09"
---

# API de lecture/écriture de valeur – WebViewGold pour iOS

> **Résumé :** Stockez durablement une valeur de chaîne sur l'appareil et relisez-la dans le JavaScript de votre application web.

[Documentation](../README.md) › [WebViewGold pour iOS](README.md) › API de lecture/écriture de valeur

**Plateforme :** iOS · **Catégorie :** API et fonctionnalités · **Version en ligne :** [www.webviewgold.com/fr/docs/iOS/read-write-value/](https://www.webviewgold.com/fr/docs/iOS/read-write-value/)

---

L'**API de lecture/écriture de valeur** stocke de manière persistante une chaîne arbitraire sur l'appareil (dans le stockage privé de l'application) et la relit dans votre JavaScript. Les valeurs survivent aux redémarrages de l'application et aux vidages de cache — tant que l'application n'est pas désinstallée.

## Écrire une valeur

Tout ce qui suit `writevalue://` est stocké tel quel sous forme d'une seule chaîne. Définissez votre propre format (query-string, JSON, CSV — ce qui convient à votre application web) :

```html
<a href="writevalue://darkmode=on;user=42">Enregistrer</a>
```

## Lire une valeur

Lorsque `readvalue://` est déclenché, l'application réinjecte la chaîne stockée dans la WebView sous la forme de `window.storedValues` afin que votre JavaScript puisse la lire :

```html
<a href="readvalue://" onclick="setTimeout(showSettings, 200)">Charger</a>
<script>
  function showSettings() {
    console.log(window.storedValues || "aucun réglage pour le moment");
  }
</script>
```

## Cas d'utilisation typiques

- Mémoriser hors ligne le thème, la langue ou l'état d'onboarding d'un utilisateur.
- Mettre en cache un jeton de session lorsque vous ne pouvez pas compter sur les cookies.
- Conserver une petite préférence locale sans aller-retour avec le backend.

**Remarques :** les valeurs sont propres à chaque installation de l'application et à chaque appareil — elles ne sont **pas** synchronisées entre appareils. Gardez des valeurs de petite taille ; cette API est destinée aux réglages, pas au stockage de blobs.

---

## Continuer la lecture

- ← Précédent : [API Presse-papiers](clipboard.md)
- Suivant → : [API d'ouverture des réglages](open-app-settings.md)
- Même fonctionnalité sur les autres plateformes : [Android – Read/Write Value API](../android/read-write-value.md)
- Langues : [🇺🇸 English](../../ios/read-write-value.md) · [🇩🇪 Deutsch](../../de/ios/read-write-value.md) · **🇫🇷 Français** · [🇪🇸 Español](../../es/ios/read-write-value.md) · [🇨🇳 中文](../../zh/ios/read-write-value.md)

> [!TIP]
> **Trop occupé ? Nous configurons votre app pour vous.** Notre équipe configure, compile & soumet votre app WebViewGold — clé en main, délai rapide, Made in Germany. [Faire configurer mon app →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **Compilez dans votre navigateur :** Pas de Mac, pas d’IDE : le **WebViewGold Cloud Builder** configure, compile & met en ligne votre app. [Découvrir Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
