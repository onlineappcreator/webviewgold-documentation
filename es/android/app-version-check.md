---
title: "API de comprobación de versión de la app – Documentación de WebViewGold para Android"
description: "Detecte la versión instalada de la aplicación desde su aplicación web y solicite a los usuarios que la actualicen cuando sea necesario."
lang: "es"
product: "WebViewGold para Android"
platform: "Android"
category: "API y funciones"
slug: "app-version-check"
canonical_url: "https://www.webviewgold.com/es/docs/android/app-version-check/"
keywords:
  - "API de comprobación de versión"
  - "WebViewGold para Android"
  - "convertir sitio web en app"
  - "documentación de app WebView"
  - "SDK WebView de Android"
  - "PWA a app"
  - "HTML a app"
  - "puente de JavaScript"
last_updated: "2026-10-09"
---

# API de comprobación de versión de la app – WebViewGold para Android

> **Resumen:** Detecte la versión instalada de la aplicación desde su aplicación web y solicite a los usuarios que la actualicen cuando sea necesario.

[Documentación](../README.md) › [WebViewGold para Android](README.md) › API de comprobación de versión

**Plataforma:** Android · **Categoría:** API y funciones · **Versión en línea:** [www.webviewgold.com/es/docs/android/app-version-check/](https://www.webviewgold.com/es/docs/android/app-version-check/)

---

Con esta API de comprobación de versión de la app de WebViewGold, su sitio web o app web puede **obtener la versión de la app de Android** que utiliza el usuario de su app de Android. Esta API resulta especialmente útil si desea avisar a los usuarios de una versión anterior para que actualicen su app. Además, puede ocultar secciones de la app web que requieren funciones compatibles solo con una versión específica de la app.\
Utilice JavaScript con este tipo de URL para leer y mostrar la versión de la app y su número de compilación (bundle):

```html
<script>
window.location.href = "getappversion://";
alert(versionNumber);
alert(bundleNumber);
</script>
```

**Como alternativa, considere establecer  `AUTO_INJECT_VARIABLES`  en `true` en Config.java para inyectar automáticamente este valor (y otros) en JavaScript sin necesidad de llamar antes a una URL.**

---

## Seguir leyendo

- ← Anterior: [API de captura de pantalla](take-screenshot.md)
- Siguiente →: [API de contactos](contacts.md)
- La misma función en otras plataformas: [iOS – API de comprobación de versión](../ios/app-version-check.md)
- Idiomas: [🇺🇸 English](../../android/app-version-check.md) · [🇩🇪 Deutsch](../../de/android/app-version-check.md) · [🇫🇷 Français](../../fr/android/app-version-check.md) · **🇪🇸 Español** · [🇨🇳 中文](../../zh/android/app-version-check.md)

> [!TIP]
> **¿Sin tiempo? Configuramos su app por usted.** Nuestro equipo configura, compila & publica su app WebViewGold: llave en mano, entrega rápida, Made in Germany. [Configurar mi app →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_android_doc_online)
>
> **Compile en su navegador:** Sin Mac ni IDE: el **WebViewGold Cloud Builder** configura, compila & sube su app en línea. [Descubra Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=android_docs)
