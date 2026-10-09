---
title: "Biometric Authentication API – Documentation WebViewGold pour Android"
description: "Prompt fingerprint or face authentication with the native Android BiometricPrompt directly from your web app."
lang: "fr"
product: "WebViewGold pour Android"
platform: "Android"
category: "API et fonctionnalités"
slug: "biometric-auth"
canonical_url: "https://www.webviewgold.com/fr/docs/android/biometric-auth/"
keywords:
  - "Biometric Auth API"
  - "WebViewGold pour Android"
  - "convertir un site web en app"
  - "documentation d’app WebView"
  - "SDK WebView Android"
  - "PWA en app"
  - "HTML en app"
  - "pont JavaScript"
last_updated: "2026-10-09"
---

# Biometric Authentication API – WebViewGold pour Android

> **Résumé :** Prompt fingerprint or face authentication with the native Android BiometricPrompt directly from your web app.

[Documentation](../README.md) › [WebViewGold pour Android](README.md) › Biometric Auth API

**Plateforme :** Android · **Catégorie :** API et fonctionnalités · **Version en ligne :** [www.webviewgold.com/fr/docs/android/biometric-auth/](https://www.webviewgold.com/fr/docs/android/biometric-auth/)

---

L'**API d'authentification biométrique** demande à l'utilisateur de s'authentifier par empreinte digitale ou reconnaissance faciale via le `BiometricPrompt` natif de l'appareil. Si le système d'exploitation est configuré ainsi, il se rabat sur le code PIN ou le schéma de déverrouillage de l'appareil.

## Utilisation

Déclenchez la boîte de dialogue système depuis un lien HTML ou depuis JavaScript :

```html
<a href="bioauth://">Unlock</a>
```

```javascript
window.location.href = "bioauth://";
```

## Cas d'usage typiques

- Restreindre l'accès à une page « portefeuille », « paramètres » ou « commandes » dans votre application web.
- Exiger une nouvelle authentification avant une étape de paiement sensible.

## Comportement

- La boîte de dialogue système est dessinée par l'application — votre application web n'a besoin d'afficher aucune interface.
- Après une authentification réussie, l'application reprend son fonctionnement normal afin que votre application web puisse réagir (par exemple en naviguant vers la page protégée).
- Sur certains appareils sans capteur biométrique, le système d'exploitation peut afficher une invite de saisie du code PIN à la place.

## Configuration associée

`enableBioMetricAuth` dans **Config.java** active le flux intégré **App Lock** qui exige une authentification biométrique à chaque lancement de l'application. `bioauth://` est indépendant de ce paramètre et peut être déclenché à tout moment depuis JavaScript.

---

## Continuer la lecture

- ← Précédent : [Read/Write Value API](read-write-value.md)
- Suivant → : [Document Scanner](document-scanner.md)
- Même fonctionnalité sur les autres plateformes : [iOS – API d'authentification biométrique](../ios/biometric-authentication.md)
- Langues : [🇺🇸 English](../../android/biometric-auth.md) · [🇩🇪 Deutsch](../../de/android/biometric-auth.md) · **🇫🇷 Français** · [🇪🇸 Español](../../es/android/biometric-auth.md) · [🇨🇳 中文](../../zh/android/biometric-auth.md)

> [!TIP]
> **Trop occupé ? Nous configurons votre app pour vous.** Notre équipe configure, compile & soumet votre app WebViewGold — clé en main, délai rapide, Made in Germany. [Faire configurer mon app →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_android_doc_online)
>
> **Compilez dans votre navigateur :** Pas de Mac, pas d’IDE : le **WebViewGold Cloud Builder** configure, compile & met en ligne votre app. [Découvrir Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=android_docs)
