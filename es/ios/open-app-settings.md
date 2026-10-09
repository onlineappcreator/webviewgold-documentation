---
title: "API para abrir los ajustes de la aplicación – Documentación de WebViewGold para iOS"
description: "Envíe a los usuarios directamente a la página de su aplicación en la app Ajustes de iOS para gestionar permisos y notificaciones."
lang: "es"
product: "WebViewGold para iOS"
platform: "iOS"
category: "API y funciones"
slug: "open-app-settings"
canonical_url: "https://www.webviewgold.com/es/docs/iOS/open-app-settings/"
keywords:
  - "API para abrir los ajustes"
  - "WebViewGold para iOS"
  - "convertir sitio web en app"
  - "documentación de app WebView"
  - "SDK WebView de iOS"
  - "PWA a app"
  - "HTML a app"
  - "puente de JavaScript"
last_updated: "2026-10-09"
---

# API para abrir los ajustes de la aplicación – WebViewGold para iOS

> **Resumen:** Envíe a los usuarios directamente a la página de su aplicación en la app Ajustes de iOS para gestionar permisos y notificaciones.

[Documentación](../README.md) › [WebViewGold para iOS](README.md) › API para abrir los ajustes

**Plataforma:** iOS · **Categoría:** API y funciones · **Versión en línea:** [www.webviewgold.com/es/docs/iOS/open-app-settings/](https://www.webviewgold.com/es/docs/iOS/open-app-settings/)

---

La **API para abrir los ajustes de la aplicación** de WebViewGold lleva al usuario directamente a la página de su aplicación en la app nativa **Ajustes** de iOS. Desde allí puede gestionar permisos (cámara, ubicación, notificaciones…), el idioma y otros ajustes de la aplicación, sin salir de su aplicación web para buscar en los Ajustes de iOS.

## Cómo usarla

Active la pantalla desde un enlace HTML o desde JavaScript:

```html
<a href="settingsapp://">Abrir ajustes de la aplicación</a>
```

```javascript
window.location.href = "settingsapp://";
```

## Casos de uso típicos

- El usuario denegó un permiso (cámara, micrófono, ubicación, notificaciones): envíelo directamente a la pantalla del sistema para volver a activarlo.
- Guiar al usuario a los ajustes de notificaciones de su aplicación, p. ej. en combinación con la llamada `checkNativePushPermissions://` de la [API de notificaciones push](push-notifications.md).

**Notas:** Sin parámetros. Cualquier URL que empiece por `settingsapp://` abre la misma pantalla.

---

## Seguir leyendo

- ← Anterior: [API de lectura/escritura de valores](read-write-value.md)
- Siguiente →: [Share Extension](share-extension.md)
- La misma función en otras plataformas: [Android – Open App Settings API](../android/open-app-settings.md)
- Idiomas: [🇺🇸 English](../../ios/open-app-settings.md) · [🇩🇪 Deutsch](../../de/ios/open-app-settings.md) · [🇫🇷 Français](../../fr/ios/open-app-settings.md) · **🇪🇸 Español** · [🇨🇳 中文](../../zh/ios/open-app-settings.md)

> [!TIP]
> **¿Sin tiempo? Configuramos su app por usted.** Nuestro equipo configura, compila & publica su app WebViewGold: llave en mano, entrega rápida, Made in Germany. [Configurar mi app →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **Compile en su navegador:** Sin Mac ni IDE: el **WebViewGold Cloud Builder** configura, compila & sube su app en línea. [Descubra Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
