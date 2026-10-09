---
title: "API Contacts – Documentation WebViewGold pour Android"
description: "Accédez au carnet d'adresses de l'appareil depuis votre application web : lisez les contacts avec l'autorisation de l'utilisateur dans WebViewGold pour Android."
lang: "fr"
product: "WebViewGold pour Android"
platform: "Android"
category: "API et fonctionnalités"
slug: "contacts"
canonical_url: "https://www.webviewgold.com/fr/docs/android/contacts/"
keywords:
  - "API Contacts"
  - "WebViewGold pour Android"
  - "convertir un site web en app"
  - "documentation d’app WebView"
  - "SDK WebView Android"
  - "PWA en app"
  - "HTML en app"
  - "pont JavaScript"
last_updated: "2026-10-09"
---

# API Contacts – WebViewGold pour Android

> **Résumé :** Accédez au carnet d'adresses de l'appareil depuis votre application web : lisez les contacts avec l'autorisation de l'utilisateur dans WebViewGold pour Android.

[Documentation](../README.md) › [WebViewGold pour Android](README.md) › API Contacts

**Plateforme :** Android · **Catégorie :** API et fonctionnalités · **Version en ligne :** [www.webviewgold.com/fr/docs/android/contacts/](https://www.webviewgold.com/fr/docs/android/contacts/)

---

WebViewGold permet d'exporter les contacts dans une variable JavaScript, au format ci-dessous, via l'API **readcontacts://**. L'objet JSON est stocké dans la variable `contacts`. Pour y accéder, votre application doit d'abord obtenir l'autorisation via l'API **requestcontactpermission://**, qui invitera votre utilisateur à activer les autorisations d'accès aux contacts. Sans cette étape, **readcontacts://** renseignera la variable `contacts` avec une valeur null.\
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

Pour ajouter cette fonctionnalité de contacts, l'autorisation `android.permission.READ_CONTACTS` doit être ajoutée au fichier *AndroidManifest.xml* afin que les utilisateurs puissent l'accorder.

---

## Continuer la lecture

- ← Précédent : [API de vérification de version](app-version-check.md)
- Suivant → : [API d'interface dynamique](dynamic-ui.md)
- Même fonctionnalité sur les autres plateformes : [iOS – API Contacts](../ios/contacts.md)
- Langues : [🇺🇸 English](../../android/contacts.md) · [🇩🇪 Deutsch](../../de/android/contacts.md) · **🇫🇷 Français** · [🇪🇸 Español](../../es/android/contacts.md) · [🇨🇳 中文](../../zh/android/contacts.md)

> [!TIP]
> **Trop occupé ? Nous configurons votre app pour vous.** Notre équipe configure, compile & soumet votre app WebViewGold — clé en main, délai rapide, Made in Germany. [Faire configurer mon app →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_android_doc_online)
>
> **Compilez dans votre navigateur :** Pas de Mac, pas d’IDE : le **WebViewGold Cloud Builder** configure, compile & met en ligne votre app. [Découvrir Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=android_docs)
