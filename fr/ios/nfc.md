---
title: "Plugin NFC – Documentation WebViewGold pour iOS"
description: "Lisez les tags NFC nativement dans votre application WebView iOS et transmettez les données du tag à votre application web."
lang: "fr"
product: "WebViewGold pour iOS"
platform: "iOS"
category: "Extensions et plugins"
slug: "nfc"
canonical_url: "https://www.webviewgold.com/fr/docs/iOS/nfc/"
keywords:
  - "Plugin NFC"
  - "WebViewGold pour iOS"
  - "convertir un site web en app"
  - "documentation d’app WebView"
  - "SDK WebView iOS"
  - "PWA en app"
  - "HTML en app"
  - "pont JavaScript"
last_updated: "2026-10-09"
---

# Plugin NFC – WebViewGold pour iOS

> **Résumé :** Lisez les tags NFC nativement dans votre application WebView iOS et transmettez les données du tag à votre application web.

[Documentation](../README.md) › [WebViewGold pour iOS](README.md) › Plugin NFC

**Plateforme :** iOS · **Catégorie :** Extensions et plugins · **Version en ligne :** [www.webviewgold.com/fr/docs/iOS/nfc/](https://www.webviewgold.com/fr/docs/iOS/nfc/)

---

La technologie **Near-Field Communication (NFC)** est l'une des technologies les plus récentes à être devenue très populaire auprès des utilisateurs mobiles. Elle permet à deux appareils, ou à un appareil et un tag NFC, de communiquer sans fil lorsqu'ils sont à proximité immédiate. NFC est largement utilisé sur les appareils iOS pour lire et écrire de petites quantités de données, ce qui en fait un outil efficace pour partager des informations via des cartes ou des tags compatibles NFC.

L'API NFC permet aux développeurs de lire et d'écrire des données sur des tags NFC directement depuis le code de l'application. Cela ouvre de nouvelles possibilités d'interaction entre les applications et les utilisateurs, du partage de coordonnées à l'intégration de fragments de texte.

## Intégration du plugin NFC de WebViewGold

Bien que le NFC ne fasse pas partie du périmètre général des fonctionnalités de WebViewGold, nous proposons, au cas par cas, une intégration personnalisée et simple du plugin NFC de WebViewGold (via JavaScript).

Veuillez nous faire part de vos besoins (par exemple, l'écriture/la lecture de fragments de texte et/ou de coordonnées de cartes de visite vers/depuis des tags NFC) par e-mail à l'adresse [webviewgold-nfc@onlineappcreator.com](mailto:webviewgold-nfc@onlineappcreator.com) pour une consultation gratuite et un devis sans engagement.

**Écriture**\
Pour écrire une valeur sur un tag NFC, envoyez une commande depuis votre application web en chargeant l'URL suivante : `writenfc://?value=data`\
Exemple :\
`<a href="writenfc://?value=WebViewGold.com"> Write to an NFC tag </a>`\
Cela fait passer votre application en mode Écriture et stocke la valeur jusqu'à ce qu'un tag soit scanné.

**Écriture dans une VCARD**\
Utilisez la même API que pour l'écriture de texte brut. Formatez le texte de la manière suivante :

```
VCARD
FN:John Doe
Title:Developer
TEL;TYPE=CELL:0452641211
_
_
_
```

Séparez les propriétés par un trait de soulignement (`_`) et préfixez le texte par `VCARD_`. Consultez <https://en.wikipedia.org/wiki/VCard#Properties> pour obtenir la liste des propriétés prises en charge.

**Lecture**\
Pour lire un tag NFC, chargez `readnfc://`. L'application renverra les informations à votre application web en appelant `readNFCResult(data, id, tag)`, où `data` est la valeur stockée, `id` l'identifiant du tag et `tag` le type de tag. Définissez cette fonction JavaScript dans votre application web pour traiter ces valeurs.

## Comment tester l'API

1. Ouvrez le fichier Config de la base de code de votre application.
2. Saisissez votre code d'achat.
3. Définissez l'URL de l'application sur la page de test de l'API NFC : <https://webviewgoldtest.github.io/NFCtesting.html>
4. Lancez l'application.
5. Appuyez sur l'une des options Lecture ou Écriture pour activer le mode correspondant. En cas d'écriture, saisissez une valeur.
6. Approchez le tag NFC de l'appareil pour terminer l'opération de lecture ou d'écriture. La page de test et l'application afficheront les résultats.

---

## Continuer la lecture

- ← Précédent : [Fonction MultiAPICall](multi-api-call.md)
- Suivant → : [Plugin Siri](siri.md)
- Même fonctionnalité sur les autres plateformes : [Android – Plugin NFC](../android/nfc.md)
- Langues : [🇺🇸 English](../../ios/nfc.md) · [🇩🇪 Deutsch](../../de/ios/nfc.md) · **🇫🇷 Français** · [🇪🇸 Español](../../es/ios/nfc.md) · [🇨🇳 中文](../../zh/ios/nfc.md)

> [!TIP]
> **Trop occupé ? Nous configurons votre app pour vous.** Notre équipe configure, compile & soumet votre app WebViewGold — clé en main, délai rapide, Made in Germany. [Faire configurer mon app →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **Compilez dans votre navigateur :** Pas de Mac, pas d’IDE : le **WebViewGold Cloud Builder** configure, compile & met en ligne votre app. [Découvrir Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
