---
title: "API de UI dinámica – Documentación de WebViewGold para iOS"
description: "Cambie dinámicamente elementos de UI nativos, como los colores de la barra de estado o la barra inferior, desde su aplicación web."
lang: "es"
product: "WebViewGold para iOS"
platform: "iOS"
category: "API y funciones"
slug: "dynamic-ui"
canonical_url: "https://www.webviewgold.com/es/docs/iOS/dynamic-ui/"
keywords:
  - "API de UI dinámica"
  - "WebViewGold para iOS"
  - "convertir sitio web en app"
  - "documentación de app WebView"
  - "SDK WebView de iOS"
  - "PWA a app"
  - "HTML a app"
  - "puente de JavaScript"
last_updated: "2026-10-09"
---

# API de UI dinámica – WebViewGold para iOS

> **Resumen:** Cambie dinámicamente elementos de UI nativos, como los colores de la barra de estado o la barra inferior, desde su aplicación web.

[Documentación](../README.md) › [WebViewGold para iOS](README.md) › API de UI dinámica

**Plataforma:** iOS · **Categoría:** API y funciones · **Versión en línea:** [www.webviewgold.com/es/docs/iOS/dynamic-ui/](https://www.webviewgold.com/es/docs/iOS/dynamic-ui/)

---

WebViewGold le permite personalizar dinámicamente los elementos de la interfaz de usuario en su aplicación web. Estos elementos pueden incluir la barra de estado, la barra inferior (iOS), la barra de navegación (Android) y el gesto de tirar para actualizar (iOS). WebViewGold incluye los siguientes comandos para personalizar dinámicamente estos elementos:

- **statusbarcolor://**
  - El COMANDO MAESTRO para cambiar el color de la barra de estado y de otras características relevantes de la interfaz automáticamente, como el color del texto de la barra de estado, el color de la barra inferior (iOS), el color de la barra de navegación (Android), etc.
- **statusbartextcolor://**
  - Le permite cambiar manualmente el color del texto de la barra de estado (iOS y Android).
- **bottombarcolor://**
  - Si existe un elemento de interfaz de barra inferior (iOS) o barra de navegación (Android), le permite cambiar manualmente su color.
- **hidebars://**
  - Le permite ocultar el fondo de la barra de estado, cuyo texto permanece sobre un fondo transparente.

## Cambiar el color de la barra de estado (y de otros elementos de la interfaz automáticamente)

Esta función admite una entrada de color con el siguiente formato:

- RGB = {red, green, blue}

Donde los valores son números enteros entre 0 (mínimo) y 255 (máximo).

Utilice JavaScript con este tipo de URL para cambiar el color de la barra de estado:

```html
<script>
// Example: red
window.location.href = "statusbarcolor://255,0,0";
</script>
```

Cuando cambie el color de la barra de estado, el texto de la barra de estado cambiará automáticamente a un color adecuado (blanco o negro) según lo oscuro que sea el color.\
Las funciones opcionales de la interfaz como *Pull To Refresh* (iOS), la *barra inferior* (iOS) y la *barra de navegación* (Android) también ajustarán sus colores automáticamente.

## Cambiar el color del texto de la barra de estado

Si desea elegir manualmente el color del texto de la barra de estado, puede hacerlo utilizando esta opción.

Esta función admite una entrada de texto con las siguientes opciones:

- "white"
- "black"

Utilice JavaScript con este tipo de URL para cambiar el color del texto de la barra de estado:

```html
<script>
// Example: white text
window.location.href = "statusbartextcolor://white";
// Example: black text
window.location.href = "statusbartextcolor://black";
</script>
```

## Cambiar el color de la barra inferior

Esta función admite una entrada de color con el siguiente formato:

- RGB = {red, green, blue}

Donde los valores son números enteros entre 0 (mínimo) y 255 (máximo).

Utilice JavaScript con este tipo de URL para cambiar el color de la barra de estado:

```html
<script>
// Example: red
window.location.href = "bottombarcolor://255,0,0";
</script>
```

## Ocultar la barra de estado

La funcionalidad hidebars puede estar **activada** o **desactivada**.

Tenga en cuenta que el texto de la barra de estado, como la hora y el porcentaje de batería, seguirán siendo visibles para el usuario,
pero el fondo que rodea al texto se vuelve transparente y el WebView se expande para ocupar el espacio dejado.

Utilice JavaScript para cambiar el estado de visibilidad de la barra:

```html
<script>
// Example: hide the bars from view
window.location.href = "hidebars://on";
// Example: redisplay the bars after being hidden
window.location.href = "hidebars://off";
</script>
```

---

## Seguir leyendo

- ← Anterior: [API de comprobación de versión](app-version-check.md)
- Siguiente →: [API de icono de app dinámico](dynamic-app-icon.md)
- La misma función en otras plataformas: [Android – API de interfaz dinámica](../android/dynamic-ui.md)
- Idiomas: [🇺🇸 English](../../ios/dynamic-ui.md) · [🇩🇪 Deutsch](../../de/ios/dynamic-ui.md) · [🇫🇷 Français](../../fr/ios/dynamic-ui.md) · **🇪🇸 Español** · [🇨🇳 中文](../../zh/ios/dynamic-ui.md)

> [!TIP]
> **¿Sin tiempo? Configuramos su app por usted.** Nuestro equipo configura, compila & publica su app WebViewGold: llave en mano, entrega rápida, Made in Germany. [Configurar mi app →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **Compile en su navegador:** Sin Mac ni IDE: el **WebViewGold Cloud Builder** configura, compila & sube su app en línea. [Descubra Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
