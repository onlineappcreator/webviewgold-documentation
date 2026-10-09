---
title: "API de téléchargement de fichiers – Documentation WebViewGold pour iOS"
description: "Permettez aux utilisateurs de télécharger des images, des PDF et d'autres fichiers depuis votre application web directement sur leur iPhone ou iPad."
lang: "fr"
product: "WebViewGold pour iOS"
platform: "iOS"
category: "API et fonctionnalités"
slug: "file-downloader"
canonical_url: "https://www.webviewgold.com/fr/docs/iOS/file-downloader/"
keywords:
  - "API de téléchargement de fichiers"
  - "WebViewGold pour iOS"
  - "convertir un site web en app"
  - "documentation d’app WebView"
  - "SDK WebView iOS"
  - "PWA en app"
  - "HTML en app"
  - "pont JavaScript"
last_updated: "2026-10-09"
---

# API de téléchargement de fichiers – WebViewGold pour iOS

> **Résumé :** Permettez aux utilisateurs de télécharger des images, des PDF et d'autres fichiers depuis votre application web directement sur leur iPhone ou iPad.

[Documentation](../README.md) › [WebViewGold pour iOS](README.md) › API de téléchargement de fichiers

**Plateforme :** iOS · **Catégorie :** API et fonctionnalités · **Version en ligne :** [www.webviewgold.com/fr/docs/iOS/file-downloader/](https://www.webviewgold.com/fr/docs/iOS/file-downloader/)

---

L'API de téléchargement de WebViewGold vous permet de proposer le téléchargement de documents, d'images et de fichiers audio au sein de votre application WebView. Les étapes suivantes décrivent comment activer et personnaliser la fonctionnalité de téléchargement :

## 1. Télécharger des images

Enregistrez des images dans la pellicule de l'utilisateur en appelant des liens avec le préfixe savethisimage://?url= :

```html
<a href="savethisimage://?url=IMAGE URL HERE">Download Image</a>
```

## 2. Télécharger des fichiers

Enregistrez des fichiers en appelant des liens avec un suffixe approprié (par exemple .mp3) :

```html
<a href="https://www.example.org/file.pdf">Link PDF</a>
<a href="https://www.example.org/file.mp3">Link mp3 Music</a>
<a href="https://www.example.org/file.mp4">Link mp4 Music</a>
<a href="https://www.example.org/file.wav">Link wav Music</a>
<a href="https://www.example.org/file.epub">Link epub eBook</a>
<a href="https://www.example.org/file.pkpass">Link Passbook / Apple Wallet</a>
<a href="https://www.example.org/file.docx">Link Word</a>
<a href="https://www.example.org/file.pptx">Link PowerPoint</a>
<a href="https://www.example.org/file.xlsx">Link Excel</a>
```

## 3. Personnaliser les types de fichiers pris en charge

Vous pouvez ajouter d'autres types de fichiers qui doivent déclencher la fonctionnalité de téléchargement (par exemple .epub, .zip, ...) Cela peut se faire via la variable de liste `extentionARY` qui se trouve dans le fichier **Config.swift**.

## 4. Activer les téléchargements automatiques de fichiers

Vous pouvez définir l'option `autodownloader` dans **Config.swift** pour activer le téléchargement automatique des fichiers signalés par des en-têtes HTTP Content-Disposition, indépendamment de la liste `extentionARY`. Cela garantit que les fichiers sont téléchargés automatiquement en fonction des configurations du serveur.

[![Regarder la vidéo: API de téléchargement de fichiers](https://img.youtube.com/vi/V0LnwnzJx6I/hqdefault.jpg)](https://www.youtube.com/watch?v=V0LnwnzJx6I)

---

## Continuer la lecture

- ← Précédent : [API de vidéo native](native-video.md)
- Suivant → : [API d'impression](printer.md)
- Même fonctionnalité sur les autres plateformes : [Android – API de téléchargement de fichiers](../android/file-downloader.md)
- Langues : [🇺🇸 English](../../ios/file-downloader.md) · [🇩🇪 Deutsch](../../de/ios/file-downloader.md) · **🇫🇷 Français** · [🇪🇸 Español](../../es/ios/file-downloader.md) · [🇨🇳 中文](../../zh/ios/file-downloader.md)

> [!TIP]
> **Trop occupé ? Nous configurons votre app pour vous.** Notre équipe configure, compile & soumet votre app WebViewGold — clé en main, délai rapide, Made in Germany. [Faire configurer mon app →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **Compilez dans votre navigateur :** Pas de Mac, pas d’IDE : le **WebViewGold Cloud Builder** configure, compile & met en ligne votre app. [Découvrir Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
