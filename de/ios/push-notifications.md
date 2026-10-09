---
title: "Push-Benachrichtigungen-API (OneSignal, Firebase, Pushwoosh) – WebViewGold für iOS Dokumentation"
description: "Sende Push-Benachrichtigungen an die Nutzer deiner iOS-App mit OneSignal, Firebase oder Pushwoosh – Einrichtung, Deep Links und nutzerspezifisches Targeting erklärt."
lang: "de"
product: "WebViewGold für iOS"
platform: "iOS"
category: "APIs & Funktionen"
slug: "push-notifications"
canonical_url: "https://www.webviewgold.com/de/docs/iOS/push-notifications/"
keywords:
  - "Push-Benachrichtigungen-API"
  - "WebViewGold für iOS"
  - "Website in App umwandeln"
  - "WebView-App-Dokumentation"
  - "iOS WebView SDK"
  - "PWA zu App"
  - "HTML zu App"
  - "JavaScript-Bridge"
last_updated: "2026-10-09"
---

# Push-Benachrichtigungen-API (OneSignal, Firebase, Pushwoosh) – WebViewGold für iOS

> **Zusammenfassung:** Sende Push-Benachrichtigungen an die Nutzer deiner iOS-App mit OneSignal, Firebase oder Pushwoosh – Einrichtung, Deep Links und nutzerspezifisches Targeting erklärt.

[Dokumentation](../README.md) › [WebViewGold für iOS](README.md) › Push-Benachrichtigungen-API

