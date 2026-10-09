---
title: "API de escáner de códigos de barras – Documentación de WebViewGold para Android"
description: "Escanee códigos de barras EAN, UPC y otros de forma nativa en su aplicación Android WebView y entregue los resultados a su aplicación web."
lang: "es"
product: "WebViewGold para Android"
platform: "Android"
category: "API y funciones"
slug: "barcode-scanner"
canonical_url: "https://www.webviewgold.com/es/docs/android/barcode-scanner/"
keywords:
  - "API de escáner de códigos de barras"
  - "WebViewGold para Android"
  - "convertir sitio web en app"
  - "documentación de app WebView"
  - "SDK WebView de Android"
  - "PWA a app"
  - "HTML a app"
  - "puente de JavaScript"
last_updated: "2026-10-09"
---

# API de escáner de códigos de barras – WebViewGold para Android

> **Resumen:** Escanee códigos de barras EAN, UPC y otros de forma nativa en su aplicación Android WebView y entregue los resultados a su aplicación web.

[Documentación](../README.md) › [WebViewGold para Android](README.md) › API de escáner de códigos de barras

**Plataforma:** Android · **Categoría:** API y funciones · **Versión en línea:** [www.webviewgold.com/es/docs/android/barcode-scanner/](https://www.webviewgold.com/es/docs/android/barcode-scanner/)

---

La API de escáner de códigos de barras de WebViewGold permite que su app basada en WebView active la cámara del dispositivo para escanear códigos de barras. Una vez escaneado correctamente un código de barras, el resultado se devuelve automáticamente a su contenido web.

## Casos de uso

- Escanear códigos de barras de productos para sistemas de inventario
- Procesar entradas o códigos de acceso en apps de logística o de eventos
- Permitir la captura rápida de datos desde códigos de barras impresos

## Cómo activar el escáner

Utilice el siguiente HTML para iniciar el escáner de códigos de barras nativo:

```html
<a href="barcodescanner://">Start Barcode Scanner</a>
<a href="#" onClick="alert(barcodescanresult);">Show Scan Result</a>
```

- **Start Barcode Scanner:** abre la cámara del dispositivo para detectar los formatos de código de barras compatibles
- **Show Scan Result:** muestra el contenido del código de barras escaneado almacenado en la variable JavaScript `barcodescanresult`

**Nota técnica:** tras el escaneo, el valor decodificado del código de barras se inyecta en la página actual a través de la variable JavaScript `barcodescanresult`. Puede usar esta variable para autocompletar formularios, activar lógica personalizada o realizar búsquedas basadas en los datos escaneados.

**Permisos:** asegúrese de que la app tenga acceso a la cámara del dispositivo, ya que es necesaria para que el escaneo de códigos de barras funcione correctamente.

---

## Seguir leyendo

- ← Anterior: [API de modo de escaneo](scanning-mode.md)
- Siguiente →: [API de captura de pantalla](take-screenshot.md)
- La misma función en otras plataformas: [iOS – API de escáner de códigos de barras](../ios/barcode-scanner.md)
- Idiomas: [🇺🇸 English](../../android/barcode-scanner.md) · [🇩🇪 Deutsch](../../de/android/barcode-scanner.md) · [🇫🇷 Français](../../fr/android/barcode-scanner.md) · **🇪🇸 Español** · [🇨🇳 中文](../../zh/android/barcode-scanner.md)

> [!TIP]
> **¿Sin tiempo? Configuramos su app por usted.** Nuestro equipo configura, compila & publica su app WebViewGold: llave en mano, entrega rápida, Made in Germany. [Configurar mi app →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_android_doc_online)
>
> **Compile en su navegador:** Sin Mac ni IDE: el **WebViewGold Cloud Builder** configura, compila & sube su app en línea. [Descubra Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=android_docs)
