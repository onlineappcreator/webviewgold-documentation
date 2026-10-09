---
title: "API de restablecer app – Documentación de WebViewGold para iOS"
description: "Restablezca la caché, las cookies y el almacenamiento local de su app WebView de iOS con un solo enlace o llamada de JavaScript."
lang: "es"
product: "WebViewGold para iOS"
platform: "iOS"
category: "API y funciones"
slug: "reset-app"
canonical_url: "https://www.webviewgold.com/es/docs/iOS/reset-app/"
keywords:
  - "API de restablecer app"
  - "WebViewGold para iOS"
  - "convertir sitio web en app"
  - "documentación de app WebView"
  - "SDK WebView de iOS"
  - "PWA a app"
  - "HTML a app"
  - "puente de JavaScript"
last_updated: "2026-10-09"
---

# API de restablecer app – WebViewGold para iOS

> **Resumen:** Restablezca la caché, las cookies y el almacenamiento local de su app WebView de iOS con un solo enlace o llamada de JavaScript.

[Documentación](../README.md) › [WebViewGold para iOS](README.md) › API de restablecer app

**Plataforma:** iOS · **Categoría:** API y funciones · **Versión en línea:** [www.webviewgold.com/es/docs/iOS/reset-app/](https://www.webviewgold.com/es/docs/iOS/reset-app/)

---

En determinados casos, restablecer la aplicación a su configuración inicial (borrando las cookies y la caché) puede ser necesario para restaurar un rendimiento óptimo. La **API de restablecimiento de la aplicación** proporciona una forma sencilla de iniciar este restablecimiento.

## Uso

Para restablecer los datos de la aplicación, simplemente utilice el siguiente enlace dentro de su aplicación:

```html
<a href="reset://">Reset App Link</a>
```

Este enlace hará lo siguiente:

- Borrar todas las cookies
- Borrar los datos en caché

## Prueba de la funcionalidad de restablecimiento

Para probar esta función, añada la siguiente URL de demostración a su aplicación WebViewGold: <https://www.onlineappcreator.com/reset_test.html>

**Nota:** Utilice la funcionalidad de restablecimiento con criterio, ya que borrará los datos del usuario relacionados con las cookies y la caché, lo que podría afectar a la configuración guardada o a los datos de sesión, incluido el cierre de sesión de los usuarios en sesiones activas.

---

## Seguir leyendo

- ← Anterior: [API de linterna](flashlight.md)
- Siguiente →: [API de decisión de seguimiento](user-tracking.md)
- La misma función en otras plataformas: [Android – API de restablecimiento](../android/reset-app.md)
- Idiomas: [🇺🇸 English](../../ios/reset-app.md) · [🇩🇪 Deutsch](../../de/ios/reset-app.md) · [🇫🇷 Français](../../fr/ios/reset-app.md) · **🇪🇸 Español** · [🇨🇳 中文](../../zh/ios/reset-app.md)

> [!TIP]
> **¿Sin tiempo? Configuramos su app por usted.** Nuestro equipo configura, compila & publica su app WebViewGold: llave en mano, entrega rápida, Made in Germany. [Configurar mi app →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **Compile en su navegador:** Sin Mac ni IDE: el **WebViewGold Cloud Builder** configura, compila & sube su app en línea. [Descubra Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
