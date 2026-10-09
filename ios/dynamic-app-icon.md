---
title: "Dynamic App Icon API – WebViewGold for iOS Documentation"
description: "Switch between alternative app icons at runtime in your iOS WebView app — triggered from your web app."
lang: "en"
product: "WebViewGold for iOS"
platform: "iOS"
category: "APIs & Features"
slug: "dynamic-app-icon"
canonical_url: "https://www.webviewgold.com/docs/iOS/dynamic-app-icon/"
keywords:
  - "Dynamic App Icon API"
  - "WebViewGold for iOS"
  - "convert website to app"
  - "WebView app documentation"
  - "iOS WebView SDK"
  - "PWA to app"
  - "HTML to app"
  - "JavaScript bridge"
last_updated: "2026-10-09"
---

# Dynamic App Icon API – WebViewGold for iOS

> **Summary:** Switch between alternative app icons at runtime in your iOS WebView app — triggered from your web app.

[Documentation](../README.md) › [WebViewGold for iOS](README.md) › Dynamic App Icon API

**Platform:** iOS · **Category:** APIs & Features · **Online version:** [www.webviewgold.com/docs/iOS/dynamic-app-icon/](https://www.webviewgold.com/docs/iOS/dynamic-app-icon/)

---

This API **allows the users of your app to change the app icon with the click of button**. WebViewGold allows **up to three alternative app icons** from your default app icon. Whenever the app icon is dynamically changed, the user will be notified upon successful completion:\
![Dynamic app icon change user notification.](../assets/ios/img/icon-change-notice.jpeg)\
If you wish to change the app icon of your app on behalf of your users, you can do so by publishing a new version of your app with the new app icon installed. See how to change your app icon on WebViewGold [here](app-name-icon-splash.md).\
To dynamically change the app icon, just link to one of the following URL formats:

```html
<script>
// Change to Alternative App Icon 1
window.location.href = "changeicon://icon1"

// Change to Alternative App Icon 2
window.location.href = "changeicon://icon2"

// Change to Alternative App Icon 3
window.location.href = "changeicon://icon3"

// Revert to the Default App Icon
window.location.href = "changeicon://default"

</script>
```

View a demonstration and testing page for this API [here](https://webviewgoldtest.github.io/alticonsios.html).\
To set your alternative app icons, open your app files in Finder and navigate to **WebView-Swift/WebView/ApplicationIcon/AppIconAlternate**.\
In this folder, you will see template app icons for all of the required app icon sizes in iOS (iPhones and iPads), for each alternative icon:\
![The 'AppIconAlternate' folder contains the alternative app icons for you to edit.](../assets/ios/img/alternative-app-icon-files.webp)\
The default names of each alternative app icon are: "AppIconAlternate1", "AppIconAlternate2" and "AppIconAlternate3".\
If you like, you can change the default names by editing the **alternativeAppIconNames** variable in the **Config** file:\
![Use this variable in Config to edit the alternative app icon file names.](../assets/ios/img/alternative-app-icon-names.webp)\
Each app icon (for example, 'AppIconAlternateX') requires five different sizes, which are described by the file name suffix:

- For iPhones:

- AppIconAlternateX *(60x60 pixels)*
- AppIconAlternateX**@2x** *(120x120 pixels)*
- AppIconAlternateX**@3x** *(180x180 pixels)*

- For iPads:

- AppIconAlternateX**-ipad@2x** *(152x152 pixels)*
- AppIconAlternateX**-ipad@3x** *(167x167 pixels)*

When replacing these template app icons with your own, make sure they follow the same file name format (with the suffixes listed above) with the correct image size.\
View a more detailed guide on app icon specifications [here](https://developer.apple.com/design/human-interface-guidelines/foundations/app-icons/).

To activate this API (also for App Store Review), please open Info.plist as source code (right-click on the file and select "Open As" -> "Source Code" from the contextual menu):
Within Info.plist, search for

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

and replace it with

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

Moreover, search for

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

and replace it with

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

This is the default setting regarding alternative app icon names and amount of alternative app icon files.

---

## Continue reading

- ← Previous: [Dynamic UI API](dynamic-ui.md)
- Next →: [Contacts API](contacts.md)
- Languages: **🇺🇸 English** · [🇩🇪 Deutsch](../de/ios/dynamic-app-icon.md) · [🇫🇷 Français](../fr/ios/dynamic-app-icon.md) · [🇪🇸 Español](../es/ios/dynamic-app-icon.md) · [🇨🇳 中文](../zh/ios/dynamic-app-icon.md)

> [!TIP]
> **Too busy? We set up your app for you.** Our team configures, builds & submits your WebViewGold app — done-for-you, fast turnaround, Made in Germany. [Get your app set up →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **Build in your browser:** No Mac, no IDE: the **WebViewGold Cloud Builder** configures, builds & uploads your app online. [Discover Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
