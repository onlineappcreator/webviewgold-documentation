---
title: "Firebase Crashlytics – Documentation WebViewGold pour Android"
description: "Ship crash reports and non-fatal events to your Firebase project, with runtime opt-in / opt-out from your web app."
lang: "fr"
product: "WebViewGold pour Android"
platform: "Android"
category: "Compiler et publier"
slug: "crashlytics"
canonical_url: "https://www.webviewgold.com/fr/docs/android/crashlytics/"
keywords:
  - "Firebase Crashlytics"
  - "WebViewGold pour Android"
  - "convertir un site web en app"
  - "documentation d’app WebView"
  - "SDK WebView Android"
  - "PWA en app"
  - "HTML en app"
  - "pont JavaScript"
last_updated: "2026-10-09"
---

# Firebase Crashlytics – WebViewGold pour Android

> **Résumé :** Ship crash reports and non-fatal events to your Firebase project, with runtime opt-in / opt-out from your web app.

[Documentation](../README.md) › [WebViewGold pour Android](README.md) › Firebase Crashlytics

**Plateforme :** Android · **Catégorie :** Compiler et publier · **Version en ligne :** [www.webviewgold.com/fr/docs/android/crashlytics/](https://www.webviewgold.com/fr/docs/android/crashlytics/)

---

L'intégration de **Firebase Crashlytics** envoie des rapports de plantage anonymes et des évènements non fatals à votre projet Firebase, afin que vous puissiez repérer les problèmes de stabilité en production.

## Comment l'activer

1. Configurez Firebase pour votre application et placez le fichier `google-services.json` dans `AndroidStudioSourceCode/app/`.
2. Dans **Config.java**, activez le suivi :

   ```java
   public static final boolean TRACKING_EVENT = true;
   ```

`TRACKING_EVENT = false` désactive toutes les fonctionnalités liées au suivi, y compris la journalisation des évènements Crashlytics et les déclencheurs `starttracking://` / `endtracking://`.

## Opt-in / Opt-out à l'exécution depuis votre application web

WebViewGold respecte un indicateur de suivi par utilisateur qui est persisté sur l'appareil. Utilisez les déclencheurs de suivi standard pour le modifier à l'exécution :

```html
<a href="starttracking://">Enable analytics & crash reports</a>
<a href="endtracking://">Disable analytics & crash reports</a>
```

Lorsque l'utilisateur a refusé, la collecte Crashlytics est désactivée — rien n'est envoyé.

## Ce qui est signalé

- Les plantages non gérés (traces d'appels, modèle d'appareil, version du système d'exploitation).
- Les exceptions non fatales enregistrées en interne par la coque de l'application.
- Aucune donnée personnelle de l'utilisateur n'est jointe par défaut.

**Où consulter les rapports :** Ouvrez votre tableau de bord **Firebase Console → Crashlytics**. Les rapports apparaissent généralement quelques minutes après un plantage.

**Remarques :** L'initialisation de Crashlytics fonctionne au mieux — si Firebase est mal configuré, l'application continue de fonctionner normalement. Envisagez d'ajouter un écran de consentement (RGPD / CCPA) avant d'appeler `starttracking://` pour la première fois.

---

## Continuer la lecture

- ← Précédent : [Health Connect API](health-connect.md)
- Suivant → : [Compiler et publier](publish.md)
- Langues : [🇺🇸 English](../../android/crashlytics.md) · [🇩🇪 Deutsch](../../de/android/crashlytics.md) · **🇫🇷 Français** · [🇪🇸 Español](../../es/android/crashlytics.md) · [🇨🇳 中文](../../zh/android/crashlytics.md)

> [!TIP]
> **Trop occupé ? Nous configurons votre app pour vous.** Notre équipe configure, compile & soumet votre app WebViewGold — clé en main, délai rapide, Made in Germany. [Faire configurer mon app →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_android_doc_online)
>
> **Compilez dans votre navigateur :** Pas de Mac, pas d’IDE : le **WebViewGold Cloud Builder** configure, compile & met en ligne votre app. [Découvrir Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=android_docs)
