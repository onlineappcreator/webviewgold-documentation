---
title: "API d'achats intégrés – Documentation WebViewGold pour iOS"
description: "Vendez des biens numériques et des abonnements dans votre application WebView iOS grâce aux achats intégrés basés sur StoreKit."
lang: "fr"
product: "WebViewGold pour iOS"
platform: "iOS"
category: "API et fonctionnalités"
slug: "in-app-purchases"
canonical_url: "https://www.webviewgold.com/fr/docs/iOS/in-app-purchases/"
keywords:
  - "API d'achats intégrés"
  - "WebViewGold pour iOS"
  - "convertir un site web en app"
  - "documentation d’app WebView"
  - "SDK WebView iOS"
  - "PWA en app"
  - "HTML en app"
  - "pont JavaScript"
last_updated: "2026-10-09"
---

# API d'achats intégrés – WebViewGold pour iOS

> **Résumé :** Vendez des biens numériques et des abonnements dans votre application WebView iOS grâce aux achats intégrés basés sur StoreKit.

[Documentation](../README.md) › [WebViewGold pour iOS](README.md) › API d'achats intégrés

**Plateforme :** iOS · **Catégorie :** API et fonctionnalités · **Version en ligne :** [www.webviewgold.com/fr/docs/iOS/in-app-purchases/](https://www.webviewgold.com/fr/docs/iOS/in-app-purchases/)

---

Dans certaines applications, vous pouvez acheter des contenus ou services supplémentaires. Ce type d'achats est appelé « achats intégrés ». Ils peuvent constituer une source de revenus attrayante pour les développeurs et sont très pratiques pour les clients, car ils utilisent les comptes et moyens de paiement existants pour le règlement. WebViewGold permet de déclencher des achats intégrés App Store. Assurez-vous de posséder une [licence étendue](credits.md) de WebViewGold si vous prévoyez d'utiliser cette fonctionnalité dans un produit final. Besoin d'une mise à niveau ? [Découvrez ici comment effectuer la mise à niveau](https://help.market.envato.com/hc/en-us/articles/115005593503-If-I-choose-the-wrong-license-or-need-to-upgrade-my-license-how-easy-is-it-to-change-to-the-correct-license).

**Option 1 (par défaut) : RevenueCat**\
Créez votre [compte RevenueCat](https://tinyurl.com/register-revenuecat) gratuit pour commencer. Les informations tarifaires sont disponibles sur leur site web. Configurez ensuite RevenueCat en suivant leurs assistants de configuration et leur documentation (les détails tarifaires sont disponibles sur leur [site web](https://tinyurl.com/register-revenuecat)). Ajoutez ensuite vos informations dans **Config.swift**. Cette approche prend également en charge le [15% Service Fee Tier Program](https://support.google.com/googleplay/android-developer/answer/112622?hl=en) du Google Play Store et le [Small Business Program](https://developer.apple.com/app-store/small-business-program/) d'Apple. Si vous participez à ces programmes à frais réduits, informez-en RevenueCat via leurs pages [Apple Small Business Program](https://www.revenuecat.com/docs/platform-resources/apple-platform-resources/app-store-small-business-program) ou [Google 15% reduced service fee](https://www.revenuecat.com/docs/platform-resources/google-platform-resources/15-reduced-service-fee). Voici à quoi ressemble la configuration dans Config.swift :

```swift
static let kRevenueCatEnable = true //Set to true to activate RevenueCat
static let kRevenueCatShowDefaultOfferingPaywall = true //Set to true to show the default offering paywall on app launch
static let revenueCatAPIKey = "xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx" //Your RevenueCat API Key (sign up via tinyurl.com/register-revenuecat first, then follow tinyurl.com/api-key-revenuecat how to find it)
static let revenueCatProjectID = "xxxxxxxxx" //Your RevenueCat Project ID (sign up via tinyurl.com/register-revenuecat first, then follow tinyurl.com/project-id-revenuecat how to find it)
```

Assurez-vous que votre Bundle ID dans Xcode et App Store Connect correspond au projet configuré dans RevenueCat. Déclenchez un achat ou un abonnement à l'aide de :

```
revenuecat://purchase?external_id=user_123&product=sub_30_days
```

`external_id` = identifiant utilisateur, par exemple l'e-mail du client ou son identifiant utilisateur. `product` = identifiant affiché dans la console RevenueCat.

Vous pouvez également présenter un **paywall RevenueCat** natif (configuré dans le tableau de bord RevenueCat) directement depuis votre app web — nécessite iOS 15 ou une version ultérieure :

```
revenuecat://launchPaywall?external_id=user_123&offering=CustomOfferingOne
```

`external_id` = identifiant utilisateur, par exemple l'e-mail du client ou son identifiant utilisateur (obligatoire). `offering` = identifiant facultatif de l'offering RevenueCat dont le paywall doit être affiché ; omettez-le pour présenter le paywall de l'offering par défaut.

## Option 2 : Manuel (sans RevenueCat)

Dans un premier temps, insérez les informations App Store Connect de votre « Shared Secret » d'achat intégré dans le fichier **Config.swift**. Pour trouver votre « Shared Secret » dans App Store Connect, vous devez d'abord vous connecter à votre compte App Store Connect. Rendez-vous ensuite dans la section « Users and Access » et sélectionnez l'onglet « Shared Secret ». Votre « Shared Secret » généré sera affiché et vous pourrez le copier/coller dans le champ « IAPSharedSecret » correspondant de Config.swift de WebViewGold. \
La réussite de nos clients nous tient à cœur et nous sommes là pour les accompagner autant que possible : c'est pourquoi nous souhaitons évoquer ici l'App Store Small Business Program et le 15% Service Fee Tier Program du Google Play Store. Dans le cadre de ces programmes, les développeurs éligibles peuvent bénéficier d'une commission réduite de 15 %, contre les 30 % standard. Il ne faut que quelques minutes pour remplir leurs formulaires, ce qui peut potentiellement vous faire économiser 50 % de frais (**passage d'une commission de 30 % à 15 %**). Une fois approuvé, vous bénéficierez du taux de commission réduit pour toutes les applications payantes et les achats intégrés effectués par les clients sur les stores concernés. Pour en savoir plus sur le programme Apple, cliquez [**ici**](https://developer.apple.com/app-store/small-business-program/), et sur le programme Google Play [**ici**](https://support.google.com/googleplay/android-developer/answer/112622?hl=en). \
Après la configuration, pour les **produits d'achat intégré**, il suffit de créer un lien vers ce type d'URL :

```html
<a href="inapppurchase://?package=IN-APP_PURCHASE_PRODUCT_IDENTIFIER&disableadmob=true&successful_url=https://www.google.com">Buy In-App Purchase</a>
```

- Le « package » est l'identifiant du produit que vous souhaitez vendre.
- La « successful_url » est l'URL que l'application doit charger une fois l'achat terminé.
  - *Vous pouvez enregistrer un cookie sur cette page afin que votre application web se souvienne que l'achat a été effectué.*
- Incluez « disableadmob=true » si vous souhaitez désactiver les publicités AdMob après l'achat du produit.

Pour les **produits d'abonnement intégré**, utilisez ce type de schéma d'URL :

```html
<a href="inappsubscription://?package=IN-APP_PURCHASE_PRODUCT_IDENTIFIER&expired_url=https://www.yahoo.com&successful_url=https://www.google.com">Start In-App Subscription</a>
```

- Le « package » est l'identifiant du produit d'abonnement que vous souhaitez vendre.
- La « successful_url » est l'URL que l'application doit charger une fois l'achat terminé.
  - *Vous pouvez enregistrer un cookie sur cette page afin que votre application web se souvienne que l'abonnement a été activé.*
- La « expired_url » est l'URL que l'application doit charger lorsque l'abonnement n'est plus valide.
  - *Vous pouvez mettre à jour/supprimer un cookie sur cette page afin que votre application web se souvienne que l'abonnement a été désactivé.*

Toutes les informations sur l'identifiant du produit d'achat intégré sont disponibles [ici](https://developer.apple.com/library/archive/qa/qa1329/_index.html).\
Vous pouvez identifier l'utilisateur côté serveur. Par exemple, si le site /buy_now.php redirige vers l'API d'achat intégré et que cette API redirige vers /thanks.php, vous pouvez toujours accéder aux cookies utilisateur/session côté serveur et identifier l'utilisateur qui vient d'effectuer cet achat intégré. Dans ce cas d'usage, veuillez vous assurer de désactiver l'option *deletecache* dans le fichier *Config.swift* afin de conserver les cookies activés par le processus d'achat intégré.

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

**Restaurer les achats :** Un appel à `restoreinapppurchases://` permet à votre application de réactiver les contenus achetés précédemment. Lorsqu'un utilisateur tape sur un lien avec ce schéma d'URL, l'application lance un processus visant à revalider et restaurer les achats intégrés — idéal pour des scénarios tels que la réinstallation de l'application ou le changement d'appareil. Ajoutez simplement un lien comme celui-ci pour permettre à vos utilisateurs de restaurer leurs achats :

```html
<a href="restoreinapppurchases://">Restore Purchases</a>
```

**Historique des achats :** pour afficher les achats précédents de l'utilisateur dans votre application web, consultez l'[API d'historique des achats In-App](iap-history.md) (`getpurchasehistory://`).

**Annuler l'abonnement :** Un appel à `cancelinapppurchase://` redirige les utilisateurs vers le portail officiel de gestion des abonnements Apple, où ils peuvent annuler leurs abonnements via l'interface native d'Apple. Ajoutez simplement un lien comme le suivant pour rediriger les utilisateurs vers la gestion de leurs abonnements :

```html
<a href="cancelinapppurchase://">Cancel Subscription</a>
```

**Tarification localisée / Obtenir la localisation du store :** Le schéma d'URL `getstorelocation://` injecte la localisation de l'App Store dans une variable JavaScript. Une fois `getstorelocation://` appelé/lié, le wrapper WebViewGold récupère le code pays de l'App Store, s'il est disponible. Vous pouvez également passer `autoInjectVariable` à `true` dans Config.swift afin d'injecter automatiquement cette valeur (et d'autres) en JavaScript sans avoir besoin d'appeler une URL au préalable. Le code pays est alors injecté dans une variable JavaScript `storeLocation` que votre application web peut utiliser (**par exemple pour afficher une tarification localisée**). Si le code n'est pas disponible, `storeLocation` sera défini sur `null` :

- En cas de succès (exemple États-Unis d'Amérique) : `var storeLocation = 'US';`
- Si aucun code pays n'est trouvé : `var storeLocation = null;`

Remarque : L'utilisation de notre API pour fournir du contenu payant aux utilisateurs d'applications comporte un certain risque que des utilisateurs techniquement avertis accèdent au contenu sans le payer. Cela peut se produire par différentes méthodes, telles que la récupération et l'ouverture directe du lien Success URL, l'annulation des produits d'abonnement après avoir désinstallé l'application, ou l'utilisation des droits de rétractation et des procédures de rétrofacturation des cartes de crédit. Cependant, il est essentiel de noter qu'un certain niveau de risque existe avec toute approche numérique. Bien que nous continuions à travailler sur des moyens de réduire ces risques, il appartient en fin de compte à l'utilisateur/développeur de WebViewGold d'accepter le risque d'accès non autorisé/non payé au contenu lorsqu'il utilise l'approche suggérée, l'API étant fournie sans garantie. Malgré cela, les avantages de l'utilisation de notre API l'emportent généralement sur les risques pour la plupart des utilisateurs. Afin d'assurer une déclaration précise des revenus et d'identifier d'éventuelles anomalies, nous recommandons de suivre et de comparer les données de vente d'App Store Connect avec les activations côté serveur des produits d'achat intégré.

---

## Continuer la lecture

- ← Précédent : [API de notation In-App](in-app-rating.md)
- Suivant → : [API d'historique des achats](iap-history.md)
- Même fonctionnalité sur les autres plateformes : [Android – API d'achats intégrés](../android/in-app-purchases.md) · [macOS – API In-App Purchases](../macos/in-app-purchases.md)
- Langues : [🇺🇸 English](../../ios/in-app-purchases.md) · [🇩🇪 Deutsch](../../de/ios/in-app-purchases.md) · **🇫🇷 Français** · [🇪🇸 Español](../../es/ios/in-app-purchases.md) · [🇨🇳 中文](../../zh/ios/in-app-purchases.md)

> [!TIP]
> **Trop occupé ? Nous configurons votre app pour vous.** Notre équipe configure, compile & soumet votre app WebViewGold — clé en main, délai rapide, Made in Germany. [Faire configurer mon app →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **Compilez dans votre navigateur :** Pas de Mac, pas d’IDE : le **WebViewGold Cloud Builder** configure, compile & met en ligne votre app. [Découvrir Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
