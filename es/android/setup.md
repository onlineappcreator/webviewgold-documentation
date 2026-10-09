---
title: "Instalar y configurar WebViewGold para Android – Documentación de WebViewGold para Android"
description: "Descargue la plantilla de WebViewGold para Android Studio, inserte su URL y explore todas las opciones de configuración integradas: sin conocimientos de programación."
lang: "es"
product: "WebViewGold para Android"
platform: "Android"
category: "Primeros pasos"
slug: "setup"
canonical_url: "https://www.webviewgold.com/es/docs/android/setup/"
keywords:
  - "Configurar WebViewGold"
  - "WebViewGold para Android"
  - "convertir sitio web en app"
  - "documentación de app WebView"
  - "SDK WebView de Android"
  - "PWA a app"
  - "HTML a app"
  - "puente de JavaScript"
last_updated: "2026-10-09"
---

# Instalar y configurar WebViewGold para Android – WebViewGold para Android

> **Resumen:** Descargue la plantilla de WebViewGold para Android Studio, inserte su URL y explore todas las opciones de configuración integradas: sin conocimientos de programación.

[Documentación](../README.md) › [WebViewGold para Android](README.md) › Configurar WebViewGold

**Plataforma:** Android · **Categoría:** Primeros pasos · **Versión en línea:** [www.webviewgold.com/es/docs/android/setup/](https://www.webviewgold.com/es/docs/android/setup/)

---

**Descargue**
la plantilla de app WebViewGold para Android Studio
**[aquí](https://www.webviewgold.com/download/android).**
[![Comprar la plantilla de app WebView para Android Studio](../../assets/android/img/cart.webp)](https://www.webviewgold.com/download/android)

> [!NOTE]
> ¿Desea compilar sin instalar Android Studio? Con [**WebViewGold Cloud Builder**](https://www.webviewgold.com/cloud-builder?ref=android_docs) (complemento de pago) puede configurar, compilar y subir su app a Play Store directamente desde el navegador.
>
> [![Ver el vídeo: Instalar y configurar WebViewGold para Android](https://img.youtube.com/vi/nzgCkydN9OM/hqdefault.jpg)](https://www.youtube.com/watch?v=nzgCkydN9OM)

Descargue [**Android Studio**](https://developer.android.com/studio) si aún no lo tiene instalado.\
Luego, abra **Android Studio**:\
![Pantalla de bienvenida de Android Studio](../../assets/android/img/androidstudio2020.webp)

Elija **Open**:\
![Botón Importar proyecto](../../assets/android/img/androidstudio_welcome2022.webp)\
Seleccione su carpeta **AndroidStudioSource** y espere a que el proyecto se cargue por completo:\
![Selector de archivos de Android Studio](../../assets/android/img/filepicker.webp)\
A continuación, abra el archivo **Config.java** para editar los principales detalles de configuración (URL, gestión de URL, UserAgent, diálogos). Consulte nuestro [canal de YouTube](https://www.youtube.com/channel/UChuOoCMcXP_8SQPbZyXTPjA?sub_confirmation=1) para ver tutoriales específicos de configuración. No olvide añadir su [código de compra de Envato/CodeCanyon](https://help.market.envato.com/hc/en-us/articles/202822600-Where-Is-My-Purchase-Code-) en el campo **PURCHASECODE** por cada app que publique. Se requiere una licencia por cada producto final personalizado. Consulte la información de licencia de su compra en CodeCanyon: [https://codecanyon.net/licenses/standard](https://codecanyon.net/licenses/standard?ref=onlineappcreator)\
El documento principal de configuración **Config.java** se ve así: \
![Config.java permite configurar la mayoría de los ajustes directamente en el documento](../../assets/android/img/config.webp)

Configurar apps con WebViewGold es **muy fácil** y no requiere ningún conocimiento de programación. Consulte esta **descripción general** de las opciones de configuración integradas en el archivo **Config.java**:

[![Ver el vídeo: Instalar y configurar WebViewGold para Android](https://img.youtube.com/vi/5rlknsdIORE/hqdefault.jpg)](https://www.youtube.com/watch?v=5rlknsdIORE)

| Ajuste | Valor | Descripción |
| --- | --- | --- |
| HOST | **valor requerido** | El host de su dominio sin el prefijo https:// o http:// (por ejemplo, "www.example.org"). De forma predeterminada, WebViewGold para Android permite tanto contenido HTTPS como HTTP. Sin embargo, si prefiere reforzar la seguridad de la app habilitando únicamente contenido HTTPS, existe la opción de [modificar esta configuración](https://www.webviewgold.com/support-center/knowledgebase/how-to-prevent-non-https-connections-in-webviewgold-for-android-switching-usescleartexttraffic-from-true-to-false/) (y/o considerar la opción 'BLOCK_SELF_SIGNED_AND_FAULTY_SSL_CERTS'). |
| HOME_URL | **valor requerido** | La URL completa de su WebView (por ejemplo, "https://www.example.org/app.html") que debe cargarse en la WebView. De forma predeterminada, WebViewGold para Android permite tanto contenido HTTPS como HTTP. Sin embargo, si prefiere reforzar la seguridad de la app habilitando únicamente contenido HTTPS, existe la opción de [modificar esta configuración](https://www.webviewgold.com/support-center/knowledgebase/how-to-prevent-non-https-connections-in-webviewgold-for-android-switching-usescleartexttraffic-from-true-to-false/) (y/o considerar la opción 'BLOCK_SELF_SIGNED_AND_FAULTY_SSL_CERTS'). |
| USE_LOCAL_HTML_FOLDER | **true** o **false** | Establezca en *true* para usar el archivo HTML local "index.html" en lugar de la URL remota de la WebView |
| FALLBACK_USE_LOCAL_HTML_FOLDER_IF_OFFLINE | **true** o **false** | Establezca en *true* si desea utilizar la carpeta "local-html" cuando el usuario esté sin conexión y usar la URL remota cuando esté en línea |
| ACTIVATE_PROGRESS_BAR | **true** o **false** | Establezca en *false* para desactivar el indicador de progreso/carga |
| PHONE_ORIENTATION | valor (orientación) | Establezca la orientación del teléfono en "portrait", "landscape" o "auto" |
| TABLET_ORIENTATION | valor (orientación) | Establezca la orientación de la tableta en "portrait", "landscape" o "auto" |
| USER_AGENT | opcional | Defina un UserAgent personalizado para las solicitudes web (o déjelo vacío para usar el UserAgent predeterminado de Android) |
| HARDWARE_ACCELERATION | **true** o **false** | Establezca en *true* para activar la aceleración por hardware; puede mejorar el rendimiento de renderizado, pero también puede aumentar el uso de memoria y provocar problemas de compatibilidad con algunos contenidos |
| APPEND_LANG_CODE | **true** o **false** | Establezca en *true* si desea ampliar la solicitud de URL con el idioma del sistema, como ?webview_language=LANGUAGE CODE (por ejemplo, ?webview_language=EN para usuarios en inglés) |
| AUTO_REFRESH_ENABLED | **true** o **false** | Establezca en *true* si desea que la WebView actualice automáticamente su contenido cuando la app vuelve al primer plano desde el segundo plano. |
| EXTERNAL_LINK_HANDLING_OPTIONS | **0** o **1** o **2** | Establezca en (0) para abrir los enlaces externos dentro de la app de forma predeterminada; (1) para abrirlos SIEMPRE en una nueva pestaña (un navegador integrado adicional); (2) para abrirlos SIEMPRE en otro navegador |
| BROWSER_WHITELIST | Lista | Añada aquí los dominios que **siempre** deban abrirse en el navegador externo, independientemente del valor asignado a la opción **EXTERNAL_LINK_HANDLING_OPTIONS**. Para añadir otro dominio, inserte otro host de la siguiente manera: ["www.alwaysopeninchrome.com", "www.google.com"]. Introduzca el host exactamente como lo enlaza (pero nunca con la inclusión de http/https). |
| BROWSER_BLACKLIST | Lista | Añada aquí los dominios que **nunca** deban abrirse en el navegador externo, independientemente del valor asignado a la opción **EXTERNAL_LINK_HANDLING_OPTIONS**. Para añadir otro dominio, inserte otro host de la siguiente manera: ["www.neveropeninchrome.com", "www.google.com"]. Introduzca el host exactamente como lo enlaza (pero nunca con la inclusión de http/https). |
| SPECIAL_LINK_HANDLING_OPTIONS | **0** o **1** o **2** | Establezca en (0) para abrir enlaces especiales dentro de la app; (1) en una nueva pestaña (un navegador integrado adicional); (2) en otro navegador; NOTA: los enlaces especiales tienen el objetivo "_blank" o terminan con "#"; anula a *EXTERNAL_LINK_HANDLING_OPTIONS* si el enlace también es un enlace externo |
| ALWAYS_OPEN_IN_INAPP_TAB | lista | Añada los prefijos de URL que desea abrir SIEMPRE en una pestaña integrada en la app (por ejemplo, {"https://www.google.com", "https://www.example.com/page"}), independientemente del valor asignado a **EXTERNAL_LINK_HANDLING_OPTIONS**. |
| NEVER_OPEN_IN_INAPP_TAB | lista | Añada los prefijos de URL que NUNCA desea abrir en una pestaña integrada en la app (por ejemplo, {"https://www.google.com", "https://www.example.com/page"}), independientemente del valor asignado a **EXTERNAL_LINK_HANDLING_OPTIONS**. |
| QR_CODE_URL_OPTIONS | **0** o **1** o **2** o **3** o **4** | Establezca en (0) para abrir en la app una URL de código QR escaneada; (1) en una pestaña integrada; (2) en un navegador nuevo; (3) en una pestaña integrada si es externa; (4) en un navegador nuevo si es externa |
| AUTO_INJECT_VARIABLES | **true** o **false** | Establezca en *true* para asignar variables de JavaScript automáticamente; eliminará la necesidad de llamar manualmente a métodos como get-uuid://. Actualmente admite la carga de la versión de la app, los IDs de suscripción de OneSignal y Firebase, así como el UUID. |
| CLEAR_CACHE_ON_STARTUP | **true** o **false** | Establezca en *true* para borrar la caché y las cookies de la WebView en cada arranque de la app y no usar versiones en caché de su web app/sitio web |
| CLEAR_CACHE_ON_EXIT | **true** o **false** | Establezca en *true* para borrar la caché y las cookies de la WebView al cerrar por completo la app (también puede que quiera activar *CLEAR_CACHE_ON_STARTUP*, ya que las diferencias entre sistemas pueden afectar la fiabilidad) |
| COOKIE_ON_LAUNCH | **true** o **false** | Establézcalo en *true* para añadir una cookie personalizada al WebView al iniciar la aplicación |
| COOKIE_ON_LAUNCH_NAME | valor de texto | Personalice el nombre de la cookie añadida al inicio (requiere COOKIE_ON_LAUNCH en *true*) |
| COOKIE_ON_LAUNCH_VALUE | valor de texto | Personalice el valor de la cookie añadida al inicio (requiere COOKIE_ON_LAUNCH en *true*) |
| COOKIE_ON_LAUNCH_IS_SECURE | **true** o **false** | Establézcalo en *true* para marcar la cookie de inicio como segura (solo HTTPS) |
| IS_DEEP_LINKING_ENABLED | **true** o **false** | Establezca en *true* para habilitar el deep-linking |
| IS_CUSTOM_SCHEME_ENABLED | **true** o **false** | Establezca en *true* si desea aceptar deeplinks con esquema personalizado como `webviewgold://` |
| CUSTOM_DEEPLINK_SCHEME | **true** o **false** | Personalice aquí el prefijo del esquema de deeplinking y también en AndroidManifest.xml |
| OPEN_NOTIFICATION_URLS_IN_SYSTEM_BROWSER | **true** o **false** | Establezca en *true* para abrir las URLs de deep linking de notificaciones en el navegador del sistema en lugar de en su app |
| SPLASH_SCREEN_ACTIVATED | **true** o **false** | Establezca en *true* para activar la pantalla de bienvenida (splash screen) |
| SPLASH_TIMEOUT | valor numérico (milisegundos) | Establezca el tiempo de espera de la pantalla de bienvenida en *milisegundos* (el indicador de carga se mostrará después de este intervalo si la URL principal aún necesita seguir cargando) |
| SPLASH_FADE_OUT | valor numérico (milisegundos) | Duración de la animación de desvanecimiento de la pantalla de bienvenida en milisegundos. Esta animación comienza una vez completados todos los demás temporizadores de retraso. Establezca en 0 para desactivar el efecto de desvanecimiento. |
| SPLASH_MIN_TIME | valor numérico (milisegundos) | Duración mínima (en ms) durante la cual se mostrará la pantalla de bienvenida; solo se aplica si *REMAIN_SPLASH_OPTION* está establecida en *true*. Si *SPLASH_MIN_TIME* supera ese valor, la pantalla de bienvenida permanecerá durante *SPLASH_MIN_TIME*. En tales casos, este valor se ignorará a favor de la duración más larga. |
| REMAIN_SPLASH_OPTION | **true** o **false** | Establezca en *true* para mostrar la pantalla de bienvenida hasta que la URL principal termine de cargarse (anula a *SPLASH_TIMEOUT*) |
| SCALE_SPLASH_IMAGE | valor porcentual [0-100] | Establezca el tamaño de la imagen de la pantalla de bienvenida en relación con el ancho/alto más pequeño del dispositivo; rango en porcentaje [0-100]; atención: un valor = 0 ocultará la imagen por completo |
| blackStatusBarText | **true** o **false** | Establezca en *true* para texto negro en la barra de estado; establezca en *false* para texto blanco; utilice 'colorPrimaryDark' en style.xml para elegir el color de fondo de la barra de estado |
| TRANSPARENT_STATUS_BAR | **true** o **false** | Establezca en *true* para una barra de estado transparente; establezca en *false* para una barra de estado opaca; utilice 'colorPrimaryDark' en style.xml para elegir el color de fondo de la barra de estado |
| enableBioMetricAuth | **true** o **false** | Establezca en *true* para habilitar el bloqueo de app (autenticación biométrica) en la app |
| PREVENT_SLEEP | **true** o **false** | Establezca en *true* para evitar que el dispositivo entre en modo de suspensión mientras la app está activa |
| ENABLE_SWIPE_NAVIGATE | **true** o **false** | Establezca en *true* para habilitar la navegación deslizando el dedo hacia la izquierda o hacia la derecha para retroceder o avanzar una página |
| ENABLE_PULL_REFRESH | **true** o **false** | Establezca en *true* para habilitar la actualización de la página deslizando hacia abajo. Además, siempre puede llamar a `enablepulltorefresh://` o `disablepulltorefresh://` desde su sitio web para activar o desactivar dinámicamente el pull-to-refresh. |
| HIDE_VERTICAL_SCROLLBAR | **true** o **false** | Establezca en *true* para ocultar la barra de desplazamiento vertical |
| HIDE_HORIZONTAL_SCROLLBAR | **true** o **false** | Establezca en *true* para ocultar la barra de desplazamiento horizontal |
| ENABLE_ZOOM | **true** o **false** | Establezca en *false* para evitar las funciones de zoom para el usuario de la app (funciona además mediante inyección de script) |
| DISABLE_DARK_MODE | **true** o **false** | Establezca en *true* para desactivar el modo oscuro (no funciona en todos los launchers) |
| HIDE_NAVIGATION_BAR_IN_LANDSCAPE | **true** o **false** | Establezca en *true* para ocultar la barra de navegación en modo horizontal |
| MAX_TEXT_ZOOM | valor numérico | Establezca un valor mayor que 0 para definir un zoom de texto máximo; establezca en (0) para desactivar esta función.  <br> *Nota: Pequeño = 85, Predeterminado = 100, Grande = 115, Muy grande = 130* |
| INPUT_SCROLL_HELPER | **true** o **false** | Establezca en *true* para forzar un desplazamiento coherente de los campos de entrada (mediante inyección de JS) |
| EXIT_APP_BY_BACK_BUTTON_ALWAYS | **true** o **false** | Establezca en *true* para cerrar la app al presionar el botón físico de retroceso (en lugar de volver a la página anterior) |
| EXIT_APP_BY_BACK_BUTTON_HOMEPAGE | **true** o **false** | Establezca en *true* para cerrar la app al presionar el botón físico de retroceso si el usuario se encuentra en la página de inicio (que no permite retroceder a una página anterior) |
| EXIT_APP_DIALOG | **true** o **false** | Establezca en *true* para preguntar al usuario si desea salir antes de cerrar la app |
| OFFLINE_SCREEN_BACKGROUND_COLOR | código de color hexadecimal | Establezca el color de fondo de la pantalla sin conexión mediante el código de color hexadecimal (por ejemplo, "#ffffff" = blanco) |
| PREVENT_SCREEN_CAPTURE | **true** o **false** | Establezca en *true* para impedir que los usuarios realicen capturas de pantalla o grabaciones de pantalla en la app. Se llamará a `onScreenCaptureAttempt()` en la web app para gestionar el evento (por ejemplo, mostrar un modal personalizado). |
| UUID_ENHANCE_WEBVIEW_URL | **true** o **false** | Establezca en *true* para añadir el parámetro UUID 'uuid=XYZ' a la primera solicitud de URL |
| BLOCK_SELF_SIGNED_AND_FAULTY_SSL_CERTS | **true** o **false** | Establezca en *true* para bloquear el contenido firmado con certificados SSL autofirmados (de usuario) y certificados SSL defectuosos; considere también [bloquear todo contenido no HTTPS](https://www.webviewgold.com/support-center/knowledgebase/how-to-prevent-non-https-connections-in-webviewgold-for-android-switching-usescleartexttraffic-from-true-to-false/) |
| BLOCK_ROOTED_DEVICES | **true** o **false** | Establezca en *true* para habilitar la función de la app para detectar dispositivos rooteados y desactivarse en ellos (nota: la detección de root no siempre es fiable y puede no funcionar en todos los dispositivos) |
| LINK_DRAG_AND_DROP | **true** o **false** | Establezca en *false* para desactivar el arrastrar y soltar de enlaces |
| LANDSCAPE_FULLSCREEN_VIDEO | **true** o **false** | Establezca en *true* para mostrar siempre los videos en pantalla completa en modo horizontal |
| SHOW_FIRSTRUN_DIALOG | **true** o **false** | Establezca en *false* para desactivar el diálogo de primera ejecución |
| SHOW_FACEBOOK_DIALOG | **true** o **false** | Establezca en *false* para desactivar el diálogo "Seguir en Facebook" |
| SHOW_RATE_DIALOG | **true** o **false** | Establezca en *false* para desactivar el diálogo "Calificar esta app" |
| RATE_DAYS_UNTIL_PROMPT | valor numérico (días) | Establezca la cantidad mínima de días que deben transcurrir tras la instalación de la aplicación antes de que se muestre el diálogo "Calificar esta app" |
| RATE_LAUNCHES_UNTIL_PROMPT | valor numérico (aperturas) | Establezca la cantidad mínima de aperturas de la aplicación antes de que se muestre el diálogo "Calificar esta app" |
| FACEBOOK_DAYS_UNTIL_PROMPT | valor numérico (días) | Establezca la cantidad mínima de días que deben transcurrir tras la instalación de la aplicación antes de que se muestre el diálogo "Seguir en Facebook" |
| FACEBOOK_LAUNCHES_UNTIL_PROMPT | valor numérico (aperturas) | Establezca la cantidad mínima de aperturas de la aplicación antes de que se muestre el diálogo "Calificar esta app" |
| FACEBOOK_URL | valor (URL) | Establezca la URL de su página de Facebook |
| ALLOW_IMAGE_DOWNLOAD | **true** o **false** | Establezca en *false* para evitar que aparezca el cuadro emergente "Descargar imágenes" al mantener pulsada una imagen |
| PUSH_ENABLED | **true** o **false** | Establezca en *true* para activar OneSignal Push (configure los IDs de OneSignal en el archivo build.gradle) |
| PUSH_ENHANCE_WEBVIEW_URL | **true** o **false** | Establezca en *true* si desea ampliar las solicitudes de la URL principal de la WebView con el ID de suscripción de OneSignal en el formato ?onesignal_push_id=XYZ (como alternativa o de forma adicional, siempre puede solicitar el ID de suscripción de OneSignal llamando a [getonesignalplayerid://](push-notifications.md), o incluso obtenerlo automáticamente si establece "AUTO_INJECT_VARIABLES" en "true" en Config.java) |
| PUSH_RELOAD_ON_USERID | **true** o **false** | Establezca en *true* si la WebView debe recargarse cuando la app reciba un UserID de OneSignal (configure los IDs de OneSignal en el archivo build.gradle) |
| FIREBASE_PUSH_ENABLED | **true** o **false** | Establezca en *true* para activar Firebase Push (reemplace previamente google-services.json) |
| FIREBASE_PUSH_ENHANCE_WEBVIEW_URL | **true** o **false** | Establezca en *true* si desea ampliar la solicitud de URL con ?firebase_push_id=XYZ (como alternativa o de forma adicional, siempre puede solicitar el ID de suscripción de Firebase llamando a [getfirebaseplayerid://](push-notifications.md#firebaseruntime), o incluso obtenerlo automáticamente si establece "AUTO_INJECT_VARIABLES" en "true" en Config.java) |
| PUSHWOOSH_ENABLED | **true** o **false** | Establezca en *true* para activar Pushwoosh Push (configure las credenciales de Pushwoosh en los archivos AndroidManifest.xml y string.xml) |
| PUSHWOOSH_ENHANCE_WEBVIEW_URL | **true** o **false** | Establezca en *true* si desea ampliar la solicitud de URL con ?pushwoosh_id=XYZ (configure las credenciales de Pushwoosh en los archivos AndroidManifest.xml y string.xml) |
| SHOW_ADSENSE_AD | **true** o **false** | Establezca en *true* para habilitar la compatibilidad con anuncios web de AdSense (independientemente de los anuncios de AdMob) |
| SHOW_BANNER_AD | **true** o **false** | Establezca en *true* si desea mostrar anuncios de banner de AdMob (configure los IDs de AdMob en el archivo strings.xml) |
| SHOW_FULL_SCREEN_AD | **true** o **false** | Establezca en *true* si desea mostrar anuncios intersticiales de pantalla completa de AdMob después de X clics en el sitio web (configure los IDs de AdMob en el archivo strings.xml) |
| SHOW_APP_OPEN_AD | **true** o **false** | Establézcalo en *true* para mostrar [anuncios app open de AdMob](admob.md#appopenads) en el arranque en frío (desde el splash del launcher) y al volver desde segundo plano (configure admob_app_open_id en el archivo strings.xml) |
| ASK_FOR_AD_CONSENT | **true** o **false** | Establezca en *false* si desea desactivar la gestión de consentimiento de Google para AdMob (consulte previamente <https://support.google.com/admob/answer/13554116>) |
| SHOW_AD_AFTER_X | valor (recargas del sitio web) | Establezca el número X de clics en el sitio web para anuncios intersticiales de AdMob (configure los IDs de AdMob en el archivo strings.xml) |
| INCREMENT_WITH_TAPS | **true** o **false** | Establezca en *true* para que los toques normales en la pantalla incrementen SHOW_AD_AFTER_X |
| USE_FACEBOOK_ADS | **true** o **false** | Establezca en *true* para usar anuncios de Facebook Audience Network en lugar de anuncios de AdMob (configure los IDs de anuncios en el archivo strings.xml) |
| ENABLE_REWARDED_ADS | **true** o **false** | Establezca en *true* para habilitar los anuncios recompensados de AdMob. Debe estar en *true* incluso para la activación manual de los anuncios. (Configure los IDs de anuncios en el archivo strings.xml.) |
| USE_REWARDED_ADS_WHERE_POSSIBLE | **true** o **false** | Establezca en *true* para mostrar anuncios recompensados de AdMob en lugar de anuncios intersticiales de AdMob, es decir, después de X toques, etc. Manténgalo en *false* si su activación debe gestionarse mediante el código de su sitio web. Tenga en cuenta que esto requiere que SHOW_FULL_SCREEN_AD también esté en *true* para que los anuncios sean reemplazados. |
| AD_TRIGGER_URLS | opcional | Añada aquí palabras desencadenantes para páginas; su presencia en una URL activa los anuncios intersticiales (por ejemplo, "thanks.html", "welcome.html", "/thank-you/", "next-step.php") |
| REVENUECAT_API_KEY | opcional | Su clave de API de RevenueCat (regístrese primero en [tinyurl.com/register-revenuecat](https://tinyurl.com/register-revenuecat) y luego siga [tinyurl.com/api-key-revenuecat](https://tinyurl.com/api-key-revenuecat) para saber cómo encontrarla) |
| REVENUECAT_PROJECT_ID | opcional | Su ID de proyecto de RevenueCat (regístrese primero en [tinyurl.com/register-revenuecat](https://tinyurl.com/register-revenuecat) y luego siga [tinyurl.com/project-id-revenuecat](https://tinyurl.com/project-id-revenuecat) para saber cómo encontrarlo) |
| downloadableExtension | lista | Añada los formatos de archivo que deben activar la función de descarga (por ejemplo, .pdf, .docx, ...) |
| AUTO_DOWNLOAD_FILES | **true** o **false** | Establezca en *true* si desea activar la función de descarga basada en los encabezados HTTP Content-Disposition, independientemente de los formatos de archivo listados en la variable downloadableExtension anterior |
| GOOGLE_LOGIN_HELPER_TRIGGERS | lista | Defina los prefijos de URL que se cargan durante el inicio de sesión de Google en su sitio web; actúa como disparador para el helper |
| FACEBOOK_LOGIN_HELPER_TRIGGERS | lista | Defina los prefijos de URL que se cargan durante el inicio de sesión de Facebook en su sitio web; actúa como disparador para el helper |
| HOME_URL_LOGOUT | valor (URL) | Defina la URL para el cierre de sesión y así borrar las cookies de inicio de sesión (opcional) |
| MANUAL_COOKIE_SYNC | **true** o **false** | Establezca en *true* para habilitar la herramienta de sincronización manual de cookies. Se debe usar si necesita que las cookies se sincronicen con una frecuencia *inferior* a 30 segundos o si alguna funcionalidad relacionada con cookies no funciona de otro modo. Consulte también las indicaciones sobre cookies [aquí](https://www.webviewgold.com/support-center/knowledgebase/will-cookies-work-will-the-login-of-my-website-web-app-still-work/). |
| COOKIE_SYNC_TIME | valor numérico (milisegundos) | Defina con qué frecuencia deben sincronizarse las cookies con la app, en milisegundos (ms) |
| MANUAL_COOKIE_SYNC_TRIGGERS | lista | Defina los prefijos de URL en los que desea utilizar la herramienta de sincronización manual de cookies. Si MANUAL_COOKIE_SYNC_TRIGGERS está vacío, se comprobará automáticamente cada página. Ejemplo: {"https://example.com/login", "https://example.com/data"} |
| USE_CUSTOM_HEADERS | **true** o **false** | Establézcalo en *true* para inyectar encabezados HTTP personalizados en cada navegación de URL; defina los nombres y valores de los encabezados en el mapa *customHeaders* justo debajo de esta opción en Config.java |
| requireLocation | **true** o **false** | Establezca en *false* si NO necesita los servicios de ubicación/coordenadas GPS; no olvide eliminar también las entradas correspondientes en *AndroidManifest.xml* si desea eliminar por completo la capacidad de permiso de la app; consulte también [uso de la ubicación en segundo plano (¡!)](geolocation.md) |
| requireBackgroundLocation | **true** o **false** | Establezca en *false* si se requieren servicios de ubicación en segundo plano. Si esta opción se establece en *false*, asegúrese de descomentar también los bloques `android.permission.FOREGROUND_SERVICE_LOCATION` y `.GPSService` en `AndroidManifest.xml` (busque esos términos dentro del archivo). Esta configuración solo es efectiva si `requireLocation` también está establecido en *true*. |
| requireStorage | **true** o **false** | Establezca en *false* si NO necesita APIs relacionadas con descargas o subidas; no olvide eliminar también las entradas correspondientes en *AndroidManifest.xml* si desea eliminar por completo la capacidad de permiso de la app |
| requireCamera | **true** o **false** | Establezca en *false* si NO necesita APIs relacionadas con imágenes de cámara / videos de cámara; no olvide eliminar también las entradas correspondientes en *AndroidManifest.xml* si desea eliminar por completo la capacidad de permiso de la app |
| requireRecordAudio | **true** o **false** | Establezca en *false* si NO necesita APIs relacionadas con la grabación de audio; no olvide eliminar también las entradas correspondientes en *AndroidManifest.xml* si desea eliminar por completo la capacidad de permiso de la app |
| filePickerMode | valor numérico | Opciones de carga de archivos: (0) cámara y galería; (1) solo cámara; (2) solo galería. |

Abra el archivo **strings.xml** para editar el nombre de la app y las cadenas de texto:\
![Archivo string.xml para editar los textos](../../assets/android/img/strings.webp)

**Apps multilingües:** para editar las traducciones —incluidas las de alemán y español, disponibles de forma predeterminada— o para crear nuevas traducciones adicionales de estas cadenas, haga clic con el botón derecho en la carpeta "strings" en Android Studio y seleccione "Open Translations Editor":\
![Soporte multilingüe para su app WebView en Android](../../assets/android/img/translations.webp)

Abra el archivo **dimens.xml** para modificar el formato del texto:\
![Utilice dimens.xml para redimensionar objetos y textos](../../assets/android/img/screenshot_Dimens.webp)

---

## Seguir leyendo

- ← Anterior: [Configurar la aplicación web](setup-website.md)
- Siguiente →: [Icono de la app](app-icon.md)
- La misma función en otras plataformas: [iOS – Configurar WebViewGold](../ios/setup.md) · [macOS – Configuración de WebViewGold](../macos/setup.md)
- Idiomas: [🇺🇸 English](../../android/setup.md) · [🇩🇪 Deutsch](../../de/android/setup.md) · [🇫🇷 Français](../../fr/android/setup.md) · **🇪🇸 Español** · [🇨🇳 中文](../../zh/android/setup.md)

> [!TIP]
> **¿Sin tiempo? Configuramos su app por usted.** Nuestro equipo configura, compila & publica su app WebViewGold: llave en mano, entrega rápida, Made in Germany. [Configurar mi app →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_android_doc_online)
>
> **Compile en su navegador:** Sin Mac ni IDE: el **WebViewGold Cloud Builder** configura, compila & sube su app en línea. [Descubra Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=android_docs)
