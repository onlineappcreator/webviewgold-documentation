---
title: "API de compras integradas – Documentación de WebViewGold para Android"
description: "Venda productos digitales y suscripciones en su aplicación Android WebView con Google Play Billing."
lang: "es"
product: "WebViewGold para Android"
platform: "Android"
category: "API y funciones"
slug: "in-app-purchases"
canonical_url: "https://www.webviewgold.com/es/docs/android/in-app-purchases/"
keywords:
  - "API de compras integradas"
  - "WebViewGold para Android"
  - "convertir sitio web en app"
  - "documentación de app WebView"
  - "SDK WebView de Android"
  - "PWA a app"
  - "HTML a app"
  - "puente de JavaScript"
last_updated: "2026-10-09"
---

# API de compras integradas – WebViewGold para Android

> **Resumen:** Venda productos digitales y suscripciones en su aplicación Android WebView con Google Play Billing.

[Documentación](../README.md) › [WebViewGold para Android](README.md) › API de compras integradas

**Plataforma:** Android · **Categoría:** API y funciones · **Versión en línea:** [www.webviewgold.com/es/docs/android/in-app-purchases/](https://www.webviewgold.com/es/docs/android/in-app-purchases/)

---

Dentro de algunas apps, se puede comprar contenido o servicios adicionales. Este tipo de compras se denominan «compras integradas» (in-app purchases). Pueden ser una fuente de ingresos atractiva para los desarrolladores y muy cómodas para los clientes, ya que utilizan las cuentas y los métodos de pago existentes para la liquidación. WebViewGold permite activar las compras integradas de Google Play. Asegúrese de disponer de una [Licencia Extendida](credits.md) de WebViewGold si tiene previsto utilizar esta función en un producto final. ¿Necesita ampliarla? [Aprenda cómo ampliarla aquí](https://help.market.envato.com/hc/en-us/articles/115005593503-If-I-choose-the-wrong-license-or-need-to-upgrade-my-license-how-easy-is-it-to-change-to-the-correct-license).

**Opción 1 (predeterminada): RevenueCat**\
Cree su cuenta gratuita de [RevenueCat](https://tinyurl.com/register-revenuecat) para empezar. La información sobre precios está disponible en su sitio web. Después, configure RevenueCat siguiendo sus asistentes de configuración y su documentación (los detalles de precios están disponibles en su [sitio web](https://tinyurl.com/register-revenuecat)). A continuación, añada sus datos a **Config.java**. Este enfoque también es compatible con el [programa de tarifa de servicio reducida del 15 %](https://support.google.com/googleplay/android-developer/answer/112622?hl=en) de Google Play Store y con el [Small Business Program](https://developer.apple.com/app-store/small-business-program/) de Apple. Si participa en estos programas de tarifa reducida, informe a RevenueCat a través de sus páginas [Apple Small Business Program](https://www.revenuecat.com/docs/platform-resources/apple-platform-resources/app-store-small-business-program) o [tarifa de servicio reducida del 15 % de Google](https://www.revenuecat.com/docs/platform-resources/google-platform-resources/15-reduced-service-fee). Así es como se ve la configuración en Config.java:

```java
public static final String REVENUECAT_API_KEY = "xxxxxxxsxxxxxxxxxxxxxxxxxxxxxxxxxx"; //Your RevenueCat API Key (sign up via tinyurl.com/register-revenuecat first, then follow tinyurl.com/api-key-revenuecat how to find it)
public static final String REVENUECAT_PROJECT_ID = "xxxxxxx"; //Your RevenueCat Project ID (sign up via tinyurl.com/register-revenuecat first, then follow tinyurl.com/project-id-revenuecat how to find it)
```

Asegúrese de que el nombre de paquete de su APK y de Google Play Console coincida con el proyecto configurado en RevenueCat. Active una compra o suscripción utilizando:

```
revenuecat://purchase?external_id=user_123&product=sub_30_days
```

`external_id` = identificador de usuario, p. ej. el correo electrónico de su cliente o su ID de usuario. `product` = ID mostrado en la consola de RevenueCat. Funciona tanto en Android como en iOS.

## Opción 2: Manual (sin RevenueCat)

Nos comprometemos a ayudar a nuestros clientes de WebViewGold a tener éxito, y queremos llamar su atención sobre el programa de tarifa de servicio reducida del 15 % de Google Play Store y el Small Business Program de Apple. Estos programas permiten a los desarrolladores que cumplan los requisitos optar a una comisión del 15 %, una reducción significativa respecto al 30 % estándar. La solicitud es rápida y sencilla, y puede ahorrarle hasta un 50 % en comisiones al **reducir las tasas de comisión de Google y Apple del 30 % al 15 %**. Una vez aprobado, recibirá la tarifa de comisión reducida para todas las apps de pago y las compras integradas que realicen los clientes en las respectivas tiendas. Para obtener más información sobre el programa de Google Play, haga clic **[aquí](https://support.google.com/googleplay/android-developer/answer/112622?hl=en)**, y para el programa de Apple, visite **[aquí](https://developer.apple.com/app-store/small-business-program/)**.

Tras la configuración, para los **productos de compra integrada** simplemente enlace a este tipo de URL:

```html
<a href="inapppurchase://?package=purchase_package_identifier_name_here&disableadmob=true&consumable=true&successful_url=https://www.google.com">Buy In-App Purchase</a>
```

- El «package» es el identificador de producto del artículo que desea vender.
- La «successful_url» es la URL que desea que la app cargue una vez completada la compra.
  - *Quizá desee guardar una cookie en esta página para que su app web recuerde que se ha realizado la compra.*
- Incluya «disableadmob=true» si desea desactivar los anuncios tras la compra del producto.
- Para permitir que se vuelva a cobrar al usuario por el mismo producto de compra integrada (si lo compra de nuevo), establezca el atributo «consumable» en true. Por el contrario, si desea evitar que se vuelva a cobrar al usuario por el mismo producto (si lo compra de nuevo), establezca «consumable» en false u omítalo por completo (ya que false es el valor predeterminado). Asegúrese de utilizar WebViewGold para Android v12.5 o una versión más reciente.

Como alternativa, utilice este tipo de URL para los **productos de suscripción integrada**:

```html
<a href="inappsubscription://?package=purchase_package_identifier_name_here&expired_url=https://www.yahoo.com&successful_url=https://www.google.com">Start In-App Subscription</a>
```

- El «package» es el identificador de producto de la suscripción que desea vender.
- La «successful_url» es la URL que desea que la app cargue una vez completada la compra.
  - *Quizá desee guardar una cookie en esta página para que su app web recuerde que se ha activado la suscripción.*
- La «expired_url» es la URL que desea que la app cargue cuando la suscripción deje de ser válida.
  - *Quizá desee actualizar o eliminar una cookie en esta página para que su app web recuerde que se ha desactivado la suscripción.*

En este ejemplo de URL, https://www.google.com debería llamarse tras la activación correcta de la suscripción, y https://www.yahoo.com debería llamarse en cuanto la suscripción caduque.\
Puede identificar al usuario en el lado del servidor. Por ejemplo, si la página /buy_now.php redirige a la API de compra integrada y esa API redirige a /thanks.php, aún puede acceder a las cookies de usuario/sesión en el servidor e identificar al usuario que acaba de realizar esa compra integrada. En este caso de uso, asegúrese de desactivar CLEAR_CACHE_ON_STARTUP en el archivo Config.java para mantener activadas las cookies del proceso de compra integrada.

**Gestionar/cancelar suscripciones:** WebViewGold para Android puede enlazar directamente a la pantalla de gestión de suscripciones de Play Store: solo tiene que apuntar su enlace a `cancelinapppurchase://`:

```html
<script>
<a href="cancelinapppurchase://">Manage/cancel subscription in Google Play</a>
<script>
```

**Restaurar compras:** WebViewGold para Android ofrece una forma sencilla de restaurar las compras integradas realizadas por los usuarios. Por ejemplo, resulta útil en situaciones en las que los usuarios reinstalan la app o cambian de dispositivo y necesitan recuperar el acceso a su contenido comprado:

```html
<script>
<a href="restoreinapppurchases://">Restore</a>
<script>
```

**Verificación del lado del servidor:** De forma adicional o alternativa, WebViewGold también le permite gestionar los datos de compra o suscripción integrada desde el lado del servidor. Tras una transacción correcta, WebViewGold crea e inyecta en la página web las siguientes variables JavaScript: \
**1. planID:** contiene el ID de producto\
**2. transactionIdentifier:** contiene el ID de transacción único\
**3. subreceipts:** contiene los ID de recibo únicos de las suscripciones del usuario\
Se puede acceder a estas variables directamente en la página web para su almacenamiento y validación en el servidor. Tenga en cuenta que estas variables se inyectan directamente en el objeto global window tras una transacción. Asegúrese de que su JavaScript se ejecute en la misma página donde las variables son accesibles. Añada mecanismos de reserva adecuados si las variables no están disponibles dentro del plazo previsto (como se muestra en la implementación con timeout).
El envío de estas variables a su servidor le permite validar suscripciones y transacciones de forma segura mediante la API de validación de recibos de Apple o el método que elija. A continuación se muestra un ejemplo de implementación en JavaScript:

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

**Precios localizados / obtener la ubicación de la tienda:** El esquema de URL `getstorelocation://` inyecta la ubicación de Play Store en una variable JavaScript. Cuando se llama o se enlaza `getstorelocation://`, el wrapper de WebViewGold obtiene el código de país de Play Store, si está disponible. Como alternativa, considere establecer `autoInjectVariable` en `true` en el archivo de configuración para inyectar automáticamente este valor (y otros) en JavaScript sin necesidad de una llamada a una URL. A continuación, el código de país se inyecta en una variable JavaScript `storeLocation` para su uso posterior por parte de su app web (**p. ej., para mostrar precios localizados**). Si el código no está disponible, `storeLocation` se establecerá en `null`:

- Si tiene éxito (ejemplo, Estados Unidos): `var storeLocation = 'US';`
- Si no se encuentra ningún código de país: `var storeLocation = null;`

Nota: como con cualquier tecnología, es fundamental mencionar que, también al utilizar nuestra API, existe el riesgo de que algunos usuarios (con conocimientos técnicos) puedan acceder al contenido restringido sin pagar por él. Esto podría ocurrir, por ejemplo, al recuperar y abrir directamente el enlace de la Success URL, al desinstalar la app y cancelar después los productos de suscripción para que la Expiration URL nunca se llame (para minimizar este riesgo, puede, por tanto, solicitar reautorizaciones de forma ocasional) o mediante el ejercicio del derecho de desistimiento o los procesos de devolución de cargos de las tarjetas de crédito. No obstante, conviene señalar que algún tipo de riesgo está presente en cualquier enfoque digital. En general, nuestra API es un enfoque práctico y fácil de integrar para entregar contenido de pago a los usuarios de la app, y seguimos trabajando en formas de reducir aún más los riesgos. El uso de nuestra API sigue siendo bajo su propia responsabilidad y sin garantía, pero, en conjunto, aunque es esencial ser consciente del riesgo de acceso no autorizado o no pagado al contenido, las ventajas de utilizar nuestra API superan con creces los riesgos para la mayoría de los usuarios. Se recomienda hacer un seguimiento y comparar los datos de ventas de la Google Play Store Developer Console con las activaciones del lado del servidor de los productos de compra integrada para garantizar informes de ingresos precisos e identificar posibles discrepancias.

---

## Seguir leyendo

- ← Anterior: [API de valoración In-App](in-app-rating.md)
- Siguiente →: [IAP History API](iap-history.md)
- La misma función en otras plataformas: [iOS – API de compras integradas](../ios/in-app-purchases.md) · [macOS – API In-App Purchases](../macos/in-app-purchases.md)
- Idiomas: [🇺🇸 English](../../android/in-app-purchases.md) · [🇩🇪 Deutsch](../../de/android/in-app-purchases.md) · [🇫🇷 Français](../../fr/android/in-app-purchases.md) · **🇪🇸 Español** · [🇨🇳 中文](../../zh/android/in-app-purchases.md)

> [!TIP]
> **¿Sin tiempo? Configuramos su app por usted.** Nuestro equipo configura, compila & publica su app WebViewGold: llave en mano, entrega rápida, Made in Germany. [Configurar mi app →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_android_doc_online)
>
> **Compile en su navegador:** Sin Mac ni IDE: el **WebViewGold Cloud Builder** configura, compila & sube su app en línea. [Descubra Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=android_docs)
