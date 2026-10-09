---
title: "Fonction MultiAPICall – Documentation WebViewGold pour iOS"
description: "Enchaînez plusieurs appels d'API WebViewGold en une seule requête grâce à la fonction MultiAPICall pour iOS."
lang: "fr"
product: "WebViewGold pour iOS"
platform: "iOS"
category: "Extensions et plugins"
slug: "multi-api-call"
canonical_url: "https://www.webviewgold.com/fr/docs/iOS/multi-api-call/"
keywords:
  - "Fonction MultiAPICall"
  - "WebViewGold pour iOS"
  - "convertir un site web en app"
  - "documentation d’app WebView"
  - "SDK WebView iOS"
  - "PWA en app"
  - "HTML en app"
  - "pont JavaScript"
last_updated: "2026-10-09"
---

# Fonction MultiAPICall – WebViewGold pour iOS

> **Résumé :** Enchaînez plusieurs appels d'API WebViewGold en une seule requête grâce à la fonction MultiAPICall pour iOS.

[Documentation](../README.md) › [WebViewGold pour iOS](README.md) › Fonction MultiAPICall

**Plateforme :** iOS · **Catégorie :** Extensions et plugins · **Version en ligne :** [www.webviewgold.com/fr/docs/iOS/multi-api-call/](https://www.webviewgold.com/fr/docs/iOS/multi-api-call/)

---

Il s'agit d'une **fonctionnalité facultative pour iOS**, car les navigateurs basés sur Apple traitent les rechargements multiples de page sur un même script différemment des navigateurs basés sur Android.
Cela signifie qu'appeler *window.location.href = "exampleAPItrigger"* plusieurs fois dans le même script de page web ne fonctionnera pas sur iOS, contrairement à Android.\
La fonctionnalité MultiAPICall **vous permet d'appeler plusieurs API dans une seule affectation *window.location.href*** à la fin du script de votre page web. Cela peut vous être utile si vous souhaitez précharger plusieurs fonctionnalités de données depuis l'application, prêtes à être utilisées sur une page.\
**MultiAPICall prend en charge les API de collecte de données suivantes en tant qu'entrées :**
"[get-uuid](uuid.md)", "[user-disable-tracking](user-tracking.md)", "[getonesignalplayerid](push-notifications.md#getonesignalid)", "[getappversion](app-version-check.md)", "[__haptics (light, medium, heavy, success, warning, error)](haptic-feedback.md)"\
Utilisez JavaScript avec ce type d'URL pour appeler plusieurs API à la fois (**veillez à inclure une vérification afin de ne l'utiliser que sur la plateforme iOS**) :

```html
<script>
// Example combination: "getonesignalplayerid" and "getappversion"

if (getMobileOperatingSystem() == "iOS") {
    // iOS: Use MultiAPICall feature, separate API names by commas (","), NO spaces
    window.location.href = "multiapicall://getonesignalplayerid,getappversion";
} else {
    // Android: Can handle multiple calls at once, use normal API call structure
    window.location.href = "getonesignalplayerid://";
    window.location.href = "getappversion://";
}
</script>
```

Cliquez [ici](https://webviewgoldtest.github.io/multiAPI.html) pour consulter une page web de démonstration de cette fonctionnalité. Inspectez la page pour voir l'exemple de code.

---

## Continuer la lecture

- ← Précédent : [Détection de capture d'écran](screen-capture.md)
- Suivant → : [Plugin NFC](nfc.md)
- Même fonctionnalité sur les autres plateformes : [Android – Multi API Call](../android/multi-api-call.md)
- Langues : [🇺🇸 English](../../ios/multi-api-call.md) · [🇩🇪 Deutsch](../../de/ios/multi-api-call.md) · **🇫🇷 Français** · [🇪🇸 Español](../../es/ios/multi-api-call.md) · [🇨🇳 中文](../../zh/ios/multi-api-call.md)

> [!TIP]
> **Trop occupé ? Nous configurons votre app pour vous.** Notre équipe configure, compile & soumet votre app WebViewGold — clé en main, délai rapide, Made in Germany. [Faire configurer mon app →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **Compilez dans votre navigateur :** Pas de Mac, pas d’IDE : le **WebViewGold Cloud Builder** configure, compile & met en ligne votre app. [Découvrir Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
