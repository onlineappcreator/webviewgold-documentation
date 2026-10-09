---
title: "In-App-Käufe-API – WebViewGold für iOS Dokumentation"
description: "Verkaufe digitale Güter und Abonnements in deiner iOS-WebView-App mit StoreKit-basierten In-App-Käufen."
lang: "de"
product: "WebViewGold für iOS"
platform: "iOS"
category: "APIs & Funktionen"
slug: "in-app-purchases"
canonical_url: "https://www.webviewgold.com/de/docs/iOS/in-app-purchases/"
keywords:
  - "In-App-Käufe-API"
  - "WebViewGold für iOS"
  - "Website in App umwandeln"
  - "WebView-App-Dokumentation"
  - "iOS WebView SDK"
  - "PWA zu App"
  - "HTML zu App"
  - "JavaScript-Bridge"
last_updated: "2026-10-09"
---

# In-App-Käufe-API – WebViewGold für iOS

> **Zusammenfassung:** Verkaufe digitale Güter und Abonnements in deiner iOS-WebView-App mit StoreKit-basierten In-App-Käufen.

[Dokumentation](../README.md) › [WebViewGold für iOS](README.md) › In-App-Käufe-API

**Plattform:** iOS · **Kategorie:** APIs & Funktionen · **Online-Version:** [www.webviewgold.com/de/docs/iOS/in-app-purchases/](https://www.webviewgold.com/de/docs/iOS/in-app-purchases/)

---

Innerhalb mancher Apps kannst du zusätzliche Inhalte oder Dienste erwerben. Solche Käufe werden als "In-App-Käufe" bezeichnet. Sie können für Entwickler eine attraktive Einnahmequelle darstellen und sind für Kunden sehr komfortabel, da sie zur Abwicklung bereits vorhandene Konten und Zahlungsquellen nutzen. WebViewGold ermöglicht das Auslösen von App Store In-App-Käufen. Stelle sicher, dass du eine [Extended License](credits.md) von WebViewGold besitzt, wenn du diese Funktion in einem Endprodukt verwenden möchtest. Möchtest du ein Upgrade durchführen? [Erfahre hier, wie du ein Upgrade durchführst](https://help.market.envato.com/hc/en-us/articles/115005593503-If-I-choose-the-wrong-license-or-need-to-upgrade-my-license-how-easy-is-it-to-change-to-the-correct-license).

**Option 1 (Standard): RevenueCat**\
Erstelle dein kostenloses [RevenueCat-Konto](https://tinyurl.com/register-revenuecat), um zu beginnen. Preisinformationen sind auf deren Website verfügbar. Richte RevenueCat anschließend gemäß deren Einrichtungsassistenten und Dokumentation ein (Preisdetails findest du auf deren [Website](https://tinyurl.com/register-revenuecat)). Füge danach deine Daten in **Config.swift** ein. Dieser Ansatz unterstützt außerdem das [15% Service Fee Tier Program](https://support.google.com/googleplay/android-developer/answer/112622?hl=en) des Google Play Store und Apples [Small Business Program](https://developer.apple.com/app-store/small-business-program/). Wenn du an diesen Programmen mit reduzierten Gebühren teilnimmst, informiere RevenueCat über deren Seiten [Apple Small Business Program](https://www.revenuecat.com/docs/platform-resources/apple-platform-resources/app-store-small-business-program) oder [Google 15% reduced service fee](https://www.revenuecat.com/docs/platform-resources/google-platform-resources/15-reduced-service-fee). So sieht die Einrichtung in Config.swift aus:

```swift
static let kRevenueCatEnable = true //Set to true to activate RevenueCat
static let kRevenueCatShowDefaultOfferingPaywall = true //Set to true to show the default offering paywall on app launch
static let revenueCatAPIKey = "xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx" //Your RevenueCat API Key (sign up via tinyurl.com/register-revenuecat first, then follow tinyurl.com/api-key-revenuecat how to find it)
static let revenueCatProjectID = "xxxxxxxxx" //Your RevenueCat Project ID (sign up via tinyurl.com/register-revenuecat first, then follow tinyurl.com/project-id-revenuecat how to find it)
```

Stelle sicher, dass deine Bundle ID in Xcode und App Store Connect mit dem in RevenueCat konfigurierten Projekt übereinstimmt. Löse einen Kauf oder ein Abonnement wie folgt aus:

```
revenuecat://purchase?external_id=user_123&product=sub_30_days
```

`external_id` = Nutzerkennung, z. B. die E-Mail-Adresse deines Kunden oder die Benutzer-ID. `product` = ID, die in der RevenueCat-Konsole angezeigt wird.

Du kannst außerdem direkt aus deiner Web-App eine native **RevenueCat-Paywall** anzeigen (konfiguriert im RevenueCat-Dashboard) – erfordert iOS 15 oder höher:

```
revenuecat://launchPaywall?external_id=user_123&offering=CustomOfferingOne
```

`external_id` = Nutzerkennung, z. B. die E-Mail-Adresse deines Kunden oder die Benutzer-ID (erforderlich). `offering` = Optionale Kennung des RevenueCat-Offerings, dessen Paywall angezeigt werden soll; lasse den Parameter weg, um die Paywall des Standard-Offerings zu präsentieren.

## Option 2: Manuell (ohne RevenueCat)

Füge im ersten Schritt die App Store Connect-Details deines "Shared Secret" für In-App-Käufe in die Datei **Config.swift** ein. Um dein "Shared Secret" in App Store Connect zu finden, musst du dich zunächst in dein App Store Connect-Konto einloggen. Gehe dann zum Abschnitt "Users and Access" und wähle den Reiter "Shared Secret". Dein generiertes "Shared Secret" wird aufgelistet, und du kannst es kopieren und in das entsprechende Feld "IAPSharedSecret" in Config.swift von WebViewGold einfügen. \
Uns liegt der Erfolg unserer Kunden am Herzen, und wir sind hier, um sie in jeder Hinsicht zu unterstützen: Aus diesem Grund möchten wir hier auf das App Store Small Business Program und das 15% Service Fee Tier Program des Google Play Store hinweisen. Im Rahmen dieser Programme können sich qualifizierte Entwickler für eine reduzierte Provision von 15 % anstelle der üblichen 30 % qualifizieren. Das Ausfüllen der Formulare dauert nur wenige Minuten und kann dir potenziell 50 % der Gebühren sparen (**Reduzierung der Provision von 30 % auf 15 %**). Sobald du zugelassen bist, erhältst du den reduzierten Provisionssatz für alle kostenpflichtigen Apps und In-App-Käufe, die Kunden in den jeweiligen Stores tätigen. Weitere Informationen zum Apple-Programm findest du [**hier**](https://developer.apple.com/app-store/small-business-program/) und zum Google Play-Programm [**hier**](https://support.google.com/googleplay/android-developer/answer/112622?hl=en). \
Verlinke nach der Einrichtung für **In-App-Kaufprodukte** einfach auf eine URL dieser Art:

```html
<a href="inapppurchase://?package=IN-APP_PURCHASE_PRODUCT_IDENTIFIER&disableadmob=true&successful_url=https://www.google.com">Buy In-App Purchase</a>
```

- Das "package" ist die Produktkennung des Artikels, den du verkaufen möchtest.
- Die "successful_url" ist die URL, die die App nach Abschluss des Kaufs laden soll.
  - *Du kannst auf dieser Seite ein Cookie speichern, damit sich deine Web-App merkt, dass der Kauf getätigt wurde.*
- Füge "disableadmob=true" hinzu, wenn du AdMob-Anzeigen nach dem Kauf des Produkts deaktivieren möchtest.

Für **In-App-Abonnementprodukte** verwende dieses URL-Schema:

```html
<a href="inappsubscription://?package=IN-APP_PURCHASE_PRODUCT_IDENTIFIER&expired_url=https://www.yahoo.com&successful_url=https://www.google.com">Start In-App Subscription</a>
```

- Das "package" ist die Produktkennung des Abonnements, das du verkaufen möchtest.
- Die "successful_url" ist die URL, die die App nach Abschluss des Kaufs laden soll.
  - *Du kannst auf dieser Seite ein Cookie speichern, damit sich deine Web-App merkt, dass das Abonnement aktiviert wurde.*
- Die "expired_url" ist die URL, die die App laden soll, sobald das Abonnement nicht mehr gültig ist.
  - *Du kannst auf dieser Seite ein Cookie aktualisieren/löschen, damit sich deine Web-App merkt, dass das Abonnement deaktiviert wurde.*

Alle Informationen zur Produktkennung für In-App-Käufe findest du [hier](https://developer.apple.com/library/archive/qa/qa1329/_index.html).\
Du kannst den Benutzer serverseitig identifizieren. Wenn z. B. die Seite /buy_now.php auf die In-App-Purchase-API weiterleitet und diese API auf /thanks.php weiterleitet, kannst du weiterhin serverseitig auf die Benutzer-/Sitzungs-Cookies zugreifen und den Benutzer identifizieren, der diesen In-App-Kauf gerade getätigt hat. Stelle in diesem Anwendungsfall bitte sicher, dass du die Option *deletecache* in der Datei *Config.swift* deaktivierst, um die durch den In-App-Kaufvorgang aktivierten Cookies zu erhalten.

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

**Käufe wiederherstellen:** Ein Aufruf von `restoreinapppurchases://` ermöglicht es deiner App, zuvor gekaufte Inhalte wieder zu aktivieren. Wenn ein Nutzer auf einen Link mit diesem URL-Schema tippt, startet die App einen Vorgang zur erneuten Validierung und Wiederherstellung von In-App-Käufen — ideal für Szenarien wie eine Neuinstallation der App oder einen Gerätewechsel. Füge einfach einen Link wie den folgenden hinzu, damit deine Nutzer ihre Käufe wiederherstellen können:

```html
<a href="restoreinapppurchases://">Restore Purchases</a>
```

**Kaufhistorie:** Wie du die bisherigen Käufe des Nutzers in deiner Web-App anzeigst, erfährst du unter [In-App-Purchase-History-API](iap-history.md) (`getpurchasehistory://`).

**Abonnement kündigen:** Ein Aufruf von `cancelinapppurchase://` leitet Nutzer zum offiziellen Apple-Portal zur Abonnementverwaltung weiter, wo sie ihre Abonnements über die native Apple-Oberfläche kündigen können. Füge einfach einen Link wie den folgenden hinzu, um Nutzer zur Verwaltung ihrer Abonnements weiterzuleiten:

```html
<a href="cancelinapppurchase://">Cancel Subscription</a>
```

**Lokalisierte Preisgestaltung / Store-Standort abrufen:** Das URL-Schema `getstorelocation://` injiziert den App-Store-Standort in eine JavaScript-Variable. Nachdem `getstorelocation://` aufgerufen/verlinkt wurde, ruft der WebViewGold-Wrapper den Ländercode des App Store ab, sofern verfügbar. Alternativ kannst du in Config.swift `autoInjectVariable` auf `true` setzen, um diesen (und andere) Werte automatisch in JavaScript zu injizieren, ohne im Vorfeld eine URL aufrufen zu müssen. Der Ländercode wird dann in die JavaScript-Variable `storeLocation` injiziert, damit deine Web-App ihn weiter verwenden kann (**z. B. zur Anzeige lokalisierter Preise**). Ist der Code nicht verfügbar, wird `storeLocation` auf `null` gesetzt:

- Bei Erfolg (Beispiel Vereinigte Staaten von Amerika): `var storeLocation = 'US';`
- Wenn kein Ländercode gefunden wird: `var storeLocation = null;`

Hinweis: Die Verwendung unserer API zur Bereitstellung bezahlter Inhalte für App-Nutzer birgt ein gewisses Risiko, dass technisch versierte Nutzer auf die Inhalte zugreifen, ohne dafür zu bezahlen. Dies kann auf verschiedene Weise geschehen, z. B. durch direktes Abrufen und Öffnen des Success-URL-Links, durch Kündigung von Abonnementprodukten nach Deinstallation der App oder durch die Ausübung von Widerrufsrechten und Rückbuchungsverfahren bei Kreditkarten. Es ist jedoch entscheidend zu beachten, dass bei jedem digitalen Ansatz ein gewisses Risiko besteht. Auch wenn wir weiterhin an Möglichkeiten arbeiten, diese Risiken zu reduzieren, liegt es letztlich beim WebViewGold-Nutzer/-Entwickler, das Risiko eines unbefugten/unbezahlten Zugriffs auf Inhalte zu akzeptieren, wenn er den vorgeschlagenen Ansatz nutzt, da die API ohne Gewährleistung geliefert wird. Trotz dessen überwiegen die Vorteile der Nutzung unserer API für die meisten Nutzer im Allgemeinen die Risiken. Um eine korrekte Umsatzberichterstattung sicherzustellen und potenzielle Abweichungen zu erkennen, empfehlen wir, die Verkaufsdaten von App Store Connect mit den serverseitigen Aktivierungen von In-App-Kaufprodukten zu verfolgen und zu vergleichen.

---

## Weiterlesen

- ← Vorherige: [In-App-Rating-Dialog-API](in-app-rating.md)
- Weiter →: [IAP-History-API](iap-history.md)
- Dieselbe Funktion auf anderen Plattformen: [Android – In-App-Käufe-API](../android/in-app-purchases.md) · [macOS – In-App Purchases API](../macos/in-app-purchases.md)
- Sprachen: [🇺🇸 English](../../ios/in-app-purchases.md) · **🇩🇪 Deutsch** · [🇫🇷 Français](../../fr/ios/in-app-purchases.md) · [🇪🇸 Español](../../es/ios/in-app-purchases.md) · [🇨🇳 中文](../../zh/ios/in-app-purchases.md)

> [!TIP]
> **Zu wenig Zeit? Wir richten deine App für dich ein.** Unser Team konfiguriert, erstellt & reicht deine WebViewGold-App ein – schlüsselfertig, mit schneller Bearbeitung, Made in Germany. [App einrichten lassen →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **Im Browser erstellen:** Kein Mac, keine IDE: Der **WebViewGold Cloud Builder** konfiguriert, erstellt & lädt deine App online hoch. [Cloud Builder entdecken →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
