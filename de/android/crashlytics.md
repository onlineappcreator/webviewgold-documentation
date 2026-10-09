---
title: "Firebase Crashlytics – WebViewGold für Android Dokumentation"
description: "Ship crash reports and non-fatal events to your Firebase project, with runtime opt-in / opt-out from your web app."
lang: "de"
product: "WebViewGold für Android"
platform: "Android"
category: "Erstellen & Veröffentlichen"
slug: "crashlytics"
canonical_url: "https://www.webviewgold.com/de/docs/android/crashlytics/"
keywords:
  - "Firebase Crashlytics"
  - "WebViewGold für Android"
  - "Website in App umwandeln"
  - "WebView-App-Dokumentation"
  - "Android WebView SDK"
  - "PWA zu App"
  - "HTML zu App"
  - "JavaScript-Bridge"
last_updated: "2026-10-09"
---

# Firebase Crashlytics – WebViewGold für Android

> **Zusammenfassung:** Ship crash reports and non-fatal events to your Firebase project, with runtime opt-in / opt-out from your web app.

[Dokumentation](../README.md) › [WebViewGold für Android](README.md) › Firebase Crashlytics

**Plattform:** Android · **Kategorie:** Erstellen & Veröffentlichen · **Online-Version:** [www.webviewgold.com/de/docs/android/crashlytics/](https://www.webviewgold.com/de/docs/android/crashlytics/)

---

Die **Firebase-Crashlytics**-Integration sendet anonyme Crash-Reports und Non-Fatal-Events an dein Firebase-Projekt, damit du Stabilitätsprobleme im Live-Betrieb erkennst.

## So aktivierst du die Funktion

1. Richte Firebase für deine App ein und lege die `google-services.json` unter `AndroidStudioSourceCode/app/` ab.
2. Aktiviere Tracking in **Config.java**:

   ```java
   public static final boolean TRACKING_EVENT = true;
   ```

`TRACKING_EVENT = false` deaktiviert alle Tracking-Features (inklusive Crashlytics-Event-Logging und der Trigger `starttracking://` / `endtracking://`).

## Opt-in / Opt-out zur Laufzeit aus der Web-App

WebViewGold respektiert ein pro-Nutzer Tracking-Flag, das auf dem Gerät gespeichert wird. Verwende die Standard-Tracking-Trigger, um es zur Laufzeit zu ändern:

```html
<a href="starttracking://">Enable analytics & crash reports</a>
<a href="endtracking://">Disable analytics & crash reports</a>
```

Ist der Nutzer opted-out, wird die Crashlytics-Erfassung deaktiviert – es wird nichts hochgeladen.

## Was gemeldet wird

- Nicht abgefangene Abstürze (Stack-Traces, Gerätemodell, OS-Version).
- Non-Fatal-Exceptions, die intern von der App-Hülle geloggt werden.
- Standardmäßig werden keine personenbezogenen Nutzerdaten angehängt.

**Wo die Reports zu sehen sind:** Öffne deine **Firebase Console → Crashlytics**. Reports erscheinen in der Regel wenige Minuten nach einem Crash.

**Hinweise:** Die Crashlytics-Initialisierung ist Best-Effort – bei falscher Firebase-Konfiguration läuft die App weiterhin. Erwäge einen Consent-Screen (DSGVO / CCPA), bevor du `starttracking://` erstmals aufrufst.

---

## Weiterlesen

- ← Vorherige: [Health Connect API](health-connect.md)
- Weiter →: [Erstellen & Veröffentlichen](publish.md)
- Sprachen: [🇺🇸 English](../../android/crashlytics.md) · **🇩🇪 Deutsch** · [🇫🇷 Français](../../fr/android/crashlytics.md) · [🇪🇸 Español](../../es/android/crashlytics.md) · [🇨🇳 中文](../../zh/android/crashlytics.md)

> [!TIP]
> **Zu wenig Zeit? Wir richten deine App für dich ein.** Unser Team konfiguriert, erstellt & reicht deine WebViewGold-App ein – schlüsselfertig, mit schneller Bearbeitung, Made in Germany. [App einrichten lassen →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_android_doc_online)
>
> **Im Browser erstellen:** Kein Mac, keine IDE: Der **WebViewGold Cloud Builder** konfiguriert, erstellt & lädt deine App online hoch. [Cloud Builder entdecken →](https://www.webviewgold.com/cloud-builder?ref=android_docs)
