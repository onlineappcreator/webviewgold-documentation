---
title: "Health Connect API – Documentation WebViewGold pour Android"
description: "Read and write Android Health Connect records from JavaScript — mirrors the WebViewGold HealthKit API on iOS so one web app covers both platforms."
lang: "fr"
product: "WebViewGold pour Android"
platform: "Android"
category: "API et fonctionnalités"
slug: "health-connect"
canonical_url: "https://www.webviewgold.com/fr/docs/android/health-connect/"
keywords:
  - "Health Connect API"
  - "WebViewGold pour Android"
  - "convertir un site web en app"
  - "documentation d’app WebView"
  - "SDK WebView Android"
  - "PWA en app"
  - "HTML en app"
  - "pont JavaScript"
last_updated: "2026-10-09"
---

# Health Connect API – WebViewGold pour Android

> **Résumé :** Read and write Android Health Connect records from JavaScript — mirrors the WebViewGold HealthKit API on iOS so one web app covers both platforms.

[Documentation](../README.md) › [WebViewGold pour Android](README.md) › Health Connect API

**Plateforme :** Android · **Catégorie :** API et fonctionnalités · **Version en ligne :** [www.webviewgold.com/fr/docs/android/health-connect/](https://www.webviewgold.com/fr/docs/android/health-connect/)

---

L'**API Health Connect** lit et écrit des données de santé via [Android Health Connect](https://health.google/health-connect-android/). Elle reflète la fonctionnalité iOS HealthKit de WebViewGold, de sorte que vous puissiez livrer une seule application web qui communique avec les données de santé sur les deux plateformes. Les lectures renvoient toujours les **totaux du jour** pour le type d'enregistrement demandé.

## Lire un enregistrement

```html
<a href="readhealthkit://StepsRecord" onclick="setTimeout(show, 300)">
  My steps today
</a>

<script>
function show() {
  // Injected variable name matches the sanitized record name.
  alert(StepsRecord); // e.g. "8421.0 steps"
}
</script>
```

## Écrire un enregistrement

Format : `writehealthkit://<RecordName>//<value>`

```html
<a href="writehealthkit://StepsRecord//1000">Log 1000 steps</a>
```

En cas de succès, l'application injecte `<RecordName> = "WRITE_SUCCESS"`. En cas d'échec, elle injecte le texte de l'erreur.

**Enregistrements pris en charge :** Tout type d'enregistrement Health Connect pour lequel votre application a demandé la permission. Les plus courants sont :

- `StepsRecord`
- `HeartRateRecord`
- `WeightRecord`
- `SleepSessionRecord`
- `HydrationRecord`
- `ActiveCaloriesBurnedRecord`
- `DistanceRecord`

## Configuration

1. Installez **Health Connect** sur l'appareil (préinstallé sur Android 14+).
2. Lors de la première utilisation, l'application ouvre la boîte de dialogue des permissions Health Connect ; l'utilisateur accorde l'autorisation de lecture et/ou d'écriture pour les types d'enregistrement demandés.
3. Si Health Connect n'est pas pris en charge, la valeur injectée est remplacée par la chaîne `"Health Connect not supported"`.

**Remarques :** Les valeurs sont renvoyées sous la forme `"<nombre> <unité>"` (p. ex. `"75.4 kg"`). Nécessite Android 8.0 (API 26) ou supérieur.

---

## Continuer la lecture

- ← Précédent : [Printer API](printer.md)
- Suivant → : [Firebase Crashlytics](crashlytics.md)
- Même fonctionnalité sur les autres plateformes : [iOS – Plugin HealthKit](../ios/healthkit.md)
- Langues : [🇺🇸 English](../../android/health-connect.md) · [🇩🇪 Deutsch](../../de/android/health-connect.md) · **🇫🇷 Français** · [🇪🇸 Español](../../es/android/health-connect.md) · [🇨🇳 中文](../../zh/android/health-connect.md)

> [!TIP]
> **Trop occupé ? Nous configurons votre app pour vous.** Notre équipe configure, compile & soumet votre app WebViewGold — clé en main, délai rapide, Made in Germany. [Faire configurer mon app →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_android_doc_online)
>
> **Compilez dans votre navigateur :** Pas de Mac, pas d’IDE : le **WebViewGold Cloud Builder** configure, compile & met en ligne votre app. [Découvrir Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=android_docs)
