---
title: "API de UUID – Documentación de WebViewGold para Android"
description: "Identifique las instalaciones de la aplicación con un UUID único añadido a su URL de WebView u obtenido mediante JavaScript."
lang: "es"
product: "WebViewGold para Android"
platform: "Android"
category: "API y funciones"
slug: "uuid"
canonical_url: "https://www.webviewgold.com/es/docs/android/uuid/"
keywords:
  - "API de UUID"
  - "WebViewGold para Android"
  - "convertir sitio web en app"
  - "documentación de app WebView"
  - "SDK WebView de Android"
  - "PWA a app"
  - "HTML a app"
  - "puente de JavaScript"
last_updated: "2026-10-09"
---

# API de UUID – WebViewGold para Android

> **Resumen:** Identifique las instalaciones de la aplicación con un UUID único añadido a su URL de WebView u obtenido mediante JavaScript.

[Documentación](../README.md) › [WebViewGold para Android](README.md) › API de UUID

**Plataforma:** Android · **Categoría:** API y funciones · **Versión en línea:** [www.webviewgold.com/es/docs/android/uuid/](https://www.webviewgold.com/es/docs/android/uuid/)

---

La API UUID de WebViewGold le permite obtener mediante JavaScript un identificador único de dispositivo no personal (UUID, del inglés "Universally Unique Identifier") con el que se puede identificar de forma unívoca un dispositivo Android. Esta función puede resultar útil para:

- Almacenar ajustes específicos del usuario en el servidor
- Mantener el estado de la sesión
- Recuperar datos guardados en el lado del cliente

**Nota sobre privacidad:** asegúrese de cumplir con las leyes de privacidad locales e internacionales al utilizar esta función, ya que implica la identificación del dispositivo.

## Cómo obtener el UUID

Para obtener el UUID desde su app basada en WebView, utilice el siguiente código:

```html
<a href="get-uuid://">Get UUID</a>
<a href="#" onClick="alert(uuid);">Show UUID</a>
```

- **Obtener UUID:** solicita el UUID a WebViewGold.
- **Mostrar UUID:** muestra el UUID mediante un **alert** para facilitar las pruebas.

## Método alternativo: añadir el UUID a la URL de la WebView

Si prefiere incluir el UUID en los parámetros de la URL, active la opción `UUID_ENHANCE_WEBVIEW_URL` en **Config.java** estableciéndola en `true`. Esto añadirá automáticamente `uuid=XYZ` a su URL de WebView en la primera solicitud, lo que le permitirá acceder al UUID directamente en su contenido web:

- **Ejemplo:** si su URL de WebView es `https://www.example.org`, se solicitará como `https://www.example.org?uuid=XYZ`.
- **Nota:** solo la primera solicitud de URL incluirá este parámetro GET, por lo que conviene guardarlo en una sesión o cookie si necesita referenciarlo más adelante dentro de la app.

## Inyectar automáticamente el UUID en JavaScript

Para hacer que el UUID (y otras variables) esté disponible automáticamente en JavaScript en todas las páginas sin modificar las URLs, establezca `AUTO_INJECT_VARIABLES` en `true` en **Config.java**. Esto le permitirá acceder al UUID y a otros valores directamente dentro de cualquier página.

---

## Seguir leyendo

- ← Anterior: [API de portapapeles](clipboard.md)
- Siguiente →: [API de linterna](flashlight.md)
- La misma función en otras plataformas: [iOS – API UUID](../ios/uuid.md) · [macOS – API UUID](../macos/uuid.md)
- Idiomas: [🇺🇸 English](../../android/uuid.md) · [🇩🇪 Deutsch](../../de/android/uuid.md) · [🇫🇷 Français](../../fr/android/uuid.md) · **🇪🇸 Español** · [🇨🇳 中文](../../zh/android/uuid.md)

> [!TIP]
> **¿Sin tiempo? Configuramos su app por usted.** Nuestro equipo configura, compila & publica su app WebViewGold: llave en mano, entrega rápida, Made in Germany. [Configurar mi app →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_android_doc_online)
>
> **Compile en su navegador:** Sin Mac ni IDE: el **WebViewGold Cloud Builder** configura, compila & sube su app en línea. [Descubra Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=android_docs)
