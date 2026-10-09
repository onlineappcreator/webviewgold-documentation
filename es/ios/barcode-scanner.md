---
title: "API de escáner de códigos de barras – Documentación de WebViewGold para iOS"
description: "Escanee códigos de barras EAN, UPC y otros de forma nativa en su app WebView de iOS y transfiera los resultados a su aplicación web."
lang: "es"
product: "WebViewGold para iOS"
platform: "iOS"
category: "API y funciones"
slug: "barcode-scanner"
canonical_url: "https://www.webviewgold.com/es/docs/iOS/barcode-scanner/"
keywords:
  - "API de escáner de códigos de barras"
  - "WebViewGold para iOS"
  - "convertir sitio web en app"
  - "documentación de app WebView"
  - "SDK WebView de iOS"
  - "PWA a app"
  - "HTML a app"
  - "puente de JavaScript"
last_updated: "2026-10-09"
---

# API de escáner de códigos de barras – WebViewGold para iOS

> **Resumen:** Escanee códigos de barras EAN, UPC y otros de forma nativa en su app WebView de iOS y transfiera los resultados a su aplicación web.

[Documentación](../README.md) › [WebViewGold para iOS](README.md) › API de escáner de códigos de barras

**Plataforma:** iOS · **Categoría:** API y funciones · **Versión en línea:** [www.webviewgold.com/es/docs/iOS/barcode-scanner/](https://www.webviewgold.com/es/docs/iOS/barcode-scanner/)

---

La API del escáner de códigos de barras de WebViewGold permite que su aplicación basada en WebView active la cámara del dispositivo para escanear códigos de barras. Una vez escaneado con éxito un código de barras, el resultado se pasa automáticamente a su contenido web.

## Casos de uso

- Escanear códigos de barras de productos para sistemas de inventario
- Procesar tickets o códigos de acceso en aplicaciones de logística o de eventos
- Captura rápida de datos a partir de códigos de barras impresos

## Cómo activar el escáner

Use el siguiente HTML para iniciar el escáner nativo de códigos de barras:

```html
<a href="barcodescanner://">Start Barcode Scanner</a>
<a href="#" onClick="alert(barcodescanresult);">Show Scan Result</a>
```

- **Iniciar escáner de códigos de barras:** Abre la cámara del dispositivo para detectar los formatos de códigos de barras compatibles
- **Mostrar resultado del escaneo:** Muestra el contenido del código de barras escaneado almacenado en la variable JavaScript `barcodescanresult`

**Nota técnica:** Tras el escaneo, el valor decodificado del código de barras se inyecta en la página actual a través de la variable JavaScript `barcodescanresult`. Puede utilizar esta variable para autocompletar formularios, activar lógica personalizada o realizar búsquedas basadas en los datos escaneados.

**Permisos:** Asegúrese de que la aplicación tenga acceso a la cámara del dispositivo, ya que es necesario para que el escaneo de códigos de barras funcione correctamente.

---

## Seguir leyendo

- ← Anterior: [API de escáner de QR](qr-code-scanner.md)
- Siguiente →: [API de modo de escaneo](scanning-mode.md)
- La misma función en otras plataformas: [Android – API de escáner de códigos de barras](../android/barcode-scanner.md)
- Idiomas: [🇺🇸 English](../../ios/barcode-scanner.md) · [🇩🇪 Deutsch](../../de/ios/barcode-scanner.md) · [🇫🇷 Français](../../fr/ios/barcode-scanner.md) · **🇪🇸 Español** · [🇨🇳 中文](../../zh/ios/barcode-scanner.md)

> [!TIP]
> **¿Sin tiempo? Configuramos su app por usted.** Nuestro equipo configura, compila & publica su app WebViewGold: llave en mano, entrega rápida, Made in Germany. [Configurar mi app →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **Compile en su navegador:** Sin Mac ni IDE: el **WebViewGold Cloud Builder** configura, compila & sube su app en línea. [Descubra Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
