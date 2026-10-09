---
title: "Installer et configurer WebViewGold pour iOS – Documentation WebViewGold pour iOS"
description: "Téléchargez le template Xcode de WebViewGold, insérez votre URL dans Config.swift et explorez toutes les options de configuration intégrées, sans aucune compétence en programmation."
lang: "fr"
product: "WebViewGold pour iOS"
platform: "iOS"
category: "Prise en main"
slug: "setup"
canonical_url: "https://www.webviewgold.com/fr/docs/iOS/setup/"
keywords:
  - "Configurer WebViewGold"
  - "WebViewGold pour iOS"
  - "convertir un site web en app"
  - "documentation d’app WebView"
  - "SDK WebView iOS"
  - "PWA en app"
  - "HTML en app"
  - "pont JavaScript"
last_updated: "2026-10-09"
---

# Installer et configurer WebViewGold pour iOS – WebViewGold pour iOS

> **Résumé :** Téléchargez le template Xcode de WebViewGold, insérez votre URL dans Config.swift et explorez toutes les options de configuration intégrées, sans aucune compétence en programmation.

[Documentation](../README.md) › [WebViewGold pour iOS](README.md) › Configurer WebViewGold

**Plateforme :** iOS · **Catégorie :** Prise en main · **Version en ligne :** [www.webviewgold.com/fr/docs/iOS/setup/](https://www.webviewgold.com/fr/docs/iOS/setup/)

---

**Téléchargez** le modèle d'application WebViewGold pour iOS **[ici](https://www.webviewgold.com/download/ios)**.\
[![Achetez le modèle d'application WebView pour iOS/Xcode](../../assets/ios/img/cart.webp)](https://www.webviewgold.com/download/ios)

> [!NOTE]
> Vous préférez éviter d'installer un logiciel ? Le [**WebViewGold Cloud Builder**](https://www.webviewgold.com/cloud-builder?ref=ios_docs) (module payant) vous permet de configurer, compiler et téléverser votre application directement depuis votre navigateur, sans ouvrir Xcode.
>
> [![Regarder la vidéo: Installer et configurer WebViewGold pour iOS](https://img.youtube.com/vi/nzgCkydN9OM/hqdefault.jpg)](https://www.youtube.com/watch?v=nzgCkydN9OM)

Après avoir téléchargé le fichier .zip de WebViewGold sur CodeCanyon, il existe **deux options de configuration** pour Xcode. L'option à choisir dépend du fait que vous possédiez ou non un Mac :

**a) Vous n'utilisez aucun système Mac :**\
Si vous ne possédez pas de Mac pour exécuter l'application Xcode requise, consultez [MacInCloud](https://www.macincloud.com) qui vous permet de louer un Mac virtuel en ligne (nous ne sommes pas affiliés au fournisseur de ce service). Grâce à ce service, vous pouvez compiler vos applications iOS basées sur WebViewGold, même sans utiliser de Mac. De plus, le [**WebViewGold Cloud Builder**](https://www.webviewgold.com/cloud-builder?ref=ios_docs) (module payant) vous permet de configurer, compiler et téléverser votre application directement depuis votre navigateur, sans Mac. \
**OU**\
**b) Vous utilisez un système Mac :**\
Téléchargez et installez l'application **Xcode** depuis le [**Mac App Store**](https://apps.apple.com/de/app/xcode/id497799835?mt=12). WebViewGold s'exécute nativement sur les Mac Intel et Apple Silicon — vous pouvez donc compiler et tester votre application directement avec le simulateur iOS standard.

**C'est fait, Xcode est prêt pour WebViewGold !**\
Si Xcode est déjà en cours d'exécution, veuillez le quitter complètement (*Commande/CMD* + *Q*). Ouvrez ensuite **WebViewGold.xcworkspace** (au lieu de WebView.xcodeproj) :\
![Veillez à sélectionner le bon fichier de projet WebView lors de l'ouverture du projet Xcode](../../assets/ios/img/file.webp)

Dans [Xcode](https://developer.apple.com/xcode/), ouvrez **Config.swift** et vous verrez un document ressemblant à celui-ci :\
![La configuration est facile grâce au fichier de configuration Config.swift](../../assets/ios/img/Configswift-img.webp)\
C'est ici que vous pouvez configurer votre application facilement. Configurer des applications avec WebViewGold est **très facile** et ne nécessite aucune connaissance en programmation. N'oubliez pas d'ajouter votre [code d'achat Envato/CodeCanyon](https://help.market.envato.com/hc/en-us/articles/202822600-Where-Is-My-Purchase-Code-) dans le champ **purchasecode** pour chaque application que vous publiez. Une licence par produit final personnalisé est requise. Informations sur la licence de votre achat CodeCanyon : [https://codecanyon.net/licenses/standard](https://codecanyon.net/licenses/standard?ref=onlineappcreator)

Veuillez consulter cette **vue d'ensemble** de toutes les options de configuration intégrées :

[![Regarder la vidéo: Installer et configurer WebViewGold pour iOS](https://img.youtube.com/vi/E4D-Q_FhEOM/hqdefault.jpg)](https://www.youtube.com/watch?v=E4D-Q_FhEOM)

| Paramètre | Valeur | Description |
| --- | --- | --- |
| purchasecode | **valeur requise** | Saisissez votre code d'achat Envato/CodeCanyon pour cette application |
| app_admin_email | optionnel | Adresse e-mail pour recevoir les mises à jour de statut (laissez la valeur par défaut pour désactiver) |
| host | **valeur requise** | L'hôte de votre domaine (par exemple, "example.org"). Par défaut, WebViewGold pour iOS autorise les contenus HTTPS et HTTP. Cependant, si vous préférez renforcer la sécurité de l'application en autorisant uniquement les contenus HTTPS, vous pouvez [modifier ce paramètre](https://www.webviewgold.com/support-center/knowledgebase/how-to-prevent-non-https-connections-in-webviewgold-for-ios-removing-nsallowsarbitraryloadsinwebcontent-from-info-plist/) (et/ou envisager l'option 'blockfaultyandselfsignedhttpscerts') |
| webviewurl | **valeur requise** | L'URL complète de votre WebView (par exemple, "example.org/app.html") qui doit être chargée dans la WebView. Par défaut, WebViewGold pour iOS autorise les contenus HTTPS et HTTP. Cependant, si vous préférez renforcer la sécurité de l'application en autorisant uniquement les contenus HTTPS, vous pouvez [modifier ce paramètre](https://www.webviewgold.com/support-center/knowledgebase/how-to-prevent-non-https-connections-in-webviewgold-for-ios-removing-nsallowsarbitraryloadsinwebcontent-from-info-plist/) (et/ou envisager l'option 'blockfaultyandselfsignedhttpscerts') |
| uselocalhtmlfolder | **true** ou **false** | Définissez sur *true* pour utiliser le fichier HTML local "local-www/index.html" au lieu de l'URL distante de la WebView (veillez à ne pas créer ni utiliser de sous-dossiers dans local-www) |
| externalLinkHandlingOptions | **0**, **1** ou **2** | Définissez sur *0* pour ouvrir les liens externes dans l'application par défaut, ou sur *2* pour TOUJOURS les ouvrir dans un autre navigateur (Safari) ; consultez l'[API URL Handling](url-handling.md) |
| specialLinkHandlingOptions | **0**, **1** ou **2** | Définissez sur *0* pour ouvrir les liens spéciaux (par ex. target="_blank") dans l'application, sur *1* pour les ouvrir dans un nouvel onglet (un navigateur intégré supplémentaire), ou sur *2* pour les ouvrir dans un autre navigateur (Safari) |
| safariwhitelist | Liste | Ajoutez ici les domaines qui doivent **toujours** être ouverts dans Safari, quelle que soit la valeur de l'option **externalLinkHandlingOptions** ; pour ajouter un autre domaine, insérez un autre hôte comme suit : ["alwaysopeninsafari.com", "google.com", "m.facebook.com"]. Veuillez saisir l'hôte exactement tel que vous y renvoyez (avec ou sans www, mais toujours sans http/https). |
| safariblacklist | Liste | Ajoutez ici les domaines qui ne doivent **jamais** être ouverts dans Safari, quelle que soit la valeur de l'option **externalLinkHandlingOptions** ; pour ajouter un autre domaine, insérez un autre hôte comme suit : ["alwaysopeninsafari.com", "google.com", "m.facebook.com"]. Veuillez saisir l'hôte exactement tel que vous y renvoyez (avec ou sans www, mais toujours sans http/https). |
| alwaysOpenInInAppTab | Liste | Ajoutez ici les domaines qui doivent **toujours** s'ouvrir dans un onglet intégré, indépendamment du réglage de l'option **externalLinkHandlingOptions** |
| neverOpenInInAppTab | Liste | Ajoutez ici les domaines qui ne doivent **jamais** s'ouvrir dans un onglet intégré, indépendamment du réglage de l'option **externalLinkHandlingOptions** |
| enableBioMetricAuth | **true** ou **false** | Définissez sur *true* pour activer notre fonctionnalité de verrouillage d'application, qui nécessite une authentification par Face ID, Touch ID ou code pour accéder à l'application. Il s'agit d'une option indépendante et complémentaire à notre [API d'authentification biométrique](biometric-authentication.md) basée sur JavaScript |
| autoInjectVariable | **true** ou **false** | Définissez sur *true* pour charger automatiquement les variables JavaScript (par exemple, UUID, version de l'application, identifiants d'abonnement OneSignal et Firebase, et localisation App Store) sans avoir à appeler des URL spécifiques comme get-uuid:// (cela prend actuellement en charge la version de l'application, les identifiants d'abonnement OneSignal et Firebase, l'UUID et la localisation App Store) |
| disablecallout | **true** ou **false** | Définissez sur *true* pour supprimer la fenêtre d'aperçu de lien / de callout 3D Touch de WKWebView pour les liens (recommandé dans la plupart des cas) |
| deletecache | **true** ou **false** | Définissez sur *true* pour vider le cache et les cookies de la WebView à chaque démarrage de l'application et ne pas utiliser les versions en cache de votre application web/site web |
| deletecacheonexit | **true** ou **false** | Définissez sur *true* pour vider le cache et les cookies de la WebView lors de la fermeture complète de l'application (vous pouvez également activer *deletecache*, car les différences entre versions d'iOS peuvent affecter la fiabilité) |
| okbutton | optionnel | Définissez le libellé des boutons "OK" (traduisible via *alternatelanguage1*/*alternatelanguage2*) |
| cancelbutton | optionnel | Définissez le libellé des boutons "Annuler" (traduisible via *alternatelanguage1*/*alternatelanguage2*) |
| bigstatusbar | **true** ou **false** | Définissez sur *true* pour agrandir la taille de la barre d'état |
| hideverticalscrollbar | **true** ou **false** | Définissez sur *true* pour masquer la barre de défilement verticale |
| hidehorizontalscrollbar | **true** ou **false** | Définissez sur *true* pour masquer la barre de défilement horizontale |
| enableswipenavigation | **true** ou **false** | Définissez sur *false* pour empêcher les balayages vers la gauche/droite de déclencher une navigation arrière/avant |
| orientationiphone | "portrait", "landscape" ou "auto" | Définissez l'orientation sur iPhone sur portrait, landscape ou auto |
| orientationipad | "portrait", "landscape" ou "auto" | Définissez l'orientation sur iPad sur portrait, landscape ou auto |
| preventsleep | **true** ou **false** | Définissez sur *true* pour empêcher l'appareil de passer en veille tant que l'application est active |
| preventZoom | **true** ou **false** | Définissez sur *true* pour désactiver le zoom de l'utilisateur en injectant du code qui empêche le zoom sur le site web |
| preventoverscroll | **true** ou **false** | Définissez sur *true* pour supprimer l'animation de rebond de WKWebView (recommandé dans la plupart des cas). Définissez sur *false* si vous utilisez pull to refresh. |
| enhanceUrlUUID | **true** ou **false** | Définissez sur *true* pour ajouter le paramètre UUID 'uuid=XYZ' à la première requête URL |
| linkDragAndDrop | **true** ou **false** | Définissez sur *false* pour désactiver le glisser-déposer des liens |
| useShortcuts | **true** ou **false** | Définissez sur *true* pour enregistrer les raccourcis dynamiques définis dans Shortcuts.json |
| pulltorefresh | **true** ou **false** | Définissez sur *true* pour activer pull to refresh dans votre application. Notez que pour activer cette fonctionnalité, **preventoverscroll** doit être défini sur *false*. De plus, vous pouvez à tout moment appeler `enablepulltorefresh://` ou `disablepulltorefresh://` depuis votre site web pour activer ou désactiver dynamiquement pull-to-refresh. |
| pulltorefresh_loadingsigncolour_lightmode | Couleur | Définissez la couleur de l'indicateur de chargement de pull to refresh en mode clair |
| pulltorefresh_backgroundcolour_lightmode | Couleur | Définissez la couleur du fond de pull to refresh en mode clair |
| pulltorefresh_loadingsigncolour_darkmode | Couleur | Définissez la couleur de l'indicateur de chargement de pull to refresh en mode sombre ; nécessite iOS 13 ou une version ultérieure |
| pulltorefresh_backgroundcolour_darkmode | Couleur | Définissez la couleur du fond de pull to refresh en mode sombre ; nécessite iOS 13 ou une version ultérieure |
| useragent_iphone | optionnel | Définissez un UserAgent personnalisé sur iPhone (ou laissez le champ vide pour utiliser l'UserAgent iOS par défaut) |
| useragent_ipad | optionnel | Définissez un UserAgent personnalisé sur iPad (ou laissez le champ vide pour utiliser l'UserAgent iOS par défaut) |
| google_login_helper_triggers | optionnel | Définissez les préfixes d'URL qui se chargent pendant la connexion Google à votre site web ; ils servent de déclencheur pour l'assistant ; Exemple : ["https://accounts.google.com", "https://accounts.youtube.com"] |
| facebook_login_helper_triggers | optionnel | Définissez les préfixes d'URL qui se chargent pendant la connexion Facebook à votre site web ; ils servent de déclencheur pour l'assistant ; Exemple : ["https://www.facebook.com", "https://m.facebook.com"] |
| activatefirstrundialog | **true** ou **false** | Définissez sur *true* pour activer la boîte de dialogue "Premier lancement" |
| firstrunmessagetitle | optionnel | Définissez le titre de la boîte de dialogue "Premier lancement" (si vous le souhaitez, vous pouvez traduire cette chaîne dans deux langues supplémentaires en utilisant les chaînes 'alternatelanguage1' et 'alternatelanguage2' situées à la fin du fichier Config.swift) |
| firstrunmessage | optionnel | Définissez le message de la boîte de dialogue "Premier lancement" (si vous le souhaitez, vous pouvez traduire cette chaîne dans deux langues supplémentaires en utilisant les chaînes 'alternatelanguage1' et 'alternatelanguage2' situées à la fin du fichier Config.swift) |
| askforpushpermissionatfirstrun | **true** ou **false** | Définissez sur *true* pour demander à vos utilisateurs l'autorisation de recevoir des notifications push lors du premier lancement de votre application. Définissez sur "false" pour ne jamais demander cette autorisation ou pour la demander plus tard via un lien/bouton/redirection *registerpush://* dans votre application web |
| offlinetitle | optionnel | Définissez le titre de la boîte de dialogue Hors ligne (si vous le souhaitez, vous pouvez traduire cette chaîne dans deux langues supplémentaires en utilisant les chaînes 'alternatelanguage1' et 'alternatelanguage2' situées à la fin du fichier Config.swift) |
| offlinemsg | optionnel | Définissez le texte de la boîte de dialogue Hors ligne (si vous le souhaitez, vous pouvez traduire cette chaîne dans deux langues supplémentaires en utilisant les chaînes 'alternatelanguage1' et 'alternatelanguage2' situées à la fin du fichier Config.swift) |
| screen1 | optionnel | Définissez le libellé de texte 1 de l'écran Hors ligne (si vous le souhaitez, vous pouvez traduire cette chaîne dans deux langues supplémentaires en utilisant les chaînes 'alternatelanguage1' et 'alternatelanguage2' situées à la fin du fichier Config.swift) |
| screen2 | optionnel | Définissez le libellé de texte 2 de l'écran Hors ligne (si vous le souhaitez, vous pouvez traduire cette chaîne dans deux langues supplémentaires en utilisant les chaînes 'alternatelanguage1' et 'alternatelanguage2' situées à la fin du fichier Config.swift) |
| offlinebuttontext | optionnel | Définissez le libellé du bouton "Réessayer" (si vous le souhaitez, vous pouvez traduire cette chaîne dans deux langues supplémentaires en utilisant les chaînes 'alternatelanguage1' et 'alternatelanguage2' situées à la fin du fichier Config.swift) |
| offlinescreenautoretry | **true** ou **false** | Définissez sur *true* si l'application doit tenter automatiquement de se reconnecter chaque seconde (même sans appui sur le bouton) |
| activateratemyappdialog | **true** ou **false** | Définissez sur *true* pour activer la boîte de dialogue "Évaluer cette application sur l'App Store" |
| activatefacebookfriendsdialog | **true** ou **false** | Définissez sur *true* pour activer la boîte de dialogue "Suivre sur Facebook" |
| becomefacebookfriendstitle | optionnel | Définissez le titre de la boîte de dialogue "Suivre sur Facebook" (si vous le souhaitez, vous pouvez traduire cette chaîne dans deux langues supplémentaires en utilisant les chaînes 'alternatelanguage1' et 'alternatelanguage2' situées à la fin du fichier Config.swift) |
| becomefacebookfriendstext | optionnel | Définissez le texte de la boîte de dialogue "Suivre sur Facebook" (si vous le souhaitez, vous pouvez traduire cette chaîne dans deux langues supplémentaires en utilisant les chaînes 'alternatelanguage1' et 'alternatelanguage2' situées à la fin du fichier Config.swift) |
| becomefacebookfriendsyes | optionnel | Définissez le libellé du bouton "Oui" de la boîte de dialogue "Suivre sur Facebook" (si vous le souhaitez, vous pouvez traduire cette chaîne dans deux langues supplémentaires en utilisant les chaînes 'alternatelanguage1' et 'alternatelanguage2' situées à la fin du fichier Config.swift) |
| becomefacebookfriendsno | optionnel | Définissez le libellé du bouton "Non" de la boîte de dialogue "Suivre sur Facebook" (si vous le souhaitez, vous pouvez traduire cette chaîne dans deux langues supplémentaires en utilisant les chaînes 'alternatelanguage1' et 'alternatelanguage2' situées à la fin du fichier Config.swift) |
| becomefacebookfriendsurl | optionnel | Définissez l'URL de votre page Facebook/Instagram/YouTube/... (par exemple, "https://facebook.com/OnlineAppCreator/") |
| imagedownloadedtitle | optionnel | Définissez le titre de la boîte de dialogue "Image enregistrée dans votre galerie photo" (si vous le souhaitez, vous pouvez traduire cette chaîne dans deux langues supplémentaires en utilisant les chaînes 'alternatelanguage1' et 'alternatelanguage2' situées à la fin du fichier Config.swift) |
| imagenotfound | optionnel | Définissez le titre de la boîte de dialogue "Image introuvable" (si vous le souhaitez, vous pouvez traduire cette chaîne dans deux langues supplémentaires en utilisant les chaînes 'alternatelanguage1' et 'alternatelanguage2' situées à la fin du fichier Config.swift) |
| transparentStatusBar | **true** ou **false** | Définissez sur *true* pour rendre la barre d'état transparente, ce qui permet au contenu web de s'afficher derrière elle |
| autoAdjustSafeAreaInsets | **true** ou **false** | Définissez sur *false* si votre site web gère déjà les marges des zones sûres (à utiliser avec *transparentStatusBar*) |
| statusBarBackgroundColor | Couleur | Définissez une couleur de fond personnalisée pour la barre d'état |
| darkModeStatusBarBackgroundColor | Couleur | Définissez une couleur de fond personnalisée pour la barre d'état lorsque l'utilisateur est en mode sombre iOS |
| statusBarTextColor | **white** ou **black** | Définissez la couleur du texte de la barre d'état |
| darkModeStatusBarTextColor | **white** ou **black** | Définissez la couleur du texte de la barre d'état lorsque l'utilisateur est en mode sombre iOS |
| showNavFooter | **true** ou **false** | Définissez sur *true* pour activer la barre de pied de navigation native (configurée via FooterBar.json) |
| bottombar | **true** ou **false** | Définissez sur *true* pour activer la bottombar afin d'éviter que la barre Home (présente sur les appareils iOS sans bouton Home, par exemple l'iPhone X) ne recouvre le contenu de l'application |
| iPadBottombar | **true** ou **false** | Définissez sur *true* pour activer ÉGALEMENT la bottombar sur les iPads (qui, disposant d'écrans plus grands, ont une mise en page différente et la barre Home pourrait ne pas recouvrir le contenu, rendant la bottombar non indispensable) |
| bottombarBackgroundColor | Couleur | Définissez une couleur de fond personnalisée pour la bottombar |
| darkmodeBottombarBackgroundColor | Couleur | Définissez une couleur de fond personnalisée pour la bottombar lorsque l'utilisateur est en mode sombre iOS ; nécessite iOS 13 ou une version ultérieure |
| qrcodelinks | **0** ou **1** ou **2** ou **3** ou **4** | Définissez sur (0) pour ouvrir une URL scannée depuis un QR code dans l'application ; (1) dans un onglet intégré à l'application ; (2) dans un nouveau navigateur ; (3) dans un onglet intégré à l'application si externe ; (4) dans un nouveau navigateur si externe ; de plus, vous pouvez éventuellement limiter les préfixes autorisés du scanner QR dans le tableau "allowedQRurls" du fichier SwiftQRScanner.swift |
| ShowExternalLink | optionnel | Définissez sur *true* pour ouvrir les liens envoyés via l'[API Universal Links](universal-links.md) (syntaxe : https://example.org) et l'[API Deep Linking](deep-linking.md) (syntaxe : example://url?link=https://example.org). |
| splashScreenEnabled | optionnel | Définissez sur *false* si vous souhaitez désactiver l'écran de démarrage pendant le lancement de l'application et afficher plutôt l'indicateur de chargement |
| remainSplashOption | optionnel | Définissez sur *true* si vous souhaitez afficher l'écran de démarrage jusqu'à ce que le chargement initial de votre page d'accueil soit terminé (au lieu de l'indicateur de chargement) |
| splashTimeout | valeur numérique (millisecondes) | Définissez le délai d'affichage de l'écran de démarrage en *millisecondes* (l'écran de chargement s'affichera après cette durée si l'URL d'accueil est encore en cours de chargement) |
| splashMinTime | valeur numérique (millisecondes) | Durée minimale (en millisecondes) d'affichage de l'écran de démarrage ; définissez sur *0* pour désactiver la durée minimale |
| splashFadeTime | valeur numérique (millisecondes) | Durée (en millisecondes) de l'animation de fondu de l'écran de démarrage ; définissez sur *0* pour désactiver le fondu |
| scaleSplashImage | valeur en pourcentage [0-100] | Définissez la taille de l'image de l'écran de démarrage par rapport à la plus petite largeur/hauteur de l'appareil ; plage en pourcentage [0-100] ; valeur = 0 masquera complètement l'image, valeur = 100 affichera l'image en mode plein écran |
| useLoadingSign | **true** ou **false** | Définissez sur *false* pour masquer l'indicateur de chargement pendant le chargement de votre URL |
| useLoadingProgressBar | **true** ou **false** | Définissez sur *true* pour utiliser la barre de progression de chargement pendant le chargement de votre URL (à la place de l'indicateur de chargement) |
| loadingIndicatorColor | Couleur | Définissez une couleur pour l'indicateur de chargement |
| alternativeAppIconNames | Liste | Modifiez cette liste pour changer les noms de fichier de vos icônes d'application alternatives |
| backgroundlocation | **true** ou **false** | Définissez sur *true* pour autoriser l'accès à la localisation en arrière-plan (assurez-vous également que la capacité "Background Modes" dans les paramètres du projet Xcode inclut "Location updates". En outre, selon votre application web, vous devrez peut-être activer "Background Processing" ; dans ce cas, ajoutez également un tableau à votre fichier Info.plist avec la clé "Permitted background task scheduler identifiers" – dans ce tableau, incluez une chaîne contenant l'identifiant de bundle de votre application, par exemple, "com.onlineappcreator.webviewgold") |
| appendlanguage | **true** ou **false** | Définissez sur *true* si vous souhaitez enrichir la requête URL avec la langue du système, sous la forme ?webview_language=LANGUAGE CODE (par exemple ?webview_language=EN pour les utilisateurs anglophones) |
| blockfaultyandselfsignedhttpscerts | **true** ou **false** | Définissez sur *true* pour bloquer les contenus signés avec des certificats SSL auto-signés (par l'utilisateur) et les certificats SSL défectueux ; vous pouvez également envisager de [bloquer tous les contenus non HTTPS](https://www.webviewgold.com/support-center/knowledgebase/how-to-prevent-non-https-connections-in-webviewgold-for-ios-removing-nsallowsarbitraryloadsinwebcontent-from-info-plist/) |
| jailbreakBlock | **true** ou **false** | Définissez sur *true* pour bloquer l'application sur les appareils jailbreakés/piratés. Remarque : la détection n'est pas infaillible, mais utilise plusieurs méthodes pour identifier les jailbreaks et les piratages |
| autoRefreshEnabled | **true** ou **false** | Définissez sur *true* si vous souhaitez que la WebView actualise automatiquement son contenu lorsque l'application revient au premier plan depuis l'arrière-plan. |
| offlinelocalhtmlswitch | **true** ou **false** | Définissez sur *true* si vous souhaitez utiliser le dossier "local-html" lorsque l'utilisateur est hors ligne et l'URL distante lorsqu'il est en ligne. |
| extentionARY | Liste | Ajoutez les formats de fichier qui doivent déclencher la fonctionnalité de téléchargement (par exemple, .pdf, .docx, ...) |
| autodownloader | **true** ou **false** | Définissez sur *true* si vous souhaitez activer la fonctionnalité de téléchargement basée sur les en-têtes HTTP Content-Disposition, quels que soient les formats de fichier répertoriés dans la variable extentionARY ci-dessus |
| splashscreencolor | Couleur | Définissez une couleur de fond pour l'écran de démarrage |
| extentionARY | Liste | Ajoutez les formats de fichier qui doivent déclencher la fonctionnalité de téléchargement (par exemple, .pdf, .docx, ...) |
| offlinelocalhtmlswitch | **true** ou **false** | Définissez sur *true* si vous souhaitez utiliser le dossier "local-html" lorsque l'utilisateur est hors ligne et l'URL distante lorsqu'il est en ligne. |
| zipfiledownloadfromserver | **true** ou **false** | Définissez sur *true* pour télécharger une archive .zip depuis une URL distante qui sera extraite et présentée si l'utilisateur est hors ligne (activez également la variable turnofflinelocalhtmlswitch sur true) ; la mise à jour aura lieu à chaque redémarrage complet de l'application |
| zipfileremoteurl | URL | L'archive .zip depuis une URL distante qui sera extraite et présentée si l'utilisateur est hors ligne |
| zipfilename | nom de fichier | Le nom interne du fichier .zip sur l'appareil de l'utilisateur (il est recommandé de ne pas le modifier) |
| zipfileextractpath | nom de dossier | Le nom interne du dossier du chemin d'extraction sur l'appareil de l'utilisateur (il est recommandé de ne pas le modifier) |
| zipfileextractindexindex | nom de fichier | Le fichier qui doit être ouvert en premier dans l'archive .zip extraite |
| zipfilepopuptitle | texte | Le titre de la fenêtre contextuelle qui sera affichée pendant le téléchargement du fichier .zip (si vous le souhaitez, vous pouvez traduire cette chaîne dans deux langues supplémentaires en utilisant les chaînes 'alternatelanguage1' et 'alternatelanguage2' situées à la fin du fichier Config.swift) |
| zipfilepopupmessage | chaîne de texte | Le message de la fenêtre contextuelle qui sera affichée pendant le téléchargement du fichier .zip (si vous le souhaitez, vous pouvez traduire cette chaîne dans deux langues supplémentaires en utilisant les chaînes 'alternatelanguage1' et 'alternatelanguage2' situées à la fin du fichier Config.swift) |
| InAppPurchAppBundleIdentifier | optionnel | Définissez l'identifiant d'application par défaut afin d'activer l'API d'achats intégrés pour le produit IAP par défaut (les détails peuvent être configurés dans App Store Connect) |
| IAPSharedSecret | optionnel | Définissez le secret d'application (App Secret) pour activer l'API d'achats intégrés (plus d'informations [ici](in-app-purchases.md)) |
| iapsuccessurl | optionnel | Définissez l'URL par défaut qui devra s'ouvrir après un achat/abonnement intégré réussi via le wrapper WebView. L'URL pourrait être par exemple "https://www.example.org/thanks.php", et thanks.php pourrait définir le cookie à vie pour le contenu premium. |
| iapexpiredurl | optionnel | Définissez l'URL par défaut qui devra s'ouvrir après l'expiration d'un abonnement intégré via le wrapper WebView. L'URL pourrait être par exemple "https://www.example.org/expired.php", et expired.php pourrait supprimer le cookie pour le contenu premium |
| revenueCatAPIKey | optionnel | Votre clé API RevenueCat (inscrivez-vous d'abord via [tinyurl.com/register-revenuecat](https://tinyurl.com/register-revenuecat), puis suivez [tinyurl.com/api-key-revenuecat](https://tinyurl.com/api-key-revenuecat) pour la trouver) |
| revenueCatProjectID | optionnel | Votre ID de projet RevenueCat (inscrivez-vous d'abord via [tinyurl.com/register-revenuecat](https://tinyurl.com/register-revenuecat), puis suivez [tinyurl.com/project-id-revenuecat](https://tinyurl.com/project-id-revenuecat) pour le trouver) |
| oneSignalID | optionnel | Requis pour la fonctionnalité de push OneSignal |
| kPushEnabled | **true** ou **false** | Définissez sur *true* pour activer la fonctionnalité de push OneSignal |
| kPushEnhanceUrl | **true** ou **false** | Définissez sur *true* si vous souhaitez enrichir les requêtes URL principales de la WebView avec l'identifiant d'abonnement OneSignal au format ?onesignal_push_id=XYZ (comme alternative ou en complément, vous pouvez à tout moment demander l'identifiant d'abonnement OneSignal en appelant [getonesignalplayerid://](push-notifications.md#onesignalruntime), ou l'obtenir automatiquement en réglant "autoInjectVariable" sur "true" dans Config.swift) |
| kPushReloadOnUserId | **true** ou **false** | Définissez sur *true* si la WebView doit être rechargée après la réception du UserID de OneSignal |
| kPushOpenDeeplinkInBrowser | **true** ou **false** | Définissez sur *true* pour ouvrir les URL de deeplinking issues de OneSignal dans le navigateur Safari au lieu de la WebView principale ; important : pour envoyer des notifications avec un lien depuis OneSignal, N'utilisez PAS 'Launch URL' ; vous devez utiliser un 'Additional Data Field' avec la clé : url et la valeur : le lien que vous souhaitez utiliser |
| kFirebasePushEnabled | **true** ou **false** | Définissez sur *true* pour connecter votre application aux services de push Firebase |
| kFirebaseEnhanceUrl | **true** ou **false** | Définissez sur *true* si vous souhaitez enrichir les requêtes URL principales de la WebView avec ?firebase_push_id=XYZ (comme alternative ou en complément, vous pouvez à tout moment demander l'identifiant d'abonnement OneSignal en appelant [getfirebaseplayerid://](push-notifications.md#firebaseruntime), ou l'obtenir automatiquement en réglant "autoInjectVariable" sur "true" dans Config.swift) |
| firebaseTopic | **optionnel** | Définissez un topic Firebase auquel s'abonner |
| kPushwooshEnable | **optionnel** | Définissez sur *true* pour activer la fonctionnalité de push Pushwoosh (définissez l'ID dans Info.plist dans la colonne Pushwoosh_APPID) |
| kPushwooshEnhanceUrl | **optionnel** | Définissez sur *true* si vous souhaitez enrichir les requêtes URL principales de la WebView avec ?pushwoosh_id=XYZ |
| showBannerAd | **true** ou **false** | Définissez sur *true* si vous souhaitez afficher des bannières AdMob (définissez également les identifiants AdMob dans Config.swift et Info.plist, voir [ici](admob.md)) |
| showFullScreenAd | **true** ou **false** | Définissez sur *true* si vous souhaitez afficher des annonces interstitielles AdMob après X clics sur le site (définissez également les identifiants AdMob dans Config.swift et Info.plist, voir [ici](admob.md)) |
| showadAfterX | optionnel | Définissez le nombre X pour afficher une annonce interstitielle AdMob tous les X (par exemple, 10) clics sur le site ou appuis à l'écran, selon la valeur de **incrementWithTaps** (définissez également les identifiants AdMob dans Config.swift et Info.plist, voir [ici](admob.md)). |
| incrementWithTaps | **true** ou **false** | Définissez sur *true* si vous souhaitez afficher des annonces interstitielles après X appuis à l'écran, ou sur *false* après X redirections du site web. |
| enableRewardedAds | **true** ou **false** | Définissez sur *true* pour activer les annonces avec récompense AdMob. Doit être défini sur *true* même pour une activation manuelle des annonces. |
| useRewardedAdsWherePossible | **true** ou **false** | Définissez sur *true* pour afficher des annonces avec récompense AdMob à la place des annonces interstitielles AdMob, par exemple après X appuis, etc. Conservez la valeur *false* si leur activation doit être gérée via le code de votre site web. Nécessite que showFullScreenAd soit également défini sur *true* pour les remplacer. |
| admobadstriggerurls | optionnel | Ajoutez ici des mots-clés déclencheurs de page ; leur présence dans une URL déclenche des annonces interstitielles AdMob (par exemple, ["see-highscore.php", "/thank-you/", "/next-step.html"]) |
| useFacebookAds | **true** ou **false** | Définissez sur *true* pour activer les annonces interstitielles Facebook |
| facebookAdsID | optionnel | Saisissez votre Placement ID, disponible lorsque vous créez une propriété dans Facebook Monetization Manager et connectez une application iOS. L'ID ressemblera à ceci : 3937960198956424_3969441893142587 |
| useTimedAds | **true** ou **false** | Utilisez des annonces temporisées pour les annonces Facebook (par exemple, toutes les 60 s) au lieu d'annonces tous les X clics |
| fbadstriggerurls | optionnel | Ajoutez ici des mots-clés déclencheurs de page ; leur présence dans une URL déclenche une annonce Facebook (par exemple, ["see-highscore.php", "/thank-you/", "/next-step.html"]) |
| showFBAdsEveryNSeconds | optionnel | Affichez une annonce interstitielle Facebook toutes les X secondes ; 120 s ou plus sont recommandées |
| ATTDeniedShowAds | **true** ou **false** | Définissez sur *false* pour arrêter complètement d'afficher des annonces si l'utilisateur refuse l'autorisation AppTrackingTransparency (ATT) |
| useAdsenseAds | **true** ou **false** | Définissez sur *true* pour activer la prise en charge des annonces web AdSense (indépendamment des annonces AdMob) |
| askForAdConsent | **true** ou **false** | Définissez sur *false* si vous souhaitez désactiver la gestion du consentement Google pour AdMob (consultez au préalable <https://support.google.com/admob/answer/13554116>) |
| showBarcodeScanner | **true** ou **false** | Définissez sur *false* pour bloquer les requêtes du site web activant le scanner de codes-barres via `barcodescanner://` |
| kFlashLightEnabled | **true** ou **false** | Définissez sur *false* pour bloquer les requêtes du site web activant la lampe torche via `enableflashlight://` |
| widgetRefreshTime | Nombre | Intervalle de rafraîchissement du widget en minutes |
| widgetfallbackURL | Chaîne | URL d'image de secours utilisée par le widget |
| preventScreenCapture | **true** ou **false** | Définissez sur *true* pour appeler onScreenCaptureAttempt dans votre application web en cas de captures ou d'enregistrements d'écran |
| kVisionKitEnable | **true** ou **false** | Définissez sur *true* pour ajouter une option de numérisation à la boîte de dialogue de téléversement de fichiers via le [scanner de documents VisionKit](document-scanner.md) (nécessite iOS 18.4 ou version ultérieure) |
| enableSidebar | **true** ou **false** | Définissez sur *true* pour activer un bouton flottant qui ouvre une [barre latérale native](sidebar.md), personnalisable dans **Sidebar.json** |
| showcustomrateappdialog | **true** ou **false** | Définissez sur *true* pour afficher une boîte de dialogue de notation personnalisée lors du déclenchement de l'[API rateapp://](in-app-rating.md) au lieu de tenter l'appel d'avis natif |
| ratemyappurl | URL | Définissez l'URL App Store de votre application, utilisée par la boîte de dialogue de notation personnalisée |
| cookieonlaunch | **true** ou **false** | Définissez sur *true* pour ajouter un cookie au lancement de la WebView ; configurez-le via les variables **cookieonlaunchname**, **cookieonlaunchvalue** et **cookieonlaunchissecure** |
| useCustomHeaders | **true** ou **false** | Définissez sur *true* pour envoyer les en-têtes HTTP personnalisés définis dans le dictionnaire **customHeaders** avec chaque requête de la WebView |
| siriEnabled | Jeton du module | Saisissez le jeton pour activer la fonctionnalité du module Siri |
| NFCEnabled | Jeton du module | Saisissez le jeton pour activer la fonctionnalité du module NFC |
| HealthKitEnabled | Jeton du module | Saisissez le jeton pour activer la fonctionnalité du module HealthKit |
| alternatelanguage1_langcode (& liste de chaînes _alternatelanguage1_) | **true** ou **false** (& liste de chaînes) | Définissez le code de langue ou laissez cette chaîne vide pour ne pas utiliser les chaînes de la langue alternative n° 1 (liste de chaînes en bas du fichier Config.swift) ; si vous souhaitez activer cette langue alternative, veuillez utiliser le code à deux lettres conforme à la norme ISO 639-1 (par exemple, "de" pour l'allemand, "fr" pour le français, "it" pour l'italien, "pt" pour le portugais, "ca" pour le catalan, "es" pour l'espagnol, …) |
| alternatelanguage2_langcode (& liste de chaînes _alternatelanguage2_) | **true** ou **false** (& liste de chaînes) | Définissez le code de langue ou laissez cette chaîne vide pour ne pas utiliser les chaînes de la langue alternative n° 2 (liste de chaînes en bas du fichier Config.swift) ; si vous souhaitez activer cette langue alternative, veuillez utiliser le code à deux lettres conforme à la norme ISO 639-1 (par exemple, "de" pour l'allemand, "fr" pour le français, "it" pour l'italien, "pt" pour le portugais, "ca" pour le catalan, "es" pour l'espagnol, …) |

---

## Continuer la lecture

- ← Précédent : [Configurer l'application web](setup-website.md)
- Suivant → : [Nom, icône et splash](app-name-icon-splash.md)
- Même fonctionnalité sur les autres plateformes : [Android – Configurer WebViewGold](../android/setup.md) · [macOS – Configuration de WebViewGold](../macos/setup.md)
- Langues : [🇺🇸 English](../../ios/setup.md) · [🇩🇪 Deutsch](../../de/ios/setup.md) · **🇫🇷 Français** · [🇪🇸 Español](../../es/ios/setup.md) · [🇨🇳 中文](../../zh/ios/setup.md)

> [!TIP]
> **Trop occupé ? Nous configurons votre app pour vous.** Notre équipe configure, compile & soumet votre app WebViewGold — clé en main, délai rapide, Made in Germany. [Faire configurer mon app →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **Compilez dans votre navigateur :** Pas de Mac, pas d’IDE : le **WebViewGold Cloud Builder** configure, compile & met en ligne votre app. [Découvrir Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
