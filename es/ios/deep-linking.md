---
title: "API de deep linking – Documentación de WebViewGold para iOS"
description: "Inicie su app iOS mediante esquemas de URL personalizados y dirija a los usuarios con deep links a páginas concretas de su aplicación web."
lang: "es"
product: "WebViewGold para iOS"
platform: "iOS"
category: "API y funciones"
slug: "deep-linking"
canonical_url: "https://www.webviewgold.com/es/docs/iOS/deep-linking/"
keywords:
  - "API de deep linking"
  - "WebViewGold para iOS"
  - "convertir sitio web en app"
  - "documentación de app WebView"
  - "SDK WebView de iOS"
  - "PWA a app"
  - "HTML a app"
  - "puente de JavaScript"
last_updated: "2026-10-09"
---

# API de deep linking – WebViewGold para iOS

> **Resumen:** Inicie su app iOS mediante esquemas de URL personalizados y dirija a los usuarios con deep links a páginas concretas de su aplicación web.

[Documentación](../README.md) › [WebViewGold para iOS](README.md) › API de deep linking

**Plataforma:** iOS · **Categoría:** API y funciones · **Versión en línea:** [www.webviewgold.com/es/docs/iOS/deep-linking/](https://www.webviewgold.com/es/docs/iOS/deep-linking/)

---

La **API de Deep Linking** facilita dirigir a los usuarios a contenido específico dentro de su aplicación. WebViewGold le permite configurar un esquema de URL personalizado (por ejemplo, `webviewgold://`) que se puede activar desde aplicaciones como **Mail, Safari y otras** para abrir enlaces directamente en su aplicación WebView.

**Nota:** la aplicación debe estar instalada previamente para que esta función funcione.

**Alternativamente**, es posible utilizar nuestra [**API de Universal Links**](universal-links.md). Aunque funciona de manera similar, utiliza una sintaxis diferente, más común que la de la API de Deep Linking. Para la mayoría de las aplicaciones, es sensato elegir una u otra, pero no ambas.

Para configurar el **Deep Linking** en su aplicación iOS, siga los pasos a continuación:

1. **Abra Config.swift:**
   - Establezca `ShowExternalLink` en `true`.

![Configuración de Deep Linking](../../assets/ios/img/universallinks.webp)
2. **Abra Info.plist:**
   - Cambie el URL Scheme al nombre de su propia aplicación (por ejemplo, `your-app-name://` en lugar de `webviewgold://`).

![Info.plist es una ubicación poderosa para configurar el deep linking que también se puede activar desde diferentes aplicaciones](../../assets/ios/img/infoplist.webp)

**¡Listo! :)** El siguiente ejemplo abriría google.com en la aplicación WebView:

```
WebViewGold://url?link=https://www.google.com
```

[![Ver el vídeo: API de deep linking](https://img.youtube.com/vi/mW4H_gUKU28/hqdefault.jpg)](https://www.youtube.com/watch?v=mW4H_gUKU28)

---

## Seguir leyendo

- ← Anterior: [API de Universal Links](universal-links.md)
- Siguiente →: [API de diálogo para compartir](app-sharing-dialog.md)
- La misma función en otras plataformas: [macOS – API Deeplinking](../macos/deep-linking.md)
- Idiomas: [🇺🇸 English](../../ios/deep-linking.md) · [🇩🇪 Deutsch](../../de/ios/deep-linking.md) · [🇫🇷 Français](../../fr/ios/deep-linking.md) · **🇪🇸 Español** · [🇨🇳 中文](../../zh/ios/deep-linking.md)

> [!TIP]
> **¿Sin tiempo? Configuramos su app por usted.** Nuestro equipo configura, compila & publica su app WebViewGold: llave en mano, entrega rápida, Made in Germany. [Configurar mi app →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **Compile en su navegador:** Sin Mac ni IDE: el **WebViewGold Cloud Builder** configura, compila & sube su app en línea. [Descubra Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
