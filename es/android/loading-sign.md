---
title: "API de indicador de carga – Documentación de WebViewGold para Android"
description: "Muestre u oculte el indicador de carga nativo cuando lo desee y personalice la experiencia de carga de su aplicación de Android."
lang: "es"
product: "WebViewGold para Android"
platform: "Android"
category: "API y funciones"
slug: "loading-sign"
canonical_url: "https://www.webviewgold.com/es/docs/android/loading-sign/"
keywords:
  - "API de indicador de carga"
  - "WebViewGold para Android"
  - "convertir sitio web en app"
  - "documentación de app WebView"
  - "SDK WebView de Android"
  - "PWA a app"
  - "HTML a app"
  - "puente de JavaScript"
last_updated: "2026-10-09"
---

# API de indicador de carga – WebViewGold para Android

> **Resumen:** Muestre u oculte el indicador de carga nativo cuando lo desee y personalice la experiencia de carga de su aplicación de Android.

[Documentación](../README.md) › [WebViewGold para Android](README.md) › API de indicador de carga

**Plataforma:** Android · **Categoría:** API y funciones · **Versión en línea:** [www.webviewgold.com/es/docs/android/loading-sign/](https://www.webviewgold.com/es/docs/android/loading-sign/)

---

El indicador de carga nativo de Android de WebViewGold aparece automáticamente cuando las páginas empiezan o terminan de cargarse. Sin embargo, también puede controlar manualmente el indicador de carga para situaciones ajenas a los eventos estándar de carga de páginas. Esto resulta especialmente útil en procesos en los que es necesario que el usuario sea consciente de la carga, como:

- Esperar en una cola de chat en vivo
- Ejecutar un proceso en segundo plano en un servidor en la nube
- Visualizar cualquier otro proceso prolongado para que el usuario sea consciente de él

## Uso

Para controlar manualmente el indicador de carga de su app WebView, utilice los siguientes enlaces:

```html
<a href="spinneron://">Show the loading spinner</a>
<a href="spinneroff://">Hide the loading spinner</a>
```

---

## Seguir leyendo

- ← Anterior: [API de restablecimiento](reset-app.md)
- Siguiente →: [API de portapapeles](clipboard.md)
- La misma función en otras plataformas: [iOS – API de indicador de carga](../ios/loading-sign.md)
- Idiomas: [🇺🇸 English](../../android/loading-sign.md) · [🇩🇪 Deutsch](../../de/android/loading-sign.md) · [🇫🇷 Français](../../fr/android/loading-sign.md) · **🇪🇸 Español** · [🇨🇳 中文](../../zh/android/loading-sign.md)

> [!TIP]
> **¿Sin tiempo? Configuramos su app por usted.** Nuestro equipo configura, compila & publica su app WebViewGold: llave en mano, entrega rápida, Made in Germany. [Configurar mi app →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_android_doc_online)
>
> **Compile en su navegador:** Sin Mac ni IDE: el **WebViewGold Cloud Builder** configura, compila & sube su app en línea. [Descubra Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=android_docs)
