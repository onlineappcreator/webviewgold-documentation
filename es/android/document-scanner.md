---
title: "ML Kit Document Scanner (PDF) – Documentación de WebViewGold para Android"
description: "Add a Scan document option to the file upload dialog — the user scans up to 5 pages and your web app receives a PDF like any other upload."
lang: "es"
product: "WebViewGold para Android"
platform: "Android"
category: "API y funciones"
slug: "document-scanner"
canonical_url: "https://www.webviewgold.com/es/docs/android/document-scanner/"
keywords:
  - "Document Scanner"
  - "WebViewGold para Android"
  - "convertir sitio web en app"
  - "documentación de app WebView"
  - "SDK WebView de Android"
  - "PWA a app"
  - "HTML a app"
  - "puente de JavaScript"
last_updated: "2026-10-09"
---

# ML Kit Document Scanner (PDF) – WebViewGold para Android

> **Resumen:** Add a Scan document option to the file upload dialog — the user scans up to 5 pages and your web app receives a PDF like any other upload.

[Documentación](../README.md) › [WebViewGold para Android](README.md) › Document Scanner

**Plataforma:** Android · **Categoría:** API y funciones · **Versión en línea:** [www.webviewgold.com/es/docs/android/document-scanner/](https://www.webviewgold.com/es/docs/android/document-scanner/)

---

La función **Escáner de documentos** añade una opción **Escanear documento** al selector estándar de carga de archivos. El usuario puede escanear hasta 5 páginas con la cámara; la app genera un PDF y lo carga a través del flujo estándar de `<input type="file">` utilizado por su aplicación web. Está impulsado por el escáner de documentos de ML Kit de Google.

## Cómo activarlo

Active la función en **Config.java**:

```java
public static final boolean ENABLE_ML_KIT_DOCUMENT_SCANNER = true;
```

Establézcalo en `false` para ocultar la entrada **Escanear documento**.

## Experiencia del usuario

1. En su página web, el usuario toca un `<input type="file">`.
2. La app muestra un cuadro de diálogo de carga con entradas como *Escanear documento*, *Tomar foto*, *Capturar vídeo* y *Elegir de la galería* (dependiendo del atributo `accept` del input).
3. Al tocar **Escanear documento** se inicia el escáner de ML Kit de Google: detecta los bordes, recorta y mejora cada página, permite añadir más páginas y devuelve un PDF.
4. El PDF resultante se introduce de nuevo en el `<input type="file">`: su aplicación web lo recibe exactamente igual que cualquier otro archivo cargado.

**Notas:** Requiere Google Play Services (disponible en todos los teléfonos Android estándar con Play Store). El formato del resultado es **PDF**, con un máximo de 5 páginas por escaneo. La importación desde la galería dentro del escáner está permitida de forma predeterminada.

---

## Seguir leyendo

- ← Anterior: [Biometric Auth API](biometric-auth.md)
- Siguiente →: [Printer API](printer.md)
- La misma función en otras plataformas: [iOS – Escáner de documentos](../ios/document-scanner.md)
- Idiomas: [🇺🇸 English](../../android/document-scanner.md) · [🇩🇪 Deutsch](../../de/android/document-scanner.md) · [🇫🇷 Français](../../fr/android/document-scanner.md) · **🇪🇸 Español** · [🇨🇳 中文](../../zh/android/document-scanner.md)

> [!TIP]
> **¿Sin tiempo? Configuramos su app por usted.** Nuestro equipo configura, compila & publica su app WebViewGold: llave en mano, entrega rápida, Made in Germany. [Configurar mi app →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_android_doc_online)
>
> **Compile en su navegador:** Sin Mac ni IDE: el **WebViewGold Cloud Builder** configura, compila & sube su app en línea. [Descubra Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=android_docs)
