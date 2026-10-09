---
title: "ML Kit Document Scanner (PDF) – WebViewGold für Android Dokumentation"
description: "Add a Scan document option to the file upload dialog — the user scans up to 5 pages and your web app receives a PDF like any other upload."
lang: "de"
product: "WebViewGold für Android"
platform: "Android"
category: "APIs & Funktionen"
slug: "document-scanner"
canonical_url: "https://www.webviewgold.com/de/docs/android/document-scanner/"
keywords:
  - "Document Scanner"
  - "WebViewGold für Android"
  - "Website in App umwandeln"
  - "WebView-App-Dokumentation"
  - "Android WebView SDK"
  - "PWA zu App"
  - "HTML zu App"
  - "JavaScript-Bridge"
last_updated: "2026-10-09"
---

# ML Kit Document Scanner (PDF) – WebViewGold für Android

> **Zusammenfassung:** Add a Scan document option to the file upload dialog — the user scans up to 5 pages and your web app receives a PDF like any other upload.

[Dokumentation](../README.md) › [WebViewGold für Android](README.md) › Document Scanner

**Plattform:** Android · **Kategorie:** APIs & Funktionen · **Online-Version:** [www.webviewgold.com/de/docs/android/document-scanner/](https://www.webviewgold.com/de/docs/android/document-scanner/)

---

Die **Document-Scanner**-Funktion fügt dem Standard-Datei-Upload-Dialog eine Option **Dokument scannen** hinzu. Der Nutzer kann bis zu 5 Seiten mit der Kamera scannen; die App erzeugt daraus ein PDF und lädt es über das gewohnte `<input type="file">` deiner Web-App hoch. Angetrieben wird das Ganze von Googles ML Kit Document Scanner.

## So aktivierst du die Funktion

Aktiviere sie in **Config.java**:

```java
public static final boolean ENABLE_ML_KIT_DOCUMENT_SCANNER = true;
```

Setze den Wert auf `false`, um den Eintrag **Dokument scannen** auszublenden.

## Nutzererfahrung

1. Auf deiner Webseite tippt der Nutzer auf ein `<input type="file">`.
2. Die App zeigt einen Upload-Dialog mit Einträgen wie *Dokument scannen*, *Foto aufnehmen*, *Video aufnehmen* und *Aus Galerie wählen* (je nach `accept`-Attribut).
3. Tippt der Nutzer auf **Dokument scannen**, startet der ML-Kit-Scanner von Google: erkennt Kanten, schneidet und optimiert jede Seite, erlaubt weitere Seiten und liefert ein PDF zurück.
4. Das PDF wird an das `<input type="file">` zurückgegeben – deine Web-App erhält es wie jede andere hochgeladene Datei.

**Hinweise:** Setzt Google Play Services voraus (auf allen Standard-Android-Handys mit Play Store vorhanden). Ausgabeformat: **PDF**, maximal 5 Seiten pro Scan. Import aus der Galerie ist im Scanner standardmäßig erlaubt.

---

## Weiterlesen

- ← Vorherige: [Biometric Auth API](biometric-auth.md)
- Weiter →: [Printer API](printer.md)
- Dieselbe Funktion auf anderen Plattformen: [iOS – Dokumentenscanner](../ios/document-scanner.md)
- Sprachen: [🇺🇸 English](../../android/document-scanner.md) · **🇩🇪 Deutsch** · [🇫🇷 Français](../../fr/android/document-scanner.md) · [🇪🇸 Español](../../es/android/document-scanner.md) · [🇨🇳 中文](../../zh/android/document-scanner.md)

> [!TIP]
> **Zu wenig Zeit? Wir richten deine App für dich ein.** Unser Team konfiguriert, erstellt & reicht deine WebViewGold-App ein – schlüsselfertig, mit schneller Bearbeitung, Made in Germany. [App einrichten lassen →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_android_doc_online)
>
> **Im Browser erstellen:** Kein Mac, keine IDE: Der **WebViewGold Cloud Builder** konfiguriert, erstellt & lädt deine App online hoch. [Cloud Builder entdecken →](https://www.webviewgold.com/cloud-builder?ref=android_docs)
