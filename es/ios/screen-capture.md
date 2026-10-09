---
title: "Detección de captura de pantalla – Documentación de WebViewGold para iOS"
description: "Detecte capturas y grabaciones de pantalla en su app iOS y reaccione desde su aplicación web."
lang: "es"
product: "WebViewGold para iOS"
platform: "iOS"
category: "Extensiones y plugins"
slug: "screen-capture"
canonical_url: "https://www.webviewgold.com/es/docs/iOS/screen-capture/"
keywords:
  - "Detección de captura de pantalla"
  - "WebViewGold para iOS"
  - "convertir sitio web en app"
  - "documentación de app WebView"
  - "SDK WebView de iOS"
  - "PWA a app"
  - "HTML a app"
  - "puente de JavaScript"
last_updated: "2026-10-09"
---

# Detección de captura de pantalla – WebViewGold para iOS

> **Resumen:** Detecte capturas y grabaciones de pantalla en su app iOS y reaccione desde su aplicación web.

[Documentación](../README.md) › [WebViewGold para iOS](README.md) › Detección de captura de pantalla

**Plataforma:** iOS · **Categoría:** Extensiones y plugins · **Versión en línea:** [www.webviewgold.com/es/docs/iOS/screen-capture/](https://www.webviewgold.com/es/docs/iOS/screen-capture/)

---

Establezca `let preventScreenCapture = true` en `Config.swift` para detectar capturas de pantalla o grabaciones de pantalla y llamar automáticamente a la función JavaScript `onScreenCaptureAttempt`.

```html
<script>
function onScreenCaptureAttempt() {
    alert('Screen capture detected');
}
</script>
```

---

## Seguir leyendo

- ← Anterior: [Barra lateral nativa](sidebar.md)
- Siguiente →: [Función MultiAPICall](multi-api-call.md)
- Idiomas: [🇺🇸 English](../../ios/screen-capture.md) · [🇩🇪 Deutsch](../../de/ios/screen-capture.md) · [🇫🇷 Français](../../fr/ios/screen-capture.md) · **🇪🇸 Español** · [🇨🇳 中文](../../zh/ios/screen-capture.md)

> [!TIP]
> **¿Sin tiempo? Configuramos su app por usted.** Nuestro equipo configura, compila & publica su app WebViewGold: llave en mano, entrega rápida, Made in Germany. [Configurar mi app →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **Compile en su navegador:** Sin Mac ni IDE: el **WebViewGold Cloud Builder** configura, compila & sube su app en línea. [Descubra Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
