---
title: "Pie de navegación nativo – Documentación de WebViewGold para iOS"
description: "Active una barra de navegación inferior nativa con botones de atrás, adelante y personalizados en su app iOS."
lang: "es"
product: "WebViewGold para iOS"
platform: "iOS"
category: "Extensiones y plugins"
slug: "navigation-footer"
canonical_url: "https://www.webviewgold.com/es/docs/iOS/navigation-footer/"
keywords:
  - "Pie de navegación nativo"
  - "WebViewGold para iOS"
  - "convertir sitio web en app"
  - "documentación de app WebView"
  - "SDK WebView de iOS"
  - "PWA a app"
  - "HTML a app"
  - "puente de JavaScript"
last_updated: "2026-10-09"
---

# Pie de navegación nativo – WebViewGold para iOS

> **Resumen:** Active una barra de navegación inferior nativa con botones de atrás, adelante y personalizados en su app iOS.

[Documentación](../README.md) › [WebViewGold para iOS](README.md) › Pie de navegación nativo

**Plataforma:** iOS · **Categoría:** Extensiones y plugins · **Versión en línea:** [www.webviewgold.com/es/docs/iOS/navigation-footer/](https://www.webviewgold.com/es/docs/iOS/navigation-footer/)

---

Establezca `var showNavFooter = true` en `Config.swift` para habilitar la barra de pie de navegación nativa. Configure los botones y enlaces en `FooterBar.json`. Ejemplo:

```json
{
   "colour":"dark",
   "layout":[
      {
         "redirection_link":"https://webviewgoldtest.github.io/index.html",
         "sf_symbol":"house",
         "name": "Home"
      },
      {
         "redirection_link":"https://webviewgoldtest.github.io/appControls.html",
         "sf_symbol":"wrench.and.screwdriver",
         "name": "Controls"
      },
      {
         "redirection_link":"https://webviewgoldtest.github.io/NFCtesting.html",
         "sf_symbol":"wifi.square",
         "name": "NFC"
      },
      {
         "redirection_link":"https://webviewgoldtest.github.io/IAPtesting.html",
         "sf_symbol":"cart",
         "name": "Purchases"
      },
      {
         "redirection_link":"https://webviewgoldtest.github.io/permissions.html",
         "sf_symbol":"lock.open",
         "name": "Permissions"
      }
   ]
}
```

Cada `sf_symbol` utiliza un [SF Symbol](https://developer.apple.com/sf-symbols/) y abre el `redirection_link` en el WebView principal.

---

## Seguir leyendo

- ← Anterior: [App Clip Extension](app-clip.md)
- Siguiente →: [Barra lateral nativa](sidebar.md)
- La misma función en otras plataformas: [Android – Navigation Drawer & Footer](../android/navigation-drawer.md)
- Idiomas: [🇺🇸 English](../../ios/navigation-footer.md) · [🇩🇪 Deutsch](../../de/ios/navigation-footer.md) · [🇫🇷 Français](../../fr/ios/navigation-footer.md) · **🇪🇸 Español** · [🇨🇳 中文](../../zh/ios/navigation-footer.md)

> [!TIP]
> **¿Sin tiempo? Configuramos su app por usted.** Nuestro equipo configura, compila & publica su app WebViewGold: llave en mano, entrega rápida, Made in Germany. [Configurar mi app →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **Compile en su navegador:** Sin Mac ni IDE: el **WebViewGold Cloud Builder** configura, compila & sube su app en línea. [Descubra Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
