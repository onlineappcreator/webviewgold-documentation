---
title: "Share Extension – Documentación de WebViewGold para iOS"
description: "Permita que los usuarios compartan contenido de otras apps directamente en su app WebView de iOS con una Share Extension."
lang: "es"
product: "WebViewGold para iOS"
platform: "iOS"
category: "Extensiones y plugins"
slug: "share-extension"
canonical_url: "https://www.webviewgold.com/es/docs/iOS/share-extension/"
keywords:
  - "Share Extension"
  - "WebViewGold para iOS"
  - "convertir sitio web en app"
  - "documentación de app WebView"
  - "SDK WebView de iOS"
  - "PWA a app"
  - "HTML a app"
  - "puente de JavaScript"
last_updated: "2026-10-09"
---

# Share Extension – WebViewGold para iOS

> **Resumen:** Permita que los usuarios compartan contenido de otras apps directamente en su app WebView de iOS con una Share Extension.

[Documentación](../README.md) › [WebViewGold para iOS](README.md) › Share Extension

**Plataforma:** iOS · **Categoría:** Extensiones y plugins · **Versión en línea:** [www.webviewgold.com/es/docs/iOS/share-extension/](https://www.webviewgold.com/es/docs/iOS/share-extension/)

---

Cuando los usuarios comparten texto o imágenes con su aplicación desde aplicaciones como Fotos o Safari, los datos quedan disponibles en la variable JavaScript `sharedData`. Las imágenes compartidas se proporcionan como cadenas Base64.

```html
<script>
if (typeof sharedData !== 'undefined') {
    console.log(sharedData);
}
</script>
```

---

## Seguir leyendo

- ← Anterior: [API para abrir los ajustes](open-app-settings.md)
- Siguiente →: [Widget Extension](widget-extension.md)
- La misma función en otras plataformas: [Android – API ShareIntent](../android/share-intent.md)
- Idiomas: [🇺🇸 English](../../ios/share-extension.md) · [🇩🇪 Deutsch](../../de/ios/share-extension.md) · [🇫🇷 Français](../../fr/ios/share-extension.md) · **🇪🇸 Español** · [🇨🇳 中文](../../zh/ios/share-extension.md)

> [!TIP]
> **¿Sin tiempo? Configuramos su app por usted.** Nuestro equipo configura, compila & publica su app WebViewGold: llave en mano, entrega rápida, Made in Germany. [Configurar mi app →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **Compile en su navegador:** Sin Mac ni IDE: el **WebViewGold Cloud Builder** configura, compila & sube su app en línea. [Descubra Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
