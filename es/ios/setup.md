---
title: "Instalar y configurar WebViewGold para iOS – Documentación de WebViewGold para iOS"
description: "Descargue la plantilla de Xcode de WebViewGold, inserte su URL en Config.swift y explore todas las opciones de configuración integradas, sin necesidad de saber programar."
lang: "es"
product: "WebViewGold para iOS"
platform: "iOS"
category: "Primeros pasos"
slug: "setup"
canonical_url: "https://www.webviewgold.com/es/docs/iOS/setup/"
keywords:
  - "Configurar WebViewGold"
  - "WebViewGold para iOS"
  - "convertir sitio web en app"
  - "documentación de app WebView"
  - "SDK WebView de iOS"
  - "PWA a app"
  - "HTML a app"
  - "puente de JavaScript"
last_updated: "2026-10-09"
---

# Instalar y configurar WebViewGold para iOS – WebViewGold para iOS

> **Resumen:** Descargue la plantilla de Xcode de WebViewGold, inserte su URL en Config.swift y explore todas las opciones de configuración integradas, sin necesidad de saber programar.

[Documentación](../README.md) › [WebViewGold para iOS](README.md) › Configurar WebViewGold

**Plataforma:** iOS · **Categoría:** Primeros pasos · **Versión en línea:** [www.webviewgold.com/es/docs/iOS/setup/](https://www.webviewgold.com/es/docs/iOS/setup/)

---

**Descargue** la plantilla de aplicación WebViewGold para iOS **[aquí](https://www.webviewgold.com/download/ios)**.\
[![Compre la plantilla de aplicación WebView para iOS/Xcode](../../assets/ios/img/cart.webp)](https://www.webviewgold.com/download/ios)

> [!NOTE]
> ¿Prefiere evitar instalar software? Con el [**WebViewGold Cloud Builder**](https://www.webviewgold.com/cloud-builder?ref=ios_docs) (complemento de pago) puede configurar, compilar y subir su aplicación directamente desde el navegador, sin necesidad de abrir Xcode.
>
> [![Ver el vídeo: Instalar y configurar WebViewGold para iOS](https://img.youtube.com/vi/nzgCkydN9OM/hqdefault.jpg)](https://www.youtube.com/watch?v=nzgCkydN9OM)

Después de descargar el archivo .zip de WebViewGold desde CodeCanyon, existen **dos opciones de configuración** para Xcode. Cuál de ellas debe utilizar depende de si dispone de un sistema Mac:

**a) No utiliza ningún sistema Mac:**\
Si no dispone de un Mac para ejecutar la aplicación Xcode necesaria, consulte [MacInCloud](https://www.macincloud.com), un servicio que le permite alquilar un Mac virtual en línea (no estamos afiliados al proveedor de este servicio). Con este servicio podrá compilar sus aplicaciones iOS basadas en WebViewGold incluso sin usar un Mac. Además, el [**WebViewGold Cloud Builder**](https://www.webviewgold.com/cloud-builder?ref=ios_docs) (complemento de pago) le permite configurar, compilar y subir su aplicación directamente desde su navegador sin necesidad de un Mac. \
**O**\
**b) Utiliza un sistema Mac:**\
Descargue e instale la aplicación **Xcode** desde la [**Mac App Store**](https://apps.apple.com/de/app/xcode/id497799835?mt=12). WebViewGold se ejecuta de forma nativa tanto en Macs con Intel como con Apple Silicon, por lo que puede compilar y probar su aplicación directamente con el simulador de iOS estándar.

**¡Listo, Xcode está preparado para WebViewGold!**\
Si ya tiene Xcode en ejecución, ciérrelo por completo (*Comando/CMD* + *Q*). Después, abra **WebViewGold.xcworkspace** (en lugar de WebView.xcodeproj):\
![Asegúrese de seleccionar el archivo de proyecto WebView correcto al abrir el proyecto de Xcode](../../assets/ios/img/file.webp)

Dentro de [Xcode](https://developer.apple.com/xcode/), abra **Config.swift** y verá un documento como este:\
![La configuración es sencilla gracias al archivo Config.swift](../../assets/ios/img/Configswift-img.webp)\
Aquí puede configurar su aplicación fácilmente. Configurar aplicaciones con WebViewGold es **muy sencillo** y no requiere conocimientos de programación. No olvide añadir su [Código de compra de Envato/CodeCanyon](https://help.market.envato.com/hc/en-us/articles/202822600-Where-Is-My-Purchase-Code-) en el campo **purchasecode** para cada aplicación que publique. Se requiere una licencia por cada producto final personalizado. Información sobre la licencia de su compra en CodeCanyon: [https://codecanyon.net/licenses/standard](https://codecanyon.net/licenses/standard?ref=onlineappcreator)

Consulte esta **visión general** de todas las opciones de configuración integradas:

[![Ver el vídeo: Instalar y configurar WebViewGold para iOS](https://img.youtube.com/vi/E4D-Q_FhEOM/hqdefault.jpg)](https://www.youtube.com/watch?v=E4D-Q_FhEOM)

| Ajuste | Valor | Descripción |
| --- | --- | --- |
| purchasecode | **valor obligatorio** | Introduzca su Código de compra de Envato/CodeCanyon para esta aplicación |
| app_admin_email | opcional | Dirección de correo electrónico para recibir actualizaciones de estado (deje el valor predeterminado para desactivarlo) |
| host | **valor obligatorio** | El host de su dominio (por ejemplo, "example.org"). De forma predeterminada, WebViewGold para iOS permite tanto contenido HTTPS como HTTP. Sin embargo, si prefiere reforzar la seguridad de la aplicación permitiendo únicamente contenido HTTPS, puede [modificar esta configuración](https://www.webviewgold.com/support-center/knowledgebase/how-to-prevent-non-https-connections-in-webviewgold-for-ios-removing-nsallowsarbitraryloadsinwebcontent-from-info-plist/) (y/o considerar la opción 'blockfaultyandselfsignedhttpscerts') |
| webviewurl | **valor obligatorio** | La URL completa de su WebView (por ejemplo, "example.org/app.html") que debe cargarse en el WebView. De forma predeterminada, WebViewGold para iOS permite tanto contenido HTTPS como HTTP. Sin embargo, si prefiere reforzar la seguridad de la aplicación permitiendo únicamente contenido HTTPS, puede [modificar esta configuración](https://www.webviewgold.com/support-center/knowledgebase/how-to-prevent-non-https-connections-in-webviewgold-for-ios-removing-nsallowsarbitraryloadsinwebcontent-from-info-plist/) (y/o considerar la opción 'blockfaultyandselfsignedhttpscerts') |
| uselocalhtmlfolder | **true** o **false** | Establezca en *true* para utilizar el archivo HTML local "local-www/index.html" en lugar de la URL remota del WebView (asegúrese de no crear ni utilizar subcarpetas dentro de local-www) |
| externalLinkHandlingOptions | **0**, **1** o **2** | Establézcalo en *0* para abrir los enlaces externos dentro de la aplicación de forma predeterminada, o en *2* para abrirlos SIEMPRE en otro navegador (Safari); consulte la [API de gestión de URL](url-handling.md) |
| specialLinkHandlingOptions | **0**, **1** o **2** | Establézcalo en *0* para abrir los enlaces especiales (p. ej., target="_blank") dentro de la aplicación, en *1* para abrirlos en una pestaña nueva (un navegador integrado adicional) o en *2* para abrirlos en otro navegador (Safari) |
| safariwhitelist | Lista | Añada aquí los dominios que **siempre** deban abrirse en Safari, independientemente del valor de la opción **externalLinkHandlingOptions**; para añadir otro dominio, inserte otro host de esta manera: ["alwaysopeninsafari.com", "google.com", "m.facebook.com"]. Introduzca el host exactamente como lo enlaza (con o sin www, pero siempre sin http/https). |
| safariblacklist | Lista | Añada aquí los dominios que **nunca** deban abrirse en Safari, independientemente del valor de la opción **externalLinkHandlingOptions**; para añadir otro dominio, inserte otro host de esta manera: ["alwaysopeninsafari.com", "google.com", "m.facebook.com"]. Introduzca el host exactamente como lo enlaza (con o sin www, pero siempre sin http/https). |
| alwaysOpenInInAppTab | Lista | Añada aquí los dominios que deben abrirse **siempre** en una pestaña integrada, independientemente del valor de la opción **externalLinkHandlingOptions** |
| neverOpenInInAppTab | Lista | Añada aquí los dominios que **nunca** deben abrirse en una pestaña integrada, independientemente del valor de la opción **externalLinkHandlingOptions** |
| enableBioMetricAuth | **true** o **false** | Establezca en *true* para activar la función de Bloqueo de la aplicación, que requiere autenticación mediante Face ID, Touch ID o código para acceder a la aplicación. Se trata de una opción independiente y adicional a nuestra [API de autenticación biométrica](biometric-authentication.md) basada en JavaScript |
| autoInjectVariable | **true** o **false** | Establezca en *true* para cargar automáticamente variables JavaScript (por ejemplo, UUID, versión de la aplicación, IDs de suscripción de OneSignal y Firebase, y ubicación en App Store) sin necesidad de invocar URLs específicas como get-uuid:// (actualmente se admiten la versión de la aplicación, los IDs de suscripción de OneSignal y Firebase, el UUID y la ubicación en App Store) |
| disablecallout | **true** o **false** | Establezca en *true* para eliminar la ventana de vista previa/llamada de enlace 3D Touch de WKWebView para los enlaces (recomendado en la mayoría de los casos) |
| deletecache | **true** o **false** | Establezca en *true* para vaciar la caché y las cookies del WebView en cada inicio de la aplicación y no utilizar versiones en caché de su aplicación web/sitio web |
| deletecacheonexit | **true** o **false** | Establezca en *true* para vaciar la caché y las cookies del WebView al cerrar por completo la aplicación (también puede convenirle activar *deletecache*, ya que las diferencias entre versiones de iOS pueden afectar a la fiabilidad) |
| okbutton | opcional | Establezca la etiqueta de texto de los botones "OK" (traducible mediante *alternatelanguage1*/*alternatelanguage2*) |
| cancelbutton | opcional | Establezca la etiqueta de texto de los botones "Cancelar" (traducible mediante *alternatelanguage1*/*alternatelanguage2*) |
| bigstatusbar | **true** o **false** | Establezca en *true* para ampliar el tamaño de la barra de estado |
| hideverticalscrollbar | **true** o **false** | Establezca en *true* para ocultar la barra de desplazamiento vertical |
| hidehorizontalscrollbar | **true** o **false** | Establezca en *true* para ocultar la barra de desplazamiento horizontal |
| enableswipenavigation | **true** o **false** | Establezca en *false* para evitar que los deslizamientos hacia la izquierda o la derecha activen la navegación hacia atrás o adelante |
| orientationiphone | "portrait", "landscape" o "auto" | Establezca la orientación en iPhone en portrait, landscape o auto |
| orientationipad | "portrait", "landscape" o "auto" | Establezca la orientación en iPad en portrait, landscape o auto |
| preventsleep | **true** o **false** | Establezca en *true* para evitar que el dispositivo entre en modo de suspensión mientras la aplicación esté activa |
| preventZoom | **true** o **false** | Establezca en *true* para desactivar el zoom del usuario inyectando código que impide el zoom en el sitio web |
| preventoverscroll | **true** o **false** | Establezca en *true* para eliminar la animación de rebote de WKWebView (recomendado en la mayoría de los casos). Establezca en *false* si utiliza pull to refresh. |
| enhanceUrlUUID | **true** o **false** | Establezca en *true* para añadir el parámetro UUID 'uuid=XYZ' a la primera solicitud de URL |
| linkDragAndDrop | **true** o **false** | Establezca en *false* para desactivar el arrastrar y soltar de enlaces |
| useShortcuts | **true** o **false** | Establezca en *true* para registrar los accesos directos dinámicos definidos en Shortcuts.json |
| pulltorefresh | **true** o **false** | Establezca en *true* para habilitar pull to refresh en su aplicación. Tenga en cuenta que para activar esta función, **preventoverscroll** debe estar establecido en *false*. Además, puede llamar en cualquier momento a `enablepulltorefresh://` o `disablepulltorefresh://` desde su sitio web para activar o desactivar dinámicamente pull-to-refresh. |
| pulltorefresh_loadingsigncolour_lightmode | Color | Establezca el color del indicador de carga de pull to refresh en modo claro |
| pulltorefresh_backgroundcolour_lightmode | Color | Establezca el color del fondo de pull to refresh en modo claro |
| pulltorefresh_loadingsigncolour_darkmode | Color | Establezca el color del indicador de carga de pull to refresh en modo oscuro; requiere iOS 13 o superior |
| pulltorefresh_backgroundcolour_darkmode | Color | Establezca el color del fondo de pull to refresh en modo oscuro; requiere iOS 13 o superior |
| useragent_iphone | opcional | Defina un UserAgent personalizado en iPhone (o déjelo vacío para utilizar el UserAgent predeterminado de iOS) |
| useragent_ipad | opcional | Defina un UserAgent personalizado en iPad (o déjelo vacío para utilizar el UserAgent predeterminado de iOS) |
| google_login_helper_triggers | opcional | Defina los prefijos de URL que se cargan durante el inicio de sesión con Google en su sitio web; actúan como disparador para el asistente; Ejemplo: ["https://accounts.google.com", "https://accounts.youtube.com"] |
| facebook_login_helper_triggers | opcional | Defina los prefijos de URL que se cargan durante el inicio de sesión con Facebook en su sitio web; actúan como disparador para el asistente; Ejemplo: ["https://www.facebook.com", "https://m.facebook.com"] |
| activatefirstrundialog | **true** o **false** | Establezca en *true* para activar el diálogo "Primer inicio" |
| firstrunmessagetitle | opcional | Establezca la etiqueta del título del diálogo "Primer inicio" (si lo desea, puede traducir esta cadena a dos idiomas adicionales usando las cadenas 'alternatelanguage1' y 'alternatelanguage2' que se encuentran al final del archivo Config.swift) |
| firstrunmessage | opcional | Establezca el mensaje del diálogo "Primer inicio" (si lo desea, puede traducir esta cadena a dos idiomas adicionales usando las cadenas 'alternatelanguage1' y 'alternatelanguage2' que se encuentran al final del archivo Config.swift) |
| askforpushpermissionatfirstrun | **true** o **false** | Establezca en *true* para pedir permiso a sus usuarios para las notificaciones push en el primer inicio de la aplicación. Establézcalo en "false" para no pedirlo nunca o para solicitarlo más tarde en su aplicación web mediante un enlace/botón/redirección *registerpush://* |
| offlinetitle | opcional | Establezca la etiqueta del título del diálogo Offline (si lo desea, puede traducir esta cadena a dos idiomas adicionales usando las cadenas 'alternatelanguage1' y 'alternatelanguage2' que se encuentran al final del archivo Config.swift) |
| offlinemsg | opcional | Establezca el texto del diálogo Offline (si lo desea, puede traducir esta cadena a dos idiomas adicionales usando las cadenas 'alternatelanguage1' y 'alternatelanguage2' que se encuentran al final del archivo Config.swift) |
| screen1 | opcional | Establezca la etiqueta de texto 1 de la pantalla Offline (si lo desea, puede traducir esta cadena a dos idiomas adicionales usando las cadenas 'alternatelanguage1' y 'alternatelanguage2' que se encuentran al final del archivo Config.swift) |
| screen2 | opcional | Establezca la etiqueta de texto 2 de la pantalla Offline (si lo desea, puede traducir esta cadena a dos idiomas adicionales usando las cadenas 'alternatelanguage1' y 'alternatelanguage2' que se encuentran al final del archivo Config.swift) |
| offlinebuttontext | opcional | Establezca la etiqueta de texto del botón Reintentar (si lo desea, puede traducir esta cadena a dos idiomas adicionales usando las cadenas 'alternatelanguage1' y 'alternatelanguage2' que se encuentran al final del archivo Config.swift) |
| offlinescreenautoretry | **true** o **false** | Establezca en *true* si la aplicación debe intentar reconectarse automáticamente cada segundo (incluso sin pulsar el botón) |
| activateratemyappdialog | **true** o **false** | Establezca en *true* para activar el diálogo "Valorar esta aplicación en App Store" |
| activatefacebookfriendsdialog | **true** o **false** | Establezca en *true* para activar el diálogo "Seguir en Facebook" |
| becomefacebookfriendstitle | opcional | Establezca la etiqueta del título del diálogo "Seguir en Facebook" (si lo desea, puede traducir esta cadena a dos idiomas adicionales usando las cadenas 'alternatelanguage1' y 'alternatelanguage2' que se encuentran al final del archivo Config.swift) |
| becomefacebookfriendstext | opcional | Establezca la etiqueta de texto del diálogo "Seguir en Facebook" (si lo desea, puede traducir esta cadena a dos idiomas adicionales usando las cadenas 'alternatelanguage1' y 'alternatelanguage2' que se encuentran al final del archivo Config.swift) |
| becomefacebookfriendsyes | opcional | Establezca la etiqueta de texto del botón "Sí" del diálogo "Seguir en Facebook" (si lo desea, puede traducir esta cadena a dos idiomas adicionales usando las cadenas 'alternatelanguage1' y 'alternatelanguage2' que se encuentran al final del archivo Config.swift) |
| becomefacebookfriendsno | opcional | Establezca la etiqueta de texto del botón "No" del diálogo "Seguir en Facebook" (si lo desea, puede traducir esta cadena a dos idiomas adicionales usando las cadenas 'alternatelanguage1' y 'alternatelanguage2' que se encuentran al final del archivo Config.swift) |
| becomefacebookfriendsurl | opcional | Establezca la URL de su página de Facebook/Instagram/YouTube/... (por ejemplo, "https://facebook.com/OnlineAppCreator/") |
| imagedownloadedtitle | opcional | Establezca la etiqueta del título del cuadro de diálogo "Imagen guardada en su galería de fotos" (si lo desea, puede traducir esta cadena a dos idiomas adicionales usando las cadenas 'alternatelanguage1' y 'alternatelanguage2' que se encuentran al final del archivo Config.swift) |
| imagenotfound | opcional | Establezca la etiqueta del título del cuadro de diálogo "No se encontró la imagen" (si lo desea, puede traducir esta cadena a dos idiomas adicionales usando las cadenas 'alternatelanguage1' y 'alternatelanguage2' que se encuentran al final del archivo Config.swift) |
| transparentStatusBar | **true** o **false** | Establezca en *true* para que la barra de estado sea transparente, permitiendo que el contenido web se represente detrás de ella |
| autoAdjustSafeAreaInsets | **true** o **false** | Establezca en *false* si su sitio web ya gestiona los márgenes de las áreas seguras (utilícese con *transparentStatusBar*) |
| statusBarBackgroundColor | Color | Defina un color de fondo personalizado para la barra de estado |
| darkModeStatusBarBackgroundColor | Color | Defina un color de fondo personalizado para la barra de estado cuando el usuario esté utilizando el modo oscuro de iOS |
| statusBarTextColor | **white** o **black** | Defina el color del texto de la barra de estado |
| darkModeStatusBarTextColor | **white** o **black** | Defina el color del texto de la barra de estado cuando el usuario esté utilizando el modo oscuro de iOS |
| showNavFooter | **true** o **false** | Establezca en *true* para activar la barra de pie de navegación nativa (configurada mediante FooterBar.json) |
| bottombar | **true** o **false** | Establezca en *true* para activar la bottombar y evitar que la barra de inicio (presente en dispositivos iOS sin botón de inicio, por ejemplo, el iPhone X) se superponga al contenido de la aplicación |
| iPadBottombar | **true** o **false** | Establezca en *true* para activar TAMBIÉN la bottombar en iPads (que, al tener pantallas más grandes, es posible que la barra de inicio no se superponga al contenido debido a un diseño distinto, por lo que la bottombar podría no ser necesaria) |
| bottombarBackgroundColor | Color | Defina un color de fondo personalizado para la bottombar |
| darkmodeBottombarBackgroundColor | Color | Defina un color de fondo personalizado para la bottombar cuando el usuario esté utilizando el modo oscuro de iOS; requiere iOS 13 o superior |
| qrcodelinks | **0** o **1** o **2** o **3** o **4** | Establezca en (0) para abrir una URL escaneada de un código QR en la aplicación; (1) en una pestaña integrada en la aplicación; (2) en un nuevo navegador; (3) en una pestaña integrada en la aplicación si es externa; (4) en un nuevo navegador si es externa; además, opcionalmente puede limitar los prefijos permitidos del escáner de códigos QR en el array "allowedQRurls" del archivo SwiftQRScanner.swift |
| ShowExternalLink | opcional | Establezca en *true* para abrir los enlaces enviados a través de la [API de Universal Links](universal-links.md) (sintaxis: https://example.org) y de la [API de Deep Linking](deep-linking.md) (sintaxis: example://url?link=https://example.org). |
| splashScreenEnabled | opcional | Establezca en *false* si desea desactivar la pantalla de inicio mientras se lanza la aplicación y mostrar el indicador de carga en su lugar |
| remainSplashOption | opcional | Establezca en *true* si desea mostrar la pantalla de inicio hasta que se haya completado la carga inicial de su página de inicio (en lugar del indicador de carga) |
| splashTimeout | valor numérico (milisegundos) | Establezca el tiempo de espera de la pantalla de inicio en *milisegundos* (la pantalla del indicador de carga se mostrará una vez transcurrido este tiempo si la URL de inicio aún tiene contenido pendiente de cargarse) |
| splashMinTime | valor numérico (milisegundos) | Tiempo mínimo (en milisegundos) que debe mostrarse la pantalla de bienvenida; establézcalo en *0* para desactivar la duración mínima |
| splashFadeTime | valor numérico (milisegundos) | Duración (en milisegundos) de la animación de desvanecimiento de la pantalla de bienvenida; establézcalo en *0* para desactivar el desvanecimiento |
| scaleSplashImage | valor porcentual [0-100] | Establezca el tamaño de la imagen de la pantalla de inicio con respecto a la menor anchura/altura del dispositivo; rango en porcentaje [0-100]; valor = 0 ocultará la imagen por completo, valor = 100 mostrará la imagen a pantalla completa |
| useLoadingSign | **true** o **false** | Establezca en *false* para ocultar el indicador de carga mientras se carga la URL |
| useLoadingProgressBar | **true** o **false** | Establezca en *true* para utilizar la barra de progreso de carga mientras se carga la URL (en lugar del indicador de carga) |
| loadingIndicatorColor | Color | Establezca un color para el indicador de carga |
| alternativeAppIconNames | Lista | Edite esta lista para cambiar los nombres de archivo de sus iconos de aplicación alternativos |
| backgroundlocation | **true** o **false** | Establezca en *true* para permitir el acceso a la ubicación en segundo plano (además, asegúrese de que la capacidad "Background Modes" en la configuración del proyecto de Xcode incluya "Location updates". Dependiendo de su aplicación web, es posible que también necesite activar "Background Processing"; en ese caso, añada además un array a su archivo Info.plist con la clave "Permitted background task scheduler identifiers" y, dentro de ese array, incluya una cadena con el ID del paquete de su aplicación, por ejemplo, "com.onlineappcreator.webviewgold") |
| appendlanguage | **true** o **false** | Establezca en *true* si desea ampliar la solicitud de URL con el idioma del sistema, como ?webview_language=LANGUAGE CODE (por ejemplo, ?webview_language=EN para usuarios angloparlantes) |
| blockfaultyandselfsignedhttpscerts | **true** o **false** | Establezca en *true* para bloquear contenidos firmados con certificados SSL autofirmados (por el usuario) y certificados SSL defectuosos; también puede considerar [bloquear todos los contenidos no HTTPS](https://www.webviewgold.com/support-center/knowledgebase/how-to-prevent-non-https-connections-in-webviewgold-for-ios-removing-nsallowsarbitraryloadsinwebcontent-from-info-plist/) |
| jailbreakBlock | **true** o **false** | Establezca en *true* para bloquear la aplicación en dispositivos con jailbreak o modificados. Nota: La detección no es infalible, pero utiliza varios métodos para identificar jailbreaks y modificaciones |
| autoRefreshEnabled | **true** o **false** | Establezca en *true* si desea que el WebView actualice automáticamente su contenido cuando la aplicación vuelva a primer plano tras estar en segundo plano. |
| offlinelocalhtmlswitch | **true** o **false** | Establezca en *true* si desea utilizar la carpeta "local-html" cuando el usuario esté sin conexión y la URL remota cuando esté en línea. |
| extentionARY | Lista | Añada los formatos de archivo que deban activar la función de descarga (por ejemplo, .pdf, .docx, ...) |
| autodownloader | **true** o **false** | Establezca en *true* si desea activar la función de descarga basada en las cabeceras HTTP Content-Disposition, independientemente de los formatos de archivo listados en la variable extentionARY anterior |
| splashscreencolor | Color | Establezca un color de fondo para la pantalla de inicio |
| extentionARY | Lista | Añada los formatos de archivo que deban activar la función de descarga (por ejemplo, .pdf, .docx, ...) |
| offlinelocalhtmlswitch | **true** o **false** | Establezca en *true* si desea utilizar la carpeta "local-html" cuando el usuario esté sin conexión y la URL remota cuando esté en línea. |
| zipfiledownloadfromserver | **true** o **false** | Establezca en *true* para descargar un archivo .zip desde una URL remota que se extraerá y mostrará si el usuario está sin conexión (además, active la variable turnofflinelocalhtmlswitch en true); la actualización se realizará con cada reinicio completo de la aplicación |
| zipfileremoteurl | URL | El archivo .zip desde una URL remota que se extraerá y mostrará si el usuario está sin conexión |
| zipfilename | nombre del archivo | El nombre interno del archivo .zip en el dispositivo del usuario (se recomienda no modificarlo) |
| zipfileextractpath | nombre de la carpeta | El nombre interno de la carpeta de la ruta de extracción en el dispositivo del usuario (se recomienda no modificarlo) |
| zipfileextractindexindex | nombre del archivo | El archivo que se abrirá primero dentro del archivo .zip extraído |
| zipfilepopuptitle | texto | El título de la ventana emergente que se mostrará mientras se descarga el archivo .zip (si lo desea, puede traducir esta cadena a dos idiomas adicionales usando las cadenas 'alternatelanguage1' y 'alternatelanguage2' que se encuentran al final del archivo Config.swift) |
| zipfilepopupmessage | cadena de texto | El mensaje de la ventana emergente que se mostrará mientras se descarga el archivo .zip (si lo desea, puede traducir esta cadena a dos idiomas adicionales usando las cadenas 'alternatelanguage1' y 'alternatelanguage2' que se encuentran al final del archivo Config.swift) |
| InAppPurchAppBundleIdentifier | opcional | Establezca el identificador de aplicación predeterminado para activar la API de compras dentro de la aplicación para el producto IAP predeterminado (los detalles se pueden configurar en App Store Connect) |
| IAPSharedSecret | opcional | Establezca el App Secret para activar la API de compras dentro de la aplicación (encontrará más información [aquí](in-app-purchases.md)) |
| iapsuccessurl | opcional | Establezca la URL predeterminada que se abrirá tras una compra o suscripción exitosa dentro de la aplicación a través del wrapper WebView. La URL podría ser, por ejemplo, "https://www.example.org/thanks.php", donde thanks.php podría establecer la cookie de por vida para el contenido premium. |
| iapexpiredurl | opcional | Establezca la URL predeterminada que se abrirá cuando expire una suscripción dentro de la aplicación a través del wrapper WebView. La URL podría ser, por ejemplo, "https://www.example.org/expired.php", donde expired.php podría eliminar la cookie del contenido premium |
| revenueCatAPIKey | opcional | Su clave API de RevenueCat (regístrese primero a través de [tinyurl.com/register-revenuecat](https://tinyurl.com/register-revenuecat) y luego siga [tinyurl.com/api-key-revenuecat](https://tinyurl.com/api-key-revenuecat) para saber cómo encontrarla) |
| revenueCatProjectID | opcional | Su ID de proyecto de RevenueCat (regístrese primero a través de [tinyurl.com/register-revenuecat](https://tinyurl.com/register-revenuecat) y luego siga [tinyurl.com/project-id-revenuecat](https://tinyurl.com/project-id-revenuecat) para saber cómo encontrarlo) |
| oneSignalID | opcional | Requerido para la funcionalidad de push de OneSignal |
| kPushEnabled | **true** o **false** | Establezca en *true* para activar la funcionalidad de push de OneSignal |
| kPushEnhanceUrl | **true** o **false** | Establezca en *true* si desea ampliar las solicitudes de URL principal del WebView con el ID de suscripción de OneSignal con el formato ?onesignal_push_id=XYZ (como alternativa o adicionalmente, siempre puede solicitar el ID de suscripción de OneSignal llamando a [getonesignalplayerid://](push-notifications.md#onesignalruntime) o incluso obtenerlo automáticamente si establece "autoInjectVariable" en "true" en Config.swift) |
| kPushReloadOnUserId | **true** o **false** | Establezca en *true* si el WebView debe recargarse tras recibir el UserID de OneSignal |
| kPushOpenDeeplinkInBrowser | **true** o **false** | Establezca en *true* para abrir las URLs de deeplinking de OneSignal en el navegador Safari en lugar del WebView principal; importante: para enviar notificaciones con un enlace desde OneSignal, NO utilice 'Launch URL', sino un 'Additional Data Field' con la clave: url y el valor: el enlace que desea utilizar |
| kFirebasePushEnabled | **true** o **false** | Establezca en *true* para conectar su aplicación a los servicios de push de Firebase |
| kFirebaseEnhanceUrl | **true** o **false** | Establezca en *true* si desea ampliar las solicitudes de URL principal del WebView con ?firebase_push_id=XYZ (como alternativa o adicionalmente, siempre puede solicitar el ID de suscripción de OneSignal llamando a [getfirebaseplayerid://](push-notifications.md#firebaseruntime) o incluso obtenerlo automáticamente si establece "autoInjectVariable" en "true" en Config.swift) |
| firebaseTopic | **opcional** | Establezca un tema (Topic) de Firebase al que suscribirse |
| kPushwooshEnable | **opcional** | Establezca en *true* para activar la funcionalidad de push de Pushwoosh (establezca el ID en Info.plist en la columna Pushwoosh_APPID) |
| kPushwooshEnhanceUrl | **opcional** | Establezca en *true* si desea ampliar las solicitudes de URL principal del WebView con ?pushwoosh_id=XYZ |
| showBannerAd | **true** o **false** | Establezca en *true* si desea mostrar anuncios de banner de AdMob (establezca también los IDs de AdMob en Config.swift e Info.plist; consulte [aquí](admob.md)) |
| showFullScreenAd | **true** o **false** | Establezca en *true* si desea mostrar anuncios intersticiales de AdMob después de X clics en el sitio web (establezca también los IDs de AdMob en Config.swift e Info.plist; consulte [aquí](admob.md)) |
| showadAfterX | opcional | Defina el número X para mostrar un anuncio intersticial de AdMob tras cada X (por ejemplo, 10) clics en el sitio web o toques en la pantalla, según el valor de **incrementWithTaps** (establezca también los IDs de AdMob en Config.swift e Info.plist; consulte [aquí](admob.md)). |
| incrementWithTaps | **true** o **false** | Establezca en *true* si desea mostrar anuncios intersticiales tras X toques en pantalla, o en *false* tras X redirecciones del sitio web. |
| enableRewardedAds | **true** o **false** | Establezca en *true* para activar los anuncios recompensados de AdMob. Debe estar en *true* incluso para la activación manual de los anuncios. |
| useRewardedAdsWherePossible | **true** o **false** | Establezca en *true* para mostrar anuncios recompensados de AdMob en lugar de anuncios intersticiales de AdMob, por ejemplo, después de X toques, etc. Mantenga *false* si su activación debe gestionarse a través del código de su sitio web. Requiere que showFullScreenAd también esté establecido en *true* para poder sobrescribirlos. |
| admobadstriggerurls | opcional | Añada aquí palabras desencadenantes de página; su presencia en una URL activa anuncios intersticiales de AdMob (por ejemplo, ["see-highscore.php", "/thank-you/", "/next-step.html"]) |
| useFacebookAds | **true** o **false** | Establezca en *true* para activar los anuncios intersticiales de Facebook |
| facebookAdsID | opcional | Introduzca su Placement ID, disponible al crear una propiedad en Facebook Monetization Manager y conectar una aplicación iOS. El ID tendrá este aspecto: 3937960198956424_3969441893142587 |
| useTimedAds | **true** o **false** | Utilice anuncios temporizados para los anuncios de Facebook (por ejemplo, cada 60 s) en lugar de anuncios cada X clics |
| fbadstriggerurls | opcional | Añada aquí palabras desencadenantes de página; su presencia en una URL activa un anuncio de Facebook (por ejemplo, ["see-highscore.php", "/thank-you/", "/next-step.html"]) |
| showFBAdsEveryNSeconds | opcional | Muestre un anuncio intersticial de Facebook cada X segundos; se recomienda 120 s o más |
| ATTDeniedShowAds | **true** o **false** | Establezca en *false* para dejar de mostrar anuncios por completo si el usuario deniega el permiso de AppTrackingTransparency (ATT) |
| useAdsenseAds | **true** o **false** | Establezca en *true* para habilitar la compatibilidad con anuncios web de AdSense (independiente de los anuncios de AdMob) |
| askForAdConsent | **true** o **false** | Establezca en *false* si desea desactivar la gestión de consentimiento de Google para AdMob (consulte previamente <https://support.google.com/admob/answer/13554116>) |
| showBarcodeScanner | **true** o **false** | Establezca en *false* para bloquear las solicitudes del sitio web que activan el escáner de códigos de barras mediante `barcodescanner://` |
| kFlashLightEnabled | **true** o **false** | Establezca en *false* para bloquear las solicitudes del sitio web que encienden la linterna mediante `enableflashlight://` |
| widgetRefreshTime | Número | Intervalo de actualización del widget en minutos |
| widgetfallbackURL | Cadena | URL de imagen de reserva utilizada por el widget |
| preventScreenCapture | **true** o **false** | Establezca en *true* para invocar onScreenCaptureAttempt en su aplicación web al detectarse capturas o grabaciones de pantalla |
| kVisionKitEnable | **true** o **false** | Establézcalo en *true* para añadir una opción de escaneo al diálogo de subida de archivos mediante el [escáner de documentos VisionKit](document-scanner.md) (requiere iOS 18.4 o superior) |
| enableSidebar | **true** o **false** | Establézcalo en *true* para activar un botón flotante que abre una [barra lateral nativa](sidebar.md), personalizable en **Sidebar.json** |
| showcustomrateappdialog | **true** o **false** | Establézcalo en *true* para mostrar un diálogo de valoración personalizado al activar la [API rateapp://](in-app-rating.md) en lugar de intentar la llamada de reseña nativa |
| ratemyappurl | URL | Establezca la URL del App Store de su aplicación, utilizada por el diálogo de valoración personalizado |
| cookieonlaunch | **true** o **false** | Establézcalo en *true* para añadir una cookie al iniciarse el WebView; configúrela mediante las variables **cookieonlaunchname**, **cookieonlaunchvalue** y **cookieonlaunchissecure** |
| useCustomHeaders | **true** o **false** | Establézcalo en *true* para enviar las cabeceras HTTP personalizadas definidas en el diccionario **customHeaders** con cada petición del WebView |
| siriEnabled | Token del complemento | Introduzca el token para habilitar la funcionalidad del complemento Siri |
| NFCEnabled | Token del complemento | Introduzca el token para habilitar la funcionalidad del complemento NFC |
| HealthKitEnabled | Token del complemento | Introduzca el token para habilitar la funcionalidad del complemento HealthKit |
| alternatelanguage1_langcode (& lista de cadenas _alternatelanguage1_) | **true** o **false** (& lista de cadenas) | Establezca el código de idioma o deje esta cadena vacía para no utilizar las cadenas del idioma alternativo n.º 1 (lista de cadenas al final del archivo Config.swift); si desea activar este idioma alternativo, utilice el código de dos letras conforme al estándar ISO 639-1 (por ejemplo, "de" para alemán, "fr" para francés, "it" para italiano, "pt" para portugués, "ca" para catalán, "es" para español, …) |
| alternatelanguage2_langcode (& lista de cadenas _alternatelanguage2_) | **true** o **false** (& lista de cadenas) | Establezca el código de idioma o deje esta cadena vacía para no utilizar las cadenas del idioma alternativo n.º 2 (lista de cadenas al final del archivo Config.swift); si desea activar este idioma alternativo, utilice el código de dos letras conforme al estándar ISO 639-1 (por ejemplo, "de" para alemán, "fr" para francés, "it" para italiano, "pt" para portugués, "ca" para catalán, "es" para español, …) |

---

## Seguir leyendo

- ← Anterior: [Configurar la aplicación web](setup-website.md)
- Siguiente →: [Nombre, icono y splash](app-name-icon-splash.md)
- La misma función en otras plataformas: [Android – Configurar WebViewGold](../android/setup.md) · [macOS – Configuración de WebViewGold](../macos/setup.md)
- Idiomas: [🇺🇸 English](../../ios/setup.md) · [🇩🇪 Deutsch](../../de/ios/setup.md) · [🇫🇷 Français](../../fr/ios/setup.md) · **🇪🇸 Español** · [🇨🇳 中文](../../zh/ios/setup.md)

> [!TIP]
> **¿Sin tiempo? Configuramos su app por usted.** Nuestro equipo configura, compila & publica su app WebViewGold: llave en mano, entrega rápida, Made in Germany. [Configurar mi app →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **Compile en su navegador:** Sin Mac ni IDE: el **WebViewGold Cloud Builder** configura, compila & sube su app en línea. [Descubra Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
