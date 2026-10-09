---
title: "API de reconexión – Documentación de WebViewGold para iOS"
description: "Añada un botón «Reintentar» a su página de respaldo sin conexión que recargue la última URL en línea de su aplicación iOS."
lang: "es"
product: "WebViewGold para iOS"
platform: "iOS"
category: "API y funciones"
slug: "reconnect"
canonical_url: "https://www.webviewgold.com/es/docs/iOS/reconnect/"
keywords:
  - "API de reconexión"
  - "WebViewGold para iOS"
  - "convertir sitio web en app"
  - "documentación de app WebView"
  - "SDK WebView de iOS"
  - "PWA a app"
  - "HTML a app"
  - "puente de JavaScript"
last_updated: "2026-10-09"
---

# API de reconexión – WebViewGold para iOS

> **Resumen:** Añada un botón «Reintentar» a su página de respaldo sin conexión que recargue la última URL en línea de su aplicación iOS.

[Documentación](../README.md) › [WebViewGold para iOS](README.md) › API de reconexión

**Plataforma:** iOS · **Categoría:** API y funciones · **Versión en línea:** [www.webviewgold.com/es/docs/iOS/reconnect/](https://www.webviewgold.com/es/docs/iOS/reconnect/)

---

La **API de reconexión** recarga la última URL en línea en la que estaba el usuario antes de que su aplicación recurriera a la página HTML sin conexión. Está pensada como botón de «Reintentar» en su propia pantalla de respaldo sin conexión.

## Cómo usarla

Añada el disparador a su página sin conexión (normalmente `local-html/index.html`):

```html
<button onclick="window.location.href='reconnect://'">Intentar reconectar</button>
```

## Cómo funciona

La aplicación recuerda la última URL cargada correctamente. Cuando el usuario toca `reconnect://`, el WebView vuelve a esa URL. Si sigue sin haber conexión, se muestra de nuevo su página de respaldo.

## Configuración relacionada

- `offlinelocalhtmlswitch` en **Config.swift** debe estar en `true`, y necesita una página de respaldo `local-html/index.html` para que esta función tenga sentido. Consulte [Configurar su aplicación web](setup-website.md) para conocer los detalles del modo de respaldo sin conexión.

---

## Seguir leyendo

- ← Anterior: [Social Login Helper](social-login.md)
- Siguiente →: [API de CSS y JS personalizados](custom-css-js.md)
- La misma función en otras plataformas: [Android – Reconnect API](../android/reconnect.md)
- Idiomas: [🇺🇸 English](../../ios/reconnect.md) · [🇩🇪 Deutsch](../../de/ios/reconnect.md) · [🇫🇷 Français](../../fr/ios/reconnect.md) · **🇪🇸 Español** · [🇨🇳 中文](../../zh/ios/reconnect.md)

> [!TIP]
> **¿Sin tiempo? Configuramos su app por usted.** Nuestro equipo configura, compila & publica su app WebViewGold: llave en mano, entrega rápida, Made in Germany. [Configurar mi app →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **Compile en su navegador:** Sin Mac ni IDE: el **WebViewGold Cloud Builder** configura, compila & sube su app en línea. [Descubra Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
