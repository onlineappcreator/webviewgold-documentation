---
title: "Push-Benachrichtigungs-API (OneSignal, Firebase, Pushwoosh) – WebViewGold für Android Dokumentation"
description: "Sende Push-Benachrichtigungen an deine Android-App-Nutzer mit OneSignal, Firebase oder Pushwoosh — Einrichtung, Deep Links und nutzerspezifisches Targeting erklärt."
lang: "de"
product: "WebViewGold für Android"
platform: "Android"
category: "APIs & Funktionen"
slug: "push-notifications"
canonical_url: "https://www.webviewgold.com/de/docs/android/push-notifications/"
keywords:
  - "Push-Benachrichtigungs-API"
  - "WebViewGold für Android"
  - "Website in App umwandeln"
  - "WebView-App-Dokumentation"
  - "Android WebView SDK"
  - "PWA zu App"
  - "HTML zu App"
  - "JavaScript-Bridge"
last_updated: "2026-10-09"
---

# Push-Benachrichtigungs-API (OneSignal, Firebase, Pushwoosh) – WebViewGold für Android

> **Zusammenfassung:** Sende Push-Benachrichtigungen an deine Android-App-Nutzer mit OneSignal, Firebase oder Pushwoosh — Einrichtung, Deep Links und nutzerspezifisches Targeting erklärt.

[Dokumentation](../README.md) › [WebViewGold für Android](README.md) › Push-Benachrichtigungs-API

