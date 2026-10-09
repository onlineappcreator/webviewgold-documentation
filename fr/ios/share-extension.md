---
title: "Share Extension – Documentation WebViewGold pour iOS"
description: "Permettez aux utilisateurs de partager du contenu d'autres apps directement dans votre application WebView iOS grâce à une Share Extension."
lang: "fr"
product: "WebViewGold pour iOS"
platform: "iOS"
category: "Extensions et plugins"
slug: "share-extension"
canonical_url: "https://www.webviewgold.com/fr/docs/iOS/share-extension/"
keywords:
  - "Share Extension"
  - "WebViewGold pour iOS"
  - "convertir un site web en app"
  - "documentation d’app WebView"
  - "SDK WebView iOS"
  - "PWA en app"
  - "HTML en app"
  - "pont JavaScript"
last_updated: "2026-10-09"
---

# Share Extension – WebViewGold pour iOS

> **Résumé :** Permettez aux utilisateurs de partager du contenu d'autres apps directement dans votre application WebView iOS grâce à une Share Extension.

[Documentation](../README.md) › [WebViewGold pour iOS](README.md) › Share Extension

**Plateforme :** iOS · **Catégorie :** Extensions et plugins · **Version en ligne :** [www.webviewgold.com/fr/docs/iOS/share-extension/](https://www.webviewgold.com/fr/docs/iOS/share-extension/)

---

Lorsque les utilisateurs partagent du texte ou des images vers votre application depuis des applications telles que Photos ou Safari, les données deviennent disponibles dans la variable JavaScript `sharedData`. Les images partagées sont fournies sous forme de chaînes Base64.

```html
<script>
if (typeof sharedData !== 'undefined') {
    console.log(sharedData);
}
</script>
```

---

## Continuer la lecture

- ← Précédent : [API d'ouverture des réglages](open-app-settings.md)
- Suivant → : [Widget Extension](widget-extension.md)
- Même fonctionnalité sur les autres plateformes : [Android – API ShareIntent](../android/share-intent.md)
- Langues : [🇺🇸 English](../../ios/share-extension.md) · [🇩🇪 Deutsch](../../de/ios/share-extension.md) · **🇫🇷 Français** · [🇪🇸 Español](../../es/ios/share-extension.md) · [🇨🇳 中文](../../zh/ios/share-extension.md)

> [!TIP]
> **Trop occupé ? Nous configurons votre app pour vous.** Notre équipe configure, compile & soumet votre app WebViewGold — clé en main, délai rapide, Made in Germany. [Faire configurer mon app →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **Compilez dans votre navigateur :** Pas de Mac, pas d’IDE : le **WebViewGold Cloud Builder** configure, compile & met en ligne votre app. [Découvrir Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
