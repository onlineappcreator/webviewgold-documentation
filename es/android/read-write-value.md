---
title: "Read/Write Value API – Documentación de WebViewGold para Android"
description: "Persist small strings on the device from JavaScript and read them back — for theme, language, session tokens, or onboarding state."
lang: "es"
product: "WebViewGold para Android"
platform: "Android"
category: "API y funciones"
slug: "read-write-value"
canonical_url: "https://www.webviewgold.com/es/docs/android/read-write-value/"
keywords:
  - "Read/Write Value API"
  - "WebViewGold para Android"
  - "convertir sitio web en app"
  - "documentación de app WebView"
  - "SDK WebView de Android"
  - "PWA a app"
  - "HTML a app"
  - "puente de JavaScript"
last_updated: "2026-10-09"
---

# Read/Write Value API – WebViewGold para Android

> **Resumen:** Persist small strings on the device from JavaScript and read them back — for theme, language, session tokens, or onboarding state.

[Documentación](../README.md) › [WebViewGold para Android](README.md) › Read/Write Value API

**Plataforma:** Android · **Categoría:** API y funciones · **Versión en línea:** [www.webviewgold.com/es/docs/android/read-write-value/](https://www.webviewgold.com/es/docs/android/read-write-value/)

---

La **API de lectura/escritura de valores** almacena de forma persistente una cadena arbitraria en el dispositivo (a través del almacenamiento privado de la app) y la vuelve a leer en su JavaScript. Los valores sobreviven a los reinicios de la app y a la eliminación de la caché, salvo que el sistema operativo borre los datos de la aplicación.

## Escritura de un valor

Todo lo que aparece después de `writevalue://` se almacena literalmente como una única cadena. Diseñe su propio formato (cadena de consulta, JSON, CSV, lo que mejor se adapte a su aplicación web):

```html
<a href="writevalue://darkmode=on;user=42">Save</a>
```

## Lectura de un valor

Cuando se activa `readvalue://`, la app inyecta la cadena almacenada de vuelta en el WebView para que su JavaScript pueda leerla:

```html
<a href="readvalue://" onclick="setTimeout(showSettings, 200)">Load</a>
<script>
  function showSettings() {
    console.log(window.appSettings || "no settings yet");
  }
</script>
```

## Casos de uso típicos

- Recordar el tema, el idioma o el estado de incorporación de un usuario sin conexión.
- Almacenar en caché un token de sesión cuando no puede confiar en las cookies.
- Persistir una pequeña preferencia local sin necesidad de un viaje de ida y vuelta al backend.

**Notas:** Los valores son específicos de cada instalación de la app y de cada dispositivo: **no** se sincronizan entre dispositivos. Mantenga los valores pequeños; esta API está pensada para configuraciones, no para almacenamiento de blobs.

---

## Seguir leyendo

- ← Anterior: [Reconnect API](reconnect.md)
- Siguiente →: [Biometric Auth API](biometric-auth.md)
- La misma función en otras plataformas: [iOS – API de lectura/escritura de valores](../ios/read-write-value.md)
- Idiomas: [🇺🇸 English](../../android/read-write-value.md) · [🇩🇪 Deutsch](../../de/android/read-write-value.md) · [🇫🇷 Français](../../fr/android/read-write-value.md) · **🇪🇸 Español** · [🇨🇳 中文](../../zh/android/read-write-value.md)

> [!TIP]
> **¿Sin tiempo? Configuramos su app por usted.** Nuestro equipo configura, compila & publica su app WebViewGold: llave en mano, entrega rápida, Made in Germany. [Configurar mi app →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_android_doc_online)
>
> **Compile en su navegador:** Sin Mac ni IDE: el **WebViewGold Cloud Builder** configura, compila & sube su app en línea. [Descubra Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=android_docs)
