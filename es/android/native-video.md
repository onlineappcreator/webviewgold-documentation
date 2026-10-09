---
title: "API de vídeo nativo con Picture-in-Picture – Documentación de WebViewGold para Android"
description: "Reproduzca vídeos de forma nativa con soporte de Picture-in-Picture en su aplicación Android WebView."
lang: "es"
product: "WebViewGold para Android"
platform: "Android"
category: "API y funciones"
slug: "native-video"
canonical_url: "https://www.webviewgold.com/es/docs/android/native-video/"
keywords:
  - "API de vídeo nativo (PiP)"
  - "WebViewGold para Android"
  - "convertir sitio web en app"
  - "documentación de app WebView"
  - "SDK WebView de Android"
  - "PWA a app"
  - "HTML a app"
  - "puente de JavaScript"
last_updated: "2026-10-09"
---

# API de vídeo nativo con Picture-in-Picture – WebViewGold para Android

> **Resumen:** Reproduzca vídeos de forma nativa con soporte de Picture-in-Picture en su aplicación Android WebView.

[Documentación](../README.md) › [WebViewGold para Android](README.md) › API de vídeo nativo (PiP)

**Plataforma:** Android · **Categoría:** API y funciones · **Versión en línea:** [www.webviewgold.com/es/docs/android/native-video/](https://www.webviewgold.com/es/docs/android/native-video/)

---

La API de video nativo permite que su sitio web inicie una transmisión de video en el reproductor nativo del dispositivo con soporte Picture-in-Picture. Active la reproducción nativa abriendo un enlace con el`startnativevideo://videostreamurl=`prefijo:

```html
<a href="startnativevideo://videostreamurl=YOUR_VIDEO_STREAM_URL">Play Video in System Video Player with PiP Support</a>
```

El usuario puede continuar viendo el video en una ventana flotante mientras navega por su aplicación u otras aplicaciones.

---

## Seguir leyendo

- ← Anterior: [API de descarga de archivos](file-downloader.md)
- Siguiente →: [API de restablecimiento](reset-app.md)
- La misma función en otras plataformas: [iOS – API de vídeo nativo](../ios/native-video.md)
- Idiomas: [🇺🇸 English](../../android/native-video.md) · [🇩🇪 Deutsch](../../de/android/native-video.md) · [🇫🇷 Français](../../fr/android/native-video.md) · **🇪🇸 Español** · [🇨🇳 中文](../../zh/android/native-video.md)

> [!TIP]
> **¿Sin tiempo? Configuramos su app por usted.** Nuestro equipo configura, compila & publica su app WebViewGold: llave en mano, entrega rápida, Made in Germany. [Configurar mi app →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_android_doc_online)
>
> **Compile en su navegador:** Sin Mac ni IDE: el **WebViewGold Cloud Builder** configura, compila & sube su app en línea. [Descubra Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=android_docs)
