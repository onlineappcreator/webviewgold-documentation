---
title: "API de Portapapeles – Documentación de WebViewGold para iOS"
description: "Copie texto al portapapeles de iOS y lea el contenido del portapapeles desde su aplicación web mediante JavaScript."
lang: "es"
product: "WebViewGold para iOS"
platform: "iOS"
category: "API y funciones"
slug: "clipboard"
canonical_url: "https://www.webviewgold.com/es/docs/iOS/clipboard/"
keywords:
  - "API de Portapapeles"
  - "WebViewGold para iOS"
  - "convertir sitio web en app"
  - "documentación de app WebView"
  - "SDK WebView de iOS"
  - "PWA a app"
  - "HTML a app"
  - "puente de JavaScript"
last_updated: "2026-10-09"
---

# API de Portapapeles – WebViewGold para iOS

> **Resumen:** Copie texto al portapapeles de iOS y lea el contenido del portapapeles desde su aplicación web mediante JavaScript.

[Documentación](../README.md) › [WebViewGold para iOS](README.md) › API de Portapapeles

**Plataforma:** iOS · **Categoría:** API y funciones · **Versión en línea:** [www.webviewgold.com/es/docs/iOS/clipboard/](https://www.webviewgold.com/es/docs/iOS/clipboard/)

---

Llame a `getclipboard://` para inyectar el contenido actual del portapapeles en la variable de JavaScript `clipboarddata`.

```html
<a href="getclipboard://">Read Clipboard</a>
<script>
function showClipboard() {
    console.log(clipboarddata);
}
</script>
```

---

## Seguir leyendo

- ← Anterior: [API Shortcut](shortcut.md)
- Siguiente →: [API de lectura/escritura de valores](read-write-value.md)
- La misma función en otras plataformas: [Android – API de portapapeles](../android/clipboard.md)
- Idiomas: [🇺🇸 English](../../ios/clipboard.md) · [🇩🇪 Deutsch](../../de/ios/clipboard.md) · [🇫🇷 Français](../../fr/ios/clipboard.md) · **🇪🇸 Español** · [🇨🇳 中文](../../zh/ios/clipboard.md)

> [!TIP]
> **¿Sin tiempo? Configuramos su app por usted.** Nuestro equipo configura, compila & publica su app WebViewGold: llave en mano, entrega rápida, Made in Germany. [Configurar mi app →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **Compile en su navegador:** Sin Mac ni IDE: el **WebViewGold Cloud Builder** configura, compila & sube su app en línea. [Descubra Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
