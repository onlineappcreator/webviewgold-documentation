---
title: "Documentation WebViewGold pour Android – Convertir un site web en application Android"
description: "Documentation officielle de WebViewGold pour Android : convertissez votre site web en application Android native en quelques minutes — guide de configuration, plus de 30 API et fonctionnalités, et publication sur Google Play."
lang: "fr"
product: "WebViewGold pour Android"
platform: "Android"
canonical_url: "https://www.webviewgold.com/fr/docs/android/"
keywords:
  - "WebViewGold pour Android"
  - "convertir un site web en app"
  - "documentation d’app WebView"
  - "SDK WebView Android"
  - "PWA en app"
  - "HTML en app"
  - "pont JavaScript"
last_updated: "2026-10-09"
---

# Documentation WebViewGold pour Android

![WebViewGold pour Android](../../assets/android/img/header.webp)

> Documentation officielle de WebViewGold pour Android : convertissez votre site web en application Android native en quelques minutes — guide de configuration, plus de 30 API et fonctionnalités, et publication sur Google Play.

[Documentation](../README.md) › WebViewGold pour Android

Convertissez votre site web, PWA, tableau de bord SaaS, boutique e-commerce ou app web générée par IA en une app Android native en quelques minutes. Utilisez WebViewGold comme un SDK d’application léger : configurez votre URL, activez des API natives, intégrez des commandes du pont JavaScript et publiez une app prête pour le store sans reconstruire votre produit web de zéro.

WebViewGold fonctionne avec les sites HTML/PHP classiques, WordPress, les projets jQuery Mobile et les apps web modernes créées avec Lovable, Base44, Bolt, Bubble, React, Vue, Angular ou des outils similaires. La documentation ci-dessous explique le flux de configuration, les API de fonctionnalités natives, les considérations de sécurité et les étapes de publication dans un format technique axé sur l’implémentation.

