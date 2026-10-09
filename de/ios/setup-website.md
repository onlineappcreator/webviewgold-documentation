---
title: "Web-App oder Website einrichten – WebViewGold für iOS Dokumentation"
description: "Bereite deine Website, PWA oder lokale HTML-Dateien für deine iOS-App vor: Verwende eine Remote-URL, bündle Dateien offline in der App oder kombiniere beides mit einem Offline-Fallback."
lang: "de"
product: "WebViewGold für iOS"
platform: "iOS"
category: "Erste Schritte"
slug: "setup-website"
canonical_url: "https://www.webviewgold.com/de/docs/iOS/setup-website/"
keywords:
  - "Web-App einrichten"
  - "WebViewGold für iOS"
  - "Website in App umwandeln"
  - "WebView-App-Dokumentation"
  - "iOS WebView SDK"
  - "PWA zu App"
  - "HTML zu App"
  - "JavaScript-Bridge"
last_updated: "2026-10-09"
---

# Web-App oder Website einrichten – WebViewGold für iOS

> **Zusammenfassung:** Bereite deine Website, PWA oder lokale HTML-Dateien für deine iOS-App vor: Verwende eine Remote-URL, bündle Dateien offline in der App oder kombiniere beides mit einem Offline-Fallback.

[Dokumentation](../README.md) › [WebViewGold für iOS](README.md) › Web-App einrichten

**Plattform:** iOS · **Kategorie:** Erste Schritte · **Online-Version:** [www.webviewgold.com/de/docs/iOS/setup-website/](https://www.webviewgold.com/de/docs/iOS/setup-website/)

---

## Option A) URL für den Zugriff auf deine Web-Anwendung verwenden (= Dateien online speichern)

Erstelle eine mobil-optimierte Website oder Web-App und lade sie auf deinen Webserver/Webspace hoch. WebViewGold für iOS ist kompatibel mit klassischem HTML, PHP, WordPress, Progressive Web Apps, HTML5-Spielen, Wix, apprat.io, Bubble, jQuery Mobile sowie modernen KI-/No-Code-Buildern wie Lovable, Base44 und Bolt. In einem typischen Workflow erstellst du die Produkt-UI in jQuery, Lovable, Base44, Bolt, React, Vue, Angular oder deinem bevorzugten Stack und nutzt anschließend WebViewGold als native iOS-App-Hülle, die App-Store-Paketierung, Push-Benachrichtigungen, Geräte-APIs, URL-Handling und weitere native Funktionen ergänzt.

Für die besten Ergebnisse beim App Store Review solltest du dein Web-Erlebnis so gestalten, dass es auf iPhone und iPad zielgerichtet wirkt: responsive Layouts, große Tap-Targets, schnelles First Paint, klare Lade-/Leer-/Fehlerzustände sowie app-typische Navigation. Standardmäßig erlaubt WebViewGold für iOS sowohl HTTPS- als auch HTTP-Inhalte. Für ein Sicherheitsprofil auf Produktionsniveau beschränke den Traffic auf HTTPS, indem du die [iOS-Transport-Security-Einstellung anpasst](https://www.webviewgold.com/support-center/knowledgebase/how-to-prevent-non-https-connections-in-webviewgold-for-ios-removing-nsallowsarbitraryloadsinwebcontent-from-info-plist/), und ziehe die Option `blockfaultyandselfsignedhttpscerts` in Betracht. Ziehe ein professionelles User Experience-/UX-Review auf [UXreviewer.io](https://www.uxreviewer.io) oder bei ähnlichen Diensten in Betracht, um die Store-Freigabebereitschaft und die langfristige Nutzerbindung zu verbessern.

## Option B) Lokalen HTML-Ordner für den Zugriff auf deine Web-Anwendung verwenden (= Dateien innerhalb der App speichern)

WebViewGold unterstützt auch Web-Apps, die auf lokalen HTML-Ordnern basieren: Setze **uselocalhtmlfolder** auf **true** (siehe [nächster Schritt](setup.md)) und kopiere deine HTML-/CSS-/JavaScript-Dateien (einschließlich Unterverzeichnissen) in den Ordner „local-www“ in deinem Xcode-Projekt. Gehe dabei wie folgt vor:

1. Lösche die Standarddateien im Ordner „local-www“, indem du diese in der Xcode-Dateihierarchie auswählst, mit der rechten Maustaste auf „Delete“ klickst und anschließend „Move to Trash“ drückst.
2. Wähle alle Dateien für deine lokale Website aus, ziehe sie per Drag-and-Drop in die Xcode-Dateihierarchie unter den Ordner „local-www“. Stelle sicher, dass „Create folder references“ aktiviert ist, und klicke auf „Finish“.

Ziehe für die besten App-Store-Freigabeergebnisse ein professionelles User Experience-/UX-Review auf [UXreviewer.io](https://www.uxreviewer.io) oder bei ähnlichen Diensten in Betracht. Ein solches UX-Review hilft dir zudem, mit Verbesserungsvorschlägen generell eine bessere Kundenbindung für dein Produkt zu erreichen.

## Option C) HTML-Ordner verwenden, wenn der Nutzer offline ist, und eine Remote-URL, wenn der Nutzer online ist (= Dateien online speichern + Backup-/Fallback-Dateien innerhalb der App speichern)

Kopiere deine HTML-/CSS-/JavaScript-Dateien (einschließlich Unterverzeichnissen) in den Ordner „local-www“ in deinem Xcode-Projekt. Gehe dabei wie folgt vor:

1. Lösche die Standarddateien im Ordner „local-www“, indem du diese in der Xcode-Dateihierarchie auswählst, mit der rechten Maustaste auf „Delete“ klickst und anschließend „Move to Trash“ drückst.
2. Wähle alle Dateien für deine lokale Website aus, ziehe sie per Drag-and-Drop in die Xcode-Dateihierarchie unter den Ordner „local-www“. Stelle sicher, dass „Create folder references“ aktiviert ist, und klicke auf „Finish“.

Setze **uselocalhtmlfolder** auf **false** (siehe [nächster Schritt](setup.md)) und setze **offlinelocalhtmlswitch** auf **true** (siehe [nächster Schritt](setup.md)). Ziehe für die besten App-Store-Freigabeergebnisse ein professionelles User Experience-/UX-Review auf [UXreviewer.io](https://www.uxreviewer.io) oder bei ähnlichen Diensten in Betracht. Ein solches UX-Review hilft dir zudem, mit Verbesserungsvorschlägen generell eine bessere Kundenbindung für dein Produkt zu erreichen.

---

## Weiterlesen

- ← Zurück zu: [Übersicht](README.md)
- Weiter →: [WebViewGold konfigurieren](setup.md)
- Dieselbe Funktion auf anderen Plattformen: [Android – Web-App einrichten](../android/setup-website.md) · [macOS – Web-App einrichten](../macos/setup-website.md)
- Sprachen: [🇺🇸 English](../../ios/setup-website.md) · **🇩🇪 Deutsch** · [🇫🇷 Français](../../fr/ios/setup-website.md) · [🇪🇸 Español](../../es/ios/setup-website.md) · [🇨🇳 中文](../../zh/ios/setup-website.md)

> [!TIP]
> **Zu wenig Zeit? Wir richten deine App für dich ein.** Unser Team konfiguriert, erstellt & reicht deine WebViewGold-App ein – schlüsselfertig, mit schneller Bearbeitung, Made in Germany. [App einrichten lassen →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **Im Browser erstellen:** Kein Mac, keine IDE: Der **WebViewGold Cloud Builder** konfiguriert, erstellt & lädt deine App online hoch. [Cloud Builder entdecken →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
