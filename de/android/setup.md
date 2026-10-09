---
title: "WebViewGold für Android einrichten & konfigurieren – WebViewGold für Android Dokumentation"
description: "Lade das WebViewGold-Template für Android Studio herunter, füge deine URL ein und entdecke alle integrierten Konfigurationsoptionen — ganz ohne Programmierkenntnisse."
lang: "de"
product: "WebViewGold für Android"
platform: "Android"
category: "Erste Schritte"
slug: "setup"
canonical_url: "https://www.webviewgold.com/de/docs/android/setup/"
keywords:
  - "WebViewGold konfigurieren"
  - "WebViewGold für Android"
  - "Website in App umwandeln"
  - "WebView-App-Dokumentation"
  - "Android WebView SDK"
  - "PWA zu App"
  - "HTML zu App"
  - "JavaScript-Bridge"
last_updated: "2026-10-09"
---

# WebViewGold für Android einrichten & konfigurieren – WebViewGold für Android

> **Zusammenfassung:** Lade das WebViewGold-Template für Android Studio herunter, füge deine URL ein und entdecke alle integrierten Konfigurationsoptionen — ganz ohne Programmierkenntnisse.

[Dokumentation](../README.md) › [WebViewGold für Android](README.md) › WebViewGold konfigurieren

**Plattform:** Android · **Kategorie:** Erste Schritte · **Online-Version:** [www.webviewgold.com/de/docs/android/setup/](https://www.webviewgold.com/de/docs/android/setup/)

---

**Lade**
die WebViewGold-App-Vorlage für Android Studio
**[hier](https://www.webviewgold.com/download/android) herunter.**
[![WebView-App-Vorlage für Android Studio kaufen](../../assets/android/img/cart.webp)](https://www.webviewgold.com/download/android)

> [!NOTE]
> Möchtest du erstellen, ohne Android Studio zu installieren? Mit dem [**WebViewGold Cloud Builder**](https://www.webviewgold.com/cloud-builder?ref=android_docs) (kostenpflichtiges Add-on) kannst du deine App direkt im Browser konfigurieren, erstellen und in den Play Store hochladen.
>
> [![Video ansehen: WebViewGold für Android einrichten & konfigurieren](https://img.youtube.com/vi/nzgCkydN9OM/hqdefault.jpg)](https://www.youtube.com/watch?v=nzgCkydN9OM)

Lade [**Android Studio**](https://developer.android.com/studio) herunter, falls du Android Studio noch nicht installiert hast.\
Öffne anschließend **Android Studio**:\
![Willkommensbildschirm von Android Studio](../../assets/android/img/androidstudio2020.webp)

Wähle **Open**:\
![Schaltfläche Projekt importieren](../../assets/android/img/androidstudio_welcome2022.webp)\
Wähle deinen Ordner **AndroidStudioSource** aus und warte, bis das Projekt vollständig geladen ist:\
![Dateiauswahl in Android Studio](../../assets/android/img/filepicker.webp)\
Öffne anschließend die Datei **Config.java**, um die wichtigsten Konfigurationsdetails (URL, URL-Handling, UserAgent, Dialoge) zu bearbeiten. Bitte wirf einen Blick auf unseren [YouTube-Kanal](https://www.youtube.com/channel/UChuOoCMcXP_8SQPbZyXTPjA?sub_confirmation=1) für spezifische Einrichtungsanleitungen. Bitte vergiss nicht, deinen [Envato/CodeCanyon Purchase Code](https://help.market.envato.com/hc/en-us/articles/202822600-Where-Is-My-Purchase-Code-) im Feld **PURCHASECODE** für jede von dir veröffentlichte App einzutragen. Pro individuell angepasstem Endprodukt ist eine Lizenz erforderlich. Bitte beachte die Lizenzinformationen zu deinem CodeCanyon-Kauf: [https://codecanyon.net/licenses/standard](https://codecanyon.net/licenses/standard?ref=onlineappcreator)\
Das Hauptkonfigurationsdokument **Config.java** sieht so aus: \
![Config.java ermöglicht die Konfiguration der meisten Einstellungen direkt im Dokument](../../assets/android/img/config.webp)

Die Einrichtung von Apps mit WebViewGold ist **sehr einfach** und erfordert keinerlei Programmierkenntnisse. Bitte wirf einen Blick auf diese **Übersicht** der integrierten Konfigurationsoptionen in der Datei **Config.java**:

[![Video ansehen: WebViewGold für Android einrichten & konfigurieren](https://img.youtube.com/vi/5rlknsdIORE/hqdefault.jpg)](https://www.youtube.com/watch?v=5rlknsdIORE)

| Einstellung | Wert | Beschreibung |
| --- | --- | --- |
| HOST | **erforderlicher Wert** | Dein Domain-Host ohne den Präfix https:// oder http:// (z. B. "www.example.org"). Standardmäßig erlaubt WebViewGold für Android sowohl HTTPS- als auch HTTP-Inhalte. Wenn du die Sicherheit deiner App erhöhen möchtest, indem du ausschließlich HTTPS-Inhalte zulässt, kannst du [diese Einstellung ändern](https://www.webviewgold.com/support-center/knowledgebase/how-to-prevent-non-https-connections-in-webviewgold-for-android-switching-usescleartexttraffic-from-true-to-false/) (und/oder die Option 'BLOCK_SELF_SIGNED_AND_FAULTY_SSL_CERTS' in Betracht ziehen). |
| HOME_URL | **erforderlicher Wert** | Deine vollständige WebView-URL (z. B. "https://www.example.org/app.html"), die in der WebView geladen werden soll. Standardmäßig erlaubt WebViewGold für Android sowohl HTTPS- als auch HTTP-Inhalte. Wenn du die Sicherheit deiner App erhöhen möchtest, indem du ausschließlich HTTPS-Inhalte zulässt, kannst du [diese Einstellung ändern](https://www.webviewgold.com/support-center/knowledgebase/how-to-prevent-non-https-connections-in-webviewgold-for-android-switching-usescleartexttraffic-from-true-to-false/) (und/oder die Option 'BLOCK_SELF_SIGNED_AND_FAULTY_SSL_CERTS' in Betracht ziehen). |
| USE_LOCAL_HTML_FOLDER | **true** oder **false** | Auf *true* setzen, um die lokale HTML-Datei "index.html" anstelle der Remote-WebView-URL zu verwenden |
| FALLBACK_USE_LOCAL_HTML_FOLDER_IF_OFFLINE | **true** oder **false** | Auf *true* setzen, wenn du den Ordner "local-html" verwenden möchtest, sobald der Nutzer offline ist, und die Remote-URL, wenn der Nutzer online ist |
| ACTIVATE_PROGRESS_BAR | **true** oder **false** | Auf *false* setzen, um den Fortschritts-/Ladeindikator zu deaktivieren |
| PHONE_ORIENTATION | Wert (Ausrichtung) | Lege die Ausrichtung für Telefone auf "portrait", "landscape" oder "auto" fest |
| TABLET_ORIENTATION | Wert (Ausrichtung) | Lege die Ausrichtung für Tablets auf "portrait", "landscape" oder "auto" fest |
| USER_AGENT | optional | Definiere einen benutzerdefinierten UserAgent für Web-Anfragen (oder lass das Feld leer, um den Standard-Android-UserAgent zu verwenden) |
| HARDWARE_ACCELERATION | **true** oder **false** | Auf *true* setzen, um Hardwarebeschleunigung zu aktivieren; sie kann die Rendering-Leistung verbessern, aber auch den Speicherverbrauch erhöhen und bei bestimmten Inhalten zu Kompatibilitätsproblemen führen |
| APPEND_LANG_CODE | **true** oder **false** | Auf *true* setzen, wenn du die URL-Anfrage um die Systemsprache erweitern möchtest, z. B. ?webview_language=LANGUAGE CODE (z. B. ?webview_language=EN für englischsprachige Nutzer) |
| AUTO_REFRESH_ENABLED | **true** oder **false** | Auf *true* setzen, wenn die WebView ihren Inhalt automatisch aktualisieren soll, sobald die App aus dem Hintergrund in den Vordergrund zurückkehrt. |
| EXTERNAL_LINK_HANDLING_OPTIONS | **0** oder **1** oder **2** | Auf (0) setzen, um externe Links standardmäßig innerhalb der App zu öffnen; (1), um sie IMMER in einem neuen Tab (einem zusätzlichen In-App-Browser) zu öffnen; (2), um sie IMMER in einem anderen Browser zu öffnen |
| BROWSER_WHITELIST | Liste | Füge hier Domains hinzu, die **immer** im externen Browser geöffnet werden sollen, unabhängig davon, worauf die Option **EXTERNAL_LINK_HANDLING_OPTIONS** gesetzt ist. Um eine weitere Domain hinzuzufügen, trage einen weiteren Host wie folgt ein: ["www.alwaysopeninchrome.com", "www.google.com"]. Bitte trage den Host genau so ein, wie du ihn verlinkst (jedoch niemals mit http/https). |
| BROWSER_BLACKLIST | Liste | Füge hier Domains hinzu, die **niemals** im externen Browser geöffnet werden sollen, unabhängig davon, worauf die Option **EXTERNAL_LINK_HANDLING_OPTIONS** gesetzt ist. Um eine weitere Domain hinzuzufügen, trage einen weiteren Host wie folgt ein: ["www.neveropeninchrome.com", "www.google.com"]. Bitte trage den Host genau so ein, wie du ihn verlinkst (jedoch niemals mit http/https). |
| SPECIAL_LINK_HANDLING_OPTIONS | **0** oder **1** oder **2** | Auf (0) setzen, um spezielle Links in der App zu öffnen; (1) in einem neuen Tab (einem zusätzlichen In-App-Browser); (2) in einem anderen Browser; HINWEIS: Spezielle Links haben das Ziel "_blank" oder enden mit "#"; überschreibt *EXTERNAL_LINK_HANDLING_OPTIONS*, wenn der Link außerdem ein externer Link ist |
| ALWAYS_OPEN_IN_INAPP_TAB | Liste | Füge URL-Präfixe hinzu, die du IMMER in einem In-App-Tab öffnen möchtest (z. B. {"https://www.google.com", "https://www.example.com/page"}), unabhängig davon, worauf **EXTERNAL_LINK_HANDLING_OPTIONS** gesetzt ist. |
| NEVER_OPEN_IN_INAPP_TAB | Liste | Füge URL-Präfixe hinzu, die du NIEMALS in einem In-App-Tab öffnen möchtest (z. B. {"https://www.google.com", "https://www.example.com/page"}), unabhängig davon, worauf **EXTERNAL_LINK_HANDLING_OPTIONS** gesetzt ist. |
| QR_CODE_URL_OPTIONS | **0** oder **1** oder **2** oder **3** oder **4** | Auf (0) setzen, um eine gescannte QR-Code-URL in der App zu öffnen; (1) in einem In-App-Tab; (2) in einem neuen Browser; (3) in einem In-App-Tab, wenn extern; (4) in einem neuen Browser, wenn extern |
| AUTO_INJECT_VARIABLES | **true** oder **false** | Auf *true* setzen, um JavaScript-Variablen automatisch zu setzen; dadurch entfällt der manuelle Aufruf von Methoden wie get-uuid://. Derzeit werden App-Version, OneSignal- und Firebase-Abonnement-IDs sowie die UUID unterstützt. |
| CLEAR_CACHE_ON_STARTUP | **true** oder **false** | Auf *true* setzen, um den WebView-Cache und Cookies bei jedem App-Start zu leeren und keine zwischengespeicherten Versionen deiner Web-App/Website zu verwenden |
| CLEAR_CACHE_ON_EXIT | **true** oder **false** | Auf *true* setzen, um den WebView-Cache und Cookies beim vollständigen Beenden der App zu leeren (du solltest eventuell auch *CLEAR_CACHE_ON_STARTUP* aktivieren, da Systemunterschiede die Zuverlässigkeit beeinträchtigen können) |
| COOKIE_ON_LAUNCH | **true** oder **false** | Auf *true* setzen, um beim App-Start ein eigenes Cookie zum WebView hinzuzufügen |
| COOKIE_ON_LAUNCH_NAME | Textwert | Passe den Namen des beim Start gesetzten Cookies an (erfordert COOKIE_ON_LAUNCH auf *true*) |
| COOKIE_ON_LAUNCH_VALUE | Textwert | Passe den Wert des beim Start gesetzten Cookies an (erfordert COOKIE_ON_LAUNCH auf *true*) |
| COOKIE_ON_LAUNCH_IS_SECURE | **true** oder **false** | Auf *true* setzen, um das Start-Cookie als sicher zu markieren (nur HTTPS) |
| IS_DEEP_LINKING_ENABLED | **true** oder **false** | Auf *true* setzen, um Deep-Linking zu aktivieren |
| IS_CUSTOM_SCHEME_ENABLED | **true** oder **false** | Auf *true* setzen, wenn du benutzerdefinierte Schema-Deeplinks wie `webviewgold://` akzeptieren möchtest |
| CUSTOM_DEEPLINK_SCHEME | **true** oder **false** | Passe hier und auch in der AndroidManifest.xml das Präfix des Deeplinking-Schemas an |
| OPEN_NOTIFICATION_URLS_IN_SYSTEM_BROWSER | **true** oder **false** | Auf *true* setzen, um die Deeplinking-URLs aus Benachrichtigungen im System-Browser anstelle deiner App zu öffnen |
| SPLASH_SCREEN_ACTIVATED | **true** oder **false** | Auf *true* setzen, um den Splash-Screen zu aktivieren |
| SPLASH_TIMEOUT | Zahlenwert (Millisekunden) | Lege das Timeout des Splash-Screens in *Millisekunden* fest (der Ladeindikator wird nach Ablauf dieser Zeit angezeigt, falls die Home-URL noch geladen wird) |
| SPLASH_FADE_OUT | Zahlenwert (Millisekunden) | Dauer der Ausblendungsanimation des Splash-Screens in Millisekunden. Diese Animation beginnt, nachdem alle anderen Verzögerungstimer abgelaufen sind. Auf 0 setzen, um den Ausblendeffekt zu deaktivieren. |
| SPLASH_MIN_TIME | Zahlenwert (Millisekunden) | Mindestdauer (in ms), für die der Splash-Screen angezeigt wird; nur wirksam, wenn *REMAIN_SPLASH_OPTION* auf *true* gesetzt ist. Übersteigt *SPLASH_MIN_TIME* diesen Wert, bleibt der Splash-Screen stattdessen für die Dauer von *SPLASH_MIN_TIME* sichtbar. In solchen Fällen wird dieser Wert zugunsten der längeren Dauer ignoriert. |
| REMAIN_SPLASH_OPTION | **true** oder **false** | Auf *true* setzen, um den Splash-Screen anzuzeigen, bis die Home-URL vollständig geladen ist (überschreibt *SPLASH_TIMEOUT*) |
| SCALE_SPLASH_IMAGE | Prozentwert [0-100] | Lege die Größe des Splash-Screen-Bildes relativ zur kleinsten Bildschirmbreite/-höhe des Geräts fest; Bereich in Prozent [0-100]; Achtung: Wert = 0 blendet das Bild vollständig aus |
| blackStatusBarText | **true** oder **false** | Auf *true* setzen für schwarzen Statusleistentext; auf *false* setzen für weißen Statusleistentext; verwende 'colorPrimaryDark' in style.xml, um die Hintergrundfarbe der Statusleiste festzulegen |
| TRANSPARENT_STATUS_BAR | **true** oder **false** | Auf *true* setzen für eine transparente Statusleiste; auf *false* setzen für eine deckende Statusleiste; verwende 'colorPrimaryDark' in style.xml, um die Hintergrundfarbe der Statusleiste festzulegen |
| enableBioMetricAuth | **true** oder **false** | Auf *true* setzen, um die App-Sperre (biometrische Authentifizierung) für die App zu aktivieren |
| PREVENT_SLEEP | **true** oder **false** | Auf *true* setzen, um zu verhindern, dass das Gerät in den Ruhemodus wechselt, während die App aktiv ist |
| ENABLE_SWIPE_NAVIGATE | **true** oder **false** | Auf *true* setzen, um die Navigation durch Wischen nach links oder rechts zu ermöglichen und so eine Seite zurück oder vor zu navigieren |
| ENABLE_PULL_REFRESH | **true** oder **false** | Auf *true* setzen, um das Aktualisieren der Seite durch Nach-unten-Wischen zu ermöglichen. Zusätzlich kannst du jederzeit `enablepulltorefresh://` oder `disablepulltorefresh://` von deiner Website aus aufrufen, um Pull-to-Refresh dynamisch zu aktivieren oder zu deaktivieren. |
| HIDE_VERTICAL_SCROLLBAR | **true** oder **false** | Auf *true* setzen, um die vertikale Bildlaufleiste auszublenden |
| HIDE_HORIZONTAL_SCROLLBAR | **true** oder **false** | Auf *true* setzen, um die horizontale Bildlaufleiste auszublenden |
| ENABLE_ZOOM | **true** oder **false** | Auf *false* setzen, um Zoom-Funktionen für den App-Nutzer zu verhindern (funktioniert zusätzlich über Skript-Injektion) |
| DISABLE_DARK_MODE | **true** oder **false** | Auf *true* setzen, um den Dark Mode zu deaktivieren (funktioniert nicht auf allen Launchern) |
| HIDE_NAVIGATION_BAR_IN_LANDSCAPE | **true** oder **false** | Auf *true* setzen, um die Navigationsleiste im Querformat auszublenden |
| MAX_TEXT_ZOOM | Zahlenwert | Auf einen Wert größer als 0 setzen, um einen maximalen Text-Zoom festzulegen; auf (0) setzen, um diese Funktion zu deaktivieren.  <br> *Hinweis: Klein = 85, Standard = 100, Groß = 115, Größte = 130* |
| INPUT_SCROLL_HELPER | **true** oder **false** | Auf *true* setzen, um ein einheitliches (per JS-Injektion umgesetztes) Scrollverhalten für Eingabefelder zu erzwingen |
| EXIT_APP_BY_BACK_BUTTON_ALWAYS | **true** oder **false** | Auf *true* setzen, um die App durch Drücken der Hardware-Zurück-Taste zu schließen (anstatt zur letzten Seite zurückzukehren) |
| EXIT_APP_BY_BACK_BUTTON_HOMEPAGE | **true** oder **false** | Auf *true* setzen, um die App durch Drücken der Hardware-Zurück-Taste zu schließen, wenn der Nutzer sich auf der Startseite befindet (auf der kein Zurücknavigieren zu einer vorherigen Seite möglich ist) |
| EXIT_APP_DIALOG | **true** oder **false** | Auf *true* setzen, um den Nutzer vor dem Beenden der App zu fragen, ob er die App wirklich beenden möchte |
| OFFLINE_SCREEN_BACKGROUND_COLOR | Hex-Farbcode | Lege die Hintergrundfarbe des Offline-Bildschirms mithilfe des Hex-Farbcodes fest (z. B. "#ffffff" = Weiß) |
| PREVENT_SCREEN_CAPTURE | **true** oder **false** | Auf *true* setzen, um Nutzer daran zu hindern, Screenshots oder Bildschirmaufnahmen in der App zu erstellen. `onScreenCaptureAttempt()` wird in der Web-App zur Verarbeitung aufgerufen (z. B. zum Anzeigen eines individuellen Modals). |
| UUID_ENHANCE_WEBVIEW_URL | **true** oder **false** | Auf *true* setzen, um der ersten URL-Anfrage den UUID-Parameter 'uuid=XYZ' hinzuzufügen |
| BLOCK_SELF_SIGNED_AND_FAULTY_SSL_CERTS | **true** oder **false** | Auf *true* setzen, um Inhalte zu blockieren, die mit selbstsignierten SSL-(Nutzer-)Zertifikaten oder fehlerhaften SSL-Zertifikaten signiert sind; ziehe außerdem in Betracht, [alle Nicht-HTTPS-Inhalte zu blockieren](https://www.webviewgold.com/support-center/knowledgebase/how-to-prevent-non-https-connections-in-webviewgold-for-android-switching-usescleartexttraffic-from-true-to-false/) |
| BLOCK_ROOTED_DEVICES | **true** oder **false** | Auf *true* setzen, um die App-Funktion zur Erkennung von gerooteten Geräten zu aktivieren und die App auf diesen zu deaktivieren (Hinweis: Root-Erkennung ist nicht immer zuverlässig und funktioniert möglicherweise nicht auf allen Geräten) |
| LINK_DRAG_AND_DROP | **true** oder **false** | Auf *false* setzen, um Drag-and-Drop von Links zu deaktivieren |
| LANDSCAPE_FULLSCREEN_VIDEO | **true** oder **false** | Auf *true* setzen, um Vollbildvideos immer im Querformat anzuzeigen |
| SHOW_FIRSTRUN_DIALOG | **true** oder **false** | Auf *false* setzen, um den Dialog beim ersten App-Start zu deaktivieren |
| SHOW_FACEBOOK_DIALOG | **true** oder **false** | Auf *false* setzen, um den Dialog "Auf Facebook folgen" zu deaktivieren |
| SHOW_RATE_DIALOG | **true** oder **false** | Auf *false* setzen, um den Dialog "App bewerten" zu deaktivieren |
| RATE_DAYS_UNTIL_PROMPT | Zahlenwert (Tage) | Lege die Mindestanzahl an Tagen fest, die nach der Installation der Anwendung vergangen sein müssen, bevor der Dialog "App bewerten" angezeigt wird |
| RATE_LAUNCHES_UNTIL_PROMPT | Zahlenwert (Starts) | Lege die Mindestanzahl an App-Starts fest, bevor der Dialog "App bewerten" angezeigt wird |
| FACEBOOK_DAYS_UNTIL_PROMPT | Zahlenwert (Tage) | Lege die Mindestanzahl an Tagen fest, die nach der Installation der Anwendung vergangen sein müssen, bevor der Dialog "Auf Facebook folgen" angezeigt wird |
| FACEBOOK_LAUNCHES_UNTIL_PROMPT | Zahlenwert (Starts) | Lege die Mindestanzahl an App-Starts fest, bevor der Dialog "App bewerten" angezeigt wird |
| FACEBOOK_URL | Wert (URL) | Lege die URL deiner Facebook-Seite fest |
| ALLOW_IMAGE_DOWNLOAD | **true** oder **false** | Auf *false* setzen, um zu verhindern, dass beim langen Drücken auf ein Bild das Popup "Bilder herunterladen" erscheint |
| PUSH_ENABLED | **true** oder **false** | Auf *true* setzen, um OneSignal Push zu aktivieren (setze die OneSignal-IDs in der Datei build.gradle) |
| PUSH_ENHANCE_WEBVIEW_URL | **true** oder **false** | Auf *true* setzen, wenn du WebView-Haupt-URL-Anfragen um die OneSignal-Abonnement-ID im Format ?onesignal_push_id=XYZ erweitern möchtest (alternativ oder zusätzlich kannst du die OneSignal-Abonnement-ID jederzeit über [getonesignalplayerid://](push-notifications.md) anfordern oder sie automatisch abrufen, wenn du in der Config.java "AUTO_INJECT_VARIABLES" auf "true" setzt) |
| PUSH_RELOAD_ON_USERID | **true** oder **false** | Auf *true* setzen, wenn die WebView neu geladen werden soll, sobald die App eine UserID von OneSignal erhält (setze die OneSignal-IDs in der Datei build.gradle) |
| FIREBASE_PUSH_ENABLED | **true** oder **false** | Auf *true* setzen, um Firebase Push zu aktivieren (ersetze zuvor google-services.json) |
| FIREBASE_PUSH_ENHANCE_WEBVIEW_URL | **true** oder **false** | Auf *true* setzen, wenn du die URL-Anfrage um ?firebase_push_id=XYZ erweitern möchtest (alternativ oder zusätzlich kannst du die Firebase-Abonnement-ID jederzeit über [getfirebaseplayerid://](push-notifications.md#firebaseruntime) anfordern oder sie automatisch abrufen, wenn du in der Config.java "AUTO_INJECT_VARIABLES" auf "true" setzt) |
| PUSHWOOSH_ENABLED | **true** oder **false** | Auf *true* setzen, um Pushwoosh Push zu aktivieren (setze die Pushwoosh-Zugangsdaten in den Dateien AndroidManifest.xml und string.xml) |
| PUSHWOOSH_ENHANCE_WEBVIEW_URL | **true** oder **false** | Auf *true* setzen, wenn du die URL-Anfrage um ?pushwoosh_id=XYZ erweitern möchtest (setze die Pushwoosh-Zugangsdaten in den Dateien AndroidManifest.xml und string.xml) |
| SHOW_ADSENSE_AD | **true** oder **false** | Auf *true* setzen, um die Unterstützung für AdSense-Web-Anzeigen zu aktivieren (unabhängig von AdMob-Anzeigen) |
| SHOW_BANNER_AD | **true** oder **false** | Auf *true* setzen, wenn du AdMob-Banner-Anzeigen anzeigen möchtest (setze die AdMob-IDs in der Datei strings.xml) |
| SHOW_FULL_SCREEN_AD | **true** oder **false** | Auf *true* setzen, wenn du AdMob-Vollbild-Interstitial-Anzeigen nach X Website-Klicks anzeigen möchtest (setze die AdMob-IDs in der Datei strings.xml) |
| SHOW_APP_OPEN_AD | **true** oder **false** | Auf *true* setzen, um [AdMob-App-Open-Anzeigen](admob.md#appopenads) beim Kaltstart (über den Launcher-Splash) und bei der Rückkehr aus dem Hintergrund anzuzeigen (setze admob_app_open_id in der Datei strings.xml) |
| ASK_FOR_AD_CONSENT | **true** oder **false** | Auf *false* setzen, wenn du die Google-Einwilligungsverwaltung für AdMob deaktivieren möchtest (informiere dich vorab unter <https://support.google.com/admob/answer/13554116>) |
| SHOW_AD_AFTER_X | Wert (Website-Neuladungen) | Lege die Anzahl X der Website-Klicks für AdMob-Interstitial-Anzeigen fest (setze die AdMob-IDs in der Datei strings.xml) |
| INCREMENT_WITH_TAPS | **true** oder **false** | Auf *true* setzen, damit normale Taps auf den Bildschirm SHOW_AD_AFTER_X hochzählen |
| USE_FACEBOOK_ADS | **true** oder **false** | Auf *true* setzen, um Facebook Audience Network-Anzeigen anstelle von AdMob-Anzeigen zu verwenden (setze die Werbe-IDs in der Datei strings.xml) |
| ENABLE_REWARDED_ADS | **true** oder **false** | Auf *true* setzen, um AdMob-Rewarded-Anzeigen zu aktivieren. Muss auch bei manueller Aktivierung von Anzeigen auf *true* gesetzt sein. (Setze die Werbe-IDs in der Datei strings.xml.) |
| USE_REWARDED_ADS_WHERE_POSSIBLE | **true** oder **false** | Auf *true* setzen, um AdMob-Rewarded-Anzeigen anstelle von AdMob-Interstitial-Anzeigen anzuzeigen, z. B. nach X Taps. Belasse den Wert bei *false*, wenn deren Aktivierung über den Code deiner Website erfolgen soll. Beachte, dass dafür SHOW_FULL_SCREEN_AD ebenfalls auf *true* gesetzt sein muss, damit die Anzeigen überschrieben werden. |
| AD_TRIGGER_URLS | optional | Füge hier Trigger-Wörter für Seiten hinzu; das Vorhandensein in einer URL löst Interstitial-Anzeigen aus (z. B. "thanks.html", "welcome.html", "/thank-you/", "next-step.php") |
| REVENUECAT_API_KEY | optional | Dein RevenueCat-API-Schlüssel (registriere dich zunächst über [tinyurl.com/register-revenuecat](https://tinyurl.com/register-revenuecat) und folge dann [tinyurl.com/api-key-revenuecat](https://tinyurl.com/api-key-revenuecat), um ihn zu finden) |
| REVENUECAT_PROJECT_ID | optional | Deine RevenueCat-Projekt-ID (registriere dich zunächst über [tinyurl.com/register-revenuecat](https://tinyurl.com/register-revenuecat) und folge dann [tinyurl.com/project-id-revenuecat](https://tinyurl.com/project-id-revenuecat), um sie zu finden) |
| downloadableExtension | Liste | Füge die Dateiformate hinzu, die die Download-Funktion auslösen sollen (z. B. .pdf, .docx, ...) |
| AUTO_DOWNLOAD_FILES | **true** oder **false** | Auf *true* setzen, wenn du die Downloader-Funktion basierend auf Content-Disposition-HTTP-Headern aktivieren möchtest, unabhängig von den in der Variable downloadableExtension oben aufgeführten Dateiformaten |
| GOOGLE_LOGIN_HELPER_TRIGGERS | Liste | Definiere die URL-Präfixe, die während der Google-Anmeldung für deine Website geladen werden; sie dienen als Auslöser für den Helfer |
| FACEBOOK_LOGIN_HELPER_TRIGGERS | Liste | Definiere die URL-Präfixe, die während der Facebook-Anmeldung für deine Website geladen werden; sie dienen als Auslöser für den Helfer |
| HOME_URL_LOGOUT | Wert (URL) | Definiere die URL für den Logout, um Anmelde-Cookies zu löschen (optional) |
| MANUAL_COOKIE_SYNC | **true** oder **false** | Auf *true* setzen, um das Tool zur manuellen Cookie-Synchronisierung zu aktivieren. Zu verwenden, wenn Cookies in Abständen von *unter* 30 Sekunden synchronisiert werden müssen oder wenn etwas Cookie-bezogenes andernfalls nicht funktioniert. Weitere Cookie-Hinweise findest du [hier](https://www.webviewgold.com/support-center/knowledgebase/will-cookies-work-will-the-login-of-my-website-web-app-still-work/). |
| COOKIE_SYNC_TIME | Zahlenwert (Millisekunden) | Definiere, wie oft die Cookies in Millisekunden (ms) mit der App synchronisiert werden sollen |
| MANUAL_COOKIE_SYNC_TRIGGERS | Liste | Definiere die URL-Präfixe, für die du das Tool zur manuellen Cookie-Synchronisierung verwenden möchtest. Ist MANUAL_COOKIE_SYNC_TRIGGERS leer, wird jede Seite automatisch geprüft. Beispiel: {"https://example.com/login", "https://example.com/data"} |
| USE_CUSTOM_HEADERS | **true** oder **false** | Auf *true* setzen, um eigene HTTP-Header in jede URL-Navigation zu injizieren; definiere die Header-Namen & -Werte in der *customHeaders*-Map direkt unter dieser Option in Config.java |
| requireLocation | **true** oder **false** | Auf *false* setzen, wenn du KEINE Ortungsdienste/GPS-Koordinaten benötigst; vergiss nicht, auch entsprechende Einträge in *AndroidManifest.xml* zu entfernen, wenn du die Berechtigung vollständig aus der App entfernen möchtest; siehe auch [Nutzung der Hintergrund-(!)Ortung](geolocation.md) |
| requireBackgroundLocation | **true** oder **false** | Auf *false* setzen, wenn Hintergrund-Ortungsdienste erforderlich sind. Wenn diese Option auf *false* gesetzt ist, stelle sicher, dass du auch die Blöcke `android.permission.FOREGROUND_SERVICE_LOCATION` und `.GPSService` in `AndroidManifest.xml` auskommentierst (suche darin nach diesen Begriffen). Diese Einstellung ist nur wirksam, wenn `requireLocation` ebenfalls auf *true* gesetzt ist. |
| requireStorage | **true** oder **false** | Auf *false* setzen, wenn du KEINE APIs für Downloads oder Uploads benötigst; vergiss nicht, auch entsprechende Einträge in *AndroidManifest.xml* zu entfernen, wenn du die Berechtigung vollständig aus der App entfernen möchtest |
| requireCamera | **true** oder **false** | Auf *false* setzen, wenn du KEINE APIs für Kamerabilder / Kameravideos benötigst; vergiss nicht, auch entsprechende Einträge in *AndroidManifest.xml* zu entfernen, wenn du die Berechtigung vollständig aus der App entfernen möchtest |
| requireRecordAudio | **true** oder **false** | Auf *false* setzen, wenn du KEINE APIs zur Audioaufnahme benötigst; vergiss nicht, auch entsprechende Einträge in *AndroidManifest.xml* zu entfernen, wenn du die Berechtigung vollständig aus der App entfernen möchtest |
| filePickerMode | Zahlenwert | Optionen für den Datei-Upload: (0) Kamera und Galerie; (1) nur Kamera; (2) nur Galerie. |

Öffne die Datei **strings.xml**, um den App-Namen und Textbausteine zu bearbeiten:\
![Datei string.xml zum Bearbeiten der Textbausteine](../../assets/android/img/strings.webp)

**Mehrsprachige Apps:** Um Übersetzungen zu bearbeiten – einschließlich der standardmäßig enthaltenen deutschen und spanischen – oder neue, zusätzliche Übersetzungen für diese Strings zu erstellen, klicke in Android Studio mit der rechten Maustaste auf den Ordner "strings" und wähle "Open Translations Editor":\
![Mehrsprachige Unterstützung für deine WebView-App auf Android](../../assets/android/img/translations.webp)

Öffne die Datei **dimens.xml**, um die Textformatierung anzupassen:\
![Verwende dimens.xml, um Objekte und Texte in der Größe anzupassen](../../assets/android/img/screenshot_Dimens.webp)

---

## Weiterlesen

- ← Vorherige: [Web-App einrichten](setup-website.md)
- Weiter →: [App-Icon](app-icon.md)
- Dieselbe Funktion auf anderen Plattformen: [iOS – WebViewGold konfigurieren](../ios/setup.md) · [macOS – WebViewGold einrichten](../macos/setup.md)
- Sprachen: [🇺🇸 English](../../android/setup.md) · **🇩🇪 Deutsch** · [🇫🇷 Français](../../fr/android/setup.md) · [🇪🇸 Español](../../es/android/setup.md) · [🇨🇳 中文](../../zh/android/setup.md)

> [!TIP]
> **Zu wenig Zeit? Wir richten deine App für dich ein.** Unser Team konfiguriert, erstellt & reicht deine WebViewGold-App ein – schlüsselfertig, mit schneller Bearbeitung, Made in Germany. [App einrichten lassen →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_android_doc_online)
>
> **Im Browser erstellen:** Kein Mac, keine IDE: Der **WebViewGold Cloud Builder** konfiguriert, erstellt & lädt deine App online hoch. [Cloud Builder entdecken →](https://www.webviewgold.com/cloud-builder?ref=android_docs)
