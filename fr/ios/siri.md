---
title: "Plugin Siri – Documentation WebViewGold pour iOS"
description: "Ajoutez la prise en charge des raccourcis Siri à votre application WebView iOS et ouvrez le contenu de l'app à la voix."
lang: "fr"
product: "WebViewGold pour iOS"
platform: "iOS"
category: "Extensions et plugins"
slug: "siri"
canonical_url: "https://www.webviewgold.com/fr/docs/iOS/siri/"
keywords:
  - "Plugin Siri"
  - "WebViewGold pour iOS"
  - "convertir un site web en app"
  - "documentation d’app WebView"
  - "SDK WebView iOS"
  - "PWA en app"
  - "HTML en app"
  - "pont JavaScript"
last_updated: "2026-10-09"
---

# Plugin Siri – WebViewGold pour iOS

> **Résumé :** Ajoutez la prise en charge des raccourcis Siri à votre application WebView iOS et ouvrez le contenu de l'app à la voix.

[Documentation](../README.md) › [WebViewGold pour iOS](README.md) › Plugin Siri

**Plateforme :** iOS · **Catégorie :** Extensions et plugins · **Version en ligne :** [www.webviewgold.com/fr/docs/iOS/siri/](https://www.webviewgold.com/fr/docs/iOS/siri/)

---

Activez l'intégration Siri en saisissant votre jeton de plugin dans `static let siriEnabled` dans `Config.swift` et en ajoutant la capability Siri à la cible WebViewGold.\
Contactez [webviewgold-siri@onlineappcreator.com](mailto:webviewgold-siri@onlineappcreator.com) pour plus d'informations.

## Comment implémenter la fonctionnalité Siri

1. Créez une fonction JavaScript que Siri doit déclencher :

```javascript
function playRadio() {
   // Ajouter la fonctionnalité souhaitée
}
```

2. Ajoutez un bouton ou un lien pour enregistrer la commande Siri (évitez les expressions telles que « Ouvrir » qui pourraient perturber Siri) :

```html
<a href="addtosiri://?command=Play%20Radio&jsFunction=playRadio()">Ajouter Play Radio à Siri</a>
```

Le paramètre `command` fournit l'expression recommandée, tandis que `jsFunction` spécifie la fonction JavaScript à exécuter.

---

## Continuer la lecture

- ← Précédent : [Plugin NFC](nfc.md)
- Suivant → : [Plugin HealthKit](healthkit.md)
- Langues : [🇺🇸 English](../../ios/siri.md) · [🇩🇪 Deutsch](../../de/ios/siri.md) · **🇫🇷 Français** · [🇪🇸 Español](../../es/ios/siri.md) · [🇨🇳 中文](../../zh/ios/siri.md)

> [!TIP]
> **Trop occupé ? Nous configurons votre app pour vous.** Notre équipe configure, compile & soumet votre app WebViewGold — clé en main, délai rapide, Made in Germany. [Faire configurer mon app →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **Compilez dans votre navigateur :** Pas de Mac, pas d’IDE : le **WebViewGold Cloud Builder** configure, compile & met en ligne votre app. [Découvrir Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
