---
title: "Escáner de documentos VisionKit – Documentación de WebViewGold para iOS"
description: "Permita que los usuarios escaneen documentos en papel con la cámara y los suban mediante la carga de archivos de su aplicación web, con la tecnología de Apple VisionKit."
lang: "es"
product: "WebViewGold para iOS"
platform: "iOS"
category: "API y funciones"
slug: "document-scanner"
canonical_url: "https://www.webviewgold.com/es/docs/iOS/document-scanner/"
keywords:
  - "Escáner de documentos"
  - "WebViewGold para iOS"
  - "convertir sitio web en app"
  - "documentación de app WebView"
  - "SDK WebView de iOS"
  - "PWA a app"
  - "HTML a app"
  - "puente de JavaScript"
last_updated: "2026-10-09"
---

# Escáner de documentos VisionKit – WebViewGold para iOS

> **Resumen:** Permita que los usuarios escaneen documentos en papel con la cámara y los suban mediante la carga de archivos de su aplicación web, con la tecnología de Apple VisionKit.

[Documentación](../README.md) › [WebViewGold para iOS](README.md) › Escáner de documentos

**Plataforma:** iOS · **Categoría:** API y funciones · **Versión en línea:** [www.webviewgold.com/es/docs/iOS/document-scanner/](https://www.webviewgold.com/es/docs/iOS/document-scanner/)

---

La función de **escáner de documentos** añade la opción **Escanear documento** al selector estándar de subida de archivos de su aplicación. El usuario puede escanear una o varias páginas con la cámara; la aplicación genera un escaneo del documento y lo sube mediante el flujo estándar de `<input type="file">` que utiliza su aplicación web. Está impulsada por el framework **VisionKit** de Apple (`VNDocumentCameraViewController`), con detección automática de bordes, recorte y mejora de imagen.

## Cómo activarla

Active la función en **Config.swift**:

```swift
var kVisionKitEnable = true
```

Establézcala en `false` para ocultar la entrada **Escanear documento**.

## Experiencia del usuario

1. En su página web, el usuario toca un `<input type="file">`.
2. La aplicación muestra un diálogo de subida con entradas como *Escanear documento*, *Cámara* y *Fototeca*.
3. Al tocar **Escanear documento**, se inicia el escáner de VisionKit: detecta los bordes, recorta y mejora cada página, y permite añadir más páginas.
4. El escaneo resultante se devuelve al `<input type="file">`: su aplicación web lo recibe exactamente igual que cualquier otro archivo subido.

**Notas:** Requiere iOS 18.4 o superior y un dispositivo compatible con la cámara de documentos de VisionKit. En los dispositivos no compatibles, la entrada **Escanear documento** se oculta automáticamente.

---

## Seguir leyendo

- ← Anterior: [API de modo de escaneo](scanning-mode.md)
- Siguiente →: [API de captura de pantalla](take-screenshot.md)
- La misma función en otras plataformas: [Android – Document Scanner](../android/document-scanner.md)
- Idiomas: [🇺🇸 English](../../ios/document-scanner.md) · [🇩🇪 Deutsch](../../de/ios/document-scanner.md) · [🇫🇷 Français](../../fr/ios/document-scanner.md) · **🇪🇸 Español** · [🇨🇳 中文](../../zh/ios/document-scanner.md)

> [!TIP]
> **¿Sin tiempo? Configuramos su app por usted.** Nuestro equipo configura, compila & publica su app WebViewGold: llave en mano, entrega rápida, Made in Germany. [Configurar mi app →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **Compile en su navegador:** Sin Mac ni IDE: el **WebViewGold Cloud Builder** configura, compila & sube su app en línea. [Descubra Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
