---
title: "WebViewGold für macOS – Dokumentation | Website in Mac-App umwandeln"
description: "Offizielle WebViewGold-Dokumentation für macOS: Verwandle deine Website, PWA, dein SaaS-Dashboard oder HTML-Projekt in eine native Mac-Desktop-App – mit Xcode-Einrichtung, Konfigurationsoptionen, JavaScript-APIs, Veröffentlichungshinweisen und Implementierungshinweisen im SDK-Stil."
lang: "de"
product: "WebViewGold für macOS"
platform: "macOS"
canonical_url: "https://www.webviewgold.com/de/docs/mac/"
keywords:
  - "WebViewGold für macOS"
  - "Website in App umwandeln"
  - "WebView-App-Dokumentation"
  - "macOS WebView SDK"
  - "PWA zu App"
  - "HTML zu App"
  - "JavaScript-Bridge"
last_updated: "2026-10-09"
---

# WebViewGold für macOS – Dokumentation

![WebViewGold für macOS](../../assets/macos/img/header.png)

> Offizielle WebViewGold-Dokumentation für macOS: Verwandle deine Website, PWA, dein SaaS-Dashboard oder HTML-Projekt in eine native Mac-Desktop-App – mit Xcode-Einrichtung, Konfigurationsoptionen, JavaScript-APIs, Veröffentlichungshinweisen und Implementierungshinweisen im SDK-Stil.

[Dokumentation](../README.md) › WebViewGold für macOS

Verwandle deine Website, PWA, dein SaaS-Dashboard, deinen Onlineshop oder deine KI-generierte Web-App in wenigen Minuten in eine native macOS-App. Nutze WebViewGold wie ein leichtgewichtiges App-SDK: konfiguriere deine URL, aktiviere native APIs, integriere JavaScript-Bridge-Befehle und veröffentliche eine store-fertige App, ohne dein Web-Produkt neu aufzubauen.

WebViewGold funktioniert mit klassischen HTML/PHP-Seiten, WordPress, jQuery-Mobile-Projekten und modernen Web-Apps, die mit Lovable, Base44, Bolt, Bubble, React, Vue, Angular oder ähnlichen Buildern erstellt wurden. Die folgende Dokumentation erläutert den Einrichtungsablauf, native Feature-APIs, Sicherheitsaspekte und Veröffentlichungsschritte in einem technischen, implementierungsorientierten Format.

**[Anleitung starten →](setup-website.md)** · [WebViewGold herunterladen](https://www.webviewgold.com/download/mac/)

## Schnellstart

1. **[Web-App einrichten](setup-website.md)** — Verwende eine Remote-URL, bündele lokale HTML-Dateien oder kombiniere beides mit einem Offline-Fallback.
2. **[WebViewGold konfigurieren](setup.md)** — Füge deine URL ein und passe jede Option in einer einfachen Konfigurationsdatei an – ohne Programmieren.

## Alle Themen, APIs & Funktionen

Alles, was WebViewGold für macOS kann – jedes Thema auf einer eigenen Seite:

### Erste Schritte

- **[Web-App einrichten](setup-website.md)** — Bereite deine Website, PWA oder Web-App für WebViewGold für macOS vor: unterstützte Technologien (HTML, PHP, WordPress, PWA, Lovable, Base44, Bolt …) und Tipps für ein natives Desktop-Erlebnis.
- **[WebViewGold einrichten](setup.md)** — Installiere Xcode, öffne das WebViewGold-für-macOS-Projekt, trage deine URL in index.html ein und konfiguriere config.json – oder bündle eigene lokale HTML-Inhalte.

### App-Design

- **[App-Symbol](app-icon.md)** — Ersetze das App-Symbol deiner WebViewGold-für-macOS-Desktop-App durch deine eigenen, passend skalierten Bilddateien.
- **[App-Name](app-name.md)** — Ändere den Anwendungsnamen deiner WebViewGold-für-macOS-Desktop-App in Xcode.
- **[Text des Offline-Bildschirms](offline-screen.md)** — Passe den Text des Offline-Bildschirms deiner Mac-WebView-App in OfflineOverlay.xib im Interface Builder an.
- **[Dialog beim ersten Start](first-run-dialog.md)** — Bearbeite den Text des Dialogs beim ersten Start deiner Mac-WebView-App in FirstRunWindow.xib (Interface Builder).
- **[Begrüßungsbildschirm](splash-screen.md)** — Ändere den Text des Begrüßungsbildschirms in SplashScreen.xib und die maximale Anzeigedauer in Preferences.m von WebViewGold für macOS.

### APIs & Funktionen

- **[In-App Purchases API](in-app-purchases.md)** — Verkaufe In-App-Käufe und Abonnements im Mac App Store direkt aus deiner Web-App: Produkt-ID in Constants.h eintragen und Käufe per inapppurchase://-Link auslösen.
- **[UUID API](uuid.md)** — Übergib eine nicht personenbezogene, eindeutige Geräte-ID (UUID) per get-uuid:// an JavaScript, um Geräte zu erkennen und Einstellungen wiederherzustellen.
- **[Deeplinking API](deep-linking.md)** — Starte deine WebViewGold-für-macOS-App über ein Custom URL Scheme und öffne direkt eine bestimmte Seite – Deeplinking Schritt für Schritt erklärt.

### Mehr

- **[Danksagungen & Lizenzen](credits.md)** — Lizenzinformationen, Marken und Open-Source-Danksagungen (MacGap, MIT-Lizenz) für WebViewGold für macOS.
- **[WebViewGold bewerten](rate.md)** — Gefällt dir WebViewGold für macOS? Bewerte es in 10 Sekunden auf CodeCanyon – das hält die Updates am Laufen.
- **[Weiter mit iOS & Android](more-platforms.md)** — Nutze deine Web-App auch mobil: WebViewGold für iOS & Android holen – plus photos2webgallery für macOS.
- **[Kontakt](support.md)** — Hilfe zu WebViewGold für macOS: Antworten im Support-Center finden oder das Team direkt kontaktieren.

## Eine Web-App, alle Plattformen

Verwende dieselbe Website für iOS-, Android- & macOS-Apps mit WebViewGold.

- [WebViewGold für iOS](../ios/README.md)
- [WebViewGold für Android](../android/README.md)

**Sprachen:** [🇺🇸 English](../../macos/README.md) · **🇩🇪 Deutsch** · [🇫🇷 Français](../../fr/macos/README.md) · [🇪🇸 Español](../../es/macos/README.md) · [🇨🇳 中文](../../zh/macos/README.md)

