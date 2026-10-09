---
title: "API de diálogo para compartir la app – Documentación de WebViewGold para Android"
description: "Active el diálogo nativo de Android para compartir desde su aplicación web y permita que los usuarios compartan su app o cualquier URL."
lang: "es"
product: "WebViewGold para Android"
platform: "Android"
category: "API y funciones"
slug: "app-sharing-dialog"
canonical_url: "https://www.webviewgold.com/es/docs/android/app-sharing-dialog/"
keywords:
  - "API de diálogo para compartir"
  - "WebViewGold para Android"
  - "convertir sitio web en app"
  - "documentación de app WebView"
  - "SDK WebView de Android"
  - "PWA a app"
  - "HTML a app"
  - "puente de JavaScript"
last_updated: "2026-10-09"
---

# API de diálogo para compartir la app – WebViewGold para Android

> **Resumen:** Active el diálogo nativo de Android para compartir desde su aplicación web y permita que los usuarios compartan su app o cualquier URL.

[Documentación](../README.md) › [WebViewGold para Android](README.md) › API de diálogo para compartir

**Plataforma:** Android · **Categoría:** API y funciones · **Versión en línea:** [www.webviewgold.com/es/docs/android/app-sharing-dialog/](https://www.webviewgold.com/es/docs/android/app-sharing-dialog/)

---

La API de diálogo de compartir de WebViewGold permite a sus usuarios compartir contenido de su app, como el enlace de descarga o mensajes personalizados, con amigos y familiares a través de sus apps preferidas (p. ej. WhatsApp, SMS, correo electrónico). Esta puede ser una forma eficaz de aumentar la visibilidad de su app y hacer crecer su base de usuarios.

## Cómo usar el diálogo de compartir en su app Android basada en WebView

Puede activar un diálogo de compartir nativo utilizando el esquema de URL `shareapp://` con parámetros de mensaje y URL personalizables.

A continuación se muestran ejemplos de las distintas formas de implementar esta función:

```html
<a href="shareapp://message?=Check out this cool thing!&url=https://www.webviewgold.com">Share (message, link)</a>

<a href="shareapp://message?=&url=https://www.webviewgold.com">Share (no message, link)</a>

<a href="shareapp://message?=Check out this cool thing!">Share (message, no link)</a>
```

![Ejemplo de diálogo de compartir de la app](../../assets/android/img/appshare.webp)

---

## Seguir leyendo

- ← Anterior: [API ShareIntent](share-intent.md)
- Siguiente →: [API de valoración In-App](in-app-rating.md)
- La misma función en otras plataformas: [iOS – API de diálogo para compartir](../ios/app-sharing-dialog.md)
- Idiomas: [🇺🇸 English](../../android/app-sharing-dialog.md) · [🇩🇪 Deutsch](../../de/android/app-sharing-dialog.md) · [🇫🇷 Français](../../fr/android/app-sharing-dialog.md) · **🇪🇸 Español** · [🇨🇳 中文](../../zh/android/app-sharing-dialog.md)

> [!TIP]
> **¿Sin tiempo? Configuramos su app por usted.** Nuestro equipo configura, compila & publica su app WebViewGold: llave en mano, entrega rápida, Made in Germany. [Configurar mi app →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_android_doc_online)
>
> **Compile en su navegador:** Sin Mac ni IDE: el **WebViewGold Cloud Builder** configura, compila & sube su app en línea. [Descubra Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=android_docs)
