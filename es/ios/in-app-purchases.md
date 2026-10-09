---
title: "API de compras integradas – Documentación de WebViewGold para iOS"
description: "Venda bienes digitales y suscripciones en su app WebView de iOS con compras integradas basadas en StoreKit."
lang: "es"
product: "WebViewGold para iOS"
platform: "iOS"
category: "API y funciones"
slug: "in-app-purchases"
canonical_url: "https://www.webviewgold.com/es/docs/iOS/in-app-purchases/"
keywords:
  - "API de compras integradas"
  - "WebViewGold para iOS"
  - "convertir sitio web en app"
  - "documentación de app WebView"
  - "SDK WebView de iOS"
  - "PWA a app"
  - "HTML a app"
  - "puente de JavaScript"
last_updated: "2026-10-09"
---

# API de compras integradas – WebViewGold para iOS

> **Resumen:** Venda bienes digitales y suscripciones en su app WebView de iOS con compras integradas basadas en StoreKit.

[Documentación](../README.md) › [WebViewGold para iOS](README.md) › API de compras integradas

**Plataforma:** iOS · **Categoría:** API y funciones · **Versión en línea:** [www.webviewgold.com/es/docs/iOS/in-app-purchases/](https://www.webviewgold.com/es/docs/iOS/in-app-purchases/)

---

Dentro de algunas apps, usted puede comprar contenidos o servicios adicionales. Este tipo de compras se denomina «compras integradas». Pueden constituir una atractiva fuente de ingresos para los desarrolladores y resultan muy cómodas para los clientes, ya que utilizan las cuentas y los métodos de pago existentes para la liquidación. WebViewGold permite activar las compras integradas del App Store. Asegúrese de contar con una [Licencia Extendida](credits.md) de WebViewGold si tiene previsto utilizar esta función en un producto final. ¿Necesita ampliar su licencia? [Descubra aquí cómo ampliarla](https://help.market.envato.com/hc/en-us/articles/115005593503-If-I-choose-the-wrong-license-or-need-to-upgrade-my-license-how-easy-is-it-to-change-to-the-correct-license).

**Opción 1 (Predeterminada): RevenueCat**\
Cree su [cuenta gratuita de RevenueCat](https://tinyurl.com/register-revenuecat) para comenzar. La información de precios está disponible en su sitio web. A continuación, configure RevenueCat siguiendo sus asistentes de configuración y su documentación (los detalles de precios están disponibles en su [sitio web](https://tinyurl.com/register-revenuecat)). Después, añada sus datos en **Config.swift**. Este enfoque también admite el [15% Service Fee Tier Program](https://support.google.com/googleplay/android-developer/answer/112622?hl=en) de Google Play Store y el [Small Business Program](https://developer.apple.com/app-store/small-business-program/) de Apple. Si participa en estos programas de tarifas reducidas, informe a RevenueCat a través de sus páginas [Apple Small Business Program](https://www.revenuecat.com/docs/platform-resources/apple-platform-resources/app-store-small-business-program) o [Google 15% reduced service fee](https://www.revenuecat.com/docs/platform-resources/google-platform-resources/15-reduced-service-fee). Así es como se ve la configuración en Config.swift:

```swift
static let kRevenueCatEnable = true //Set to true to activate RevenueCat
static let kRevenueCatShowDefaultOfferingPaywall = true //Set to true to show the default offering paywall on app launch
static let revenueCatAPIKey = "xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx" //Your RevenueCat API Key (sign up via tinyurl.com/register-revenuecat first, then follow tinyurl.com/api-key-revenuecat how to find it)
static let revenueCatProjectID = "xxxxxxxxx" //Your RevenueCat Project ID (sign up via tinyurl.com/register-revenuecat first, then follow tinyurl.com/project-id-revenuecat how to find it)
```

Asegúrese de que su Bundle ID en Xcode y App Store Connect coincida con el proyecto configurado en RevenueCat. Active una compra o suscripción usando:

```
revenuecat://purchase?external_id=user_123&product=sub_30_days
```

`external_id` = identificador de usuario, por ejemplo, el correo electrónico o el ID de usuario de su cliente. `product` = ID mostrado en la consola de RevenueCat.

También puede presentar un **paywall nativo de RevenueCat** (configurado en el panel de RevenueCat) directamente desde su app web; requiere iOS 15 o superior:

```
revenuecat://launchPaywall?external_id=user_123&offering=CustomOfferingOne
```

`external_id` = identificador de usuario, por ejemplo, el correo electrónico o el ID de usuario de su cliente (obligatorio). `offering` = identificador opcional del offering de RevenueCat cuyo paywall debe mostrarse; omítalo para presentar el paywall del offering predeterminado.

## Opción 2: Manual (sin RevenueCat)

Como primer paso, introduzca en el archivo **Config.swift** los datos del «Shared Secret» de su compra integrada obtenidos en App Store Connect. Para encontrar su «Shared Secret» en App Store Connect, primero debe iniciar sesión en su cuenta de App Store Connect. A continuación, vaya a la sección «Users and Access» y seleccione la pestaña «Shared Secret». Su «Shared Secret» generado aparecerá listado y podrá copiarlo y pegarlo en el campo «IAPSharedSecret» correspondiente de Config.swift de WebViewGold. \
Nos importa el éxito de nuestros clientes y estamos aquí para apoyarles en todo lo posible: por eso queremos mencionar aquí el App Store Small Business Program y el 15% Service Fee Tier Program de Google Play Store. Bajo estos programas, los desarrolladores que cumplan los requisitos pueden acogerse a una comisión reducida del 15 %, frente al 30 % estándar. Rellenar los formularios solo lleva unos minutos y puede ahorrarle potencialmente el 50 % de las comisiones (**reducción del 30 % al 15 %**). Una vez aprobado, obtendrá la tarifa de comisión reducida para todas las apps de pago y compras integradas realizadas por clientes en las tiendas correspondientes. Encuentre más información sobre el programa de Apple [**aquí**](https://developer.apple.com/app-store/small-business-program/) y sobre el programa de Google Play [**aquí**](https://support.google.com/googleplay/android-developer/answer/112622?hl=en). \
Una vez configurado, para los **productos de compra integrada** basta con enlazar a una URL de este tipo:

```html
<a href="inapppurchase://?package=IN-APP_PURCHASE_PRODUCT_IDENTIFIER&disableadmob=true&successful_url=https://www.google.com">Buy In-App Purchase</a>
```

- El «package» es el identificador de producto del artículo que desea vender.
- La «successful_url» es la URL que quiere que cargue la app una vez completada la compra.
  - *Puede guardar una cookie en esta página para que su web app recuerde que se ha realizado la compra.*
- Incluya «disableadmob=true» si desea desactivar los anuncios de AdMob tras la compra del producto.

Para los **productos de suscripción integrada**, utilice este tipo de esquema de URL:

```html
<a href="inappsubscription://?package=IN-APP_PURCHASE_PRODUCT_IDENTIFIER&expired_url=https://www.yahoo.com&successful_url=https://www.google.com">Start In-App Subscription</a>
```

- El «package» es el identificador de producto de la suscripción que desea vender.
- La «successful_url» es la URL que quiere que cargue la app una vez completada la compra.
  - *Puede guardar una cookie en esta página para que su web app recuerde que la suscripción se ha activado.*
- La «expired_url» es la URL que quiere que cargue la app cuando la suscripción deje de ser válida.
  - *Puede actualizar/eliminar una cookie en esta página para que su web app recuerde que la suscripción se ha desactivado.*

Puede encontrar toda la información sobre el identificador de producto de la compra integrada [aquí](https://developer.apple.com/library/archive/qa/qa1329/_index.html).\
Puede identificar al usuario en el servidor. Por ejemplo, si el sitio /buy_now.php redirige a la API de compras integradas y esa API redirige a /thanks.php, seguirá pudiendo acceder a las cookies de usuario/sesión desde el servidor e identificar al usuario que acaba de realizar esa compra integrada. En este caso de uso, asegúrese de desactivar la opción *deletecache* en el archivo *Config.swift* para conservar las cookies activadas durante el proceso de compra integrada.

**Verificación en el servidor:** Adicionalmente o como alternativa, WebViewGold le permite además gestionar los datos de compras integradas o suscripciones desde el servidor. Tras una transacción exitosa, WebViewGold crea e inyecta en la página web las siguientes variables JavaScript: \
**1. planID:** Contiene el ID de producto\
**2. transactionIdentifier:** Contiene el ID único de transacción\
**3. subreceipts:** Contiene los IDs de recibo únicos de las suscripciones del usuario\
Se puede acceder a estas variables directamente en la página web para su almacenamiento y validación en el servidor. Tenga en cuenta que estas variables se inyectan directamente en el objeto global window tras una transacción. Asegúrese de que su JavaScript se ejecuta en la misma página en la que las variables son accesibles. Añada mecanismos de reserva adecuados si las variables no están disponibles dentro del plazo previsto (como se muestra en la implementación del timeout).
El envío de estas variables a su servidor le permite validar suscripciones y transacciones de forma segura utilizando la API de validación de recibos de Apple o el método que prefiera. A continuación, un ejemplo de implementación en JavaScript:

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

**Restaurar compras:** Una llamada a `restoreinapppurchases://` permite a su app rehabilitar contenidos comprados anteriormente. Cuando un usuario pulsa un enlace con este esquema de URL, la app inicia un proceso para revalidar y restaurar las compras integradas, ideal para casos como la reinstalación de la app o el cambio de dispositivo. Simplemente añada un enlace como el siguiente para que los usuarios puedan restaurar sus compras:

```html
<a href="restoreinapppurchases://">Restore Purchases</a>
```

**Historial de compras:** Para mostrar las compras anteriores del usuario dentro de su aplicación web, consulte la [API del historial de compras In-App](iap-history.md) (`getpurchasehistory://`).

**Cancelar suscripción:** Una llamada a `cancelinapppurchase://` dirige a los usuarios al portal oficial de gestión de suscripciones de Apple, donde pueden cancelar sus suscripciones a través de la interfaz nativa de Apple. Simplemente añada un enlace como el siguiente para redirigir a los usuarios a gestionar sus suscripciones:

```html
<a href="cancelinapppurchase://">Cancel Subscription</a>
```

**Precios localizados / Obtener ubicación de la tienda:** El esquema de URL `getstorelocation://` inyecta la ubicación del App Store en una variable JavaScript. Tras llamar/enlazar a `getstorelocation://`, el wrapper de WebViewGold recupera el código de país del App Store, si está disponible. Como alternativa, puede activar `autoInjectVariable` a `true` en Config.swift para inyectar automáticamente este (y otros) valores en JavaScript sin necesidad de llamar a una URL previamente. El código de país se inyecta entonces en una variable JavaScript `storeLocation` para que su web app pueda seguir utilizándolo (**por ejemplo, para mostrar precios localizados**). Si el código no está disponible, `storeLocation` se establecerá en `null`:

- Si tiene éxito (ejemplo Estados Unidos de América): `var storeLocation = 'US';`
- Si no se encuentra ningún código de país: `var storeLocation = null;`

Nota: Utilizar nuestra API para ofrecer contenido de pago a los usuarios de la app conlleva cierto riesgo de que usuarios con conocimientos técnicos accedan al contenido sin pagar por él. Esto podría ocurrir mediante distintos métodos, como recuperar y abrir directamente el enlace de la Success URL, cancelar productos de suscripción después de desinstalar la app o utilizar derechos de desistimiento y procesos de contracargo en las tarjetas de crédito. Sin embargo, es fundamental señalar que cualquier enfoque digital lleva asociado algún nivel de riesgo. Aunque seguimos trabajando en reducir estos riesgos, en última instancia corresponde al usuario/desarrollador de WebViewGold aceptar el riesgo de acceso no autorizado/impago al contenido al utilizar el enfoque propuesto, ya que la API se ofrece sin garantía. A pesar de ello, para la mayoría de los usuarios las ventajas de utilizar nuestra API superan generalmente los riesgos. Para garantizar un informe preciso de los ingresos e identificar posibles discrepancias, recomendamos hacer un seguimiento y comparar los datos de ventas de App Store Connect con las activaciones en el servidor de los productos de compras integradas.

---

## Seguir leyendo

- ← Anterior: [API del diálogo de valoración](in-app-rating.md)
- Siguiente →: [API del historial de compras](iap-history.md)
- La misma función en otras plataformas: [Android – API de compras integradas](../android/in-app-purchases.md) · [macOS – API In-App Purchases](../macos/in-app-purchases.md)
- Idiomas: [🇺🇸 English](../../ios/in-app-purchases.md) · [🇩🇪 Deutsch](../../de/ios/in-app-purchases.md) · [🇫🇷 Français](../../fr/ios/in-app-purchases.md) · **🇪🇸 Español** · [🇨🇳 中文](../../zh/ios/in-app-purchases.md)

> [!TIP]
> **¿Sin tiempo? Configuramos su app por usted.** Nuestro equipo configura, compila & publica su app WebViewGold: llave en mano, entrega rápida, Made in Germany. [Configurar mi app →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **Compile en su navegador:** Sin Mac ni IDE: el **WebViewGold Cloud Builder** configura, compila & sube su app en línea. [Descubra Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
