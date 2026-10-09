---
title: "Navigation Drawer & Bottom Navigation Footer – Documentation WebViewGold pour Android"
description: "Ship an app-like navigation experience with the built-in Material navigation drawer and Material 3 bottom navigation bar — no changes to your website required."
lang: "fr"
product: "WebViewGold pour Android"
platform: "Android"
category: "Design de l’app"
slug: "navigation-drawer"
canonical_url: "https://www.webviewgold.com/fr/docs/android/navigation-drawer/"
keywords:
  - "Navigation Drawer & Footer"
  - "WebViewGold pour Android"
  - "convertir un site web en app"
  - "documentation d’app WebView"
  - "SDK WebView Android"
  - "PWA en app"
  - "HTML en app"
  - "pont JavaScript"
last_updated: "2026-10-09"
---

# Navigation Drawer & Bottom Navigation Footer – WebViewGold pour Android

> **Résumé :** Ship an app-like navigation experience with the built-in Material navigation drawer and Material 3 bottom navigation bar — no changes to your website required.

[Documentation](../README.md) › [WebViewGold pour Android](README.md) › Navigation Drawer & Footer

**Plateforme :** Android · **Catégorie :** Design de l’app · **Version en ligne :** [www.webviewgold.com/fr/docs/android/navigation-drawer/](https://www.webviewgold.com/fr/docs/android/navigation-drawer/)

---

WebViewGold est livré avec deux interfaces de navigation natives intégrées vous permettant de proposer une expérience de navigation semblable à celle d'une application, sans toucher à votre site web : un **tiroir de navigation** latéral et un **pied de navigation inférieur** Material 3. Les deux sont facultatifs et peuvent être combinés ou utilisés indépendamment.

## 1. Tiroir de navigation latéral

Un bouton de menu flottant ouvre un tiroir de navigation Material contenant vos liens. Activez-le dans **Config.java** :

```java
static boolean ENABLE_NAVIGATION_DRAWER = true;
```

Configurez les entrées et les icônes dans :

```
app/src/main/res/menu/menu_drawer.xml
```

Chaque `<item>` devient une ligne du tiroir et, une fois cliqué, fait naviguer la WebView vers l'URL que vous lui associez.

## 2. Pied de navigation inférieur

Une barre de navigation inférieure Material 3 se place en bas de l'écran et bascule entre vos sections principales. Activez-la dans **Config.java** :

```java
static boolean ENABLE_NAVIGATION_FOOTER = true;
```

Le même fichier (`res/menu/menu_drawer.xml`) définit les entrées — choisissez 3 à 5 destinations principales.

## Comportement

- Les deux interfaces respectent automatiquement le mode sombre/clair de l'appareil.
- Les icônes et les libellés proviennent de votre menu XML.
- Un appui sur une entrée charge l'URL associée dans la WebView principale, de sorte que votre application web ne quitte jamais la coque de l'application.

**Référence :** [Directives Material 3 pour la barre de navigation](https://m3.material.io/components/navigation-bar/overview).

---

## Continuer la lecture

- ← Précédent : [Écran de démarrage](splash-screen.md)
- Suivant → : [API de gestion des URL](url-handling.md)
- Même fonctionnalité sur les autres plateformes : [iOS – Pied de navigation natif](../ios/navigation-footer.md)
- Langues : [🇺🇸 English](../../android/navigation-drawer.md) · [🇩🇪 Deutsch](../../de/android/navigation-drawer.md) · **🇫🇷 Français** · [🇪🇸 Español](../../es/android/navigation-drawer.md) · [🇨🇳 中文](../../zh/android/navigation-drawer.md)

> [!TIP]
> **Trop occupé ? Nous configurons votre app pour vous.** Notre équipe configure, compile & soumet votre app WebViewGold — clé en main, délai rapide, Made in Germany. [Faire configurer mon app →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_android_doc_online)
>
> **Compilez dans votre navigateur :** Pas de Mac, pas d’IDE : le **WebViewGold Cloud Builder** configure, compile & met en ligne votre app. [Découvrir Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=android_docs)
