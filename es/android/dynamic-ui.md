---
title: "API de interfaz dinámica – Documentación de WebViewGold para Android"
description: "Cambie elementos de la interfaz nativa, como el color de la barra de estado, de forma dinámica desde su aplicación web en Android."
lang: "es"
product: "WebViewGold para Android"
platform: "Android"
category: "API y funciones"
slug: "dynamic-ui"
canonical_url: "https://www.webviewgold.com/es/docs/android/dynamic-ui/"
keywords:
  - "API de interfaz dinámica"
  - "WebViewGold para Android"
  - "convertir sitio web en app"
  - "documentación de app WebView"
  - "SDK WebView de Android"
  - "PWA a app"
  - "HTML a app"
  - "puente de JavaScript"
last_updated: "2026-10-09"
---

# API de interfaz dinámica – WebViewGold para Android

> **Resumen:** Cambie elementos de la interfaz nativa, como el color de la barra de estado, de forma dinámica desde su aplicación web en Android.

[Documentación](../README.md) › [WebViewGold para Android](README.md) › API de interfaz dinámica

**Plataforma:** Android · **Categoría:** API y funciones · **Versión en línea:** [www.webviewgold.com/es/docs/android/dynamic-ui/](https://www.webviewgold.com/es/docs/android/dynamic-ui/)

---

WebViewGold le permite personalizar dinámicamente los elementos de la interfaz de su app web. Estos elementos pueden ser la barra de estado, la barra inferior (iOS), la barra de navegación (Android) y el «deslizar para actualizar» (iOS). WebViewGold incluye los siguientes comandos para personalizar dinámicamente estos elementos:

- **statusbarcolor://**
  - El COMANDO PRINCIPAL para cambiar el color de la barra de estado y de cualquier otro elemento relevante de la interfaz de forma automática, como el color del texto de la barra de estado, el color de la barra inferior (iOS), el color de la barra de navegación (Android), etc.
- **statusbartextcolor://**
  - Le permite cambiar manualmente el color del texto de la barra de estado (iOS y Android).
- **bottombarcolor://**
  - Si existe un elemento de barra inferior (iOS) o de barra de navegación (Android), le permite cambiar su color manualmente.
- **navbartextcolor://**
  - Le permite cambiar manualmente el color del texto de la barra de navegación en Android. La petición se ignorará en iOS (la barra inferior de iOS no tiene texto).
- **hidebars://**
  - Le permite ocultar el fondo de la barra de estado y de navegación.

## Cambiar el color de la barra de estado (y de otros elementos de la interfaz automáticamente)

Esta función admite una entrada de color en el siguiente formato:

- RGB = {rojo, verde, azul}

Donde los valores son números enteros entre 0 (mín.) y 255 (máx.).

Utilice JavaScript con este tipo de URL para cambiar el color de la barra de estado:

```html
<script>
// Example: red
window.location.href = "statusbarcolor://255,0,0";
</script>
```

Cuando cambia el color de la barra de estado, el texto de la barra de estado cambiará automáticamente a un color adecuado (blanco o negro) según lo oscuro que sea el color.\
Los elementos opcionales de la interfaz como *Pull To Refresh* (iOS), la *barra inferior* (iOS) y la *barra de navegación* (Android) también ajustarán sus colores automáticamente.

## Cambiar el color del texto de la barra de estado

Si desea elegir manualmente el color del texto de la barra de estado, puede hacerlo con esta opción.

Esta función admite una entrada de texto para las siguientes opciones:

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

## Cambiar el color de la barra de navegación

Esta función admite una entrada de color en el siguiente formato:

- RGB = {rojo, verde, azul}

Donde los valores son números enteros entre 0 (mín.) y 255 (máx.).

Utilice JavaScript con este tipo de URL para cambiar el color de la barra de navegación:

```html
<script>
// Example: red
window.location.href = "bottombarcolor://255,0,0";
</script>
```

## Cambiar el color del texto de la barra de navegación

Si desea elegir manualmente el color del texto de la barra de navegación, puede hacerlo con esta opción. Tenga en cuenta que esta petición se ignorará en iOS.

Esta función admite una entrada de texto para las siguientes opciones:

- "white"
- "black"

Utilice JavaScript con este tipo de URL para cambiar el color del texto de la barra de navegación:

```html
<script>
// Example: white text
window.location.href = "navbartextcolor://white";
// Example: black text
window.location.href = "navbartextcolor://black";
</script>
```

## Ocultar la barra de estado y la barra inferior

La funcionalidad hidebars puede estar **on** u **off**.

Tenga en cuenta que el texto de la barra de estado, como la hora y el porcentaje de batería, *no* permanece visible para el usuario.
Sin embargo, se pueden volver a mostrar con un deslizamiento del usuario desde la parte superior.

Utilice JavaScript para cambiar el estado de visibilidad de la barra de estado y de navegación:

```html
<script>
// Example: hide the bars from view
window.location.href = "hidebars://on";
// Example: redisplay the bars after being hidden
window.location.href = "hidebars://off";
</script>
```

---

## Detectar el modo oscuro (variable JavaScript `isDarkMode`)

Para adaptar los colores dinámicos de su interfaz al tema del sistema del usuario, WebViewGold inyecta automáticamente la variable JavaScript `isDarkMode` (`true` o `false`) en cada página una vez cargada. Ejemplo:

```html
<script>
if (typeof isDarkMode !== "undefined" && isDarkMode) {
    // Modo oscuro: p. ej., establecer una barra de estado oscura
    window.location.href = "statusbarcolor://0,0,0";
    window.location.href = "statusbartextcolor://white";
} else {
    // Modo claro
    window.location.href = "statusbarcolor://255,255,255";
    window.location.href = "statusbartextcolor://black";
}
</script>
```

**Nota:** Como alternativa, puede usar la media query CSS estándar `prefers-color-scheme` en su web app. La variable inyectada `isDarkMode` resulta útil cuando desea activar las APIs de interfaz de WebViewGold descritas arriba desde JavaScript.

---

## Seguir leyendo

- ← Anterior: [API de contactos](contacts.md)
- Siguiente →: [API de respuesta háptica](haptic-feedback.md)
- La misma función en otras plataformas: [iOS – API de UI dinámica](../ios/dynamic-ui.md)
- Idiomas: [🇺🇸 English](../../android/dynamic-ui.md) · [🇩🇪 Deutsch](../../de/android/dynamic-ui.md) · [🇫🇷 Français](../../fr/android/dynamic-ui.md) · **🇪🇸 Español** · [🇨🇳 中文](../../zh/android/dynamic-ui.md)

> [!TIP]
> **¿Sin tiempo? Configuramos su app por usted.** Nuestro equipo configura, compila & publica su app WebViewGold: llave en mano, entrega rápida, Made in Germany. [Configurar mi app →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_android_doc_online)
>
> **Compile en su navegador:** Sin Mac ni IDE: el **WebViewGold Cloud Builder** configura, compila & sube su app en línea. [Descubra Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=android_docs)
