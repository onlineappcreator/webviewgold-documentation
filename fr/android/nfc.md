---
title: "Plugin NFC – Documentation WebViewGold pour Android"
description: "Lisez les tags NFC nativement dans votre application Android WebView et transmettez les données du tag à votre application web."
lang: "fr"
product: "WebViewGold pour Android"
platform: "Android"
category: "API et fonctionnalités"
slug: "nfc"
canonical_url: "https://www.webviewgold.com/fr/docs/android/nfc/"
keywords:
  - "Plugin NFC"
  - "WebViewGold pour Android"
  - "convertir un site web en app"
  - "documentation d’app WebView"
  - "SDK WebView Android"
  - "PWA en app"
  - "HTML en app"
  - "pont JavaScript"
last_updated: "2026-10-09"
---

# Plugin NFC – WebViewGold pour Android

> **Résumé :** Lisez les tags NFC nativement dans votre application Android WebView et transmettez les données du tag à votre application web.

[Documentation](../README.md) › [WebViewGold pour Android](README.md) › Plugin NFC

**Plateforme :** Android · **Catégorie :** API et fonctionnalités · **Version en ligne :** [www.webviewgold.com/fr/docs/android/nfc/](https://www.webviewgold.com/fr/docs/android/nfc/)

---

La **communication en champ proche (NFC)** permet à deux appareils, ou à un appareil et un tag NFC, de communiquer sans fil lorsqu'ils sont à proximité. Le NFC est largement utilisé sur les appareils Android pour lire et écrire de petites quantités de données, ce qui en fait un outil efficace pour partager des informations via des cartes ou tags compatibles NFC.

L'**API NFC de WebViewGold** permet à votre web app de lire et d'écrire des tags NFC directement via un pont JavaScript — du partage d'informations de contact à l'intégration d'extraits de texte.

**Écriture**\
Pour écrire une valeur sur un tag NFC, envoyez une commande depuis votre web app en chargeant l'URL suivante : `writenfc://?value=data`\
Exemple :\
`<a href="writenfc://?value=WebViewGold.com"> Écrire sur un tag NFC </a>`\
Cela met votre application en mode écriture et mémorise la valeur jusqu'à ce qu'un tag soit scanné : dès que l'utilisateur approche un tag NFC de l'appareil, la valeur y est écrite.

**Écrire une VCARD (carte de visite)**\
Utilisez la même API que pour l'écriture de texte brut et formatez le texte ainsi :

```
VCARD
FN:John Doe
Title:Developer
TEL;TYPE=CELL:0452641211
```

Séparez les propriétés par un tiret bas (`_`), encodez les espaces avec `%20` et préfixez le texte par `VCARD_`. Exemple :

```
writenfc://?value=VCARD_FN:John%20Doe_Title:Developer_TEL;TYPE=CELL:0452641211
```

Consultez <https://en.wikipedia.org/wiki/VCard#Properties> pour la liste des propriétés prises en charge.

**Lecture**\
Pour lire un tag NFC, chargez `readnfc://`. Cela met votre application en mode lecture. Lorsque l'utilisateur scanne un tag, l'application renvoie les informations stockées à votre web app en appelant la fonction JavaScript `readNFCResult(data)`, où `data` est la valeur enregistrée sur le tag. Définissez cette fonction JavaScript dans votre web app pour traiter la valeur :

```html
<script>
window.location.href = "readnfc://";

function readNFCResult(data) {
    alert("Contenu du tag NFC : " + data);
}
</script>
```

## Comment tester l'API

1. Ouvrez le fichier Config du code de votre application.
2. Saisissez votre code d'achat.
3. Définissez l'URL de l'application sur la page de test de l'API NFC : <https://webviewgoldtest.github.io/NFCtesting.html>
4. Lancez l'application sur un appareil physique compatible NFC.
5. Appuyez sur l'une des options de lecture ou d'écriture pour activer le mode correspondant. En cas d'écriture, saisissez une valeur.
6. Approchez le tag NFC de l'appareil pour terminer l'opération de lecture ou d'écriture. La page de test et l'application afficheront les résultats.

**Besoin de plus ?** Si vous avez besoin de fonctionnalités NFC étendues au-delà de cette API (p. ex. types de tags spéciaux ou formats de données personnalisés), nous proposons des intégrations de plugin NFC sur mesure au cas par cas. Envoyez-nous vos besoins par e-mail à [webviewgold-nfc@onlineappcreator.com](mailto:webviewgold-nfc@onlineappcreator.com) pour une consultation gratuite et un devis sans engagement.

---

## Continuer la lecture

- ← Précédent : [API de retour haptique](haptic-feedback.md)
- Suivant → : [Open App Settings API](open-app-settings.md)
- Même fonctionnalité sur les autres plateformes : [iOS – Plugin NFC](../ios/nfc.md)
- Langues : [🇺🇸 English](../../android/nfc.md) · [🇩🇪 Deutsch](../../de/android/nfc.md) · **🇫🇷 Français** · [🇪🇸 Español](../../es/android/nfc.md) · [🇨🇳 中文](../../zh/android/nfc.md)

> [!TIP]
> **Trop occupé ? Nous configurons votre app pour vous.** Notre équipe configure, compile & soumet votre app WebViewGold — clé en main, délai rapide, Made in Germany. [Faire configurer mon app →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_android_doc_online)
>
> **Compilez dans votre navigateur :** Pas de Mac, pas d’IDE : le **WebViewGold Cloud Builder** configure, compile & met en ligne votre app. [Découvrir Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=android_docs)
