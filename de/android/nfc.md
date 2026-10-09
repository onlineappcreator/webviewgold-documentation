---
title: "NFC-Plugin – WebViewGold für Android Dokumentation"
description: "Lies NFC-Tags nativ in deiner Android-WebView-App und übergib die Tag-Daten an deine Web-App."
lang: "de"
product: "WebViewGold für Android"
platform: "Android"
category: "APIs & Funktionen"
slug: "nfc"
canonical_url: "https://www.webviewgold.com/de/docs/android/nfc/"
keywords:
  - "NFC-Plugin"
  - "WebViewGold für Android"
  - "Website in App umwandeln"
  - "WebView-App-Dokumentation"
  - "Android WebView SDK"
  - "PWA zu App"
  - "HTML zu App"
  - "JavaScript-Bridge"
last_updated: "2026-10-09"
---

# NFC-Plugin – WebViewGold für Android

> **Zusammenfassung:** Lies NFC-Tags nativ in deiner Android-WebView-App und übergib die Tag-Daten an deine Web-App.

[Dokumentation](../README.md) › [WebViewGold für Android](README.md) › NFC-Plugin

**Plattform:** Android · **Kategorie:** APIs & Funktionen · **Online-Version:** [www.webviewgold.com/de/docs/android/nfc/](https://www.webviewgold.com/de/docs/android/nfc/)

---

**Near-Field Communication (NFC)** ermöglicht es zwei Geräten oder einem Gerät und einem NFC-Tag, drahtlos zu kommunizieren, wenn sie sich in unmittelbarer Nähe befinden. NFC wird auf Android-Geräten häufig zum Lesen und Schreiben kleiner Datenmengen verwendet und ist damit ein effektives Werkzeug, um Informationen über NFC-fähige Karten oder Tags auszutauschen.

Mit der **WebViewGold-NFC-API** kann deine Web-App NFC-Tags direkt über eine JavaScript-Bridge lesen und beschreiben – vom Teilen von Kontaktdaten bis zum Einbetten von Textausschnitten.

**Schreiben**\
Um einen Wert auf ein NFC-Tag zu schreiben, sende aus deiner Web-App einen Befehl, indem du folgende URL lädst: `writenfc://?value=data`\
Beispiel:\
`<a href="writenfc://?value=WebViewGold.com"> Auf ein NFC-Tag schreiben </a>`\
Damit wechselt deine App in den Schreibmodus und speichert den Wert, bis ein Tag gescannt wird: Sobald der Nutzer ein NFC-Tag an das Gerät hält, wird der Wert darauf geschrieben.

**VCARD (Kontaktkarte) schreiben**\
Verwende dieselbe API wie beim Schreiben von Text und formatiere den Text so:

```
VCARD
FN:John Doe
Title:Developer
TEL;TYPE=CELL:0452641211
```

Trenne die Eigenschaften mit einem Unterstrich (`_`), kodiere Leerzeichen als `%20` und stelle dem Text `VCARD_` voran. Beispiel:

```
writenfc://?value=VCARD_FN:John%20Doe_Title:Developer_TEL;TYPE=CELL:0452641211
```

Eine Liste der unterstützten Eigenschaften findest du unter <https://en.wikipedia.org/wiki/VCard#Properties>.

**Lesen**\
Um ein NFC-Tag zu lesen, lade `readnfc://`. Damit wechselt deine App in den Lesemodus. Scannt der Nutzer ein Tag, gibt die App die gespeicherten Informationen an deine Web-App zurück, indem sie die JavaScript-Funktion `readNFCResult(data)` aufruft – `data` ist der auf dem Tag gespeicherte Wert. Definiere diese JavaScript-Funktion in deiner Web-App, um den Wert zu verarbeiten:

```html
<script>
window.location.href = "readnfc://";

function readNFCResult(data) {
    alert("Inhalt des NFC-Tags: " + data);
}
</script>
```

## So testest du die API

1. Öffne die Config-Datei deines App-Projekts.
2. Trage deinen Purchase Code ein.
3. Setze die App-URL auf die NFC-API-Testseite: <https://webviewgoldtest.github.io/NFCtesting.html>
4. Starte die App auf einem physischen Gerät mit NFC-Unterstützung.
5. Wähle eine der Lese- oder Schreiboptionen, um den entsprechenden Modus zu aktivieren. Gib beim Schreiben einen Wert ein.
6. Halte das NFC-Tag an das Gerät, um den Lese- oder Schreibvorgang abzuschließen. Testseite und App zeigen die Ergebnisse an.

**Mehr benötigt?** Wenn du erweiterte NFC-Funktionen über diese API hinaus benötigst (z. B. spezielle Tag-Typen oder eigene Datenformate), bieten wir individuelle NFC-Plugin-Integrationen an. Sende uns deine Anforderungen per E-Mail an [webviewgold-nfc@onlineappcreator.com](mailto:webviewgold-nfc@onlineappcreator.com) für eine kostenlose Beratung und ein unverbindliches Angebot.

---

## Weiterlesen

- ← Vorherige: [Haptisches-Feedback-API](haptic-feedback.md)
- Weiter →: [Open App Settings API](open-app-settings.md)
- Dieselbe Funktion auf anderen Plattformen: [iOS – NFC-Plugin](../ios/nfc.md)
- Sprachen: [🇺🇸 English](../../android/nfc.md) · **🇩🇪 Deutsch** · [🇫🇷 Français](../../fr/android/nfc.md) · [🇪🇸 Español](../../es/android/nfc.md) · [🇨🇳 中文](../../zh/android/nfc.md)

> [!TIP]
> **Zu wenig Zeit? Wir richten deine App für dich ein.** Unser Team konfiguriert, erstellt & reicht deine WebViewGold-App ein – schlüsselfertig, mit schneller Bearbeitung, Made in Germany. [App einrichten lassen →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_android_doc_online)
>
> **Im Browser erstellen:** Kein Mac, keine IDE: Der **WebViewGold Cloud Builder** konfiguriert, erstellt & lädt deine App online hoch. [Cloud Builder entdecken →](https://www.webviewgold.com/cloud-builder?ref=android_docs)
