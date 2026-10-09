---
title: "Pull-to-Refresh-API – WebViewGold für iOS Dokumentation"
description: "Aktiviere die native Pull-to-Refresh-Geste in deiner iOS-WebView-App, passe ihre Farben an und schalte sie dynamisch aus deiner Web-App um."
lang: "de"
product: "WebViewGold für iOS"
platform: "iOS"
category: "APIs & Funktionen"
slug: "pull-to-refresh"
canonical_url: "https://www.webviewgold.com/de/docs/iOS/pull-to-refresh/"
keywords:
  - "Pull-to-Refresh-API"
  - "WebViewGold für iOS"
  - "Website in App umwandeln"
  - "WebView-App-Dokumentation"
  - "iOS WebView SDK"
  - "PWA zu App"
  - "HTML zu App"
  - "JavaScript-Bridge"
last_updated: "2026-10-09"
---

# Pull-to-Refresh-API – WebViewGold für iOS

> **Zusammenfassung:** Aktiviere die native Pull-to-Refresh-Geste in deiner iOS-WebView-App, passe ihre Farben an und schalte sie dynamisch aus deiner Web-App um.

[Dokumentation](../README.md) › [WebViewGold für iOS](README.md) › Pull-to-Refresh-API

**Plattform:** iOS · **Kategorie:** APIs & Funktionen · **Online-Version:** [www.webviewgold.com/de/docs/iOS/pull-to-refresh/](https://www.webviewgold.com/de/docs/iOS/pull-to-refresh/)

---

Die **Pull-to-Refresh-API** bringt die native iOS-Geste zum Aktualisieren in deine WebView-App: Nutzer ziehen die Seite nach unten, um die aktuelle URL neu zu laden – genau wie in nativen Apps wie Mail oder Safari.

## So aktivierst du das Feature

Öffne **Config.swift** und setze:

```swift
var pulltorefresh = true
var preventoverscroll = false
```

- `pulltorefresh` aktiviert das native Refresh-Element.
- `preventoverscroll` muss auf `false` stehen – die Geste benötigt die Bounce-/Overscroll-Animation der WebView.

## Farben anpassen

Den Lade-Spinner und seinen Hintergrund kannst du in **Config.swift** getrennt für den Light und Dark Mode gestalten:

```swift
var pulltorefresh_loadingsigncolour_lightmode = #colorLiteral(...)
var pulltorefresh_backgroundcolour_lightmode = #colorLiteral(...)
var pulltorefresh_loadingsigncolour_darkmode = #colorLiteral(...)
var pulltorefresh_backgroundcolour_darkmode = #colorLiteral(...)
```

Tipp: Klicke in Xcode auf das Farbfeld neben dem jeweiligen `#colorLiteral`, um eine Farbe visuell auszuwählen. Die Dark-Mode-Varianten erfordern iOS 13 oder höher.

## Dynamisch aus deiner Web-App umschalten

Du kannst Pull-to-Refresh zur Laufzeit ein- oder ausschalten – zum Beispiel, um es auf Seiten mit eigenen Wisch-Gesten (Karten, Slider, Spiele) zu deaktivieren:

```html
<a href="enablepulltorefresh://">Pull-to-Refresh aktivieren</a>
<a href="disablepulltorefresh://">Pull-to-Refresh deaktivieren</a>
```

Oder per JavaScript:

```javascript
window.location.href = "disablepulltorefresh://";
```

Beide Befehle werden auch innerhalb eines [MultiAPICall](multi-api-call.md)-Aufrufs unterstützt.

## Gut zu wissen

- Das Refresh-Element lädt die URL neu, die aktuell in der WebView angezeigt wird.
- Wenn du über die [Dynamic-UI-API](dynamic-ui.md) die Farbe der unteren Leiste zur Laufzeit änderst, werden die Pull-to-Refresh-Farben automatisch passend angepasst.

---

## Weiterlesen

- ← Vorherige: [Ladeanzeige-API](loading-sign.md)
- Weiter →: [URL-Handling-API](url-handling.md)
- Sprachen: [🇺🇸 English](../../ios/pull-to-refresh.md) · **🇩🇪 Deutsch** · [🇫🇷 Français](../../fr/ios/pull-to-refresh.md) · [🇪🇸 Español](../../es/ios/pull-to-refresh.md) · [🇨🇳 中文](../../zh/ios/pull-to-refresh.md)

> [!TIP]
> **Zu wenig Zeit? Wir richten deine App für dich ein.** Unser Team konfiguriert, erstellt & reicht deine WebViewGold-App ein – schlüsselfertig, mit schneller Bearbeitung, Made in Germany. [App einrichten lassen →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **Im Browser erstellen:** Kein Mac, keine IDE: Der **WebViewGold Cloud Builder** konfiguriert, erstellt & lädt deine App online hoch. [Cloud Builder entdecken →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
