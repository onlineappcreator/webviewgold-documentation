---
title: "Reconnect API – Documentación de WebViewGold para Android"
description: "Reload the last online URL from your offline / fallback HTML page — the perfect \"Try again\" button for your custom offline screen."
lang: "es"
product: "WebViewGold para Android"
platform: "Android"
category: "API y funciones"
slug: "reconnect"
canonical_url: "https://www.webviewgold.com/es/docs/android/reconnect/"
keywords:
  - "Reconnect API"
  - "WebViewGold para Android"
  - "convertir sitio web en app"
  - "documentación de app WebView"
  - "SDK WebView de Android"
  - "PWA a app"
  - "HTML a app"
  - "puente de JavaScript"
last_updated: "2026-10-09"
---

# Reconnect API – WebViewGold para Android

> **Resumen:** Reload the last online URL from your offline / fallback HTML page — the perfect "Try again" button for your custom offline screen.

[Documentación](../README.md) › [WebViewGold para Android](README.md) › Reconnect API

**Plataforma:** Android · **Categoría:** API y funciones · **Versión en línea:** [www.webviewgold.com/es/docs/android/reconnect/](https://www.webviewgold.com/es/docs/android/reconnect/)

---

La **API de reconexión** vuelve a cargar la última URL en línea en la que se encontraba el usuario antes de que su app recurriera a la página HTML sin conexión. Está diseñada como un botón «Intentar de nuevo» en su pantalla personalizada sin conexión o de respaldo.

## Cómo utilizarla

Añada el activador a su página sin conexión (normalmente `local-html/index.html`):

```html
<button onclick="window.location.href='reconnect://'">Try to reconnect</button>
```

## Cómo funciona

La app recuerda la última URL no auxiliar que se cargó correctamente. Cuando el usuario toca `reconnect://`, el WebView navega de nuevo a esa URL. Si la conectividad sigue caída, se muestra de nuevo su página de respaldo.

## Configuración relacionada

- `FALLBACK_USE_LOCAL_HTML_FOLDER_IF_OFFLINE` en **Config.java** debe estar en `true`, y necesita una página de respaldo `local-html/index.html` para que esta función tenga sentido.

---

## Seguir leyendo

- ← Anterior: [Open App Settings API](open-app-settings.md)
- Siguiente →: [Read/Write Value API](read-write-value.md)
- La misma función en otras plataformas: [iOS – API de reconexión](../ios/reconnect.md)
- Idiomas: [🇺🇸 English](../../android/reconnect.md) · [🇩🇪 Deutsch](../../de/android/reconnect.md) · [🇫🇷 Français](../../fr/android/reconnect.md) · **🇪🇸 Español** · [🇨🇳 中文](../../zh/android/reconnect.md)

> [!TIP]
> **¿Sin tiempo? Configuramos su app por usted.** Nuestro equipo configura, compila & publica su app WebViewGold: llave en mano, entrega rápida, Made in Germany. [Configurar mi app →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_android_doc_online)
>
> **Compile en su navegador:** Sin Mac ni IDE: el **WebViewGold Cloud Builder** configura, compila & sube su app en línea. [Descubra Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=android_docs)
