---
title: "Open App Settings API – Documentación de WebViewGold para Android"
description: "Send the user straight to the system App-info screen from your web app to manage permissions, notifications, storage, or force-stop your Android app."
lang: "es"
product: "WebViewGold para Android"
platform: "Android"
category: "API y funciones"
slug: "open-app-settings"
canonical_url: "https://www.webviewgold.com/es/docs/android/open-app-settings/"
keywords:
  - "Open App Settings API"
  - "WebViewGold para Android"
  - "convertir sitio web en app"
  - "documentación de app WebView"
  - "SDK WebView de Android"
  - "PWA a app"
  - "HTML a app"
  - "puente de JavaScript"
last_updated: "2026-10-09"
---

# Open App Settings API – WebViewGold para Android

> **Resumen:** Send the user straight to the system App-info screen from your web app to manage permissions, notifications, storage, or force-stop your Android app.

[Documentación](../README.md) › [WebViewGold para Android](README.md) › Open App Settings API

**Plataforma:** Android · **Categoría:** API y funciones · **Versión en línea:** [www.webviewgold.com/es/docs/android/open-app-settings/](https://www.webviewgold.com/es/docs/android/open-app-settings/)

---

La **API de apertura de la configuración de la app** de WebViewGold envía al usuario directamente a la pantalla del sistema **Información de la app** de su aplicación. Desde allí puede gestionar los permisos, las notificaciones, el almacenamiento o forzar la detención de la app, sin salir de su aplicación web para buscar en la configuración de Android.

## Cómo utilizarla

Active la pantalla desde un enlace HTML o desde JavaScript:

```html
<a href="settingsapp://">Open app settings</a>
```

```javascript
window.location.href = "settingsapp://";
```

## Casos de uso típicos

- El usuario denegó un permiso (cámara, micrófono, ubicación, notificaciones): envíelo directamente a la pantalla del sistema para volver a habilitarlo.
- Guíe al usuario para desactivar la optimización de la batería o borrar la caché desde el lado del sistema operativo.

**Notas:** Sin parámetros. Cualquier URL que empiece por `settingsapp://` activa la misma pantalla. Funciona en todas las versiones de Android compatibles.

---

## Seguir leyendo

- ← Anterior: [Plugin NFC](nfc.md)
- Siguiente →: [Reconnect API](reconnect.md)
- La misma función en otras plataformas: [iOS – API para abrir los ajustes](../ios/open-app-settings.md)
- Idiomas: [🇺🇸 English](../../android/open-app-settings.md) · [🇩🇪 Deutsch](../../de/android/open-app-settings.md) · [🇫🇷 Français](../../fr/android/open-app-settings.md) · **🇪🇸 Español** · [🇨🇳 中文](../../zh/android/open-app-settings.md)

> [!TIP]
> **¿Sin tiempo? Configuramos su app por usted.** Nuestro equipo configura, compila & publica su app WebViewGold: llave en mano, entrega rápida, Made in Germany. [Configurar mi app →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_android_doc_online)
>
> **Compile en su navegador:** Sin Mac ni IDE: el **WebViewGold Cloud Builder** configura, compila & sube su app en línea. [Descubra Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=android_docs)
