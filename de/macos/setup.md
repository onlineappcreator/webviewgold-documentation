---
title: "WebViewGold für macOS-Desktop-Apps einrichten – WebViewGold für macOS Dokumentation"
description: "Installiere Xcode, öffne das WebViewGold-für-macOS-Projekt, trage deine URL in index.html ein und konfiguriere config.json – oder bündle eigene lokale HTML-Inhalte."
lang: "de"
product: "WebViewGold für macOS"
platform: "macOS"
category: "Erste Schritte"
slug: "setup"
canonical_url: "https://www.webviewgold.com/de/docs/mac/#setup"
keywords:
  - "WebViewGold einrichten"
  - "WebViewGold für macOS"
  - "Website in App umwandeln"
  - "WebView-App-Dokumentation"
  - "macOS WebView SDK"
  - "PWA zu App"
  - "HTML zu App"
  - "JavaScript-Bridge"
last_updated: "2026-10-09"
---

# WebViewGold für macOS-Desktop-Apps einrichten – WebViewGold für macOS

> **Zusammenfassung:** Installiere Xcode, öffne das WebViewGold-für-macOS-Projekt, trage deine URL in index.html ein und konfiguriere config.json – oder bündle eigene lokale HTML-Inhalte.

[Dokumentation](../README.md) › [WebViewGold für macOS](README.md) › WebViewGold einrichten

**Plattform:** macOS · **Kategorie:** Erste Schritte · **Online-Version:** [www.webviewgold.com/de/docs/mac/#setup](https://www.webviewgold.com/de/docs/mac/#setup)

---

Xcode ist erforderlich, um Apps mit WebViewGold für macOS einzurichten. Xcode ist eine leistungsstarke integrierte Entwicklungsumgebung (IDE), mit der Apps für Apple-Geräte wie iPhones, iPads und Macs erstellt werden. Wichtig zu wissen: Xcode ist ein großes Programm und kann viel Speicherplatz auf deinem Mac belegen. Außerdem ist Xcode nur für Macs verfügbar und nicht mit Windows oder Linux kompatibel. Hier findest du eine Schritt-für-Schritt-Anleitung zum Herunterladen und Installieren von Xcode auf deinem Mac:

- Klicke hier: [**Xcode im Mac App Store herunterladen**](https://apps.apple.com/us/app/xcode/id497799835)
- Klicke auf die Schaltfläche „Laden“ oder „Herunterladen“, um den Download-Vorgang zu starten.
- Sobald der Download abgeschlossen ist, wird das Xcode-Installationsprogramm automatisch gestartet.
- Folge den Anweisungen im Installationsprogramm, um die Installation abzuschließen.
- Öffne Xcode nach Abschluss der Installation über den Ordner „Programme“ oder die Spotlight-Suche.
- Wenn du Xcode zum ersten Mal öffnest, wirst du möglicherweise aufgefordert, zusätzliche Komponenten zu installieren oder den Nutzungsbedingungen zuzustimmen. Folge den Aufforderungen, um die Einrichtung abzuschließen.

Im nächsten Schritt kannst du **[WebViewGold für macOS herunterladen](https://www.webviewgold.com/download/mac/)**, um macOS-Desktop-Apps zu erstellen. Öffne anschließend die **Xcode-Projektdatei**:\
![Hauptdatei des Xcode-Projekts](../../assets/macos/img/xcodefile.jpg)

Wähle den **Ordner „public“** und konfiguriere die Datei **config.json**:\
![Konfigurationsdatei von WebViewGold für macOS](../../assets/macos/img/config1.png)

Öffne die Datei **index.html**, um die URL zu bearbeiten:\
![Füge die URL deiner Web-App in die Datei index.html ein](../../assets/macos/img/config2.png)

Wenn du **lokale HTML-Inhalte** (anstelle einer entfernten URL) verwenden möchtest, ersetze einfach die Datei index.html durch deine eigenen Inhalte.

---

## Weiterlesen

- ← Vorherige: [Web-App einrichten](setup-website.md)
- Weiter →: [App-Symbol](app-icon.md)
- Dieselbe Funktion auf anderen Plattformen: [iOS – WebViewGold konfigurieren](../ios/setup.md) · [Android – WebViewGold konfigurieren](../android/setup.md)
- Sprachen: [🇺🇸 English](../../macos/setup.md) · **🇩🇪 Deutsch** · [🇫🇷 Français](../../fr/macos/setup.md) · [🇪🇸 Español](../../es/macos/setup.md) · [🇨🇳 中文](../../zh/macos/setup.md)

