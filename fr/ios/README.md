---
title: "Documentation WebViewGold pour iOS – Convertir un site web en app iOS"
description: "Documentation officielle de WebViewGold pour iOS : convertissez votre site web en application iOS native en quelques minutes : guide de configuration, plus de 40 API et fonctionnalités, et publication sur l'App Store."
lang: "fr"
product: "WebViewGold pour iOS"
platform: "iOS"
canonical_url: "https://www.webviewgold.com/fr/docs/iOS/"
keywords:
  - "WebViewGold pour iOS"
  - "convertir un site web en app"
  - "documentation d’app WebView"
  - "SDK WebView iOS"
  - "PWA en app"
  - "HTML en app"
  - "pont JavaScript"
last_updated: "2026-10-09"
---

# Documentation WebViewGold pour iOS

![WebViewGold pour iOS](../../assets/ios/img/header.webp)

> Documentation officielle de WebViewGold pour iOS : convertissez votre site web en application iOS native en quelques minutes : guide de configuration, plus de 40 API et fonctionnalités, et publication sur l'App Store.

[Documentation](../README.md) › WebViewGold pour iOS

Convertissez votre site web, PWA, tableau de bord SaaS, boutique e-commerce ou app web générée par IA en une app iOS native en quelques minutes. Utilisez WebViewGold comme un SDK d’application léger : configurez votre URL, activez des API natives, intégrez des commandes du pont JavaScript et publiez une app prête pour le store sans reconstruire votre produit web de zéro.

WebViewGold fonctionne avec les sites HTML/PHP classiques, WordPress, les projets jQuery Mobile et les apps web modernes créées avec Lovable, Base44, Bolt, Bubble, React, Vue, Angular ou des outils similaires. La documentation ci-dessous explique le flux de configuration, les API de fonctionnalités natives, les considérations de sécurité et les étapes de publication dans un format technique axé sur l’implémentation.

