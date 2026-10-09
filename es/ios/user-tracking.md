---
title: "API de decisión de seguimiento del usuario – Documentación de WebViewGold para iOS"
description: "Respete App Tracking Transparency: lea la decisión de seguimiento del usuario y reaccione ante ella dentro de su app WebViewGold de iOS."
lang: "es"
product: "WebViewGold para iOS"
platform: "iOS"
category: "API y funciones"
slug: "user-tracking"
canonical_url: "https://www.webviewgold.com/es/docs/iOS/user-tracking/"
keywords:
  - "API de decisión de seguimiento"
  - "WebViewGold para iOS"
  - "convertir sitio web en app"
  - "documentación de app WebView"
  - "SDK WebView de iOS"
  - "PWA a app"
  - "HTML a app"
  - "puente de JavaScript"
last_updated: "2026-10-09"
---

# API de decisión de seguimiento del usuario – WebViewGold para iOS

> **Resumen:** Respete App Tracking Transparency: lea la decisión de seguimiento del usuario y reaccione ante ella dentro de su app WebViewGold de iOS.

[Documentación](../README.md) › [WebViewGold para iOS](README.md) › API de decisión de seguimiento

**Plataforma:** iOS · **Categoría:** API y funciones · **Versión en línea:** [www.webviewgold.com/es/docs/iOS/user-tracking/](https://www.webviewgold.com/es/docs/iOS/user-tracking/)

---

En iOS, las aplicaciones tienen que solicitar permiso para rastrear los datos del usuario según el framework AppTrackingTransparency de Apple. WebViewGold le permite ver qué opción eligió el usuario al instalar su aplicación para actuar en consecuencia en su aplicación web. La variable JavaScript **trackingDisabled** puede ser establecida por WebViewGold en true para indicar que el rastreo se ha bloqueado, o en false si no se ha bloqueado. En su aplicación web, puede comprobar fácilmente el estado de JavaScript obteniendo primero la variable JavaScript y mostrándola después en una alerta:

```html
<a href="user-disable-tracking://">Set JavaScript variable</a>
<a href="#" onClick="alert(trackingDisabled);">Show tracking decision</a>
```

---

## Seguir leyendo

- ← Anterior: [API de restablecer app](reset-app.md)
- Siguiente →: [API de indicador de carga](loading-sign.md)
- Idiomas: [🇺🇸 English](../../ios/user-tracking.md) · [🇩🇪 Deutsch](../../de/ios/user-tracking.md) · [🇫🇷 Français](../../fr/ios/user-tracking.md) · **🇪🇸 Español** · [🇨🇳 中文](../../zh/ios/user-tracking.md)

> [!TIP]
> **¿Sin tiempo? Configuramos su app por usted.** Nuestro equipo configura, compila & publica su app WebViewGold: llave en mano, entrega rápida, Made in Germany. [Configurar mi app →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **Compile en su navegador:** Sin Mac ni IDE: el **WebViewGold Cloud Builder** configura, compila & sube su app en línea. [Descubra Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
