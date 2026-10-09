---
title: "API Contacts – Documentation WebViewGold pour iOS"
description: "Accédez au carnet d'adresses de l'appareil depuis votre application web : lisez les contacts avec l'autorisation de l'utilisateur dans WebViewGold pour iOS."
lang: "fr"
product: "WebViewGold pour iOS"
platform: "iOS"
category: "API et fonctionnalités"
slug: "contacts"
canonical_url: "https://www.webviewgold.com/fr/docs/iOS/contacts/"
keywords:
  - "API Contacts"
  - "WebViewGold pour iOS"
  - "convertir un site web en app"
  - "documentation d’app WebView"
  - "SDK WebView iOS"
  - "PWA en app"
  - "HTML en app"
  - "pont JavaScript"
last_updated: "2026-10-09"
---

# API Contacts – WebViewGold pour iOS

> **Résumé :** Accédez au carnet d'adresses de l'appareil depuis votre application web : lisez les contacts avec l'autorisation de l'utilisateur dans WebViewGold pour iOS.

[Documentation](../README.md) › [WebViewGold pour iOS](README.md) › API Contacts

**Plateforme :** iOS · **Catégorie :** API et fonctionnalités · **Version en ligne :** [www.webviewgold.com/fr/docs/iOS/contacts/](https://www.webviewgold.com/fr/docs/iOS/contacts/)

---

WebViewGold permet d'exporter les contacts dans une variable JavaScript, au format ci-dessous, via l'API **readcontacts://**. L'objet JSON est stocké dans la variable `contacts`. Pour y accéder, votre application doit d'abord obtenir la permission via l'API **requestcontactpermission://**, qui invitera votre utilisateur à activer les autorisations d'accès aux contacts. Sans cette étape préalable, **readcontacts://** initialisera la variable `contacts` avec la valeur null.\
Exemple de sortie stockée dans la variable JS `contacts` :

```json
 {
   "John Appleseed":[
      "888-555-5512",
      "888-555-1212"
   ],
   "Daniel Higgins":[
      "555-478-7672",
      "(408) 555-5270",
      "(408) 555-3514"
   ],
   "David Taylor":[
      "555-610-6679"
   ],
   "Hank Zakroff":[
      "(555) 766-4823",
      "(707) 555-1854"
   ]
}
```

---

## Continuer la lecture

- ← Précédent : [API d'icône d'app dynamique](dynamic-app-icon.md)
- Suivant → : [API d'authentification biométrique](biometric-authentication.md)
- Même fonctionnalité sur les autres plateformes : [Android – API Contacts](../android/contacts.md)
- Langues : [🇺🇸 English](../../ios/contacts.md) · [🇩🇪 Deutsch](../../de/ios/contacts.md) · **🇫🇷 Français** · [🇪🇸 Español](../../es/ios/contacts.md) · [🇨🇳 中文](../../zh/ios/contacts.md)

> [!TIP]
> **Trop occupé ? Nous configurons votre app pour vous.** Notre équipe configure, compile & soumet votre app WebViewGold — clé en main, délai rapide, Made in Germany. [Faire configurer mon app →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **Compilez dans votre navigateur :** Pas de Mac, pas d’IDE : le **WebViewGold Cloud Builder** configure, compile & met en ligne votre app. [Découvrir Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