**Plattform:** iOS · **Kategorie:** APIs & Funktionen · **Online-Version:** [www.webviewgold.com/de/docs/iOS/push-notifications/](https://www.webviewgold.com/de/docs/iOS/push-notifications/)

---

Push-Benachrichtigungen sind Benachrichtigungen, die auf deinem Smartphone erscheinen, ohne dass die App geöffnet werden muss. Diese Art von Nachrichten ermöglicht eine hervorragende Interaktion mit Kunden und Nutzern der App. Deine App muss nicht geöffnet sein, um solche Benachrichtigungen zu empfangen. Auf diese Weise verpassen deine Kunden keine wichtigen Neuigkeiten oder Nachrichten. Push-Benachrichtigungen eignen sich für viele Anwendungsfälle, z. B. für Bestellaktualisierungen, Live-Ticker oder Social-Media-Communities. Für den Empfang von Push-Nachrichten muss eine Internetverbindung vorhanden sein. WebViewGold unterstützt mehrere Wege, um deine Nutzer per Push-Benachrichtigung zu erreichen. Wenn du Push-Benachrichtigungen **NICHT** verwenden möchtest, öffne **Config.swift** und setze **askforpushpermissionatfirstrun** auf *false*, um zu verhindern, dass der App-Nutzer nach der Benachrichtigungsberechtigung gefragt wird.

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

Dies kann für verschiedene Situationen genutzt werden (Countdowns, Happy Hours, spezielle Erinnerungen, ...).

Um alle geplanten lokalen Push-Benachrichtigungen zu **abbrechen**, verwende:

```html
<script>
window.location.href = "sendlocalpushmsg://push.send.cancel";
</script>
```

## Nativen Push-Berechtigungsstatus prüfen

Rufe `checkNativePushPermissions://` auf, um zu prüfen, ob der Nutzer die native iOS-Mitteilungsberechtigung erteilt hat. Das Ergebnis wird als JavaScript-Variable `nativePushEnabled` (`true` oder `false`) in deine Web-App injiziert — nützlich z. B., um einen eigenen Hinweis mit Link zu den [App-Einstellungen](open-app-settings.md) anzuzeigen, wenn Mitteilungen deaktiviert sind:

```html
<script>
window.location.href = "checkNativePushPermissions://";
setTimeout(function() {
  if (typeof nativePushEnabled !== "undefined" && !nativePushEnabled) {
    // z. B. einen Banner mit Link zu settingsapp:// anzeigen
  }
}, 500);
</script>
```

## Option 2: Pushwoosh Remote-Push-Benachrichtigungen verwenden

**WebViewGold-Nutzer erhalten zwei Monate Pushwoosh kostenlos!**\
Um dieses Angebot in Anspruch zu nehmen, sende bitte deine WebViewGold-Lizenz per E-Mail an [pushwoosh-love@webviewgold.com](mailto:pushwoosh-love@webviewgold.com) und du erhältst in Kürze eine persönliche Antwort.

Wenn du [Pushwoosh](https://www.pushwoosh.com) (eine ausgezeichnete Wahl!) für Push-Benachrichtigungen in deiner App verwenden möchtest, aktiviere einfach die Optionen in **Config.swift**, indem du **kPushwooshEnable** auf **true** setzt, und stelle sicher, dass du auch die **Pushwoosh_APPID** in der Datei **Info.plist** mit deiner eigenen Pushwoosh-Application-ID aktualisierst.\
![Sende eine neue Push-Benachrichtigung an deine App-Nutzer mit Pushwoosh](../../assets/ios/img/pushwoosh1.webp)\
![Sende eine neue Push-Benachrichtigung an deine App-Nutzer mit Pushwoosh](../../assets/ios/img/pushwoosh2.webp)

Stelle sicher, dass du auch die Pushwoosh-Einrichtung auf deren [Website](https://www.pushwoosh.com) einschließlich des Zertifikatsimports abschließt.\
Glückwunsch, deine Einrichtung ist bereits abgeschlossen. Du bist nun bereit, Push-Benachrichtigungen zu versenden:\
[![Sende eine neue Push-Benachrichtigung an deine App-Nutzer mit Pushwoosh](../../assets/ios/img/pushwoosh3.webp)](https://www.pushwoosh.com)\
Möchtest du **die individuelle Geräte-ID jedes Nutzers** für personalisierte Push-Benachrichtigungen oder zur weiteren Verarbeitung erhalten? Setze einfach **kPushwooshEnhanceUrl** in **Config.swift** auf **true**, um ?pushwoosh_id=XYZ an deine WebView-URL anzuhängen:\
![Sende eine neue Push-Benachrichtigung an deine App-Nutzer mit Pushwoosh](../../assets/ios/img/pushwoosh4.webp)\
Wenn deine WebView-URL beispielsweise https://www.example.org lautet, ruft WebViewGold stattdessen https://www.example.org?pushwoosh_id=XYZ auf. Denke daran, dass nur die erste URL-Anfrage diese GET-Variable erhält. Bitte speichere diese daher in einer Session oder einem Cookie zur späteren Verwendung auf deinen verlinkten Seiten. Alternativ oder zusätzlich kannst du **diese Information auf jeder Seite per JavaScript abrufen und verarbeiten**:

```html
<script>
window.location.href = "getpushwooshid://";
alert(pushwooshplayerid);
</script>
```

## Option 3: OneSignal Remote-Push-Benachrichtigungen verwenden

Wenn du [OneSignal](https://www.onesignal.com) in deiner App verwenden möchtest, aktiviere diese Optionen in **Config.swift** (indem du die Werte von **false** auf **true** setzt) und stelle sicher, dass du auch den Platzhalter **oneSignalID** durch deine eigene ID ersetzt. \
![Aktiviere die OneSignal-Funktionen von WebViewGold für die Unterstützung von Push-Benachrichtigungen](../../assets/ios/img/onesignal_configs.webp)

[Generiere](https://documentation.onesignal.com/docs/generate-an-ios-push-certificate) nun ein iOS-Push-Zertifikat und importiere es:\
[![Generiere ein iOS-Zertifikat für die OneSignal-Push-Zustellung](../../assets/ios/img/onesignal_guide_cert.webp)](https://documentation.onesignal.com/docs/generate-an-ios-push-certificate)

Super, du bist **fertig**. Du kannst nun Push-Benachrichtigungen versenden:\
[![Sende eine neue Push-Benachrichtigung an deine App-Nutzer](../../assets/ios/img/onesignal_newmsg.webp)](https://www.onesignal.com)\
Wenn du das OneSignal-URL-Deeplinking verwenden möchtest (öffnet eine bestimmte URL beim Klicken auf deine Benachrichtigung), füge bitte die gewünschte URL in einem benutzerdefinierten Feld namens **url** hinzu:\
<a id="getonesignalid"></a>![Gib eine Webadresse in OneSignal ein, um Deeplinking in deine WebView-App zu ermöglichen](../../assets/ios/img/onesignal_deeplinking.webp)

Im OneSignal.com-Backend kannst du dieses Key-Value-Fenster ausfüllen, nachdem du auf „Advanced settings" geklickt hast. Mit der OneSignal-API kannst du das Feld „url" zur API-Anfrage hinzufügen (<https://documentation.onesignal.com/docs/onesignal-api>).\
Möchtest du **<a id="onesignalruntime"></a>die individuelle Abonnement-ID jedes Nutzers** auf deinem Server zur weiteren Verarbeitung und für **individuelle Nutzer-**Push-Nachrichten erhalten? Aktiviere einfach die Option **kPushEnhanceUrl** in Config.swift (indem du den Wert von *false* auf *true* setzt), um ?onesignal_push_id=XYZ an deine WebView-URL anzuhängen. Wenn deine WebView-URL https://www.example.org lautet, ruft WebViewGold stattdessen https://www.example.org?onesignal_push_id=XYZ auf. Nur die erste URL-Anfrage erhält diese GET-Variable. Speichere diese daher in einer Session oder einem Cookie, um auf deinen verlinkten Seiten darauf zugreifen zu können. Eine alternative oder zusätzliche Möglichkeit besteht darin, **die Information auf jeder Seite per JavaScript abzurufen und zu verarbeiten**:

```html
<script>
window.location.href = "getonesignalplayerid://";
alert(onesignalplayerid);
</script>
```

**Alternativ solltest du in Betracht ziehen, `autoInjectVariable` in Config.swift auf `true` zu setzen, um diesen (und andere) Werte automatisch in JavaScript zu injizieren, ohne zuvor eine URL aufrufen zu müssen.**

## Option 4: Firebase Remote-Push-Benachrichtigungen verwenden

**Schritt 1: Firebase-Projekt erstellen**\
Beginne mit der Erstellung eines Firebase-Projekts in deiner [Firebase-Konsole](https://console.firebase.google.com/). Dies ist eine Voraussetzung für die Integration von Firebase in deine WebViewGold-App.\
**Schritt 2: Deine App bei Firebase registrieren**\
Sobald dein Firebase-Projekt bereit ist, kannst du deine WebViewGold-App hinzufügen, indem du diese Schritte befolgst:\
a. Navigiere zur Projektübersichtsseite in deiner Firebase-Konsole und wähle das iOS-Symbol, um den App-Registrierungsprozess zu starten.\
b. Um eine neue App zu deinem Projekt hinzuzufügen, klicke auf **App hinzufügen** und wähle die Plattformoptionen aus. Gib im entsprechenden Feld die Bundle-ID deiner App ein. Diese ID ist entscheidend und lässt sich wie folgt ermitteln:
- Öffne dein App-Projekt in Xcode.
- Wähle den Projektnamen oben im Navigator aus, um zum Tab „General" zu gelangen.
- Die Bundle-ID deiner App wird unter dem Feld „Bundle Identifier" angezeigt (z. B. com.onlineappcreator.webviewgold).\
Stelle sicher, dass du die exakte Bundle-ID eingibst, die deine App verwendet. Dieser Wert ist nach der Registrierung deiner App bei Firebase unveränderlich.\
c. Schließe die Einrichtung ab, indem du die erforderlichen App-Informationen bereitstellst, u. a.:
- App-Nickname: Eine praktische Bezeichnung zu deiner Referenz in der Firebase-Konsole.
- App-Store-ID: Erforderlich für Firebase Dynamic Links und die Google-Analytics-Integration. Du kannst diese später hinzufügen, falls deine App noch keine besitzt.\
**Schritt 3: Deine App registrieren**\
Klicke auf *App registrieren*, um den Registrierungsprozess abzuschließen.\
**Schritt 4: GoogleService-Info.plist herunterladen**\
Lade diese Konfigurationsdatei herunter und ersetze den Platzhalter in deinem WebViewGold-Projekt durch die heruntergeladene GoogleService-Info.plist-Datei.\
**Schritt 5: Firebase in WebViewGold aktivieren**\
Setze in der Datei Config.swift die Variable **kFirebasePushEnabled** auf **true**, um die Firebase-Funktionen zu aktivieren.\
**Schritt 6: APN einrichten und App signieren**\
Generiere einen APN-Schlüssel für Firebase, lade ihn hoch und signiere dann deine App mit dem Firebase-Provisioning-Profil. Eine ausführliche Anleitung findest du in der [Firebase-Dokumentation zu iOS-Zertifikaten](https://firebase.google.com/docs/cloud-messaging/ios/certs).\
**Schritt 7: URL-Deeplinking implementieren (optional)**\
Um Firebase-URL-Deeplinking zu unterstützen, füge die Ziel-URL in einem **Custom Data**-Feld unter **Additional options (optional)** hinzu, mit **Key** = „url" und **Value** = {gewünschte URL}.

![Füge eine benutzerdefinierte URL für Deeplinking-Zwecke im WebView hinzu](../../assets/ios/img/firebase_deeplinking.webp)\
Um ein Firebase-Topic zu abonnieren, setze **firebaseTopic** in Config.swift auf den Namen des gewünschten Topics.\
Möchtest du **die individuelle Abonnement-ID jedes Nutzers** auf deinem Server zur weiteren Verarbeitung und für **<a id="firebaseruntime"></a>individuelle Nutzer-**Push-Nachrichten erhalten? Aktiviere einfach die Option **kFirebaseEnhanceUrl** in Config.swift (indem du den Wert von *false* auf *true* setzt), um ?firebase_push_id=XYZ an deine WebView-URL anzuhängen. Wenn deine WebView-URL https://www.example.org lautet, ruft WebViewGold stattdessen https://www.example.org?firebase_push_id=XYZ auf. Nur die ERSTE URL-Anfrage erhält diese GET-Variable. Speichere diese daher in einer Session oder einem Cookie, um auf deinen verlinkten Seiten darauf zugreifen zu können. Eine alternative oder zusätzliche Möglichkeit besteht darin, **die Information auf jeder Seite per JavaScript abzurufen und zu verarbeiten**:

```html
<script>
window.location.href = "getfirebaseplayerid://";
alert(firebaseplayerid);
</script>
```

**Alternativ solltest du in Betracht ziehen, `autoInjectVariable` in Config.swift auf `true` zu setzen, um diesen (und andere) Werte automatisch in JavaScript zu injizieren, ohne zuvor eine URL aufrufen zu müssen.**

## Option 5: bubble.io Push-Benachrichtigungen verwenden

[![Video ansehen: Push-Benachrichtigungen-API (OneSignal, Firebase, Pushwoosh)](https://img.youtube.com/vi/C0HBXlMSK2E/hqdefault.jpg)](https://www.youtube.com/watch?v=C0HBXlMSK2E)

1. Erstelle eine **bubble.io-App**
2. Installiere das Plugin **[WebViewGold OneSignal Push](https://bubble.io/plugin/webviewgold-onesignal-push-1602240916803x713805488222896100)**:

[![bubble.io WebViewGold OneSignal Push Plugin](../../assets/ios/img/bubblepushplugin-2048x724.webp)](https://bubble.io/plugin/webviewgold-onesignal-push-1602240916803x713805488222896100)
3. Folge den **OneSignal-Anweisungen (siehe oben)** und den **Plugin-Anweisungen (siehe [hier](https://bubble.io/plugin/webviewgold-onesignal-push-1602240916803x713805488222896100) und [hier](https://www.youtube.com/watch?v=C0HBXlMSK2E))**.

---

## Weiterlesen

- ← Vorherige: [Geolocation-API](geolocation.md)
- Weiter →: [AdMob-Ads-API](admob.md)
- Dieselbe Funktion auf anderen Plattformen: [Android – Push-Benachrichtigungs-API](../android/push-notifications.md)
- Sprachen: [🇺🇸 English](../../ios/push-notifications.md) · **🇩🇪 Deutsch** · [🇫🇷 Français](../../fr/ios/push-notifications.md) · [🇪🇸 Español](../../es/ios/push-notifications.md) · [🇨🇳 中文](../../zh/ios/push-notifications.md)

> [!TIP]
> **Zu wenig Zeit? Wir richten deine App für dich ein.** Unser Team konfiguriert, erstellt & reicht deine WebViewGold-App ein – schlüsselfertig, mit schneller Bearbeitung, Made in Germany. [App einrichten lassen →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **Im Browser erstellen:** Kein Mac, keine IDE: Der **WebViewGold Cloud Builder** konfiguriert, erstellt & lädt deine App online hoch. [Cloud Builder entdecken →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
