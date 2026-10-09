---
title: "API d'icône d'app dynamique – Documentation WebViewGold pour iOS"
description: "Basculez entre différentes icônes d'app à l'exécution dans votre application WebView iOS, déclenché depuis votre application web."
lang: "fr"
product: "WebViewGold pour iOS"
platform: "iOS"
category: "API et fonctionnalités"
slug: "dynamic-app-icon"
canonical_url: "https://www.webviewgold.com/fr/docs/iOS/dynamic-app-icon/"
keywords:
  - "API d'icône d'app dynamique"
  - "WebViewGold pour iOS"
  - "convertir un site web en app"
  - "documentation d’app WebView"
  - "SDK WebView iOS"
  - "PWA en app"
  - "HTML en app"
  - "pont JavaScript"
last_updated: "2026-10-09"
---

# API d'icône d'app dynamique – WebViewGold pour iOS

> **Résumé :** Basculez entre différentes icônes d'app à l'exécution dans votre application WebView iOS, déclenché depuis votre application web.

[Documentation](../README.md) › [WebViewGold pour iOS](README.md) › API d'icône d'app dynamique

**Plateforme :** iOS · **Catégorie :** API et fonctionnalités · **Version en ligne :** [www.webviewgold.com/fr/docs/iOS/dynamic-app-icon/](https://www.webviewgold.com/fr/docs/iOS/dynamic-app-icon/)

---

Cette API **permet aux utilisateurs de votre application de changer l'icône de l'application d'un simple clic**. WebViewGold autorise **jusqu'à trois icônes alternatives** en plus de l'icône par défaut. Chaque fois que l'icône de l'application est modifiée dynamiquement, l'utilisateur sera notifié une fois l'opération réussie :\
![Notification à l'utilisateur du changement dynamique d'icône de l'application.](../../assets/ios/img/icon-change-notice.jpeg)\
Si vous souhaitez changer l'icône de votre application au nom de vos utilisateurs, vous pouvez le faire en publiant une nouvelle version de votre application avec la nouvelle icône installée. Découvrez comment changer l'icône de votre application sur WebViewGold [ici](app-name-icon-splash.md).\
Pour changer dynamiquement l'icône de l'application, il suffit de créer un lien vers l'un des formats d'URL suivants :

```html
<script>
// Passer à l'icône alternative 1
window.location.href = "changeicon://icon1"

// Passer à l'icône alternative 2
window.location.href = "changeicon://icon2"

// Passer à l'icône alternative 3
window.location.href = "changeicon://icon3"

// Revenir à l'icône par défaut
window.location.href = "changeicon://default"

</script>
```

