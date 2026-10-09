---
title: "API de linterna – Documentación de WebViewGold para Android"
description: "Controle la linterna del dispositivo desde su aplicación web con sencillos enlaces de JavaScript en WebViewGold para Android."
lang: "es"
product: "WebViewGold para Android"
platform: "Android"
category: "API y funciones"
slug: "flashlight"
canonical_url: "https://www.webviewgold.com/es/docs/android/flashlight/"
keywords:
  - "API de linterna"
  - "WebViewGold para Android"
  - "convertir sitio web en app"
  - "documentación de app WebView"
  - "SDK WebView de Android"
  - "PWA a app"
  - "HTML a app"
  - "puente de JavaScript"
last_updated: "2026-10-09"
---

# API de linterna – WebViewGold para Android

> **Resumen:** Controle la linterna del dispositivo desde su aplicación web con sencillos enlaces de JavaScript en WebViewGold para Android.

[Documentación](../README.md) › [WebViewGold para Android](README.md) › API de linterna

**Plataforma:** Android · **Categoría:** API y funciones · **Versión en línea:** [www.webviewgold.com/es/docs/android/flashlight/](https://www.webviewgold.com/es/docs/android/flashlight/)

---

La API de linterna de WebViewGold permite que su sitio web controle la linterna (flash) del dispositivo. Esta función puede resultar útil para:

- Crear apps de utilidades que requieran activar y desactivar la linterna
- Mejorar la experiencia de usuario durante el uso de la app con gamificación
- Ofrecer funciones de accesibilidad adicionales

## Cómo usarlo

Puede encender o apagar la linterna directamente desde su contenido HTML utilizando los siguientes enlaces:

```html
<a href="enableflashlight://">Turn On Flashlight</a>
<a href="disableflashlight://">Turn Off Flashlight</a>
```

**Nota:** asegúrese de que su app tenga los permisos de cámara necesarios en AndroidManifest.xml, ya que la funcionalidad de linterna está vinculada al hardware de la cámara del dispositivo.

---

## Seguir leyendo

- ← Anterior: [API de UUID](uuid.md)
- Siguiente →: [App Links / Deep Linking](app-links.md)
- La misma función en otras plataformas: [iOS – API de linterna](../ios/flashlight.md)
- Idiomas: [🇺🇸 English](../../android/flashlight.md) · [🇩🇪 Deutsch](../../de/android/flashlight.md) · [🇫🇷 Français](../../fr/android/flashlight.md) · **🇪🇸 Español** · [🇨🇳 中文](../../zh/android/flashlight.md)

> [!TIP]
> **¿Sin tiempo? Configuramos su app por usted.** Nuestro equipo configura, compila & publica su app WebViewGold: llave en mano, entrega rápida, Made in Germany. [Configurar mi app →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_android_doc_online)
>
> **Compile en su navegador:** Sin Mac ni IDE: el **WebViewGold Cloud Builder** configura, compila & sube su app en línea. [Descubra Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=android_docs)
