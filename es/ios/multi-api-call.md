---
title: "Función MultiAPICall – Documentación de WebViewGold para iOS"
description: "Encadene varias llamadas a la API de WebViewGold en una sola petición con la función MultiAPICall para iOS."
lang: "es"
product: "WebViewGold para iOS"
platform: "iOS"
category: "Extensiones y plugins"
slug: "multi-api-call"
canonical_url: "https://www.webviewgold.com/es/docs/iOS/multi-api-call/"
keywords:
  - "Función MultiAPICall"
  - "WebViewGold para iOS"
  - "convertir sitio web en app"
  - "documentación de app WebView"
  - "SDK WebView de iOS"
  - "PWA a app"
  - "HTML a app"
  - "puente de JavaScript"
last_updated: "2026-10-09"
---

# Función MultiAPICall – WebViewGold para iOS

> **Resumen:** Encadene varias llamadas a la API de WebViewGold en una sola petición con la función MultiAPICall para iOS.

[Documentación](../README.md) › [WebViewGold para iOS](README.md) › Función MultiAPICall

**Plataforma:** iOS · **Categoría:** Extensiones y plugins · **Versión en línea:** [www.webviewgold.com/es/docs/iOS/multi-api-call/](https://www.webviewgold.com/es/docs/iOS/multi-api-call/)

---

Esta es una **función opcional para iOS**, ya que los navegadores basados en Apple procesan las recargas múltiples de una misma página con el mismo script de forma diferente a los navegadores basados en Android.
Esto significa que llamar a *window.location.href = "exampleAPItrigger"* varias veces en el mismo script de la página web no funcionará en iOS, a diferencia de Android.\
La función MultiAPICall **le permite llamar a varias API en una sola asignación de *window.location.href*** al final del script de su página web. Esto puede resultarle útil si desea precargar más de una función de datos de la aplicación, lista para usarse en una página.\
**MultiAPICall admite las siguientes API de recopilación de datos como entradas:**
"[get-uuid](uuid.md)", "[user-disable-tracking](user-tracking.md)", "[getonesignalplayerid](push-notifications.md#getonesignalid)", "[getappversion](app-version-check.md)", "[__haptics (light, medium, heavy, success, warning, error)](haptic-feedback.md)"\
Utilice JavaScript con este tipo de URL para llamar a varias API a la vez (**asegúrese de incluir una comprobación para usarlo únicamente en la plataforma iOS**):

```html
<script>
// Example combination: "getonesignalplayerid" and "getappversion"

if (getMobileOperatingSystem() == "iOS") {
    // iOS: Use MultiAPICall feature, separate API names by commas (","), NO spaces
    window.location.href = "multiapicall://getonesignalplayerid,getappversion";
} else {
    // Android: Can handle multiple calls at once, use normal API call structure
    window.location.href = "getonesignalplayerid://";
    window.location.href = "getappversion://";
}
</script>
```

Haga clic [aquí](https://webviewgoldtest.github.io/multiAPI.html) para ver una página web de demostración de esta función. Inspeccione la página para ver el código de ejemplo.

---

## Seguir leyendo

- ← Anterior: [Detección de captura de pantalla](screen-capture.md)
- Siguiente →: [Plugin NFC](nfc.md)
- La misma función en otras plataformas: [Android – Multi API Call](../android/multi-api-call.md)
- Idiomas: [🇺🇸 English](../../ios/multi-api-call.md) · [🇩🇪 Deutsch](../../de/ios/multi-api-call.md) · [🇫🇷 Français](../../fr/ios/multi-api-call.md) · **🇪🇸 Español** · [🇨🇳 中文](../../zh/ios/multi-api-call.md)

> [!TIP]
> **¿Sin tiempo? Configuramos su app por usted.** Nuestro equipo configura, compila & publica su app WebViewGold: llave en mano, entrega rápida, Made in Germany. [Configurar mi app →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **Compile en su navegador:** Sin Mac ni IDE: el **WebViewGold Cloud Builder** configura, compila & sube su app en línea. [Descubra Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
