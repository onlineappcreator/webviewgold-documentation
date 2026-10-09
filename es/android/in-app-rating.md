---
title: "API del diálogo de valoración In-App – Documentación de WebViewGold para Android"
description: "Pida a sus usuarios una reseña en Google Play: active el diálogo nativo \"Valorar esta app\" mediante rateapp:// desde su web app o deje que WebViewGold lo muestre automáticamente."
lang: "es"
product: "WebViewGold para Android"
platform: "Android"
category: "API y funciones"
slug: "in-app-rating"
canonical_url: "https://www.webviewgold.com/es/docs/android/in-app-rating/"
keywords:
  - "API de valoración In-App"
  - "WebViewGold para Android"
  - "convertir sitio web en app"
  - "documentación de app WebView"
  - "SDK WebView de Android"
  - "PWA a app"
  - "HTML a app"
  - "puente de JavaScript"
last_updated: "2026-10-09"
---

# API del diálogo de valoración In-App – WebViewGold para Android

> **Resumen:** Pida a sus usuarios una reseña en Google Play: active el diálogo nativo "Valorar esta app" mediante rateapp:// desde su web app o deje que WebViewGold lo muestre automáticamente.

[Documentación](../README.md) › [WebViewGold para Android](README.md) › API de valoración In-App

**Plataforma:** Android · **Categoría:** API y funciones · **Versión en línea:** [www.webviewgold.com/es/docs/android/in-app-rating/](https://www.webviewgold.com/es/docs/android/in-app-rating/)

---

Las reseñas positivas en Google Play son uno de los motores de crecimiento más potentes para su aplicación. La **API del diálogo de valoración In-App** de WebViewGold le permite pedir una valoración a sus usuarios en el momento exacto — por ejemplo, justo después de una compra exitosa o de completar una tarea en su web app.

## Opción 1: Activar el diálogo de valoración manualmente desde su web app

Llame a la siguiente URL desde un enlace HTML o desde JavaScript para mostrar un diálogo nativo de "Valorar esta app":

```html
<a href="rateapp://">¿Le gusta la app? ¡Valórenos!</a>
```

```javascript
window.location.href = "rateapp://";
```

Si el usuario confirma el diálogo, se abre la página de Google Play de su aplicación para que pueda dejar una reseña. Para que esto funcione, configure `RATE_MY_APP_URL` en **Config.java** con la URL de Google Play de su aplicación:

```java
public static final String RATE_MY_APP_URL = "https://play.google.com/store/apps/details?id=com.yourcompany.yourapp";
```

**Nota:** Si `RATE_MY_APP_URL` está vacío, las llamadas a `rateapp://` se ignoran. El título y el mensaje del diálogo se pueden personalizar mediante las entradas `rate_title` y `rate_message` en **strings.xml**.

## Opción 2: Dejar que WebViewGold pregunte automáticamente

WebViewGold también puede mostrar automáticamente la solicitud de "Valorar esta app" después de que el usuario haya utilizado su aplicación durante un tiempo. Configure este comportamiento en **Config.java**:

- `SHOW_RATE_DIALOG` — establézcalo en `true` para activar la solicitud automática de valoración (o en `false` para desactivarla).
- `RATE_DAYS_UNTIL_PROMPT` — número mínimo de días tras la instalación antes de mostrar la solicitud.
- `RATE_LAUNCHES_UNTIL_PROMPT` — número mínimo de inicios de la aplicación antes de mostrar la solicitud.

## Casos de uso típicos

- Pedir una reseña justo después de una interacción positiva (pedido completado, subida de nivel, reserva exitosa).
- Mostrar primero su propio flujo "¿Le gusta la app?" en su sitio web y enviar solo a los usuarios satisfechos a `rateapp://`.

---

## Seguir leyendo

- ← Anterior: [API de diálogo para compartir](app-sharing-dialog.md)
- Siguiente →: [API de compras integradas](in-app-purchases.md)
- La misma función en otras plataformas: [iOS – API del diálogo de valoración](../ios/in-app-rating.md)
- Idiomas: [🇺🇸 English](../../android/in-app-rating.md) · [🇩🇪 Deutsch](../../de/android/in-app-rating.md) · [🇫🇷 Français](../../fr/android/in-app-rating.md) · **🇪🇸 Español** · [🇨🇳 中文](../../zh/android/in-app-rating.md)

> [!TIP]
> **¿Sin tiempo? Configuramos su app por usted.** Nuestro equipo configura, compila & publica su app WebViewGold: llave en mano, entrega rápida, Made in Germany. [Configurar mi app →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_android_doc_online)
>
> **Compile en su navegador:** Sin Mac ni IDE: el **WebViewGold Cloud Builder** configura, compila & sube su app en línea. [Descubra Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=android_docs)
