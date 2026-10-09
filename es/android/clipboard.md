---
title: "API de portapapeles – Documentación de WebViewGold para Android"
description: "Copie texto al portapapeles de Android y lea su contenido desde su aplicación web mediante JavaScript."
lang: "es"
product: "WebViewGold para Android"
platform: "Android"
category: "API y funciones"
slug: "clipboard"
canonical_url: "https://www.webviewgold.com/es/docs/android/clipboard/"
keywords:
  - "API de portapapeles"
  - "WebViewGold para Android"
  - "convertir sitio web en app"
  - "documentación de app WebView"
  - "SDK WebView de Android"
  - "PWA a app"
  - "HTML a app"
  - "puente de JavaScript"
last_updated: "2026-10-09"
---

# API de portapapeles – WebViewGold para Android

> **Resumen:** Copie texto al portapapeles de Android y lea su contenido desde su aplicación web mediante JavaScript.

[Documentación](../README.md) › [WebViewGold para Android](README.md) › API de portapapeles

**Plataforma:** Android · **Categoría:** API y funciones · **Versión en línea:** [www.webviewgold.com/es/docs/android/clipboard/](https://www.webviewgold.com/es/docs/android/clipboard/)

---

La API de portapapeles de WebViewGold ofrece una forma sencilla y segura de acceder al contenido del portapapeles del dispositivo desde su app basada en WebView. Sirve como alternativa a depender del acceso nativo al portapapeles del WebView, ofreciendo una mayor fiabilidad entre plataformas y actualizaciones.

## Casos de uso

- Rellenar previamente campos de formulario con datos copiados
- Mejorar los flujos de usuario en apps de autenticación, toma de notas o de compartir contenido
- Crear funciones de pegado rápido o herramientas de historial del portapapeles

## Cómo obtener el contenido del portapapeles

Para acceder a los datos del portapapeles, utilice la siguiente llamada:

```html
<a href="getclipboard://">Get Clipboard Data</a>
<a href="#" onClick="alert(clipboarddata);">Show Clipboard Data</a>
```

- **Get Clipboard Data:** activa la función nativa de lectura del portapapeles.
- **Show Clipboard Data:** muestra el resultado almacenado en la variable JavaScript `clipboarddata`.

**Nota técnica:** una vez que se activa `getclipboard://`, WebViewGold inyecta automáticamente el contenido del portapapeles en la variable JavaScript `clipboarddata` de la página, dejándolo accesible para cualquier acción posterior.

---

## Seguir leyendo

- ← Anterior: [API de indicador de carga](loading-sign.md)
- Siguiente →: [API de UUID](uuid.md)
- La misma función en otras plataformas: [iOS – API de Portapapeles](../ios/clipboard.md)
- Idiomas: [🇺🇸 English](../../android/clipboard.md) · [🇩🇪 Deutsch](../../de/android/clipboard.md) · [🇫🇷 Français](../../fr/android/clipboard.md) · **🇪🇸 Español** · [🇨🇳 中文](../../zh/android/clipboard.md)

> [!TIP]
> **¿Sin tiempo? Configuramos su app por usted.** Nuestro equipo configura, compila & publica su app WebViewGold: llave en mano, entrega rápida, Made in Germany. [Configurar mi app →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_android_doc_online)
>
> **Compile en su navegador:** Sin Mac ni IDE: el **WebViewGold Cloud Builder** configura, compila & sube su app en línea. [Descubra Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=android_docs)
