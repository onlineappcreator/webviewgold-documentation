---
title: "Dokumentation zu WebViewGold für Android – Website in Android-App umwandeln"
description: "Offizielle WebViewGold-für-Android-Dokumentation: Verwandle deine Website in Minuten in eine native Android-App — Einrichtungsanleitung, 30+ APIs & Funktionen und Veröffentlichung bei Google Play."
lang: "de"
product: "WebViewGold für Android"
platform: "Android"
canonical_url: "https://www.webviewgold.com/de/docs/android/"
keywords:
  - "WebViewGold für Android"
  - "Website in App umwandeln"
  - "WebView-App-Dokumentation"
  - "Android WebView SDK"
  - "PWA zu App"
  - "HTML zu App"
  - "JavaScript-Bridge"
last_updated: "2026-10-09"
---

# WebViewGold für Android – Dokumentation

![WebViewGold für Android](../../assets/android/img/header.webp)

> Offizielle WebViewGold-für-Android-Dokumentation: Verwandle deine Website in Minuten in eine native Android-App — Einrichtungsanleitung, 30+ APIs & Funktionen und Veröffentlichung bei Google Play.

[Dokumentation](../README.md) › WebViewGold für Android

Verwandle deine Website, PWA, dein SaaS-Dashboard, deinen Onlineshop oder deine KI-generierte Web-App in wenigen Minuten in eine native Android-App. Nutze WebViewGold wie ein leichtgewichtiges App-SDK: konfiguriere deine URL, aktiviere native APIs, integriere JavaScript-Bridge-Befehle und veröffentliche eine store-fertige App, ohne dein Web-Produkt neu aufzubauen.

WebViewGold funktioniert mit klassischen HTML/PHP-Seiten, WordPress, jQuery-Mobile-Projekten und modernen Web-Apps, die mit Lovable, Base44, Bolt, Bubble, React, Vue, Angular oder ähnlichen Buildern erstellt wurden. Die folgende Dokumentation erläutert den Einrichtungsablauf, native Feature-APIs, Sicherheitsaspekte und Veröffentlichungsschritte in einem technischen, implementierungsorientierten Format.

