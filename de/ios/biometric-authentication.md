---
title: "Biometrische Authentifizierungs-API (Face ID / Touch ID) – WebViewGold für iOS Dokumentation"
description: "Schütze deine iOS-App mit Face ID oder Touch ID und verifiziere Nutzer biometrisch aus deiner Web-App."
lang: "de"
product: "WebViewGold für iOS"
platform: "iOS"
category: "APIs & Funktionen"
slug: "biometric-authentication"
canonical_url: "https://www.webviewgold.com/de/docs/iOS/biometric-authentication/"
keywords:
  - "Biometrische-Auth-API"
  - "WebViewGold für iOS"
  - "Website in App umwandeln"
  - "WebView-App-Dokumentation"
  - "iOS WebView SDK"
  - "PWA zu App"
  - "HTML zu App"
  - "JavaScript-Bridge"
last_updated: "2026-10-09"
---

# Biometrische Authentifizierungs-API (Face ID / Touch ID) – WebViewGold für iOS

> **Zusammenfassung:** Schütze deine iOS-App mit Face ID oder Touch ID und verifiziere Nutzer biometrisch aus deiner Web-App.

[Dokumentation](../README.md) › [WebViewGold für iOS](README.md) › Biometrische-Auth-API

**Plattform:** iOS · **Kategorie:** APIs & Funktionen · **Online-Version:** [www.webviewgold.com/de/docs/iOS/biometric-authentication/](https://www.webviewgold.com/de/docs/iOS/biometric-authentication/)

---

**Dies ist eine eigenständige, leistungsfähigere, aber auch komplexere Alternative zu unserer einfachen, auf Config.swift basierenden Option *enableBioMetricAuth*.** Diese API ermöglicht es dir, biometrische Authentifizierung in deiner App zu verwenden und das Ergebnis per JavaScript an deine Website zurückzugeben. Zur biometrischen Authentifizierung gehören Face ID (bei neueren iPhone-Designs) und Touch ID (bei älteren iPhone-Designs) mit Code als Fallback. Durch den Aufruf des URL-Befehls „bioauth://“ kannst du die biometrische Authentifizierung nativ in deiner App auslösen. Sobald der Vorgang abgeschlossen ist, meldet WebViewGold die Ergebnisse an deine Web-App zurück, indem eine der folgenden Funktionen aufgerufen wird:

- **onBioAuthSuccess()**
  - Wird aufgerufen, wenn der Authentifizierungsvorgang erfolgreich war.
- **onBioAuthFailure(errorCode, errorMessage)**
  - Wird aufgerufen, wenn der Authentifizierungsvorgang fehlschlägt, und liefert Fehlerinformationen.
- **onBioAuthUnavailable()**
  - Wird aufgerufen, wenn die biometrische Authentifizierung auf dem Gerät nicht verfügbar ist.

Um diese API zu nutzen, musst du zunächst den Privacy-Key für die biometrische Face-ID-Authentifizierung in deiner **Info.plist**-Datei hinzufügen. Öffne dazu die **Info.plist**, fahre mit dem Mauszeiger über einen bestehenden Key, klicke auf das (+)-Symbol, um darunter einen neuen Key hinzuzufügen, und wähle die Option „**Privacy - Face ID Usage Description**“ aus. Ohne diesen Key unterstützt die App Face ID nicht. Der Wert dieses Keys ist eine Beschreibung, die dem Nutzer beim ersten Face-ID-Zugriff deiner App angezeigt wird. Diese Beschreibung sollte klar erläutern, warum deine App Face ID benötigt. Nachfolgend findest du ein Beispiel für eine Beschreibung dieses Keys:

![Beispiel des Face-ID-Privacy-Keys in Info.plist.](../../assets/ios/img/faceID_key.webp)\
Als Nächstes musst du die folgenden Funktionen (in JavaScript) in deiner Web-App definieren, um die Ergebnisse einer biometrischen Authentifizierung zu verarbeiten:

```html
<script>

function onBioAuthSuccess() {
    alert("Bio Authentication Succeeded");
}

function onBioAuthFailure(errorCode, errorMessage) {
    // errorCode = Int, errorMessage = String
    alert(`Bio Authentication Failed, ${errorMessage} (code ${errorCode})`);
}

function onBioAuthUnavailable() {
    alert("Bio Authentication Unavailable");
}

</script>
```

Lade dann diese Art von URL, um den biometrischen Authentifizierungsvorgang in deiner Web-App auszulösen:

```html
<script>

window.location.href = "bioauth://";

</script>
```

**Sicherheitshinweis:** Es ist zu beachten, dass böswillige Nutzer möglicherweise die Funktion onBioAuthSuccess() aufrufen können, ohne den Authentifizierungsvorgang tatsächlich abzuschlossen. Da die Authentifizierung ein sensibler Vorgang ist, wird empfohlen, in deiner Web-App eine zusätzliche Sicherheitsebene wie eine Cookie- oder Geolocation-Prüfung einzubauen, um die Integrität der Authentifizierung zu unterstützen. Bitte konsultiere den Cybersecurity-Experten deiner Website, um eine auf die Anforderungen deiner Web-App zugeschnittene Beratung zu erhalten.

---

## Weiterlesen

- ← Vorherige: [Kontakte-API](contacts.md)
- Weiter →: [Haptisches-Feedback-API](haptic-feedback.md)
- Dieselbe Funktion auf anderen Plattformen: [Android – Biometric Auth API](../android/biometric-auth.md)
- Sprachen: [🇺🇸 English](../../ios/biometric-authentication.md) · **🇩🇪 Deutsch** · [🇫🇷 Français](../../fr/ios/biometric-authentication.md) · [🇪🇸 Español](../../es/ios/biometric-authentication.md) · [🇨🇳 中文](../../zh/ios/biometric-authentication.md)

> [!TIP]
> **Zu wenig Zeit? Wir richten deine App für dich ein.** Unser Team konfiguriert, erstellt & reicht deine WebViewGold-App ein – schlüsselfertig, mit schneller Bearbeitung, Made in Germany. [App einrichten lassen →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **Im Browser erstellen:** Kein Mac, keine IDE: Der **WebViewGold Cloud Builder** konfiguriert, erstellt & lädt deine App online hoch. [Cloud Builder entdecken →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
