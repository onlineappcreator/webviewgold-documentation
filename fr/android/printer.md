---
title: "Printer API – Documentation WebViewGold pour Android"
description: "Send a remote image or PDF to the Android system print dialog — Wi-Fi printers, cloud print, or Save-as-PDF, straight from your web app."
lang: "fr"
product: "WebViewGold pour Android"
platform: "Android"
category: "API et fonctionnalités"
slug: "printer"
canonical_url: "https://www.webviewgold.com/fr/docs/android/printer/"
keywords:
  - "Printer API"
  - "WebViewGold pour Android"
  - "convertir un site web en app"
  - "documentation d’app WebView"
  - "SDK WebView Android"
  - "PWA en app"
  - "HTML en app"
  - "pont JavaScript"
last_updated: "2026-10-09"
---

# Printer API – WebViewGold pour Android

> **Résumé :** Send a remote image or PDF to the Android system print dialog — Wi-Fi printers, cloud print, or Save-as-PDF, straight from your web app.

[Documentation](../README.md) › [WebViewGold pour Android](README.md) › Printer API

**Plateforme :** Android · **Catégorie :** API et fonctionnalités · **Version en ligne :** [www.webviewgold.com/fr/docs/android/printer/](https://www.webviewgold.com/fr/docs/android/printer/)

---

L'**API Printer** envoie un fichier distant (image ou PDF) à la boîte de dialogue d'impression du système Android, de sorte que l'utilisateur puisse l'imprimer sur n'importe quelle imprimante configurée — Wi-Fi, impression cloud, ou « Enregistrer au format PDF ».

## Utilisation

```html
<a href="printitem://?jobName=Invoice%20%23123&printItem=https://example.com/invoice.pdf">
  Print invoice
</a>
```

## Paramètres de la requête

| Nom | Requis | Description |
| --- | --- | --- |
| `printItem` | oui | URL complète du fichier à imprimer (PDF, JPG, PNG, WebP…). |
| `jobName` | non | Nom de tâche lisible affiché dans la boîte de dialogue d'impression. Par défaut : `Print Job`. |

## Fonctionnement

1. L'application télécharge le fichier depuis `printItem` dans un cache temporaire.
2. S'il s'agit d'une image, le fichier est imprimé via `PrintHelper` (ajusté pour s'adapter).
3. S'il s'agit d'un PDF (ou de tout autre format de document), il est envoyé au `PrintManager` Android avec un adaptateur de document approprié.
4. Le fichier temporaire est supprimé une fois la tâche mise en file d'attente.

**Remarques :** Le fichier cible doit être accessible publiquement depuis l'appareil (l'URL doit se résoudre). Les utilisateurs peuvent choisir **Enregistrer au format PDF** dans la boîte de dialogue d'impression pour en exporter une copie.

---

## Continuer la lecture

- ← Précédent : [Document Scanner](document-scanner.md)
- Suivant → : [Health Connect API](health-connect.md)
- Même fonctionnalité sur les autres plateformes : [iOS – API d'impression](../ios/printer.md)
- Langues : [🇺🇸 English](../../android/printer.md) · [🇩🇪 Deutsch](../../de/android/printer.md) · **🇫🇷 Français** · [🇪🇸 Español](../../es/android/printer.md) · [🇨🇳 中文](../../zh/android/printer.md)

> [!TIP]
> **Trop occupé ? Nous configurons votre app pour vous.** Notre équipe configure, compile & soumet votre app WebViewGold — clé en main, délai rapide, Made in Germany. [Faire configurer mon app →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_android_doc_online)
>
> **Compilez dans votre navigateur :** Pas de Mac, pas d’IDE : le **WebViewGold Cloud Builder** configure, compile & met en ligne votre app. [Découvrir Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=android_docs)
