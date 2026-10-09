---
title: "Navegación con barra lateral nativa – Documentación de WebViewGold para iOS"
description: "Active un menú lateral deslizante nativo con enlaces personalizados e iconos de SF Symbols, configurado mediante Sidebar.json."
lang: "es"
product: "WebViewGold para iOS"
platform: "iOS"
category: "Extensiones y plugins"
slug: "sidebar"
canonical_url: "https://www.webviewgold.com/es/docs/iOS/sidebar/"
keywords:
  - "Barra lateral nativa"
  - "WebViewGold para iOS"
  - "convertir sitio web en app"
  - "documentación de app WebView"
  - "SDK WebView de iOS"
  - "PWA a app"
  - "HTML a app"
  - "puente de JavaScript"
last_updated: "2026-10-09"
---

# Navegación con barra lateral nativa – WebViewGold para iOS

> **Resumen:** Active un menú lateral deslizante nativo con enlaces personalizados e iconos de SF Symbols, configurado mediante Sidebar.json.

[Documentación](../README.md) › [WebViewGold para iOS](README.md) › Barra lateral nativa

**Plataforma:** iOS · **Categoría:** Extensiones y plugins · **Versión en línea:** [www.webviewgold.com/es/docs/iOS/sidebar/](https://www.webviewgold.com/es/docs/iOS/sidebar/)

---

Además del [pie de navegación nativo](navigation-footer.md), WebViewGold incluye una **barra lateral deslizante** nativa para ofrecer una experiencia de navegación propia de una app sin tocar su sitio web. Un botón de menú flotante abre una barra lateral con sus enlaces: cada entrada hace que el WebView principal navegue a la URL que usted le asocie.

## Cómo activarla

Establezca la siguiente opción en **Config.swift**:

```swift
var enableSidebar = true
```

## Cómo configurarla

Abra **Sidebar.json** en el proyecto de Xcode y defina el esquema de color y las entradas del menú:

```json
{
   "colour":"dark",
   "layout":[
      {
         "redirection_link":"https://example.org/home",
         "sf_symbol":"house",
         "name": "Inicio"
      },
      {
         "redirection_link":"https://example.org/shop",
         "sf_symbol":"cart",
         "name": "Tienda"
      }
   ]
}
```

| Clave | Descripción |
| --- | --- |
| `colour` | Esquema de color de la barra lateral: `dark` o `light`. |
| `redirection_link` | URL que se carga en el WebView principal al tocar la entrada. |
| `sf_symbol` | Nombre del icono de la biblioteca [SF Symbols](https://developer.apple.com/sf-symbols/) de Apple (p. ej., `house`, `cart`, `wrench.and.screwdriver`). |
| `name` | Etiqueta de la entrada de la barra lateral. |

## Comportamiento

- Un botón flotante abre y cierra la barra lateral sobre su contenido web.
- Al tocar una entrada se carga la URL asociada en el WebView principal, de modo que su aplicación web nunca abandona el contenedor de la app.
- La barra lateral puede combinarse con el [pie de navegación nativo](navigation-footer.md) o usarse de forma independiente.

---

## Seguir leyendo

- ← Anterior: [Pie de navegación nativo](navigation-footer.md)
- Siguiente →: [Detección de captura de pantalla](screen-capture.md)
- Idiomas: [🇺🇸 English](../../ios/sidebar.md) · [🇩🇪 Deutsch](../../de/ios/sidebar.md) · [🇫🇷 Français](../../fr/ios/sidebar.md) · **🇪🇸 Español** · [🇨🇳 中文](../../zh/ios/sidebar.md)

> [!TIP]
> **¿Sin tiempo? Configuramos su app por usted.** Nuestro equipo configura, compila & publica su app WebViewGold: llave en mano, entrega rápida, Made in Germany. [Configurar mi app →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **Compile en su navegador:** Sin Mac ni IDE: el **WebViewGold Cloud Builder** configura, compila & sube su app en línea. [Descubra Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
