---
title: "App-Name, Icon und Splash Screen – WebViewGold für iOS Dokumentation"
description: "Benenne deine iOS-App um, füge ein eigenes App-Icon hinzu und richte personalisierte Splash-Screen-Grafiken für deine WebViewGold-App ein."
lang: "de"
product: "WebViewGold für iOS"
platform: "iOS"
category: "App-Design"
slug: "app-name-icon-splash"
canonical_url: "https://www.webviewgold.com/de/docs/iOS/app-name-icon-splash/"
keywords:
  - "Name, Icon & Splash"
  - "WebViewGold für iOS"
  - "Website in App umwandeln"
  - "WebView-App-Dokumentation"
  - "iOS WebView SDK"
  - "PWA zu App"
  - "HTML zu App"
  - "JavaScript-Bridge"
last_updated: "2026-10-09"
---

# App-Name, Icon und Splash Screen – WebViewGold für iOS

> **Zusammenfassung:** Benenne deine iOS-App um, füge ein eigenes App-Icon hinzu und richte personalisierte Splash-Screen-Grafiken für deine WebViewGold-App ein.

[Dokumentation](../README.md) › [WebViewGold für iOS](README.md) › Name, Icon & Splash

**Plattform:** iOS · **Kategorie:** App-Design · **Online-Version:** [www.webviewgold.com/de/docs/iOS/app-name-icon-splash/](https://www.webviewgold.com/de/docs/iOS/app-name-icon-splash/)

---

## Den angezeigten App-Namen ändern

Navigiere wie im Screenshot gezeigt über **WebViewGold** → **WebViewGold** → **Build Settings** zu **Product Name** und ändere den Namen wie im folgenden Screenshot gezeigt:

- ***HINWEIS:*** Wenn dein App-Name Akzentbuchstaben enthält (wie zum Beispiel 'à'), musst du diese für den **Product Name** durch normale Buchstaben ersetzen. Der **Product Name** wird auch zur Benennung von Dateien in deiner App verwendet und unterstützt daher keine Akzentbuchstaben (die App würde abstürzen). Um sicherzustellen, dass deine App den Benutzern auf dem iOS-Homescreen den korrekten Namen anzeigt, ändere anschließend bitte auch den **Bundle Display Name** (zu finden in der Datei **Info.plist**) von "$PRODUCT_NAME" in deinen App-Namen mit Akzentbuchstaben. Wenn dein App-Name beispielsweise "WebViewGold" lautet, sollte der **Product Name** "WebViewGolda" und der **Bundle Display Name** "WebViewGold" lauten.

![Ändere den iOS-Namen deiner Web-View-App](../../assets/ios/img/rename_xcode14.webp)

## Ein benutzerdefiniertes App-Icon hinzufügen

Führe diese einfachen Schritte aus, um deiner WebView-basierten iOS-App ein benutzerdefiniertes App-Icon hinzuzufügen:\
**1. App-Icon-Einstellungen finden**\
Navigiere zu **WebViewGold** → **WebViewGold** → **General** → **App Icons and Launch Screen** → **App Icon Source**.\
![Füge dein iOS-Icon zum Projektbereich hinzu](../../assets/ios/img/screen6.webp)\
**2. Durch dein eigenes Icon ersetzen**\
Ersetze einfach die enthaltenen Bilddateien durch deine eigenen, in der Größe angepassten Bilddateien. Es gibt kostenlose Online-Tools, die beim Erstellen dieser verschiedenen Bildgrößen helfen, wie zum Beispiel [**App Icon Generator**](https://www.appicon.co/) (wir stehen in keiner Verbindung mit dem Entwicklerunternehmen). Alternativ kannst du nach einem beliebigen "iOS App Icon Generator"-Tool deiner Wahl suchen.

## Einen benutzerdefinierten Splash Screen hinzufügen

Führe diese Schritte aus, um deiner WebView-basierten iOS-App benutzerdefinierte Splash-Screen-Grafiken hinzuzufügen:

### 1. Den Splash Screen aktivieren

So aktivierst du den Splash Screen für deine App:

- Öffne die Datei **Config.swift** und suche nach `splashScreenEnabled`.
- Stelle sicher, dass diese Variable auf `true` gesetzt ist.

### 2. Das Splash-Screen-Bild ersetzen

So verwendest du dein eigenes Branding als Splash Screen:

- Ersetze die vorhandene Datei **splash.gif** im Hauptverzeichnis des XCode-Projekts durch deine eigene GIF-Datei.
- **Wichtig:** Stelle sicher, dass deine Bilddatei quadratisch ist (Breite = Höhe), um eine optimale Darstellung zu erzielen. Zum Beispiel:
  - 128x128 px
  - 512x512 px
  - 1024x1024 px

### 3. Die Anzeigedauer anpassen

So steuerst du, wie lange der Splash Screen angezeigt wird:

- Öffne die Datei **Config.swift** und suche nach `splashTimeout`.
- Ändere die Timeout-Einstellung auf die von dir gewünschte Dauer (in Millisekunden).

**Beispiel:** Setze den Wert auf `2000` für eine 2-sekündige Anzeige.

Setze die Option `remainSplashOption` (zu finden in der Datei **Config.swift**) auf `true`, wenn du den Splash Screen anzeigen möchtest, bis deine Seite erfolgreich geladen wurde. Andernfalls wird er nur für kurze Zeit angezeigt und der native iOS-Ladeindikator beginnt.\
Verwende die Option `splashscreencolor` (zu finden in der Datei **Config.swift**), um die Hintergrundfarbe des Splash Screens zu ändern. Farboptionen findest du [hier](https://developer.apple.com/documentation/uikit/uicolor/standard_colors).

### 4. Optionaler App-Hinweis für deine Datenschutzerklärung / Nutzungsbedingungen

Wenn du deinen Benutzern (WebViewGold-basierte) mobile Apps anbietest, kannst du optional die folgende Erklärung in deine Datenschutzerklärung oder deine Nutzungsbedingungen aufnehmen (dieser Hinweis dient ausschließlich zu Informationszwecken und stellt keine Rechtsberatung dar. Wir übernehmen keine Haftung dafür, wie dieser Text verwendet wird. Bitte konsultiere für eine individuelle Beratung einen Rechtsexperten):

> ```
> Our mobile apps (iOS/Android) are developed using WebViewGold by jocapps GmbH (Germany). These apps display the content of our website using a WebView framework and enrich it with selected native features to improve usability and performance. Accordingly, the same privacy policy and terms of service that apply to our website also apply to our mobile apps. For more information, please visit
> https://www.webviewgold.com/#convert-website-to-app-privacy, or contact us directly.
> ```

---

## Weiterlesen

- ← Vorherige: [WebViewGold konfigurieren](setup.md)
- Weiter →: [Safe Area anpassen](safe-area.md)
- Dieselbe Funktion auf anderen Plattformen: [Android – App-Icon](../android/app-icon.md) · [macOS – App-Symbol](../macos/app-icon.md)
- Sprachen: [🇺🇸 English](../../ios/app-name-icon-splash.md) · **🇩🇪 Deutsch** · [🇫🇷 Français](../../fr/ios/app-name-icon-splash.md) · [🇪🇸 Español](../../es/ios/app-name-icon-splash.md) · [🇨🇳 中文](../../zh/ios/app-name-icon-splash.md)

> [!TIP]
> **Zu wenig Zeit? Wir richten deine App für dich ein.** Unser Team konfiguriert, erstellt & reicht deine WebViewGold-App ein – schlüsselfertig, mit schneller Bearbeitung, Made in Germany. [App einrichten lassen →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **Im Browser erstellen:** Kein Mac, keine IDE: Der **WebViewGold Cloud Builder** konfiguriert, erstellt & lädt deine App online hoch. [Cloud Builder entdecken →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
