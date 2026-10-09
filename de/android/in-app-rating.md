---
title: "In-App-Rating-Dialog-API – WebViewGold für Android Dokumentation"
description: "Bitte deine Nutzer um eine Google-Play-Bewertung: Löse den nativen „App bewerten“-Dialog per rateapp:// aus deiner Web-App aus oder lass WebViewGold automatisch fragen."
lang: "de"
product: "WebViewGold für Android"
platform: "Android"
category: "APIs & Funktionen"
slug: "in-app-rating"
canonical_url: "https://www.webviewgold.com/de/docs/android/in-app-rating/"
keywords:
  - "In-App-Rating-API"
  - "WebViewGold für Android"
  - "Website in App umwandeln"
  - "WebView-App-Dokumentation"
  - "Android WebView SDK"
  - "PWA zu App"
  - "HTML zu App"
  - "JavaScript-Bridge"
last_updated: "2026-10-09"
---

# In-App-Rating-Dialog-API – WebViewGold für Android

> **Zusammenfassung:** Bitte deine Nutzer um eine Google-Play-Bewertung: Löse den nativen „App bewerten“-Dialog per rateapp:// aus deiner Web-App aus oder lass WebViewGold automatisch fragen.

[Dokumentation](../README.md) › [WebViewGold für Android](README.md) › In-App-Rating-API

**Plattform:** Android · **Kategorie:** APIs & Funktionen · **Online-Version:** [www.webviewgold.com/de/docs/android/in-app-rating/](https://www.webviewgold.com/de/docs/android/in-app-rating/)

---

Positive Google-Play-Bewertungen sind einer der stärksten Wachstumstreiber für deine App. Mit der **In-App-Rating-Dialog-API** von WebViewGold bittest du deine Nutzer genau im richtigen Moment um eine Bewertung – zum Beispiel direkt nach einem erfolgreichen Kauf oder nachdem sie eine Aufgabe in deiner Web-App abgeschlossen haben.

## Option 1: Bewertungsdialog manuell aus der Web-App auslösen

Rufe die folgende URL über einen HTML-Link oder aus JavaScript auf, um einen nativen „App bewerten"-Dialog anzuzeigen:

```html
<a href="rateapp://">Gefällt dir die App? Bewerte uns!</a>
```

```javascript
window.location.href = "rateapp://";
```

Bestätigt der Nutzer den Dialog, öffnet sich die Google-Play-Seite deiner App, damit er eine Bewertung hinterlassen kann. Setze dafür `RATE_MY_APP_URL` in **Config.java** auf die Google-Play-URL deiner App:

```java
public static final String RATE_MY_APP_URL = "https://play.google.com/store/apps/details?id=com.yourcompany.yourapp";
```

**Hinweis:** Ist `RATE_MY_APP_URL` leer, werden `rateapp://`-Aufrufe ignoriert. Titel und Text des Dialogs lassen sich über die Einträge `rate_title` und `rate_message` in **strings.xml** anpassen.

## Option 2: WebViewGold automatisch fragen lassen

WebViewGold kann die „App bewerten"-Abfrage auch automatisch anzeigen, nachdem der Nutzer deine App eine Weile verwendet hat. Konfiguriere dieses Verhalten in **Config.java**:

- `SHOW_RATE_DIALOG` – auf `true` setzen, um die automatische Bewertungsabfrage zu aktivieren (oder `false`, um sie zu deaktivieren).
- `RATE_DAYS_UNTIL_PROMPT` – Mindestanzahl an Tagen nach der Installation, bevor die Abfrage erscheint.
- `RATE_LAUNCHES_UNTIL_PROMPT` – Mindestanzahl an App-Starts, bevor die Abfrage erscheint.

## Typische Anwendungsfälle

- Direkt nach einer positiven Interaktion um eine Bewertung bitten (abgeschlossene Bestellung, Level-Aufstieg, erfolgreiche Buchung).
- Zuerst einen eigenen „Gefällt dir die App?"-Flow auf deiner Website anzeigen und nur zufriedene Nutzer zu `rateapp://` weiterleiten.

---

## Weiterlesen

- ← Vorherige: [App-Teilen-Dialog-API](app-sharing-dialog.md)
- Weiter →: [In-App-Käufe-API](in-app-purchases.md)
- Dieselbe Funktion auf anderen Plattformen: [iOS – In-App-Rating-Dialog-API](../ios/in-app-rating.md)
- Sprachen: [🇺🇸 English](../../android/in-app-rating.md) · **🇩🇪 Deutsch** · [🇫🇷 Français](../../fr/android/in-app-rating.md) · [🇪🇸 Español](../../es/android/in-app-rating.md) · [🇨🇳 中文](../../zh/android/in-app-rating.md)

> [!TIP]
> **Zu wenig Zeit? Wir richten deine App für dich ein.** Unser Team konfiguriert, erstellt & reicht deine WebViewGold-App ein – schlüsselfertig, mit schneller Bearbeitung, Made in Germany. [App einrichten lassen →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_android_doc_online)
>
> **Im Browser erstellen:** Kein Mac, keine IDE: Der **WebViewGold Cloud Builder** konfiguriert, erstellt & lädt deine App online hoch. [Cloud Builder entdecken →](https://www.webviewgold.com/cloud-builder?ref=android_docs)
