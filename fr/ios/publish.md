---
title: "Compiler et publier votre app sur l'App Store – Documentation WebViewGold pour iOS"
description: "Publiez votre application WebView sur l'Apple App Store : service de publication complet, processus manuel et modification de l'identifiant de bundle."
lang: "fr"
product: "WebViewGold pour iOS"
platform: "iOS"
category: "Compiler et publier"
slug: "publish"
canonical_url: "https://www.webviewgold.com/fr/docs/iOS/publish/"
keywords:
  - "Compiler et publier"
  - "WebViewGold pour iOS"
  - "convertir un site web en app"
  - "documentation d’app WebView"
  - "SDK WebView iOS"
  - "PWA en app"
  - "HTML en app"
  - "pont JavaScript"
last_updated: "2026-10-09"
---

# Compiler et publier votre app sur l'App Store – WebViewGold pour iOS

> **Résumé :** Publiez votre application WebView sur l'Apple App Store : service de publication complet, processus manuel et modification de l'identifiant de bundle.

[Documentation](../README.md) › [WebViewGold pour iOS](README.md) › Compiler et publier

**Plateforme :** iOS · **Catégorie :** Compiler et publier · **Version en ligne :** [www.webviewgold.com/fr/docs/iOS/publish/](https://www.webviewgold.com/fr/docs/iOS/publish/)

---

Votre application est prête et il est maintenant temps de la mettre en ligne sur l'Apple App Store et d'atteindre un public de millions de personnes ? Passionnant ! La section suivante vous montrera comment procéder — que vous souhaitiez le faire vous-même ou qu'une partie du travail soit effectuée pour vous.

> [!NOTE]
> Vous préférez un flux de travail basé sur le navigateur ? Le [**WebViewGold Cloud Builder**](https://www.webviewgold.com/cloud-builder?ref=ios_docs) (module complémentaire payant) prend en charge la configuration, la compilation et les mises en ligne directement depuis votre navigateur, sans Xcode.
>
> [![Regarder la vidéo: Compiler et publier votre app sur l'App Store](https://img.youtube.com/vi/nzgCkydN9OM/hqdefault.jpg)](https://www.youtube.com/watch?v=nzgCkydN9OM)

## Option A) Service complet de publication d'application

Amener votre application sur l'App Store devrait être simple et sans stress. Offrez-vous un peu d'aide — avec [appsubmitter.io](https://www.appsubmitter.io), vous pouvez profiter d'un **processus de publication pratique et piloté par des experts** — afin que vous puissiez vous concentrer sur ce qui compte le plus pendant que nous nous occupons des détails.

**Pourquoi choisir appsubmitter.io ?**

- **Gagnez du temps** – Nous nous occupons des certificats, des captures d'écran et des mises en ligne.
- **Prise en charge experte** – Votre application est soumise de manière professionnelle, sans tracas.
- **Publiée sous votre compte** – Vous gardez le contrôle total, sans restrictions.
- **Garantie d'approbation** – Si Apple rejette votre application, vous êtes intégralement remboursé (voir [Conditions générales](https://www.onlineappcreator.com/terms.php)).

**Prêt à vous lancer ?** [Réservez un appel vidéo](https://www.appsubmitter.io/order-wizard/?platform=ios) et mettons votre application en ligne !

[![Service de publication sur l'Apple App Store](../../assets/ios/img/apppublishingservice-ios.webp)](https://www.appsubmitter.io)

[![Regarder la vidéo: Compiler et publier votre app sur l'App Store](https://img.youtube.com/vi/3o0xgQXagI8/hqdefault.jpg)](https://www.youtube.com/watch?v=3o0xgQXagI8)

## Option B) Processus de publication manuel

Vous ne souhaitez pas utiliser notre service de soumission sans stress, mais vous préférez vous en charger vous-même ? Bien sûr, suivez ce guide :

Utilisez votre **[abonnement à l'Apple Developer Program](https://developer.apple.com)** pour publier votre application sur l'App Store. Avant la mise en ligne, modifiez le **Bundle Identifier** (également appelé « Bundle ID ») :

[![Regarder la vidéo: Compiler et publier votre app sur l'App Store](https://img.youtube.com/vi/xqChOhStl3Q/hqdefault.jpg)](https://www.youtube.com/watch?v=xqChOhStl3Q)

*Astuce :* Le [**WebViewGold Cloud Builder**](https://www.webviewgold.com/cloud-builder?ref=ios_docs) (module complémentaire payant) gère automatiquement les bundle identifiers et les mises en ligne sur l'App Store, ce qui vous permet d'éviter cette étape.

Répétez ce processus pour chaque target tel que `OneSignalNotificationServiceExtension`, `AppClip` et d'autres extensions. Le bundle identifier de chaque target doit utiliser le bundle ID de votre application principale comme préfixe. Par exemple, si le bundle ID de votre application principale est `com.my.app`, le bundle ID de l'extension d'application OneSignal devrait être `com.my.app.OneSignalNotificationServiceExtension`.

*Veuillez noter que le **Bundle Identifier** et le nom affiché de votre application (le **Product Name**) sont les seuls éléments d'identification que vous devez modifier dans le modèle d'application. Évitez de modifier le Project Name (nommé « WebViewGold » ; c'est le nom qui figure en haut du navigateur de projet dans le panneau gauche de la fenêtre Xcode), car cela peut causer des problèmes. Le Project Name n'est pas visible par les utilisateurs de votre application et n'a pas d'importance dans le processus de soumission de l'application.*

Ajoutez ensuite des textes personnalisés aux détails des autorisations concernant la localisation, l'accès aux photos/à la caméra et tous les autres détails d'API. Supprimez les autorisations dont votre application n'a pas besoin, à l'exception de la clé **Privacy - Tracking Usage Description** (exigée par Apple pour toutes les applications ; supprimer cette clé entraînera le plantage de votre application). Vous trouverez les détails dans le fichier **Info.plist** : \
![Activer ou désactiver les autorisations iOS dans le fichier Info.plist](../../assets/ios/img/infoplist2.webp)\
Ensuite, envisagez une revue professionnelle de l'expérience utilisateur/UX sur [UXreviewer.io](https://www.uxreviewer.io) ou sur des services similaires afin d'obtenir les meilleurs résultats d'approbation par l'App Store. Une telle revue UX vous aide également à améliorer globalement la fidélisation des clients de votre produit grâce à des suggestions d'amélioration.\
Parfait, vous êtes maintenant prêt pour la soumission à l'App Store de votre application web. L'approbation par l'App Store fonctionne dans la plupart des cas sans problème mais dépend fortement du contenu que vous proposez dans votre application, car WebViewGold ne fournit pas de contenu par lui-même. Assurez-vous de soumettre une application utilisant un site web/une application web qui se comporte comme une application mobile (par exemple, en utilisant un **design responsive**). Assurez-vous que le contenu ne contredit pas les exigences légales de l'Apple Developer Program. Utilisez des couleurs de liens différentes des couleurs HTML standard pour une meilleure expérience utilisateur.

Ensuite, suivez les étapes de cette deuxième vidéo :

[![Regarder la vidéo: Compiler et publier votre app sur l'App Store](https://img.youtube.com/vi/YPLs3xrDcm0/hqdefault.jpg)](https://www.youtube.com/watch?v=YPLs3xrDcm0)

**Un complément à la vidéo tutoriel :**
Au minutage 07:00, après la création de l'App Identifier, veillez à activer les deux capacités « App Groups » et « Push Notifications » dans la section App Identifier de l'Apple Developer Portal (choisissez le bon App ID [ici](https://developer.apple.com/account/resources/identifiers/list)). Voir ces captures d'écran : <https://prnt.sc/xz4hg5> & <https://prnt.sc/xz4j01>. Redémarrez ensuite Xcode.

**La mise en ligne sur l'App Store vous demande si vous utilisez le chiffrement ?**
Nous ne fournissons pas de conseils juridiquement contraignants, mais dans la plupart des cas, il faut indiquer « Non » ici. Toutefois, si HTTPS est utilisé, un rapport de sécurité annuel peut devoir être soumis aux autorités américaines. Vous trouverez plus d'informations à ce sujet [ici](https://developer.apple.com/documentation/security/complying_with_encryption_export_regulations).

**La mise en ligne sur l'App Store vous demande si vous utilisez l'Ad ID / IDFA ?**
L'Ad ID est inclus car AdMob est intégré, mais il n'est pas actif par défaut. La suppression du SDK AdMob produira de nombreuses erreurs de dépendance, la suggestion la plus simple serait donc de choisir « Yes » à la question « Does your app use the Ad ID? » et de cocher uniquement la case « Attribute this app installation to a previously served advertisement » (laissez toutes les autres cases vides). Ainsi, si vous utilisez des publicités bannière/interstitielles AdMob dans WebViewGold, configurez cet écran comme [ceci](https://prnt.sc/t8cj0a). Si vous n'utilisez pas de publicités bannière/interstitielles AdMob dans WebViewGold alors que le SDK est toujours intégré (ce qui est le cas typique lorsque vous n'utilisez pas AdMob dans WebViewGold), veuillez sélectionner [ces](https://prnt.sc/t8ci23) options.

Si Apple rejette votre application, utilisez le **Apple Resolution Center** pour expliquer la fonctionnalité de l'application en général (par exemple « Our app enables our existing users to login in/use our products on their handheld device/....). Si Apple rejette toujours votre application, nous pouvons vous offrir un **remboursement intégral** de la licence WebViewGold (à réclamer dans les 14 jours suivant l'achat ; voir [Conditions générales](https://www.onlineappcreator.com/terms.php)). Il vous suffit de nous contacter par e-mail.\
**Félicitations pour votre propre application iOS publiée ! 🎉**\
Pas le temps ou pas envie de signer et de mettre en ligne manuellement ? Envisagez le service [appsubmitter.io](https://www.appsubmitter.io) :\
[![Service de publication sur l'Apple App Store](../../assets/ios/img/apppublishingservice-ios.webp)](https://www.appsubmitter.io)

Bien sûr, après la sortie, il faut d'abord fêter ça ! Mais peut-être que le prochain projet est déjà à l'ordre du jour ? Nos spécialistes en applications sont également ravis de vous accompagner avec des [services de développement personnalisés](https://www.onlineappcreator.com/custom-development-services.php) pour applications web, applications iOS, applications Android, chatbots, idées marketing et bien plus. **[En savoir plus](https://www.onlineappcreator.com/custom-development-services.php)**

---

## Continuer la lecture

- ← Précédent : [Plugin HealthKit](healthkit.md)
- Suivant → : [Crédits et licences](credits.md)
- Même fonctionnalité sur les autres plateformes : [Android – Compiler et publier](../android/publish.md)
- Langues : [🇺🇸 English](../../ios/publish.md) · [🇩🇪 Deutsch](../../de/ios/publish.md) · **🇫🇷 Français** · [🇪🇸 Español](../../es/ios/publish.md) · [🇨🇳 中文](../../zh/ios/publish.md)

> [!TIP]
> **Trop occupé ? Nous configurons votre app pour vous.** Notre équipe configure, compile & soumet votre app WebViewGold — clé en main, délai rapide, Made in Germany. [Faire configurer mon app →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **Compilez dans votre navigateur :** Pas de Mac, pas d’IDE : le **WebViewGold Cloud Builder** configure, compile & met en ligne votre app. [Découvrir Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
