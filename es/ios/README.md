---
title: "Documentación de WebViewGold para iOS: convierta un sitio web en app iOS"
description: "Documentación oficial de WebViewGold para iOS: convierta su sitio web en una app iOS nativa en minutos: guía de configuración, más de 40 API y funciones, y publicación en la App Store."
lang: "es"
product: "WebViewGold para iOS"
platform: "iOS"
canonical_url: "https://www.webviewgold.com/es/docs/iOS/"
keywords:
  - "WebViewGold para iOS"
  - "convertir sitio web en app"
  - "documentación de app WebView"
  - "SDK WebView de iOS"
  - "PWA a app"
  - "HTML a app"
  - "puente de JavaScript"
last_updated: "2026-10-09"
---

# Documentación de WebViewGold para iOS

![WebViewGold para iOS](../../assets/ios/img/header.webp)

> Documentación oficial de WebViewGold para iOS: convierta su sitio web en una app iOS nativa en minutos: guía de configuración, más de 40 API y funciones, y publicación en la App Store.

[Documentación](../README.md) › WebViewGold para iOS

Convierta su sitio web, PWA, panel SaaS, tienda de comercio electrónico o app web generada por IA en una app nativa de iOS en minutos. Use WebViewGold como un SDK de app ligero: configure su URL, habilite API nativas, integre comandos del puente de JavaScript y publique una app lista para la tienda sin reconstruir su producto web desde cero.

WebViewGold funciona con sitios HTML/PHP clásicos, WordPress, proyectos de jQuery Mobile y apps web modernas creadas con Lovable, Base44, Bolt, Bubble, React, Vue, Angular o constructores similares. La documentación siguiente explica el flujo de configuración, las API de funciones nativas, las consideraciones de seguridad y los pasos de publicación en un formato técnico centrado en la implementación.

