---
title: "Read/Write Value API – Documentation WebViewGold pour Android"
description: "Persist small strings on the device from JavaScript and read them back — for theme, language, session tokens, or onboarding state."
lang: "fr"
product: "WebViewGold pour Android"
platform: "Android"
category: "API et fonctionnalités"
slug: "read-write-value"
canonical_url: "https://www.webviewgold.com/fr/docs/android/read-write-value/"
keywords:
  - "Read/Write Value API"
  - "WebViewGold pour Android"
  - "convertir un site web en app"
  - "documentation d’app WebView"
  - "SDK WebView Android"
  - "PWA en app"
  - "HTML en app"
  - "pont JavaScript"
last_updated: "2026-10-09"
---

# Read/Write Value API – WebViewGold pour Android

> **Résumé :** Persist small strings on the device from JavaScript and read them back — for theme, language, session tokens, or onboarding state.

[Documentation](../README.md) › [WebViewGold pour Android](README.md) › Read/Write Value API

**Plateforme :** Android · **Catégorie :** API et fonctionnalités · **Version en ligne :** [www.webviewgold.com/fr/docs/android/read-write-value/](https://www.webviewgold.com/fr/docs/android/read-write-value/)

---

L'**API Read/Write Value** stocke de manière persistante une chaîne de caractères arbitraire sur l'appareil (via le stockage privé de l'application) et la relit dans votre JavaScript. Les valeurs persistent aux redémarrages de l'application et aux vidages du cache — sauf si le système d'exploitation efface les données de l'application.

## Écrire une valeur

Tout ce qui suit `writevalue://` est stocké tel quel sous forme d'une seule chaîne. Concevez votre propre format (chaîne de requête, JSON, CSV — ce qui convient à votre application web) :

```html
<a href="writevalue://darkmode=on;user=42">Save</a>
```

## Lire une valeur

Lorsque `readvalue://` est déclenché, l'application injecte la chaîne stockée dans la WebView afin que votre JavaScript puisse la lire :

```html
<a href="readvalue://" onclick="setTimeout(showSettings, 200)">Load</a>
<script>
  function showSettings() {
    console.log(window.appSettings || "no settings yet");
  }
</script>
```

## Cas d'usage typiques

- Mémoriser le thème, la langue ou l'état d'onboarding d'un utilisateur hors ligne.
- Mettre en cache un jeton de session lorsque vous ne pouvez pas vous appuyer sur les cookies.
- Persister une petite préférence locale sans aller-retour avec le backend.

**Remarques :** Les valeurs sont spécifiques à chaque installation d'application et à chaque appareil — elles ne sont **pas** synchronisées entre appareils. Conservez des valeurs de petite taille ; cette API est destinée aux paramètres, pas au stockage de blobs.

---

## Continuer la lecture

- ← Précédent : [Reconnect API](reconnect.md)
- Suivant → : [Biometric Auth API](biometric-auth.md)
- Même fonctionnalité sur les autres plateformes : [iOS – API de lecture/écriture de valeur](../ios/read-write-value.md)
- Langues : [🇺🇸 English](../../android/read-write-value.md) · [🇩🇪 Deutsch](../../de/android/read-write-value.md) · **🇫🇷 Français** · [🇪🇸 Español](../../es/android/read-write-value.md) · [🇨🇳 中文](../../zh/android/read-write-value.md)

> [!TIP]
> **Trop occupé ? Nous configurons votre app pour vous.** Notre équipe configure, compile & soumet votre app WebViewGold — clé en main, délai rapide, Made in Germany. [Faire configurer mon app →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_android_doc_online)
>
> **Compilez dans votre navigateur :** Pas de Mac, pas d’IDE : le **WebViewGold Cloud Builder** configure, compile & met en ligne votre app. [Découvrir Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=android_docs)
