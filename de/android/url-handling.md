---
title: "URL-Handling-API – WebViewGold für Android Dokumentation"
description: "Lege fest, welche Links in deiner Android-App, in Chrome Custom Tabs oder im externen Browser geöffnet werden."
lang: "de"
product: "WebViewGold für Android"
platform: "Android"
category: "APIs & Funktionen"
slug: "url-handling"
canonical_url: "https://www.webviewgold.com/de/docs/android/url-handling/"
keywords:
  - "URL-Handling-API"
  - "WebViewGold für Android"
  - "Website in App umwandeln"
  - "WebView-App-Dokumentation"
  - "Android WebView SDK"
  - "PWA zu App"
  - "HTML zu App"
  - "JavaScript-Bridge"
last_updated: "2026-10-09"
---

# URL-Handling-API – WebViewGold für Android

> **Zusammenfassung:** Lege fest, welche Links in deiner Android-App, in Chrome Custom Tabs oder im externen Browser geöffnet werden.

[Dokumentation](../README.md) › [WebViewGold für Android](README.md) › URL-Handling-API

**Plattform:** Android · **Kategorie:** APIs & Funktionen · **Online-Version:** [www.webviewgold.com/de/docs/android/url-handling/](https://www.webviewgold.com/de/docs/android/url-handling/)

---

Zur Verbesserung der Nutzererfahrung ist es oft sinnvoll, das Verhalten deiner App bei verschiedenen Arten von Weblinks anzupassen. Beispielsweise können Buttons für soziale Netzwerke so konfiguriert werden, dass sie im Systembrowser bzw. in der entsprechenden App geöffnet werden, statt in deiner App. WebViewGold bietet flexible Einstellungen zur Anpassung des URL-Handlings für deine WebView-basierte Android-App:

## Arten von Links

1. **Externe Links:** Links, die zu einer **anderen Domain** als der Hauptdomain deiner App führen.
   - **Beispiel:** Wenn die Domain deiner App **mydomain.com** ist, wäre ein externer Link **google.com**.
2. **Interne Links:** Links, die innerhalb **derselben Domain** deiner App bleiben.
   - **Beispiel:** Wenn die Domain deiner App **mydomain.com** ist, wäre ein interner Link **mydomain.com/purchase**.
3. **Spezielle Links:** Links, die spezielle Attribute enthalten, wie z. B. **target="_blank"** oder Links, die mit **#** enden.

## Optionen zur Link-Behandlung

Du kannst das Link-Verhalten konfigurieren, indem du die Einstellungen in der Datei **Config.java** wie unten gezeigt anpasst.

## Behandlung externer Links

- **Standardoption (0):** Um externe Links im Haupt-WebView zu öffnen (wie interne Links), setze `EXTERNAL_LINK_HANDLING_OPTIONS` auf `0`.
- **Option 1:** Um externe Links in einem neuen In-App-Tab zu öffnen, setze `EXTERNAL_LINK_HANDLING_OPTIONS` auf `1`.
- **Option 2:** Um externe Links im Standardsystembrowser des Geräts (z. B. Chrome, Safari) zu öffnen, setze `EXTERNAL_LINK_HANDLING_OPTIONS` auf `2`.

## Behandlung spezieller Links

- **Option 0:** Um spezielle Links im Haupt-WebView der App zu öffnen, setze `SPECIAL_LINK_HANDLING_OPTIONS` auf `0`.
- **Option 1:** Um spezielle Links in einem neuen In-App-Tab zu öffnen, setze `SPECIAL_LINK_HANDLING_OPTIONS` auf `1`.
- **Option 2:** Um spezielle Links im Standardsystembrowser des Geräts (z. B. Chrome, Safari) zu öffnen, setze `SPECIAL_LINK_HANDLING_OPTIONS` auf `2`.

Hinweis: Diese Einstellung überschreibt `EXTERNAL_LINK_HANDLING_OPTIONS` bei Links, die sowohl extern als auch speziell sind.

## Anpassung des Linkzugriffs: Whitelist und Blacklist

Um Ausnahmen für bestimmte Websites oder Seiten festzulegen, öffne **Config.java** und füge die Domain einem der folgenden Arrays hinzu:

- **BROWSER_WHITELIST:** Listet bestimmte Domains auf, die im WebView der App geöffnet werden.
- **BROWSER_BLACKLIST:** Listet bestimmte Domains auf, die im externen Browser geöffnet werden.

Ausführliche Hinweise zur Link-Konfiguration für deine Android-App findest du im folgenden Video-Tutorial:

[![Video ansehen: URL-Handling-API](https://img.youtube.com/vi/lq7jgaB6TxY/hqdefault.jpg)](https://www.youtube.com/watch?v=lq7jgaB6TxY)

---

## URL-Handling – In-App-Browser für bestimmte Links verwenden

Manche Links, etwa eine Seite mit Allgemeinen Geschäftsbedingungen, sind nicht wichtig genug, um im externen Systembrowser geöffnet zu werden, aber zu speziell für den Haupt-WebView deiner App. WebViewGold bietet eine kreative Lösung für die Behandlung solcher Links: **einen In-App-Browser-Tab**, der sich über dem Haupt-WebView öffnet und eine hybride App- und Browser-Erfahrung bietet. So sieht das Ganze aus:\
![Einen Link in einem zusätzlichen In-App-Browser/Tab in Android-WebView-Apps öffnen](../../assets/android/img/tabs.webp)

### Hauptmerkmale des In-App-Browser-Tabs

- Der In-App-Browser-Tab enthält eine **Adressleiste** und **Navigationsschaltflächen** und bietet damit eine browserähnlichere Erfahrung als der primäre WebView.
- Ideal für Inhalte, die eine einfache Navigation erfordern, wie z. B. Tutorials, Wissensdatenbanken oder Seiten mit spezifischen Informationen.

### So verwendest du den In-App-Browser-Tab in deiner WebView-basierten Android-App

Um einen Link im In-App-Browser-Tab zu öffnen, formatiere die URL in deinem HTML wie folgt:

```html
<a href='#' onClick="top.location.href='https://www.example.com';">Open Example Page</a>
```

**Beispiel:** Um Google zu öffnen, verwende:

```html
<a href='#' onClick="top.location.href='https://www.google.com';">Open Google</a>
```

**Testen des Link-Verhaltens:**\
Um zu sehen, wie deine App verschiedene Arten von Links verarbeitet, verwende beim Testen die folgende URL als WebView-URL:\
Testlink: <https://www.webviewgold.com/demo/testlinks.php>\
**Hinweis:** Du kannst dieselbe Domain auch in deinem Desktop-Browser öffnen, um den Quellcode einzusehen und das Format für deine Links zu übernehmen.

---

## Einen bestimmten Link gezielt im In-App-Tab oder Browser öffnen (`newtab:`-Präfix)

Manchmal soll ein **einzelner, bestimmter Link** im In-App-Browser-Tab (oder im externen Browser) geöffnet werden – unabhängig von deiner globalen Link-Handling-Konfiguration. Stelle der URL einfach das Präfix `newtab:` voran:

```html
<a href="newtab:https://www.example.com">Beispielseite öffnen</a>
```

Der so markierte Link wird dann wie ein Special Link behandelt: Mit `SPECIAL_LINK_HANDLING_OPTIONS` auf `1` öffnet er sich im In-App-Browser-Tab, mit `2` im externen System-Browser. Dafür muss `SPECIAL_LINK_HANDLING_OPTIONS` in **Config.java** auf einen anderen Wert als `0` gesetzt sein.

## Eine Authentifizierungs-URL in einem Chrome Custom Tab öffnen (`googlelogin://`)

Einige Login-Anbieter (insbesondere **Google Sign-In**) blockieren die Authentifizierung innerhalb einfacher WebViews. Wenn das [Social-Media-Login-Helper-Tool](setup.md) nicht zu deinem Flow passt, kannst du die Authentifizierungs-URL stattdessen in einem sicheren **Chrome Custom Tab** öffnen, indem du ihr das Präfix `googlelogin://` voranstellst:

```javascript
window.location.href = "googlelogin://" + encodeURIComponent("https://accounts.google.com/o/oauth2/v2/auth?...");
```

Die URL nach dem Präfix wird dekodiert und in einem In-App-Chrome-Custom-Tab geöffnet, in dem der Login abgeschlossen werden kann. Leite den Nutzer anschließend zurück in deine Web-App (z. B. über deine OAuth-Redirect-URL).

---

## Weiterlesen

- ← Vorherige: [Navigation Drawer & Footer](navigation-drawer.md)
- Weiter →: [Eigene CSS- & JS-API](custom-css-js.md)
- Dieselbe Funktion auf anderen Plattformen: [iOS – URL-Handling-API](../ios/url-handling.md)
- Sprachen: [🇺🇸 English](../../android/url-handling.md) · **🇩🇪 Deutsch** · [🇫🇷 Français](../../fr/android/url-handling.md) · [🇪🇸 Español](../../es/android/url-handling.md) · [🇨🇳 中文](../../zh/android/url-handling.md)

> [!TIP]
> **Zu wenig Zeit? Wir richten deine App für dich ein.** Unser Team konfiguriert, erstellt & reicht deine WebViewGold-App ein – schlüsselfertig, mit schneller Bearbeitung, Made in Germany. [App einrichten lassen →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_android_doc_online)
>
> **Im Browser erstellen:** Kein Mac, keine IDE: Der **WebViewGold Cloud Builder** konfiguriert, erstellt & lädt deine App online hoch. [Cloud Builder entdecken →](https://www.webviewgold.com/cloud-builder?ref=android_docs)
