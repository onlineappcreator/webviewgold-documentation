---
title: "WebViewGold für iOS – Dokumentation – Website in iOS-App umwandeln"
description: "Offizielle WebViewGold-für-iOS-Dokumentation: Wandle deine Website in wenigen Minuten in eine native iOS-App um – Einrichtungsanleitung, 40+ APIs & Funktionen und Veröffentlichung im App Store."
lang: "de"
product: "WebViewGold für iOS"
platform: "iOS"
canonical_url: "https://www.webviewgold.com/de/docs/iOS/"
keywords:
  - "WebViewGold für iOS"
  - "Website in App umwandeln"
  - "WebView-App-Dokumentation"
  - "iOS WebView SDK"
  - "PWA zu App"
  - "HTML zu App"
  - "JavaScript-Bridge"
last_updated: "2026-10-09"
---

# WebViewGold für iOS – Dokumentation

![WebViewGold für iOS](../../assets/ios/img/header.webp)

> Offizielle WebViewGold-für-iOS-Dokumentation: Wandle deine Website in wenigen Minuten in eine native iOS-App um – Einrichtungsanleitung, 40+ APIs & Funktionen und Veröffentlichung im App Store.

[Dokumentation](../README.md) › WebViewGold für iOS

Verwandle deine Website, PWA, dein SaaS-Dashboard, deinen Onlineshop oder deine KI-generierte Web-App in wenigen Minuten in eine native iOS-App. Nutze WebViewGold wie ein leichtgewichtiges App-SDK: konfiguriere deine URL, aktiviere native APIs, integriere JavaScript-Bridge-Befehle und veröffentliche eine store-fertige App, ohne dein Web-Produkt neu aufzubauen.

WebViewGold funktioniert mit klassischen HTML/PHP-Seiten, WordPress, jQuery-Mobile-Projekten und modernen Web-Apps, die mit Lovable, Base44, Bolt, Bubble, React, Vue, Angular oder ähnlichen Buildern erstellt wurden. Die folgende Dokumentation erläutert den Einrichtungsablauf, native Feature-APIs, Sicherheitsaspekte und Veröffentlichungsschritte in einem technischen, implementierungsorientierten Format.

