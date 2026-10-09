---
title: "API d'impression – Documentation WebViewGold pour iOS"
description: "Imprimez des images et des PDF depuis votre application web via AirPrint : envoyez des fichiers à la boîte de dialogue d'impression native d'iOS avec un seul lien."
lang: "fr"
product: "WebViewGold pour iOS"
platform: "iOS"
category: "API et fonctionnalités"
slug: "printer"
canonical_url: "https://www.webviewgold.com/fr/docs/iOS/printer/"
keywords:
  - "API d'impression"
  - "WebViewGold pour iOS"
  - "convertir un site web en app"
  - "documentation d’app WebView"
  - "SDK WebView iOS"
  - "PWA en app"
  - "HTML en app"
  - "pont JavaScript"
last_updated: "2026-10-09"
---

# API d'impression – WebViewGold pour iOS

> **Résumé :** Imprimez des images et des PDF depuis votre application web via AirPrint : envoyez des fichiers à la boîte de dialogue d'impression native d'iOS avec un seul lien.

[Documentation](../README.md) › [WebViewGold pour iOS](README.md) › API d'impression

**Plateforme :** iOS · **Catégorie :** API et fonctionnalités · **Version en ligne :** [www.webviewgold.com/fr/docs/iOS/printer/](https://www.webviewgold.com/fr/docs/iOS/printer/)

---

L'**API d'impression** envoie un fichier distant (image ou PDF) à la boîte de dialogue d'impression native d'iOS (**AirPrint**), afin que l'utilisateur puisse l'imprimer sur n'importe quelle imprimante configurée ou l'enregistrer en PDF.

## Utilisation

```html
<a href="printitem://?jobName=Facture%20%23123&printItem=https://example.com/invoice.pdf">
  Imprimer la facture
</a>
```

## Paramètres de requête

| Nom | Obligatoire | Description |
| --- | --- | --- |
| `printItem` | oui | URL complète du fichier à imprimer (PDF, JPG, PNG, WebP…). |
| `jobName` | non | Nom lisible de la tâche, affiché dans la boîte de dialogue d'impression. |

## Fonctionnement

1. L'application télécharge le fichier depuis `printItem` dans un cache temporaire.
2. Le fichier est transmis au `UIPrintInteractionController` natif, qui affiche la boîte de dialogue d'impression d'iOS.
3. L'utilisateur choisit une imprimante AirPrint (ou **Enregistrer au format PDF** via les options de partage) et confirme.

**Remarques :** le fichier cible doit être accessible publiquement depuis l'appareil (l'URL doit être résolvable). Encodez les caractères spéciaux du paramètre `jobName` au format URL (par ex. `%20` pour les espaces).

---

## Continuer la lecture

- ← Précédent : [API de téléchargement de fichiers](file-downloader.md)
- Suivant → : [API calendrier iCal](ical-calendar.md)
- Même fonctionnalité sur les autres plateformes : [Android – Printer API](../android/printer.md)
- Langues : [🇺🇸 English](../../ios/printer.md) · [🇩🇪 Deutsch](../../de/ios/printer.md) · **🇫🇷 Français** · [🇪🇸 Español](../../es/ios/printer.md) · [🇨🇳 中文](../../zh/ios/printer.md)

> [!TIP]
> **Trop occupé ? Nous configurons votre app pour vous.** Notre équipe configure, compile & soumet votre app WebViewGold — clé en main, délai rapide, Made in Germany. [Faire configurer mon app →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **Compilez dans votre navigateur :** Pas de Mac, pas d’IDE : le **WebViewGold Cloud Builder** configure, compile & met en ligne votre app. [Découvrir Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
