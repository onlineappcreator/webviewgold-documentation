---
title: "API de modo de escaneo – Documentación de WebViewGold para Android"
description: "Ajuste con precisión el comportamiento de escaneo de la cámara del escáner de códigos QR y de barras en WebViewGold para Android."
lang: "es"
product: "WebViewGold para Android"
platform: "Android"
category: "API y funciones"
slug: "scanning-mode"
canonical_url: "https://www.webviewgold.com/es/docs/android/scanning-mode/"
keywords:
  - "API de modo de escaneo"
  - "WebViewGold para Android"
  - "convertir sitio web en app"
  - "documentación de app WebView"
  - "SDK WebView de Android"
  - "PWA a app"
  - "HTML a app"
  - "puente de JavaScript"
last_updated: "2026-10-09"
---

# API de modo de escaneo – WebViewGold para Android

> **Resumen:** Ajuste con precisión el comportamiento de escaneo de la cámara del escáner de códigos QR y de barras en WebViewGold para Android.

[Documentación](../README.md) › [WebViewGold para Android](README.md) › API de modo de escaneo

**Plataforma:** Android · **Categoría:** API y funciones · **Versión en línea:** [www.webviewgold.com/es/docs/android/scanning-mode/](https://www.webviewgold.com/es/docs/android/scanning-mode/)

---

Si su aplicación web presenta información en la pantalla que se va a escanear (por ejemplo, un código QR), puede resultar útil aumentar el brillo de la pantalla al 100 % y evitar que la pantalla entre en suspensión. WebViewGold proporciona la API del modo de escaneo para habilitar dinámicamente estas condiciones óptimas de escaneo.\
Esta API incluye 3 comandos:

- "auto" = activa el modo de escaneo y lo desactiva automáticamente al redirigir la página.
- "on" = activa el modo de escaneo, permanece encendido después de que la página se redirecciona.
- "off" = desactiva el modo de escaneo.

Enlace a este tipo de URL para utilizar la API del modo de escaneo:

```html
<a href="scanningmode://auto">Enable Scanning Mode; will automatically disable on page redirect.</a>
<a href="scanningmode://on">Enable Scanning Mode; will persist until manually disabled.</a>
<a href="scanningmode://off">Disable Scanning Mode.</a>
```

---

## Seguir leyendo

- ← Anterior: [API de escáner de QR](qr-code-scanner.md)
- Siguiente →: [API de escáner de códigos de barras](barcode-scanner.md)
- La misma función en otras plataformas: [iOS – API de modo de escaneo](../ios/scanning-mode.md)
- Idiomas: [🇺🇸 English](../../android/scanning-mode.md) · [🇩🇪 Deutsch](../../de/android/scanning-mode.md) · [🇫🇷 Français](../../fr/android/scanning-mode.md) · **🇪🇸 Español** · [🇨🇳 中文](../../zh/android/scanning-mode.md)

> [!TIP]
> **¿Sin tiempo? Configuramos su app por usted.** Nuestro equipo configura, compila & publica su app WebViewGold: llave en mano, entrega rápida, Made in Germany. [Configurar mi app →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_android_doc_online)
>
> **Compile en su navegador:** Sin Mac ni IDE: el **WebViewGold Cloud Builder** configura, compila & sube su app en línea. [Descubra Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=android_docs)
