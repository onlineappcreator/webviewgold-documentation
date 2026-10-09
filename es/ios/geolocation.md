---
title: "API de geolocalización HTML5 – Documentación de WebViewGold para iOS"
description: "Active la geolocalización HTML5 en su app WebView de iOS y solicite los permisos de ubicación precisa de la manera correcta."
lang: "es"
product: "WebViewGold para iOS"
platform: "iOS"
category: "API y funciones"
slug: "geolocation"
canonical_url: "https://www.webviewgold.com/es/docs/iOS/geolocation/"
keywords:
  - "API de geolocalización"
  - "WebViewGold para iOS"
  - "convertir sitio web en app"
  - "documentación de app WebView"
  - "SDK WebView de iOS"
  - "PWA a app"
  - "HTML a app"
  - "puente de JavaScript"
last_updated: "2026-10-09"
---

# API de geolocalización HTML5 – WebViewGold para iOS

> **Resumen:** Active la geolocalización HTML5 en su app WebView de iOS y solicite los permisos de ubicación precisa de la manera correcta.

[Documentación](../README.md) › [WebViewGold para iOS](README.md) › API de geolocalización

**Plataforma:** iOS · **Categoría:** API y funciones · **Versión en línea:** [www.webviewgold.com/es/docs/iOS/geolocation/](https://www.webviewgold.com/es/docs/iOS/geolocation/)

---

La API de Geolocalización HTML5 permite a los usuarios compartir su ubicación con su aplicación, mejorando funciones como el contenido basado en la ubicación. En WebViewGold, la API de Geolocalización se admite de forma predeterminada una vez integrada en su contenido web. Así se implementa el seguimiento de geolocalización en su aplicación iOS basada en WebView:

## Configuración de la geolocalización HTML5

Para la configuración básica de geolocalización, consulte la [guía de Geolocalización de Mozilla](https://developer.mozilla.org/en-US/docs/Web/API/Geolocation_API) para obtener detalles sobre cómo implementar esta función en su sitio web o aplicación web.

Para ver una demostración, visite esta [demo de Geolocalización de W3Schools](https://www.w3schools.com/html/html5_geolocation.asp).

Desde iOS 10, la geolocalización solo está disponible en sitios HTTPS, así que asegúrese de usar una URL de aplicación web que empiece por `https://` en lugar de `http://` cuando utilice solicitudes de ubicación.

## Acceso a la ubicación en segundo plano

De forma predeterminada, las solicitudes de ubicación solo funcionan mientras la app está en primer plano. Si su app web necesita seguir recibiendo actualizaciones de ubicación mientras la app está en segundo plano (p. ej., para casos de uso de seguimiento o geovallado), active la opción de ubicación en segundo plano en **Config.swift**:

```swift
static let backgroundlocation = true
```

- En la configuración del proyecto de Xcode, añada la capacidad **Background Modes** al target de WebViewGold y marque **Location updates**.
- Según su app web, puede que además necesite activar **Background Processing**. En ese caso, añada también un array con la clave `Permitted background task scheduler identifiers` a su **Info.plist** e incluya una cadena con el identificador de paquete de su app (p. ej., `com.yourcompany.yourapp`).
- Tenga en cuenta que el acceso a la ubicación en segundo plano requiere una justificación clara durante la revisión de la App Store: describa el beneficio para el usuario en sus notas de revisión.

---

## Seguir leyendo

- ← Anterior: [Modificar la Safe Area](safe-area.md)
- Siguiente →: [API de notificaciones push](push-notifications.md)
- La misma función en otras plataformas: [Android – API de geolocalización](../android/geolocation.md)
- Idiomas: [🇺🇸 English](../../ios/geolocation.md) · [🇩🇪 Deutsch](../../de/ios/geolocation.md) · [🇫🇷 Français](../../fr/ios/geolocation.md) · **🇪🇸 Español** · [🇨🇳 中文](../../zh/ios/geolocation.md)

> [!TIP]
> **¿Sin tiempo? Configuramos su app por usted.** Nuestro equipo configura, compila & publica su app WebViewGold: llave en mano, entrega rápida, Made in Germany. [Configurar mi app →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **Compile en su navegador:** Sin Mac ni IDE: el **WebViewGold Cloud Builder** configura, compila & sube su app en línea. [Descubra Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
