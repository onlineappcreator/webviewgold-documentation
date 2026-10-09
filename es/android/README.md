---
title: "Documentación de WebViewGold para Android: convierta un sitio web en una app de Android"
description: "Documentación oficial de WebViewGold para Android: convierta su sitio web en una aplicación de Android nativa en minutos, con guía de configuración, más de 30 API y funciones, y publicación en Google Play."
lang: "es"
product: "WebViewGold para Android"
platform: "Android"
canonical_url: "https://www.webviewgold.com/es/docs/android/"
keywords:
  - "WebViewGold para Android"
  - "convertir sitio web en app"
  - "documentación de app WebView"
  - "SDK WebView de Android"
  - "PWA a app"
  - "HTML a app"
  - "puente de JavaScript"
last_updated: "2026-10-09"
---

# Documentación de WebViewGold para Android

![WebViewGold para Android](../../assets/android/img/header.webp)

> Documentación oficial de WebViewGold para Android: convierta su sitio web en una aplicación de Android nativa en minutos, con guía de configuración, más de 30 API y funciones, y publicación en Google Play.

[Documentación](../README.md) › WebViewGold para Android

Convierta su sitio web, PWA, panel SaaS, tienda de comercio electrónico o app web generada por IA en una app nativa de Android en minutos. Use WebViewGold como un SDK de app ligero: configure su URL, habilite API nativas, integre comandos del puente de JavaScript y publique una app lista para la tienda sin reconstruir su producto web desde cero.

WebViewGold funciona con sitios HTML/PHP clásicos, WordPress, proyectos de jQuery Mobile y apps web modernas creadas con Lovable, Base44, Bolt, Bubble, React, Vue, Angular o constructores similares. La documentación siguiente explica el flujo de configuración, las API de funciones nativas, las consideraciones de seguridad y los pasos de publicación en un formato técnico centrado en la implementación.

