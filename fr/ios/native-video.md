---
title: "API de lecteur vidéo natif – Documentation WebViewGold pour iOS"
description: "Lisez des flux vidéo dans le lecteur natif d'iOS avec prise en charge du mode Image dans l'image — déclenchés directement depuis votre application web."
lang: "fr"
product: "WebViewGold pour iOS"
platform: "iOS"
category: "API et fonctionnalités"
slug: "native-video"
canonical_url: "https://www.webviewgold.com/fr/docs/iOS/native-video/"
keywords:
  - "API de vidéo native"
  - "WebViewGold pour iOS"
  - "convertir un site web en app"
  - "documentation d’app WebView"
  - "SDK WebView iOS"
  - "PWA en app"
  - "HTML en app"
  - "pont JavaScript"
last_updated: "2026-10-09"
---

# API de lecteur vidéo natif – WebViewGold pour iOS

> **Résumé :** Lisez des flux vidéo dans le lecteur natif d'iOS avec prise en charge du mode Image dans l'image — déclenchés directement depuis votre application web.

[Documentation](../README.md) › [WebViewGold pour iOS](README.md) › API de vidéo native

**Plateforme :** iOS · **Catégorie :** API et fonctionnalités · **Version en ligne :** [www.webviewgold.com/fr/docs/iOS/native-video/](https://www.webviewgold.com/fr/docs/iOS/native-video/)

---

L'**API de lecteur vidéo natif** permet à votre site web de lancer un flux vidéo dans le lecteur vidéo natif d'iOS avec prise en charge du mode **Image dans l'image** (Picture-in-Picture). Déclenchez la lecture native en ouvrant un lien avec le préfixe `startnativevideo://videostreamurl=` :

```html
<a href="startnativevideo://videostreamurl=YOUR_VIDEO_STREAM_URL">Lire la vidéo dans le lecteur système avec prise en charge PiP</a>
```

L'utilisateur peut continuer à regarder la vidéo dans une fenêtre flottante Image dans l'image tout en naviguant dans votre application web, voire dans d'autres applications.

## Cas d'utilisation typiques

- Diffusions en direct qui doivent continuer pendant que l'utilisateur parcourt votre application web.
- Cours vidéo ou tutoriels avec les commandes de lecture du système.
- Toute vidéo qui bénéficie d'AirPlay, du plein écran et du mode Image dans l'image du lecteur natif.

**Remarque :** utilisez une URL directe du flux vidéo (par ex. un fichier .mp4 ou un flux HLS .m3u8) — et non l'URL d'une page HTML qui intègre la vidéo.

---

## Continuer la lecture

- ← Précédent : [API audio HTML](html-audio.md)
- Suivant → : [API de téléchargement de fichiers](file-downloader.md)
- Même fonctionnalité sur les autres plateformes : [Android – API vidéo native (PiP)](../android/native-video.md)
- Langues : [🇺🇸 English](../../ios/native-video.md) · [🇩🇪 Deutsch](../../de/ios/native-video.md) · **🇫🇷 Français** · [🇪🇸 Español](../../es/ios/native-video.md) · [🇨🇳 中文](../../zh/ios/native-video.md)

> [!TIP]
> **Trop occupé ? Nous configurons votre app pour vous.** Notre équipe configure, compile & soumet votre app WebViewGold — clé en main, délai rapide, Made in Germany. [Faire configurer mon app →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **Compilez dans votre navigateur :** Pas de Mac, pas d’IDE : le **WebViewGold Cloud Builder** configure, compile & met en ligne votre app. [Découvrir Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
