---
title: "Universal Links-API – WebViewGold für iOS Dokumentation"
description: "Öffne Links zu deiner Domain direkt in deiner iOS-App mit Apple Universal Links – Einrichtung, AASA-Datei und Fehlerbehebung."
lang: "de"
product: "WebViewGold für iOS"
platform: "iOS"
category: "APIs & Funktionen"
slug: "universal-links"
canonical_url: "https://www.webviewgold.com/de/docs/iOS/universal-links/"
keywords:
  - "Universal Links-API"
  - "WebViewGold für iOS"
  - "Website in App umwandeln"
  - "WebView-App-Dokumentation"
  - "iOS WebView SDK"
  - "PWA zu App"
  - "HTML zu App"
  - "JavaScript-Bridge"
last_updated: "2026-10-09"
---

# Universal Links-API – WebViewGold für iOS

> **Zusammenfassung:** Öffne Links zu deiner Domain direkt in deiner iOS-App mit Apple Universal Links – Einrichtung, AASA-Datei und Fehlerbehebung.

[Dokumentation](../README.md) › [WebViewGold für iOS](README.md) › Universal Links-API

**Plattform:** iOS · **Kategorie:** APIs & Funktionen · **Online-Version:** [www.webviewgold.com/de/docs/iOS/universal-links/](https://www.webviewgold.com/de/docs/iOS/universal-links/)

---

Die **Universal-Links-API** vereinfacht das Verlinken auf Inhalte innerhalb deiner App und sorgt für ein nahtloseres, natives Nutzererlebnis. Mit WebViewGold kannst du deine Domain so konfigurieren, dass Links aus Apps wie **Mail, Safari und anderen** automatisch in deiner WebViewGold-basierten App geöffnet werden – ganz ohne zusätzliche Aufforderungen.

**Hinweis:** Damit diese Funktion funktioniert, muss die App zuerst auf dem Gerät des Nutzers installiert sein.

**Alternativ** kannst du unsere [**Deep-Linking-API**](deep-linking.md) verwenden. Sie funktioniert ähnlich, nutzt jedoch eine andere Syntax. Es ist zu beachten, dass die Syntax der [**Universal-Links-API**](universal-links.md) verbreiteter ist als die der Deep-Linking-API. Für die meisten Apps ist es sinnvoll, sich für eine der beiden Varianten zu entscheiden, nicht für beide.

Um **Universal Links** in deiner iOS-App einzurichten, folge bitte den nachstehenden Schritten:

1. **Einrichtung im Apple Developer Center:**

1. Melde dich mit deinem Konto im [Apple Developer Center](https://developer.apple.com/account/) an.
2. Klicke auf „Certificates, Identifiers & Profiles“.
3. Wähle unter „Identifiers“ die Option „App IDs“ und anschließend die ID deiner App aus der Liste aus.
4. Aktiviere im Bereich „App Services“ die Option „Associated Domains“ und speichere deine Änderungen.

2. **Einrichtung in Xcode:**

1. Öffne dein App-Projekt in Xcode.
2. Wähle das Target aus (in den meisten Fällen „WebViewGold“). Navigiere im Tab „Signing & Capabilities“ zum Abschnitt „Associated Domains“. Klicke auf „+“, um eine Domain hinzuzufügen. Deiner Domain sollte „applinks:“ vorangestellt sein, zum Beispiel: `applinks:example.org` & `applinks:www.example.org`:\
   ![Associated Domains in Xcode](../../assets/ios/img/associateddomains.webp)
3. Setze in Config.swift **ShowExternalLink** auf **true**.
4. Achte auf Subdomains. Es gibt einen Unterschied zwischen „www.\*“ und Nicht-„www“-Domains (ziehe in Betracht, beide hinzuzufügen). Stelle sicher, dass du das richtige Provisioning Profile mit der Capability „Associated Domains“ besitzt. Andernfalls sollte Xcode dich zur Korrektur auffordern.

3. **Server-Einrichtung:**

1. Auf deinem Website-Server musst du eine Apple App Site Association (AASA)-Datei entweder auf der Root-Ebene deines Servers oder unter dem Präfix `/.well-known/` hosten. Zum Beispiel: `https://example.org/.well-known/apple-app-site-association`
2. Die AASA-Datei sollte Details zur App und zu den zugeordneten Domains enthalten. Beziehe dich für die genaue Struktur auf die [offizielle Dokumentation](https://developer.apple.com/documentation/safariservices/supporting_associated_domains). Stelle sicher, dass die apple-app-site-association-Datei auf einem Server gehostet wird, der HTTPS unterstützt, nicht nur HTTP.

**Fertig! :-)** Das Testen im Simulator ist nicht so effektiv wie auf einem echten Gerät. Für die besten Ergebnisse verwende ein echtes iPhone oder iPad.

---

## Weiterlesen

- ← Vorherige: [Eigenes CSS & JS API](custom-css-js.md)
- Weiter →: [Deep-Linking-API](deep-linking.md)
- Dieselbe Funktion auf anderen Plattformen: [Android – App Links / Deep Linking](../android/app-links.md)
- Sprachen: [🇺🇸 English](../../ios/universal-links.md) · **🇩🇪 Deutsch** · [🇫🇷 Français](../../fr/ios/universal-links.md) · [🇪🇸 Español](../../es/ios/universal-links.md) · [🇨🇳 中文](../../zh/ios/universal-links.md)

> [!TIP]
> **Zu wenig Zeit? Wir richten deine App für dich ein.** Unser Team konfiguriert, erstellt & reicht deine WebViewGold-App ein – schlüsselfertig, mit schneller Bearbeitung, Made in Germany. [App einrichten lassen →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **Im Browser erstellen:** Kein Mac, keine IDE: Der **WebViewGold Cloud Builder** konfiguriert, erstellt & lädt deine App online hoch. [Cloud Builder entdecken →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
