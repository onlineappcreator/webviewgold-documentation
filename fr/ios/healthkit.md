---
title: "Plugin HealthKit – Documentation WebViewGold pour iOS"
description: "Connectez votre application web à Apple HealthKit et lisez les données de santé avec l'autorisation de l'utilisateur sur iOS."
lang: "fr"
product: "WebViewGold pour iOS"
platform: "iOS"
category: "Extensions et plugins"
slug: "healthkit"
canonical_url: "https://www.webviewgold.com/fr/docs/iOS/healthkit/"
keywords:
  - "Plugin HealthKit"
  - "WebViewGold pour iOS"
  - "convertir un site web en app"
  - "documentation d’app WebView"
  - "SDK WebView iOS"
  - "PWA en app"
  - "HTML en app"
  - "pont JavaScript"
last_updated: "2026-10-09"
---

# Plugin HealthKit – WebViewGold pour iOS

> **Résumé :** Connectez votre application web à Apple HealthKit et lisez les données de santé avec l'autorisation de l'utilisateur sur iOS.

[Documentation](../README.md) › [WebViewGold pour iOS](README.md) › Plugin HealthKit

**Plateforme :** iOS · **Catégorie :** Extensions et plugins · **Version en ligne :** [www.webviewgold.com/fr/docs/iOS/healthkit/](https://www.webviewgold.com/fr/docs/iOS/healthkit/)

---

Activez les fonctionnalités HealthKit en réglant `static let HealthKitEnabled` dans `Config.swift` sur votre jeton de plugin et en ajoutant la capacité HealthKit.\
Contactez [webviewgold-healthkit@onlineappcreator.com](mailto:webviewgold-healthkit@onlineappcreator.com) pour plus de détails.

## Utilisation de l'API (une fois activée)

**Lisez** une valeur HealthKit en appelant `readhealthkit://` suivi d'un [identifiant HealthKit](https://developer.apple.com/documentation/healthkit/hkquantitytypeidentifier). Le résultat est injecté dans votre application web sous la forme d'une variable JavaScript portant le nom de l'identifiant (valeur et unité sous forme de chaîne) :

```html
<a href="readhealthkit://HKQuantityTypeIdentifierStepCount" onclick="setTimeout(function(){ alert(HKQuantityTypeIdentifierStepCount); }, 500)">Lire le nombre de pas</a>
```

**Écrivez** une valeur HealthKit avec la syntaxe `writehealthkit://Identifiant//Valeur` :

```html
<a href="writehealthkit://HKQuantityTypeIdentifierStepCount//100">Enregistrer 100 pas</a>
```

**Remarque :** nécessite la capacité HealthKit ainsi que les entrées *Privacy - Health Share Usage Description* / *Privacy - Health Update Usage Description* dans **Info.plist**.

---

## Continuer la lecture

- ← Précédent : [Plugin Siri](siri.md)
- Suivant → : [Compiler et publier](publish.md)
- Même fonctionnalité sur les autres plateformes : [Android – Health Connect API](../android/health-connect.md)
- Langues : [🇺🇸 English](../../ios/healthkit.md) · [🇩🇪 Deutsch](../../de/ios/healthkit.md) · **🇫🇷 Français** · [🇪🇸 Español](../../es/ios/healthkit.md) · [🇨🇳 中文](../../zh/ios/healthkit.md)

> [!TIP]
> **Trop occupé ? Nous configurons votre app pour vous.** Notre équipe configure, compile & soumet votre app WebViewGold — clé en main, délai rapide, Made in Germany. [Faire configurer mon app →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **Compilez dans votre navigateur :** Pas de Mac, pas d’IDE : le **WebViewGold Cloud Builder** configure, compile & met en ligne votre app. [Découvrir Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
