---
title: "API de téléchargement de fichiers – Documentation WebViewGold pour Android"
description: "Permettez aux utilisateurs de télécharger images, PDF et autres fichiers depuis votre application web vers leur appareil Android."
lang: "fr"
product: "WebViewGold pour Android"
platform: "Android"
category: "API et fonctionnalités"
slug: "file-downloader"
canonical_url: "https://www.webviewgold.com/fr/docs/android/file-downloader/"
keywords:
  - "API de téléchargement de fichiers"
  - "WebViewGold pour Android"
  - "convertir un site web en app"
  - "documentation d’app WebView"
  - "SDK WebView Android"
  - "PWA en app"
  - "HTML en app"
  - "pont JavaScript"
last_updated: "2026-10-09"
---

# API de téléchargement de fichiers – WebViewGold pour Android

> **Résumé :** Permettez aux utilisateurs de télécharger images, PDF et autres fichiers depuis votre application web vers leur appareil Android.

[Documentation](../README.md) › [WebViewGold pour Android](README.md) › API de téléchargement de fichiers

**Plateforme :** Android · **Catégorie :** API et fonctionnalités · **Version en ligne :** [www.webviewgold.com/fr/docs/android/file-downloader/](https://www.webviewgold.com/fr/docs/android/file-downloader/)

---

L'API Download de WebViewGold vous permet de proposer le téléchargement de documents, d'images et de fichiers audio dans votre application WebView. Les étapes suivantes décrivent comment activer et personnaliser la fonctionnalité de téléchargement :

## 1. Télécharger des images

Enregistrez les images dans la pellicule de l'utilisateur en appelant des liens avec le préfixe savethisimage://?url= :

```html
<a href="savethisimage://?url=IMAGE URL HERE">Download Image</a>
```

## 2. Télécharger des fichiers PDF

Enregistrez les fichiers PDF en appelant des liens avec un suffixe .pdf :

```html
<a href="https://www.example.org/file.pdf">Download PDF</a>
```

## 3. Télécharger des fichiers musicaux

Enregistrez les fichiers musicaux en appelant simplement des liens avec un suffixe .mp3, .mp4 ou .wav :

```html
<a href="https://www.example.org/file.mp3">Download MP3</a>
<a href="https://www.example.org/file.mp4">Download MP4</a>
<a href="https://www.example.org/file.wav">Download WAV</a>
```

## 4. Personnaliser les types de fichiers pris en charge

Pour ajouter des formats de fichiers supplémentaires au téléchargeur, insérez-les dans la liste `downloadableExtension` dans **Config.java**.

## 5. Activer les téléchargements automatiques

Envisagez de définir l'option `AUTO_DOWNLOAD_FILES` dans **Config.java** pour activer les téléchargements automatiques des fichiers signalés par des en-têtes HTTP Content-Disposition, indépendamment de la liste `downloadableExtension`. Cela garantit que les fichiers sont téléchargés automatiquement en fonction des configurations serveur.

---

## Continuer la lecture

- ← Précédent : [API Facebook Ads](facebook-ads.md)
- Suivant → : [API vidéo native (PiP)](native-video.md)
- Même fonctionnalité sur les autres plateformes : [iOS – API de téléchargement de fichiers](../ios/file-downloader.md)
- Langues : [🇺🇸 English](../../android/file-downloader.md) · [🇩🇪 Deutsch](../../de/android/file-downloader.md) · **🇫🇷 Français** · [🇪🇸 Español](../../es/android/file-downloader.md) · [🇨🇳 中文](../../zh/android/file-downloader.md)

> [!TIP]
> **Trop occupé ? Nous configurons votre app pour vous.** Notre équipe configure, compile & soumet votre app WebViewGold — clé en main, délai rapide, Made in Germany. [Faire configurer mon app →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_android_doc_online)
>
> **Compilez dans votre navigateur :** Pas de Mac, pas d’IDE : le **WebViewGold Cloud Builder** configure, compile & met en ligne votre app. [Découvrir Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=android_docs)
