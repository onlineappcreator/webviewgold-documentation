---
title: "API de respuesta háptica – Documentación de WebViewGold para iOS"
description: "Active la respuesta háptica nativa (vibraciones) desde su aplicación web para una sensación de app verdaderamente nativa en iOS."
lang: "es"
product: "WebViewGold para iOS"
platform: "iOS"
category: "API y funciones"
slug: "haptic-feedback"
canonical_url: "https://www.webviewgold.com/es/docs/iOS/haptic-feedback/"
keywords:
  - "API de respuesta háptica"
  - "WebViewGold para iOS"
  - "convertir sitio web en app"
  - "documentación de app WebView"
  - "SDK WebView de iOS"
  - "PWA a app"
  - "HTML a app"
  - "puente de JavaScript"
last_updated: "2026-10-09"
---

# API de respuesta háptica – WebViewGold para iOS

> **Resumen:** Active la respuesta háptica nativa (vibraciones) desde su aplicación web para una sensación de app verdaderamente nativa en iOS.

[Documentación](../README.md) › [WebViewGold para iOS](README.md) › API de respuesta háptica

**Plataforma:** iOS · **Categoría:** API y funciones · **Versión en línea:** [www.webviewgold.com/es/docs/iOS/haptic-feedback/](https://www.webviewgold.com/es/docs/iOS/haptic-feedback/)

---

**WebViewGold** permite implementar el control háptico nativo de iOS dentro de su aplicación web.
Utilizando nuestra API, podrá realizar las siguientes acciones:

| Nombre | Esquema de URL | Descripción |
| --- | --- | --- |
| Impacto ligero | lighthaptic:// | Se utiliza para una colisión entre elementos de la interfaz pequeños y ligeros |
| Impacto medio | mediumhaptic:// | Se utiliza para una colisión entre elementos de la interfaz de tamaño moderado |
| Impacto fuerte | heavyhaptic:// | Se utiliza para una colisión entre elementos de la interfaz grandes y pesados |
| Notificación de éxito | successhaptic:// | Indica que una tarea o acción se ha completado con éxito |
| Notificación de advertencia | warninghaptic:// | Indica que una tarea o acción ha producido una advertencia de algún tipo |
| Notificación de error | errorhaptic:// | Indica que se ha producido un error |

Le sugerimos que revise la información general de [mejores prácticas](https://developer.apple.com/design/human-interface-guidelines/playing-haptics) de Apple antes de incluir estas funciones en su aplicación.
A continuación se muestra un ejemplo de cómo se puede utilizar esta API, con una etiqueta de anclaje y una función JavaScript personalizada que interactúan con nuestra API háptica.

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

- ← Anterior: [API de autenticación biométrica](biometric-authentication.md)
- Siguiente →: [API Shortcut](shortcut.md)
- La misma función en otras plataformas: [Android – API de respuesta háptica](../android/haptic-feedback.md)
- Idiomas: [🇺🇸 English](../../ios/haptic-feedback.md) · [🇩🇪 Deutsch](../../de/ios/haptic-feedback.md) · [🇫🇷 Français](../../fr/ios/haptic-feedback.md) · **🇪🇸 Español** · [🇨🇳 中文](../../zh/ios/haptic-feedback.md)

> [!TIP]
> **¿Sin tiempo? Configuramos su app por usted.** Nuestro equipo configura, compila & publica su app WebViewGold: llave en mano, entrega rápida, Made in Germany. [Configurar mi app →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **Compile en su navegador:** Sin Mac ni IDE: el **WebViewGold Cloud Builder** configura, compila & sube su app en línea. [Descubra Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
