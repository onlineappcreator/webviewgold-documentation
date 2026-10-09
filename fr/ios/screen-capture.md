---
title: "Détection de capture d'écran – Documentation WebViewGold pour iOS"
description: "Détectez les captures et les enregistrements d'écran dans votre application iOS et réagissez depuis votre application web."
lang: "fr"
product: "WebViewGold pour iOS"
platform: "iOS"
category: "Extensions et plugins"
slug: "screen-capture"
canonical_url: "https://www.webviewgold.com/fr/docs/iOS/screen-capture/"
keywords:
  - "Détection de capture d'écran"
  - "WebViewGold pour iOS"
  - "convertir un site web en app"
  - "documentation d’app WebView"
  - "SDK WebView iOS"
  - "PWA en app"
  - "HTML en app"
  - "pont JavaScript"
last_updated: "2026-10-09"
---

# Détection de capture d'écran – WebViewGold pour iOS

> **Résumé :** Détectez les captures et les enregistrements d'écran dans votre application iOS et réagissez depuis votre application web.

[Documentation](../README.md) › [WebViewGold pour iOS](README.md) › Détection de capture d'écran

**Plateforme :** iOS · **Catégorie :** Extensions et plugins · **Version en ligne :** [www.webviewgold.com/fr/docs/iOS/screen-capture/](https://www.webviewgold.com/fr/docs/iOS/screen-capture/)

---

Définissez `let preventScreenCapture = true` dans `Config.swift` pour détecter les captures d'écran ou les enregistrements d'écran et appeler automatiquement la fonction JavaScript `onScreenCaptureAttempt`.

```html
<script>
function onScreenCaptureAttempt() {
    alert('Screen capture detected');
}
</script>
```

---

## Continuer la lecture

- ← Précédent : [Barre latérale native](sidebar.md)
- Suivant → : [Fonction MultiAPICall](multi-api-call.md)
- Langues : [🇺🇸 English](../../ios/screen-capture.md) · [🇩🇪 Deutsch](../../de/ios/screen-capture.md) · **🇫🇷 Français** · [🇪🇸 Español](../../es/ios/screen-capture.md) · [🇨🇳 中文](../../zh/ios/screen-capture.md)

> [!TIP]
> **Trop occupé ? Nous configurons votre app pour vous.** Notre équipe configure, compile & soumet votre app WebViewGold — clé en main, délai rapide, Made in Germany. [Faire configurer mon app →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **Compilez dans votre navigateur :** Pas de Mac, pas d’IDE : le **WebViewGold Cloud Builder** configure, compile & met en ligne votre app. [Découvrir Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
