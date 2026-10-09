---
title: "Social-Media-Login-Helper (Google, Facebook & Apple) – WebViewGold für iOS Dokumentation"
description: "Bringe Google-, Facebook- und Apple-OAuth-Logins mit den integrierten Social-Login-Helfern zuverlässig in deiner iOS-WebView-App zum Laufen."
lang: "de"
product: "WebViewGold für iOS"
platform: "iOS"
category: "APIs & Funktionen"
slug: "social-login"
canonical_url: "https://www.webviewgold.com/de/docs/iOS/social-login/"
keywords:
  - "Social Login Helper"
  - "WebViewGold für iOS"
  - "Website in App umwandeln"
  - "WebView-App-Dokumentation"
  - "iOS WebView SDK"
  - "PWA zu App"
  - "HTML zu App"
  - "JavaScript-Bridge"
last_updated: "2026-10-09"
---

# Social-Media-Login-Helper (Google, Facebook & Apple) – WebViewGold für iOS

> **Zusammenfassung:** Bringe Google-, Facebook- und Apple-OAuth-Logins mit den integrierten Social-Login-Helfern zuverlässig in deiner iOS-WebView-App zum Laufen.

[Dokumentation](../README.md) › [WebViewGold für iOS](README.md) › Social Login Helper

**Plattform:** iOS · **Kategorie:** APIs & Funktionen · **Online-Version:** [www.webviewgold.com/de/docs/iOS/social-login/](https://www.webviewgold.com/de/docs/iOS/social-login/)

---

Google, Facebook und andere OAuth-Anbieter blockieren Logins aus eingebetteten WebViews (z. B. Googles Fehler *„disallowed_useragent“*). Der in WebViewGold integrierte **Social Login Helper** sorgt dafür, dass diese Logins zuverlässig in deiner iOS-App funktionieren – ohne dass du den Login-Ablauf deiner Website ändern musst.

## So funktioniert es

Du definierst URL-Präfixe, die während des Login-Ablaufs deiner Web-App aufgerufen werden. Sobald eine dieser Trigger-URLs lädt, öffnet WebViewGold den Login in einem eigenen Popup-Login-Fenster mit einem angepassten User Agent, den der OAuth-Anbieter akzeptiert. Nach erfolgreichem Login kehrt der Ablauf automatisch zu deiner Web-App zurück. „Sign in with Apple“ (`appleid.apple.com`) wird automatisch erkannt und behandelt – ganz ohne Konfiguration.

## Konfiguration

Öffne **Config.swift** und definiere die Trigger-URL-Präfixe für deinen Login-Ablauf:

```javascript
var google_login_helper_triggers: [String] = ["https://accounts.google.com", "https://accounts.youtube.com"]
var facebook_login_helper_triggers: [String] = ["https://m.facebook.com", "https://www.facebook.com"]
```

- `google_login_helper_triggers` – URL-Präfixe, die während eines Google-Logins auf deiner Website geladen werden.
- `facebook_login_helper_triggers` – URL-Präfixe, die während eines Facebook-Logins auf deiner Website geladen werden.

Um die richtigen Trigger-URLs zu finden, starte den Login-Ablauf deiner Website in einem Desktop-Browser und notiere, über welche URLs die OAuth-Weiterleitung läuft.

## Auth-URL im externen Browser öffnen

Alternativ kannst du eine Login-URL explizit an den System-Browser übergeben (die Session lebt dann im Browser, nicht in der App):

```javascript
window.location.href = "googlelogin://" + encodeURIComponent("https://accounts.google.com/o/oauth2/v2/auth?...");
```

WebViewGold dekodiert die URL nach dem Präfix `googlelogin://` und öffnet sie extern.

## Wann du den Helper nutzen solltest

Probiere zuerst die einfacheren Optionen – oft lösen sie Login-Probleme bereits:

- Öffne die Login-Domain über die [URL-Handling-API](url-handling.md) in einem In-App-Browser-Tab oder im externen Browser (z. B. `specialLinkHandlingOptions`, `safariblacklist`).
- Setze einen [Custom User Agent](setup.md) (`useragent_iphone` / `useragent_ipad`).

Wenn der Login in der App weiterhin fehlschlägt, sind die Social-Login-Helper-Trigger die empfohlene Lösung.

---

## Weiterlesen

- ← Vorherige: [URL-Handling-API](url-handling.md)
- Weiter →: [Reconnect-API](reconnect.md)
- Sprachen: [🇺🇸 English](../../ios/social-login.md) · **🇩🇪 Deutsch** · [🇫🇷 Français](../../fr/ios/social-login.md) · [🇪🇸 Español](../../es/ios/social-login.md) · [🇨🇳 中文](../../zh/ios/social-login.md)

> [!TIP]
> **Zu wenig Zeit? Wir richten deine App für dich ein.** Unser Team konfiguriert, erstellt & reicht deine WebViewGold-App ein – schlüsselfertig, mit schneller Bearbeitung, Made in Germany. [App einrichten lassen →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **Im Browser erstellen:** Kein Mac, keine IDE: Der **WebViewGold Cloud Builder** konfiguriert, erstellt & lädt deine App online hoch. [Cloud Builder entdecken →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