**[Anleitung starten →](setup-website.md)** · [WebViewGold herunterladen](https://www.webviewgold.com/download/ios) · [Cloud Builder](https://www.webviewgold.com/cloud-builder?ref=ios_docs)

## Schnellstart

In drei Schritten von der Website zur veröffentlichten App:

1. **[Web-App einrichten](setup-website.md)** — Verwende eine Remote-URL, bündele lokale HTML-Dateien oder kombiniere beides mit einem Offline-Fallback.
2. **[WebViewGold konfigurieren](setup.md)** — Füge deine URL ein und passe jede Option in einer einfachen Konfigurationsdatei an – ohne Programmieren.
3. **[Erstellen & veröffentlichen](publish.md)** — Bring deine App in den Store – selbst, über den Cloud Builder oder mit unserem Veröffentlichungsservice.

## Neuigkeiten

WebViewGold wird regelmäßig aktualisiert. Den vollständigen Änderungsverlauf findest du [hier](https://www.webviewgold.com/changelog/ios/).

## Alle Themen, APIs & Funktionen

Alles, was WebViewGold für iOS kann – jedes Thema auf einer eigenen Seite:

### Erste Schritte

- **[Web-App einrichten](setup-website.md)** — Bereite deine Website, PWA oder lokale HTML-Dateien für deine iOS-App vor: Verwende eine Remote-URL, bündle Dateien offline in der App oder kombiniere beides mit einem Offline-Fallback.
- **[WebViewGold konfigurieren](setup.md)** — Lade das WebViewGold-Xcode-Template herunter, trage deine URL in Config.swift ein und entdecke alle integrierten Konfigurationsoptionen – ganz ohne Programmierkenntnisse.

### App-Design

- **[Name, Icon & Splash](app-name-icon-splash.md)** — Benenne deine iOS-App um, füge ein eigenes App-Icon hinzu und richte personalisierte Splash-Screen-Grafiken für deine WebViewGold-App ein.
- **[Safe Area anpassen](safe-area.md)** — Passe die Safe Area an und aktiviere die individuelle untere Leiste, damit deine Web-App auf iPhones mit Home-Leiste perfekt aussieht.

### APIs & Funktionen

- **[Geolocation-API](geolocation.md)** — Aktiviere die HTML5-Geolokalisierung in deiner iOS-WebView-App und fordere präzise Standortberechtigungen auf die richtige Weise an.
- **[Push-Benachrichtigungen-API](push-notifications.md)** — Sende Push-Benachrichtigungen an die Nutzer deiner iOS-App mit OneSignal, Firebase oder Pushwoosh – Einrichtung, Deep Links und nutzerspezifisches Targeting erklärt.
- **[AdMob-Ads-API](admob.md)** — Monetarisiere deine iOS-App mit Google-AdMob-Banner-, Interstitial- und Rewarded-Anzeigen – Konfiguration und JavaScript-Trigger.
- **[Facebook-Ads-API](facebook-ads.md)** — Zeige Facebook-Audience-Network-Banner- und -Interstitial-Anzeigen in deiner WebViewGold-iOS-App an.
- **[HTML-Audio-API](html-audio.md)** — Lass HTML-Audio im Hintergrund deiner iOS-WebView-App weiterlaufen – selbst bei gesperrtem Bildschirm.
- **[Native-Video-API](native-video.md)** — Spiele Videostreams im nativen iOS-Videoplayer mit Bild-in-Bild-Unterstützung ab — direkt aus deiner Web-App ausgelöst.
- **[Datei-Downloader-API](file-downloader.md)** — Lass Nutzer Bilder, PDFs und andere Dateien aus deiner Web-App direkt auf ihr iPhone oder iPad herunterladen.
- **[Drucker-API](printer.md)** — Drucke Bilder und PDFs aus deiner Web-App per AirPrint: Sende Dateien mit einem einzigen Link an den nativen iOS-Druckdialog.
- **[iCal-Kalender-API](ical-calendar.md)** — Füge Kalenderereignisse aus deiner Web-App über die iCal-Kalender-API zum nativen iOS-Kalender hinzu.
- **[Apple-Wallet-Pass-API](wallet-pass.md)** — Lass Nutzer .pkpass-Pässe (Tickets, Coupons, Mitgliedskarten) aus deiner Web-App zu Apple Wallet hinzufügen.
- **[UUID-API](uuid.md)** — Identifiziere App-Installationen mit einer eindeutigen UUID, die an deine WebView-URL angehängt oder per JavaScript abgerufen wird.
- **[Taschenlampen-API](flashlight.md)** — Steuere die Taschenlampe des Geräts aus deiner Web-App mit einfachen JavaScript-Links in WebViewGold für iOS.
- **[App-Zurücksetzen-API](reset-app.md)** — Setze Cache, Cookies und lokalen Speicher deiner iOS-WebView-App mit einem einzigen Link oder JavaScript-Aufruf zurück.
- **[Nutzer-Tracking-Entscheidung-API](user-tracking.md)** — Berücksichtige App Tracking Transparency: Lies die Tracking-Entscheidung des Nutzers aus und reagiere darauf in deiner WebViewGold-iOS-App.
- **[Ladeanzeige-API](loading-sign.md)** — Blende die native Ladeanzeige bei Bedarf ein oder aus und passe das Ladeerlebnis deiner iOS-App an.
- **[Pull-to-Refresh-API](pull-to-refresh.md)** — Aktiviere die native Pull-to-Refresh-Geste in deiner iOS-WebView-App, passe ihre Farben an und schalte sie dynamisch aus deiner Web-App um.
- **[URL-Handling-API](url-handling.md)** — Lege fest, welche Links in deiner App, in einem In-App-Browser-Tab oder in Safari geöffnet werden – volle URL-Handling-Kontrolle für iOS.
- **[Social Login Helper](social-login.md)** — Bringe Google-, Facebook- und Apple-OAuth-Logins mit den integrierten Social-Login-Helfern zuverlässig in deiner iOS-WebView-App zum Laufen.
- **[Reconnect-API](reconnect.md)** — Füge deiner Offline-Fallback-Seite einen „Erneut versuchen“-Button hinzu, der die letzte Online-URL deiner iOS-App neu lädt.
- **[Eigenes CSS & JS API](custom-css-js.md)** — Füge eigene CSS-Styles und JavaScript-Code in jede Seite deiner iOS-WebView-App ein – perfekt für App-spezifische Anpassungen.
- **[Universal Links-API](universal-links.md)** — Öffne Links zu deiner Domain direkt in deiner iOS-App mit Apple Universal Links – Einrichtung, AASA-Datei und Fehlerbehebung.
- **[Deep-Linking-API](deep-linking.md)** — Starte deine iOS-App über benutzerdefinierte URL-Schemata und leite Nutzer per Deep Link zu bestimmten Seiten deiner Web-App.
- **[App-Teilen-Dialog-API](app-sharing-dialog.md)** — Löse das native iOS-Teilen-Menü aus deiner Web-App aus, damit Nutzer deine App oder eine beliebige URL teilen können.
- **[In-App-Rating-Dialog-API](in-app-rating.md)** — Bitte Nutzer im perfekten Moment um eine App-Store-Bewertung — löse den nativen iOS-Bewertungsdialog aus deiner Web-App aus.
- **[In-App-Käufe-API](in-app-purchases.md)** — Verkaufe digitale Güter und Abonnements in deiner iOS-WebView-App mit StoreKit-basierten In-App-Käufen.
- **[IAP-History-API](iap-history.md)** — Lies die bisherigen In-App-Käufe des Nutzers als JSON aus deiner Web-App — perfekt für „Meine Käufe“-Seiten.
- **[QR-Code-Scanner-API](qr-code-scanner.md)** — Öffne einen nativen QR-Code-Scanner aus deiner Web-App und verarbeite die Scan-Ergebnisse per URL oder JavaScript.
- **[Barcode-Scanner-API](barcode-scanner.md)** — Scanne EAN-, UPC- und andere Barcodes nativ in deiner iOS-WebView-App und übergib die Ergebnisse an deine Web-App.
- **[Scan-Modus-API](scanning-mode.md)** — Optimiere das Kamera-Scan-Verhalten des QR- und Barcode-Scanners in WebViewGold für iOS.
- **[Dokumentenscanner](document-scanner.md)** — Lass Nutzer Papierdokumente mit der Kamera scannen und über den Datei-Upload deiner Web-App hochladen — auf Basis von Apple VisionKit.
- **[Screenshot-erstellen-API](take-screenshot.md)** — Erstelle programmgesteuert einen Screenshot des aktuellen App-Bildschirms und teile oder speichere ihn – per JavaScript.
- **[App-Versionsprüfung-API](app-version-check.md)** — Erkenne die installierte App-Version aus deiner Web-App und fordere Nutzer bei Bedarf zum Aktualisieren auf.
- **[Dynamische-UI-API](dynamic-ui.md)** — Ändere native UI-Elemente wie die Farben der Statusleiste oder der unteren Leiste dynamisch aus deiner Web-App.
- **[Dynamisches-App-Icon-API](dynamic-app-icon.md)** — Wechsle zur Laufzeit zwischen alternativen App-Icons in deiner iOS-WebView-App – ausgelöst aus deiner Web-App.
- **[Kontakte-API](contacts.md)** — Greife aus deiner Web-App auf das Adressbuch des Geräts zu: Lies Kontakte mit Nutzerberechtigung in WebViewGold für iOS.
- **[Biometrische-Auth-API](biometric-authentication.md)** — Schütze deine iOS-App mit Face ID oder Touch ID und verifiziere Nutzer biometrisch aus deiner Web-App.
- **[Haptisches-Feedback-API](haptic-feedback.md)** — Löse natives haptisches Feedback (Vibrationen) aus deiner Web-App aus, für ein echtes natives App-Gefühl auf iOS.
- **[Shortcut-API](shortcut.md)** — Füge deiner iOS-App Schnellaktion-Shortcuts für den Home-Bildschirm hinzu, die per Deep Link zu bestimmten Seiten führen.
- **[Zwischenablage-API](clipboard.md)** — Kopiere Text in die iOS-Zwischenablage und lies den Inhalt der Zwischenablage aus deiner Web-App per JavaScript.
- **[Read/Write-Value-API](read-write-value.md)** — Speichere einen String-Wert dauerhaft auf dem Gerät und lies ihn zurück in das JavaScript deiner Web-App.
- **[Open-App-Settings-API](open-app-settings.md)** — Führe Nutzer direkt zur Seite deiner App in der iOS-Einstellungen-App, um Berechtigungen und Mitteilungen zu verwalten.

### Erweiterungen & Plugins

- **[Share Extension](share-extension.md)** — Lass Nutzer Inhalte aus anderen Apps mit einer Share Extension direkt in deine iOS-WebView-App teilen.
- **[Widget Extension](widget-extension.md)** — Füge deiner iOS-WebView-App ein Home-Bildschirm-Widget hinzu, das Nutzer direkt in deine Web-App führt.
- **[App Clip Extension](app-clip.md)** — Biete eine schlanke App-Clip-Version deiner iOS-App an, die sich ohne Installation sofort öffnet.
- **[Native Navigationsleiste](navigation-footer.md)** — Aktiviere eine native untere Navigationsleiste mit Zurück-, Vorwärts- und individuellen Schaltflächen in deiner iOS-App.
- **[Native Sidebar](sidebar.md)** — Aktiviere ein natives ausklappbares Sidebar-Menü mit eigenen Links und SF-Symbols-Icons — konfiguriert über Sidebar.json.
- **[Bildschirmaufnahme-Erkennung](screen-capture.md)** — Erkenne Screenshots und Bildschirmaufnahmen in deiner iOS-App und reagiere aus deiner Web-App darauf.
- **[MultiAPICall-Funktion](multi-api-call.md)** — Verkette mehrere WebViewGold-API-Aufrufe in einer einzigen Anfrage mit der MultiAPICall-Funktion für iOS.
- **[NFC-Plugin](nfc.md)** — Lies NFC-Tags nativ in deiner iOS-WebView-App und übergib die Tag-Daten an deine Web-App.
- **[Siri-Plugin](siri.md)** — Füge deiner iOS-WebView-App Unterstützung für Siri Shortcuts hinzu und öffne App-Inhalte per Sprache.
- **[HealthKit-Plugin](healthkit.md)** — Verbinde deine Web-App mit Apple HealthKit und lies Gesundheitsdaten mit Nutzerberechtigung auf iOS.

### Erstellen & Veröffentlichen

- **[Erstellen & Veröffentlichen](publish.md)** — Veröffentliche deine WebView-App im Apple App Store: kompletter Veröffentlichungsservice, manueller Prozess und Ändern des Bundle Identifiers.

### Mehr

- **[Credits & Lizenzen](credits.md)** — Lizenzbedingungen für WebViewGold für iOS, wann du eine Envato Extended License benötigst, und Open-Source-Credits.
- **[WebViewGold bewerten](rate.md)** — Gefällt dir WebViewGold? Bewerte es in Sekunden auf CodeCanyon – so bleiben die Updates am Laufen.
- **[Android- & macOS-Versionen](more-platforms.md)** — Bringe deine App auf weitere Plattformen: Hole dir WebViewGold für Android und macOS und nutze dieselbe Web-App erneut.
- **[Support & Kontakt](support.md)** — Erhalte schnell Hilfe: Durchsuche das WebViewGold Support Center, kontaktiere unser Team direkt oder fordere professionelle individuelle App-Entwicklung made in Germany an.

## Eine Web-App, alle Plattformen

Verwende dieselbe Website für iOS-, Android- & macOS-Apps mit WebViewGold.

- [WebViewGold für Android](../android/README.md)
- [WebViewGold für macOS](../macos/README.md)

**Sprachen:** [🇺🇸 English](../../ios/README.md) · **🇩🇪 Deutsch** · [🇫🇷 Français](../../fr/ios/README.md) · [🇪🇸 Español](../../es/ios/README.md) · [🇨🇳 中文](../../zh/ios/README.md)

> [!TIP]
> **Zu wenig Zeit? Wir richten deine App für dich ein.** Unser Team konfiguriert, erstellt & reicht deine WebViewGold-App ein – schlüsselfertig, mit schneller Bearbeitung, Made in Germany. [App einrichten lassen →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **Im Browser erstellen:** Kein Mac, keine IDE: Der **WebViewGold Cloud Builder** konfiguriert, erstellt & lädt deine App online hoch. [Cloud Builder entdecken →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
