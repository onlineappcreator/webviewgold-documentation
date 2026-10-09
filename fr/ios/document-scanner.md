---
title: "Scanner de documents VisionKit – Documentation WebViewGold pour iOS"
description: "Permettez aux utilisateurs de scanner des documents papier avec l'appareil photo et de les téléverser via l'upload de fichiers de votre application web — propulsé par Apple VisionKit."
lang: "fr"
product: "WebViewGold pour iOS"
platform: "iOS"
category: "API et fonctionnalités"
slug: "document-scanner"
canonical_url: "https://www.webviewgold.com/fr/docs/iOS/document-scanner/"
keywords:
  - "Scanner de documents"
  - "WebViewGold pour iOS"
  - "convertir un site web en app"
  - "documentation d’app WebView"
  - "SDK WebView iOS"
  - "PWA en app"
  - "HTML en app"
  - "pont JavaScript"
last_updated: "2026-10-09"
---

# Scanner de documents VisionKit – WebViewGold pour iOS

> **Résumé :** Permettez aux utilisateurs de scanner des documents papier avec l'appareil photo et de les téléverser via l'upload de fichiers de votre application web — propulsé par Apple VisionKit.

[Documentation](../README.md) › [WebViewGold pour iOS](README.md) › Scanner de documents

**Plateforme :** iOS · **Catégorie :** API et fonctionnalités · **Version en ligne :** [www.webviewgold.com/fr/docs/iOS/document-scanner/](https://www.webviewgold.com/fr/docs/iOS/document-scanner/)

---

La fonctionnalité **Scanner de documents** ajoute une option **Scanner un document** au sélecteur standard de téléversement de fichiers de votre application. L'utilisateur peut scanner une ou plusieurs pages avec l'appareil photo ; l'application produit un scan du document et le téléverse via le flux standard `<input type="file">` utilisé par votre application web. Elle s'appuie sur le framework **VisionKit** d'Apple (`VNDocumentCameraViewController`) — avec détection automatique des bords, recadrage et amélioration de l'image.

## Activation

Activez la fonctionnalité dans **Config.swift** :

```swift
var kVisionKitEnable = true
```

Définissez-la sur `false` pour masquer l'entrée **Scanner un document**.

## Expérience utilisateur

1. Sur votre page web, l'utilisateur touche un `<input type="file">`.
2. L'application affiche une boîte de dialogue de téléversement avec des entrées telles que *Scanner un document*, *Appareil photo* et *Photothèque*.
3. Toucher **Scanner un document** lance le scanner VisionKit : il détecte les bords, recadre et améliore chaque page, et permet d'ajouter d'autres pages.
4. Le scan obtenu est renvoyé dans le `<input type="file">` — votre application web le reçoit exactement comme n'importe quel autre fichier téléversé.

**Remarques :** nécessite iOS 18.4 ou version ultérieure et un appareil prenant en charge la caméra de documents VisionKit. Sur les appareils non compatibles, l'entrée **Scanner un document** est masquée automatiquement.

---

## Continuer la lecture

- ← Précédent : [API de mode de scan](scanning-mode.md)
- Suivant → : [API de capture d'écran](take-screenshot.md)
- Même fonctionnalité sur les autres plateformes : [Android – Document Scanner](../android/document-scanner.md)
- Langues : [🇺🇸 English](../../ios/document-scanner.md) · [🇩🇪 Deutsch](../../de/ios/document-scanner.md) · **🇫🇷 Français** · [🇪🇸 Español](../../es/ios/document-scanner.md) · [🇨🇳 中文](../../zh/ios/document-scanner.md)

> [!TIP]
> **Trop occupé ? Nous configurons votre app pour vous.** Notre équipe configure, compile & soumet votre app WebViewGold — clé en main, délai rapide, Made in Germany. [Faire configurer mon app →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **Compilez dans votre navigateur :** Pas de Mac, pas d’IDE : le **WebViewGold Cloud Builder** configure, compile & met en ligne votre app. [Découvrir Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
