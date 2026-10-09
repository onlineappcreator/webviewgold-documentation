---
title: "API de modo de escaneo – Documentación de WebViewGold para iOS"
description: "Ajuste con precisión el comportamiento de escaneo de la cámara del escáner de QR y de códigos de barras en WebViewGold para iOS."
lang: "es"
product: "WebViewGold para iOS"
platform: "iOS"
category: "API y funciones"
slug: "scanning-mode"
canonical_url: "https://www.webviewgold.com/es/docs/iOS/scanning-mode/"
keywords:
  - "API de modo de escaneo"
  - "WebViewGold para iOS"
  - "convertir sitio web en app"
  - "documentación de app WebView"
  - "SDK WebView de iOS"
  - "PWA a app"
  - "HTML a app"
  - "puente de JavaScript"
last_updated: "2026-10-09"
---

# API de modo de escaneo – WebViewGold para iOS

> **Resumen:** Ajuste con precisión el comportamiento de escaneo de la cámara del escáner de QR y de códigos de barras en WebViewGold para iOS.

[Documentación](../README.md) › [WebViewGold para iOS](README.md) › API de modo de escaneo

**Plataforma:** iOS · **Categoría:** API y funciones · **Versión en línea:** [www.webviewgold.com/es/docs/iOS/scanning-mode/](https://www.webviewgold.com/es/docs/iOS/scanning-mode/)

---

Si su aplicación web muestra información en la pantalla para ser escaneada (por ejemplo, un código QR), puede resultar útil aumentar el brillo de la pantalla al 100 % y evitar que la pantalla se apague. WebViewGold proporciona la API de modo escaneo (Scanning Mode) para habilitar dinámicamente estas condiciones óptimas de escaneo.\
Esta API incluye 3 comandos:

- "auto" = activa el modo escaneo y lo desactiva automáticamente al redirigir a otra página.
- "on" = activa el modo escaneo y permanece activo tras las redirecciones de página.
- "off" = desactiva el modo escaneo.

Enlace a este tipo de URL para usar la API de modo escaneo:

```html
<a href="scanningmode://auto">Enable Scanning Mode; will automatically disable on page redirect</a>
<a href="scanningmode://on">Enable Scanning Mode; will persist until manually disabled</a>
<a href="scanningmode://off">Disable Scanning Mode</a>
```

---

## Seguir leyendo

- ← Anterior: [API de escáner de códigos de barras](barcode-scanner.md)
- Siguiente →: [Escáner de documentos](document-scanner.md)
- La misma función en otras plataformas: [Android – API de modo de escaneo](../android/scanning-mode.md)
- Idiomas: [🇺🇸 English](../../ios/scanning-mode.md) · [🇩🇪 Deutsch](../../de/ios/scanning-mode.md) · [🇫🇷 Français](../../fr/ios/scanning-mode.md) · **🇪🇸 Español** · [🇨🇳 中文](../../zh/ios/scanning-mode.md)

> [!TIP]
> **¿Sin tiempo? Configuramos su app por usted.** Nuestro equipo configura, compila & publica su app WebViewGold: llave en mano, entrega rápida, Made in Germany. [Configurar mi app →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **Compile en su navegador:** Sin Mac ni IDE: el **WebViewGold Cloud Builder** configura, compila & sube su app en línea. [Descubra Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