**[Empezar la guía →](setup-website.md)** · [Descargar WebViewGold](https://www.webviewgold.com/download/ios) · [Cloud Builder](https://www.webviewgold.com/cloud-builder?ref=ios_docs)

## Inicio rápido

Tres pasos del sitio web a la app publicada:

1. **[Configure su app web](setup-website.md)** — Use una URL remota, empaquete archivos HTML locales o combine ambos con una alternativa sin conexión.
2. **[Configure WebViewGold](setup.md)** — Introduzca su URL y ajuste cada opción en un sencillo archivo de configuración, sin programar.
3. **[Compilar & publicar](publish.md)** — Lleve su app a la tienda: usted mismo, con Cloud Builder o con nuestro servicio de publicación.

## Novedades

WebViewGold se actualiza con regularidad. Consulte el registro de cambios completo [aquí](https://www.webviewgold.com/changelog/ios/).

## Todos los temas, API & funciones

Todo lo que WebViewGold para iOS puede hacer: cada tema en su propia página:

### Primeros pasos

- **[Configurar la aplicación web](setup-website.md)** — Prepare su sitio web, PWA o archivos HTML locales para su app iOS: utilice una URL remota, incluya archivos sin conexión en la app o combine ambos con un respaldo sin conexión.
- **[Configurar WebViewGold](setup.md)** — Descargue la plantilla de Xcode de WebViewGold, inserte su URL en Config.swift y explore todas las opciones de configuración integradas, sin necesidad de saber programar.

### Diseño de la app

- **[Nombre, icono y splash](app-name-icon-splash.md)** — Cambie el nombre de su app iOS, añada un icono de app personalizado y configure gráficos de pantalla de bienvenida personalizados para su app WebViewGold.
- **[Modificar la Safe Area](safe-area.md)** — Ajuste la safe area y active la barra inferior personalizada para que su aplicación web se vea perfecta en los iPhone con barra de inicio.

### API y funciones

- **[API de geolocalización](geolocation.md)** — Active la geolocalización HTML5 en su app WebView de iOS y solicite los permisos de ubicación precisa de la manera correcta.
- **[API de notificaciones push](push-notifications.md)** — Envíe notificaciones push a los usuarios de su app iOS con OneSignal, Firebase o Pushwoosh: configuración, deep links y segmentación por usuario explicados.
- **[API de anuncios AdMob](admob.md)** — Monetice su app iOS con anuncios de banner, intersticiales y recompensados de Google AdMob: configuración y disparadores de JavaScript.
- **[API de anuncios Facebook](facebook-ads.md)** — Muestre anuncios de banner e intersticiales de Facebook Audience Network en su app WebViewGold de iOS.
- **[API de audio HTML](html-audio.md)** — Mantenga el audio HTML reproduciéndose en segundo plano de su app WebView de iOS, incluso con la pantalla bloqueada.
- **[API de vídeo nativo](native-video.md)** — Reproduzca transmisiones de vídeo en el reproductor nativo de iOS con soporte de imagen en imagen, activadas directamente desde su aplicación web.
- **[API de descarga de archivos](file-downloader.md)** — Permita que los usuarios descarguen imágenes, PDF y otros archivos desde su aplicación web directamente a su iPhone o iPad.
- **[API de impresora](printer.md)** — Imprima imágenes y PDF desde su aplicación web mediante AirPrint: envíe archivos al diálogo de impresión nativo de iOS con un solo enlace.
- **[API de calendario iCal](ical-calendar.md)** — Añada eventos de calendario desde su aplicación web al calendario nativo de iOS mediante la API de calendario iCal.
- **[API de pases de Apple Wallet](wallet-pass.md)** — Permita que los usuarios añadan pases .pkpass (entradas, cupones, tarjetas de socio) desde su aplicación web a Apple Wallet.
- **[API UUID](uuid.md)** — Identifique las instalaciones de la app con un UUID único añadido a su URL de WebView u obtenido mediante JavaScript.
- **[API de linterna](flashlight.md)** — Controle la linterna del dispositivo desde su aplicación web con sencillos enlaces de JavaScript en WebViewGold para iOS.
- **[API de restablecer app](reset-app.md)** — Restablezca la caché, las cookies y el almacenamiento local de su app WebView de iOS con un solo enlace o llamada de JavaScript.
- **[API de decisión de seguimiento](user-tracking.md)** — Respete App Tracking Transparency: lea la decisión de seguimiento del usuario y reaccione ante ella dentro de su app WebViewGold de iOS.
- **[API de indicador de carga](loading-sign.md)** — Muestre u oculte el indicador de carga nativo cuando lo necesite y personalice la experiencia de carga de su app iOS.
- **[API Pull-to-Refresh](pull-to-refresh.md)** — Active el gesto nativo de deslizar para actualizar en su app WebView de iOS, personalice sus colores y actívelo o desactívelo dinámicamente desde su app web.
- **[API de gestión de URL](url-handling.md)** — Decida qué enlaces se abren dentro de su app, en una pestaña del navegador integrado o en Safari: control total de la gestión de URL para iOS.
- **[Social Login Helper](social-login.md)** — Haga que los inicios de sesión OAuth de Google, Facebook y Apple funcionen de forma fiable en su app WebView de iOS con los asistentes de inicio de sesión integrados.
- **[API de reconexión](reconnect.md)** — Añada un botón «Reintentar» a su página de respaldo sin conexión que recargue la última URL en línea de su aplicación iOS.
- **[API de CSS y JS personalizados](custom-css-js.md)** — Inyecte estilos CSS y código JavaScript personalizados en cualquier página de su app WebView de iOS, ideal para ajustes exclusivos de la app.
- **[API de Universal Links](universal-links.md)** — Abra los enlaces a su dominio directamente en su app iOS con Apple Universal Links: configuración, archivo AASA y resolución de problemas.
- **[API de deep linking](deep-linking.md)** — Inicie su app iOS mediante esquemas de URL personalizados y dirija a los usuarios con deep links a páginas concretas de su aplicación web.
- **[API de diálogo para compartir](app-sharing-dialog.md)** — Active la hoja de compartir nativa de iOS desde su aplicación web para que los usuarios compartan su app o cualquier URL.
- **[API del diálogo de valoración](in-app-rating.md)** — Pida a los usuarios una valoración en el App Store en el momento perfecto: active el diálogo de valoración nativo de iOS desde su aplicación web.
- **[API de compras integradas](in-app-purchases.md)** — Venda bienes digitales y suscripciones en su app WebView de iOS con compras integradas basadas en StoreKit.
- **[API del historial de compras](iap-history.md)** — Lea las compras In-App anteriores del usuario desde su aplicación web como JSON, perfecto para páginas de «Mis compras».
- **[API de escáner de QR](qr-code-scanner.md)** — Abra un escáner de código QR nativo desde su aplicación web y procese los resultados del escaneo mediante URL o JavaScript.
- **[API de escáner de códigos de barras](barcode-scanner.md)** — Escanee códigos de barras EAN, UPC y otros de forma nativa en su app WebView de iOS y transfiera los resultados a su aplicación web.
- **[API de modo de escaneo](scanning-mode.md)** — Ajuste con precisión el comportamiento de escaneo de la cámara del escáner de QR y de códigos de barras en WebViewGold para iOS.
- **[Escáner de documentos](document-scanner.md)** — Permita que los usuarios escaneen documentos en papel con la cámara y los suban mediante la carga de archivos de su aplicación web, con la tecnología de Apple VisionKit.
- **[API de captura de pantalla](take-screenshot.md)** — Capture mediante programación una captura de la pantalla actual de la app y compártala o guárdela, mediante JavaScript.
- **[API de comprobación de versión](app-version-check.md)** — Detecte la versión instalada de la app desde su aplicación web e invite a los usuarios a actualizarla cuando sea necesario.
- **[API de UI dinámica](dynamic-ui.md)** — Cambie dinámicamente elementos de UI nativos, como los colores de la barra de estado o la barra inferior, desde su aplicación web.
- **[API de icono de app dinámico](dynamic-app-icon.md)** — Cambie entre iconos de app alternativos en tiempo de ejecución en su app WebView de iOS, activado desde su aplicación web.
- **[API de Contactos](contacts.md)** — Acceda a la agenda del dispositivo desde su aplicación web: lea los contactos con el permiso del usuario en WebViewGold para iOS.
- **[API de autenticación biométrica](biometric-authentication.md)** — Proteja su app iOS con Face ID o Touch ID y verifique a los usuarios de forma biométrica desde su aplicación web.
- **[API de respuesta háptica](haptic-feedback.md)** — Active la respuesta háptica nativa (vibraciones) desde su aplicación web para una sensación de app verdaderamente nativa en iOS.
- **[API Shortcut](shortcut.md)** — Añada accesos directos de acción rápida en la pantalla de inicio de su app iOS que dirijan con deep link a páginas concretas.
- **[API de Portapapeles](clipboard.md)** — Copie texto al portapapeles de iOS y lea el contenido del portapapeles desde su aplicación web mediante JavaScript.
- **[API de lectura/escritura de valores](read-write-value.md)** — Almacene de forma persistente un valor de cadena en el dispositivo y léalo de nuevo en el JavaScript de su aplicación web.
- **[API para abrir los ajustes](open-app-settings.md)** — Envíe a los usuarios directamente a la página de su aplicación en la app Ajustes de iOS para gestionar permisos y notificaciones.

### Extensiones y plugins

- **[Share Extension](share-extension.md)** — Permita que los usuarios compartan contenido de otras apps directamente en su app WebView de iOS con una Share Extension.
- **[Widget Extension](widget-extension.md)** — Añada un widget de pantalla de inicio a su app WebView de iOS que dirija a los usuarios directamente a su aplicación web.
- **[App Clip Extension](app-clip.md)** — Ofrezca una versión App Clip ligera de su app iOS que se abre al instante sin necesidad de instalación.
- **[Pie de navegación nativo](navigation-footer.md)** — Active una barra de navegación inferior nativa con botones de atrás, adelante y personalizados en su app iOS.
- **[Barra lateral nativa](sidebar.md)** — Active un menú lateral deslizante nativo con enlaces personalizados e iconos de SF Symbols, configurado mediante Sidebar.json.
- **[Detección de captura de pantalla](screen-capture.md)** — Detecte capturas y grabaciones de pantalla en su app iOS y reaccione desde su aplicación web.
- **[Función MultiAPICall](multi-api-call.md)** — Encadene varias llamadas a la API de WebViewGold en una sola petición con la función MultiAPICall para iOS.
- **[Plugin NFC](nfc.md)** — Lea etiquetas NFC de forma nativa en su app WebView de iOS y transfiera los datos de la etiqueta a su aplicación web.
- **[Plugin Siri](siri.md)** — Añada compatibilidad con los atajos de Siri a su app WebView de iOS y abra el contenido de la app por voz.
- **[Plugin HealthKit](healthkit.md)** — Conecte su aplicación web con Apple HealthKit y lea los datos de salud con el permiso del usuario en iOS.

### Compilar y publicar

- **[Compilar y publicar](publish.md)** — Publique su app WebView en la Apple App Store: servicio de publicación completo, proceso manual y cambio del identificador de bundle.

### Más

- **[Créditos y licencias](credits.md)** — Condiciones de licencia de WebViewGold para iOS, cuándo necesita una Envato Extended License y créditos de código abierto.
- **[Valorar WebViewGold](rate.md)** — ¿Le gusta WebViewGold? Valórelo en CodeCanyon en segundos: así seguirán llegando las actualizaciones.
- **[Versiones Android y macOS](more-platforms.md)** — Lleve su app a más plataformas: consiga WebViewGold para Android y macOS y reutilice la misma aplicación web.
- **[Soporte y contacto](support.md)** — Obtenga ayuda rápido: explore el centro de soporte de WebViewGold, contacte directamente con nuestro equipo o solicite un desarrollo de app a medida y profesional, made in Germany.

## Una app web, todas las plataformas

Reutilice el mismo sitio web para apps de iOS, Android & macOS con WebViewGold.

- [WebViewGold para Android](../android/README.md)
- [WebViewGold para macOS](../macos/README.md)

**Idiomas:** [🇺🇸 English](../../ios/README.md) · [🇩🇪 Deutsch](../../de/ios/README.md) · [🇫🇷 Français](../../fr/ios/README.md) · **🇪🇸 Español** · [🇨🇳 中文](../../zh/ios/README.md)

> [!TIP]
> **¿Sin tiempo? Configuramos su app por usted.** Nuestro equipo configura, compila & publica su app WebViewGold: llave en mano, entrega rápida, Made in Germany. [Configurar mi app →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **Compile en su navegador:** Sin Mac ni IDE: el **WebViewGold Cloud Builder** configura, compila & sube su app en línea. [Descubra Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