**[Empezar la guía →](setup-website.md)** · [Descargar WebViewGold](https://www.webviewgold.com/download/android) · [Cloud Builder](https://www.webviewgold.com/cloud-builder?ref=android_docs)

## Inicio rápido

Tres pasos del sitio web a la app publicada:

1. **[Configure su app web](setup-website.md)** — Use una URL remota, empaquete archivos HTML locales o combine ambos con una alternativa sin conexión.
2. **[Configure WebViewGold](setup.md)** — Introduzca su URL y ajuste cada opción en un sencillo archivo de configuración, sin programar.
3. **[Compilar & publicar](publish.md)** — Lleve su app a la tienda: usted mismo, con Cloud Builder o con nuestro servicio de publicación.

## Novedades

WebViewGold se actualiza con regularidad. Consulte el registro de cambios completo [aquí](https://www.webviewgold.com/changelog/android/).

## Todos los temas, API & funciones

Todo lo que WebViewGold para Android puede hacer: cada tema en su propia página:

### Primeros pasos

- **[Configurar la aplicación web](setup-website.md)** — Prepare su sitio web, PWA o archivos HTML locales para su aplicación de Android: use una URL remota, incluya archivos sin conexión en la aplicación o combine ambos con un respaldo sin conexión.
- **[Configurar WebViewGold](setup.md)** — Descargue la plantilla de WebViewGold para Android Studio, inserte su URL y explore todas las opciones de configuración integradas: sin conocimientos de programación.

### Diseño de la app

- **[Icono de la app](app-icon.md)** — Añada su icono de aplicación personalizado a su app de Android WebViewGold en Android Studio, paso a paso.
- **[Pantalla de bienvenida](splash-screen.md)** — Personalice la pantalla de inicio de su aplicación Android WebView con sus propios gráficos.
- **[Navigation Drawer & Footer](navigation-drawer.md)** — Ship an app-like navigation experience with the built-in Material navigation drawer and Material 3 bottom navigation bar — no changes to your website required.

### API y funciones

- **[API de gestión de URL](url-handling.md)** — Decida qué enlaces se abren dentro de su aplicación de Android, en las Chrome Custom Tabs o en el navegador externo.
- **[API de CSS y JS personalizados](custom-css-js.md)** — Inyecte estilos CSS y código JavaScript personalizados en cualquier página de su aplicación Android WebView: ideal para ajustes exclusivos de la app.
- **[Multi API Call](multi-api-call.md)** — Llame a varias APIs de datos de WebViewGold en una sola asignación de window.location.href — ideal para web apps multiplataforma que también usan la versión de iOS.
- **[API de geolocalización](geolocation.md)** — Active la geolocalización HTML5 en su aplicación Android WebView y solicite correctamente los permisos de ubicación.
- **[API de notificaciones push](push-notifications.md)** — Envíe notificaciones push a los usuarios de su aplicación de Android con OneSignal, Firebase o Pushwoosh: configuración, deep links y segmentación por usuario explicados.
- **[API de anuncios AdMob](admob.md)** — Monetice su aplicación de Android con anuncios de banner e intersticiales de Google AdMob: configuración y disparadores de JavaScript.
- **[API de anuncios de Facebook](facebook-ads.md)** — Muestre anuncios de banner e intersticiales de Facebook Audience Network en su aplicación de Android WebViewGold.
- **[API de descarga de archivos](file-downloader.md)** — Permita que los usuarios descarguen imágenes, PDF y otros archivos desde su aplicación web a su dispositivo Android.
- **[API de vídeo nativo (PiP)](native-video.md)** — Reproduzca vídeos de forma nativa con soporte de Picture-in-Picture en su aplicación Android WebView.
- **[API de restablecimiento](reset-app.md)** — Restablezca la caché, las cookies y el almacenamiento local de su aplicación Android WebView con un solo enlace o llamada de JavaScript.
- **[API de indicador de carga](loading-sign.md)** — Muestre u oculte el indicador de carga nativo cuando lo desee y personalice la experiencia de carga de su aplicación de Android.
- **[API de portapapeles](clipboard.md)** — Copie texto al portapapeles de Android y lea su contenido desde su aplicación web mediante JavaScript.
- **[API de UUID](uuid.md)** — Identifique las instalaciones de la aplicación con un UUID único añadido a su URL de WebView u obtenido mediante JavaScript.
- **[API de linterna](flashlight.md)** — Controle la linterna del dispositivo desde su aplicación web con sencillos enlaces de JavaScript en WebViewGold para Android.
- **[App Links / Deep Linking](app-links.md)** — Abra los enlaces a su dominio directamente en su aplicación de Android con App Links y deep linking mediante un esquema de URL personalizado.
- **[API ShareIntent](share-intent.md)** — Reciba el contenido compartido desde otras aplicaciones de Android directamente en su aplicación WebView mediante Share Intents.
- **[API de diálogo para compartir](app-sharing-dialog.md)** — Active el diálogo nativo de Android para compartir desde su aplicación web y permita que los usuarios compartan su app o cualquier URL.
- **[API de valoración In-App](in-app-rating.md)** — Pida a sus usuarios una reseña en Google Play: active el diálogo nativo "Valorar esta app" mediante rateapp:// desde su web app o deje que WebViewGold lo muestre automáticamente.
- **[API de compras integradas](in-app-purchases.md)** — Venda productos digitales y suscripciones en su aplicación Android WebView con Google Play Billing.
- **[IAP History API](iap-history.md)** — Return the user's Google Play purchase history as window.purchaseHistory so your web app can list subscriptions or unlock premium content client-side.
- **[API de escáner de QR](qr-code-scanner.md)** — Abra un escáner de códigos QR nativo desde su aplicación web y procese los resultados mediante URL o JavaScript.
- **[API de modo de escaneo](scanning-mode.md)** — Ajuste con precisión el comportamiento de escaneo de la cámara del escáner de códigos QR y de barras en WebViewGold para Android.
- **[API de escáner de códigos de barras](barcode-scanner.md)** — Escanee códigos de barras EAN, UPC y otros de forma nativa en su aplicación Android WebView y entregue los resultados a su aplicación web.
- **[API de captura de pantalla](take-screenshot.md)** — Realice una captura de la pantalla actual de la aplicación mediante programación y compártala o guárdela con JavaScript.
- **[API de comprobación de versión](app-version-check.md)** — Detecte la versión instalada de la aplicación desde su aplicación web y solicite a los usuarios que la actualicen cuando sea necesario.
- **[API de contactos](contacts.md)** — Acceda a la agenda del dispositivo desde su aplicación web: lea los contactos con el permiso del usuario en WebViewGold para Android.
- **[API de interfaz dinámica](dynamic-ui.md)** — Cambie elementos de la interfaz nativa, como el color de la barra de estado, de forma dinámica desde su aplicación web en Android.
- **[API de respuesta háptica](haptic-feedback.md)** — Active la respuesta háptica por vibración nativa desde su aplicación web para lograr una sensación de app nativa en Android.
- **[Plugin NFC](nfc.md)** — Lea etiquetas NFC de forma nativa en su aplicación Android WebView y transfiera los datos de la etiqueta a su aplicación web.
- **[Open App Settings API](open-app-settings.md)** — Send the user straight to the system App-info screen from your web app to manage permissions, notifications, storage, or force-stop your Android app.
- **[Reconnect API](reconnect.md)** — Reload the last online URL from your offline / fallback HTML page — the perfect "Try again" button for your custom offline screen.
- **[Read/Write Value API](read-write-value.md)** — Persist small strings on the device from JavaScript and read them back — for theme, language, session tokens, or onboarding state.
- **[Biometric Auth API](biometric-auth.md)** — Prompt fingerprint or face authentication with the native Android BiometricPrompt directly from your web app.
- **[Document Scanner](document-scanner.md)** — Add a Scan document option to the file upload dialog — the user scans up to 5 pages and your web app receives a PDF like any other upload.
- **[Printer API](printer.md)** — Send a remote image or PDF to the Android system print dialog — Wi-Fi printers, cloud print, or Save-as-PDF, straight from your web app.
- **[Health Connect API](health-connect.md)** — Read and write Android Health Connect records from JavaScript — mirrors the WebViewGold HealthKit API on iOS so one web app covers both platforms.

### Compilar y publicar

- **[Firebase Crashlytics](crashlytics.md)** — Ship crash reports and non-fatal events to your Firebase project, with runtime opt-in / opt-out from your web app.
- **[Compilar y publicar](publish.md)** — Publique su aplicación WebView en Google Play Store: servicio de publicación completo, proceso manual y cambio del nombre de paquete.

### Más

- **[Créditos y licencias](credits.md)** — Condiciones de licencia de WebViewGold para Android, cuándo necesita una Envato Extended License y créditos de código abierto.
- **[Valorar WebViewGold](rate.md)** — ¿Le gusta WebViewGold? Valórelo en CodeCanyon en segundos: así seguimos lanzando actualizaciones.
- **[Versiones iOS y macOS](more-platforms.md)** — Lleve su aplicación a más plataformas: consiga WebViewGold para iOS y macOS y reutilice la misma aplicación web.
- **[Soporte y contacto](support.md)** — Obtenga ayuda rápidamente: explore el Centro de Soporte de WebViewGold, contacte directamente con nuestro equipo o solicite un desarrollo de aplicaciones personalizado y profesional made in Germany.

## Una app web, todas las plataformas

Reutilice el mismo sitio web para apps de iOS, Android & macOS con WebViewGold.

- [WebViewGold para iOS](../ios/README.md)
- [WebViewGold para macOS](../macos/README.md)

**Idiomas:** [🇺🇸 English](../../android/README.md) · [🇩🇪 Deutsch](../../de/android/README.md) · [🇫🇷 Français](../../fr/android/README.md) · **🇪🇸 Español** · [🇨🇳 中文](../../zh/android/README.md)

> [!TIP]
> **¿Sin tiempo? Configuramos su app por usted.** Nuestro equipo configura, compila & publica su app WebViewGold: llave en mano, entrega rápida, Made in Germany. [Configurar mi app →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_android_doc_online)
>
> **Compile en su navegador:** Sin Mac ni IDE: el **WebViewGold Cloud Builder** configura, compila & sube su app en línea. [Descubra Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=android_docs)
