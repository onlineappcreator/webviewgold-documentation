---
title: "API UUID – Documentación de WebViewGold para iOS"
description: "Identifique las instalaciones de la app con un UUID único añadido a su URL de WebView u obtenido mediante JavaScript."
lang: "es"
product: "WebViewGold para iOS"
platform: "iOS"
category: "API y funciones"
slug: "uuid"
canonical_url: "https://www.webviewgold.com/es/docs/iOS/uuid/"
keywords:
  - "API UUID"
  - "WebViewGold para iOS"
  - "convertir sitio web en app"
  - "documentación de app WebView"
  - "SDK WebView de iOS"
  - "PWA a app"
  - "HTML a app"
  - "puente de JavaScript"
last_updated: "2026-10-09"
---

# API UUID – WebViewGold para iOS

> **Resumen:** Identifique las instalaciones de la app con un UUID único añadido a su URL de WebView u obtenido mediante JavaScript.

[Documentación](../README.md) › [WebViewGold para iOS](README.md) › API UUID

**Plataforma:** iOS · **Categoría:** API y funciones · **Versión en línea:** [www.webviewgold.com/es/docs/iOS/uuid/](https://www.webviewgold.com/es/docs/iOS/uuid/)

---

La API de UUID de WebViewGold le permite obtener un ID de dispositivo único y no personal (UUID, "Universally Unique Identifier"), que puede **identificar de forma única un dispositivo iOS**. Esta función puede resultar útil para:

- Almacenar configuraciones específicas del usuario en el servidor
- Mantener los estados de sesión
- Recuperar los datos guardados en el lado del cliente

**Nota sobre privacidad:** Asegúrese de cumplir con las **leyes de privacidad** locales e internacionales al usar esta función, ya que implica la identificación del dispositivo.

## Cómo obtener el UUID

Para obtener el UUID desde su aplicación basada en WebView, utilice el siguiente código:

```html
<a href="get-uuid://">Get UUID</a>
<a href="#" onClick="alert(uuid);">Show UUID</a>
```

- **Get UUID:** Solicita el UUID a WebViewGold.
- **Show UUID:** Muestra el UUID mediante una **alerta** para facilitar las pruebas.

## Método alternativo: añadir el UUID a la URL del WebView

Si prefiere incluir el UUID en los parámetros de la URL, habilite la opción `enhanceUrlUUID` en **Config.swift** estableciéndola en `true`. Esto añadirá automáticamente `uuid=XYZ` a la URL de su WebView en la primera solicitud, lo que le permitirá acceder al UUID directamente en su contenido web:

- **Ejemplo:** Si la URL de su WebView es `https://www.example.org`, se solicitará como `https://www.example.org?uuid=XYZ`.
- **Nota:** Solo la solicitud inicial de la URL incluirá este parámetro GET, por lo que conviene guardarlo en una sesión o cookie si necesita consultarlo más adelante en la aplicación.

## Inyectar automáticamente el UUID en JavaScript

Para hacer que el UUID (y otras variables) estén disponibles automáticamente en JavaScript en todas las páginas sin modificar las URL, establezca `autoInjectVariable` en `true` en **Config.swift**. Esto le permite acceder al UUID y a otros valores directamente dentro de cualquier página.

---

## Seguir leyendo

- ← Anterior: [API de pases de Apple Wallet](wallet-pass.md)
- Siguiente →: [API de linterna](flashlight.md)
- La misma función en otras plataformas: [Android – API de UUID](../android/uuid.md) · [macOS – API UUID](../macos/uuid.md)
- Idiomas: [🇺🇸 English](../../ios/uuid.md) · [🇩🇪 Deutsch](../../de/ios/uuid.md) · [🇫🇷 Français](../../fr/ios/uuid.md) · **🇪🇸 Español** · [🇨🇳 中文](../../zh/ios/uuid.md)

> [!TIP]
> **¿Sin tiempo? Configuramos su app por usted.** Nuestro equipo configura, compila & publica su app WebViewGold: llave en mano, entrega rápida, Made in Germany. [Configurar mi app →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **Compile en su navegador:** Sin Mac ni IDE: el **WebViewGold Cloud Builder** configura, compila & sube su app en línea. [Descubra Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
