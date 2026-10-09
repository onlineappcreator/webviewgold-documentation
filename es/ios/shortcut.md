---
title: "API Shortcut – Documentación de WebViewGold para iOS"
description: "Añada accesos directos de acción rápida en la pantalla de inicio de su app iOS que dirijan con deep link a páginas concretas."
lang: "es"
product: "WebViewGold para iOS"
platform: "iOS"
category: "API y funciones"
slug: "shortcut"
canonical_url: "https://www.webviewgold.com/es/docs/iOS/shortcut/"
keywords:
  - "API Shortcut"
  - "WebViewGold para iOS"
  - "convertir sitio web en app"
  - "documentación de app WebView"
  - "SDK WebView de iOS"
  - "PWA a app"
  - "HTML a app"
  - "puente de JavaScript"
last_updated: "2026-10-09"
---

# API Shortcut – WebViewGold para iOS

> **Resumen:** Añada accesos directos de acción rápida en la pantalla de inicio de su app iOS que dirijan con deep link a páginas concretas.

[Documentación](../README.md) › [WebViewGold para iOS](README.md) › API Shortcut

**Plataforma:** iOS · **Categoría:** API y funciones · **Versión en línea:** [www.webviewgold.com/es/docs/iOS/shortcut/](https://www.webviewgold.com/es/docs/iOS/shortcut/)

---

Habilite `var useShortcuts = true` en `Config.swift` para registrar accesos directos dinámicos definidos en `Shortcuts.json`. Cada acceso directo puede abrir una URL, inyectar JavaScript y mostrar un SF Symbol. Ejemplo:

```json
{
    "shortcuts": [
        {
            "title": "Open Google",
            "redirection_link": "https://google.com",
            "injection": "",
            "symbol": "wrench.and.screwdriver"
        },
        {
            "title": "Open & Inject",
            "redirection_link": "https://apple.com",
            "injection": "(function() { console.log('Injected and executed!'); })();",
            "symbol": "lock.open"
        }
    ]
}
```

Los usuarios pueden acceder a los accesos directos manteniendo pulsado el icono de la aplicación.

---

## Seguir leyendo

- ← Anterior: [API de respuesta háptica](haptic-feedback.md)
- Siguiente →: [API de Portapapeles](clipboard.md)
- Idiomas: [🇺🇸 English](../../ios/shortcut.md) · [🇩🇪 Deutsch](../../de/ios/shortcut.md) · [🇫🇷 Français](../../fr/ios/shortcut.md) · **🇪🇸 Español** · [🇨🇳 中文](../../zh/ios/shortcut.md)

> [!TIP]
> **¿Sin tiempo? Configuramos su app por usted.** Nuestro equipo configura, compila & publica su app WebViewGold: llave en mano, entrega rápida, Made in Germany. [Configurar mi app →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **Compile en su navegador:** Sin Mac ni IDE: el **WebViewGold Cloud Builder** configura, compila & sube su app en línea. [Descubra Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
