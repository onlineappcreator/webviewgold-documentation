---
title: "API de retour haptique – Documentation WebViewGold pour Android"
description: "Déclenchez un retour haptique par vibration native depuis votre application web pour une sensation d'application native sous Android."
lang: "fr"
product: "WebViewGold pour Android"
platform: "Android"
category: "API et fonctionnalités"
slug: "haptic-feedback"
canonical_url: "https://www.webviewgold.com/fr/docs/android/haptic-feedback/"
keywords:
  - "API de retour haptique"
  - "WebViewGold pour Android"
  - "convertir un site web en app"
  - "documentation d’app WebView"
  - "SDK WebView Android"
  - "PWA en app"
  - "HTML en app"
  - "pont JavaScript"
last_updated: "2026-10-09"
---

# API de retour haptique – WebViewGold pour Android

> **Résumé :** Déclenchez un retour haptique par vibration native depuis votre application web pour une sensation d'application native sous Android.

[Documentation](../README.md) › [WebViewGold pour Android](README.md) › API de retour haptique

**Plateforme :** Android · **Catégorie :** API et fonctionnalités · **Version en ligne :** [www.webviewgold.com/fr/docs/android/haptic-feedback/](https://www.webviewgold.com/fr/docs/android/haptic-feedback/)

---

**WebViewGold** permet la mise en œuvre d'un contrôle haptique Android natif au sein de votre application web.
Grâce à notre API, vous pouvez effectuer les actions suivantes :

| Nom | Schéma d'URL | Description |
| --- | --- | --- |
| Impact léger | lighthaptic:// | Utilisé pour une collision entre de petits éléments d'interface légers |
| Impact fort | heavyhaptic:// | Utilisé pour une collision entre de grands éléments d'interface lourds |
| Notification de succès | successhaptic:// | Indique qu'une tâche ou une action a été effectuée avec succès |
| Notification d'avertissement | warninghaptic:// | Indique qu'une tâche ou une action a produit un avertissement quelconque |
| Notification d'erreur | errorhaptic:// | Indique qu'une erreur s'est produite |

Un exemple d'utilisation de cette API est présenté ci-dessous, avec une balise d'ancrage et une fonction JavaScript personnalisée qui interagissent avec notre API haptique.

```html
<a onclick="lightHaptic('index.html')">Navigation Link with Haptics</a>

<script>
function lightHaptic(url) {
  if (isWebViewBrowser) {
    window.location.href = url;
    loadInnerHref("lighthaptic://");
  } else {
    window.location.href = url;
  }
}

function loadInnerHref(url) {
  iFrame = document.createElement("iframe");
  iFrame.setAttribute("src", url);
  document.body.appendChild(iFrame);
  iFrame.parentNode.removeChild(iFrame);
  iFrame = null;
}
</script>
```

Cliquez [ici](https://webviewgoldtest.github.io/hapticFeedback.html) pour consulter une page web de démonstration de cette fonctionnalité. Inspectez la page pour voir l'exemple de code.

---

## Continuer la lecture

- ← Précédent : [API d'interface dynamique](dynamic-ui.md)
- Suivant → : [Plugin NFC](nfc.md)
- Même fonctionnalité sur les autres plateformes : [iOS – API de retour haptique](../ios/haptic-feedback.md)
- Langues : [🇺🇸 English](../../android/haptic-feedback.md) · [🇩🇪 Deutsch](../../de/android/haptic-feedback.md) · **🇫🇷 Français** · [🇪🇸 Español](../../es/android/haptic-feedback.md) · [🇨🇳 中文](../../zh/android/haptic-feedback.md)

> [!TIP]
> **Trop occupé ? Nous configurons votre app pour vous.** Notre équipe configure, compile & soumet votre app WebViewGold — clé en main, délai rapide, Made in Germany. [Faire configurer mon app →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_android_doc_online)
>
> **Compilez dans votre navigateur :** Pas de Mac, pas d’IDE : le **WebViewGold Cloud Builder** configure, compile & met en ligne votre app. [Découvrir Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=android_docs)
