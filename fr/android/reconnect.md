---
title: "Reconnect API – Documentation WebViewGold pour Android"
description: "Reload the last online URL from your offline / fallback HTML page — the perfect \"Try again\" button for your custom offline screen."
lang: "fr"
product: "WebViewGold pour Android"
platform: "Android"
category: "API et fonctionnalités"
slug: "reconnect"
canonical_url: "https://www.webviewgold.com/fr/docs/android/reconnect/"
keywords:
  - "Reconnect API"
  - "WebViewGold pour Android"
  - "convertir un site web en app"
  - "documentation d’app WebView"
  - "SDK WebView Android"
  - "PWA en app"
  - "HTML en app"
  - "pont JavaScript"
last_updated: "2026-10-09"
---

# Reconnect API – WebViewGold pour Android

> **Résumé :** Reload the last online URL from your offline / fallback HTML page — the perfect "Try again" button for your custom offline screen.

[Documentation](../README.md) › [WebViewGold pour Android](README.md) › Reconnect API

**Plateforme :** Android · **Catégorie :** API et fonctionnalités · **Version en ligne :** [www.webviewgold.com/fr/docs/android/reconnect/](https://www.webviewgold.com/fr/docs/android/reconnect/)

---

L'**API Reconnect** recharge la dernière URL en ligne sur laquelle se trouvait l'utilisateur avant que votre application ne bascule sur la page HTML hors ligne. Elle est conçue comme un bouton « Réessayer » sur votre écran personnalisé de repli/hors ligne.

## Utilisation

Ajoutez le déclencheur à votre page hors ligne (généralement `local-html/index.html`) :

```html
<button onclick="window.location.href='reconnect://'">Try to reconnect</button>
```

## Fonctionnement

L'application mémorise la dernière URL non auxiliaire chargée avec succès. Lorsque l'utilisateur appuie sur `reconnect://`, la WebView revient vers cette URL. Si la connectivité est toujours indisponible, votre page de repli est de nouveau affichée.

## Configuration associée

- `FALLBACK_USE_LOCAL_HTML_FOLDER_IF_OFFLINE` dans **Config.java** doit être défini sur `true`, et vous devez disposer d'une page de repli `local-html/index.html` pour que cette fonctionnalité ait du sens.

---

## Continuer la lecture

- ← Précédent : [Open App Settings API](open-app-settings.md)
- Suivant → : [Read/Write Value API](read-write-value.md)
- Même fonctionnalité sur les autres plateformes : [iOS – API de reconnexion](../ios/reconnect.md)
- Langues : [🇺🇸 English](../../android/reconnect.md) · [🇩🇪 Deutsch](../../de/android/reconnect.md) · **🇫🇷 Français** · [🇪🇸 Español](../../es/android/reconnect.md) · [🇨🇳 中文](../../zh/android/reconnect.md)

> [!TIP]
> **Trop occupé ? Nous configurons votre app pour vous.** Notre équipe configure, compile & soumet votre app WebViewGold — clé en main, délai rapide, Made in Germany. [Faire configurer mon app →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_android_doc_online)
>
> **Compilez dans votre navigateur :** Pas de Mac, pas d’IDE : le **WebViewGold Cloud Builder** configure, compile & met en ligne votre app. [Découvrir Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=android_docs)
