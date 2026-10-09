---
title: "In-App-Käufe-API – WebViewGold für Android Dokumentation"
description: "Verkaufe digitale Güter und Abonnements in deiner Android-WebView-App mit Google Play Billing."
lang: "de"
product: "WebViewGold für Android"
platform: "Android"
category: "APIs & Funktionen"
slug: "in-app-purchases"
canonical_url: "https://www.webviewgold.com/de/docs/android/in-app-purchases/"
keywords:
  - "In-App-Käufe-API"
  - "WebViewGold für Android"
  - "Website in App umwandeln"
  - "WebView-App-Dokumentation"
  - "Android WebView SDK"
  - "PWA zu App"
  - "HTML zu App"
  - "JavaScript-Bridge"
last_updated: "2026-10-09"
---

# In-App-Käufe-API – WebViewGold für Android

> **Zusammenfassung:** Verkaufe digitale Güter und Abonnements in deiner Android-WebView-App mit Google Play Billing.

[Dokumentation](../README.md) › [WebViewGold für Android](README.md) › In-App-Käufe-API

**Plattform:** Android · **Kategorie:** APIs & Funktionen · **Online-Version:** [www.webviewgold.com/de/docs/android/in-app-purchases/](https://www.webviewgold.com/de/docs/android/in-app-purchases/)

---

Innerhalb mancher Apps kannst du zusätzliche Inhalte oder Dienste erwerben. Solche Käufe werden als "In-App-Käufe" bezeichnet. Sie können für Entwickler eine attraktive Einnahmequelle darstellen und sind für Kunden sehr komfortabel, da sie zur Abwicklung bereits vorhandene Konten und Zahlungsquellen nutzen. WebViewGold ermöglicht das Auslösen von Google Play In-App-Käufen. Stelle sicher, dass du eine [Extended License](credits.md) von WebViewGold besitzt, wenn du diese Funktion in einem Endprodukt verwenden möchtest. Möchtest du ein Upgrade durchführen? [Erfahre hier, wie du ein Upgrade durchführst](https://help.market.envato.com/hc/en-us/articles/115005593503-If-I-choose-the-wrong-license-or-need-to-upgrade-my-license-how-easy-is-it-to-change-to-the-correct-license).

**Option 1 (Standard): RevenueCat**\
Erstelle dein kostenloses [RevenueCat-Konto](https://tinyurl.com/register-revenuecat), um zu beginnen. Preisinformationen sind auf deren Website verfügbar. Richte RevenueCat anschließend gemäß deren Einrichtungsassistenten und Dokumentation ein (Preisdetails findest du auf deren [Website](https://tinyurl.com/register-revenuecat)). Füge danach deine Daten in **Config.java** ein. Dieser Ansatz unterstützt außerdem das [15% Service Fee Tier Program](https://support.google.com/googleplay/android-developer/answer/112622?hl=en) des Google Play Store und Apples [Small Business Program](https://developer.apple.com/app-store/small-business-program/). Wenn du an diesen Programmen mit reduzierten Gebühren teilnimmst, informiere RevenueCat über deren Seiten [Apple Small Business Program](https://www.revenuecat.com/docs/platform-resources/apple-platform-resources/app-store-small-business-program) oder [Google 15% reduced service fee](https://www.revenuecat.com/docs/platform-resources/google-platform-resources/15-reduced-service-fee). So sieht die Einrichtung in Config.java aus:

```java
public static final String REVENUECAT_API_KEY = "xxxxxxxsxxxxxxxxxxxxxxxxxxxxxxxxxx"; //Your RevenueCat API Key (sign up via tinyurl.com/register-revenuecat first, then follow tinyurl.com/api-key-revenuecat how to find it)
public static final String REVENUECAT_PROJECT_ID = "xxxxxxx"; //Your RevenueCat Project ID (sign up via tinyurl.com/register-revenuecat first, then follow tinyurl.com/project-id-revenuecat how to find it)
```

Stelle sicher, dass der Paketname in der APK und in der Google Play Console mit dem in RevenueCat konfigurierten Projekt übereinstimmt. Löse einen Kauf oder ein Abonnement wie folgt aus:

```
revenuecat://purchase?external_id=user_123&product=sub_30_days
```

`external_id` = Nutzerkennung, z. B. die E-Mail-Adresse deines Kunden oder die Benutzer-ID. `product` = ID, die in der RevenueCat-Konsole angezeigt wird. Funktioniert sowohl unter Android als auch unter iOS.

## Option 2: Manuell (ohne RevenueCat)

Wir setzen uns dafür ein, unseren WebViewGold-Kunden zum Erfolg zu verhelfen, und möchten dich auf das 15% Service Fee Tier Program des Google Play Store und Apples Small Business Program aufmerksam machen. Diese Programme ermöglichen es qualifizierten Entwicklern, eine Provision von 15 % zu erhalten, was eine deutliche Reduzierung gegenüber den üblichen 30 % darstellt. Die Anmeldung ist schnell und einfach und kann dir potenziell 50 % an Gebühren sparen, indem **die Google- und Apple-Provisionssätze von 30 % auf 15 % reduziert werden**. Sobald du zugelassen bist, erhältst du den reduzierten Provisionssatz für alle kostenpflichtigen Apps und In-App-Käufe, die Kunden in den jeweiligen Stores tätigen. Weitere Informationen zum Google Play-Programm findest du **[hier](https://support.google.com/googleplay/android-developer/answer/112622?hl=en)** und zum Apple-Programm **[hier](https://developer.apple.com/app-store/small-business-program/)**.

Verlinke nach der Einrichtung für **In-App-Kaufprodukte** einfach auf eine URL dieser Art:

```html
<a href="inapppurchase://?package=purchase_package_identifier_name_here&disableadmob=true&consumable=true&successful_url=https://www.google.com">Buy In-App Purchase</a>
```

- Das "package" ist die Produktkennung des Artikels, den du verkaufen möchtest.
- Die "successful_url" ist die URL, die die App nach Abschluss des Kaufs laden soll.
  - *Du kannst auf dieser Seite ein Cookie speichern, damit sich deine Web-App merkt, dass der Kauf getätigt wurde.*
- Füge "disableadmob=true" hinzu, wenn du Werbung nach dem Kauf des Produkts deaktivieren möchtest.
- Damit der Nutzer für dasselbe In-App-Kaufprodukt erneut belastet werden kann (bei einem weiteren Kauf), setze das Attribut "consumable" auf true. Wenn du hingegen verhindern möchtest, dass der Nutzer für dasselbe Produkt erneut belastet wird (bei einem weiteren Kauf), setze "consumable" auf false oder lasse es ganz weg (da false der Standardwert ist). Stelle sicher, dass du WebViewGold für Android v12.5 oder neuer verwendest.

Alternativ kannst du für **In-App-Abonnementprodukte** eine URL dieser Art verwenden:

```html
<a href="inappsubscription://?package=purchase_package_identifier_name_here&expired_url=https://www.yahoo.com&successful_url=https://www.google.com">Start In-App Subscription</a>
```

- Das "package" ist die Produktkennung des Abonnements, das du verkaufen möchtest.
- Die "successful_url" ist die URL, die die App nach Abschluss des Kaufs laden soll.
  - *Du kannst auf dieser Seite ein Cookie speichern, damit sich deine Web-App merkt, dass das Abonnement aktiviert wurde.*
- Die "expired_url" ist die URL, die die App laden soll, sobald das Abonnement nicht mehr gültig ist.
  - *Du kannst auf dieser Seite ein Cookie aktualisieren/löschen, damit sich deine Web-App merkt, dass das Abonnement deaktiviert wurde.*

In diesem URL-Beispiel soll https://www.google.com nach der erfolgreichen Abonnementaktivierung aufgerufen werden, und https://www.yahoo.com soll aufgerufen werden, sobald das Abonnement abgelaufen ist.\
Du kannst den Benutzer serverseitig identifizieren. Wenn z. B. die Seite /buy_now.php auf die In-App-Purchase-API weiterleitet und diese API auf /thanks.php weiterleitet, kannst du weiterhin serverseitig auf die Benutzer-/Sitzungs-Cookies zugreifen und den Benutzer identifizieren, der diesen In-App-Kauf gerade getätigt hat. Stelle in diesem Anwendungsfall bitte sicher, dass du CLEAR_CACHE_ON_STARTUP in der Datei Config.java deaktivierst, um die durch den In-App-Kaufvorgang aktivierten Cookies zu erhalten.

**Abonnements verwalten/kündigen:** WebViewGold für Android kann direkt auf den Bildschirm zur Abonnementverwaltung des Play Store verlinken – richte deinen Link einfach auf `cancelinapppurchase://`:

```html
<script>
<a href="cancelinapppurchase://">Manage/cancel subscription in Google Play</a>
<script>
```

**Käufe wiederherstellen:** WebViewGold für Android bietet eine einfache Möglichkeit, von Nutzern getätigte In-App-Käufe wiederherzustellen. Nützlich z. B. für Szenarien, in denen Nutzer die App neu installieren oder das Gerät wechseln und wieder Zugriff auf ihre erworbenen Inhalte benötigen:

```html
<script>
<a href="restoreinapppurchases://">Restore</a>
<script>
```

**Serverseitige Verifizierung:** Zusätzlich oder alternativ ermöglicht dir WebViewGold, In-App-Kauf- oder Abonnementdaten serverseitig zu verarbeiten. Nach einer erfolgreichen Transaktion werden die folgenden JavaScript-Variablen erstellt und von WebViewGold in die Webseite injiziert: \
**1. planID:** Enthält die Produkt-ID\
**2. transactionIdentifier:** Enthält die eindeutige Transaktions-ID\
**3. subreceipts:** Enthält eindeutige Beleg-IDs für die Abonnements des Nutzers\
Auf diese Variablen kann direkt auf der Webseite für die serverseitige Speicherung und Validierung zugegriffen werden. Beachte, dass diese Variablen nach einer Transaktion direkt in das globale window-Objekt injiziert werden. Stelle sicher, dass dein JavaScript auf derselben Seite ausgeführt wird, auf der die Variablen zugänglich sind. Füge geeignete Fallback-Mechanismen hinzu, falls die Variablen nicht innerhalb des erwarteten Zeitraums verfügbar sind (wie in der Timeout-Implementierung dargestellt).
Das Senden dieser Variablen an deinen Server ermöglicht dir die sichere Validierung von Abonnements und Transaktionen mithilfe der Beleg-Validierungs-API von Apple oder einer von dir gewählten Methode. Hier ist ein Beispiel für eine JavaScript-Implementierung:

```html
<script>
// Utility function to wait for a variable to be defined
function waitForVariable(variableName, callback, timeout = 5000) {
    const startTime = Date.now();

    (function checkVariable() {
        if (window[variableName] !== undefined) {
            callback(window[variableName]);
        } else if (Date.now() - startTime < timeout) {
            setTimeout(checkVariable, 100);
        } else {
            console.error(`Timeout: ${variableName} was not set within ${timeout} ms`);
        }
    })();
}

// Example: Handling In-App Purchase/Subscription variables
waitForVariable("planID", function(planID) {
    console.log("planID:", planID);
    // Send the Product ID to your server
    sendToServer("planID", planID);
});

waitForVariable("transactionIdentifier", function(transactionIdentifier) {
    console.log("transactionIdentifier:", transactionIdentifier);
    // Send the Transaction ID to your server
    sendToServer("transactionIdentifier", transactionIdentifier);
});

waitForVariable("subreceipts", function(subreceipts) {
    console.log("subreceipts:", subreceipts);
    // Send Subscription Receipt IDs to your server
    sendToServer("subreceipts", subreceipts);
});

// Function to send data to your server for validation
function sendToServer(key, value) {
    fetch("https://example.com/api/validate", {
        method: "POST",
        headers: {
            "Content-Type": "application/json"
        },
        body: JSON.stringify({ [key]: value })
    })
    .then(response => response.json())
    .then(data => console.log(`Server Response for ${key}:`, data))
    .catch(error => console.error(`Error sending ${key}:`, error));
}
</script>
```

**Lokalisierte Preisgestaltung / Store-Standort abrufen:** Das URL-Schema `getstorelocation://` injiziert den Play-Store-Standort in eine JavaScript-Variable. Wenn `getstorelocation://` aufgerufen/verlinkt wird, ruft der WebViewGold-Wrapper den Ländercode des Play Store ab, sofern verfügbar. Alternativ kannst du in der Konfigurationsdatei `autoInjectVariable` auf `true` setzen, um diesen (und andere) Werte automatisch in JavaScript zu injizieren, ohne einen URL-Aufruf zu benötigen. Der Ländercode wird dann in die JavaScript-Variable `storeLocation` injiziert, damit deine Web-App ihn weiter verwenden kann (**z. B. zur Anzeige lokalisierter Preise**). Ist der Code nicht verfügbar, wird `storeLocation` auf `null` gesetzt:

- Bei Erfolg (Beispiel Vereinigte Staaten): `var storeLocation = 'US';`
- Wenn kein Ländercode gefunden wird: `var storeLocation = null;`

Hinweis: Wie bei jeder Technologie ist es wichtig zu erwähnen, dass auch bei der Nutzung unserer API das Risiko besteht, dass einige (technisch versierte) Nutzer möglicherweise auf die eingeschränkten Inhalte zugreifen können, ohne dafür zu bezahlen. Dies könnte beispielsweise geschehen, indem der Success-URL-Link direkt abgerufen und geöffnet wird, die App deinstalliert und anschließend Abonnementprodukte gekündigt werden, sodass die Expiration-URL nie aufgerufen wird (um dieses Risiko zu minimieren, kannst du gelegentlich erneute Autorisierungen anfordern), oder durch die Ausübung von Widerrufsrechten und/oder Rückbuchungsverfahren bei Kreditkarten. Es ist jedoch erwähnenswert, dass bei jedem digitalen Ansatz ein gewisses Risiko besteht. Insgesamt ist unsere API ein praktischer und leicht zu integrierender Ansatz zur Bereitstellung bezahlter Inhalte für App-Nutzer, und wir arbeiten weiter an Möglichkeiten, Risiken weiter zu reduzieren. Die Nutzung unserer API erfolgt weiterhin auf eigenes Risiko und ohne Gewährleistung, aber insgesamt überwiegen die Vorteile der Nutzung unserer API die Risiken für die meisten Nutzer bei Weitem, auch wenn es wichtig ist, sich des Risikos eines unbefugten/unbezahlten Zugriffs auf Inhalte bewusst zu sein. Es wird empfohlen, die Verkaufsdaten der Google Play Store Developer Console mit serverseitigen Aktivierungen von In-App-Kaufprodukten zu verfolgen und zu vergleichen, um eine korrekte Umsatzberichterstattung zu gewährleisten und potenzielle Abweichungen zu erkennen.

---

## Weiterlesen

- ← Vorherige: [In-App-Rating-API](in-app-rating.md)
- Weiter →: [IAP History API](iap-history.md)
- Dieselbe Funktion auf anderen Plattformen: [iOS – In-App-Käufe-API](../ios/in-app-purchases.md) · [macOS – In-App Purchases API](../macos/in-app-purchases.md)
- Sprachen: [🇺🇸 English](../../android/in-app-purchases.md) · **🇩🇪 Deutsch** · [🇫🇷 Français](../../fr/android/in-app-purchases.md) · [🇪🇸 Español](../../es/android/in-app-purchases.md) · [🇨🇳 中文](../../zh/android/in-app-purchases.md)

> [!TIP]
> **Zu wenig Zeit? Wir richten deine App für dich ein.** Unser Team konfiguriert, erstellt & reicht deine WebViewGold-App ein – schlüsselfertig, mit schneller Bearbeitung, Made in Germany. [App einrichten lassen →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_android_doc_online)
>
> **Im Browser erstellen:** Kein Mac, keine IDE: Der **WebViewGold Cloud Builder** konfiguriert, erstellt & lädt deine App online hoch. [Cloud Builder entdecken →](https://www.webviewgold.com/cloud-builder?ref=android_docs)
