---
title: "API de impresora – Documentación de WebViewGold para iOS"
description: "Imprima imágenes y PDF desde su aplicación web mediante AirPrint: envíe archivos al diálogo de impresión nativo de iOS con un solo enlace."
lang: "es"
product: "WebViewGold para iOS"
platform: "iOS"
category: "API y funciones"
slug: "printer"
canonical_url: "https://www.webviewgold.com/es/docs/iOS/printer/"
keywords:
  - "API de impresora"
  - "WebViewGold para iOS"
  - "convertir sitio web en app"
  - "documentación de app WebView"
  - "SDK WebView de iOS"
  - "PWA a app"
  - "HTML a app"
  - "puente de JavaScript"
last_updated: "2026-10-09"
---

# API de impresora – WebViewGold para iOS

> **Resumen:** Imprima imágenes y PDF desde su aplicación web mediante AirPrint: envíe archivos al diálogo de impresión nativo de iOS con un solo enlace.

[Documentación](../README.md) › [WebViewGold para iOS](README.md) › API de impresora

**Plataforma:** iOS · **Categoría:** API y funciones · **Versión en línea:** [www.webviewgold.com/es/docs/iOS/printer/](https://www.webviewgold.com/es/docs/iOS/printer/)

---

La **API de impresora** envía un archivo remoto (imagen o PDF) al diálogo de impresión nativo de iOS (**AirPrint**), para que el usuario pueda imprimirlo en cualquier impresora configurada o guardarlo como PDF.

## Cómo usarla

```html
<a href="printitem://?jobName=Factura%20%23123&printItem=https://example.com/invoice.pdf">
  Imprimir factura
</a>
```

## Parámetros de consulta

| Nombre | Obligatorio | Descripción |
| --- | --- | --- |
| `printItem` | sí | URL completa del archivo que se debe imprimir (PDF, JPG, PNG, WebP…). |
| `jobName` | no | Nombre legible del trabajo que se muestra en el diálogo de impresión. |

## Cómo funciona

1. La aplicación descarga el archivo de `printItem` en una caché temporal.
2. El archivo se entrega al `UIPrintInteractionController` nativo, que muestra el diálogo de impresión de iOS.
3. El usuario elige una impresora AirPrint (o **Guardar como PDF** mediante las opciones de compartir) y confirma.

**Notas:** El archivo de destino debe ser accesible públicamente desde el dispositivo (la URL debe resolverse). Codifique los caracteres especiales del parámetro `jobName` en formato URL (p. ej., `%20` para espacios).

---

## Seguir leyendo

- ← Anterior: [API de descarga de archivos](file-downloader.md)
- Siguiente →: [API de calendario iCal](ical-calendar.md)
- La misma función en otras plataformas: [Android – Printer API](../android/printer.md)
- Idiomas: [🇺🇸 English](../../ios/printer.md) · [🇩🇪 Deutsch](../../de/ios/printer.md) · [🇫🇷 Français](../../fr/ios/printer.md) · **🇪🇸 Español** · [🇨🇳 中文](../../zh/ios/printer.md)

> [!TIP]
> **¿Sin tiempo? Configuramos su app por usted.** Nuestro equipo configura, compila & publica su app WebViewGold: llave en mano, entrega rápida, Made in Germany. [Configurar mi app →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **Compile en su navegador:** Sin Mac ni IDE: el **WebViewGold Cloud Builder** configura, compila & sube su app en línea. [Descubra Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
