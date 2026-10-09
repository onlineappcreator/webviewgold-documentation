---
title: "API de lectura/escritura de valores – Documentación de WebViewGold para iOS"
description: "Almacene de forma persistente un valor de cadena en el dispositivo y léalo de nuevo en el JavaScript de su aplicación web."
lang: "es"
product: "WebViewGold para iOS"
platform: "iOS"
category: "API y funciones"
slug: "read-write-value"
canonical_url: "https://www.webviewgold.com/es/docs/iOS/read-write-value/"
keywords:
  - "API de lectura/escritura de valores"
  - "WebViewGold para iOS"
  - "convertir sitio web en app"
  - "documentación de app WebView"
  - "SDK WebView de iOS"
  - "PWA a app"
  - "HTML a app"
  - "puente de JavaScript"
last_updated: "2026-10-09"
---

# API de lectura/escritura de valores – WebViewGold para iOS

> **Resumen:** Almacene de forma persistente un valor de cadena en el dispositivo y léalo de nuevo en el JavaScript de su aplicación web.

[Documentación](../README.md) › [WebViewGold para iOS](README.md) › API de lectura/escritura de valores

**Plataforma:** iOS · **Categoría:** API y funciones · **Versión en línea:** [www.webviewgold.com/es/docs/iOS/read-write-value/](https://www.webviewgold.com/es/docs/iOS/read-write-value/)

---

La **API de lectura/escritura de valores** almacena de forma persistente una cadena arbitraria en el dispositivo (en el almacenamiento privado de la aplicación) y la vuelve a leer en su JavaScript. Los valores sobreviven a reinicios de la aplicación y a limpiezas de caché, salvo que se desinstale la aplicación.

## Escribir un valor

Todo lo que sigue a `writevalue://` se guarda tal cual como una única cadena. Diseñe su propio formato (query-string, JSON, CSV, lo que encaje con su aplicación web):

```html
<a href="writevalue://darkmode=on;user=42">Guardar</a>
```

## Leer un valor

Cuando se activa `readvalue://`, la aplicación inyecta la cadena almacenada de nuevo en el WebView como `window.storedValues` para que su JavaScript pueda leerla:

```html
<a href="readvalue://" onclick="setTimeout(showSettings, 200)">Cargar</a>
<script>
  function showSettings() {
    console.log(window.storedValues || "todavía sin ajustes");
  }
</script>
```

## Casos de uso típicos

- Recordar el tema, el idioma o el estado de onboarding de un usuario sin conexión.
- Guardar un token de sesión cuando no puede confiar en las cookies.
- Persistir una pequeña preferencia local sin una llamada al backend.

**Notas:** Los valores son por instalación de la aplicación y por dispositivo: **no** se sincronizan entre dispositivos. Mantenga los valores pequeños; esta API está pensada para ajustes, no para almacenar blobs.

---

## Seguir leyendo

- ← Anterior: [API de Portapapeles](clipboard.md)
- Siguiente →: [API para abrir los ajustes](open-app-settings.md)
- La misma función en otras plataformas: [Android – Read/Write Value API](../android/read-write-value.md)
- Idiomas: [🇺🇸 English](../../ios/read-write-value.md) · [🇩🇪 Deutsch](../../de/ios/read-write-value.md) · [🇫🇷 Français](../../fr/ios/read-write-value.md) · **🇪🇸 Español** · [🇨🇳 中文](../../zh/ios/read-write-value.md)

> [!TIP]
> **¿Sin tiempo? Configuramos su app por usted.** Nuestro equipo configura, compila & publica su app WebViewGold: llave en mano, entrega rápida, Made in Germany. [Configurar mi app →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **Compile en su navegador:** Sin Mac ni IDE: el **WebViewGold Cloud Builder** configura, compila & sube su app en línea. [Descubra Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
