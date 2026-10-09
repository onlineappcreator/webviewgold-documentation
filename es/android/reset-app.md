---
title: "API de restablecimiento de la app – Documentación de WebViewGold para Android"
description: "Restablezca la caché, las cookies y el almacenamiento local de su aplicación Android WebView con un solo enlace o llamada de JavaScript."
lang: "es"
product: "WebViewGold para Android"
platform: "Android"
category: "API y funciones"
slug: "reset-app"
canonical_url: "https://www.webviewgold.com/es/docs/android/reset-app/"
keywords:
  - "API de restablecimiento"
  - "WebViewGold para Android"
  - "convertir sitio web en app"
  - "documentación de app WebView"
  - "SDK WebView de Android"
  - "PWA a app"
  - "HTML a app"
  - "puente de JavaScript"
last_updated: "2026-10-09"
---

# API de restablecimiento de la app – WebViewGold para Android

> **Resumen:** Restablezca la caché, las cookies y el almacenamiento local de su aplicación Android WebView con un solo enlace o llamada de JavaScript.

[Documentación](../README.md) › [WebViewGold para Android](README.md) › API de restablecimiento

**Plataforma:** Android · **Categoría:** API y funciones · **Versión en línea:** [www.webviewgold.com/es/docs/android/reset-app/](https://www.webviewgold.com/es/docs/android/reset-app/)

---

En ciertos casos, puede ser necesario restablecer la aplicación a su configuración inicial (borrando las cookies y el caché) para restaurar el rendimiento óptimo. La **API de restablecimiento de la app** proporciona una forma sencilla de iniciar este reinicio.

## Uso

Para restablecer los datos de la aplicación, simplemente use el siguiente enlace dentro de su aplicación:

```html
<a href="reset://">Reset App Link</a>
```

Este enlace:

- Borrar todas las cookies
- Borrar datos en caché

## Prueba de la funcionalidad de reinicio

Para probar esta función, agregue la siguiente URL de demostración a su aplicación WebViewGold:<https://www.onlineappcreator.com/reset_test.html>

**Nota:**Utilice la función de reinicio con sensatez, ya que borrará los datos del usuario relacionados con las cookies y el caché, lo que podría afectar la configuración guardada o los datos de la sesión, incluido el cierre de sesión de los usuarios en las sesiones activas.

---

## Seguir leyendo

- ← Anterior: [API de vídeo nativo (PiP)](native-video.md)
- Siguiente →: [API de indicador de carga](loading-sign.md)
- La misma función en otras plataformas: [iOS – API de restablecer app](../ios/reset-app.md)
- Idiomas: [🇺🇸 English](../../android/reset-app.md) · [🇩🇪 Deutsch](../../de/android/reset-app.md) · [🇫🇷 Français](../../fr/android/reset-app.md) · **🇪🇸 Español** · [🇨🇳 中文](../../zh/android/reset-app.md)

> [!TIP]
> **¿Sin tiempo? Configuramos su app por usted.** Nuestro equipo configura, compila & publica su app WebViewGold: llave en mano, entrega rápida, Made in Germany. [Configurar mi app →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_android_doc_online)
>
> **Compile en su navegador:** Sin Mac ni IDE: el **WebViewGold Cloud Builder** configura, compila & sube su app en línea. [Descubra Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=android_docs)
