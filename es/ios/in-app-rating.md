---
title: "API del diálogo de valoración In-App – Documentación de WebViewGold para iOS"
description: "Pida a los usuarios una valoración en el App Store en el momento perfecto: active el diálogo de valoración nativo de iOS desde su aplicación web."
lang: "es"
product: "WebViewGold para iOS"
platform: "iOS"
category: "API y funciones"
slug: "in-app-rating"
canonical_url: "https://www.webviewgold.com/es/docs/iOS/in-app-rating/"
keywords:
  - "API del diálogo de valoración"
  - "WebViewGold para iOS"
  - "convertir sitio web en app"
  - "documentación de app WebView"
  - "SDK WebView de iOS"
  - "PWA a app"
  - "HTML a app"
  - "puente de JavaScript"
last_updated: "2026-10-09"
---

# API del diálogo de valoración In-App – WebViewGold para iOS

> **Resumen:** Pida a los usuarios una valoración en el App Store en el momento perfecto: active el diálogo de valoración nativo de iOS desde su aplicación web.

[Documentación](../README.md) › [WebViewGold para iOS](README.md) › API del diálogo de valoración

**Plataforma:** iOS · **Categoría:** API y funciones · **Versión en línea:** [www.webviewgold.com/es/docs/iOS/in-app-rating/](https://www.webviewgold.com/es/docs/iOS/in-app-rating/)

---

Las reseñas positivas en el App Store son uno de los motores de crecimiento más potentes para su aplicación. La **API del diálogo de valoración In-App** de WebViewGold le permite pedir una valoración a sus usuarios justo en el momento adecuado, por ejemplo, justo después de una compra correcta o de completar una tarea en su aplicación web.

## Opción 1: diálogo de valoración nativo de iOS (predeterminado)

Llame a la siguiente URL desde un enlace HTML o desde JavaScript para mostrar el diálogo de valoración nativo **SKStoreReviewController**:

```html
<a href="rateapp://">¿Le gusta la app? ¡Valórenos!</a>
```

```javascript
window.location.href = "rateapp://";
```

**Nota:** Apple limita la frecuencia con la que puede mostrarse el diálogo de valoración nativo (unas tres veces al año por usuario), por lo que es posible que no aparezca en cada llamada; esto es intencionado y también se aplica durante el desarrollo.

## Opción 2: diálogo de valoración personalizado

Si prefiere un diálogo que aparezca siempre y que lleve al usuario a su página del App Store, configúrelo en **Config.swift**:

- `showcustomrateappdialog` — establézcalo en `true` para mostrar un diálogo de valoración personalizado al activar `rateapp://` en lugar de intentar la llamada de reseña nativa.
- `ratemyappurl` — establezca la URL del App Store de su aplicación, p. ej. `https://apps.apple.com/app/idXXXXXXXXX?action=write-review`.

## Casos de uso típicos

- Pedir una reseña justo después de una interacción positiva (pedido completado, subida de nivel, reserva realizada).
- Mostrar primero su propio flujo «¿Le gusta la app?» en su sitio web y enviar solo a los usuarios satisfechos a `rateapp://`.

---

## Seguir leyendo

- ← Anterior: [API de diálogo para compartir](app-sharing-dialog.md)
- Siguiente →: [API de compras integradas](in-app-purchases.md)
- La misma función en otras plataformas: [Android – API de valoración In-App](../android/in-app-rating.md)
- Idiomas: [🇺🇸 English](../../ios/in-app-rating.md) · [🇩🇪 Deutsch](../../de/ios/in-app-rating.md) · [🇫🇷 Français](../../fr/ios/in-app-rating.md) · **🇪🇸 Español** · [🇨🇳 中文](../../zh/ios/in-app-rating.md)

> [!TIP]
> **¿Sin tiempo? Configuramos su app por usted.** Nuestro equipo configura, compila & publica su app WebViewGold: llave en mano, entrega rápida, Made in Germany. [Configurar mi app →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **Compile en su navegador:** Sin Mac ni IDE: el **WebViewGold Cloud Builder** configura, compila & sube su app en línea. [Descubra Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
