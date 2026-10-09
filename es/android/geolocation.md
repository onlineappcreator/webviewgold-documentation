---
title: "API de geolocalización HTML5 – Documentación de WebViewGold para Android"
description: "Active la geolocalización HTML5 en su aplicación Android WebView y solicite correctamente los permisos de ubicación."
lang: "es"
product: "WebViewGold para Android"
platform: "Android"
category: "API y funciones"
slug: "geolocation"
canonical_url: "https://www.webviewgold.com/es/docs/android/geolocation/"
keywords:
  - "API de geolocalización"
  - "WebViewGold para Android"
  - "convertir sitio web en app"
  - "documentación de app WebView"
  - "SDK WebView de Android"
  - "PWA a app"
  - "HTML a app"
  - "puente de JavaScript"
last_updated: "2026-10-09"
---

# API de geolocalización HTML5 – WebViewGold para Android

> **Resumen:** Active la geolocalización HTML5 en su aplicación Android WebView y solicite correctamente los permisos de ubicación.

[Documentación](../README.md) › [WebViewGold para Android](README.md) › API de geolocalización

**Plataforma:** Android · **Categoría:** API y funciones · **Versión en línea:** [www.webviewgold.com/es/docs/android/geolocation/](https://www.webviewgold.com/es/docs/android/geolocation/)

---

La API de geolocalización de HTML5 permite a los usuarios compartir su ubicación con su app, mejorando funciones como el contenido basado en la ubicación. En WebViewGold, la API de geolocalización es compatible de forma predeterminada una vez integrada en su contenido web. A continuación se explica cómo implementar el seguimiento de geolocalización en su app Android basada en WebView:

## Configurar la geolocalización de HTML5

Para la configuración básica de la geolocalización, consulte la [guía de geolocalización de Mozilla](https://developer.mozilla.org/en-US/docs/Web/API/Geolocation_API) para obtener detalles sobre cómo implementar esta función en su sitio web o app web.

Para ver una demostración, visite esta [demo de geolocalización de W3Schools](https://www.w3schools.com/html/html5_geolocation.asp).

## Activar el seguimiento de ubicación en segundo plano (solo Android)

Para activar el seguimiento de ubicación en segundo plano en su app Android basada en WebView, siga estos pasos:

1. Establezca los permisos en **Config.java**:
   - Establezca `requireBackgroundLocation` en `true` si necesita el seguimiento de ubicación en segundo plano.
   - Asegúrese de que `requireLocation` también esté establecido en `true` para activar cualquier servicio de ubicación.
2. Ajuste los permisos en **AndroidManifest.xml**:
   - Descomente los bloques de permisos de `android.permission.FOREGROUND_SERVICE_LOCATION` y `GPSService`.
   - Busque estos términos dentro del archivo para asegurarse de que se establezcan los permisos correctos.

## Activar y desactivar el seguimiento de ubicación en segundo plano con esquemas de URL

Utilice los siguientes esquemas de URL para activar o desactivar el seguimiento de ubicación en segundo plano en su app Android basada en WebView:

Para activar el seguimiento de ubicación en segundo plano, redirija al usuario a la siguiente URL:

```html
<script>window.location.href = "backgroundlocationon://";  </script>
```

Para desactivar el seguimiento de ubicación en segundo plano, redirija al usuario a la siguiente URL:

```html
<script>window.location.href = "backgroundlocationoff://";  </script>
```

**Nota:** estos esquemas de URL son específicos de WebViewGold para Android y es posible que no funcionen en navegadores web estándar. Para asegurarse de que estas redirecciones solo se apliquen a los usuarios de la app de Android, considere detectar el User-Agent.

---

## Seguir leyendo

- ← Anterior: [Multi API Call](multi-api-call.md)
- Siguiente →: [API de notificaciones push](push-notifications.md)
- La misma función en otras plataformas: [iOS – API de geolocalización](../ios/geolocation.md)
- Idiomas: [🇺🇸 English](../../android/geolocation.md) · [🇩🇪 Deutsch](../../de/android/geolocation.md) · [🇫🇷 Français](../../fr/android/geolocation.md) · **🇪🇸 Español** · [🇨🇳 中文](../../zh/android/geolocation.md)

> [!TIP]
> **¿Sin tiempo? Configuramos su app por usted.** Nuestro equipo configura, compila & publica su app WebViewGold: llave en mano, entrega rápida, Made in Germany. [Configurar mi app →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_android_doc_online)
>
> **Compile en su navegador:** Sin Mac ni IDE: el **WebViewGold Cloud Builder** configura, compila & sube su app en línea. [Descubra Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=android_docs)
