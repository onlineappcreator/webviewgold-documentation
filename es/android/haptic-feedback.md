---
title: "API de respuesta háptica – Documentación de WebViewGold para Android"
description: "Active la respuesta háptica por vibración nativa desde su aplicación web para lograr una sensación de app nativa en Android."
lang: "es"
product: "WebViewGold para Android"
platform: "Android"
category: "API y funciones"
slug: "haptic-feedback"
canonical_url: "https://www.webviewgold.com/es/docs/android/haptic-feedback/"
keywords:
  - "API de respuesta háptica"
  - "WebViewGold para Android"
  - "convertir sitio web en app"
  - "documentación de app WebView"
  - "SDK WebView de Android"
  - "PWA a app"
  - "HTML a app"
  - "puente de JavaScript"
last_updated: "2026-10-09"
---

# API de respuesta háptica – WebViewGold para Android

> **Resumen:** Active la respuesta háptica por vibración nativa desde su aplicación web para lograr una sensación de app nativa en Android.

[Documentación](../README.md) › [WebViewGold para Android](README.md) › API de respuesta háptica

**Plataforma:** Android · **Categoría:** API y funciones · **Versión en línea:** [www.webviewgold.com/es/docs/android/haptic-feedback/](https://www.webviewgold.com/es/docs/android/haptic-feedback/)

---

**WebViewGold** permite implementar el control háptico nativo de Android dentro de su app web.
Con nuestra API, puede realizar las siguientes acciones:

| Nombre | Esquema de URL | Descripción |
| --- | --- | --- |
| Impacto ligero | lighthaptic:// | Se utiliza para una colisión entre elementos de interfaz pequeños y ligeros |
| Impacto fuerte | heavyhaptic:// | Se utiliza para una colisión entre elementos de interfaz grandes y pesados |
| Notificación de éxito | successhaptic:// | Indica que una tarea o acción se ha completado correctamente |
| Notificación de advertencia | warninghaptic:// | Indica que una tarea o acción ha generado algún tipo de advertencia |
| Notificación de error | errorhaptic:// | Indica que se ha producido un error |

A continuación puede ver un ejemplo de cómo se puede utilizar esta API, con una etiqueta de anclaje y una función JavaScript personalizada que interactúan con nuestra API háptica.

```html
<a onclick="lightHaptic('index.html')">Navigation Link with Haptics</a>

<script>
function lightHaptic(url) {
  if (isWebViewBrowser) {
    window.location.href = url;
    loadInnerHref("lighthaptic://");
  } else {
    window.location.href = url;
  }
}

function loadInnerHref(url) {
  iFrame = document.createElement("iframe");
  iFrame.setAttribute("src", url);
  document.body.appendChild(iFrame);
  iFrame.parentNode.removeChild(iFrame);
  iFrame = null;
}
</script>
```

Haga clic [aquí](https://webviewgoldtest.github.io/hapticFeedback.html) para ver una página web de demostración de esta función. Inspeccione la página para ver el código de ejemplo.

---

## Seguir leyendo

- ← Anterior: [API de interfaz dinámica](dynamic-ui.md)
- Siguiente →: [Plugin NFC](nfc.md)
- La misma función en otras plataformas: [iOS – API de respuesta háptica](../ios/haptic-feedback.md)
- Idiomas: [🇺🇸 English](../../android/haptic-feedback.md) · [🇩🇪 Deutsch](../../de/android/haptic-feedback.md) · [🇫🇷 Français](../../fr/android/haptic-feedback.md) · **🇪🇸 Español** · [🇨🇳 中文](../../zh/android/haptic-feedback.md)

> [!TIP]
> **¿Sin tiempo? Configuramos su app por usted.** Nuestro equipo configura, compila & publica su app WebViewGold: llave en mano, entrega rápida, Made in Germany. [Configurar mi app →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_android_doc_online)
>
> **Compile en su navegador:** Sin Mac ni IDE: el **WebViewGold Cloud Builder** configura, compila & sube su app en línea. [Descubra Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=android_docs)