**[Démarrer le guide →](setup-website.md)** · [Télécharger WebViewGold](https://www.webviewgold.com/download/ios) · [Cloud Builder](https://www.webviewgold.com/cloud-builder?ref=ios_docs)

## Démarrage rapide

Trois étapes du site web à l’app publiée :

1. **[Configurez votre app web](setup-website.md)** — Utilisez une URL distante, empaquetez des fichiers HTML locaux, ou combinez les deux avec une solution de repli hors ligne.
2. **[Configurez WebViewGold](setup.md)** — Insérez votre URL et affinez chaque option dans un simple fichier de config — sans coder.
3. **[Compiler & publier](publish.md)** — Publiez votre app sur le store — vous-même, via Cloud Builder ou avec notre service de publication.

## Nouveautés

WebViewGold est mis à jour régulièrement. Consultez le journal des modifications complet [ici](https://www.webviewgold.com/changelog/ios/).

## Tous les sujets, API & fonctionnalités

Tout ce que WebViewGold pour iOS peut faire — chaque sujet sur sa propre page :

### Prise en main

- **[Configurer l'application web](setup-website.md)** — Préparez votre site web, votre PWA ou vos fichiers HTML locaux pour votre application iOS : utilisez une URL distante, intégrez les fichiers hors ligne dans l'application ou combinez les deux avec une solution de repli hors ligne.
- **[Configurer WebViewGold](setup.md)** — Téléchargez le template Xcode de WebViewGold, insérez votre URL dans Config.swift et explorez toutes les options de configuration intégrées, sans aucune compétence en programmation.

### Design de l’app

- **[Nom, icône et splash](app-name-icon-splash.md)** — Renommez votre application iOS, ajoutez une icône d'app personnalisée et configurez des écrans de démarrage personnalisés pour votre application WebViewGold.
- **[Modifier la Safe Area](safe-area.md)** — Ajustez la Safe Area et activez la barre inférieure personnalisée pour que votre application web s'affiche parfaitement sur les iPhone dotés d'une barre d'accueil.

### API et fonctionnalités

- **[API de géolocalisation](geolocation.md)** — Activez la géolocalisation HTML5 dans votre application WebView iOS et demandez les autorisations de localisation précise de la bonne manière.
- **[API de notifications push](push-notifications.md)** — Envoyez des notifications push aux utilisateurs de votre application iOS avec OneSignal, Firebase ou Pushwoosh : configuration, deep links et ciblage par utilisateur expliqués.
- **[API AdMob Ads](admob.md)** — Monétisez votre application iOS avec les publicités bannière, interstitielles et récompensées de Google AdMob : configuration et déclencheurs JavaScript.
- **[API Facebook Ads](facebook-ads.md)** — Affichez des publicités bannière et interstitielles Facebook Audience Network dans votre application WebViewGold iOS.
- **[API audio HTML](html-audio.md)** — Continuez à lire l'audio HTML en arrière-plan de votre application WebView iOS, même lorsque l'écran est verrouillé.
- **[API de vidéo native](native-video.md)** — Lisez des flux vidéo dans le lecteur natif d'iOS avec prise en charge du mode Image dans l'image — déclenchés directement depuis votre application web.
- **[API de téléchargement de fichiers](file-downloader.md)** — Permettez aux utilisateurs de télécharger des images, des PDF et d'autres fichiers depuis votre application web directement sur leur iPhone ou iPad.
- **[API d'impression](printer.md)** — Imprimez des images et des PDF depuis votre application web via AirPrint : envoyez des fichiers à la boîte de dialogue d'impression native d'iOS avec un seul lien.
- **[API calendrier iCal](ical-calendar.md)** — Ajoutez des événements de calendrier depuis votre application web au calendrier iOS natif grâce à l'API calendrier iCal.
- **[API de cartes Apple Wallet](wallet-pass.md)** — Permettez aux utilisateurs d'ajouter des cartes .pkpass (billets, coupons, cartes de membre) depuis votre application web à Apple Wallet.
- **[API UUID](uuid.md)** — Identifiez les installations de l'app avec un UUID unique ajouté à votre URL WebView ou récupéré via JavaScript.
- **[API lampe torche](flashlight.md)** — Contrôlez la lampe torche de l'appareil depuis votre application web avec de simples liens JavaScript dans WebViewGold pour iOS.
- **[API de réinitialisation de l'app](reset-app.md)** — Réinitialisez le cache, les cookies et le stockage local de votre application WebView iOS avec un simple lien ou appel JavaScript.
- **[API de décision de suivi](user-tracking.md)** — Respectez l'App Tracking Transparency : lisez la décision de suivi de l'utilisateur et réagissez en conséquence dans votre application WebViewGold iOS.
- **[API d'indicateur de chargement](loading-sign.md)** — Affichez ou masquez l'indicateur de chargement natif à la demande et personnalisez l'expérience de chargement de votre application iOS.
- **[API Pull-to-Refresh](pull-to-refresh.md)** — Activez le geste natif « tirer pour actualiser » dans votre app WebView iOS, personnalisez ses couleurs et basculez-le dynamiquement depuis votre app web.
- **[API de gestion des URL](url-handling.md)** — Décidez quels liens s'ouvrent dans votre app, dans un onglet de navigateur intégré ou dans Safari : un contrôle total de la gestion des URL pour iOS.
- **[Social Login Helper](social-login.md)** — Faites fonctionner les connexions OAuth Google, Facebook et Apple de manière fiable dans votre app WebView iOS grâce aux assistants de connexion intégrés.
- **[API de reconnexion](reconnect.md)** — Ajoutez un bouton « Réessayer » à votre page de secours hors ligne qui recharge la dernière URL en ligne de votre application iOS.
- **[API CSS et JS personnalisés](custom-css-js.md)** — Injectez des styles CSS et du code JavaScript personnalisés dans n'importe quelle page de votre application WebView iOS, idéal pour les ajustements propres à l'app.
- **[API Universal Links](universal-links.md)** — Ouvrez les liens vers votre domaine directement dans votre application iOS grâce aux Apple Universal Links : configuration, fichier AASA et dépannage.
- **[API de deep linking](deep-linking.md)** — Lancez votre application iOS via des schémas d'URL personnalisés et redirigez les utilisateurs par deep link vers des pages précises de votre application web.
- **[API de partage d'app](app-sharing-dialog.md)** — Déclenchez la feuille de partage iOS native depuis votre application web pour permettre aux utilisateurs de partager votre app ou n'importe quelle URL.
- **[API de notation In-App](in-app-rating.md)** — Demandez une note App Store à vos utilisateurs au moment idéal — déclenchez la boîte de dialogue de notation native d'iOS depuis votre application web.
- **[API d'achats intégrés](in-app-purchases.md)** — Vendez des biens numériques et des abonnements dans votre application WebView iOS grâce aux achats intégrés basés sur StoreKit.
- **[API d'historique des achats](iap-history.md)** — Lisez les achats In-App précédents de l'utilisateur depuis votre application web au format JSON — parfait pour les pages « Mes achats ».
- **[API de scanner de QR code](qr-code-scanner.md)** — Ouvrez un scanner de QR code natif depuis votre application web et traitez les résultats de scan via URL ou JavaScript.
- **[API de scanner de codes-barres](barcode-scanner.md)** — Scannez des codes-barres EAN, UPC et autres nativement dans votre application WebView iOS et transmettez les résultats à votre application web.
- **[API de mode de scan](scanning-mode.md)** — Affinez le comportement de scan de la caméra du scanner de QR codes et de codes-barres dans WebViewGold pour iOS.
- **[Scanner de documents](document-scanner.md)** — Permettez aux utilisateurs de scanner des documents papier avec l'appareil photo et de les téléverser via l'upload de fichiers de votre application web — propulsé par Apple VisionKit.
- **[API de capture d'écran](take-screenshot.md)** — Capturez par programmation une capture d'écran de l'écran actuel de l'app et partagez-la ou enregistrez-la, via JavaScript.
- **[API de vérification de version](app-version-check.md)** — Détectez la version installée de l'app depuis votre application web et invitez les utilisateurs à la mettre à jour si nécessaire.
- **[API d'UI dynamique](dynamic-ui.md)** — Modifiez dynamiquement des éléments d'UI natifs comme les couleurs de la barre d'état ou de la barre inférieure depuis votre application web.
- **[API d'icône d'app dynamique](dynamic-app-icon.md)** — Basculez entre différentes icônes d'app à l'exécution dans votre application WebView iOS, déclenché depuis votre application web.
- **[API Contacts](contacts.md)** — Accédez au carnet d'adresses de l'appareil depuis votre application web : lisez les contacts avec l'autorisation de l'utilisateur dans WebViewGold pour iOS.
- **[API d'authentification biométrique](biometric-authentication.md)** — Protégez votre application iOS avec Face ID ou Touch ID et authentifiez les utilisateurs par biométrie depuis votre application web.
- **[API de retour haptique](haptic-feedback.md)** — Déclenchez un retour haptique natif (vibrations) depuis votre application web pour une sensation d'app vraiment native sur iOS.
- **[API Shortcut](shortcut.md)** — Ajoutez des raccourcis d'action rapide sur l'écran d'accueil de votre application iOS qui redirigent par deep link vers des pages précises.
- **[API Presse-papiers](clipboard.md)** — Copiez du texte dans le presse-papiers iOS et lisez le contenu du presse-papiers depuis votre application web via JavaScript.
- **[API de lecture/écriture de valeur](read-write-value.md)** — Stockez durablement une valeur de chaîne sur l'appareil et relisez-la dans le JavaScript de votre application web.
- **[API d'ouverture des réglages](open-app-settings.md)** — Envoyez les utilisateurs directement vers la page de votre application dans les Réglages d'iOS pour gérer autorisations et notifications.

### Extensions et plugins

- **[Share Extension](share-extension.md)** — Permettez aux utilisateurs de partager du contenu d'autres apps directement dans votre application WebView iOS grâce à une Share Extension.
- **[Widget Extension](widget-extension.md)** — Ajoutez un widget d'écran d'accueil à votre application WebView iOS qui redirige les utilisateurs directement vers votre application web.
- **[App Clip Extension](app-clip.md)** — Proposez une version App Clip légère de votre application iOS qui s'ouvre instantanément sans installation.
- **[Pied de navigation natif](navigation-footer.md)** — Activez une barre de navigation inférieure native avec des boutons précédent, suivant et personnalisés dans votre application iOS.
- **[Barre latérale native](sidebar.md)** — Activez un menu latéral coulissant natif avec des liens personnalisés et des icônes SF Symbols — configuré via Sidebar.json.
- **[Détection de capture d'écran](screen-capture.md)** — Détectez les captures et les enregistrements d'écran dans votre application iOS et réagissez depuis votre application web.
- **[Fonction MultiAPICall](multi-api-call.md)** — Enchaînez plusieurs appels d'API WebViewGold en une seule requête grâce à la fonction MultiAPICall pour iOS.
- **[Plugin NFC](nfc.md)** — Lisez les tags NFC nativement dans votre application WebView iOS et transmettez les données du tag à votre application web.
- **[Plugin Siri](siri.md)** — Ajoutez la prise en charge des raccourcis Siri à votre application WebView iOS et ouvrez le contenu de l'app à la voix.
- **[Plugin HealthKit](healthkit.md)** — Connectez votre application web à Apple HealthKit et lisez les données de santé avec l'autorisation de l'utilisateur sur iOS.

### Compiler et publier

- **[Compiler et publier](publish.md)** — Publiez votre application WebView sur l'Apple App Store : service de publication complet, processus manuel et modification de l'identifiant de bundle.

### Plus

- **[Crédits et licences](credits.md)** — Conditions de licence de WebViewGold pour iOS, cas où vous avez besoin d'une Envato Extended License et crédits open source.
- **[Noter WebViewGold](rate.md)** — WebViewGold vous plaît ? Notez-le sur CodeCanyon en quelques secondes : c'est ce qui fait vivre les mises à jour.
- **[Versions Android et macOS](more-platforms.md)** — Déployez votre app sur davantage de plateformes : procurez-vous WebViewGold pour Android et macOS et réutilisez la même application web.
- **[Support et contact](support.md)** — Obtenez de l'aide rapidement : parcourez le centre de support WebViewGold, contactez directement notre équipe ou demandez un développement d'app sur mesure et professionnel, made in Germany.

## Une app web, toutes les plateformes

Réutilisez le même site web pour des apps iOS, Android & macOS avec WebViewGold.

- [WebViewGold pour Android](../android/README.md)
- [WebViewGold pour macOS](../macos/README.md)

**Langues :** [🇺🇸 English](../../ios/README.md) · [🇩🇪 Deutsch](../../de/ios/README.md) · **🇫🇷 Français** · [🇪🇸 Español](../../es/ios/README.md) · [🇨🇳 中文](../../zh/ios/README.md)

> [!TIP]
> **Trop occupé ? Nous configurons votre app pour vous.** Notre équipe configure, compile & soumet votre app WebViewGold — clé en main, délai rapide, Made in Germany. [Faire configurer mon app →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **Compilez dans votre navigateur :** Pas de Mac, pas d’IDE : le **WebViewGold Cloud Builder** configure, compile & met en ligne votre app. [Découvrir Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
