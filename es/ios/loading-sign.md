---
title: "API de indicador de carga – Documentación de WebViewGold para iOS"
description: "Muestre u oculte el indicador de carga nativo cuando lo necesite y personalice la experiencia de carga de su app iOS."
lang: "es"
product: "WebViewGold para iOS"
platform: "iOS"
category: "API y funciones"
slug: "loading-sign"
canonical_url: "https://www.webviewgold.com/es/docs/iOS/loading-sign/"
keywords:
  - "API de indicador de carga"
  - "WebViewGold para iOS"
  - "convertir sitio web en app"
  - "documentación de app WebView"
  - "SDK WebView de iOS"
  - "PWA a app"
  - "HTML a app"
  - "puente de JavaScript"
last_updated: "2026-10-09"
---

# API de indicador de carga – WebViewGold para iOS

> **Resumen:** Muestre u oculte el indicador de carga nativo cuando lo necesite y personalice la experiencia de carga de su app iOS.

[Documentación](../README.md) › [WebViewGold para iOS](README.md) › API de indicador de carga

**Plataforma:** iOS · **Categoría:** API y funciones · **Versión en línea:** [www.webviewgold.com/es/docs/iOS/loading-sign/](https://www.webviewgold.com/es/docs/iOS/loading-sign/)

---

El indicador de carga nativo de iOS de WebViewGold **aparece automáticamente** cuando las páginas empiezan o terminan de cargarse. Sin embargo, también puede controlar manualmente el indicador de carga en situaciones que queden fuera de los eventos de carga estándar de una página. Esto resulta particularmente útil para procesos en los que es necesario que el usuario sea consciente de la carga, como:

- La espera en una cola de chat en vivo
- La ejecución de un proceso en segundo plano en un servidor en la nube
- La visualización de cualquier otro proceso prolongado para informar al usuario

## Uso

Para controlar manualmente el indicador de carga en su aplicación WebView, utilice los siguientes enlaces:

```html
<a href="spinneron://">Show the loading spinner</a>
<a href="spinneroff://">Hide the loading spinner</a>
```

---

## Seguir leyendo

- ← Anterior: [API de decisión de seguimiento](user-tracking.md)
- Siguiente →: [API Pull-to-Refresh](pull-to-refresh.md)
- La misma función en otras plataformas: [Android – API de indicador de carga](../android/loading-sign.md)
- Idiomas: [🇺🇸 English](../../ios/loading-sign.md) · [🇩🇪 Deutsch](../../de/ios/loading-sign.md) · [🇫🇷 Français](../../fr/ios/loading-sign.md) · **🇪🇸 Español** · [🇨🇳 中文](../../zh/ios/loading-sign.md)

> [!TIP]
> **¿Sin tiempo? Configuramos su app por usted.** Nuestro equipo configura, compila & publica su app WebViewGold: llave en mano, entrega rápida, Made in Germany. [Configurar mi app →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **Compile en su navegador:** Sin Mac ni IDE: el **WebViewGold Cloud Builder** configura, compila & sube su app en línea. [Descubra Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
