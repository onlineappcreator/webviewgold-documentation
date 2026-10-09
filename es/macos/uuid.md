---
title: "API UUID – WebViewGold para macOS Documentación"
description: "Pase un ID de dispositivo único y no personal (UUID) a JavaScript mediante get-uuid:// para identificar dispositivos y restaurar ajustes."
lang: "es"
product: "WebViewGold para macOS"
platform: "macOS"
category: "API y funciones"
slug: "uuid"
canonical_url: "https://www.webviewgold.com/es/docs/mac/#uuid"
keywords:
  - "API UUID"
  - "WebViewGold para macOS"
  - "convertir sitio web en app"
  - "documentación de app WebView"
  - "SDK WebView de macOS"
  - "PWA a app"
  - "HTML a app"
  - "puente de JavaScript"
last_updated: "2026-10-09"
---

# API UUID – WebViewGold para macOS

> **Resumen:** Pase un ID de dispositivo único y no personal (UUID) a JavaScript mediante get-uuid:// para identificar dispositivos y restaurar ajustes.

[Documentación](../README.md) › [WebViewGold para macOS](README.md) › API UUID

**Plataforma:** macOS · **Categoría:** API y funciones · **Versión en línea:** [www.webviewgold.com/es/docs/mac/#uuid](https://www.webviewgold.com/es/docs/mac/#uuid)

---

WebViewGold permite pasar un **identificador de dispositivo único y no personal** (UUID / «Universally Unique Identifier») a JavaScript, que **puede utilizarse para identificar de forma única los dispositivos macOS**. Esta API puede resultar útil, por ejemplo, para guardar configuraciones o valores en el servidor y restaurarlos en el cliente. Respete la **normativa local e internacional en materia de privacidad** si utiliza esta API.

```html
<a href="get-uuid://">Get UDID</a>
<a href="#" onClick="alert(uuid);">Show UDID</a>
```

---

## Seguir leyendo

- ← Anterior: [API In-App Purchases](in-app-purchases.md)
- Siguiente →: [API Deeplinking](deep-linking.md)
- La misma función en otras plataformas: [iOS – API UUID](../ios/uuid.md) · [Android – API de UUID](../android/uuid.md)
- Idiomas: [🇺🇸 English](../../macos/uuid.md) · [🇩🇪 Deutsch](../../de/macos/uuid.md) · [🇫🇷 Français](../../fr/macos/uuid.md) · **🇪🇸 Español** · [🇨🇳 中文](../../zh/macos/uuid.md)

