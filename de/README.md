---
title: "WebViewGold-Dokumentation – Website in native iOS-, Android- & macOS-App umwandeln"
description: "Offizielle WebViewGold-Dokumentation in Markdown: Verwandle jede Website, PWA oder Web-App in eine native iOS-, Android- oder macOS-App – mit Einrichtungsanleitungen, nativen JavaScript-APIs und App-Store-Veröffentlichung."
lang: "de"
product: "WebViewGold"
canonical_url: "https://www.webviewgold.com/de/docs/"
keywords:
  - "WebViewGold"
  - "convert website to app"
  - "WebView app template"
  - "PWA to native app"
  - "iOS WebView app"
  - "Android WebView app"
  - "macOS WebView app"
  - "JavaScript bridge"
last_updated: "2026-10-09"
---

# WebViewGold-Dokumentation – Website in native iOS-, Android- & macOS-App umwandeln

> Offizielle WebViewGold-Dokumentation in Markdown: Verwandle jede Website, PWA oder Web-App in eine native iOS-, Android- oder macOS-App – mit Einrichtungsanleitungen, nativen JavaScript-APIs und App-Store-Veröffentlichung.

WebViewGold ist ein sofort einsetzbares Xcode- und Android-Studio-App-Template von OnlineAppCreator, das deine Website, PWA, dein SaaS-Dashboard, deinen Onlineshop oder deine KI-generierte Web-App in eine native App verpackt. Deine Website bleibt die zentrale Quelle – native Funktionen wie Push-Benachrichtigungen, In-App-Käufe, AdMob, QR-/Barcode-Scanner, Biometrie, Deep Links und vieles mehr aktivierst du über einfache Konfigurationsoptionen und JavaScript-/URL-Schema-APIs.

## Hier starten

| Plattform | Dokumentation | Projekt / IDE | Themen |
|---|---|---|---|
| **iOS** | [WebViewGold für iOS](ios/README.md) | Xcode · Swift (`Config.swift`) | 60 Seiten |
| **Android** | [WebViewGold für Android](android/README.md) | Android Studio · Java (`Config.java`) | 47 Seiten |
| **macOS** | [WebViewGold für macOS](macos/README.md) | Xcode (`config.json`, `index.html`) | 14 Seiten |

## Aufbau dieser Dokumentation

Jede Plattform hat eine Übersichtsseite und pro Thema eine eigene Markdown-Seite. Jede Seite beginnt mit einer kurzen Zusammenfassung und Metadaten (Plattform, Kategorie, kanonische URL) und endet mit Links zum vorherigen/nächsten Thema, zur gleichen Funktion auf anderen Plattformen und zu allen Übersetzungen.

```text
docs-for-github/
├── README.md            (English)
├── llms.txt             (AI / LLM index)
├── llms-full.txt        (all English pages in one file)
├── ios/                 (WebViewGold for iOS)
├── android/             (WebViewGold for Android)
├── macos/               (WebViewGold for macOS)
├── de/ fr/ es/ zh/      (translations, same structure)
└── assets/              (screenshots & images)
```

## Häufig gestellte Fragen

### Was ist WebViewGold?

WebViewGold ist ein natives App-Template für iOS, Android und macOS, das eine Website oder Web-App in eine store-fertige native App umwandelt. Es wird über Envato/CodeCanyon vertrieben und auf [webviewgold.com/docs](https://www.webviewgold.com/de/docs/) dokumentiert.

### Brauche ich Programmierkenntnisse?

Nein. Du fügst deine URL ein und schaltest Optionen in einer Konfigurationsdatei ein oder aus (`Config.swift` unter iOS, `Config.java` unter Android). Native Funktionen löst deine Web-App über einfache Links wie `rateapp://` oder kleine JavaScript-Snippets aus.

### Welche Websites und Frameworks werden unterstützt?

Klassische HTML-/PHP-Seiten, WordPress, PWAs, jQuery-Mobile-Projekte sowie moderne Web-Apps, die mit Lovable, Base44, Bolt, Bubble, React, Vue, Angular oder ähnlichen Buildern erstellt wurden. Du kannst eine Remote-URL laden, lokale HTML-Dateien bündeln oder beides mit einem Offline-Fallback kombinieren.

### Kann ich die App im App Store und bei Google Play veröffentlichen?

Ja. Die Anleitungen unter *Erstellen & Veröffentlichen* erklären den manuellen Weg. Alternativ erstellt und lädt der WebViewGold Cloud Builder deine App im Browser hoch, oder das Team von WeSetupYourWebViewApp richtet alles für dich ein.

### Wo bekomme ich Hilfe?

Im [WebViewGold Support-Center](https://www.webviewgold.com/support-center/) findest du FAQs und bekannte Probleme; alternativ erreichst du das Team über die Seite *Support & Kontakt* deiner Plattform.

## Sprachen

[🇺🇸 English](../README.md) · **🇩🇪 Deutsch** · [🇫🇷 Français](../fr/README.md) · [🇪🇸 Español](../es/README.md) · [🇨🇳 中文](../zh/README.md)

## Über

WebViewGold wird von OnlineAppCreator (jocapps GmbH) in Deutschland entwickelt. Diese Markdown-Ausgabe spiegelt die offizielle Online-Dokumentation unter [www.webviewgold.com/de/docs](https://www.webviewgold.com/de/docs/); die Online-Version ist die kanonische Quelle.
