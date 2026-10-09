---
title: "URL-Handling-API – WebViewGold für iOS Dokumentation"
description: "Lege fest, welche Links in deiner App, in einem In-App-Browser-Tab oder in Safari geöffnet werden – volle URL-Handling-Kontrolle für iOS."
lang: "de"
product: "WebViewGold für iOS"
platform: "iOS"
category: "APIs & Funktionen"
slug: "url-handling"
canonical_url: "https://www.webviewgold.com/de/docs/iOS/url-handling/"
keywords:
  - "URL-Handling-API"
  - "WebViewGold für iOS"
  - "Website in App umwandeln"
  - "WebView-App-Dokumentation"
  - "iOS WebView SDK"
  - "PWA zu App"
  - "HTML zu App"
  - "JavaScript-Bridge"
last_updated: "2026-10-09"
---

# URL-Handling-API – WebViewGold für iOS

> **Zusammenfassung:** Lege fest, welche Links in deiner App, in einem In-App-Browser-Tab oder in Safari geöffnet werden – volle URL-Handling-Kontrolle für iOS.

[Dokumentation](../README.md) › [WebViewGold für iOS](README.md) › URL-Handling-API

**Plattform:** iOS · **Kategorie:** APIs & Funktionen · **Online-Version:** [www.webviewgold.com/de/docs/iOS/url-handling/](https://www.webviewgold.com/de/docs/iOS/url-handling/)

---

Zur Verbesserung der Nutzererfahrung ist es oft sinnvoll, das Verhalten deiner App bei verschiedenen Arten von Weblinks anzupassen. Beispielsweise können Buttons für soziale Netzwerke so konfiguriert werden, dass sie im Systembrowser bzw. in der entsprechenden App geöffnet werden, statt in deiner App. WebViewGold bietet flexible Einstellungen zur Anpassung des URL-Handlings für deine WebView-basierte iOS-App.

## Arten von Links

1. **Externe Links:** Links, die zu einer **anderen Domain** als der Hauptdomain deiner App führen.
   - **Beispiel:** Wenn die Domain deiner App **mydomain.com** ist, wäre ein externer Link **google.com**.
2. **Interne Links:** Links, die innerhalb **derselben Domain** deiner App bleiben.
   - **Beispiel:** Wenn die Domain deiner App **mydomain.com** ist, wäre ein interner Link **mydomain.com/purchase**.
3. **Spezielle Links:** Links, die spezielle Attribute enthalten, wie z. B. **target="_blank"**.

## Um die URL-Handling-API zu konfigurieren, öffne Config.swift

1. Um das Standardverhalten für **externe Links** festzulegen:
   - Setze `externalLinkHandlingOptions` auf `0`, um externe Links standardmäßig in der App zu öffnen, oder auf `2`, um sie IMMER in einem anderen Browser (Safari) zu öffnen.

2. Um das Standardverhalten für **spezielle Links** (z. B. **target="_blank"**) festzulegen:
   - Setze `specialLinkHandlingOptions` auf `0`, um spezielle Links in der App zu öffnen, auf `1`, um sie in einem neuen Tab (einem zusätzlichen In-App-Browser) zu öffnen, oder auf `2`, um sie in einem anderen Browser (Safari) zu öffnen.

3. Um Domains festzulegen, die ***immer* in Safari** geöffnet werden sollen (unabhängig von der Einstellung `externalLinkHandlingOptions`):
   - Füge die gewünschten Domains zur Liste `safariwhitelist` hinzu.
   - Füge einen weiteren Host wie folgt ein: ["alwaysopeninsafari.com", "google.com", "m.facebook.com"].
   - Bitte gib den Host genau so an, wie du ihn verlinkst (mit oder ohne www, aber immer ohne http/https).

4. Um Domains festzulegen, die ***nie* in Safari** geöffnet werden sollen (unabhängig von der Einstellung `externalLinkHandlingOptions`):
   - Füge die gewünschten Domains zur Liste `safariblacklist` hinzu.
   - Füge einen weiteren Host wie folgt ein: ["alwaysopeninsafari.com", "google.com", "m.facebook.com"].
   - Bitte gib den Host genau so an, wie du ihn verlinkst (mit oder ohne www, aber immer ohne http/https).

5. Um Domains festzulegen, die ***immer*** oder ***nie* in einem In-App-Tab** geöffnet werden sollen (unabhängig von der Einstellung `externalLinkHandlingOptions`):
   - Füge die gewünschten Domains zur Liste `alwaysOpenInInAppTab` bzw. `neverOpenInInAppTab` hinzu.

## Links in einem Tab/zusätzlichen In-App-Browser öffnen

Manche Links, etwa eine Seite mit Allgemeinen Geschäftsbedingungen, sind nicht wichtig genug, um im externen Systembrowser geöffnet zu werden, aber zu speziell für den Haupt-WebView deiner App. WebViewGold bietet eine kreative Lösung für die Behandlung solcher Links: **einen In-App-Browser-Tab**, der sich über dem Haupt-WebView öffnet und eine hybride App- und Browser-Erfahrung bietet. So sieht das Ganze aus:

![Einen Link in einem zusätzlichen In-App-Browser/Tab SFSafariViewController öffnen](../../assets/ios/img/tabs.webp)

### Hauptmerkmale des In-App-Browser-Tabs

- Der In-App-Browser-Tab enthält eine **Adressleiste** und **Navigationsschaltflächen** und bietet damit eine browserähnlichere Erfahrung als der primäre WebView.
- Ideal für Inhalte, die eine einfache Navigation erfordern, wie z. B. Tutorials, Wissensdatenbanken oder Seiten mit spezifischen Informationen.

### So verwendest du den In-App-Browser-Tab in deiner WebView-basierten iOS-App

Um einen Link im In-App-Browser-Tab zu öffnen, setze `specialLinkHandlingOptions` auf `1` und formatiere die URL in deinem HTML wie folgt:

```html
<a href="https://www.example.com" target="_blank">Open link in an in-app tab</a>
```

Einfach ausgedrückt: Ein **spezieller Link** ist ein Link, an dem das Attribut "_blank" als Target angehängt ist. In einem normalen Browser würde ein solcher Link in einem neuen Tab geöffnet. In der WebViewGold-App kannst du ihn stattdessen im In-App-Tab öffnen lassen.

Bitte beachte: Wenn der von dir verwendete Link extern ist (also eine andere Domain als deine Website hat, z. B. "www.google.com"), stelle sicher, dass `externalLinkHandlingOptions` auf `0` gesetzt ist, da das Öffnen aller externen Links in einem anderen Browser den speziell-externen Link sonst überschreibt und stattdessen in der Safari-App öffnet.

**Testen des Link-Verhaltens:**\
Um zu sehen, wie deine App verschiedene Arten von Links verarbeitet, verwende beim Testen die folgende URL als WebView-URL:\
Testlink: <https://www.webviewgold.com/demo/testlinks.php>\
**Hinweis:** Du kannst dieselbe Domain auch in deinem Desktop-Browser öffnen, um den Quellcode einzusehen und das Format für deine Links zu übernehmen.

---

## Weiterlesen

- ← Vorherige: [Pull-to-Refresh-API](pull-to-refresh.md)
- Weiter →: [Social Login Helper](social-login.md)
- Dieselbe Funktion auf anderen Plattformen: [Android – URL-Handling-API](../android/url-handling.md)
- Sprachen: [🇺🇸 English](../../ios/url-handling.md) · **🇩🇪 Deutsch** · [🇫🇷 Français](../../fr/ios/url-handling.md) · [🇪🇸 Español](../../es/ios/url-handling.md) · [🇨🇳 中文](../../zh/ios/url-handling.md)

> [!TIP]
> **Zu wenig Zeit? Wir richten deine App für dich ein.** Unser Team konfiguriert, erstellt & reicht deine WebViewGold-App ein – schlüsselfertig, mit schneller Bearbeitung, Made in Germany. [App einrichten lassen →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **Im Browser erstellen:** Kein Mac, keine IDE: Der **WebViewGold Cloud Builder** konfiguriert, erstellt & lädt deine App online hoch. [Cloud Builder entdecken →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
