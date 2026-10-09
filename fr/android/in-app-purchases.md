---
title: "API d'achats intégrés – Documentation WebViewGold pour Android"
description: "Vendez des biens numériques et des abonnements dans votre application Android WebView avec Google Play Billing."
lang: "fr"
product: "WebViewGold pour Android"
platform: "Android"
category: "API et fonctionnalités"
slug: "in-app-purchases"
canonical_url: "https://www.webviewgold.com/fr/docs/android/in-app-purchases/"
keywords:
  - "API d'achats intégrés"
  - "WebViewGold pour Android"
  - "convertir un site web en app"
  - "documentation d’app WebView"
  - "SDK WebView Android"
  - "PWA en app"
  - "HTML en app"
  - "pont JavaScript"
last_updated: "2026-10-09"
---

# API d'achats intégrés – WebViewGold pour Android

> **Résumé :** Vendez des biens numériques et des abonnements dans votre application Android WebView avec Google Play Billing.

[Documentation](../README.md) › [WebViewGold pour Android](README.md) › API d'achats intégrés

**Plateforme :** Android · **Catégorie :** API et fonctionnalités · **Version en ligne :** [www.webviewgold.com/fr/docs/android/in-app-purchases/](https://www.webviewgold.com/fr/docs/android/in-app-purchases/)

---

Dans certaines applications, vous pouvez acheter des contenus ou services supplémentaires. Ce type d'achats est appelé « achats intégrés ». Ils peuvent constituer une source de revenus attrayante pour les développeurs et sont très pratiques pour les clients, car ils utilisent les comptes et moyens de paiement existants pour le règlement. WebViewGold permet de déclencher des achats intégrés Google Play. Assurez-vous de posséder une [licence étendue](credits.md) de WebViewGold si vous prévoyez d'utiliser cette fonctionnalité dans un produit final. Besoin d'une mise à niveau ? [Découvrez ici comment effectuer la mise à niveau](https://help.market.envato.com/hc/en-us/articles/115005593503-If-I-choose-the-wrong-license-or-need-to-upgrade-my-license-how-easy-is-it-to-change-to-the-correct-license).

**Option 1 (par défaut) : RevenueCat**\
Créez votre [compte RevenueCat](https://tinyurl.com/register-revenuecat) gratuit pour commencer. Les informations tarifaires sont disponibles sur leur site web. Configurez ensuite RevenueCat en suivant leurs assistants de configuration et leur documentation (les détails tarifaires sont disponibles sur leur [site web](https://tinyurl.com/register-revenuecat)). Ajoutez ensuite vos informations dans **Config.java**. Cette approche prend également en charge le [15% Service Fee Tier Program](https://support.google.com/googleplay/android-developer/answer/112622?hl=en) du Google Play Store et le [Small Business Program](https://developer.apple.com/app-store/small-business-program/) d'Apple. Si vous participez à ces programmes à frais réduits, informez-en RevenueCat via leurs pages [Apple Small Business Program](https://www.revenuecat.com/docs/platform-resources/apple-platform-resources/app-store-small-business-program) ou [Google 15% reduced service fee](https://www.revenuecat.com/docs/platform-resources/google-platform-resources/15-reduced-service-fee). Voici à quoi ressemble la configuration dans Config.java :

```java
public static final String REVENUECAT_API_KEY = "xxxxxxxsxxxxxxxxxxxxxxxxxxxxxxxxxx"; //Your RevenueCat API Key (sign up via tinyurl.com/register-revenuecat first, then follow tinyurl.com/api-key-revenuecat how to find it)
public static final String REVENUECAT_PROJECT_ID = "xxxxxxx"; //Your RevenueCat Project ID (sign up via tinyurl.com/register-revenuecat first, then follow tinyurl.com/project-id-revenuecat how to find it)
```

Assurez-vous que le nom de package de votre APK et de la Google Play Console correspond au projet configuré dans RevenueCat. Déclenchez un achat ou un abonnement à l'aide de :

```
revenuecat://purchase?external_id=user_123&product=sub_30_days
```

`external_id` = identifiant utilisateur, par exemple l'e-mail du client ou son identifiant utilisateur. `product` = identifiant affiché dans la console RevenueCat. Fonctionne à la fois pour Android et iOS.

## Option 2 : Manuel (sans RevenueCat)

Nous nous engageons à aider nos clients WebViewGold à réussir et souhaitons attirer votre attention sur le 15% Service Fee Tier Program du Google Play Store et sur le Small Business Program d'Apple. Ces programmes permettent aux développeurs éligibles de bénéficier d'une commission de 15 %, une réduction significative par rapport aux 30 % standard. La demande est rapide et facile, et peut potentiellement vous faire économiser 50 % de frais en **réduisant les taux de commission de Google et d'Apple de 30 % à 15 %**. Une fois approuvé, vous bénéficierez du taux de commission réduit pour toutes les applications payantes et achats intégrés effectués par les clients sur les stores concernés. Pour en savoir plus sur le programme Google Play, cliquez **[ici](https://support.google.com/googleplay/android-developer/answer/112622?hl=en)**, et pour le programme Apple, rendez-vous **[ici](https://developer.apple.com/app-store/small-business-program/)**.

Après la configuration, pour les **produits d'achat intégré**, il suffit de créer un lien vers ce type d'URL :

```html
<a href="inapppurchase://?package=purchase_package_identifier_name_here&disableadmob=true&consumable=true&successful_url=https://www.google.com">Buy In-App Purchase</a>
```

- Le « package » est l'identifiant du produit que vous souhaitez vendre.
- La « successful_url » est l'URL que l'application doit charger une fois l'achat terminé.
  - *Vous pouvez enregistrer un cookie sur cette page afin que votre application web se souvienne que l'achat a été effectué.*
- Incluez « disableadmob=true » si vous souhaitez désactiver les publicités après l'achat du produit.
- Pour permettre que l'utilisateur soit à nouveau facturé pour le même produit d'achat intégré (s'il l'achète une nouvelle fois), définissez l'attribut « consumable » sur true. En revanche, si vous souhaitez empêcher que l'utilisateur soit à nouveau facturé pour le même produit (s'il l'achète une nouvelle fois), définissez « consumable » sur false ou omettez-le totalement (puisque false est la valeur par défaut). Veillez à utiliser WebViewGold pour Android v12.5 ou ultérieure.

Vous pouvez également utiliser ce type d'URL pour les **produits d'abonnement intégré** :

```html
<a href="inappsubscription://?package=purchase_package_identifier_name_here&expired_url=https://www.yahoo.com&successful_url=https://www.google.com">Start In-App Subscription</a>
```

- Le « package » est l'identifiant du produit d'abonnement que vous souhaitez vendre.
- La « successful_url » est l'URL que l'application doit charger une fois l'achat terminé.
  - *Vous pouvez enregistrer un cookie sur cette page afin que votre application web se souvienne que l'abonnement a été activé.*
- La « expired_url » est l'URL que l'application doit charger lorsque l'abonnement n'est plus valide.
  - *Vous pouvez mettre à jour/supprimer un cookie sur cette page afin que votre application web se souvienne que l'abonnement a été désactivé.*

Dans cet exemple d'URL, https://www.google.com doit être appelée après l'activation réussie de l'abonnement, et https://www.yahoo.com doit être appelée dès que l'abonnement expire.\
Vous pouvez identifier l'utilisateur côté serveur. Par exemple, si le site /buy_now.php redirige vers l'API d'achat intégré et que cette API redirige vers /thanks.php, vous pouvez toujours accéder aux cookies utilisateur/session côté serveur et identifier l'utilisateur qui vient d'effectuer cet achat intégré. Dans ce cas d'usage, veuillez vous assurer de désactiver CLEAR_CACHE_ON_STARTUP dans le fichier Config.java afin de conserver les cookies activés par le processus d'achat intégré.

**Gérer/annuler les abonnements :** WebViewGold pour Android peut créer un lien direct vers l'écran de gestion des abonnements du Play Store — dirigez simplement votre lien vers `cancelinapppurchase://` :

```html
<script>
<a href="cancelinapppurchase://">Manage/cancel subscription in Google Play</a>
<script>
```

**Restaurer les achats :** WebViewGold pour Android offre un moyen simple de restaurer les achats intégrés effectués par les utilisateurs. Utile par exemple dans les cas où les utilisateurs réinstallent l'application ou changent d'appareil et doivent retrouver l'accès à leur contenu acheté :

```html
<script>
<a href="restoreinapppurchases://">Restore</a>
<script>
```

**Vérification côté serveur :** En complément ou en alternative, WebViewGold vous permet également de gérer les données d'achat intégré ou d'abonnement côté serveur. Après une transaction réussie, les variables JavaScript suivantes sont créées et injectées dans la page web par WebViewGold : \
**1. planID :** Contient l'identifiant du produit\
**2. transactionIdentifier :** Contient l'identifiant unique de la transaction\
**3. subreceipts :** Contient les identifiants de reçu uniques pour les abonnements de l'utilisateur\
Ces variables sont accessibles directement sur la page web pour le stockage et la validation côté serveur. Notez que ces variables sont injectées directement dans l'objet window global après une transaction. Assurez-vous que votre JavaScript est exécuté sur la même page où les variables sont accessibles. Ajoutez des mécanismes de repli appropriés si les variables ne sont pas disponibles dans le délai prévu (comme le montre l'implémentation du timeout).
L'envoi de ces variables à votre serveur vous permet de valider les abonnements et transactions en toute sécurité à l'aide de l'API de validation de reçus d'Apple ou de la méthode de votre choix. Voici un exemple d'implémentation JavaScript :

```html
<script>
// Utility function to wait for a variable to be defined
function waitForVariable(variableName, callback, timeout = 5000) {
    const startTime = Date.now();

    (function checkVariable() {
        if (window[variableName] !== undefined) {
            callback(window[variableName]);
        } else if (Date.now() - startTime < timeout) {
            setTimeout(checkVariable, 100);
        } else {
            console.error(`Timeout: ${variableName} was not set within ${timeout} ms`);
        }
    })();
}

// Example: Handling In-App Purchase/Subscription variables
waitForVariable("planID", function(planID) {
    console.log("planID:", planID);
    // Send the Product ID to your server
    sendToServer("planID", planID);
});

waitForVariable("transactionIdentifier", function(transactionIdentifier) {
    console.log("transactionIdentifier:", transactionIdentifier);
    // Send the Transaction ID to your server
    sendToServer("transactionIdentifier", transactionIdentifier);
});

waitForVariable("subreceipts", function(subreceipts) {
    console.log("subreceipts:", subreceipts);
    // Send Subscription Receipt IDs to your server
    sendToServer("subreceipts", subreceipts);
});

// Function to send data to your server for validation
function sendToServer(key, value) {
    fetch("https://example.com/api/validate", {
        method: "POST",
        headers: {
            "Content-Type": "application/json"
        },
        body: JSON.stringify({ [key]: value })
    })
    .then(response => response.json())
    .then(data => console.log(`Server Response for ${key}:`, data))
    .catch(error => console.error(`Error sending ${key}:`, error));
}
</script>
```

**Tarification localisée / Obtenir la localisation du store :** Le schéma d'URL `getstorelocation://` injecte la localisation du Play Store dans une variable JavaScript. Lorsque `getstorelocation://` est appelé/lié, le wrapper WebViewGold récupère le code pays du Play Store, s'il est disponible. Vous pouvez également définir `autoInjectVariable` sur `true` dans le fichier de configuration afin d'injecter automatiquement cette valeur (et d'autres) en JavaScript sans avoir besoin d'appeler une URL. Le code pays est alors injecté dans une variable JavaScript `storeLocation` que votre application web peut utiliser (**par exemple pour afficher une tarification localisée**). Si le code n'est pas disponible, `storeLocation` sera défini sur `null` :

- En cas de succès (exemple États-Unis) : `var storeLocation = 'US';`
- Si aucun code pays n'est trouvé : `var storeLocation = null;`

Remarque : Comme pour toute technologie, il est essentiel de mentionner que, même en utilisant notre API, il existe un risque que certains utilisateurs (techniquement avertis) puissent accéder au contenu restreint sans le payer. Cela pourrait par exemple se produire en récupérant et en ouvrant directement le lien Success URL, en désinstallant l'application puis en annulant les produits d'abonnement afin que l'URL d'expiration ne soit jamais appelée (pour minimiser ce risque, vous pouvez donc demander occasionnellement une nouvelle autorisation), ou en utilisant les droits de rétractation et/ou les procédures de rétrofacturation des cartes de crédit. Il convient toutefois de noter qu'un certain niveau de risque existe avec toute approche numérique. De manière générale, notre API constitue une approche pratique et facile à intégrer pour fournir du contenu payant aux utilisateurs d'applications, et nous continuons à travailler sur des moyens de réduire davantage les risques. L'utilisation de notre API se fait toujours à vos risques et sans garantie, mais globalement, bien qu'il soit essentiel d'être conscient du risque d'accès non autorisé/non payé au contenu, les avantages de l'utilisation de notre API l'emportent largement sur les risques pour la plupart des utilisateurs. Il est recommandé de suivre et de comparer les données de vente de la Google Play Store Developer Console avec les activations côté serveur des produits d'achat intégré, afin de garantir une déclaration précise des revenus et d'identifier tout écart potentiel.

---

## Continuer la lecture

- ← Précédent : [API de notation In-App](in-app-rating.md)
- Suivant → : [IAP History API](iap-history.md)
- Même fonctionnalité sur les autres plateformes : [iOS – API d'achats intégrés](../ios/in-app-purchases.md) · [macOS – API In-App Purchases](../macos/in-app-purchases.md)
- Langues : [🇺🇸 English](../../android/in-app-purchases.md) · [🇩🇪 Deutsch](../../de/android/in-app-purchases.md) · **🇫🇷 Français** · [🇪🇸 Español](../../es/android/in-app-purchases.md) · [🇨🇳 中文](../../zh/android/in-app-purchases.md)

> [!TIP]
> **Trop occupé ? Nous configurons votre app pour vous.** Notre équipe configure, compile & soumet votre app WebViewGold — clé en main, délai rapide, Made in Germany. [Faire configurer mon app →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_android_doc_online)
>
> **Compilez dans votre navigateur :** Pas de Mac, pas d’IDE : le **WebViewGold Cloud Builder** configure, compile & met en ligne votre app. [Découvrir Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=android_docs)
