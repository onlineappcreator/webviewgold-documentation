---
title: "ML Kit Document Scanner (PDF) – Documentation WebViewGold pour Android"
description: "Add a Scan document option to the file upload dialog — the user scans up to 5 pages and your web app receives a PDF like any other upload."
lang: "fr"
product: "WebViewGold pour Android"
platform: "Android"
category: "API et fonctionnalités"
slug: "document-scanner"
canonical_url: "https://www.webviewgold.com/fr/docs/android/document-scanner/"
keywords:
  - "Document Scanner"
  - "WebViewGold pour Android"
  - "convertir un site web en app"
  - "documentation d’app WebView"
  - "SDK WebView Android"
  - "PWA en app"
  - "HTML en app"
  - "pont JavaScript"
last_updated: "2026-10-09"
---

# ML Kit Document Scanner (PDF) – WebViewGold pour Android

> **Résumé :** Add a Scan document option to the file upload dialog — the user scans up to 5 pages and your web app receives a PDF like any other upload.

[Documentation](../README.md) › [WebViewGold pour Android](README.md) › Document Scanner

**Plateforme :** Android · **Catégorie :** API et fonctionnalités · **Version en ligne :** [www.webviewgold.com/fr/docs/android/document-scanner/](https://www.webviewgold.com/fr/docs/android/document-scanner/)

---

La fonctionnalité **Document Scanner** ajoute une option **Numériser un document** au sélecteur de téléchargement de fichiers standard. L'utilisateur peut numériser jusqu'à 5 pages avec la caméra ; l'application génère un PDF et le téléverse via le flux standard `<input type="file">` utilisé par votre application web. La fonctionnalité s'appuie sur le Document Scanner ML Kit de Google.

## Comment l'activer

Activez la fonctionnalité dans **Config.java** :

```java
public static final boolean ENABLE_ML_KIT_DOCUMENT_SCANNER = true;
```

Réglez sur `false` pour masquer l'entrée **Numériser un document**.

## Expérience utilisateur

1. Sur votre page web, l'utilisateur tape sur un `<input type="file">`.
2. L'application affiche une boîte de dialogue de téléversement avec des entrées telles que *Numériser un document*, *Prendre une photo*, *Enregistrer une vidéo* et *Choisir dans la galerie* (selon l'attribut `accept` de l'input).
3. Un appui sur **Numériser un document** lance le scanner ML Kit de Google : il détecte les bords, recadre et améliore chaque page, permet d'ajouter d'autres pages, et renvoie un PDF.
4. Le PDF résultant est réinjecté dans le `<input type="file">` — votre application web le reçoit exactement comme n'importe quel autre fichier téléversé.

**Remarques :** Nécessite les Google Play Services (disponibles sur tous les téléphones Android standard équipés du Play Store). Le format de résultat est **PDF**, avec un maximum de 5 pages par numérisation. L'import depuis la galerie au sein du scanner est autorisé par défaut.

---

## Continuer la lecture

- ← Précédent : [Biometric Auth API](biometric-auth.md)
- Suivant → : [Printer API](printer.md)
- Même fonctionnalité sur les autres plateformes : [iOS – Scanner de documents](../ios/document-scanner.md)
- Langues : [🇺🇸 English](../../android/document-scanner.md) · [🇩🇪 Deutsch](../../de/android/document-scanner.md) · **🇫🇷 Français** · [🇪🇸 Español](../../es/android/document-scanner.md) · [🇨🇳 中文](../../zh/android/document-scanner.md)

> [!TIP]
> **Trop occupé ? Nous configurons votre app pour vous.** Notre équipe configure, compile & soumet votre app WebViewGold — clé en main, délai rapide, Made in Germany. [Faire configurer mon app →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_android_doc_online)
>
> **Compilez dans votre navigateur :** Pas de Mac, pas d’IDE : le **WebViewGold Cloud Builder** configure, compile & met en ligne votre app. [Découvrir Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=android_docs)
