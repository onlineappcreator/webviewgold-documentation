---
title: "API de anuncios de Facebook Audience Network – Documentación de WebViewGold para iOS"
description: "Muestre anuncios de banner e intersticiales de Facebook Audience Network en su app WebViewGold de iOS."
lang: "es"
product: "WebViewGold para iOS"
platform: "iOS"
category: "API y funciones"
slug: "facebook-ads"
canonical_url: "https://www.webviewgold.com/es/docs/iOS/facebook-ads/"
keywords:
  - "API de anuncios Facebook"
  - "WebViewGold para iOS"
  - "convertir sitio web en app"
  - "documentación de app WebView"
  - "SDK WebView de iOS"
  - "PWA a app"
  - "HTML a app"
  - "puente de JavaScript"
last_updated: "2026-10-09"
---

# API de anuncios de Facebook Audience Network – WebViewGold para iOS

> **Resumen:** Muestre anuncios de banner e intersticiales de Facebook Audience Network en su app WebViewGold de iOS.

[Documentación](../README.md) › [WebViewGold para iOS](README.md) › API de anuncios Facebook

**Plataforma:** iOS · **Categoría:** API y funciones · **Versión en línea:** [www.webviewgold.com/es/docs/iOS/facebook-ads/](https://www.webviewgold.com/es/docs/iOS/facebook-ads/)

---

La [Facebook Audience Network](https://www.facebook.com/audiencenetwork/) permite a los desarrolladores de aplicaciones móviles monetizar aplicaciones iOS y Android mostrando anuncios. A través de WebViewGold, puede incorporar fácilmente anuncios de Facebook en sus aplicaciones iOS basadas en WebView para obtener ingresos por clics (CPC) e impresiones (CPM).

## Paso 1: Crear una cuenta de Facebook Audience Network

Debe crear una cuenta de [Facebook Audience Network](https://www.facebook.com/audiencenetwork/) y crear una property en Integración dentro del Monetization Manager. Luego debe vincular una aplicación iOS (aunque no necesita enlazar una aplicación iOS publicada con fines de prueba).

Siga esta guía como referencia: <https://www.facebook.com/business/help/191133327919314>

## Paso 2: Establecer las variables de configuración necesarias

- Abra **Config.swift** y establezca `useFacebookAds` en `true`.
- Introduzca su ID de ubicación (Placement ID) de Facebook en `facebookAdsID`.

![Captura de la configuración de Facebook Ads](../../assets/ios/img/fbadsconfig.webp)

## Paso 3: Configurar los ajustes de los anuncios

- Para usar anuncios programados por tiempo, establezca `useTimedAds` en `true` y ajuste `showFBAdsEveryNSeconds` al tiempo deseado entre anuncios.
- Puede añadir palabras desencadenantes de URL a `fbadstriggerurls` para inicializar los anuncios bajo demanda.

## Consideraciones adicionales

- Debe utilizar un dispositivo iOS real para las pruebas (no un simulador)
- El dispositivo debe añadirse como dispositivo de prueba; consulte <https://developers.facebook.com/docs/audience-network/setting-up/testing/platform>
- Facebook debe estar instalado y con sesión iniciada en el dispositivo
- «Limit Ad Tracking» o cualquier ajuste similar que pueda incluirse en futuras versiones de iOS debe estar desactivado.

---

## Seguir leyendo

- ← Anterior: [API de anuncios AdMob](admob.md)
- Siguiente →: [API de audio HTML](html-audio.md)
- La misma función en otras plataformas: [Android – API de anuncios de Facebook](../android/facebook-ads.md)
- Idiomas: [🇺🇸 English](../../ios/facebook-ads.md) · [🇩🇪 Deutsch](../../de/ios/facebook-ads.md) · [🇫🇷 Français](../../fr/ios/facebook-ads.md) · **🇪🇸 Español** · [🇨🇳 中文](../../zh/ios/facebook-ads.md)

> [!TIP]
> **¿Sin tiempo? Configuramos su app por usted.** Nuestro equipo configura, compila & publica su app WebViewGold: llave en mano, entrega rápida, Made in Germany. [Configurar mi app →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **Compile en su navegador:** Sin Mac ni IDE: el **WebViewGold Cloud Builder** configura, compila & sube su app en línea. [Descubra Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
