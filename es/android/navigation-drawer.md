---
title: "Navigation Drawer & Bottom Navigation Footer – Documentación de WebViewGold para Android"
description: "Ship an app-like navigation experience with the built-in Material navigation drawer and Material 3 bottom navigation bar — no changes to your website required."
lang: "es"
product: "WebViewGold para Android"
platform: "Android"
category: "Diseño de la app"
slug: "navigation-drawer"
canonical_url: "https://www.webviewgold.com/es/docs/android/navigation-drawer/"
keywords:
  - "Navigation Drawer & Footer"
  - "WebViewGold para Android"
  - "convertir sitio web en app"
  - "documentación de app WebView"
  - "SDK WebView de Android"
  - "PWA a app"
  - "HTML a app"
  - "puente de JavaScript"
last_updated: "2026-10-09"
---

# Navigation Drawer & Bottom Navigation Footer – WebViewGold para Android

> **Resumen:** Ship an app-like navigation experience with the built-in Material navigation drawer and Material 3 bottom navigation bar — no changes to your website required.

[Documentación](../README.md) › [WebViewGold para Android](README.md) › Navigation Drawer & Footer

**Plataforma:** Android · **Categoría:** Diseño de la app · **Versión en línea:** [www.webviewgold.com/es/docs/android/navigation-drawer/](https://www.webviewgold.com/es/docs/android/navigation-drawer/)

---

WebViewGold incluye dos interfaces de navegación nativas integradas para que pueda ofrecer una experiencia de navegación tipo app sin tocar su sitio web: un **panel de navegación** lateral y un **pie de navegación inferior** Material 3. Ambas son opcionales y pueden combinarse o utilizarse de forma independiente.

## 1. Panel de navegación lateral

Un botón de menú flotante abre un panel de navegación Material con sus enlaces. Actívelo en **Config.java**:

```java
static boolean ENABLE_NAVIGATION_DRAWER = true;
```

Configure las entradas y los iconos en:

```
app/src/main/res/menu/menu_drawer.xml
```

Cada `<item>` se convierte en una fila del panel y, al tocarla, dirige el WebView a la URL que le asocie.

## 2. Pie de navegación inferior

Una barra de navegación inferior Material 3 se sitúa en la parte inferior de la pantalla y permite alternar entre las secciones principales. Actívela en **Config.java**:

```java
static boolean ENABLE_NAVIGATION_FOOTER = true;
```

El mismo archivo (`res/menu/menu_drawer.xml`) gestiona las entradas: elija de 3 a 5 destinos de nivel superior.

## Comportamiento

- Ambas interfaces respetan automáticamente el modo oscuro o claro del dispositivo.
- Los iconos y las etiquetas provienen de su XML de menú.
- Al tocar una entrada se carga la URL asociada en el WebView principal, por lo que su aplicación web nunca abandona el envoltorio de la app.

**Referencia:** [Directrices de la barra de navegación de Material 3](https://m3.material.io/components/navigation-bar/overview).

---

## Seguir leyendo

- ← Anterior: [Pantalla de bienvenida](splash-screen.md)
- Siguiente →: [API de gestión de URL](url-handling.md)
- La misma función en otras plataformas: [iOS – Pie de navegación nativo](../ios/navigation-footer.md)
- Idiomas: [🇺🇸 English](../../android/navigation-drawer.md) · [🇩🇪 Deutsch](../../de/android/navigation-drawer.md) · [🇫🇷 Français](../../fr/android/navigation-drawer.md) · **🇪🇸 Español** · [🇨🇳 中文](../../zh/android/navigation-drawer.md)

> [!TIP]
> **¿Sin tiempo? Configuramos su app por usted.** Nuestro equipo configura, compila & publica su app WebViewGold: llave en mano, entrega rápida, Made in Germany. [Configurar mi app →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_android_doc_online)
>
> **Compile en su navegador:** Sin Mac ni IDE: el **WebViewGold Cloud Builder** configura, compila & sube su app en línea. [Descubra Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=android_docs)
