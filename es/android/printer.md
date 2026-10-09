---
title: "Printer API – Documentación de WebViewGold para Android"
description: "Send a remote image or PDF to the Android system print dialog — Wi-Fi printers, cloud print, or Save-as-PDF, straight from your web app."
lang: "es"
product: "WebViewGold para Android"
platform: "Android"
category: "API y funciones"
slug: "printer"
canonical_url: "https://www.webviewgold.com/es/docs/android/printer/"
keywords:
  - "Printer API"
  - "WebViewGold para Android"
  - "convertir sitio web en app"
  - "documentación de app WebView"
  - "SDK WebView de Android"
  - "PWA a app"
  - "HTML a app"
  - "puente de JavaScript"
last_updated: "2026-10-09"
---

# Printer API – WebViewGold para Android

> **Resumen:** Send a remote image or PDF to the Android system print dialog — Wi-Fi printers, cloud print, or Save-as-PDF, straight from your web app.

[Documentación](../README.md) › [WebViewGold para Android](README.md) › Printer API

**Plataforma:** Android · **Categoría:** API y funciones · **Versión en línea:** [www.webviewgold.com/es/docs/android/printer/](https://www.webviewgold.com/es/docs/android/printer/)

---

La **API de impresora** envía un archivo remoto (imagen o PDF) al cuadro de diálogo de impresión del sistema Android, para que el usuario pueda imprimirlo en cualquier impresora configurada: Wi-Fi, impresión en la nube o «Guardar como PDF».

## Cómo utilizarla

```html
<a href="printitem://?jobName=Invoice%20%23123&printItem=https://example.com/invoice.pdf">
  Print invoice
</a>
```

## Parámetros de consulta

| Nombre | Obligatorio | Descripción |
| --- | --- | --- |
| `printItem` | sí | URL completa del archivo que se va a imprimir (PDF, JPG, PNG, WebP…). |
| `jobName` | no | Nombre legible del trabajo que se muestra en el cuadro de diálogo de impresión. Su valor predeterminado es `Print Job`. |

## Cómo funciona

1. La app descarga el archivo desde `printItem` a una caché temporal.
2. Si es una imagen, el archivo se imprime mediante `PrintHelper` (ajustado a la escala).
3. Si es un PDF (o cualquier otro formato de documento), se envía al `PrintManager` de Android con un adaptador de documento adecuado.
4. El archivo temporal se elimina una vez que el trabajo está en cola.

**Notas:** El archivo de destino debe ser accesible públicamente desde el dispositivo (la URL debe resolverse). Los usuarios pueden elegir **Guardar como PDF** en el cuadro de diálogo de impresión para exportar una copia.

---

## Seguir leyendo

- ← Anterior: [Document Scanner](document-scanner.md)
- Siguiente →: [Health Connect API](health-connect.md)
- La misma función en otras plataformas: [iOS – API de impresora](../ios/printer.md)
- Idiomas: [🇺🇸 English](../../android/printer.md) · [🇩🇪 Deutsch](../../de/android/printer.md) · [🇫🇷 Français](../../fr/android/printer.md) · **🇪🇸 Español** · [🇨🇳 中文](../../zh/android/printer.md)

> [!TIP]
> **¿Sin tiempo? Configuramos su app por usted.** Nuestro equipo configura, compila & publica su app WebViewGold: llave en mano, entrega rápida, Made in Germany. [Configurar mi app →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_android_doc_online)
>
> **Compile en su navegador:** Sin Mac ni IDE: el **WebViewGold Cloud Builder** configura, compila & sube su app en línea. [Descubra Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=android_docs)
