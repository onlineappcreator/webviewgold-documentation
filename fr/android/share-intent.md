---
title: "API ShareIntent – Documentation WebViewGold pour Android"
description: "Recevez le contenu partagé depuis d'autres applications Android directement dans votre application WebView via les Share Intents."
lang: "fr"
product: "WebViewGold pour Android"
platform: "Android"
category: "API et fonctionnalités"
slug: "share-intent"
canonical_url: "https://www.webviewgold.com/fr/docs/android/share-intent/"
keywords:
  - "API ShareIntent"
  - "WebViewGold pour Android"
  - "convertir un site web en app"
  - "documentation d’app WebView"
  - "SDK WebView Android"
  - "PWA en app"
  - "HTML en app"
  - "pont JavaScript"
last_updated: "2026-10-09"
---

# API ShareIntent – WebViewGold pour Android

> **Résumé :** Recevez le contenu partagé depuis d'autres applications Android directement dans votre application WebView via les Share Intents.

[Documentation](../README.md) › [WebViewGold pour Android](README.md) › API ShareIntent

**Plateforme :** Android · **Catégorie :** API et fonctionnalités · **Version en ligne :** [www.webviewgold.com/fr/docs/android/share-intent/](https://www.webviewgold.com/fr/docs/android/share-intent/)

---

L'**API ShareIntent** de WebViewGold permet à votre application d'apparaître comme cible dans la boîte de dialogue de partage native d'Android. Cela permet aux utilisateurs de partager du contenu tel que du texte, des URL ou des images (sous forme de chaînes base64) depuis n'importe quelle autre application, directement vers votre application basée sur WebView.

## Cas d'usage

- Partager des liens vers des profils utilisateurs, des notes ou des articles directement dans votre application
- Recevoir du contenu depuis des applications de messagerie ou des navigateurs
- Envoyer des images depuis la galerie vers votre interface WebView (encodées en base64)

## Étape 1 : Activer la prise en charge du partage dans AndroidManifest.xml

Pour permettre à votre application de recevoir des données partagées, décommentez les filtres d'intention pertinents dans votre fichier **AndroidManifest.xml** :

```html
<!-- Receive shared text (e.g., URLs or notes) -->
<intent-filter>
    <action android:name="android.intent.action.SEND" />
    <category android:name="android.intent.category.DEFAULT" />
    <data android:mimeType="text/plain" />
</intent-filter>

<!-- Receive a single shared image -->
<intent-filter>
    <action android:name="android.intent.action.SEND" />
    <category android:name="android.intent.category.DEFAULT" />
    <data android:mimeType="image/*" />
</intent-filter>

<!-- Receive multiple shared images -->
<intent-filter>
    <action android:name="android.intent.action.SEND_MULTIPLE" />
    <category android:name="android.intent.category.DEFAULT" />
    <data android:mimeType="image/*" />
</intent-filter>
```

Une fois ces filtres actifs, l'icône de votre application basée sur WebViewGold apparaîtra comme cible de partage chaque fois que les utilisateurs partageront du contenu depuis une autre application.

## Étape 2 : Gérer les données partagées dans votre WebView

Lorsqu'un utilisateur partage du contenu vers votre application, WebViewGold injecte automatiquement le contenu partagé dans une variable JavaScript nommée `sharedData`.

```html
<script>
    alert(sharedData); // Displays the shared content (text or base64 image)

</script>
```

- **Texte ou URL :** transmis sous forme de texte brut dans `sharedData`
- **Image :** convertie en une chaîne encodée en base64 et transmise dans `sharedData`

**Exemple d'utilisation :** Remplir automatiquement un formulaire ou prévisualiser une image en fonction du contenu reçu :

```html
<script>
    if (sharedData) {
        document.getElementById("myInput").value = sharedData;
    }
</script>
```

**Remarque :** Assurez-vous que votre JavaScript est prêt à gérer à la fois du texte brut et de longues chaînes base64. Vous pouvez également mettre en place des vérifications côté client pour distinguer les différents types de contenu.

---

## Continuer la lecture

- ← Précédent : [App Links / Deep Linking](app-links.md)
- Suivant → : [API de dialogue de partage](app-sharing-dialog.md)
- Même fonctionnalité sur les autres plateformes : [iOS – Share Extension](../ios/share-extension.md)
- Langues : [🇺🇸 English](../../android/share-intent.md) · [🇩🇪 Deutsch](../../de/android/share-intent.md) · **🇫🇷 Français** · [🇪🇸 Español](../../es/android/share-intent.md) · [🇨🇳 中文](../../zh/android/share-intent.md)

> [!TIP]
> **Trop occupé ? Nous configurons votre app pour vous.** Notre équipe configure, compile & soumet votre app WebViewGold — clé en main, délai rapide, Made in Germany. [Faire configurer mon app →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_android_doc_online)
>
> **Compilez dans votre navigateur :** Pas de Mac, pas d’IDE : le **WebViewGold Cloud Builder** configure, compile & met en ligne votre app. [Découvrir Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=android_docs)
