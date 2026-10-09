---
title: "Installer et configurer WebViewGold pour Android – Documentation WebViewGold pour Android"
description: "Téléchargez le modèle WebViewGold pour Android Studio, insérez votre URL et explorez toutes les options de configuration intégrées — sans aucune compétence en programmation."
lang: "fr"
product: "WebViewGold pour Android"
platform: "Android"
category: "Prise en main"
slug: "setup"
canonical_url: "https://www.webviewgold.com/fr/docs/android/setup/"
keywords:
  - "Configurer WebViewGold"
  - "WebViewGold pour Android"
  - "convertir un site web en app"
  - "documentation d’app WebView"
  - "SDK WebView Android"
  - "PWA en app"
  - "HTML en app"
  - "pont JavaScript"
last_updated: "2026-10-09"
---

# Installer et configurer WebViewGold pour Android – WebViewGold pour Android

> **Résumé :** Téléchargez le modèle WebViewGold pour Android Studio, insérez votre URL et explorez toutes les options de configuration intégrées — sans aucune compétence en programmation.

[Documentation](../README.md) › [WebViewGold pour Android](README.md) › Configurer WebViewGold

**Plateforme :** Android · **Catégorie :** Prise en main · **Version en ligne :** [www.webviewgold.com/fr/docs/android/setup/](https://www.webviewgold.com/fr/docs/android/setup/)

---

**Téléchargez**
le modèle d'application WebViewGold pour Android Studio
**[ici](https://www.webviewgold.com/download/android).**
[![Achetez le modèle d'application WebView pour Android Studio](../../assets/android/img/cart.webp)](https://www.webviewgold.com/download/android)

> [!NOTE]
> Vous souhaitez créer votre application sans installer Android Studio ? Le [**WebViewGold Cloud Builder**](https://www.webviewgold.com/cloud-builder?ref=android_docs) (module payant) vous permet de configurer, compiler et téléverser votre application vers le Play Store directement depuis votre navigateur.
>
> [![Regarder la vidéo: Installer et configurer WebViewGold pour Android](https://img.youtube.com/vi/nzgCkydN9OM/hqdefault.jpg)](https://www.youtube.com/watch?v=nzgCkydN9OM)

Téléchargez [**Android Studio**](https://developer.android.com/studio) si vous ne l'avez pas encore installé.\
Ensuite, ouvrez **Android Studio** :\
![Écran d'accueil d'Android Studio](../../assets/android/img/androidstudio2020.webp)

Choisissez **Open** :\
![Bouton Importer un projet](../../assets/android/img/androidstudio_welcome2022.webp)\
Sélectionnez votre dossier **AndroidStudioSource** et patientez jusqu'à ce que le projet soit entièrement chargé :\
![Sélecteur de fichiers Android Studio](../../assets/android/img/filepicker.webp)\
Ensuite, ouvrez le fichier **Config.java** pour modifier les principaux paramètres de configuration (URL, gestion des URL, UserAgent, dialogues). Consultez notre [chaîne YouTube](https://www.youtube.com/channel/UChuOoCMcXP_8SQPbZyXTPjA?sub_confirmation=1) pour des tutoriels de configuration spécifiques. N'oubliez pas de saisir votre [code d'achat Envato/CodeCanyon](https://help.market.envato.com/hc/en-us/articles/202822600-Where-Is-My-Purchase-Code-) dans le champ **PURCHASECODE** pour chaque application que vous publiez. Une licence par produit final personnalisé est requise. Pour plus d'informations sur la licence de votre achat CodeCanyon, veuillez consulter : [https://codecanyon.net/licenses/standard](https://codecanyon.net/licenses/standard?ref=onlineappcreator)\
Le document de configuration principal **Config.java** se présente comme suit : \
![Config.java vous permet de configurer la plupart des paramètres directement dans le document](../../assets/android/img/config.webp)

Configurer des applications avec WebViewGold est **très facile** et ne nécessite aucune connaissance en programmation. Consultez cette **vue d'ensemble** des options de configuration intégrées dans le fichier **Config.java** :

[![Regarder la vidéo: Installer et configurer WebViewGold pour Android](https://img.youtube.com/vi/5rlknsdIORE/hqdefault.jpg)](https://www.youtube.com/watch?v=5rlknsdIORE)

| Paramètre | Valeur | Description |
| --- | --- | --- |
| HOST | **valeur requise** | L'hôte de votre domaine sans le préfixe https:// ou http:// (par exemple "www.example.org"). Par défaut, WebViewGold pour Android autorise les contenus HTTPS et HTTP. Cependant, si vous préférez renforcer la sécurité de l'application en autorisant uniquement les contenus HTTPS, vous pouvez [modifier ce paramètre](https://www.webviewgold.com/support-center/knowledgebase/how-to-prevent-non-https-connections-in-webviewgold-for-android-switching-usescleartexttraffic-from-true-to-false/) (et/ou envisager l'option 'BLOCK_SELF_SIGNED_AND_FAULTY_SSL_CERTS'). |
| HOME_URL | **valeur requise** | L'URL complète de votre WebView (par exemple "https://www.example.org/app.html") qui doit être chargée dans la WebView. Par défaut, WebViewGold pour Android autorise les contenus HTTPS et HTTP. Cependant, si vous préférez renforcer la sécurité de l'application en autorisant uniquement les contenus HTTPS, vous pouvez [modifier ce paramètre](https://www.webviewgold.com/support-center/knowledgebase/how-to-prevent-non-https-connections-in-webviewgold-for-android-switching-usescleartexttraffic-from-true-to-false/) (et/ou envisager l'option 'BLOCK_SELF_SIGNED_AND_FAULTY_SSL_CERTS'). |
| USE_LOCAL_HTML_FOLDER | **true** ou **false** | Définissez sur *true* pour utiliser le fichier HTML local "index.html" au lieu de l'URL distante de la WebView |
| FALLBACK_USE_LOCAL_HTML_FOLDER_IF_OFFLINE | **true** ou **false** | Définissez sur *true* si vous souhaitez utiliser le dossier "local-html" lorsque l'utilisateur est hors ligne et l'URL distante lorsqu'il est en ligne |
| ACTIVATE_PROGRESS_BAR | **true** ou **false** | Définissez sur *false* pour désactiver l'indicateur de progression/de chargement |
| PHONE_ORIENTATION | valeur (orientation) | Définissez l'orientation du téléphone sur "portrait", "landscape" ou "auto" |
| TABLET_ORIENTATION | valeur (orientation) | Définissez l'orientation de la tablette sur "portrait", "landscape" ou "auto" |
| USER_AGENT | optionnel | Définissez un UserAgent personnalisé pour les requêtes web (ou laissez ce champ vide pour utiliser l'UserAgent Android par défaut) |
| HARDWARE_ACCELERATION | **true** ou **false** | Définissez sur *true* pour activer l'accélération matérielle ; elle peut améliorer les performances de rendu mais aussi augmenter l'utilisation de la mémoire et provoquer des problèmes de compatibilité avec certains contenus |
| APPEND_LANG_CODE | **true** ou **false** | Définissez sur *true* si vous souhaitez enrichir la requête URL avec la langue du système, sous la forme ?webview_language=LANGUAGE CODE (par exemple ?webview_language=EN pour les utilisateurs anglophones) |
| AUTO_REFRESH_ENABLED | **true** ou **false** | Définissez sur *true* si vous souhaitez que la WebView actualise automatiquement son contenu lorsque l'application revient au premier plan depuis l'arrière-plan. |
| EXTERNAL_LINK_HANDLING_OPTIONS | **0** ou **1** ou **2** | Définissez sur (0) pour ouvrir les liens externes dans l'application par défaut ; (1) pour TOUJOURS les ouvrir dans un nouvel onglet (un navigateur intégré supplémentaire) ; (2) pour TOUJOURS les ouvrir dans un autre navigateur |
| BROWSER_WHITELIST | Liste | Ajoutez ici les domaines qui doivent **toujours** être ouverts dans le navigateur externe, quelle que soit la valeur de l'option **EXTERNAL_LINK_HANDLING_OPTIONS**. Pour ajouter un autre domaine, insérez un autre hôte comme suit : ["www.alwaysopeninchrome.com", "www.google.com"]. Veuillez saisir l'hôte exactement tel que vous y renvoyez (mais jamais avec http/https). |
| BROWSER_BLACKLIST | Liste | Ajoutez ici les domaines qui ne doivent **jamais** être ouverts dans le navigateur externe, quelle que soit la valeur de l'option **EXTERNAL_LINK_HANDLING_OPTIONS**. Pour ajouter un autre domaine, insérez un autre hôte comme suit : ["www.neveropeninchrome.com", "www.google.com"]. Veuillez saisir l'hôte exactement tel que vous y renvoyez (mais jamais avec http/https). |
| SPECIAL_LINK_HANDLING_OPTIONS | **0** ou **1** ou **2** | Définissez sur (0) pour ouvrir les liens spéciaux dans l'application ; (1) dans un nouvel onglet (un navigateur intégré supplémentaire) ; (2) dans un autre navigateur ; REMARQUE : les liens spéciaux ont une cible "_blank" ou se terminent par "#" ; ceci prime sur *EXTERNAL_LINK_HANDLING_OPTIONS* si le lien est également externe |
| ALWAYS_OPEN_IN_INAPP_TAB | liste | Ajoutez les préfixes d'URL que vous souhaitez TOUJOURS ouvrir dans un onglet intégré à l'application (par exemple, {"https://www.google.com", "https://www.example.com/page"}), quelle que soit la valeur de **EXTERNAL_LINK_HANDLING_OPTIONS**. |
| NEVER_OPEN_IN_INAPP_TAB | liste | Ajoutez les préfixes d'URL que vous ne souhaitez JAMAIS ouvrir dans un onglet intégré à l'application (par exemple, {"https://www.google.com", "https://www.example.com/page"}), quelle que soit la valeur de **EXTERNAL_LINK_HANDLING_OPTIONS**. |
| QR_CODE_URL_OPTIONS | **0** ou **1** ou **2** ou **3** ou **4** | Définissez sur (0) pour ouvrir une URL scannée depuis un QR code dans l'application ; (1) dans un onglet intégré à l'application ; (2) dans un nouveau navigateur ; (3) dans un onglet intégré à l'application si externe ; (4) dans un nouveau navigateur si externe |
| AUTO_INJECT_VARIABLES | **true** ou **false** | Définissez sur *true* pour définir automatiquement les variables JavaScript ; cela évite d'avoir à appeler manuellement des méthodes telles que get-uuid://. Actuellement, cela prend en charge le chargement de la version de l'application, des identifiants d'abonnement OneSignal et Firebase, ainsi que l'UUID |
| CLEAR_CACHE_ON_STARTUP | **true** ou **false** | Définissez sur *true* pour vider le cache et les cookies de la WebView à chaque démarrage de l'application et ne pas utiliser les versions en cache de votre application web/site web |
| CLEAR_CACHE_ON_EXIT | **true** ou **false** | Définissez sur *true* pour vider le cache et les cookies de la WebView lors de la fermeture complète de l'application (vous pouvez également activer *CLEAR_CACHE_ON_STARTUP*, car des différences entre les systèmes peuvent affecter la fiabilité) |
| COOKIE_ON_LAUNCH | **true** ou **false** | Définissez-le sur *true* pour ajouter un cookie personnalisé au WebView au lancement de l'application |
| COOKIE_ON_LAUNCH_NAME | valeur texte | Personnalisez le nom du cookie ajouté au lancement (nécessite COOKIE_ON_LAUNCH sur *true*) |
| COOKIE_ON_LAUNCH_VALUE | valeur texte | Personnalisez la valeur du cookie ajouté au lancement (nécessite COOKIE_ON_LAUNCH sur *true*) |
| COOKIE_ON_LAUNCH_IS_SECURE | **true** ou **false** | Définissez-le sur *true* pour marquer le cookie de lancement comme sécurisé (HTTPS uniquement) |
| IS_DEEP_LINKING_ENABLED | **true** ou **false** | Définissez sur *true* pour activer le deep linking |
| IS_CUSTOM_SCHEME_ENABLED | **true** ou **false** | Définissez sur *true* si vous souhaitez accepter les deeplinks à schéma personnalisé tels que `webviewgold://` |
| CUSTOM_DEEPLINK_SCHEME | **true** ou **false** | Personnalisez ici le préfixe du schéma de deeplinking, ainsi que dans AndroidManifest.xml |
| OPEN_NOTIFICATION_URLS_IN_SYSTEM_BROWSER | **true** ou **false** | Définissez sur *true* pour ouvrir les URL de deep linking des notifications dans le navigateur système au lieu de votre application |
| SPLASH_SCREEN_ACTIVATED | **true** ou **false** | Définissez sur *true* pour activer l'écran de démarrage |
| SPLASH_TIMEOUT | valeur numérique (millisecondes) | Définissez le délai d'affichage de l'écran de démarrage en *millisecondes* (l'écran de chargement s'affichera après cette durée si l'URL d'accueil est encore en cours de chargement) |
| SPLASH_FADE_OUT | valeur numérique (millisecondes) | Durée de l'animation de fondu sortant de l'écran de démarrage en millisecondes. Cette animation démarre une fois que toutes les autres temporisations sont terminées. Définissez sur 0 pour désactiver l'effet de fondu sortant. |
| SPLASH_MIN_TIME | valeur numérique (millisecondes) | Durée minimale (en ms) d'affichage de l'écran de démarrage, utilisée uniquement si *REMAIN_SPLASH_OPTION* est défini sur *true* ; si *SPLASH_MIN_TIME* dépasse cette valeur, l'écran de démarrage restera affiché pendant *SPLASH_MIN_TIME*. Dans ce cas, cette valeur sera ignorée au profit de la durée la plus longue. |
| REMAIN_SPLASH_OPTION | **true** ou **false** | Définissez sur *true* pour afficher l'écran de démarrage jusqu'à ce que l'URL d'accueil ait fini de se charger (prime sur *SPLASH_TIMEOUT*) |
| SCALE_SPLASH_IMAGE | valeur en pourcentage [0-100] | Définissez la taille de l'image de l'écran de démarrage par rapport à la plus petite largeur/hauteur de l'appareil ; plage en pourcentage [0-100] ; Attention : valeur = 0 masquera complètement l'image |
| blackStatusBarText | **true** ou **false** | Définissez sur *true* pour un texte noir dans la barre d'état ; sur *false* pour un texte blanc ; utilisez 'colorPrimaryDark' dans style.xml pour choisir la couleur de fond de la barre d'état |
| TRANSPARENT_STATUS_BAR | **true** ou **false** | Définissez sur *true* pour une barre d'état transparente ; sur *false* pour une barre d'état opaque ; utilisez 'colorPrimaryDark' dans style.xml pour choisir la couleur de fond de la barre d'état |
| enableBioMetricAuth | **true** ou **false** | Définissez sur *true* pour activer le verrouillage de l'application (authentification biométrique) |
| PREVENT_SLEEP | **true** ou **false** | Définissez sur *true* pour empêcher l'appareil de passer en veille tant que l'application est active |
| ENABLE_SWIPE_NAVIGATE | **true** ou **false** | Définissez sur *true* pour activer la navigation en balayant vers la gauche ou vers la droite afin de revenir en arrière ou d'avancer d'une page |
| ENABLE_PULL_REFRESH | **true** ou **false** | Définissez sur *true* pour activer le rafraîchissement de la page par balayage vers le bas. Vous pouvez également appeler à tout moment `enablepulltorefresh://` ou `disablepulltorefresh://` depuis votre site web pour activer ou désactiver dynamiquement le pull-to-refresh. |
| HIDE_VERTICAL_SCROLLBAR | **true** ou **false** | Définissez sur *true* pour masquer la barre de défilement verticale |
| HIDE_HORIZONTAL_SCROLLBAR | **true** ou **false** | Définissez sur *true* pour masquer la barre de défilement horizontale |
| ENABLE_ZOOM | **true** ou **false** | Définissez sur *false* pour empêcher les fonctions de zoom pour l'utilisateur de l'application (fonctionne également via l'injection de script) |
| DISABLE_DARK_MODE | **true** ou **false** | Définissez sur *true* pour désactiver le mode sombre (ne fonctionne pas sur tous les lanceurs) |
| HIDE_NAVIGATION_BAR_IN_LANDSCAPE | **true** ou **false** | Définissez sur *true* pour masquer la barre de navigation en mode paysage |
| MAX_TEXT_ZOOM | valeur numérique | Définissez une valeur supérieure à 0 pour définir un zoom de texte maximal ; définissez sur (0) pour désactiver cette fonctionnalité.  <br> *Remarque : Petit = 85, Par défaut = 100, Grand = 115, Le plus grand = 130* |
| INPUT_SCROLL_HELPER | **true** ou **false** | Définissez sur *true* pour imposer un défilement homogène des champs de saisie (injecté par JS) |
| EXIT_APP_BY_BACK_BUTTON_ALWAYS | **true** ou **false** | Définissez sur *true* pour fermer l'application en appuyant sur le bouton retour matériel (au lieu de revenir à la page précédente) |
| EXIT_APP_BY_BACK_BUTTON_HOMEPAGE | **true** ou **false** | Définissez sur *true* pour fermer l'application en appuyant sur le bouton retour matériel lorsque l'utilisateur se trouve sur la page d'accueil (qui ne permet pas de revenir à une page précédente) |
| EXIT_APP_DIALOG | **true** ou **false** | Définissez sur *true* pour demander à l'utilisateur s'il souhaite quitter avant de fermer l'application |
| OFFLINE_SCREEN_BACKGROUND_COLOR | code couleur hexadécimal | Définissez la couleur de fond de l'écran hors ligne à l'aide d'un code couleur hexadécimal (par exemple, "#ffffff" = blanc) |
| PREVENT_SCREEN_CAPTURE | **true** ou **false** | Définissez sur *true* pour empêcher les utilisateurs de faire des captures d'écran ou d'enregistrer l'écran dans l'application. `onScreenCaptureAttempt()` sera appelé dans l'application web pour la gestion (par exemple, l'affichage d'une modale personnalisée). |
| UUID_ENHANCE_WEBVIEW_URL | **true** ou **false** | Définissez sur *true* pour ajouter le paramètre UUID 'uuid=XYZ' à la première requête URL |
| BLOCK_SELF_SIGNED_AND_FAULTY_SSL_CERTS | **true** ou **false** | Définissez sur *true* pour bloquer les contenus signés avec des certificats SSL auto-signés (par l'utilisateur) et les certificats SSL défectueux ; vous pouvez également envisager de [bloquer tous les contenus non-HTTPS](https://www.webviewgold.com/support-center/knowledgebase/how-to-prevent-non-https-connections-in-webviewgold-for-android-switching-usescleartexttraffic-from-true-to-false/) |
| BLOCK_ROOTED_DEVICES | **true** ou **false** | Définissez sur *true* pour activer la fonctionnalité de détection des appareils rootés et désactiver l'application sur ceux-ci (Remarque : la détection du root n'est pas toujours fiable et peut ne pas fonctionner sur tous les appareils) |
| LINK_DRAG_AND_DROP | **true** ou **false** | Définissez sur *false* pour désactiver le glisser-déposer des liens |
| LANDSCAPE_FULLSCREEN_VIDEO | **true** ou **false** | Définissez sur *true* pour toujours présenter les vidéos plein écran en mode paysage |
| SHOW_FIRSTRUN_DIALOG | **true** ou **false** | Définissez sur *false* pour désactiver la boîte de dialogue de premier lancement |
| SHOW_FACEBOOK_DIALOG | **true** ou **false** | Définissez sur *false* pour désactiver la boîte de dialogue "Suivre sur Facebook" |
| SHOW_RATE_DIALOG | **true** ou **false** | Définissez sur *false* pour désactiver la boîte de dialogue "Évaluer cette application" |
| RATE_DAYS_UNTIL_PROMPT | valeur numérique (jours) | Définissez le nombre minimum de jours à écouler après l'installation de l'application avant l'affichage de la boîte de dialogue "Évaluer cette application" |
| RATE_LAUNCHES_UNTIL_PROMPT | valeur numérique (lancements) | Définissez le nombre minimum de lancements de l'application avant l'affichage de la boîte de dialogue "Évaluer cette application" |
| FACEBOOK_DAYS_UNTIL_PROMPT | valeur numérique (jours) | Définissez le nombre minimum de jours à écouler après l'installation de l'application avant l'affichage de la boîte de dialogue "Suivre sur Facebook" |
| FACEBOOK_LAUNCHES_UNTIL_PROMPT | valeur numérique (lancements) | Définissez le nombre minimum de lancements de l'application avant l'affichage de la boîte de dialogue "Évaluer cette application" |
| FACEBOOK_URL | valeur (URL) | Définissez l'URL de votre page Facebook |
| ALLOW_IMAGE_DOWNLOAD | **true** ou **false** | Définissez sur *false* pour empêcher la fenêtre contextuelle "Télécharger les images" d'apparaître lors d'un appui long sur une image |
| PUSH_ENABLED | **true** ou **false** | Définissez sur *true* pour activer les notifications push OneSignal (définissez les identifiants OneSignal dans le fichier build.gradle) |
| PUSH_ENHANCE_WEBVIEW_URL | **true** ou **false** | Définissez sur *true* si vous souhaitez enrichir les requêtes URL principales de la WebView avec l'identifiant d'abonnement OneSignal au format ?onesignal_push_id=XYZ (vous pouvez également demander à tout moment l'identifiant d'abonnement OneSignal en appelant [getonesignalplayerid://](push-notifications.md) ou l'obtenir automatiquement en réglant "AUTO_INJECT_VARIABLES" sur "true" dans Config.java) |
| PUSH_RELOAD_ON_USERID | **true** ou **false** | Définissez sur *true* si la WebView doit être rechargée lorsque l'application reçoit un UserID de OneSignal (définissez les identifiants OneSignal dans le fichier build.gradle) |
| FIREBASE_PUSH_ENABLED | **true** ou **false** | Définissez sur *true* pour activer Firebase Push (remplacez d'abord google-services.json) |
| FIREBASE_PUSH_ENHANCE_WEBVIEW_URL | **true** ou **false** | Définissez sur *true* si vous souhaitez enrichir la requête URL avec ?firebase_push_id=XYZ (vous pouvez également demander à tout moment l'identifiant d'abonnement Firebase en appelant [getfirebaseplayerid://](push-notifications.md#firebaseruntime) ou l'obtenir automatiquement en réglant "AUTO_INJECT_VARIABLES" sur "true" dans Config.java) |
| PUSHWOOSH_ENABLED | **true** ou **false** | Définissez sur *true* pour activer les notifications push Pushwoosh (définissez les identifiants Pushwoosh dans les fichiers AndroidManifest.xml et string.xml) |
| PUSHWOOSH_ENHANCE_WEBVIEW_URL | **true** ou **false** | Définissez sur *true* si vous souhaitez enrichir la requête URL avec ?pushwoosh_id=XYZ (définissez les identifiants Pushwoosh dans les fichiers AndroidManifest.xml et string.xml) |
| SHOW_ADSENSE_AD | **true** ou **false** | Définissez sur *true* pour activer la prise en charge des annonces web AdSense (indépendamment des annonces AdMob) |
| SHOW_BANNER_AD | **true** ou **false** | Définissez sur *true* si vous souhaitez afficher des bannières AdMob (définissez les identifiants AdMob dans le fichier strings.xml) |
| SHOW_FULL_SCREEN_AD | **true** ou **false** | Définissez sur *true* si vous souhaitez afficher des annonces interstitielles plein écran AdMob après X clics sur le site (définissez les identifiants AdMob dans le fichier strings.xml) |
| SHOW_APP_OPEN_AD | **true** ou **false** | Définissez-le sur *true* pour afficher des [annonces app open AdMob](admob.md#appopenads) au démarrage à froid (depuis le splash du launcher) et au retour depuis l'arrière-plan (configurez admob_app_open_id dans le fichier strings.xml) |
| ASK_FOR_AD_CONSENT | **true** ou **false** | Définissez sur *false* si vous souhaitez désactiver la gestion du consentement Google pour AdMob (consultez au préalable <https://support.google.com/admob/answer/13554116>) |
| SHOW_AD_AFTER_X | valeur (rechargements de site) | Définissez le nombre X de clics sur le site pour les annonces interstitielles AdMob (définissez les identifiants AdMob dans le fichier strings.xml) |
| INCREMENT_WITH_TAPS | **true** ou **false** | Définissez sur *true* pour permettre aux appuis normaux sur l'écran d'incrémenter SHOW_AD_AFTER_X |
| USE_FACEBOOK_ADS | **true** ou **false** | Définissez sur *true* pour utiliser les annonces Facebook Audience Network au lieu des annonces AdMob (définissez les identifiants d'annonce dans le fichier strings.xml) |
| ENABLE_REWARDED_ADS | **true** ou **false** | Définissez sur *true* pour activer les annonces avec récompense AdMob. Doit être défini sur *true* même pour une activation manuelle des annonces. (Définissez les identifiants d'annonce dans le fichier strings.xml.) |
| USE_REWARDED_ADS_WHERE_POSSIBLE | **true** ou **false** | Définissez sur *true* pour afficher des annonces avec récompense AdMob à la place des annonces interstitielles AdMob, par exemple après x appuis, etc. Conservez la valeur *false* si leur activation doit être gérée via le code de votre site web. Notez que cela nécessite également que SHOW_FULL_SCREEN_AD soit défini sur *true* pour les remplacer. |
| AD_TRIGGER_URLS | optionnel | Ajoutez ici des mots-clés déclencheurs de page ; leur présence dans une URL déclenche des annonces interstitielles (par exemple, "thanks.html", "welcome.html", "/thank-you/", "next-step.php") |
| REVENUECAT_API_KEY | optionnel | Votre clé API RevenueCat (inscrivez-vous d'abord via [tinyurl.com/register-revenuecat](https://tinyurl.com/register-revenuecat), puis suivez [tinyurl.com/api-key-revenuecat](https://tinyurl.com/api-key-revenuecat) pour la trouver) |
| REVENUECAT_PROJECT_ID | optionnel | Votre ID de projet RevenueCat (inscrivez-vous d'abord via [tinyurl.com/register-revenuecat](https://tinyurl.com/register-revenuecat), puis suivez [tinyurl.com/project-id-revenuecat](https://tinyurl.com/project-id-revenuecat) pour le trouver) |
| downloadableExtension | liste | Ajoutez les formats de fichier qui doivent déclencher la fonctionnalité de téléchargement (par exemple, .pdf, .docx, ...) |
| AUTO_DOWNLOAD_FILES | **true** ou **false** | Définissez sur *true* si vous souhaitez activer la fonctionnalité de téléchargement basée sur les en-têtes HTTP Content-Disposition, quels que soient les formats de fichier répertoriés dans la variable downloadableExtension ci-dessus |
| GOOGLE_LOGIN_HELPER_TRIGGERS | liste | Définissez les préfixes d'URL qui se chargent pendant la connexion Google à votre site web ; ils servent de déclencheur pour l'assistant |
| FACEBOOK_LOGIN_HELPER_TRIGGERS | liste | Définissez les préfixes d'URL qui se chargent pendant la connexion Facebook à votre site web ; ils servent de déclencheur pour l'assistant |
| HOME_URL_LOGOUT | valeur (URL) | Définissez l'URL de déconnexion pour effacer les cookies de connexion (facultatif) |
| MANUAL_COOKIE_SYNC | **true** ou **false** | Définissez sur *true* pour activer l'outil de synchronisation manuelle des cookies. À utiliser si vous avez besoin que les cookies soient synchronisés à intervalles *inférieurs* à 30 secondes ou si quelque chose lié aux cookies ne fonctionne pas autrement. Consultez également les remarques sur les cookies [ici](https://www.webviewgold.com/support-center/knowledgebase/will-cookies-work-will-the-login-of-my-website-web-app-still-work/). |
| COOKIE_SYNC_TIME | valeur numérique (millisecondes) | Définissez à quelle fréquence les cookies doivent se synchroniser avec l'application, en millisecondes (ms) |
| MANUAL_COOKIE_SYNC_TRIGGERS | liste | Définissez les préfixes d'URL pour lesquels vous souhaitez utiliser l'outil de synchronisation manuelle des cookies. Si MANUAL_COOKIE_SYNC_TRIGGERS est vide, il vérifiera automatiquement chaque page. Exemple : {"https://example.com/login", "https://example.com/data"} |
| USE_CUSTOM_HEADERS | **true** ou **false** | Définissez-le sur *true* pour injecter des en-têtes HTTP personnalisés dans chaque navigation d'URL ; définissez les noms et valeurs des en-têtes dans la map *customHeaders* juste en dessous de cette option dans Config.java |
| requireLocation | **true** ou **false** | Définissez sur *false* si vous n'avez PAS besoin des services de localisation/coordonnées GPS ; n'oubliez pas de supprimer également les entrées correspondantes dans *AndroidManifest.xml* si vous souhaitez garantir la suppression complète de cette autorisation dans l'application ; consultez également l'[utilisation de la localisation en arrière-plan (!)](geolocation.md) |
| requireBackgroundLocation | **true** ou **false** | Définissez sur *false* si les services de localisation en arrière-plan sont requis. Si cette option est définie sur *false*, veillez à décommenter également les blocs `android.permission.FOREGROUND_SERVICE_LOCATION` et `.GPSService` dans `AndroidManifest.xml` (recherchez ces termes dans le fichier). Ce paramètre n'est effectif que si `requireLocation` est également défini sur *true*. |
| requireStorage | **true** ou **false** | Définissez sur *false* si vous n'avez PAS besoin d'API liées aux téléchargements ou aux envois ; n'oubliez pas de supprimer également les entrées correspondantes dans *AndroidManifest.xml* si vous souhaitez garantir la suppression complète de cette autorisation dans l'application |
| requireCamera | **true** ou **false** | Définissez sur *false* si vous n'avez PAS besoin d'API liées aux images ou vidéos de la caméra ; n'oubliez pas de supprimer également les entrées correspondantes dans *AndroidManifest.xml* si vous souhaitez garantir la suppression complète de cette autorisation dans l'application |
| requireRecordAudio | **true** ou **false** | Définissez sur *false* si vous n'avez PAS besoin d'API liées à l'enregistrement audio ; n'oubliez pas de supprimer également les entrées correspondantes dans *AndroidManifest.xml* si vous souhaitez garantir la suppression complète de cette autorisation dans l'application |
| filePickerMode | valeur numérique | Options de téléversement de fichiers : (0) caméra et galerie ; (1) caméra uniquement ; (2) galerie uniquement. |

Ouvrez le fichier **strings.xml** pour modifier le nom de l'application et les chaînes de texte :\
![Fichier string.xml pour modifier les légendes textuelles](../../assets/android/img/strings.webp)

**Applications multilingues :** Pour modifier les traductions – y compris celles par défaut en allemand et en espagnol – ou pour créer de nouvelles traductions supplémentaires pour ces chaînes, cliquez avec le bouton droit sur le dossier "strings" dans Android Studio et sélectionnez "Open Translations Editor" :\
![Prise en charge multilingue pour votre application WebView sur Android](../../assets/android/img/translations.webp)

Ouvrez le fichier **dimens.xml** pour modifier la mise en forme du texte :\
![Utilisez dimens.xml pour redimensionner les objets et le texte](../../assets/android/img/screenshot_Dimens.webp)

---

## Continuer la lecture

- ← Précédent : [Configurer l'application web](setup-website.md)
- Suivant → : [Icône de l'application](app-icon.md)
- Même fonctionnalité sur les autres plateformes : [iOS – Configurer WebViewGold](../ios/setup.md) · [macOS – Configuration de WebViewGold](../macos/setup.md)
- Langues : [🇺🇸 English](../../android/setup.md) · [🇩🇪 Deutsch](../../de/android/setup.md) · **🇫🇷 Français** · [🇪🇸 Español](../../es/android/setup.md) · [🇨🇳 中文](../../zh/android/setup.md)

> [!TIP]
> **Trop occupé ? Nous configurons votre app pour vous.** Notre équipe configure, compile & soumet votre app WebViewGold — clé en main, délai rapide, Made in Germany. [Faire configurer mon app →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_android_doc_online)
>
> **Compilez dans votre navigateur :** Pas de Mac, pas d’IDE : le **WebViewGold Cloud Builder** configure, compile & met en ligne votre app. [Découvrir Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=android_docs)
