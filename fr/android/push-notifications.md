---
title: "API de notifications push (OneSignal, Firebase, Pushwoosh) – Documentation WebViewGold pour Android"
description: "Envoyez des notifications push aux utilisateurs de votre application Android avec OneSignal, Firebase ou Pushwoosh — configuration, deep links et ciblage par utilisateur expliqués."
lang: "fr"
product: "WebViewGold pour Android"
platform: "Android"
category: "API et fonctionnalités"
slug: "push-notifications"
canonical_url: "https://www.webviewgold.com/fr/docs/android/push-notifications/"
keywords:
  - "API de notifications push"
  - "WebViewGold pour Android"
  - "convertir un site web en app"
  - "documentation d’app WebView"
  - "SDK WebView Android"
  - "PWA en app"
  - "HTML en app"
  - "pont JavaScript"
last_updated: "2026-10-09"
---

# API de notifications push (OneSignal, Firebase, Pushwoosh) – WebViewGold pour Android

> **Résumé :** Envoyez des notifications push aux utilisateurs de votre application Android avec OneSignal, Firebase ou Pushwoosh — configuration, deep links et ciblage par utilisateur expliqués.

[Documentation](../README.md) › [WebViewGold pour Android](README.md) › API de notifications push

**Plateforme :** Android · **Catégorie :** API et fonctionnalités · **Version en ligne :** [www.webviewgold.com/fr/docs/android/push-notifications/](https://www.webviewgold.com/fr/docs/android/push-notifications/)

---

Les notifications push sont des notifications qui apparaissent sur votre smartphone sans avoir à ouvrir l'application. Ce type de message permet une interaction fantastique avec les clients et les utilisateurs de l'application. Votre application n'a pas besoin d'être ouverte. Ainsi, vos clients ne manquent aucune nouvelle ou aucun message important. Les notifications push conviennent à de nombreux cas d'usage, par exemple pour les mises à jour de commandes, les live tickers ou les communautés de réseaux sociaux. Une connexion Internet est nécessaire pour que les utilisateurs de l'application puissent recevoir des messages push. WebViewGold prend en charge plusieurs moyens pour atteindre vos utilisateurs via des notifications push.

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

Cela peut être utilisé dans différentes situations (comptes à rebours, happy hours (comme dans l'exemple de code), rappels, ...).\
Pour annuler toutes les notifications push locales programmées, exécutez :

```html
<script>
window.location.href = "sendlocalpushmsg://push.send.cancel";
</script>
```

## Option 2 : Utiliser les notifications push distantes Pushwoosh

**Les utilisateurs de WebViewGold bénéficient de deux mois gratuits de Pushwoosh !**\
Pour profiter de cette offre, veuillez envoyer votre licence WebViewGold par e-mail à [pushwoosh-love@webviewgold.com](mailto:pushwoosh-love@webviewgold.com) et vous recevrez rapidement une réponse personnalisée.

Si vous souhaitez utiliser [Pushwoosh](https://www.pushwoosh.com) (excellent choix !) pour les notifications push dans votre application, activez simplement les options dans **Config.java** en réglant **PUSHWOOSH_ENABLED** sur **true** et veillez également à mettre à jour les **identifiants Pushwoosh** dans les fichiers **string.xml** et **AndroidManifest.xml** avec vos propres identifiants Pushwoosh :\
![Envoyez une nouvelle notification push à vos utilisateurs avec Pushwoosh](../../assets/android/img/pushwoosh1.webp)\
![Envoyez une nouvelle notification push à vos utilisateurs avec Pushwoosh](../../assets/android/img/pushwoosh2a.webp)\
![Envoyez une nouvelle notification push à vos utilisateurs avec Pushwoosh](../../assets/android/img/pushwoosh2b.webp)

Félicitations, votre configuration est déjà terminée. Vous êtes maintenant prêt à envoyer des notifications push :\
[![Envoyez une nouvelle notification push à vos utilisateurs avec Pushwoosh](../../assets/android/img/pushwoosh3.webp)](https://www.pushwoosh.com)\
Vous souhaitez récupérer **l'identifiant d'appareil de chaque utilisateur** pour des notifications push personnalisées ou un traitement ultérieur ? Il suffit de régler **WONDERPUSH_ENHANCE_WEBVIEW_URL** sur **true** dans **Config.java** pour ajouter ?pushwoosh_id=XYZ à l'URL de votre WebView :\
![Envoyez une nouvelle notification push à vos utilisateurs avec Pushwoosh](../../assets/android/img/pushwoosh4.webp)\
Par exemple, si l'URL de votre WebView est https://www.example.org, WebViewGold appellera à la place https://www.example.org?pushwoosh_id=XYZ. Souvenez-vous que seule la première requête d'URL recevra cette variable GET ; veuillez donc l'enregistrer dans une session ou un cookie afin de pouvoir l'utiliser dans vos pages liées. Alternativement ou en complément, vous pouvez **récupérer et traiter cette information sur n'importe quelle page à l'aide de JavaScript** :

```html
<script>
window.location.href = "getpushwooshid://";
alert(pushwooshplayerid);
</script>
```

## Option 3 : Utiliser les notifications push distantes OneSignal

Si vous souhaitez utiliser OneSignal pour configurer des notifications push distantes, ce tutoriel vidéo vous guidera pas à pas tout au long du processus.

[![Regarder la vidéo: API de notifications push (OneSignal, Firebase, Pushwoosh)](https://img.youtube.com/vi/0cPNGqMQVm0/hqdefault.jpg)](https://www.youtube.com/watch?v=0cPNGqMQVm0)

Après avoir terminé ce tutoriel vidéo, vous pourrez configurer facilement les notifications push distantes pour votre application mobile à l'aide de OneSignal. Cela vous permettra d'envoyer des mises à jour importantes, des rappels ou des contenus promotionnels directement sur les appareils de vos utilisateurs, même s'ils n'utilisent pas votre application à ce moment-là.

En résumé, la procédure pour configurer OneSignal pour les notifications push est la suivante :

1. Ouvrez Android Studio et repérez les options OneSignal. Par défaut, PUSH_ENABLE, PUSH_ENHANCE_WEBVIEW_URL et PUSH_RELOAD_ON_USERID sont réglés sur false ; passez-les à true.
2. Ouvrez votre compte OneSignal et sélectionnez votre organisation et le nom de votre application.

***Si vous n'avez pas encore créé votre application dans le projet OneSignal, suivez d'abord ces étapes.***

[![Regarder la vidéo: API de notifications push (OneSignal, Firebase, Pushwoosh)](https://img.youtube.com/vi/X9jepbGFw7A/hqdefault.jpg)](https://www.youtube.com/watch?v=X9jepbGFw7A)

***Notez que pour créer et configurer votre compte OneSignal, vous aurez besoin d'un fichier JSON. Pour obtenir ce fichier, vous devez avoir configuré votre compte Firebase. Si votre compte Firebase n'est pas encore configuré pour obtenir le fichier JSON, consultez ce tutoriel complémentaire.***

[![Regarder la vidéo: API de notifications push (OneSignal, Firebase, Pushwoosh)](https://img.youtube.com/vi/qAqdhcd3ngs/hqdefault.jpg)](https://www.youtube.com/watch?v=qAqdhcd3ngs)

- Une fois votre application OneSignal créée, allez dans la section des paramètres et sélectionnez Native Android comme plateforme, puis copiez le code d'App ID obtenu.
- Ouvrez Android Studio et allez dans la section Gradle Scripts et sélectionnez build.gradle (Module:app).
- Dans la section ONE_SIGNAL_APP_ID, collez le code que vous avez copié depuis OneSignal.
- Ensuite, générez votre fichier *APK* et exécutez-le sur un appareil physique.
- Allez sur OneSignal et, dans votre projet d'application, sélectionnez *New Message* puis cliquez sur *New Push*.
- Remplissez les informations requises et c'est terminé ! Vous avez testé vos messages push OneSignal.

Remplacez **ic_stat_onesignal_default.png** pour remplacer **l'icône cloche de secours par défaut** des notifications push OneSignal. \
Vous souhaitez récupérer **l'identifiant d'abonnement individuel de chaque utilisateur** sur votre serveur pour un traitement ultérieur et pour envoyer des **<a id="firebaseruntime"></a>messages push individuels** ? Activez simplement l'option **PUSH_ENHANCE_WEBVIEW_URL** dans Config.java (en passant la valeur de false à true) pour ajouter ?onesignal_push_id=XYZ à l'URL de votre WebView. Si l'URL de votre WebView est https://www.example.org, WebViewGold appellera à la place https://www.example.org?onesignal_push_id=XYZ. Seule la PREMIÈRE requête d'URL recevra cette variable GET ; enregistrez-la donc dans une session ou un cookie pour y accéder sur vos pages liées. Une autre approche possible, ou complémentaire, consiste à **récupérer et traiter cette information sur n'importe quelle page via JavaScript** :

```html
<script>
window.location.href = "getonesignalplayerid://";
alert(onesignalplayerid);
</script>
```

**Alternativement, envisagez de passer  `AUTO_INJECT_VARIABLES`  à `true` dans Config.java afin d'injecter automatiquement cette valeur (et d'autres) dans JavaScript sans avoir à appeler une URL au préalable.**

## Option 4 : Utiliser les notifications push distantes Firebase

Si vous souhaitez utiliser Firebase pour configurer des notifications push distantes, ce tutoriel vidéo vous guidera pas à pas tout au long du processus.

[![Regarder la vidéo: API de notifications push (OneSignal, Firebase, Pushwoosh)](https://img.youtube.com/vi/X-02iJSBaAQ/hqdefault.jpg)](https://www.youtube.com/watch?v=X-02iJSBaAQ)

En résumé, la procédure pour configurer Firebase pour les notifications push est la suivante :

### 1. Renommer le nom du package et créer un projet Firebase

Veuillez [renommer le nom du package](publish.md#renamepackagename) de votre application Android WebViewGold. Ensuite, vous devez créer un projet Firebase dans votre [Firebase Console](https://console.firebase.google.com/).

### 2. Activer Firebase dans WebViewGold

Dans Android Studio, allez dans le fichier Config.java et passez la variable **FIREBASE_PUSH_ENABLED** à **true**.

![Remplacez google-services.json dans votre application Android WebViewGold](../../assets/android/img/firebase2.webp)

### 3. Enregistrer votre application auprès de Firebase

Après avoir créé votre projet Firebase, vous pouvez y ajouter votre application WebViewGold.

a. Sur la page d'aperçu du projet dans la console Firebase, cliquez sur l'icône Android pour lancer le processus de configuration.

b. Si vous avez déjà ajouté une application à votre projet Firebase, cliquez sur **Ajouter une application** pour afficher les options de plateforme.
Saisissez le nom du package de votre application tel qu'il a été modifié/défini [à cette étape](publish.md).
Assurez-vous de saisir le nom de package utilisé par votre application. Vous ne pouvez ni ajouter ni modifier cette valeur après l'enregistrement de votre application auprès de votre projet Firebase.\
**4. Cliquez sur le bouton *Enregistrer l'application*.**
**5. Téléchargez google-services.json**
Cliquez sur « Télécharger google-services.json » pour obtenir votre fichier de configuration Firebase Android (google-services.json) et remplacez le fichier exemple déjà inclus dans le projet WebViewGold à l'aide du Finder de Mac ou de l'Explorateur Windows :\
![Remplacez google-services.json dans votre application Android WebViewGold](../../assets/android/img/firebase1.webp)\
 **C'est tout !**\
Si vous souhaitez utiliser le deeplinking d'URL Firebase (qui ouvre une URL spécifique lorsque l'on clique sur votre notification), veuillez ajouter l'URL souhaitée dans un champ **Custom Data** (dans la section **Additional options (optional)**) avec **Key** = « url » et **Value** = {l'URL souhaitée}.\
![Ajoutez une URL personnalisée pour le deeplinking dans WebView](../../assets/android/img/firebase_deeplinking.webp)\
Vous souhaitez récupérer **l'identifiant d'abonnement individuel de chaque utilisateur** sur votre serveur pour un traitement ultérieur et pour envoyer des **messages push individuels** ? Activez simplement l'option **FIREBASE_PUSH_ENHANCE_WEBVIEW_URL** dans Config.java (en passant la valeur de false à true) pour ajouter ?firebase_push_id=XYZ à l'URL de votre WebView. Si l'URL de votre WebView est https://www.example.org, WebViewGold appellera à la place https://www.example.org?firebase_push_id=XYZ. Seule la PREMIÈRE requête d'URL recevra cette variable GET ; enregistrez-la donc dans une session ou un cookie pour y accéder sur vos pages liées. Une autre approche possible, ou complémentaire, consiste à **récupérer et traiter cette information sur n'importe quelle page via JavaScript** :

```html
<script>
window.location.href = "getfirebaseplayerid://";
alert(firebaseplayerid);
</script>
```

**Alternativement, envisagez de passer  `AUTO_INJECT_VARIABLES`  à `true` dans Config.java afin d'injecter automatiquement cette valeur (et d'autres) dans JavaScript sans avoir à appeler une URL au préalable.**

## Option 5 : Utiliser les notifications push bubble.io

[![Regarder la vidéo: API de notifications push (OneSignal, Firebase, Pushwoosh)](https://img.youtube.com/vi/C0HBXlMSK2E/hqdefault.jpg)](https://www.youtube.com/watch?v=C0HBXlMSK2E)

1. Créez une **application bubble.io**
2. Installez le plugin **[WebViewGold OneSignal Push](https://bubble.io/plugin/webviewgold-onesignal-push-1602240916803x713805488222896100)** :

[![Plugin bubble.io WebViewGold OneSignal Push](../../assets/android/img/bubblepushplugin-2048x724.webp)](https://bubble.io/plugin/webviewgold-onesignal-push-1602240916803x713805488222896100)
3. Suivez les **instructions OneSignal (voir ci-dessus)** et les **instructions du plugin (voir [ici](https://bubble.io/plugin/webviewgold-onesignal-push-1602240916803x713805488222896100) et [ici](https://www.youtube.com/watch?v=C0HBXlMSK2E))**.

---

## APIs de permission push : Demander au bon moment et vérifier le statut actuel

### Demander manuellement la permission de notifications push (`registerpush://`)

Par défaut, WebViewGold demande à l'utilisateur la permission de notifications push au premier lancement de l'application (`requirePush = true` dans **Config.java**). Les demandes de permission convertissent bien mieux lorsqu'elles apparaissent dans le bon contexte — vous pouvez donc aussi définir `requirePush` sur `false` et déclencher la boîte de dialogue native de permission depuis votre web app au moment idéal (p. ex. après la connexion ou l'onboarding) :

```html
<a href="registerpush://">Activer les notifications</a>
```

```javascript
window.location.href = "registerpush://";
```

**Remarque :** Cela nécessite qu'au moins un service push soit activé dans **Config.java** (`PUSH_ENABLED`, `FIREBASE_PUSH_ENABLED` ou `PUSHWOOSH_ENABLED`).

### Vérifier le statut actuel de la permission push (`checkNativePushPermissions://`)

Pour savoir si l'utilisateur autorise actuellement les notifications push, appelez :

```javascript
window.location.href = "checkNativePushPermissions://";
```

WebViewGold injecte alors la variable JavaScript `nativePushEnabled` (`true` ou `false`) dans votre page. Sous Android 13 et versions ultérieures, le réglage système des notifications et la permission d'exécution `POST_NOTIFICATIONS` doivent tous deux être accordés pour que la valeur soit `true`. Exemple :

```html
<script>
window.location.href = "checkNativePushPermissions://";
setTimeout(function () {
    if (typeof nativePushEnabled !== "undefined" && nativePushEnabled) {
        console.log("Les notifications push sont activées");
    } else {
        // p. ex. afficher votre propre message et proposer registerpush:// ou settingsapp://
    }
}, 500);
</script>
```

Si la permission a été refusée définitivement, vous pouvez guider l'utilisateur vers les réglages système via l'[API Open App Settings](open-app-settings.md) (`settingsapp://`).

---

## Continuer la lecture

- ← Précédent : [API de géolocalisation](geolocation.md)
- Suivant → : [API AdMob](admob.md)
- Même fonctionnalité sur les autres plateformes : [iOS – API de notifications push](../ios/push-notifications.md)
- Langues : [🇺🇸 English](../../android/push-notifications.md) · [🇩🇪 Deutsch](../../de/android/push-notifications.md) · **🇫🇷 Français** · [🇪🇸 Español](../../es/android/push-notifications.md) · [🇨🇳 中文](../../zh/android/push-notifications.md)

> [!TIP]
> **Trop occupé ? Nous configurons votre app pour vous.** Notre équipe configure, compile & soumet votre app WebViewGold — clé en main, délai rapide, Made in Germany. [Faire configurer mon app →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_android_doc_online)
>
> **Compilez dans votre navigateur :** Pas de Mac, pas d’IDE : le **WebViewGold Cloud Builder** configure, compile & met en ligne votre app. [Découvrir Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=android_docs)
