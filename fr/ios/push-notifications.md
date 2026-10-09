---
title: "API de notifications push (OneSignal, Firebase, Pushwoosh) – Documentation WebViewGold pour iOS"
description: "Envoyez des notifications push aux utilisateurs de votre application iOS avec OneSignal, Firebase ou Pushwoosh : configuration, deep links et ciblage par utilisateur expliqués."
lang: "fr"
product: "WebViewGold pour iOS"
platform: "iOS"
category: "API et fonctionnalités"
slug: "push-notifications"
canonical_url: "https://www.webviewgold.com/fr/docs/iOS/push-notifications/"
keywords:
  - "API de notifications push"
  - "WebViewGold pour iOS"
  - "convertir un site web en app"
  - "documentation d’app WebView"
  - "SDK WebView iOS"
  - "PWA en app"
  - "HTML en app"
  - "pont JavaScript"
last_updated: "2026-10-09"
---

# API de notifications push (OneSignal, Firebase, Pushwoosh) – WebViewGold pour iOS

> **Résumé :** Envoyez des notifications push aux utilisateurs de votre application iOS avec OneSignal, Firebase ou Pushwoosh : configuration, deep links et ciblage par utilisateur expliqués.

[Documentation](../README.md) › [WebViewGold pour iOS](README.md) › API de notifications push