**Plattform:** Android · **Kategorie:** APIs & Funktionen · **Online-Version:** [www.webviewgold.com/de/docs/android/push-notifications/](https://www.webviewgold.com/de/docs/android/push-notifications/)

---

Push-Benachrichtigungen sind Benachrichtigungen, die auf deinem Smartphone erscheinen, ohne dass die App geöffnet werden muss. Diese Art von Nachrichten ermöglicht eine hervorragende Interaktion mit Kunden und Nutzern der App. Deine App muss dafür nicht geöffnet sein. Auf diese Weise verpassen deine Kunden keine wichtigen Neuigkeiten oder Nachrichten. Push-Benachrichtigungen eignen sich für viele Anwendungsfälle, z. B. für Bestellaktualisierungen, Live-Ticker oder Social-Media-Communities. Für den Empfang von Push-Nachrichten muss eine Internetverbindung vorhanden sein. WebViewGold unterstützt mehrere Wege, um deine Nutzer per Push-Benachrichtigung zu erreichen.

## Option 1: Lokale Push-Benachrichtigung per JavaScript-API verwenden

Du kannst ein Code-Snippet (JavaScript) in deine Website einfügen, um eine Push-Benachrichtigung zu definieren, die **nach** dem Schließen deiner App angezeigt werden kann (die Planung erfolgt, während die App geöffnet ist). Dies funktioniert ganz ohne OneSignal-Konfiguration.

```html
<script>
var title = "Your cart is waiting!"; //notification title
var message = "You have left a cart full of dreams and deals behind. Dont leave it feeling abandoned"; //notification message
var seconds = 120; //seconds from now on
var url = "https://myshop.org/cart.php"; //deep-linking URL

window.location.href = "sendlocalpushmsg://push.send?s="+ seconds +"=msg!"+ message +"&!#"+ title +"&!#"+ url +"";
</script>
```

Dies kann für verschiedene Situationen genutzt werden (Countdowns, Happy Hours (wie im Beispielcode), Erinnerungen, ...).\
Um alle geplanten lokalen Push-Benachrichtigungen abzubrechen, verwende:

```html
<script>
window.location.href = "sendlocalpushmsg://push.send.cancel";
</script>
```

## Option 2: Pushwoosh Remote-Push-Benachrichtigungen verwenden

**WebViewGold-Nutzer erhalten zwei Monate Pushwoosh kostenlos!**\
Um dieses Angebot in Anspruch zu nehmen, sende bitte deine WebViewGold-Lizenz per E-Mail an [pushwoosh-love@webviewgold.com](mailto:pushwoosh-love@webviewgold.com) und du erhältst in Kürze eine persönliche Antwort.

Wenn du [Pushwoosh](https://www.pushwoosh.com) (eine ausgezeichnete Wahl!) für Push-Benachrichtigungen in deiner App verwenden möchtest, aktiviere einfach die Optionen in **Config.java**, indem du **PUSHWOOSH_ENABLED** auf **true** setzt, und stelle sicher, dass du auch die **Pushwoosh-IDs** in den Dateien **string.xml** und **AndroidManifest.xml** mit deinen eigenen Pushwoosh-IDs aktualisierst:\
![Sende eine neue Push-Benachrichtigung an deine App-Nutzer mit Pushwoosh](../../assets/android/img/pushwoosh1.webp)\
![Sende eine neue Push-Benachrichtigung an deine App-Nutzer mit Pushwoosh](../../assets/android/img/pushwoosh2a.webp)\
![Sende eine neue Push-Benachrichtigung an deine App-Nutzer mit Pushwoosh](../../assets/android/img/pushwoosh2b.webp)

Glückwunsch, deine Einrichtung ist bereits abgeschlossen. Du bist nun bereit, Push-Benachrichtigungen zu versenden:\
[![Sende eine neue Push-Benachrichtigung an deine App-Nutzer mit Pushwoosh](../../assets/android/img/pushwoosh3.webp)](https://www.pushwoosh.com)\
Möchtest du **die individuelle Geräte-ID jedes Nutzers** für personalisierte Push-Benachrichtigungen oder zur weiteren Verarbeitung erhalten? Setze einfach **WONDERPUSH_ENHANCE_WEBVIEW_URL** in **Config.java** auf **true**, um ?pushwoosh_id=XYZ an deine WebView-URL anzuhängen:\
![Sende eine neue Push-Benachrichtigung an deine App-Nutzer mit Pushwoosh](../../assets/android/img/pushwoosh4.webp)\
Wenn deine WebView-URL beispielsweise https://www.example.org lautet, ruft WebViewGold stattdessen https://www.example.org?pushwoosh_id=XYZ auf. Denke daran, dass nur die erste URL-Anfrage diese GET-Variable erhält. Bitte speichere diese daher in einer Session oder einem Cookie zur späteren Verwendung auf deinen verlinkten Seiten. Alternativ oder zusätzlich kannst du **diese Information auf jeder Seite per JavaScript abrufen und verarbeiten**:

```html
<script>
window.location.href = "getpushwooshid://";
alert(pushwooshplayerid);
</script>
```

## Option 3: OneSignal Remote-Push-Benachrichtigungen verwenden

Wenn du OneSignal für die Konfiguration von Remote-Push-Benachrichtigungen verwenden möchtest, führt dich dieses Video-Tutorial Schritt für Schritt durch den Prozess.

[![Video ansehen: Push-Benachrichtigungs-API (OneSignal, Firebase, Pushwoosh)](https://img.youtube.com/vi/0cPNGqMQVm0/hqdefault.jpg)](https://www.youtube.com/watch?v=0cPNGqMQVm0)

Nach Abschluss dieses Video-Tutorials kannst du mit OneSignal problemlos Remote-Push-Benachrichtigungen für deine mobile Anwendung einrichten. So kannst du wichtige Updates, Erinnerungen oder Werbeinhalte direkt an die Geräte deiner Nutzer senden, selbst wenn diese deine App gerade nicht verwenden.

Zusammengefasst verläuft die Konfiguration von OneSignal für Push-Benachrichtigungen wie folgt:

1. Öffne Android Studio und suche die OneSignal-Optionen. Standardmäßig sind PUSH_ENABLE, PUSH_ENHANCE_WEBVIEW_URL und PUSH_RELOAD_ON_USERID auf false gesetzt; ändere diese auf true.
2. Öffne dein OneSignal-Konto und wähle deine Organisation und deinen App-Namen aus.

***Falls du deine App im OneSignal-Projekt noch nicht angelegt hast, folge zunächst diesen Schritten.***

[![Video ansehen: Push-Benachrichtigungs-API (OneSignal, Firebase, Pushwoosh)](https://img.youtube.com/vi/X9jepbGFw7A/hqdefault.jpg)](https://www.youtube.com/watch?v=X9jepbGFw7A)

***Beachte, dass du für die Erstellung und Konfiguration deines OneSignal-Kontos eine JSON-Datei benötigst. Um diese Datei zu erhalten, muss dein Firebase-Konto konfiguriert sein. Wenn du Firebase noch nicht konfiguriert hast, um die JSON-Datei zu erhalten, sieh dir dieses zusätzliche Tutorial an.***

[![Video ansehen: Push-Benachrichtigungs-API (OneSignal, Firebase, Pushwoosh)](https://img.youtube.com/vi/qAqdhcd3ngs/hqdefault.jpg)](https://www.youtube.com/watch?v=qAqdhcd3ngs)

- Sobald du deine OneSignal-App erstellt hast, gehe in den Einstellungsbereich, wähle Native Android als Plattform und kopiere den erhaltenen App-ID-Code.
- Öffne Android Studio und gehe zum Bereich Gradle Scripts und wähle build.gradle (Module:app).
- Füge im Abschnitt ONE_SIGNAL_APP_ID den zuvor aus OneSignal kopierten Code ein.
- Erstelle anschließend deine *APK*-Datei und starte sie auf einem physischen Gerät.
- Gehe in OneSignal zu deinem App-Projekt, wähle *New Message* und klicke auf *New Push*.
- Fülle die erforderlichen Informationen aus und fertig! Du hast deine OneSignal-Push-Nachrichten erfolgreich getestet.

Ersetze **ic_stat_onesignal_default.png**, um das **Standard-Fallback-Glockensymbol** der OneSignal-Push-Benachrichtigungen zu ersetzen. \
Möchtest du **die individuelle Abonnement-ID jedes Nutzers** auf deinem Server zur weiteren Verarbeitung und für **<a id="firebaseruntime"></a>individuelle Nutzer-**Push-Nachrichten erhalten? Aktiviere einfach die Option **PUSH_ENHANCE_WEBVIEW_URL** in Config.java (indem du den Wert von false auf true änderst), um ?onesignal_push_id=XYZ an deine WebView-URL anzuhängen. Wenn deine WebView-URL https://www.example.org lautet, ruft WebViewGold stattdessen https://www.example.org?onesignal_push_id=XYZ auf. Nur die ERSTE URL-Anfrage erhält diese GET-Variable. Speichere diese daher in einer Session oder einem Cookie, um auf deinen verlinkten Seiten darauf zugreifen zu können. Eine alternative oder zusätzliche Möglichkeit besteht darin, **die Information auf jeder Seite per JavaScript abzurufen und zu verarbeiten**:

```html
<script>
window.location.href = "getonesignalplayerid://";
alert(onesignalplayerid);
</script>
```

**Alternativ solltest du in Betracht ziehen,  `AUTO_INJECT_VARIABLES`  in Config.java auf `true` zu setzen, um diesen (und andere) Werte automatisch in JavaScript zu injizieren, ohne zuvor eine URL aufrufen zu müssen.**

## Option 4: Firebase Remote-Push-Benachrichtigungen verwenden

Wenn du Firebase für die Konfiguration von Remote-Push-Benachrichtigungen verwenden möchtest, führt dich dieses Video-Tutorial Schritt für Schritt durch den Prozess.

[![Video ansehen: Push-Benachrichtigungs-API (OneSignal, Firebase, Pushwoosh)](https://img.youtube.com/vi/X-02iJSBaAQ/hqdefault.jpg)](https://www.youtube.com/watch?v=X-02iJSBaAQ)

Zusammengefasst verläuft die Konfiguration von Firebase für Push-Benachrichtigungen wie folgt:

### 1. Paketnamen umbenennen und Firebase-Projekt erstellen

Bitte [benenne den Paketnamen](publish.md#renamepackagename) deiner WebViewGold-Android-App um. Anschließend musst du in deiner [Firebase-Konsole](https://console.firebase.google.com/) ein Firebase-Projekt erstellen.

### 2. Firebase in WebViewGold aktivieren

Öffne in Android Studio die Datei Config.java und setze die Variable **FIREBASE_PUSH_ENABLED** auf **true**.

![Ersetze google-services.json in deiner WebViewGold-Android-App](../../assets/android/img/firebase2.webp)

### 3. Deine App bei Firebase registrieren

Nachdem du dein Firebase-Projekt erstellt hast, kannst du deine WebViewGold-App hinzufügen.

a. Klicke in der Mitte der Projektübersichtsseite der Firebase-Konsole auf das Android-Symbol, um den Einrichtungsprozess zu starten.

b. Wenn du deinem Firebase-Projekt bereits eine App hinzugefügt hast, klicke auf **App hinzufügen**, um die Plattformoptionen anzuzeigen.
Gib den Paketnamen deiner App ein, wie er [in diesem Schritt](publish.md) geändert/definiert wurde.
Stelle sicher, dass du den Paketnamen eingibst, den deine App verwendet. Du kannst diesen Wert nach der Registrierung deiner App bei deinem Firebase-Projekt nicht mehr hinzufügen oder ändern.\
**4. Klicke auf die Schaltfläche *App registrieren*.**
**5. google-services.json herunterladen**
Klicke auf „google-services.json herunterladen", um deine Firebase-Android-Konfigurationsdatei (google-services.json) zu erhalten, und ersetze die im WebViewGold-Projekt bereits enthaltene Beispieldatei mit Hilfe des Mac Finders oder des Windows Explorers:\
![Ersetze google-services.json in deiner WebViewGold-Android-App](../../assets/android/img/firebase1.webp)\
 **Das war's!**\
Wenn du das Firebase-URL-Deeplinking verwenden möchtest (öffnet eine bestimmte URL beim Klicken auf deine Benachrichtigung), füge bitte die gewünschte URL in einem **Custom Data**-Feld (im Bereich **Additional options (optional)**) mit **Key** = „url" und **Value** = {die gewünschte URL} hinzu.\
![Füge eine benutzerdefinierte URL für Deeplinking-Zwecke im WebView hinzu](../../assets/android/img/firebase_deeplinking.webp)\
Möchtest du **die individuelle Abonnement-ID jedes Nutzers** auf deinem Server zur weiteren Verarbeitung und für **individuelle Nutzer-**Push-Nachrichten erhalten? Aktiviere einfach die Option **FIREBASE_PUSH_ENHANCE_WEBVIEW_URL** in Config.java (indem du den Wert von false auf true änderst), um ?firebase_push_id=XYZ an deine WebView-URL anzuhängen. Wenn deine WebView-URL https://www.example.org lautet, ruft WebViewGold stattdessen https://www.example.org?firebase_push_id=XYZ auf. Nur die ERSTE URL-Anfrage erhält diese GET-Variable. Speichere diese daher in einer Session oder einem Cookie, um auf deinen verlinkten Seiten darauf zugreifen zu können. Eine alternative oder zusätzliche Möglichkeit besteht darin, **die Information auf jeder Seite per JavaScript abzurufen und zu verarbeiten**:

```html
<script>
window.location.href = "getfirebaseplayerid://";
alert(firebaseplayerid);
</script>
```

**Alternativ solltest du in Betracht ziehen,  `AUTO_INJECT_VARIABLES`  in Config.java auf `true` zu setzen, um diesen (und andere) Werte automatisch in JavaScript zu injizieren, ohne zuvor eine URL aufrufen zu müssen.**

## Option 5: bubble.io Push-Benachrichtigungen verwenden

[![Video ansehen: Push-Benachrichtigungs-API (OneSignal, Firebase, Pushwoosh)](https://img.youtube.com/vi/C0HBXlMSK2E/hqdefault.jpg)](https://www.youtube.com/watch?v=C0HBXlMSK2E)

1. Erstelle eine **bubble.io-App**
2. Installiere das Plugin **[WebViewGold OneSignal Push](https://bubble.io/plugin/webviewgold-onesignal-push-1602240916803x713805488222896100)**:

[![bubble.io WebViewGold OneSignal Push Plugin](../../assets/android/img/bubblepushplugin-2048x724.webp)](https://bubble.io/plugin/webviewgold-onesignal-push-1602240916803x713805488222896100)
3. Folge den **OneSignal-Anweisungen (siehe oben)** und den **Plugin-Anweisungen (siehe [hier](https://bubble.io/plugin/webviewgold-onesignal-push-1602240916803x713805488222896100) und [hier](https://www.youtube.com/watch?v=C0HBXlMSK2E))**.

---

## Push-Berechtigungs-APIs: Im richtigen Moment fragen & aktuellen Status prüfen

### Push-Berechtigung manuell anfordern (`registerpush://`)

Standardmäßig fragt WebViewGold den Nutzer beim ersten Start der App nach der Berechtigung für Push-Benachrichtigungen (`requirePush = true` in **Config.java**). Berechtigungsabfragen konvertieren deutlich besser, wenn sie im passenden Kontext erscheinen – du kannst `requirePush` daher auch auf `false` setzen und den nativen Berechtigungsdialog im perfekten Moment aus deiner Web-App auslösen (z. B. nach dem Login oder Onboarding):

```html
<a href="registerpush://">Benachrichtigungen aktivieren</a>
```

```javascript
window.location.href = "registerpush://";
```

**Hinweis:** Dafür muss mindestens ein Push-Dienst in **Config.java** aktiviert sein (`PUSH_ENABLED`, `FIREBASE_PUSH_ENABLED` oder `PUSHWOOSH_ENABLED`).

### Aktuellen Push-Berechtigungsstatus prüfen (`checkNativePushPermissions://`)

Um herauszufinden, ob der Nutzer Push-Benachrichtigungen aktuell erlaubt, rufe auf:

```javascript
window.location.href = "checkNativePushPermissions://";
```

WebViewGold injiziert anschließend die JavaScript-Variable `nativePushEnabled` (`true` oder `false`) in deine Seite. Ab Android 13 müssen sowohl die System-Benachrichtigungseinstellung als auch die Laufzeitberechtigung `POST_NOTIFICATIONS` erteilt sein, damit der Wert `true` ist. Beispiel:

```html
<script>
window.location.href = "checkNativePushPermissions://";
setTimeout(function () {
    if (typeof nativePushEnabled !== "undefined" && nativePushEnabled) {
        console.log("Push-Benachrichtigungen sind aktiviert");
    } else {
        // z. B. eigenen Hinweis anzeigen und registerpush:// oder settingsapp:// anbieten
    }
}, 500);
</script>
```

Wurde die Berechtigung dauerhaft verweigert, kannst du den Nutzer über die [Open-App-Settings-API](open-app-settings.md) (`settingsapp://`) in die Systemeinstellungen führen.

---

## Weiterlesen

- ← Vorherige: [Geolocation-API](geolocation.md)
- Weiter →: [AdMob-Ads-API](admob.md)
- Dieselbe Funktion auf anderen Plattformen: [iOS – Push-Benachrichtigungen-API](../ios/push-notifications.md)
- Sprachen: [🇺🇸 English](../../android/push-notifications.md) · **🇩🇪 Deutsch** · [🇫🇷 Français](../../fr/android/push-notifications.md) · [🇪🇸 Español](../../es/android/push-notifications.md) · [🇨🇳 中文](../../zh/android/push-notifications.md)

> [!TIP]
> **Zu wenig Zeit? Wir richten deine App für dich ein.** Unser Team konfiguriert, erstellt & reicht deine WebViewGold-App ein – schlüsselfertig, mit schneller Bearbeitung, Made in Germany. [App einrichten lassen →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_android_doc_online)
>
> **Im Browser erstellen:** Kein Mac, keine IDE: Der **WebViewGold Cloud Builder** konfiguriert, erstellt & lädt deine App online hoch. [Cloud Builder entdecken →](https://www.webviewgold.com/cloud-builder?ref=android_docs)
