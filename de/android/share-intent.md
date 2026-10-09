---
title: "ShareIntent-API – WebViewGold für Android Dokumentation"
description: "Empfange Inhalte, die aus anderen Android-Apps geteilt werden, direkt in deiner WebView-App über Share Intents."
lang: "de"
product: "WebViewGold für Android"
platform: "Android"
category: "APIs & Funktionen"
slug: "share-intent"
canonical_url: "https://www.webviewgold.com/de/docs/android/share-intent/"
keywords:
  - "ShareIntent-API"
  - "WebViewGold für Android"
  - "Website in App umwandeln"
  - "WebView-App-Dokumentation"
  - "Android WebView SDK"
  - "PWA zu App"
  - "HTML zu App"
  - "JavaScript-Bridge"
last_updated: "2026-10-09"
---

# ShareIntent-API – WebViewGold für Android

> **Zusammenfassung:** Empfange Inhalte, die aus anderen Android-Apps geteilt werden, direkt in deiner WebView-App über Share Intents.

[Dokumentation](../README.md) › [WebViewGold für Android](README.md) › ShareIntent-API

**Plattform:** Android · **Kategorie:** APIs & Funktionen · **Online-Version:** [www.webviewgold.com/de/docs/android/share-intent/](https://www.webviewgold.com/de/docs/android/share-intent/)

---

Die **ShareIntent-API** von WebViewGold ermöglicht es deiner App, als Ziel im nativen Android-Teilen-Dialog zu erscheinen. Damit können Nutzer Inhalte wie Text, URLs oder Bilder (als Base64-Strings) aus einer beliebigen anderen App direkt in deine WebView-basierte App teilen.

## Anwendungsfälle

- Teilen von Links zu Nutzerprofilen, Notizen oder Artikeln direkt in deine App
- Empfangen von Inhalten aus Messaging- oder Browser-Apps
- Senden von Bildern aus der Galerie an deine WebView-Oberfläche (Base64-codiert)

## Schritt 1: Teilen-Unterstützung in AndroidManifest.xml aktivieren

Damit deine App geteilte Daten empfangen kann, entferne die Kommentarzeichen bei den entsprechenden Intent-Filtern in deiner **AndroidManifest.xml**-Datei:

```html
<!-- Receive shared text (e.g., URLs or notes) -->
<intent-filter>
    <action android:name="android.intent.action.SEND" />
    <category android:name="android.intent.category.DEFAULT" />
    <data android:mimeType="text/plain" />
</intent-filter>

<!-- Receive a single shared image -->
<intent-filter>
    <action android:name="android.intent.action.SEND" />
    <category android:name="android.intent.category.DEFAULT" />
    <data android:mimeType="image/*" />
</intent-filter>

<!-- Receive multiple shared images -->
<intent-filter>
    <action android:name="android.intent.action.SEND_MULTIPLE" />
    <category android:name="android.intent.category.DEFAULT" />
    <data android:mimeType="image/*" />
</intent-filter>
```

Sobald diese Filter aktiv sind, erscheint das App-Symbol deiner WebViewGold-basierten App als Teilen-Ziel, wenn Nutzer Inhalte aus einer anderen App teilen.

## Schritt 2: Geteilte Daten in deiner WebView verarbeiten

Wenn ein Nutzer Inhalte in deine App teilt, injiziert WebViewGold den geteilten Inhalt automatisch in eine JavaScript-Variable namens `sharedData`.

```html
<script>
    alert(sharedData); // Displays the shared content (text or base64 image)

</script>
```

- **Text oder URL:** Wird als Klartext an `sharedData` übergeben
- **Bild:** Wird in einen Base64-codierten String umgewandelt und an `sharedData` übergeben

**Beispielhafte Verwendung:** Automatisches Ausfüllen eines Formulars oder Vorschau eines Bildes basierend auf dem empfangenen Inhalt:

```html
<script>
    if (sharedData) {
        document.getElementById("myInput").value = sharedData;
    }
</script>
```

**Hinweis:** Stelle sicher, dass dein JavaScript sowohl Klartext als auch lange Base64-Strings verarbeiten kann. Du kannst auch clientseitige Prüfungen implementieren, um zwischen verschiedenen Inhaltstypen zu unterscheiden.

---

## Weiterlesen

- ← Vorherige: [App Links / Deep Linking](app-links.md)
- Weiter →: [App-Teilen-Dialog-API](app-sharing-dialog.md)
- Dieselbe Funktion auf anderen Plattformen: [iOS – Share Extension](../ios/share-extension.md)
- Sprachen: [🇺🇸 English](../../android/share-intent.md) · **🇩🇪 Deutsch** · [🇫🇷 Français](../../fr/android/share-intent.md) · [🇪🇸 Español](../../es/android/share-intent.md) · [🇨🇳 中文](../../zh/android/share-intent.md)

> [!TIP]
> **Zu wenig Zeit? Wir richten deine App für dich ein.** Unser Team konfiguriert, erstellt & reicht deine WebViewGold-App ein – schlüsselfertig, mit schneller Bearbeitung, Made in Germany. [App einrichten lassen →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_android_doc_online)
>
> **Im Browser erstellen:** Kein Mac, keine IDE: Der **WebViewGold Cloud Builder** konfiguriert, erstellt & lädt deine App online hoch. [Cloud Builder entdecken →](https://www.webviewgold.com/cloud-builder?ref=android_docs)
