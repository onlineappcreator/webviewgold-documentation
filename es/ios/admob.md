---
title: "API de anuncios AdMob – Documentación de WebViewGold para iOS"
description: "Monetice su app iOS con anuncios de banner, intersticiales y recompensados de Google AdMob: configuración y disparadores de JavaScript."
lang: "es"
product: "WebViewGold para iOS"
platform: "iOS"
category: "API y funciones"
slug: "admob"
canonical_url: "https://www.webviewgold.com/es/docs/iOS/admob/"
keywords:
  - "API de anuncios AdMob"
  - "WebViewGold para iOS"
  - "convertir sitio web en app"
  - "documentación de app WebView"
  - "SDK WebView de iOS"
  - "PWA a app"
  - "HTML a app"
  - "puente de JavaScript"
last_updated: "2026-10-09"
---

# API de anuncios AdMob – WebViewGold para iOS

> **Resumen:** Monetice su app iOS con anuncios de banner, intersticiales y recompensados de Google AdMob: configuración y disparadores de JavaScript.

[Documentación](../README.md) › [WebViewGold para iOS](README.md) › API de anuncios AdMob

**Plataforma:** iOS · **Categoría:** API y funciones · **Versión en línea:** [www.webviewgold.com/es/docs/iOS/admob/](https://www.webviewgold.com/es/docs/iOS/admob/)

---

AdMob es un servicio de Google para monetizar aplicaciones móviles en las plataformas iOS y Android. Permite a los desarrolladores integrar anuncios de banner, intersticiales y recompensados, que se pagan por clics (CPC, coste por clic) o impresiones (CPM, coste por mil). WebViewGold simplifica la integración de AdMob y permite una configuración rápida para mostrar anuncios en su aplicación iOS basada en WebView.

[![Ver el vídeo: API de anuncios AdMob](https://img.youtube.com/vi/7j7NW5CTwqo/hqdefault.jpg)](https://www.youtube.com/watch?v=7j7NW5CTwqo)

**Paso 1:** Abra el archivo **Info.plist** y establezca el ID global de su cuenta de AdMob en el campo *GADApplicationIdentifier*:\
![Añada su ID de cuenta de AdMob al proyecto](../../assets/ios/img/admobglobal.webp)

**Paso 2:** Inserte sus IDs de AdMob en el archivo **Config.swift** para `AdmobBannerID`, `AdmobinterstitialID` y `AdmobRewardedID`:\
![Active bloques específicos de banners de AdMob en su aplicación](../../assets/ios/img/admobconstants.webp)

**Paso 3:** Dentro de **Config.swift** puede:

- **Activar o desactivar** anuncios de banner y/o intersticiales estableciendo `showBannerAd` en `true` para banners y `showFullScreenAd` en `true` para anuncios intersticiales.
- **Definir intervalos** para mostrar anuncios intersticiales cambiando `showadAfterX` al número deseado de interacciones con la web antes de reproducir un anuncio intersticial.

**Para activar los anuncios recompensados** *(solo disponibles para versiones de iOS superiores a 13.0)***:** Establezca `enableRewardedAds` en `true`.

Para reproducir un anuncio recompensado, utilice una llamada a nuestra funcionalidad de API de anuncios recompensados.

```html
<a href="displayrewardedad://>Display Rewarded Advertisement</a>
```

Una vez completada la visualización íntegra de un anuncio, se enviará a su sitio web una llamada a la función JavaScript **updateRewardedStatus('true');**. Debe implementar esta función en su código JavaScript, ya que es usted quien decide cómo recompensar al usuario.

WebViewGold admite mostrar anuncios recompensados como opción publicitaria predeterminada, sobrescribiendo las opciones intersticiales. Para que esto ocurra, establezca `useRewardedAdsWherePossible` y `showFullScreenAd` en `true`.

**Consejo:** Si muestra anuncios intersticiales después de X toques (`incrementWithTaps` en `true`), también puede aumentar el contador de toques manualmente desde su aplicación web llamando a `increasetapcounter://` — útil para contar solo interacciones específicas para el intervalo de anuncios.

*Para más información, consulte también la [documentación oficial del SDK de AdMob](https://developers.google.com/admob/) (pero omita las partes de configuración, ya que WebViewGold ya incluye el framework).*

---

## Seguir leyendo

- ← Anterior: [API de notificaciones push](push-notifications.md)
- Siguiente →: [API de anuncios Facebook](facebook-ads.md)
- La misma función en otras plataformas: [Android – API de anuncios AdMob](../android/admob.md)
- Idiomas: [🇺🇸 English](../../ios/admob.md) · [🇩🇪 Deutsch](../../de/ios/admob.md) · [🇫🇷 Français](../../fr/ios/admob.md) · **🇪🇸 Español** · [🇨🇳 中文](../../zh/ios/admob.md)

> [!TIP]
> **¿Sin tiempo? Configuramos su app por usted.** Nuestro equipo configura, compila & publica su app WebViewGold: llave en mano, entrega rápida, Made in Germany. [Configurar mi app →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **Compile en su navegador:** Sin Mac ni IDE: el **WebViewGold Cloud Builder** configura, compila & sube su app en línea. [Descubra Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
