---
title: "Multi API Call (multiapicall://) – Documentación de WebViewGold para Android"
description: "Llame a varias APIs de datos de WebViewGold en una sola asignación de window.location.href — ideal para web apps multiplataforma que también usan la versión de iOS."
lang: "es"
product: "WebViewGold para Android"
platform: "Android"
category: "API y funciones"
slug: "multi-api-call"
canonical_url: "https://www.webviewgold.com/es/docs/android/multi-api-call/"
keywords:
  - "Multi API Call"
  - "WebViewGold para Android"
  - "convertir sitio web en app"
  - "documentación de app WebView"
  - "SDK WebView de Android"
  - "PWA a app"
  - "HTML a app"
  - "puente de JavaScript"
last_updated: "2026-10-09"
---

# Multi API Call (multiapicall://) – WebViewGold para Android

> **Resumen:** Llame a varias APIs de datos de WebViewGold en una sola asignación de window.location.href — ideal para web apps multiplataforma que también usan la versión de iOS.

[Documentación](../README.md) › [WebViewGold para Android](README.md) › Multi API Call

**Plataforma:** Android · **Categoría:** API y funciones · **Versión en línea:** [www.webviewgold.com/es/docs/android/multi-api-call/](https://www.webviewgold.com/es/docs/android/multi-api-call/)

---

La **función Multi API Call** le permite activar **varias APIs de WebViewGold en una sola asignación de *window.location.href***. Es especialmente útil para **aplicaciones web multiplataforma**: los navegadores basados en Apple procesan varios redireccionamientos de página en el mismo script de forma diferente a Android — llamar a *window.location.href = "exampleAPItrigger"* varias veces en el mismo script funciona en Android, pero no en iOS. Con `multiapicall://`, el mismo código web funciona en ambas plataformas.

## APIs compatibles como entradas

- [get-uuid](uuid.md)
- [getonesignalplayerid](push-notifications.md)
- [getappversion](app-version-check.md)
- [statusbarcolor](dynamic-ui.md) (seguido de tres entradas para los valores RGB)
- [statusbartextcolor](dynamic-ui.md) (seguido de una entrada: `black` o `white`)
- [bottombarcolor](dynamic-ui.md) (seguido de tres entradas para los valores RGB)
- [navbartextcolor](dynamic-ui.md) (seguido de una entrada: `black` o `white`)

## Cómo usarlo

Separe los nombres de las APIs (y sus valores, si los hay) con comas (`,`) — **sin espacios**:

```html
<script>
// Combinación de ejemplo: "getonesignalplayerid" y "getappversion"
window.location.href = "multiapicall://getonesignalplayerid,getappversion";
</script>
```

Así se pasan valores a las APIs de Dynamic UI:

```html
<script>
// Poner la barra de estado en rojo, su texto en blanco y obtener el UUID — todo en una sola llamada
window.location.href = "multiapicall://statusbarcolor,255,0,0,statusbartextcolor,white,get-uuid";
</script>
```

**Nota:** En Android también funciona llamar a las APIs individuales una tras otra (p. ej., `window.location.href = "get-uuid://";` seguido de `window.location.href = "getappversion://";`). Use `multiapicall://` si desea compartir una única base de código con la [versión de WebViewGold para iOS](../ios/multi-api-call.md).

Haga clic [aquí](https://webviewgoldtest.github.io/multiAPI.html) para ver una página web de demostración de esta función. Inspeccione la página para ver el código de ejemplo.

---

## Seguir leyendo

- ← Anterior: [API de CSS y JS personalizados](custom-css-js.md)
- Siguiente →: [API de geolocalización](geolocation.md)
- La misma función en otras plataformas: [iOS – Función MultiAPICall](../ios/multi-api-call.md)
- Idiomas: [🇺🇸 English](../../android/multi-api-call.md) · [🇩🇪 Deutsch](../../de/android/multi-api-call.md) · [🇫🇷 Français](../../fr/android/multi-api-call.md) · **🇪🇸 Español** · [🇨🇳 中文](../../zh/android/multi-api-call.md)

> [!TIP]
> **¿Sin tiempo? Configuramos su app por usted.** Nuestro equipo configura, compila & publica su app WebViewGold: llave en mano, entrega rápida, Made in Germany. [Configurar mi app →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_android_doc_online)
>
> **Compile en su navegador:** Sin Mac ni IDE: el **WebViewGold Cloud Builder** configura, compila & sube su app en línea. [Descubra Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=android_docs)
