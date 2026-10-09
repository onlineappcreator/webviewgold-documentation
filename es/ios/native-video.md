---
title: "API de reproductor de vídeo nativo – Documentación de WebViewGold para iOS"
description: "Reproduzca transmisiones de vídeo en el reproductor nativo de iOS con soporte de imagen en imagen, activadas directamente desde su aplicación web."
lang: "es"
product: "WebViewGold para iOS"
platform: "iOS"
category: "API y funciones"
slug: "native-video"
canonical_url: "https://www.webviewgold.com/es/docs/iOS/native-video/"
keywords:
  - "API de vídeo nativo"
  - "WebViewGold para iOS"
  - "convertir sitio web en app"
  - "documentación de app WebView"
  - "SDK WebView de iOS"
  - "PWA a app"
  - "HTML a app"
  - "puente de JavaScript"
last_updated: "2026-10-09"
---

# API de reproductor de vídeo nativo – WebViewGold para iOS

> **Resumen:** Reproduzca transmisiones de vídeo en el reproductor nativo de iOS con soporte de imagen en imagen, activadas directamente desde su aplicación web.

[Documentación](../README.md) › [WebViewGold para iOS](README.md) › API de vídeo nativo

**Plataforma:** iOS · **Categoría:** API y funciones · **Versión en línea:** [www.webviewgold.com/es/docs/iOS/native-video/](https://www.webviewgold.com/es/docs/iOS/native-video/)

---

La **API de reproductor de vídeo nativo** permite que su sitio web inicie una transmisión de vídeo en el reproductor nativo de iOS con soporte de **imagen en imagen** (Picture-in-Picture). Active la reproducción nativa abriendo un enlace con el prefijo `startnativevideo://videostreamurl=`:

```html
<a href="startnativevideo://videostreamurl=YOUR_VIDEO_STREAM_URL">Reproducir vídeo en el reproductor del sistema con soporte PiP</a>
```

El usuario puede seguir viendo el vídeo en una ventana flotante de imagen en imagen mientras navega por su aplicación web o incluso por otras aplicaciones.

## Casos de uso típicos

- Transmisiones en directo que deben seguir reproduciéndose mientras el usuario navega por su aplicación web.
- Cursos en vídeo o tutoriales con los controles de reproducción del sistema.
- Cualquier vídeo que se beneficie de AirPlay, pantalla completa y de la función imagen en imagen del reproductor nativo.

**Nota:** Utilice una URL directa de la transmisión de vídeo (p. ej., un archivo .mp4 o una transmisión HLS .m3u8), no la URL de una página HTML que incruste el vídeo.

---

## Seguir leyendo

- ← Anterior: [API de audio HTML](html-audio.md)
- Siguiente →: [API de descarga de archivos](file-downloader.md)
- La misma función en otras plataformas: [Android – API de vídeo nativo (PiP)](../android/native-video.md)
- Idiomas: [🇺🇸 English](../../ios/native-video.md) · [🇩🇪 Deutsch](../../de/ios/native-video.md) · [🇫🇷 Français](../../fr/ios/native-video.md) · **🇪🇸 Español** · [🇨🇳 中文](../../zh/ios/native-video.md)

> [!TIP]
> **¿Sin tiempo? Configuramos su app por usted.** Nuestro equipo configura, compila & publica su app WebViewGold: llave en mano, entrega rápida, Made in Germany. [Configurar mi app →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **Compile en su navegador:** Sin Mac ni IDE: el **WebViewGold Cloud Builder** configura, compila & sube su app en línea. [Descubra Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
