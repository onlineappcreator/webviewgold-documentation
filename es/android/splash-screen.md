---
title: "Pantalla de bienvenida – Documentación de WebViewGold para Android"
description: "Personalice la pantalla de inicio de su aplicación Android WebView con sus propios gráficos."
lang: "es"
product: "WebViewGold para Android"
platform: "Android"
category: "Diseño de la app"
slug: "splash-screen"
canonical_url: "https://www.webviewgold.com/es/docs/android/splash-screen/"
keywords:
  - "Pantalla de bienvenida"
  - "WebViewGold para Android"
  - "convertir sitio web en app"
  - "documentación de app WebView"
  - "SDK WebView de Android"
  - "PWA a app"
  - "HTML a app"
  - "puente de JavaScript"
last_updated: "2026-10-09"
---

# Pantalla de bienvenida – WebViewGold para Android

> **Resumen:** Personalice la pantalla de inicio de su aplicación Android WebView con sus propios gráficos.

[Documentación](../README.md) › [WebViewGold para Android](README.md) › Pantalla de bienvenida

**Plataforma:** Android · **Categoría:** Diseño de la app · **Versión en línea:** [www.webviewgold.com/es/docs/android/splash-screen/](https://www.webviewgold.com/es/docs/android/splash-screen/)

---

Personalice el comportamiento de la pantalla de presentación configurando las siguientes variables en`Config.java`:

| Opción | Tipo | Descripción |
| --- | --- | --- |
| SPLASH_SCREEN_ACTIVATED | **true** o **false** | Establezca en *true* para activar la pantalla de bienvenida |
| SPLASH_TIMEOUT | número (milisegundos) | Retraso antes de mostrar el indicador de carga si la URL de inicio aún se está cargando |
| REMAIN_SPLASH_OPTION | **true** o **false** | Cuando*true*, mantiene la pantalla de presentación visible hasta que la URL de inicio se haya cargado por completo (anula`SPLASH_TIMEOUT`) |
| SPLASH_MIN_TIME | número (milisegundos) | Duración mínima de visualización cuando`REMAIN_SPLASH_OPTION`es*true*; ignorado si el tiempo de carga real excede este valor |
| SPLASH_FADE_OUT | número (milisegundos) | Duración de la animación que desaparece después de todos los temporizadores; establezca en *0* para desactivar el efecto de desvanecimiento |
| SCALE_SPLASH_IMAGE | porcentaje [0–100] | Escale la imagen de presentación en relación con la dimensión más pequeña del dispositivo;*0*oculta la imagen |

## Reemplazo de la imagen de la pantalla de bienvenida

- Reemplace `splash.gif` en sus assets por su propio GIF cuadrado (por ejemplo, 128×128, 512×512 o 1024×1024 px)
- Asegúrese de que las dimensiones de la imagen sean iguales (ancho = alto) para una visualización óptima
- Establezca el color de fondo en `colors.xml`

Los pasos para agregar una pantalla de presentación personalizada a su aplicación de Android se muestran en el siguiente video:

[![Ver el vídeo: Pantalla de bienvenida](https://img.youtube.com/vi/x684JHvW8lI/hqdefault.jpg)](https://www.youtube.com/watch?v=x684JHvW8lI)

---

## Seguir leyendo

- ← Anterior: [Icono de la app](app-icon.md)
- Siguiente →: [Navigation Drawer & Footer](navigation-drawer.md)
- La misma función en otras plataformas: [iOS – Nombre, icono y splash](../ios/app-name-icon-splash.md) · [macOS – Pantalla de inicio](../macos/splash-screen.md)
- Idiomas: [🇺🇸 English](../../android/splash-screen.md) · [🇩🇪 Deutsch](../../de/android/splash-screen.md) · [🇫🇷 Français](../../fr/android/splash-screen.md) · **🇪🇸 Español** · [🇨🇳 中文](../../zh/android/splash-screen.md)

> [!TIP]
> **¿Sin tiempo? Configuramos su app por usted.** Nuestro equipo configura, compila & publica su app WebViewGold: llave en mano, entrega rápida, Made in Germany. [Configurar mi app →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_android_doc_online)
>
> **Compile en su navegador:** Sin Mac ni IDE: el **WebViewGold Cloud Builder** configura, compila & sube su app en línea. [Descubra Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=android_docs)
