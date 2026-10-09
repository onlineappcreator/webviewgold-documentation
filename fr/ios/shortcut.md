---
title: "API Shortcut – Documentation WebViewGold pour iOS"
description: "Ajoutez des raccourcis d'action rapide sur l'écran d'accueil de votre application iOS qui redirigent par deep link vers des pages précises."
lang: "fr"
product: "WebViewGold pour iOS"
platform: "iOS"
category: "API et fonctionnalités"
slug: "shortcut"
canonical_url: "https://www.webviewgold.com/fr/docs/iOS/shortcut/"
keywords:
  - "API Shortcut"
  - "WebViewGold pour iOS"
  - "convertir un site web en app"
  - "documentation d’app WebView"
  - "SDK WebView iOS"
  - "PWA en app"
  - "HTML en app"
  - "pont JavaScript"
last_updated: "2026-10-09"
---

# API Shortcut – WebViewGold pour iOS

> **Résumé :** Ajoutez des raccourcis d'action rapide sur l'écran d'accueil de votre application iOS qui redirigent par deep link vers des pages précises.

[Documentation](../README.md) › [WebViewGold pour iOS](README.md) › API Shortcut

**Plateforme :** iOS · **Catégorie :** API et fonctionnalités · **Version en ligne :** [www.webviewgold.com/fr/docs/iOS/shortcut/](https://www.webviewgold.com/fr/docs/iOS/shortcut/)

---

Activez `var useShortcuts = true` dans `Config.swift` pour enregistrer les raccourcis dynamiques définis dans `Shortcuts.json`. Chaque raccourci peut ouvrir une URL, injecter du JavaScript et afficher un SF Symbol. Exemple :

```json
{
    "shortcuts": [
        {
            "title": "Open Google",
            "redirection_link": "https://google.com",
            "injection": "",
            "symbol": "wrench.and.screwdriver"
        },
        {
            "title": "Open & Inject",
            "redirection_link": "https://apple.com",
            "injection": "(function() { console.log('Injected and executed!'); })();",
            "symbol": "lock.open"
        }
    ]
}
```

Les utilisateurs peuvent accéder aux raccourcis en effectuant un appui prolongé sur l'icône de l'application.

---

## Continuer la lecture

- ← Précédent : [API de retour haptique](haptic-feedback.md)
- Suivant → : [API Presse-papiers](clipboard.md)
- Langues : [🇺🇸 English](../../ios/shortcut.md) · [🇩🇪 Deutsch](../../de/ios/shortcut.md) · **🇫🇷 Français** · [🇪🇸 Español](../../es/ios/shortcut.md) · [🇨🇳 中文](../../zh/ios/shortcut.md)

> [!TIP]
> **Trop occupé ? Nous configurons votre app pour vous.** Notre équipe configure, compile & soumet votre app WebViewGold — clé en main, délai rapide, Made in Germany. [Faire configurer mon app →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **Compilez dans votre navigateur :** Pas de Mac, pas d’IDE : le **WebViewGold Cloud Builder** configure, compile & met en ligne votre app. [Découvrir Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