**Plateforme :** iOS · **Catégorie :** API et fonctionnalités · **Version en ligne :** [www.webviewgold.com/fr/docs/iOS/push-notifications/](https://www.webviewgold.com/fr/docs/iOS/push-notifications/)

---

Les notifications push sont des notifications qui apparaissent sur votre smartphone sans avoir à ouvrir l'application. Ce type de message permet une interaction fantastique avec les clients et les utilisateurs de l'application. Votre application n'a pas besoin d'être ouverte pour recevoir ce genre de notifications. Ainsi, vos clients ne manquent aucune nouvelle ou aucun message important. Les notifications push conviennent à de nombreux cas d'usage, par exemple pour les mises à jour de commandes, les live tickers ou les communautés de réseaux sociaux. Une connexion Internet est nécessaire pour que les utilisateurs de l'application puissent recevoir des messages push. WebViewGold prend en charge plusieurs moyens pour atteindre vos utilisateurs via des notifications push. Si vous ne souhaitez **PAS** utiliser les notifications push, ouvrez **Config.swift** et réglez **askforpushpermissionatfirstrun** sur *false* afin d'éviter que l'application demande à l'utilisateur l'autorisation de notifications.

## Option 1 : Utiliser l'API JavaScript des notifications push locales

Vous pouvez insérer un extrait de code (JavaScript) dans votre site web afin de définir une notification push, qui pourra être affichée **après** la fermeture de votre application (la planification se faisant pendant que l'application est ouverte). Cela fonctionne sans aucune configuration OneSignal.

```html
<script>
var title = "Your cart is waiting!"; //notification title
var message = "You have left a cart full of dreams and deals behind. Dont leave it feeling abandoned"; //notification message
var seconds = 120; //seconds from now on
var url = "https://myshop.org/cart.php"; //deep-linking URL

window.location.href = "sendlocalpushmsg://push.send?s="+ seconds +"=msg!"+ message +"&!#"+ title +"&!#"+ url +"";
</script>
```

Cela peut être utilisé dans différentes situations (comptes à rebours, happy hours, rappels spécifiques, ...).

Pour **annuler** toutes les notifications push locales programmées, exécutez :

```html
<script>
window.location.href = "sendlocalpushmsg://push.send.cancel";
</script>
```

## Vérifier l'état de l'autorisation de notifications native

Appelez `checkNativePushPermissions://` pour vérifier si l'utilisateur a accordé l'autorisation de notifications native d'iOS. Le résultat est injecté dans votre application web sous la forme de la variable JavaScript `nativePushEnabled` (`true` ou `false`) — utile par exemple pour afficher votre propre message avec un lien vers les [réglages de l'application](open-app-settings.md) si les notifications sont désactivées :

```html
<script>
window.location.href = "checkNativePushPermissions://";
setTimeout(function() {
  if (typeof nativePushEnabled !== "undefined" && !nativePushEnabled) {
    // par ex. afficher une bannière avec un lien vers settingsapp://
  }
}, 500);
</script>
```

## Option 2 : Utiliser les notifications push distantes Pushwoosh

**Les utilisateurs de WebViewGold bénéficient de deux mois gratuits de Pushwoosh !**\
Pour profiter de cette offre, veuillez envoyer votre licence WebViewGold par e-mail à [pushwoosh-love@webviewgold.com](mailto:pushwoosh-love@webviewgold.com) et vous recevrez rapidement une réponse personnalisée.

Si vous souhaitez utiliser [Pushwoosh](https://www.pushwoosh.com) (excellent choix !) pour les notifications push dans votre application, activez simplement les options dans **Config.swift** en réglant **kPushwooshEnable** sur **true** et veillez également à mettre à jour **Pushwoosh_APPID** dans le fichier **Info.plist** avec votre propre Application ID Pushwoosh.\
![Envoyez une nouvelle notification push à vos utilisateurs avec Pushwoosh](../../assets/ios/img/pushwoosh1.webp)\
![Envoyez une nouvelle notification push à vos utilisateurs avec Pushwoosh](../../assets/ios/img/pushwoosh2.webp)

Veillez également à finaliser la configuration de Pushwoosh sur leur [site web](https://www.pushwoosh.com), y compris l'importation du certificat.\
Félicitations, votre configuration est déjà terminée. Vous êtes maintenant prêt à envoyer des notifications push :\
[![Envoyez une nouvelle notification push à vos utilisateurs avec Pushwoosh](../../assets/ios/img/pushwoosh3.webp)](https://www.pushwoosh.com)\
Vous souhaitez récupérer **l'identifiant d'appareil de chaque utilisateur** pour des notifications push personnalisées ou un traitement ultérieur ? Il suffit de régler **kPushwooshEnhanceUrl** sur **true** dans **Config.swift** pour ajouter ?pushwoosh_id=XYZ à l'URL de votre WebView :\
![Envoyez une nouvelle notification push à vos utilisateurs avec Pushwoosh](../../assets/ios/img/pushwoosh4.webp)\
Par exemple, si l'URL de votre WebView est https://www.example.org, WebViewGold appellera à la place https://www.example.org?pushwoosh_id=XYZ. Souvenez-vous que seule la première requête d'URL recevra cette variable GET ; veuillez donc l'enregistrer dans une session ou un cookie afin de pouvoir l'utiliser dans vos pages liées. Alternativement ou en complément, vous pouvez **récupérer et traiter cette information sur n'importe quelle page à l'aide de JavaScript** :

```html
<script>
window.location.href = "getpushwooshid://";
alert(pushwooshplayerid);
</script>
```

## Option 3 : Utiliser les notifications push distantes OneSignal

Si vous souhaitez utiliser [OneSignal](https://www.onesignal.com) dans votre application, activez ces options dans **Config.swift** (en passant les valeurs de **false** à **true**) et veillez à remplacer également le paramètre fictif **oneSignalID** par le vôtre. \
![Activez les fonctionnalités OneSignal de WebViewGold pour la prise en charge des notifications push](../../assets/ios/img/onesignal_configs.webp)

Maintenant, [générez](https://documentation.onesignal.com/docs/generate-an-ios-push-certificate) un certificat push iOS et importez-le :\
[![Générez un certificat iOS pour la livraison des notifications push OneSignal](../../assets/ios/img/onesignal_guide_cert.webp)](https://documentation.onesignal.com/docs/generate-an-ios-push-certificate)

Youpi, vous avez **terminé**. Vous pouvez maintenant envoyer des notifications push :\
[![Envoyez une nouvelle notification push aux utilisateurs de votre application](../../assets/ios/img/onesignal_newmsg.webp)](https://www.onesignal.com)\
Si vous souhaitez utiliser le deeplinking d'URL de OneSignal (qui ouvre une URL spécifique lorsque l'on clique sur votre notification), ajoutez l'URL souhaitée dans un champ personnalisé nommé **url** :\
<a id="getonesignalid"></a>![Saisissez une adresse web dans OneSignal pour activer le deeplinking vers votre application WebView](../../assets/ios/img/onesignal_deeplinking.webp)

Dans le backend de OneSignal.com, vous pouvez remplir cette fenêtre clé-valeur après avoir cliqué sur « Advanced settings ». En utilisant l'API OneSignal, vous pouvez ajouter le champ « url » à la requête de l'API (<https://documentation.onesignal.com/docs/onesignal-api>).\
Vous souhaitez récupérer **<a id="onesignalruntime"></a>l'identifiant d'abonnement individuel de chaque utilisateur** sur votre serveur pour un traitement ultérieur et pour envoyer des **messages push individuels** ? Activez simplement l'option **kPushEnhanceUrl** dans Config.swift (en passant la valeur de *false* à *true*) pour ajouter ?onesignal_push_id=XYZ à l'URL de votre WebView. Si l'URL de votre WebView est https://www.example.org, WebViewGold appellera à la place https://www.example.org?onesignal_push_id=XYZ. Seule la première requête d'URL recevra cette variable GET ; veuillez donc l'enregistrer dans une session ou un cookie pour y accéder sur vos pages liées. Une autre approche possible, ou complémentaire, consiste à **récupérer et traiter cette information sur n'importe quelle page via JavaScript** :

```html
<script>
window.location.href = "getonesignalplayerid://";
alert(onesignalplayerid);
</script>
```

**Alternativement, envisagez de passer `autoInjectVariable` à `true` dans Config.swift afin d'injecter automatiquement cette valeur (et d'autres) dans JavaScript sans avoir à appeler une URL au préalable.**

## Option 4 : Utiliser les notifications push distantes Firebase

**Étape 1 : Créer un projet Firebase**\
Commencez par créer un projet Firebase dans votre [Firebase Console](https://console.firebase.google.com/). Ceci est un prérequis pour intégrer Firebase à votre application WebViewGold.\
**Étape 2 : Enregistrer votre application auprès de Firebase**\
Une fois votre projet Firebase prêt, vous pouvez y ajouter votre application WebViewGold en suivant ces étapes :\
a. Naviguez vers la page d'aperçu du projet dans votre console Firebase, puis sélectionnez l'icône iOS pour lancer le processus d'enregistrement de l'application.\
b. Pour ajouter une nouvelle application à votre projet, cliquez sur **Ajouter une application** et sélectionnez les options de plateforme. Lorsque cela vous est demandé, saisissez le bundle ID de votre application dans le champ iOS bundle ID. Cet ID est crucial et peut être trouvé en :
- Ouvrant votre projet d'application dans Xcode.
- Sélectionnant le nom du projet en haut du navigateur pour accéder à l'onglet General.
- Le bundle ID de votre application est indiqué dans le champ Bundle Identifier (par exemple, com.onlineappcreator.webviewgold).\
Assurez-vous de saisir le bundle ID exact utilisé par votre application. Cette valeur est définitive une fois votre application enregistrée auprès de Firebase.\
c. Complétez la configuration en fournissant les informations requises sur l'application, notamment :
- Nom court de l'application : Un identifiant pratique pour votre référence dans la console Firebase.
- App Store ID : Nécessaire pour l'intégration à Firebase Dynamic Links et Google Analytics. Vous pourrez l'ajouter plus tard si votre application n'en dispose pas encore.\
**Étape 3 : Enregistrer votre application**\
Cliquez sur *Enregistrer l'application* pour finaliser le processus d'enregistrement.\
**Étape 4 : Télécharger GoogleService-Info.plist**\
Téléchargez ce fichier de configuration et remplacez le fichier fictif dans votre projet WebViewGold par le fichier GoogleService-Info.plist téléchargé.\
**Étape 5 : Activer Firebase dans WebViewGold**\
Dans le fichier Config.swift, réglez la variable **kFirebasePushEnabled** sur **true** pour activer les fonctionnalités Firebase.\
**Étape 6 : Configurer l'APN et signer votre application**\
Générez une clé APN pour Firebase, téléversez-la, puis signez votre application à l'aide du profil de provisioning Firebase. Pour un guide détaillé, consultez la [documentation Firebase sur les certificats iOS](https://firebase.google.com/docs/cloud-messaging/ios/certs).\
**Étape 7 : Implémenter le deeplinking d'URL (optionnel)**\
Pour prendre en charge le deeplinking d'URL Firebase, ajoutez l'URL cible dans un champ **Custom Data** sous **Additional options (optional)**, avec **Key** = « url » et **Value** = {URL souhaitée}.

![Ajoutez une URL personnalisée pour le deeplinking dans WebView](../../assets/ios/img/firebase_deeplinking.webp)\
Pour vous abonner à un topic Firebase, réglez **firebaseTopic** dans Config.swift sur le nom du topic souhaité.\
Vous souhaitez récupérer **l'identifiant d'abonnement individuel de chaque utilisateur** sur votre serveur pour un traitement ultérieur et pour envoyer des **<a id="firebaseruntime"></a>messages push individuels** ? Activez simplement l'option **kFirebaseEnhanceUrl** dans Config.swift (en passant la valeur de *false* à *true*) pour ajouter ?firebase_push_id=XYZ à l'URL de votre WebView. Si l'URL de votre WebView est https://www.example.org, WebViewGold appellera à la place https://www.example.org?firebase_push_id=XYZ. Seule la PREMIÈRE requête d'URL recevra cette variable GET ; enregistrez-la donc dans une session ou un cookie pour y accéder sur vos pages liées. Une autre approche possible, ou complémentaire, consiste à **récupérer et traiter cette information sur n'importe quelle page via JavaScript** :

```html
<script>
window.location.href = "getfirebaseplayerid://";
alert(firebaseplayerid);
</script>
```

**Alternativement, envisagez de passer `autoInjectVariable` à `true` dans Config.swift afin d'injecter automatiquement cette valeur (et d'autres) dans JavaScript sans avoir à appeler une URL au préalable.**

## Option 5 : Utiliser les notifications push bubble.io

[![Regarder la vidéo: API de notifications push (OneSignal, Firebase, Pushwoosh)](https://img.youtube.com/vi/C0HBXlMSK2E/hqdefault.jpg)](https://www.youtube.com/watch?v=C0HBXlMSK2E)

1. Créez une **application bubble.io**
2. Installez le plugin **[WebViewGold OneSignal Push](https://bubble.io/plugin/webviewgold-onesignal-push-1602240916803x713805488222896100)** :

[![Plugin bubble.io WebViewGold OneSignal Push](../../assets/ios/img/bubblepushplugin-2048x724.webp)](https://bubble.io/plugin/webviewgold-onesignal-push-1602240916803x713805488222896100)
3. Suivez les **instructions OneSignal (voir ci-dessus)** et les **instructions du plugin (voir [ici](https://bubble.io/plugin/webviewgold-onesignal-push-1602240916803x713805488222896100) et [ici](https://www.youtube.com/watch?v=C0HBXlMSK2E))**.

---

## Continuer la lecture

- ← Précédent : [API de géolocalisation](geolocation.md)
- Suivant → : [API AdMob Ads](admob.md)
- Même fonctionnalité sur les autres plateformes : [Android – API de notifications push](../android/push-notifications.md)
- Langues : [🇺🇸 English](../../ios/push-notifications.md) · [🇩🇪 Deutsch](../../de/ios/push-notifications.md) · **🇫🇷 Français** · [🇪🇸 Español](../../es/ios/push-notifications.md) · [🇨🇳 中文](../../zh/ios/push-notifications.md)

> [!TIP]
> **Trop occupé ? Nous configurons votre app pour vous.** Notre équipe configure, compile & soumet votre app WebViewGold — clé en main, délai rapide, Made in Germany. [Faire configurer mon app →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **Compilez dans votre navigateur :** Pas de Mac, pas d’IDE : le **WebViewGold Cloud Builder** configure, compile & met en ligne votre app. [Découvrir Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
