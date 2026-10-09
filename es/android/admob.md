---
title: "API de anuncios AdMob – Documentación de WebViewGold para Android"
description: "Monetice su aplicación de Android con anuncios de banner e intersticiales de Google AdMob: configuración y disparadores de JavaScript."
lang: "es"
product: "WebViewGold para Android"
platform: "Android"
category: "API y funciones"
slug: "admob"
canonical_url: "https://www.webviewgold.com/es/docs/android/admob/"
keywords:
  - "API de anuncios AdMob"
  - "WebViewGold para Android"
  - "convertir sitio web en app"
  - "documentación de app WebView"
  - "SDK WebView de Android"
  - "PWA a app"
  - "HTML a app"
  - "puente de JavaScript"
last_updated: "2026-10-09"
---

# API de anuncios AdMob – WebViewGold para Android

> **Resumen:** Monetice su aplicación de Android con anuncios de banner e intersticiales de Google AdMob: configuración y disparadores de JavaScript.

[Documentación](../README.md) › [WebViewGold para Android](README.md) › API de anuncios AdMob

**Plataforma:** Android · **Categoría:** API y funciones · **Versión en línea:** [www.webviewgold.com/es/docs/android/admob/](https://www.webviewgold.com/es/docs/android/admob/)

---

AdMob es un servicio de Google para monetizar apps móviles en las plataformas iOS y Android. Permite a los desarrolladores integrar anuncios de banner, intersticiales y recompensados, que se pagan por clics (CPC, coste por clic) o impresiones (CPM, coste por mil). WebViewGold simplifica la integración de AdMob, permitiendo una configuración rápida para mostrar anuncios en su aplicación Android basada en WebView.

## Paso 1: Abra el archivo Config.java

Para empezar, abra el archivo **Config.java** de su app para definir las preferencias de anuncios y activar la funcionalidad de AdMob.

## Paso 2: Monetice su app con el SDK nativo de AdMob

En **Config.java** puede:

- **Activar o desactivar** los anuncios de banner o intersticiales estableciendo `SHOW_BANNER_AD` en true para los anuncios de banner y `SHOW_FULL_SCREEN_AD` en true para los anuncios intersticiales.
- **Definir los intervalos** para mostrar anuncios intersticiales cambiando `SHOW_AD_AFTER_X` al número deseado de interacciones con el sitio web antes de reproducir un anuncio intersticial.

**Nota:** Antes de publicar su app, asegúrese de que sus identificadores únicos de AdMob se hayan añadido correctamente en el archivo **strings.xml**:\
![Active bloques de anuncios de AdMob concretos en su app](../../assets/android/img/admobconfig.webp)

## Paso 3: Active los anuncios recompensados

- Configuración de los anuncios recompensados:
  - Para activar los anuncios recompensados, establezca `ENABLE_REWARDED_ADS` en `true`.
  - Utilice el siguiente enlace para mostrar un anuncio recompensado

    ```html
    <a href="displayrewardedad://">Display Rewarded Advertisement</a>
    ```

  - Una vez que un usuario termina de ver el anuncio, WebViewGold activa la función JavaScript `updateRewardedStatus('true');` para que usted gestione las recompensas dentro del código de su app.
- Anuncios recompensados de forma predeterminada:
  - Si prefiere que los anuncios recompensados se muestren de forma predeterminada, establezca tanto `USE_REWARDED_ADS_WHERE_POSSIBLE` como `SHOW_FULL_SCREEN_AD` en `true`. Esto dará prioridad a los anuncios recompensados sobre los intersticiales.

## Recursos adicionales

Para conocer opciones más detalladas, consulte la [documentación oficial del SDK de AdMob](https://developers.google.com/admob/), pero omita las instrucciones de configuración, ya que WebViewGold ya incluye el framework necesario.

[![Ver el vídeo: API de anuncios AdMob](https://img.youtube.com/vi/vq5FM7n0Syg/hqdefault.jpg)](https://www.youtube.com/watch?v=vq5FM7n0Syg)

También puede controlar de forma **dinámica** la visibilidad de los anuncios para un usuario llamando a los siguientes esquemas de URL personalizados desde su sitio web o app:

- `enableads://` – Hace que los anuncios se vuelvan a mostrar para el usuario actual
- `disableads://` – Desactiva permanentemente los anuncios para el usuario actual

## <a id="appopenads"></a>Paso 4: Activar los anuncios App Open

Los **anuncios app open** son anuncios a pantalla completa que aparecen cuando el usuario abre la aplicación (arranque en frío desde el splash del launcher) o vuelve a ella desde segundo plano. Para activarlos:

- Establezca `SHOW_APP_OPEN_AD` en `true` en **Config.java**.
- Sustituya el valor `admob_app_open_id` en **strings.xml** por el ID de su propio bloque de anuncios app open de AdMob (la plantilla incluye el ID de prueba oficial de AdMob — ¡sustitúyalo antes del lanzamiento!).

**Nota:** Los anuncios app open respetan la gestión de consentimiento de Google (`ASK_FOR_AD_CONSENT`) igual que los demás formatos de AdMob.

---

## Seguir leyendo

- ← Anterior: [API de notificaciones push](push-notifications.md)
- Siguiente →: [API de anuncios de Facebook](facebook-ads.md)
- La misma función en otras plataformas: [iOS – API de anuncios AdMob](../ios/admob.md)
- Idiomas: [🇺🇸 English](../../android/admob.md) · [🇩🇪 Deutsch](../../de/android/admob.md) · [🇫🇷 Français](../../fr/android/admob.md) · **🇪🇸 Español** · [🇨🇳 中文](../../zh/android/admob.md)

> [!TIP]
> **¿Sin tiempo? Configuramos su app por usted.** Nuestro equipo configura, compila & publica su app WebViewGold: llave en mano, entrega rápida, Made in Germany. [Configurar mi app →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_android_doc_online)
>
> **Compile en su navegador:** Sin Mac ni IDE: el **WebViewGold Cloud Builder** configura, compila & sube su app en línea. [Descubra Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=android_docs)
