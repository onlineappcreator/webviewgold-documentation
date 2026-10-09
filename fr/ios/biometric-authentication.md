---
title: "API d'authentification biométrique (Face ID / Touch ID) – Documentation WebViewGold pour iOS"
description: "Protégez votre application iOS avec Face ID ou Touch ID et authentifiez les utilisateurs par biométrie depuis votre application web."
lang: "fr"
product: "WebViewGold pour iOS"
platform: "iOS"
category: "API et fonctionnalités"
slug: "biometric-authentication"
canonical_url: "https://www.webviewgold.com/fr/docs/iOS/biometric-authentication/"
keywords:
  - "API d'authentification biométrique"
  - "WebViewGold pour iOS"
  - "convertir un site web en app"
  - "documentation d’app WebView"
  - "SDK WebView iOS"
  - "PWA en app"
  - "HTML en app"
  - "pont JavaScript"
last_updated: "2026-10-09"
---

# API d'authentification biométrique (Face ID / Touch ID) – WebViewGold pour iOS

> **Résumé :** Protégez votre application iOS avec Face ID ou Touch ID et authentifiez les utilisateurs par biométrie depuis votre application web.

[Documentation](../README.md) › [WebViewGold pour iOS](README.md) › API d'authentification biométrique

**Plateforme :** iOS · **Catégorie :** API et fonctionnalités · **Version en ligne :** [www.webviewgold.com/fr/docs/iOS/biometric-authentication/](https://www.webviewgold.com/fr/docs/iOS/biometric-authentication/)

---

**Ceci est une alternative indépendante, plus puissante mais plus complexe, à notre option simple *enableBioMetricAuth* basée sur Config.swift.** Cette API vous permet d'utiliser l'authentification biométrique dans votre application et de renvoyer le résultat via JavaScript à votre site web. L'authentification biométrique inclut Face ID (sur les iPhones plus récents) et Touch ID (sur les iPhones plus anciens) avec le code comme solution de repli. En appelant la commande d'URL « bioauth:// », vous pouvez déclencher l'authentification biométrique nativement dans votre application. Une fois le processus terminé, WebViewGold renverra les résultats à votre application web en appelant l'une des fonctions suivantes :

- **onBioAuthSuccess()**
  - Appelée lorsque le processus d'authentification a réussi.
- **onBioAuthFailure(errorCode, errorMessage)**
  - Appelée lorsque le processus d'authentification échoue et fournit des informations sur l'erreur.
- **onBioAuthUnavailable()**
  - Appelée lorsque l'authentification biométrique s'avère indisponible sur l'appareil.

Pour utiliser cette API, vous devez d'abord ajouter la clé de confidentialité pour l'authentification biométrique Face ID dans votre fichier **Info.plist**. Pour ce faire, ouvrez **Info.plist**, survolez une clé existante, cliquez sur le symbole (+) pour ajouter une nouvelle clé en dessous de celle actuellement sélectionnée, puis sélectionnez l'option de clé « **Privacy - Face ID Usage Description** ». Sans cette clé, l'application ne prendra pas en charge Face ID. La valeur de cette clé est une description présentée à l'utilisateur la première fois que votre application tente d'utiliser Face ID. Cette description doit expliquer clairement pourquoi votre application a besoin d'utiliser Face ID. Voir ci-dessous un exemple de description pour cette clé :

![Exemple de clé de confidentialité Face ID dans Info.plist.](../../assets/ios/img/faceID_key.webp)\
Ensuite, vous devez définir les fonctions suivantes (en JavaScript) dans votre application web pour gérer les résultats d'une authentification biométrique :

```html
<script>

function onBioAuthSuccess() {
    alert("Bio Authentication Succeeded");
}

function onBioAuthFailure(errorCode, errorMessage) {
    // errorCode = Int, errorMessage = String
    alert(`Bio Authentication Failed, ${errorMessage} (code ${errorCode})`);
}

function onBioAuthUnavailable() {
    alert("Bio Authentication Unavailable");
}

</script>
```

Puis, chargez ce type d'URL pour déclencher le processus d'authentification biométrique dans votre application web :

```html
<script>

window.location.href = "bioauth://";

</script>
```

**Avis de sécurité :** Il convient de noter que des utilisateurs malveillants pourraient être en mesure de faire appeler la fonction onBioAuthSuccess() sans avoir complété le processus d'authentification. L'authentification étant un processus sensible, il est recommandé d'ajouter une couche de sécurité supplémentaire dans votre application web, telle qu'une vérification par cookie ou par géolocalisation, afin de garantir l'intégrité de l'authentification. Veuillez consulter votre expert en cybersécurité pour un accompagnement adapté aux besoins de votre application web.

---

## Continuer la lecture

- ← Précédent : [API Contacts](contacts.md)
- Suivant → : [API de retour haptique](haptic-feedback.md)
- Même fonctionnalité sur les autres plateformes : [Android – Biometric Auth API](../android/biometric-auth.md)
- Langues : [🇺🇸 English](../../ios/biometric-authentication.md) · [🇩🇪 Deutsch](../../de/ios/biometric-authentication.md) · **🇫🇷 Français** · [🇪🇸 Español](../../es/ios/biometric-authentication.md) · [🇨🇳 中文](../../zh/ios/biometric-authentication.md)

> [!TIP]
> **Trop occupé ? Nous configurons votre app pour vous.** Notre équipe configure, compile & soumet votre app WebViewGold — clé en main, délai rapide, Made in Germany. [Faire configurer mon app →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **Compilez dans votre navigateur :** Pas de Mac, pas d’IDE : le **WebViewGold Cloud Builder** configure, compile & met en ligne votre app. [Découvrir Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
