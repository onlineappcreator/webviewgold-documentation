---
title: "API de notificaciones push (OneSignal, Firebase, Pushwoosh) – Documentación de WebViewGold para Android"
description: "Envíe notificaciones push a los usuarios de su aplicación de Android con OneSignal, Firebase o Pushwoosh: configuración, deep links y segmentación por usuario explicados."
lang: "es"
product: "WebViewGold para Android"
platform: "Android"
category: "API y funciones"
slug: "push-notifications"
canonical_url: "https://www.webviewgold.com/es/docs/android/push-notifications/"
keywords:
  - "API de notificaciones push"
  - "WebViewGold para Android"
  - "convertir sitio web en app"
  - "documentación de app WebView"
  - "SDK WebView de Android"
  - "PWA a app"
  - "HTML a app"
  - "puente de JavaScript"
last_updated: "2026-10-09"
---

# API de notificaciones push (OneSignal, Firebase, Pushwoosh) – WebViewGold para Android

> **Resumen:** Envíe notificaciones push a los usuarios de su aplicación de Android con OneSignal, Firebase o Pushwoosh: configuración, deep links y segmentación por usuario explicados.

[Documentación](../README.md) › [WebViewGold para Android](README.md) › API de notificaciones push

**Plataforma:** Android · **Categoría:** API y funciones · **Versión en línea:** [www.webviewgold.com/es/docs/android/push-notifications/](https://www.webviewgold.com/es/docs/android/push-notifications/)

---

Las notificaciones push son notificaciones que aparecen en su smartphone sin necesidad de abrir la aplicación. Este tipo de mensajes permite una interacción fantástica con los clientes y usuarios de la app. Su aplicación no tiene que estar abierta. De esta forma, sus clientes no se pierden ninguna noticia o mensaje importante. Las notificaciones push son adecuadas para muchos casos de uso, por ejemplo, actualizaciones de pedidos, live tickers o comunidades en redes sociales. Debe existir una conexión a Internet para que los usuarios de la app puedan recibir mensajes push. WebViewGold admite múltiples formas de llegar a sus usuarios mediante notificaciones push.

## Opción 1: Usar la API de JavaScript para notificaciones push locales

Puede insertar un fragmento de código (JavaScript) en su sitio web para definir una notificación push que puede mostrarse **después** de que su app se haya cerrado (programándola mientras la app está abierta). Esto funciona sin ninguna configuración de OneSignal.

```html
<script>
var title = "Your cart is waiting!"; //notification title
var message = "You have left a cart full of dreams and deals behind. Dont leave it feeling abandoned"; //notification message
var seconds = 120; //seconds from now on
var url = "https://myshop.org/cart.php"; //deep-linking URL

window.location.href = "sendlocalpushmsg://push.send?s="+ seconds +"=msg!"+ message +"&!#"+ title +"&!#"+ url +"";
</script>
```

Esto puede utilizarse en distintas situaciones (cuentas atrás, happy hours (como en el código de ejemplo), recordatorios, ...).\
Para cancelar todas las notificaciones push locales programadas, ejecute:

```html
<script>
window.location.href = "sendlocalpushmsg://push.send.cancel";
</script>
```

## Opción 2: Usar notificaciones push remotas de Pushwoosh

**¡Los usuarios de WebViewGold pueden disfrutar de dos meses gratis de Pushwoosh!**\
Para aprovechar esta oferta, envíe su licencia de WebViewGold por correo electrónico a [pushwoosh-love@webviewgold.com](mailto:pushwoosh-love@webviewgold.com) y recibirá pronto una respuesta personalizada.

Si desea utilizar [Pushwoosh](https://www.pushwoosh.com) (¡una excelente elección!) para las notificaciones push en su app, simplemente active las opciones en **Config.java** estableciendo **PUSHWOOSH_ENABLED** en **true**, y asegúrese de actualizar también los **Pushwoosh IDs** en los archivos **string.xml** y **AndroidManifest.xml** con sus propios Pushwoosh IDs:\
![Envíe una nueva notificación push a los usuarios de su app con Pushwoosh](../../assets/android/img/pushwoosh1.webp)\
![Envíe una nueva notificación push a los usuarios de su app con Pushwoosh](../../assets/android/img/pushwoosh2a.webp)\
![Envíe una nueva notificación push a los usuarios de su app con Pushwoosh](../../assets/android/img/pushwoosh2b.webp)

Felicidades, su configuración ya está completa. Ahora está listo para enviar notificaciones push:\
[![Envíe una nueva notificación push a los usuarios de su app con Pushwoosh](../../assets/android/img/pushwoosh3.webp)](https://www.pushwoosh.com)\
¿Desea obtener **el ID de dispositivo individual de cada usuario** para notificaciones push personalizadas o para un procesamiento adicional? Simplemente establezca **WONDERPUSH_ENHANCE_WEBVIEW_URL** en **true** en **Config.java** para añadir ?pushwoosh_id=XYZ a la URL de su WebView:\
![Envíe una nueva notificación push a los usuarios de su app con Pushwoosh](../../assets/android/img/pushwoosh4.webp)\
Por ejemplo, si la URL de su WebView es https://www.example.org, WebViewGold llamará a https://www.example.org?pushwoosh_id=XYZ en su lugar. Recuerde que solo la primera solicitud de URL recibirá esta variable GET, por lo que le recomendamos guardarla en una sesión o en una cookie para su uso posterior dentro de sus páginas enlazadas. Como alternativa o de forma adicional, puede **recuperar y procesar esta información en cualquier página mediante JavaScript**:

```html
<script>
window.location.href = "getpushwooshid://";
alert(pushwooshplayerid);
</script>
```

## Opción 3: Usar notificaciones push remotas de OneSignal

Si desea utilizar OneSignal para configurar notificaciones push remotas, este video tutorial le guiará paso a paso durante el proceso.

[![Ver el vídeo: API de notificaciones push (OneSignal, Firebase, Pushwoosh)](https://img.youtube.com/vi/0cPNGqMQVm0/hqdefault.jpg)](https://www.youtube.com/watch?v=0cPNGqMQVm0)

Tras completar este video tutorial, podrá configurar fácilmente notificaciones push remotas para su aplicación móvil utilizando OneSignal. Esto le permitirá enviar actualizaciones importantes, recordatorios o contenido promocional directamente a los dispositivos de sus usuarios, incluso si no están usando su app en ese momento.

En resumen, el proceso para configurar OneSignal para notificaciones push es el siguiente:

1. Vaya a Android Studio y localice las opciones de OneSignal. De forma predeterminada, PUSH_ENABLE, PUSH_ENHANCE_WEBVIEW_URL y PUSH_RELOAD_ON_USERID aparecen como false; cámbielos a true.
2. Abra su cuenta de OneSignal y seleccione su organización y el nombre de su app.

***Si aún no ha creado su app en el proyecto de OneSignal, siga primero estos pasos.***

[![Ver el vídeo: API de notificaciones push (OneSignal, Firebase, Pushwoosh)](https://img.youtube.com/vi/X9jepbGFw7A/hqdefault.jpg)](https://www.youtube.com/watch?v=X9jepbGFw7A)

***Tenga en cuenta que para crear y configurar su cuenta de OneSignal necesitará un archivo JSON. Para obtener este archivo debe tener configurada su cuenta de Firebase. Si aún no ha configurado Firebase para obtener el archivo JSON, consulte este tutorial adicional.***

[![Ver el vídeo: API de notificaciones push (OneSignal, Firebase, Pushwoosh)](https://img.youtube.com/vi/qAqdhcd3ngs/hqdefault.jpg)](https://www.youtube.com/watch?v=qAqdhcd3ngs)

- Una vez creada su app de OneSignal, vaya a la sección de configuración, seleccione Native Android como plataforma y luego copie el código de App ID obtenido.
- Abra Android Studio y vaya a la sección Gradle Scripts y seleccione build.gradle (Module:app).
- En la sección ONE_SIGNAL_APP_ID, pegue el código que había copiado de OneSignal.
- A continuación, genere su archivo *APK* y ejecútelo en un dispositivo físico.
- Vaya a OneSignal y en su proyecto de app seleccione *New Message* y haga clic en *New Push*.
- Complete la información requerida y ¡listo! Ha probado con éxito sus mensajes push de OneSignal.

Reemplace **ic_stat_onesignal_default.png** para sustituir el **icono de campana predeterminado** de las notificaciones push de OneSignal. \
¿Desea obtener **el ID de suscripción individual de cada usuario** en su servidor para un procesamiento posterior y para mensajes push a **<a id="firebaseruntime"></a>usuarios individuales**? Simplemente active la opción **PUSH_ENHANCE_WEBVIEW_URL** en Config.java (cambiando el valor de false a true) para añadir ?onesignal_push_id=XYZ a la URL de su WebView. Si la URL de su WebView es https://www.example.org, WebViewGold llamará a https://www.example.org?onesignal_push_id=XYZ en su lugar. Solo la PRIMERA solicitud de URL recibirá esta variable GET, así que guárdela en una sesión o en una cookie para acceder a ella en sus páginas enlazadas. Una alternativa o forma adicional es **recuperar y procesar la información en cualquier página mediante JavaScript**:

```html
<script>
window.location.href = "getonesignalplayerid://";
alert(onesignalplayerid);
</script>
```

**Como alternativa, considere establecer  `AUTO_INJECT_VARIABLES`  en `true` en Config.java para inyectar automáticamente este (y otros) valores en JavaScript sin necesidad de llamar a una URL previamente.**

## Opción 4: Usar notificaciones push remotas de Firebase

Si desea utilizar Firebase para configurar notificaciones push remotas, este video tutorial le guiará paso a paso durante el proceso.

[![Ver el vídeo: API de notificaciones push (OneSignal, Firebase, Pushwoosh)](https://img.youtube.com/vi/X-02iJSBaAQ/hqdefault.jpg)](https://www.youtube.com/watch?v=X-02iJSBaAQ)

En resumen, el proceso para configurar Firebase para notificaciones push es el siguiente:

### 1. Renombrar el nombre del paquete y crear un proyecto de Firebase

Por favor, [renombre el nombre del paquete](publish.md#renamepackagename) de su app WebViewGold para Android. A continuación, debe crear un proyecto de Firebase en su [Consola de Firebase](https://console.firebase.google.com/).

### 2. Activar Firebase en WebViewGold

En Android Studio, abra el archivo Config.java y establezca la variable **FIREBASE_PUSH_ENABLED** en **true**.

![Reemplace google-services.json en su app WebViewGold para Android](../../assets/android/img/firebase2.webp)

### 3. Registrar su app en Firebase

Después de crear su proyecto de Firebase, puede añadir su app WebViewGold.

a. En el centro de la página de resumen del proyecto de la consola de Firebase, haga clic en el icono de Android para iniciar el flujo de configuración.

b. Si ya ha añadido una app a su proyecto de Firebase, haga clic en **Añadir app** para mostrar las opciones de plataforma.
Introduzca el nombre del paquete de su app tal como se cambió/definió [en este paso](publish.md).
Asegúrese de introducir el nombre del paquete que utiliza su app. No podrá añadir ni modificar este valor después de registrar su app en su proyecto de Firebase.\
**4. Haga clic en el botón *Registrar app*.**
**5. Descargar google-services.json**
Haga clic en Descargar google-services.json para obtener su archivo de configuración de Firebase para Android (google-services.json) y reemplace el archivo de ejemplo ya incluido en el proyecto WebViewGold utilizando el Finder de Mac o el Explorador de Windows:\
![Reemplace google-services.json en su app WebViewGold para Android](../../assets/android/img/firebase1.webp)\
 **¡Eso es todo!**\
Si desea utilizar el URL Deeplinking de Firebase (abre una URL específica al hacer clic en su notificación), añada la URL deseada en un campo **Custom Data** (en la sección **Additional options (optional)**) con **Key** = "url" y **Value** = {la URL deseada}.\
![Añadir una URL personalizada para propósitos de deeplinking en el WebView](../../assets/android/img/firebase_deeplinking.webp)\
¿Desea obtener **el ID de suscripción individual de cada usuario** en su servidor para un procesamiento posterior y para mensajes push a **usuarios individuales**? Simplemente active la opción **FIREBASE_PUSH_ENHANCE_WEBVIEW_URL** en Config.java (cambiando el valor de false a true) para añadir ?firebase_push_id=XYZ a la URL de su WebView. Si la URL de su WebView es https://www.example.org, WebViewGold llamará a https://www.example.org?firebase_push_id=XYZ en su lugar. Solo la PRIMERA solicitud de URL recibirá esta variable GET, así que guárdela en una sesión o en una cookie para acceder a ella en sus páginas enlazadas. Una alternativa o forma adicional es **recuperar y procesar la información en cualquier página mediante JavaScript**:

```html
<script>
window.location.href = "getfirebaseplayerid://";
alert(firebaseplayerid);
</script>
```

**Como alternativa, considere establecer  `AUTO_INJECT_VARIABLES`  en `true` en Config.java para inyectar automáticamente este (y otros) valores en JavaScript sin necesidad de llamar a una URL previamente.**

## Opción 5: Usar notificaciones push de bubble.io

[![Ver el vídeo: API de notificaciones push (OneSignal, Firebase, Pushwoosh)](https://img.youtube.com/vi/C0HBXlMSK2E/hqdefault.jpg)](https://www.youtube.com/watch?v=C0HBXlMSK2E)

1. Cree una **app de bubble.io**
2. Instale el plugin **[WebViewGold OneSignal Push](https://bubble.io/plugin/webviewgold-onesignal-push-1602240916803x713805488222896100)**:

[![Plugin bubble.io WebViewGold OneSignal Push](../../assets/android/img/bubblepushplugin-2048x724.webp)](https://bubble.io/plugin/webviewgold-onesignal-push-1602240916803x713805488222896100)
3. Siga las **instrucciones de OneSignal (véase arriba)** y las **instrucciones del plugin (véase [aquí](https://bubble.io/plugin/webviewgold-onesignal-push-1602240916803x713805488222896100) y [aquí](https://www.youtube.com/watch?v=C0HBXlMSK2E))**.

---

## APIs de permiso de push: Preguntar en el momento adecuado y comprobar el estado actual

### Solicitar manualmente el permiso de notificaciones push (`registerpush://`)

De forma predeterminada, WebViewGold solicita al usuario el permiso de notificaciones push en el primer inicio de la aplicación (`requirePush = true` en **Config.java**). Las solicitudes de permiso convierten mucho mejor cuando aparecen en el contexto adecuado — por eso también puede establecer `requirePush` en `false` y activar el diálogo nativo de permiso desde su web app en el momento perfecto (p. ej., tras el inicio de sesión o el onboarding):

```html
<a href="registerpush://">Activar notificaciones</a>
```

```javascript
window.location.href = "registerpush://";
```

**Nota:** Esto requiere que al menos un servicio de push esté activado en **Config.java** (`PUSH_ENABLED`, `FIREBASE_PUSH_ENABLED` o `PUSHWOOSH_ENABLED`).

### Comprobar el estado actual del permiso de push (`checkNativePushPermissions://`)

Para saber si el usuario permite actualmente las notificaciones push, llame a:

```javascript
window.location.href = "checkNativePushPermissions://";
```

WebViewGold inyecta entonces la variable JavaScript `nativePushEnabled` (`true` o `false`) en su página. En Android 13 y superior, tanto el ajuste de notificaciones del sistema como el permiso de ejecución `POST_NOTIFICATIONS` deben estar concedidos para que el valor sea `true`. Ejemplo:

```html
<script>
window.location.href = "checkNativePushPermissions://";
setTimeout(function () {
    if (typeof nativePushEnabled !== "undefined" && nativePushEnabled) {
        console.log("Las notificaciones push están activadas");
    } else {
        // p. ej., mostrar su propio aviso y ofrecer registerpush:// o settingsapp://
    }
}, 500);
</script>
```

Si el permiso fue denegado de forma permanente, puede guiar al usuario a los ajustes del sistema mediante la [API Open App Settings](open-app-settings.md) (`settingsapp://`).

---

## Seguir leyendo

- ← Anterior: [API de geolocalización](geolocation.md)
- Siguiente →: [API de anuncios AdMob](admob.md)
- La misma función en otras plataformas: [iOS – API de notificaciones push](../ios/push-notifications.md)
- Idiomas: [🇺🇸 English](../../android/push-notifications.md) · [🇩🇪 Deutsch](../../de/android/push-notifications.md) · [🇫🇷 Français](../../fr/android/push-notifications.md) · **🇪🇸 Español** · [🇨🇳 中文](../../zh/android/push-notifications.md)

> [!TIP]
> **¿Sin tiempo? Configuramos su app por usted.** Nuestro equipo configura, compila & publica su app WebViewGold: llave en mano, entrega rápida, Made in Germany. [Configurar mi app →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_android_doc_online)
>
> **Compile en su navegador:** Sin Mac ni IDE: el **WebViewGold Cloud Builder** configura, compila & sube su app en línea. [Descubra Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=android_docs)
