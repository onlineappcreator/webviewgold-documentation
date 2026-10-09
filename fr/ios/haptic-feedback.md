---
title: "API de retour haptique – Documentation WebViewGold pour iOS"
description: "Déclenchez un retour haptique natif (vibrations) depuis votre application web pour une sensation d'app vraiment native sur iOS."
lang: "fr"
product: "WebViewGold pour iOS"
platform: "iOS"
category: "API et fonctionnalités"
slug: "haptic-feedback"
canonical_url: "https://www.webviewgold.com/fr/docs/iOS/haptic-feedback/"
keywords:
  - "API de retour haptique"
  - "WebViewGold pour iOS"
  - "convertir un site web en app"
  - "documentation d’app WebView"
  - "SDK WebView iOS"
  - "PWA en app"
  - "HTML en app"
  - "pont JavaScript"
last_updated: "2026-10-09"
---

# API de retour haptique – WebViewGold pour iOS

> **Résumé :** Déclenchez un retour haptique natif (vibrations) depuis votre application web pour une sensation d'app vraiment native sur iOS.

[Documentation](../README.md) › [WebViewGold pour iOS](README.md) › API de retour haptique

**Plateforme :** iOS · **Catégorie :** API et fonctionnalités · **Version en ligne :** [www.webviewgold.com/fr/docs/iOS/haptic-feedback/](https://www.webviewgold.com/fr/docs/iOS/haptic-feedback/)

---

**WebViewGold** permet la mise en œuvre du contrôle haptique natif d'iOS au sein de votre application web.
Grâce à notre API, vous pouvez effectuer les actions suivantes :

| Nom | Schéma d'URL | Description |
| --- | --- | --- |
| Impact léger | lighthaptic:// | Utilisé pour une collision entre de petits éléments d'interface légers |
| Impact moyen | mediumhaptic:// | Utilisé pour une collision entre des éléments d'interface de taille modérée |
| Impact fort | heavyhaptic:// | Utilisé pour une collision entre de grands éléments d'interface lourds |
| Notification de succès | successhaptic:// | Indique qu'une tâche ou une action a été menée à bien |
| Notification d'avertissement | warninghaptic:// | Indique qu'une tâche ou une action a généré un avertissement |
| Notification d'erreur | errorhaptic:// | Indique qu'une erreur s'est produite |

Nous vous suggérons de consulter au préalable les [bonnes pratiques](https://developer.apple.com/design/human-interface-guidelines/playing-haptics) d'Apple avant d'intégrer ces fonctionnalités dans votre application.
Un exemple d'utilisation de cette API est illustré ci-dessous, avec une balise d'ancrage et une fonction JavaScript personnalisée qui interagissent avec notre API haptique.

```html
<a onclick="lightHaptic('index.html')">Lien de navigation avec haptique</a>

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

- ← Précédent : [API d'authentification biométrique](biometric-authentication.md)
- Suivant → : [API Shortcut](shortcut.md)
- Même fonctionnalité sur les autres plateformes : [Android – API de retour haptique](../android/haptic-feedback.md)
- Langues : [🇺🇸 English](../../ios/haptic-feedback.md) · [🇩🇪 Deutsch](../../de/ios/haptic-feedback.md) · **🇫🇷 Français** · [🇪🇸 Español](../../es/ios/haptic-feedback.md) · [🇨🇳 中文](../../zh/ios/haptic-feedback.md)

> [!TIP]
> **Trop occupé ? Nous configurons votre app pour vous.** Notre équipe configure, compile & soumet votre app WebViewGold — clé en main, délai rapide, Made in Germany. [Faire configurer mon app →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **Compilez dans votre navigateur :** Pas de Mac, pas d’IDE : le **WebViewGold Cloud Builder** configure, compile & met en ligne votre app. [Découvrir Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
