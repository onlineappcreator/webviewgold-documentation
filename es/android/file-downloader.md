---
title: "API de descarga de archivos – Documentación de WebViewGold para Android"
description: "Permita que los usuarios descarguen imágenes, PDF y otros archivos desde su aplicación web a su dispositivo Android."
lang: "es"
product: "WebViewGold para Android"
platform: "Android"
category: "API y funciones"
slug: "file-downloader"
canonical_url: "https://www.webviewgold.com/es/docs/android/file-downloader/"
keywords:
  - "API de descarga de archivos"
  - "WebViewGold para Android"
  - "convertir sitio web en app"
  - "documentación de app WebView"
  - "SDK WebView de Android"
  - "PWA a app"
  - "HTML a app"
  - "puente de JavaScript"
last_updated: "2026-10-09"
---

# API de descarga de archivos – WebViewGold para Android

> **Resumen:** Permita que los usuarios descarguen imágenes, PDF y otros archivos desde su aplicación web a su dispositivo Android.

[Documentación](../README.md) › [WebViewGold para Android](README.md) › API de descarga de archivos

**Plataforma:** Android · **Categoría:** API y funciones · **Versión en línea:** [www.webviewgold.com/es/docs/android/file-downloader/](https://www.webviewgold.com/es/docs/android/file-downloader/)

---

La API de descargas de WebViewGold le permite ofrecer descargas de archivos de documentos, imágenes y audio dentro de su app WebView. Los siguientes pasos describen cómo activar y personalizar la funcionalidad de descarga:

## 1. Descargar imágenes

Guarde imágenes en el carrete del usuario llamando a enlaces con el prefijo savethisimage://?url=:

```html
<a href="savethisimage://?url=IMAGE URL HERE">Download Image</a>
```

## 2. Descargar archivos PDF

Guarde archivos PDF llamando a enlaces con el sufijo .pdf:

```html
<a href="https://www.example.org/file.pdf">Download PDF</a>
```

## 3. Descargar archivos de música

Guarde archivos de música simplemente llamando a enlaces con el sufijo .mp3, .mp4 o .wav:

```html
<a href="https://www.example.org/file.mp3">Download MP3</a>
<a href="https://www.example.org/file.mp4">Download MP4</a>
<a href="https://www.example.org/file.wav">Download WAV</a>
```

## 4. Personalizar los tipos de archivo admitidos

Para añadir formatos de archivo adicionales al gestor de descargas, insértelos en la lista `downloadableExtension` de **Config.java**.

## 5. Activar las descargas automáticas de archivos

Considere establecer la opción `AUTO_DOWNLOAD_FILES` en **Config.java** para activar las descargas automáticas de archivos marcados con cabeceras HTTP Content-Disposition, independientemente de la lista `downloadableExtension`. Esto garantiza que los archivos se descarguen automáticamente según la configuración del servidor.

---

## Seguir leyendo

- ← Anterior: [API de anuncios de Facebook](facebook-ads.md)
- Siguiente →: [API de vídeo nativo (PiP)](native-video.md)
- La misma función en otras plataformas: [iOS – API de descarga de archivos](../ios/file-downloader.md)
- Idiomas: [🇺🇸 English](../../android/file-downloader.md) · [🇩🇪 Deutsch](../../de/android/file-downloader.md) · [🇫🇷 Français](../../fr/android/file-downloader.md) · **🇪🇸 Español** · [🇨🇳 中文](../../zh/android/file-downloader.md)

> [!TIP]
> **¿Sin tiempo? Configuramos su app por usted.** Nuestro equipo configura, compila & publica su app WebViewGold: llave en mano, entrega rápida, Made in Germany. [Configurar mi app →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_android_doc_online)
>
> **Compile en su navegador:** Sin Mac ni IDE: el **WebViewGold Cloud Builder** configura, compila & sube su app en línea. [Descubra Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=android_docs)