**[Anleitung starten →](setup-website.md)** · [WebViewGold herunterladen](https://www.webviewgold.com/download/android) · [Cloud Builder](https://www.webviewgold.com/cloud-builder?ref=android_docs)

## Schnellstart

In drei Schritten von der Website zur veröffentlichten App:

1. **[Web-App einrichten](setup-website.md)** — Verwende eine Remote-URL, bündele lokale HTML-Dateien oder kombiniere beides mit einem Offline-Fallback.
2. **[WebViewGold konfigurieren](setup.md)** — Füge deine URL ein und passe jede Option in einer einfachen Konfigurationsdatei an – ohne Programmieren.
3. **[Erstellen & veröffentlichen](publish.md)** — Bring deine App in den Store – selbst, über den Cloud Builder oder mit unserem Veröffentlichungsservice.

## Neuigkeiten

WebViewGold wird regelmäßig aktualisiert. Den vollständigen Änderungsverlauf findest du [hier](https://www.webviewgold.com/changelog/android/).

## Alle Themen, APIs & Funktionen

Alles, was WebViewGold für Android kann – jedes Thema auf einer eigenen Seite:

### Erste Schritte

- **[Web-App einrichten](setup-website.md)** — Bereite deine Website, PWA oder lokalen HTML-Dateien für deine Android-App vor: Nutze eine Remote-URL, bündle Dateien offline in der App oder kombiniere beides mit einem Offline-Fallback.
- **[WebViewGold konfigurieren](setup.md)** — Lade das WebViewGold-Template für Android Studio herunter, füge deine URL ein und entdecke alle integrierten Konfigurationsoptionen — ganz ohne Programmierkenntnisse.

### App-Design

- **[App-Icon](app-icon.md)** — Füge dein individuelles App-Icon Schritt für Schritt in Android Studio zu deiner WebViewGold-Android-App hinzu.
- **[Splash Screen](splash-screen.md)** — Passe den Splash- bzw. Startbildschirm deiner Android-WebView-App mit deinen eigenen Grafiken an.
- **[Navigation Drawer & Footer](navigation-drawer.md)** — Ship an app-like navigation experience with the built-in Material navigation drawer and Material 3 bottom navigation bar — no changes to your website required.

### APIs & Funktionen

- **[URL-Handling-API](url-handling.md)** — Lege fest, welche Links in deiner Android-App, in Chrome Custom Tabs oder im externen Browser geöffnet werden.
- **[Eigene CSS- & JS-API](custom-css-js.md)** — Füge eigene CSS-Stile und JavaScript-Code in jede Seite deiner Android-WebView-App ein — perfekt für App-spezifische Anpassungen.
- **[Multi API Call](multi-api-call.md)** — Rufe mehrere WebViewGold-Daten-APIs in einer einzigen window.location.href-Zuweisung auf – ideal für plattformübergreifende Web-Apps, die auch die iOS-Version nutzen.
- **[Geolocation-API](geolocation.md)** — Aktiviere HTML5-Geolocation in deiner Android-WebView-App und fordere Standortberechtigungen korrekt an.
- **[Push-Benachrichtigungs-API](push-notifications.md)** — Sende Push-Benachrichtigungen an deine Android-App-Nutzer mit OneSignal, Firebase oder Pushwoosh — Einrichtung, Deep Links und nutzerspezifisches Targeting erklärt.
- **[AdMob-Ads-API](admob.md)** — Monetarisiere deine Android-App mit Google-AdMob-Banner- und Interstitial-Anzeigen — Konfiguration und JavaScript-Trigger.
- **[Facebook-Ads-API](facebook-ads.md)** — Zeige Banner- und Interstitial-Anzeigen des Facebook Audience Network in deiner WebViewGold-Android-App an.
- **[Datei-Downloader-API](file-downloader.md)** — Lass Nutzer Bilder, PDFs und andere Dateien aus deiner Web-App auf ihr Android-Gerät herunterladen.
- **[Natives Video (PiP) API](native-video.md)** — Spiele Videos nativ mit Picture-in-Picture-Unterstützung in deiner Android-WebView-App ab.
- **[App-Zurücksetzen-API](reset-app.md)** — Setze Cache, Cookies und lokalen Speicher deiner Android-WebView-App mit einem einzigen Link oder JavaScript-Aufruf zurück.
- **[Ladeanzeige-API](loading-sign.md)** — Blende die native Ladeanzeige bei Bedarf ein oder aus und passe das Ladeerlebnis deiner Android-App an.
- **[Zwischenablage-API](clipboard.md)** — Kopiere Text in die Android-Zwischenablage und lies deren Inhalt aus deiner Web-App per JavaScript aus.
- **[UUID-API](uuid.md)** — Identifiziere App-Installationen mit einer eindeutigen UUID, die an deine WebView-URL angehängt oder per JavaScript abgerufen wird.
- **[Taschenlampen-API](flashlight.md)** — Steuere die Taschenlampe des Geräts aus deiner Web-App mit einfachen JavaScript-Links in WebViewGold für Android.
- **[App Links / Deep Linking](app-links.md)** — Öffne Links zu deiner Domain direkt in deiner Android-App mit App Links und Deep Linking über ein eigenes URL-Schema.
- **[ShareIntent-API](share-intent.md)** — Empfange Inhalte, die aus anderen Android-Apps geteilt werden, direkt in deiner WebView-App über Share Intents.
- **[App-Teilen-Dialog-API](app-sharing-dialog.md)** — Löse den nativen Android-Teilen-Dialog aus deiner Web-App aus, damit Nutzer deine App oder beliebige URLs teilen können.
- **[In-App-Rating-API](in-app-rating.md)** — Bitte deine Nutzer um eine Google-Play-Bewertung: Löse den nativen „App bewerten“-Dialog per rateapp:// aus deiner Web-App aus oder lass WebViewGold automatisch fragen.
- **[In-App-Käufe-API](in-app-purchases.md)** — Verkaufe digitale Güter und Abonnements in deiner Android-WebView-App mit Google Play Billing.
- **[IAP History API](iap-history.md)** — Return the user's Google Play purchase history as window.purchaseHistory so your web app can list subscriptions or unlock premium content client-side.
- **[QR-Code-Scanner-API](qr-code-scanner.md)** — Öffne einen nativen QR-Code-Scanner aus deiner Web-App und verarbeite die Scan-Ergebnisse per URL oder JavaScript.
- **[Scan-Modus-API](scanning-mode.md)** — Optimiere das Kamera-Scanverhalten des QR- und Barcode-Scanners in WebViewGold für Android.
- **[Barcode-Scanner-API](barcode-scanner.md)** — Scanne EAN-, UPC- und andere Barcodes nativ in deiner Android-WebView-App und übergib die Ergebnisse an deine Web-App.
- **[Screenshot-API](take-screenshot.md)** — Erstelle programmgesteuert einen Screenshot des aktuellen App-Bildschirms und teile oder speichere ihn — per JavaScript.
- **[App-Versionsprüfung-API](app-version-check.md)** — Erkenne die installierte App-Version aus deiner Web-App und fordere Nutzer bei Bedarf zum Update auf.
- **[Kontakte-API](contacts.md)** — Greife aus deiner Web-App auf das Adressbuch des Geräts zu: Lies Kontakte mit Nutzerberechtigung in WebViewGold für Android.
- **[Dynamische-UI-API](dynamic-ui.md)** — Ändere native UI-Elemente wie die Statusleistenfarbe dynamisch aus deiner Web-App unter Android.
- **[Haptisches-Feedback-API](haptic-feedback.md)** — Löse natives Vibrations-Feedback aus deiner Web-App aus — für ein natives App-Gefühl unter Android.
- **[NFC-Plugin](nfc.md)** — Lies NFC-Tags nativ in deiner Android-WebView-App und übergib die Tag-Daten an deine Web-App.
- **[Open App Settings API](open-app-settings.md)** — Send the user straight to the system App-info screen from your web app to manage permissions, notifications, storage, or force-stop your Android app.
- **[Reconnect API](reconnect.md)** — Reload the last online URL from your offline / fallback HTML page — the perfect "Try again" button for your custom offline screen.
- **[Read/Write Value API](read-write-value.md)** — Persist small strings on the device from JavaScript and read them back — for theme, language, session tokens, or onboarding state.
- **[Biometric Auth API](biometric-auth.md)** — Prompt fingerprint or face authentication with the native Android BiometricPrompt directly from your web app.
- **[Document Scanner](document-scanner.md)** — Add a Scan document option to the file upload dialog — the user scans up to 5 pages and your web app receives a PDF like any other upload.
- **[Printer API](printer.md)** — Send a remote image or PDF to the Android system print dialog — Wi-Fi printers, cloud print, or Save-as-PDF, straight from your web app.
- **[Health Connect API](health-connect.md)** — Read and write Android Health Connect records from JavaScript — mirrors the WebViewGold HealthKit API on iOS so one web app covers both platforms.

### Erstellen & Veröffentlichen

- **[Firebase Crashlytics](crashlytics.md)** — Ship crash reports and non-fatal events to your Firebase project, with runtime opt-in / opt-out from your web app.
- **[Erstellen & Veröffentlichen](publish.md)** — Veröffentliche deine WebView-App im Google Play Store: kompletter Veröffentlichungsservice, manueller Prozess und Ändern des Paketnamens.

### Mehr

- **[Danksagungen & Lizenzen](credits.md)** — Lizenzbedingungen für WebViewGold für Android, wann du eine Envato Extended License benötigst, und Open-Source-Danksagungen.
- **[WebViewGold bewerten](rate.md)** — Gefällt dir WebViewGold? Bewerte es in Sekunden auf CodeCanyon — so bleiben die Updates am Laufen.
- **[iOS- & macOS-Versionen](more-platforms.md)** — Bringe deine App auf weitere Plattformen: Hole dir WebViewGold für iOS und macOS und verwende dieselbe Web-App weiter.
- **[Support & Kontakt](support.md)** — Schnelle Hilfe: Durchsuche das WebViewGold Support Center, kontaktiere unser Team direkt oder fordere professionelle individuelle App-Entwicklung made in Germany an.

## Eine Web-App, alle Plattformen

Verwende dieselbe Website für iOS-, Android- & macOS-Apps mit WebViewGold.

- [WebViewGold für iOS](../ios/README.md)
- [WebViewGold für macOS](../macos/README.md)

**Sprachen:** [🇺🇸 English](../../android/README.md) · **🇩🇪 Deutsch** · [🇫🇷 Français](../../fr/android/README.md) · [🇪🇸 Español](../../es/android/README.md) · [🇨🇳 中文](../../zh/android/README.md)

> [!TIP]
> **Zu wenig Zeit? Wir richten deine App für dich ein.** Unser Team konfiguriert, erstellt & reicht deine WebViewGold-App ein – schlüsselfertig, mit schneller Bearbeitung, Made in Germany. [App einrichten lassen →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_android_doc_online)
>
> **Im Browser erstellen:** Kein Mac, keine IDE: Der **WebViewGold Cloud Builder** konfiguriert, erstellt & lädt deine App online hoch. [Cloud Builder entdecken →](https://www.webviewgold.com/cloud-builder?ref=android_docs)
