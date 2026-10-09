---
title: "API Presse-papiers – Documentation WebViewGold pour iOS"
description: "Copiez du texte dans le presse-papiers iOS et lisez le contenu du presse-papiers depuis votre application web via JavaScript."
lang: "fr"
product: "WebViewGold pour iOS"
platform: "iOS"
category: "API et fonctionnalités"
slug: "clipboard"
canonical_url: "https://www.webviewgold.com/fr/docs/iOS/clipboard/"
keywords:
  - "API Presse-papiers"
  - "WebViewGold pour iOS"
  - "convertir un site web en app"
  - "documentation d’app WebView"
  - "SDK WebView iOS"
  - "PWA en app"
  - "HTML en app"
  - "pont JavaScript"
last_updated: "2026-10-09"
---

# API Presse-papiers – WebViewGold pour iOS

> **Résumé :** Copiez du texte dans le presse-papiers iOS et lisez le contenu du presse-papiers depuis votre application web via JavaScript.

[Documentation](../README.md) › [WebViewGold pour iOS](README.md) › API Presse-papiers

**Plateforme :** iOS · **Catégorie :** API et fonctionnalités · **Version en ligne :** [www.webviewgold.com/fr/docs/iOS/clipboard/](https://www.webviewgold.com/fr/docs/iOS/clipboard/)

---

Appelez `getclipboard://` pour injecter le contenu actuel du presse-papiers dans la variable JavaScript `clipboarddata`.

```html
<a href="getclipboard://">Lire le presse-papiers</a>
<script>
function showClipboard() {
    console.log(clipboarddata);
}
</script>
```

---

## Continuer la lecture

- ← Précédent : [API Shortcut](shortcut.md)
- Suivant → : [API de lecture/écriture de valeur](read-write-value.md)
- Même fonctionnalité sur les autres plateformes : [Android – API Presse-papiers](../android/clipboard.md)
- Langues : [🇺🇸 English](../../ios/clipboard.md) · [🇩🇪 Deutsch](../../de/ios/clipboard.md) · **🇫🇷 Français** · [🇪🇸 Español](../../es/ios/clipboard.md) · [🇨🇳 中文](../../zh/ios/clipboard.md)

> [!TIP]
> **Trop occupé ? Nous configurons votre app pour vous.** Notre équipe configure, compile & soumet votre app WebViewGold — clé en main, délai rapide, Made in Germany. [Faire configurer mon app →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **Compilez dans votre navigateur :** Pas de Mac, pas d’IDE : le **WebViewGold Cloud Builder** configure, compile & met en ligne votre app. [Découvrir Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
