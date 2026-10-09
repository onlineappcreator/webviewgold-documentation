---
title: "API Pull-to-Refresh – Documentación de WebViewGold para iOS"
description: "Active el gesto nativo de deslizar para actualizar en su app WebView de iOS, personalice sus colores y actívelo o desactívelo dinámicamente desde su app web."
lang: "es"
product: "WebViewGold para iOS"
platform: "iOS"
category: "API y funciones"
slug: "pull-to-refresh"
canonical_url: "https://www.webviewgold.com/es/docs/iOS/pull-to-refresh/"
keywords:
  - "API Pull-to-Refresh"
  - "WebViewGold para iOS"
  - "convertir sitio web en app"
  - "documentación de app WebView"
  - "SDK WebView de iOS"
  - "PWA a app"
  - "HTML a app"
  - "puente de JavaScript"
last_updated: "2026-10-09"
---

# API Pull-to-Refresh – WebViewGold para iOS

> **Resumen:** Active el gesto nativo de deslizar para actualizar en su app WebView de iOS, personalice sus colores y actívelo o desactívelo dinámicamente desde su app web.

[Documentación](../README.md) › [WebViewGold para iOS](README.md) › API Pull-to-Refresh

**Plataforma:** iOS · **Categoría:** API y funciones · **Versión en línea:** [www.webviewgold.com/es/docs/iOS/pull-to-refresh/](https://www.webviewgold.com/es/docs/iOS/pull-to-refresh/)

---

La **API Pull-to-Refresh** añade el gesto nativo de iOS «deslizar para actualizar» a su app WebView: los usuarios arrastran la página hacia abajo para recargar la URL actual, igual que en apps nativas como Mail o Safari.

## Cómo activarlo

Abra **Config.swift** y establezca:

```swift
var pulltorefresh = true
var preventoverscroll = false
```

- `pulltorefresh` activa el control de actualización nativo.
- `preventoverscroll` debe estar en `false`: el gesto necesita la animación de rebote (overscroll) del WebView para funcionar.

## Personalizar los colores

Puede dar estilo al indicador de carga y a su fondo por separado para el modo claro y el modo oscuro en **Config.swift**:

```swift
var pulltorefresh_loadingsigncolour_lightmode = #colorLiteral(...)
var pulltorefresh_backgroundcolour_lightmode = #colorLiteral(...)
var pulltorefresh_loadingsigncolour_darkmode = #colorLiteral(...)
var pulltorefresh_backgroundcolour_darkmode = #colorLiteral(...)
```

Consejo: haga clic en la muestra de color junto a cada `#colorLiteral` en Xcode para elegir un color visualmente. Las variantes del modo oscuro requieren iOS 13 o superior.

## Alternar dinámicamente desde su app web

Puede activar o desactivar el pull-to-refresh en tiempo de ejecución, por ejemplo, para desactivarlo en páginas con sus propios gestos de deslizamiento (mapas, sliders, juegos):

```html
<a href="enablepulltorefresh://">Activar pull-to-refresh</a>
<a href="disablepulltorefresh://">Desactivar pull-to-refresh</a>
```

O mediante JavaScript:

```javascript
window.location.href = "disablepulltorefresh://";
```

Ambos comandos también se admiten dentro de una solicitud [MultiAPICall](multi-api-call.md).

## Conviene saber

- El control de actualización recarga la URL que se muestra actualmente en el WebView.
- Si utiliza la [API Dynamic UI](dynamic-ui.md) para cambiar el color de la barra inferior en tiempo de ejecución, los colores del pull-to-refresh se ajustan automáticamente para coincidir.

---

## Seguir leyendo

- ← Anterior: [API de indicador de carga](loading-sign.md)
- Siguiente →: [API de gestión de URL](url-handling.md)
- Idiomas: [🇺🇸 English](../../ios/pull-to-refresh.md) · [🇩🇪 Deutsch](../../de/ios/pull-to-refresh.md) · [🇫🇷 Français](../../fr/ios/pull-to-refresh.md) · **🇪🇸 Español** · [🇨🇳 中文](../../zh/ios/pull-to-refresh.md)

> [!TIP]
> **¿Sin tiempo? Configuramos su app por usted.** Nuestro equipo configura, compila & publica su app WebViewGold: llave en mano, entrega rápida, Made in Germany. [Configurar mi app →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **Compile en su navegador:** Sin Mac ni IDE: el **WebViewGold Cloud Builder** configura, compila & sube su app en línea. [Descubra Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
