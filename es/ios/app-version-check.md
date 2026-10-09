---
title: "API de comprobación de versión de la app – Documentación de WebViewGold para iOS"
description: "Detecte la versión instalada de la app desde su aplicación web e invite a los usuarios a actualizarla cuando sea necesario."
lang: "es"
product: "WebViewGold para iOS"
platform: "iOS"
category: "API y funciones"
slug: "app-version-check"
canonical_url: "https://www.webviewgold.com/es/docs/iOS/app-version-check/"
keywords:
  - "API de comprobación de versión"
  - "WebViewGold para iOS"
  - "convertir sitio web en app"
  - "documentación de app WebView"
  - "SDK WebView de iOS"
  - "PWA a app"
  - "HTML a app"
  - "puente de JavaScript"
last_updated: "2026-10-09"
---

# API de comprobación de versión de la app – WebViewGold para iOS

> **Resumen:** Detecte la versión instalada de la app desde su aplicación web e invite a los usuarios a actualizarla cuando sea necesario.

[Documentación](../README.md) › [WebViewGold para iOS](README.md) › API de comprobación de versión

**Plataforma:** iOS · **Categoría:** API y funciones · **Versión en línea:** [www.webviewgold.com/es/docs/iOS/app-version-check/](https://www.webviewgold.com/es/docs/iOS/app-version-check/)

---

Utilizando este enfoque de la API de JavaScript de WebViewGold, su sitio web/aplicación web puede **obtener la versión de la aplicación iOS** que utiliza el usuario. Esto resulta especialmente útil si desea notificar a los usuarios con una versión antigua para que actualicen su aplicación. Además, permite ocultar secciones de la aplicación web que requieran funciones compatibles con una versión concreta.\
Use JavaScript con este tipo de URL para leer y mostrar la versión de la aplicación y el número de build:

```html
<script>
window.location.href = "getappversion://";
alert(versionNumber);
alert(bundleNumber);
</script>
```

**Alternativamente, considere establecer `autoInjectVariable` en `true` dentro de Config.swift para inyectar automáticamente este (y otros) valores en JavaScript, sin necesidad de invocar una URL previamente.**

---

## Seguir leyendo

- ← Anterior: [API de captura de pantalla](take-screenshot.md)
- Siguiente →: [API de UI dinámica](dynamic-ui.md)
- La misma función en otras plataformas: [Android – API de comprobación de versión](../android/app-version-check.md)
- Idiomas: [🇺🇸 English](../../ios/app-version-check.md) · [🇩🇪 Deutsch](../../de/ios/app-version-check.md) · [🇫🇷 Français](../../fr/ios/app-version-check.md) · **🇪🇸 Español** · [🇨🇳 中文](../../zh/ios/app-version-check.md)

> [!TIP]
> **¿Sin tiempo? Configuramos su app por usted.** Nuestro equipo configura, compila & publica su app WebViewGold: llave en mano, entrega rápida, Made in Germany. [Configurar mi app →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **Compile en su navegador:** Sin Mac ni IDE: el **WebViewGold Cloud Builder** configura, compila & sube su app en línea. [Descubra Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
