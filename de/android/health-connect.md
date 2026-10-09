---
title: "Health Connect API – WebViewGold für Android Dokumentation"
description: "Read and write Android Health Connect records from JavaScript — mirrors the WebViewGold HealthKit API on iOS so one web app covers both platforms."
lang: "de"
product: "WebViewGold für Android"
platform: "Android"
category: "APIs & Funktionen"
slug: "health-connect"
canonical_url: "https://www.webviewgold.com/de/docs/android/health-connect/"
keywords:
  - "Health Connect API"
  - "WebViewGold für Android"
  - "Website in App umwandeln"
  - "WebView-App-Dokumentation"
  - "Android WebView SDK"
  - "PWA zu App"
  - "HTML zu App"
  - "JavaScript-Bridge"
last_updated: "2026-10-09"
---

# Health Connect API – WebViewGold für Android

> **Zusammenfassung:** Read and write Android Health Connect records from JavaScript — mirrors the WebViewGold HealthKit API on iOS so one web app covers both platforms.

[Dokumentation](../README.md) › [WebViewGold für Android](README.md) › Health Connect API

**Plattform:** Android · **Kategorie:** APIs & Funktionen · **Online-Version:** [www.webviewgold.com/de/docs/android/health-connect/](https://www.webviewgold.com/de/docs/android/health-connect/)

---

Die **Health-Connect-API** liest und schreibt Gesundheitsdaten über [Android Health Connect](https://health.google/health-connect-android/). Sie spiegelt die iOS-HealthKit-Funktionalität von WebViewGold, sodass eine einzige Web-App auf beiden Plattformen mit Gesundheitsdaten sprechen kann. Lese-Aufrufe liefern immer die **heutige Gesamtmenge** für den angefragten Record-Typ.

## Einen Wert lesen

```html
<a href="readhealthkit://StepsRecord" onclick="setTimeout(show, 300)">
  My steps today
</a>

<script>
function show() {
  // Injected variable name matches the sanitized record name.
  alert(StepsRecord); // e.g. "8421.0 steps"
}
</script>
```

## Einen Wert schreiben

Format: `writehealthkit://<RecordName>//<value>`

```html
<a href="writehealthkit://StepsRecord//1000">Log 1000 steps</a>
```

Bei Erfolg injiziert die App `<RecordName> = "WRITE_SUCCESS"`. Bei Fehlern die Fehlermeldung.

**Unterstützte Records:** Jeder Health-Connect-Record-Typ, für den deine App eine Berechtigung angefragt hat. Häufige:

- `StepsRecord`
- `HeartRateRecord`
- `WeightRecord`
- `SleepSessionRecord`
- `HydrationRecord`
- `ActiveCaloriesBurnedRecord`
- `DistanceRecord`

## Einrichtung

1. **Health Connect** auf dem Gerät installieren (auf Android 14+ vorinstalliert).
2. Beim ersten Aufruf zeigt die App den Health-Connect-Berechtigungsdialog; der Nutzer erlaubt Lese- und/oder Schreibzugriff auf die gewünschten Records.
3. Falls Health Connect nicht unterstützt wird, ist der injizierte Wert `"Health Connect not supported"`.

**Hinweise:** Werte werden als `"<Zahl> <Einheit>"` zurückgegeben (z. B. `"75.4 kg"`). Setzt Android 8.0 (API 26) oder höher voraus.

---

## Weiterlesen

- ← Vorherige: [Printer API](printer.md)
- Weiter →: [Firebase Crashlytics](crashlytics.md)
- Dieselbe Funktion auf anderen Plattformen: [iOS – HealthKit-Plugin](../ios/healthkit.md)
- Sprachen: [🇺🇸 English](../../android/health-connect.md) · **🇩🇪 Deutsch** · [🇫🇷 Français](../../fr/android/health-connect.md) · [🇪🇸 Español](../../es/android/health-connect.md) · [🇨🇳 中文](../../zh/android/health-connect.md)

> [!TIP]
> **Zu wenig Zeit? Wir richten deine App für dich ein.** Unser Team konfiguriert, erstellt & reicht deine WebViewGold-App ein – schlüsselfertig, mit schneller Bearbeitung, Made in Germany. [App einrichten lassen →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_android_doc_online)
>
> **Im Browser erstellen:** Kein Mac, keine IDE: Der **WebViewGold Cloud Builder** konfiguriert, erstellt & lädt deine App online hoch. [Cloud Builder entdecken →](https://www.webviewgold.com/cloud-builder?ref=android_docs)
