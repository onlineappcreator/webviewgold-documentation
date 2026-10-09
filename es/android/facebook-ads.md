---
title: "API de anuncios de Facebook Audience Network – Documentación de WebViewGold para Android"
description: "Muestre anuncios de banner e intersticiales de Facebook Audience Network en su aplicación de Android WebViewGold."
lang: "es"
product: "WebViewGold para Android"
platform: "Android"
category: "API y funciones"
slug: "facebook-ads"
canonical_url: "https://www.webviewgold.com/es/docs/android/facebook-ads/"
keywords:
  - "API de anuncios de Facebook"
  - "WebViewGold para Android"
  - "convertir sitio web en app"
  - "documentación de app WebView"
  - "SDK WebView de Android"
  - "PWA a app"
  - "HTML a app"
  - "puente de JavaScript"
last_updated: "2026-10-09"
---

# API de anuncios de Facebook Audience Network – WebViewGold para Android

> **Resumen:** Muestre anuncios de banner e intersticiales de Facebook Audience Network en su aplicación de Android WebViewGold.

[Documentación](../README.md) › [WebViewGold para Android](README.md) › API de anuncios de Facebook

**Plataforma:** Android · **Categoría:** API y funciones · **Versión en línea:** [www.webviewgold.com/es/docs/android/facebook-ads/](https://www.webviewgold.com/es/docs/android/facebook-ads/)

---

Facebook Audience Network permite a los desarrolladores de apps móviles monetizar aplicaciones iOS y Android mostrando anuncios. A través de WebViewGold, puede incorporar fácilmente anuncios de Facebook en su app Android basada en WebView para obtener ingresos mediante clics (CPC) e impresiones (CPM).

## Paso 1: Abra el archivo Config.java

- Para empezar, abra el archivo **Config.java** de su app para configurar los ajustes de Audience Network.

## Paso 2: Active los anuncios de Facebook Audience Network

1. **Active las variables de configuración necesarias:**
   - Establezca las siguientes variables en `true` en Config.java:
     - `USE_FACEBOOK_ADS` hace que la app utilice anuncios de Facebook Audience Network en lugar de anuncios de AdMob.
     - `SHOW_BANNER_AD` activa los anuncios de banner en su app.
     - `SHOW_FULLSCREEN_AD` activa los anuncios intersticiales a pantalla completa en su app.
   - Establezca `SHOW_AD_AFTER_X` en el número deseado de clics en el sitio web para mostrar un anuncio intersticial.

2. **Introduzca sus identificadores de anuncios de Facebook:**
   - Vaya a `strings.xml` y añada sus identificadores únicos de anuncios de Facebook en los campos correspondientes.

Tras configurar los ajustes anteriores y confirmar sus identificadores de anuncios, su app estará lista para publicarse con los anuncios de Facebook Audience Network activados.

Para más detalles, también puede consultar la [documentación oficial de Facebook Audience Network](https://developers.facebook.com/docs/audience-network) para obtener consejos adicionales de configuración u optimización específicos de su estrategia publicitaria.

[![Ver el vídeo: API de anuncios de Facebook Audience Network](https://img.youtube.com/vi/81wCzuFttic/hqdefault.jpg)](https://www.youtube.com/watch?v=81wCzuFttic)

También puede controlar de forma **dinámica** la visibilidad de los anuncios para un usuario llamando a los siguientes esquemas de URL personalizados desde su sitio web o app:

- `enableads://` – Hace que los anuncios se vuelvan a mostrar para el usuario actual
- `disableads://` – Desactiva permanentemente los anuncios para el usuario actual

```html
<a href="enableads://">Enable Ads</a>
<a href="disableads://">Disable Ads</a>
```

---

## Seguir leyendo

- ← Anterior: [API de anuncios AdMob](admob.md)
- Siguiente →: [API de descarga de archivos](file-downloader.md)
- La misma función en otras plataformas: [iOS – API de anuncios Facebook](../ios/facebook-ads.md)
- Idiomas: [🇺🇸 English](../../android/facebook-ads.md) · [🇩🇪 Deutsch](../../de/android/facebook-ads.md) · [🇫🇷 Français](../../fr/android/facebook-ads.md) · **🇪🇸 Español** · [🇨🇳 中文](../../zh/android/facebook-ads.md)

> [!TIP]
> **¿Sin tiempo? Configuramos su app por usted.** Nuestro equipo configura, compila & publica su app WebViewGold: llave en mano, entrega rápida, Made in Germany. [Configurar mi app →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_android_doc_online)
>
> **Compile en su navegador:** Sin Mac ni IDE: el **WebViewGold Cloud Builder** configura, compila & sube su app en línea. [Descubra Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=android_docs)
