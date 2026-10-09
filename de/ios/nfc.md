---
title: "NFC-Plugin – WebViewGold für iOS Dokumentation"
description: "Lies NFC-Tags nativ in deiner iOS-WebView-App und übergib die Tag-Daten an deine Web-App."
lang: "de"
product: "WebViewGold für iOS"
platform: "iOS"
category: "Erweiterungen & Plugins"
slug: "nfc"
canonical_url: "https://www.webviewgold.com/de/docs/iOS/nfc/"
keywords:
  - "NFC-Plugin"
  - "WebViewGold für iOS"
  - "Website in App umwandeln"
  - "WebView-App-Dokumentation"
  - "iOS WebView SDK"
  - "PWA zu App"
  - "HTML zu App"
  - "JavaScript-Bridge"
last_updated: "2026-10-09"
---

# NFC-Plugin – WebViewGold für iOS

> **Zusammenfassung:** Lies NFC-Tags nativ in deiner iOS-WebView-App und übergib die Tag-Daten an deine Web-App.

[Dokumentation](../README.md) › [WebViewGold für iOS](README.md) › NFC-Plugin

**Plattform:** iOS · **Kategorie:** Erweiterungen & Plugins · **Online-Version:** [www.webviewgold.com/de/docs/iOS/nfc/](https://www.webviewgold.com/de/docs/iOS/nfc/)

---

Die **Near-Field Communication (NFC)**-Technologie ist eine der neuesten Technologien, die bei mobilen Nutzern sehr beliebt geworden ist. Sie ermöglicht es zwei Geräten oder einem Gerät und einem NFC-Tag, bei geringer Entfernung drahtlos zu kommunizieren. NFC wird auf iOS-Geräten häufig zum Lesen und Schreiben kleiner Datenmengen verwendet und ist damit ein effektives Werkzeug, um Informationen über NFC-fähige Karten oder Tags auszutauschen.

Die NFC-API ermöglicht es Entwicklern, Daten direkt aus dem App-Code auf NFC-Tags zu lesen und zu schreiben. Das eröffnet Apps neue Möglichkeiten der Interaktion mit Nutzern – vom Teilen von Kontaktinformationen bis zum Einbetten von Textausschnitten.

## WebViewGold NFC-Plugin-Integration

Obwohl NFC nicht zum allgemeinen Funktionsumfang von WebViewGold gehört, bieten wir auf individueller Basis eine maßgeschneiderte, einfache WebViewGold NFC-Plugin-Integration (über JavaScript) an.

Bitte sende uns deine Anforderungen (z. B. das Schreiben/Lesen von Textausschnitten und/oder Kontaktkartendaten auf/von NFC-Tags) per E-Mail an [webviewgold-nfc@onlineappcreator.com](mailto:webviewgold-nfc@onlineappcreator.com) für eine kostenlose Beratung und ein unverbindliches Angebot.

**Schreiben**\
Um einen Wert auf einen NFC-Tag zu schreiben, sende einen Befehl aus deiner Web-App, indem du die folgende URL lädst: `writenfc://?value=data`\
Beispiel:\
`<a href="writenfc://?value=WebViewGold.com"> Write to an NFC tag </a>`\
Dadurch wird deine App in den Schreibmodus versetzt und der Wert gespeichert, bis ein Tag gescannt wird.

**Auf eine VCARD schreiben**\
Verwende dieselbe API wie beim Schreiben von Klartext. Formatiere den Text wie folgt:

```
VCARD
FN:John Doe
Title:Developer
TEL;TYPE=CELL:0452641211
_
_
_
```

Trenne die Eigenschaften mit einem Unterstrich (`_`) und stelle dem Text `VCARD_` voran. Eine Liste der unterstützten Eigenschaften findest du unter <https://en.wikipedia.org/wiki/VCard#Properties>.

**Lesen**\
Um einen NFC-Tag zu lesen, lade `readnfc://`. Die App gibt die Informationen an deine Web-App zurück, indem sie `readNFCResult(data, id, tag)` aufruft, wobei `data` der gespeicherte Wert, `id` die Tag-Kennung und `tag` der Tag-Typ ist. Definiere diese JavaScript-Funktion in deiner Web-App, um die Werte zu verarbeiten.

## So testest du die API

1. Öffne die Config-Datei der Codebasis deiner App.
2. Gib deinen Purchase Code ein.
3. Lege als URL der App die NFC-API-Testseite fest: <https://webviewgoldtest.github.io/NFCtesting.html>
4. Führe die App aus.
5. Drücke eine der Lese- oder Schreiboptionen, um den entsprechenden Modus zu aktivieren. Beim Schreiben gibst du einen Wert ein.
6. Halte den NFC-Tag an das Gerät, um den Lese- oder Schreibvorgang abzuschließen. Die Testseite und die App zeigen die Ergebnisse an.

---

## Weiterlesen

- ← Vorherige: [MultiAPICall-Funktion](multi-api-call.md)
- Weiter →: [Siri-Plugin](siri.md)
- Dieselbe Funktion auf anderen Plattformen: [Android – NFC-Plugin](../android/nfc.md)
- Sprachen: [🇺🇸 English](../../ios/nfc.md) · **🇩🇪 Deutsch** · [🇫🇷 Français](../../fr/ios/nfc.md) · [🇪🇸 Español](../../es/ios/nfc.md) · [🇨🇳 中文](../../zh/ios/nfc.md)

> [!TIP]
> **Zu wenig Zeit? Wir richten deine App für dich ein.** Unser Team konfiguriert, erstellt & reicht deine WebViewGold-App ein – schlüsselfertig, mit schneller Bearbeitung, Made in Germany. [App einrichten lassen →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **Im Browser erstellen:** Kein Mac, keine IDE: Der **WebViewGold Cloud Builder** konfiguriert, erstellt & lädt deine App online hoch. [Cloud Builder entdecken →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
