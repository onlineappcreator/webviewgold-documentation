---
title: "Plugin Siri – Documentación de WebViewGold para iOS"
description: "Añada compatibilidad con los atajos de Siri a su app WebView de iOS y abra el contenido de la app por voz."
lang: "es"
product: "WebViewGold para iOS"
platform: "iOS"
category: "Extensiones y plugins"
slug: "siri"
canonical_url: "https://www.webviewgold.com/es/docs/iOS/siri/"
keywords:
  - "Plugin Siri"
  - "WebViewGold para iOS"
  - "convertir sitio web en app"
  - "documentación de app WebView"
  - "SDK WebView de iOS"
  - "PWA a app"
  - "HTML a app"
  - "puente de JavaScript"
last_updated: "2026-10-09"
---

# Plugin Siri – WebViewGold para iOS

> **Resumen:** Añada compatibilidad con los atajos de Siri a su app WebView de iOS y abra el contenido de la app por voz.

[Documentación](../README.md) › [WebViewGold para iOS](README.md) › Plugin Siri

**Plataforma:** iOS · **Categoría:** Extensiones y plugins · **Versión en línea:** [www.webviewgold.com/es/docs/iOS/siri/](https://www.webviewgold.com/es/docs/iOS/siri/)

---

Active la integración con Siri introduciendo su token de plugin en `static let siriEnabled` dentro de `Config.swift` y añadiendo la capacidad de Siri al target de WebViewGold.\
Contacte con [webviewgold-siri@onlineappcreator.com](mailto:webviewgold-siri@onlineappcreator.com) para más información.

## Cómo implementar la funcionalidad de Siri

1. Cree una función de JavaScript que Siri deba activar:

```javascript
function playRadio() {
   // Add desired functionality
}
```

2. Añada un botón o enlace para registrar el comando de Siri (evite frases como "Open", que pueden confundir a Siri):

```html
<a href="addtosiri://?command=Play%20Radio&jsFunction=playRadio()">Add Play Radio to Siri</a>
```

El parámetro `command` proporciona la frase recomendada, mientras que `jsFunction` especifica la función de JavaScript que se debe ejecutar.

---

## Seguir leyendo

- ← Anterior: [Plugin NFC](nfc.md)
- Siguiente →: [Plugin HealthKit](healthkit.md)
- Idiomas: [🇺🇸 English](../../ios/siri.md) · [🇩🇪 Deutsch](../../de/ios/siri.md) · [🇫🇷 Français](../../fr/ios/siri.md) · **🇪🇸 Español** · [🇨🇳 中文](../../zh/ios/siri.md)

> [!TIP]
> **¿Sin tiempo? Configuramos su app por usted.** Nuestro equipo configura, compila & publica su app WebViewGold: llave en mano, entrega rápida, Made in Germany. [Configurar mi app →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **Compile en su navegador:** Sin Mac ni IDE: el **WebViewGold Cloud Builder** configura, compila & sube su app en línea. [Descubra Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
