---
title: "API de descarga de archivos – Documentación de WebViewGold para iOS"
description: "Permita que los usuarios descarguen imágenes, PDF y otros archivos desde su aplicación web directamente a su iPhone o iPad."
lang: "es"
product: "WebViewGold para iOS"
platform: "iOS"
category: "API y funciones"
slug: "file-downloader"
canonical_url: "https://www.webviewgold.com/es/docs/iOS/file-downloader/"
keywords:
  - "API de descarga de archivos"
  - "WebViewGold para iOS"
  - "convertir sitio web en app"
  - "documentación de app WebView"
  - "SDK WebView de iOS"
  - "PWA a app"
  - "HTML a app"
  - "puente de JavaScript"
last_updated: "2026-10-09"
---

# API de descarga de archivos – WebViewGold para iOS

> **Resumen:** Permita que los usuarios descarguen imágenes, PDF y otros archivos desde su aplicación web directamente a su iPhone o iPad.

[Documentación](../README.md) › [WebViewGold para iOS](README.md) › API de descarga de archivos

**Plataforma:** iOS · **Categoría:** API y funciones · **Versión en línea:** [www.webviewgold.com/es/docs/iOS/file-downloader/](https://www.webviewgold.com/es/docs/iOS/file-downloader/)

---

La API de descargas de WebViewGold le permite ofrecer descargas de documentos, imágenes y archivos de audio dentro de su aplicación WebView. Los siguientes pasos describen cómo habilitar y personalizar la funcionalidad del descargador:

## 1. Descargar imágenes

Guarde imágenes en el carrete del usuario invocando enlaces con el prefijo savethisimage://?url=:

```html
<a href="savethisimage://?url=IMAGE URL HERE">Download Image</a>
```

## 2. Descargar archivos

Guarde archivos invocando enlaces con el sufijo correspondiente (por ejemplo, .mp3):

```html
<a href="https://www.example.org/file.pdf">Link PDF</a>
<a href="https://www.example.org/file.mp3">Link mp3 Music</a>
<a href="https://www.example.org/file.mp4">Link mp4 Music</a>
<a href="https://www.example.org/file.wav">Link wav Music</a>
<a href="https://www.example.org/file.epub">Link epub eBook</a>
<a href="https://www.example.org/file.pkpass">Link Passbook / Apple Wallet</a>
<a href="https://www.example.org/file.docx">Link Word</a>
<a href="https://www.example.org/file.pptx">Link PowerPoint</a>
<a href="https://www.example.org/file.xlsx">Link Excel</a>
```

## 3. Personalizar los tipos de archivo admitidos

Puede añadir más tipos de archivo que deben activar la funcionalidad del descargador (por ejemplo, .epub, .zip, ...). Esto se hace mediante la variable de lista `extentionARY` que se encuentra en el archivo **Config.swift**.

## 4. Habilitar descargas automáticas de archivos

Considere establecer la opción `autodownloader` en **Config.swift** para habilitar descargas automáticas de archivos marcados con las cabeceras HTTP Content-Disposition, independientemente de la lista `extentionARY`. Esto garantiza que los archivos se descarguen automáticamente según las configuraciones del servidor.

[![Ver el vídeo: API de descarga de archivos](https://img.youtube.com/vi/V0LnwnzJx6I/hqdefault.jpg)](https://www.youtube.com/watch?v=V0LnwnzJx6I)

---

## Seguir leyendo

- ← Anterior: [API de vídeo nativo](native-video.md)
- Siguiente →: [API de impresora](printer.md)
- La misma función en otras plataformas: [Android – API de descarga de archivos](../android/file-downloader.md)
- Idiomas: [🇺🇸 English](../../ios/file-downloader.md) · [🇩🇪 Deutsch](../../de/ios/file-downloader.md) · [🇫🇷 Français](../../fr/ios/file-downloader.md) · **🇪🇸 Español** · [🇨🇳 中文](../../zh/ios/file-downloader.md)

> [!TIP]
> **¿Sin tiempo? Configuramos su app por usted.** Nuestro equipo configura, compila & publica su app WebViewGold: llave en mano, entrega rápida, Made in Germany. [Configurar mi app →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **Compile en su navegador:** Sin Mac ni IDE: el **WebViewGold Cloud Builder** configura, compila & sube su app en línea. [Descubra Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
