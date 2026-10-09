---
title: "API de linterna – Documentación de WebViewGold para iOS"
description: "Controle la linterna del dispositivo desde su aplicación web con sencillos enlaces de JavaScript en WebViewGold para iOS."
lang: "es"
product: "WebViewGold para iOS"
platform: "iOS"
category: "API y funciones"
slug: "flashlight"
canonical_url: "https://www.webviewgold.com/es/docs/iOS/flashlight/"
keywords:
  - "API de linterna"
  - "WebViewGold para iOS"
  - "convertir sitio web en app"
  - "documentación de app WebView"
  - "SDK WebView de iOS"
  - "PWA a app"
  - "HTML a app"
  - "puente de JavaScript"
last_updated: "2026-10-09"
---

# API de linterna – WebViewGold para iOS

> **Resumen:** Controle la linterna del dispositivo desde su aplicación web con sencillos enlaces de JavaScript en WebViewGold para iOS.

[Documentación](../README.md) › [WebViewGold para iOS](README.md) › API de linterna

**Plataforma:** iOS · **Categoría:** API y funciones · **Versión en línea:** [www.webviewgold.com/es/docs/iOS/flashlight/](https://www.webviewgold.com/es/docs/iOS/flashlight/)

---

La API de linterna (Flashlight) de WebViewGold permite que su sitio web controle la linterna del dispositivo. Esta función puede resultar útil para:

- Crear aplicaciones de utilidad que requieran alternar la linterna
- Mejorar la experiencia de usuario durante el uso de la aplicación mediante gamificación
- Ofrecer funciones adicionales de accesibilidad

## Cómo utilizarla

Puede activar o desactivar la linterna directamente desde su contenido HTML mediante los siguientes enlaces:

```html
<a href="enableflashlight://">Turn On Flashlight</a>
<a href="disableflashlight://">Turn Off Flashlight</a>
```

**Nota:** asegúrese de que su aplicación disponga de los permisos de cámara necesarios en Info.plist, ya que la funcionalidad de la linterna está vinculada al hardware de la cámara del dispositivo.

---

## Seguir leyendo

- ← Anterior: [API UUID](uuid.md)
- Siguiente →: [API de restablecer app](reset-app.md)
- La misma función en otras plataformas: [Android – API de linterna](../android/flashlight.md)
- Idiomas: [🇺🇸 English](../../ios/flashlight.md) · [🇩🇪 Deutsch](../../de/ios/flashlight.md) · [🇫🇷 Français](../../fr/ios/flashlight.md) · **🇪🇸 Español** · [🇨🇳 中文](../../zh/ios/flashlight.md)

> [!TIP]
> **¿Sin tiempo? Configuramos su app por usted.** Nuestro equipo configura, compila & publica su app WebViewGold: llave en mano, entrega rápida, Made in Germany. [Configurar mi app →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **Compile en su navegador:** Sin Mac ni IDE: el **WebViewGold Cloud Builder** configura, compila & sube su app en línea. [Descubra Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