Consultez une page de démonstration et de test de cette API [ici](https://webviewgoldtest.github.io/alticonsios.html).\
Pour définir vos icônes alternatives, ouvrez les fichiers de votre application dans le Finder et accédez à **WebView-Swift/WebView/ApplicationIcon/AppIconAlternate**.\
Dans ce dossier, vous verrez des icônes modèles pour toutes les tailles d'icônes requises sous iOS (iPhones et iPads), pour chaque icône alternative :\
![Le dossier « AppIconAlternate » contient les icônes alternatives que vous pouvez modifier.](../../assets/ios/img/alternative-app-icon-files.webp)\
Les noms par défaut de chaque icône alternative sont : « AppIconAlternate1 », « AppIconAlternate2 » et « AppIconAlternate3 ».\
Si vous le souhaitez, vous pouvez modifier les noms par défaut en éditant la variable **alternativeAppIconNames** dans le fichier **Config** :\
![Utilisez cette variable dans Config pour modifier les noms de fichiers des icônes alternatives.](../../assets/ios/img/alternative-app-icon-names.webp)\
Chaque icône (par exemple, « AppIconAlternateX ») nécessite cinq tailles différentes, décrites par le suffixe du nom de fichier :

- Pour les iPhones :

- AppIconAlternateX *(60x60 pixels)*
- AppIconAlternateX**@2x** *(120x120 pixels)*
- AppIconAlternateX**@3x** *(180x180 pixels)*

- Pour les iPads :

- AppIconAlternateX**-ipad@2x** *(152x152 pixels)*
- AppIconAlternateX**-ipad@3x** *(167x167 pixels)*

Lorsque vous remplacez ces icônes modèles par les vôtres, assurez-vous qu'elles respectent le même format de nom de fichier (avec les suffixes indiqués ci-dessus) et la taille d'image correcte.\
Consultez un guide plus détaillé sur les spécifications des icônes d'application [ici](https://developer.apple.com/design/human-interface-guidelines/foundations/app-icons/).

Pour activer cette API (également pour la validation par l'App Store), veuillez ouvrir Info.plist en tant que code source (clic droit sur le fichier et sélectionnez « Open As » -> « Source Code » dans le menu contextuel) :
Dans Info.plist, recherchez

```xml
<key>CFBundleIcons</key>
	<dict>
		<key>CFBundlePrimaryIcon</key>
		<dict>
			<key>CFBundleIconFiles</key>
			<array>
				<string></string>
			</array>
			<key>UIPrerenderedIcon</key>
			<false/>
		</dict>
	</dict>
```

et remplacez-le par

```xml
<key>CFBundleIcons</key>
<dict>
	<key>CFBundleAlternateIcons</key>
	<dict>
		<key>AppIconAlternate1</key>
		<dict>
			<key>CFBundleIconFiles</key>
			<array>
				<string>AppIconAlternate1</string>
			</array>
			<key>UIPrerenderedIcon</key>
			<false/>
		</dict>
		<key>AppIconAlternate2</key>
		<dict>
			<key>CFBundleIconFiles</key>
			<array>
				<string>AppIconAlternate2</string>
			</array>
			<key>UIPrerenderedIcon</key>
			<false/>
		</dict>
		<key>AppIconAlternate3</key>
		<dict>
			<key>CFBundleIconFiles</key>
			<array>
				<string>AppIconAlternate3</string>
			</array>
			<key>UIPrerenderedIcon</key>
			<false/>
		</dict>
	</dict>
	<key>CFBundlePrimaryIcon</key>
	<dict>
		<key>CFBundleIconFiles</key>
		<array>
			<string></string>
		</array>
		<key>UIPrerenderedIcon</key>
		<false/>
	</dict>
</dict>
```

De plus, recherchez

```xml
<key>CFBundleIcons~ipad</key>
<dict>
    <key>CFBundlePrimaryIcon</key>
    <dict>
        <key>CFBundleIconFiles</key>
        <array>
            <string></string>
        </array>
        <key>UIPrerenderedIcon</key>
        <false/>
    </dict>
</dict>
```

et remplacez-le par

```xml
<key>CFBundleIcons~ipad</key>
<dict>
	<key>CFBundleAlternateIcons</key>
	<dict>
		<key>AppIconAlternate1</key>
		<dict>
			<key>CFBundleIconFiles</key>
			<array>
				<string>AppIconAlternate1-ipad</string>
			</array>
			<key>UIPrerenderedIcon</key>
			<false/>
		</dict>
		<key>AppIconAlternate2</key>
		<dict>
			<key>CFBundleIconFiles</key>
			<array>
				<string>AppIconAlternate2-ipad</string>
			</array>
			<key>UIPrerenderedIcon</key>
			<false/>
		</dict>
		<key>AppIconAlternate3</key>
		<dict>
			<key>CFBundleIconFiles</key>
			<array>
				<string>AppIconAlternate3-ipad</string>
			</array>
			<key>UIPrerenderedIcon</key>
			<false/>
		</dict>
	</dict>
	<key>CFBundlePrimaryIcon</key>
	<dict>
		<key>CFBundleIconFiles</key>
		<array>
			<string></string>
		</array>
		<key>UIPrerenderedIcon</key>
		<false/>
	</dict>
</dict>
```

Il s'agit du paramétrage par défaut concernant les noms des icônes alternatives et le nombre de fichiers d'icônes alternatives.

---

## Continuer la lecture

- ← Précédent : [API d'UI dynamique](dynamic-ui.md)
- Suivant → : [API Contacts](contacts.md)
- Langues : [🇺🇸 English](../../ios/dynamic-app-icon.md) · [🇩🇪 Deutsch](../../de/ios/dynamic-app-icon.md) · **🇫🇷 Français** · [🇪🇸 Español](../../es/ios/dynamic-app-icon.md) · [🇨🇳 中文](../../zh/ios/dynamic-app-icon.md)

> [!TIP]
> **Trop occupé ? Nous configurons votre app pour vous.** Notre équipe configure, compile & soumet votre app WebViewGold — clé en main, délai rapide, Made in Germany. [Faire configurer mon app →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **Compilez dans votre navigateur :** Pas de Mac, pas d’IDE : le **WebViewGold Cloud Builder** configure, compile & met en ligne votre app. [Découvrir Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