**[Démarrer le guide →](setup-website.md)** · [Télécharger WebViewGold](https://www.webviewgold.com/download/android) · [Cloud Builder](https://www.webviewgold.com/cloud-builder?ref=android_docs)

## Démarrage rapide

Trois étapes du site web à l’app publiée :

1. **[Configurez votre app web](setup-website.md)** — Utilisez une URL distante, empaquetez des fichiers HTML locaux, ou combinez les deux avec une solution de repli hors ligne.
2. **[Configurez WebViewGold](setup.md)** — Insérez votre URL et affinez chaque option dans un simple fichier de config — sans coder.
3. **[Compiler & publier](publish.md)** — Publiez votre app sur le store — vous-même, via Cloud Builder ou avec notre service de publication.

## Nouveautés

WebViewGold est mis à jour régulièrement. Consultez le journal des modifications complet [ici](https://www.webviewgold.com/changelog/android/).

## Tous les sujets, API & fonctionnalités

Tout ce que WebViewGold pour Android peut faire — chaque sujet sur sa propre page :

### Prise en main

- **[Configurer l'application web](setup-website.md)** — Préparez votre site web, PWA ou fichiers HTML locaux pour votre application Android : utilisez une URL distante, intégrez des fichiers hors ligne dans l'application ou combinez les deux avec un repli hors ligne.
- **[Configurer WebViewGold](setup.md)** — Téléchargez le modèle WebViewGold pour Android Studio, insérez votre URL et explorez toutes les options de configuration intégrées — sans aucune compétence en programmation.

### Design de l’app

- **[Icône de l'application](app-icon.md)** — Ajoutez votre icône d'application personnalisée à votre application Android WebViewGold dans Android Studio — étape par étape.
- **[Écran de démarrage](splash-screen.md)** — Personnalisez l'écran de démarrage de votre application Android WebView avec vos propres graphismes.
- **[Navigation Drawer & Footer](navigation-drawer.md)** — Ship an app-like navigation experience with the built-in Material navigation drawer and Material 3 bottom navigation bar — no changes to your website required.

### API et fonctionnalités

- **[API de gestion des URL](url-handling.md)** — Décidez quels liens s'ouvrent dans votre application Android, dans les Chrome Custom Tabs ou dans le navigateur externe.
- **[API CSS et JS personnalisés](custom-css-js.md)** — Injectez des styles CSS et du code JavaScript personnalisés dans n'importe quelle page de votre application Android WebView — idéal pour des ajustements propres à l'application.
- **[Multi API Call](multi-api-call.md)** — Appelez plusieurs APIs de données WebViewGold en une seule affectation window.location.href — idéal pour les web apps multiplateformes qui utilisent aussi la version iOS.
- **[API de géolocalisation](geolocation.md)** — Activez la géolocalisation HTML5 dans votre application Android WebView et demandez correctement les autorisations de localisation.
- **[API de notifications push](push-notifications.md)** — Envoyez des notifications push aux utilisateurs de votre application Android avec OneSignal, Firebase ou Pushwoosh — configuration, deep links et ciblage par utilisateur expliqués.
- **[API AdMob](admob.md)** — Monétisez votre application Android avec les annonces bannière et interstitielles Google AdMob — configuration et déclencheurs JavaScript.
- **[API Facebook Ads](facebook-ads.md)** — Affichez des annonces bannière et interstitielles du Facebook Audience Network dans votre application Android WebViewGold.
- **[API de téléchargement de fichiers](file-downloader.md)** — Permettez aux utilisateurs de télécharger images, PDF et autres fichiers depuis votre application web vers leur appareil Android.
- **[API vidéo native (PiP)](native-video.md)** — Lisez des vidéos nativement avec la prise en charge du Picture-in-Picture dans votre application Android WebView.
- **[API de réinitialisation](reset-app.md)** — Réinitialisez le cache, les cookies et le stockage local de votre application Android WebView d'un simple lien ou appel JavaScript.
- **[API d'indicateur de chargement](loading-sign.md)** — Affichez ou masquez l'indicateur de chargement natif à la demande et personnalisez l'expérience de chargement de votre application Android.
- **[API Presse-papiers](clipboard.md)** — Copiez du texte dans le presse-papiers Android et lisez son contenu depuis votre application web via JavaScript.
- **[API UUID](uuid.md)** — Identifiez les installations de l'application grâce à un UUID unique ajouté à votre URL WebView ou récupéré via JavaScript.
- **[API Lampe torche](flashlight.md)** — Contrôlez la lampe torche de l'appareil depuis votre application web avec de simples liens JavaScript dans WebViewGold pour Android.
- **[App Links / Deep Linking](app-links.md)** — Ouvrez les liens vers votre domaine directement dans votre application Android grâce aux App Links et au deep linking par schéma d'URL personnalisé.
- **[API ShareIntent](share-intent.md)** — Recevez le contenu partagé depuis d'autres applications Android directement dans votre application WebView via les Share Intents.
- **[API de dialogue de partage](app-sharing-dialog.md)** — Déclenchez le dialogue de partage natif d'Android depuis votre application web pour permettre aux utilisateurs de partager votre application ou n'importe quelle URL.
- **[API de notation In-App](in-app-rating.md)** — Demandez un avis Google Play à vos utilisateurs : déclenchez le dialogue natif « Noter cette app » via rateapp:// depuis votre web app ou laissez WebViewGold le proposer automatiquement.
- **[API d'achats intégrés](in-app-purchases.md)** — Vendez des biens numériques et des abonnements dans votre application Android WebView avec Google Play Billing.
- **[IAP History API](iap-history.md)** — Return the user's Google Play purchase history as window.purchaseHistory so your web app can list subscriptions or unlock premium content client-side.
- **[API scanner de QR codes](qr-code-scanner.md)** — Ouvrez un scanner de QR codes natif depuis votre application web et traitez les résultats via URL ou JavaScript.
- **[API mode de scan](scanning-mode.md)** — Ajustez finement le comportement de scan de la caméra du scanner de QR codes et de codes-barres dans WebViewGold pour Android.
- **[API scanner de codes-barres](barcode-scanner.md)** — Scannez les codes-barres EAN, UPC et autres nativement dans votre application Android WebView et transmettez les résultats à votre application web.
- **[API de capture d'écran](take-screenshot.md)** — Capturez une capture d'écran de l'écran actuel de l'application par programmation, puis partagez-la ou enregistrez-la — via JavaScript.
- **[API de vérification de version](app-version-check.md)** — Détectez la version installée de l'application depuis votre application web et invitez les utilisateurs à effectuer la mise à jour si nécessaire.
- **[API Contacts](contacts.md)** — Accédez au carnet d'adresses de l'appareil depuis votre application web : lisez les contacts avec l'autorisation de l'utilisateur dans WebViewGold pour Android.
- **[API d'interface dynamique](dynamic-ui.md)** — Modifiez dynamiquement les éléments d'interface natifs, comme la couleur de la barre d'état, depuis votre application web sous Android.
- **[API de retour haptique](haptic-feedback.md)** — Déclenchez un retour haptique par vibration native depuis votre application web pour une sensation d'application native sous Android.
- **[Plugin NFC](nfc.md)** — Lisez les tags NFC nativement dans votre application Android WebView et transmettez les données du tag à votre application web.
- **[Open App Settings API](open-app-settings.md)** — Send the user straight to the system App-info screen from your web app to manage permissions, notifications, storage, or force-stop your Android app.
- **[Reconnect API](reconnect.md)** — Reload the last online URL from your offline / fallback HTML page — the perfect "Try again" button for your custom offline screen.
- **[Read/Write Value API](read-write-value.md)** — Persist small strings on the device from JavaScript and read them back — for theme, language, session tokens, or onboarding state.
- **[Biometric Auth API](biometric-auth.md)** — Prompt fingerprint or face authentication with the native Android BiometricPrompt directly from your web app.
- **[Document Scanner](document-scanner.md)** — Add a Scan document option to the file upload dialog — the user scans up to 5 pages and your web app receives a PDF like any other upload.
- **[Printer API](printer.md)** — Send a remote image or PDF to the Android system print dialog — Wi-Fi printers, cloud print, or Save-as-PDF, straight from your web app.
- **[Health Connect API](health-connect.md)** — Read and write Android Health Connect records from JavaScript — mirrors the WebViewGold HealthKit API on iOS so one web app covers both platforms.

### Compiler et publier

- **[Firebase Crashlytics](crashlytics.md)** — Ship crash reports and non-fatal events to your Firebase project, with runtime opt-in / opt-out from your web app.
- **[Compiler et publier](publish.md)** — Publiez votre application WebView sur le Google Play Store : service de publication complet, procédure manuelle et modification du nom de package.

### Plus

- **[Crédits et licences](credits.md)** — Conditions de licence de WebViewGold pour Android, cas où une Envato Extended License est nécessaire, et crédits open source.
- **[Noter WebViewGold](rate.md)** — WebViewGold vous plaît ? Notez-le sur CodeCanyon en quelques secondes — c'est ce qui permet aux mises à jour de continuer.
- **[Versions iOS et macOS](more-platforms.md)** — Déployez votre application sur davantage de plateformes : obtenez WebViewGold pour iOS et macOS et réutilisez la même application web.
- **[Support et contact](support.md)** — Obtenez de l'aide rapidement : parcourez le Centre de support WebViewGold, contactez directement notre équipe ou demandez un développement d'application sur mesure professionnel made in Germany.

## Une app web, toutes les plateformes

Réutilisez le même site web pour des apps iOS, Android & macOS avec WebViewGold.

- [WebViewGold pour iOS](../ios/README.md)
- [WebViewGold pour macOS](../macos/README.md)

**Langues :** [🇺🇸 English](../../android/README.md) · [🇩🇪 Deutsch](../../de/android/README.md) · **🇫🇷 Français** · [🇪🇸 Español](../../es/android/README.md) · [🇨🇳 中文](../../zh/android/README.md)

> [!TIP]
> **Trop occupé ? Nous configurons votre app pour vous.** Notre équipe configure, compile & soumet votre app WebViewGold — clé en main, délai rapide, Made in Germany. [Faire configurer mon app →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_android_doc_online)
>
> **Compilez dans votre navigateur :** Pas de Mac, pas d’IDE : le **WebViewGold Cloud Builder** configure, compile & met en ligne votre app. [Découvrir Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=android_docs)
