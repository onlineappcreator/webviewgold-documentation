---
title: "Configurar su aplicación web o sitio web – Documentación de WebViewGold para iOS"
description: "Prepare su sitio web, PWA o archivos HTML locales para su app iOS: utilice una URL remota, incluya archivos sin conexión en la app o combine ambos con un respaldo sin conexión."
lang: "es"
product: "WebViewGold para iOS"
platform: "iOS"
category: "Primeros pasos"
slug: "setup-website"
canonical_url: "https://www.webviewgold.com/es/docs/iOS/setup-website/"
keywords:
  - "Configurar la aplicación web"
  - "WebViewGold para iOS"
  - "convertir sitio web en app"
  - "documentación de app WebView"
  - "SDK WebView de iOS"
  - "PWA a app"
  - "HTML a app"
  - "puente de JavaScript"
last_updated: "2026-10-09"
---

# Configurar su aplicación web o sitio web – WebViewGold para iOS

> **Resumen:** Prepare su sitio web, PWA o archivos HTML locales para su app iOS: utilice una URL remota, incluya archivos sin conexión en la app o combine ambos con un respaldo sin conexión.

[Documentación](../README.md) › [WebViewGold para iOS](README.md) › Configurar la aplicación web

**Plataforma:** iOS · **Categoría:** Primeros pasos · **Versión en línea:** [www.webviewgold.com/es/docs/iOS/setup-website/](https://www.webviewgold.com/es/docs/iOS/setup-website/)

---

## Opción A) Usar una URL para acceder a su aplicación web (= almacenar los archivos en línea)

Cree un sitio web o una aplicación web optimizados para móviles y súbalos a su servidor web/espacio web. WebViewGold para iOS es compatible con HTML clásico, PHP, WordPress, aplicaciones web progresivas, juegos HTML5, Wix, apprat.io, Bubble, jQuery Mobile y modernos creadores de IA/no-code como Lovable, Base44 y Bolt. En un flujo de trabajo típico, usted crea la interfaz de usuario del producto en jQuery, Lovable, Base44, Bolt, React, Vue, Angular o su stack preferido, y luego utiliza WebViewGold como el contenedor nativo de aplicación iOS que añade el empaquetado para la App Store, notificaciones push, API de dispositivo, gestión de URL y otras capacidades nativas.

Para obtener los mejores resultados en la revisión de la App Store, diseñe su experiencia web para que resulte intencionada en iPhone y iPad: diseños responsivos, objetivos táctiles grandes, primer renderizado rápido, estados de carga/vacío/error claros y una navegación similar a la de una aplicación. De forma predeterminada, WebViewGold para iOS permite tanto contenido HTTPS como contenido HTTP. Para un perfil de seguridad más apto para producción, restrinja el tráfico a HTTPS [modificando el ajuste de seguridad de transporte de iOS](https://www.webviewgold.com/support-center/knowledgebase/how-to-prevent-non-https-connections-in-webviewgold-for-ios-removing-nsallowsarbitraryloadsinwebcontent-from-info-plist/) y considere la opción `blockfaultyandselfsignedhttpscerts`. Considere realizar una revisión profesional de experiencia de usuario/UX en [UXreviewer.io](https://www.uxreviewer.io) o servicios similares para mejorar la preparación de cara a la aprobación en la tienda y la retención de usuarios a largo plazo.

## Opción B) Usar una carpeta HTML local para acceder a su aplicación web (= almacenar los archivos dentro de la aplicación)

WebViewGold también admite aplicaciones web basadas en carpetas HTML locales: establezca **uselocalhtmlfolder** en **true** (consulte el [siguiente paso](setup.md)) y copie sus archivos HTML/CSS/JavaScript (incluidos los subdirectorios) en la carpeta "local-www" de su proyecto de Xcode. Para ello, asegúrese de:

1. Eliminar los archivos predeterminados de la carpeta "local-www" seleccionándolos en la jerarquía de archivos de Xcode, luego haga clic derecho para pulsar "Delete" y después pulse "Move to Trash".
2. Seleccionar todos los archivos de su sitio web local y arrastrarlos y soltarlos en la jerarquía de archivos de Xcode, dentro de la carpeta "local-www". Asegúrese de que la opción "Create folder references" esté marcada y pulse "Finish".

Considere realizar una revisión profesional de experiencia de usuario/UX en [UXreviewer.io](https://www.uxreviewer.io) o servicios similares para obtener los mejores resultados de aprobación en la App Store. Este tipo de revisión de UX también le ayuda a lograr una mejor retención de clientes en general para su producto, con sugerencias de mejora.

## Opción C) Usar una carpeta HTML si el usuario está sin conexión y usar una URL remota si el usuario está en línea (= almacenar los archivos en línea + almacenar archivos de copia de seguridad/respaldo dentro de la aplicación)

Copie sus archivos HTML/CSS/JavaScript (incluidos los subdirectorios) en la carpeta "local-www" de su proyecto de Xcode. Para ello, asegúrese de:

1. Eliminar los archivos predeterminados de la carpeta "local-www" seleccionándolos en la jerarquía de archivos de Xcode, luego haga clic derecho para pulsar "Delete" y después pulse "Move to Trash".
2. Seleccionar todos los archivos de su sitio web local y arrastrarlos y soltarlos en la jerarquía de archivos de Xcode, dentro de la carpeta "local-www". Asegúrese de que la opción "Create folder references" esté marcada y pulse "Finish".

Establezca **uselocalhtmlfolder** en **false** (consulte el [siguiente paso](setup.md)) y establezca **offlinelocalhtmlswitch** en **true** (consulte el [siguiente paso](setup.md)). Considere realizar una revisión profesional de experiencia de usuario/UX en [UXreviewer.io](https://www.uxreviewer.io) o servicios similares para obtener los mejores resultados de aprobación en la App Store. Este tipo de revisión de UX también le ayuda a lograr una mejor retención de clientes en general para su producto, con sugerencias de mejora.

---

## Seguir leyendo

- ← Volver a: [Resumen](README.md)
- Siguiente →: [Configurar WebViewGold](setup.md)
- La misma función en otras plataformas: [Android – Configurar la aplicación web](../android/setup-website.md) · [macOS – Configuración de su aplicación web](../macos/setup-website.md)
- Idiomas: [🇺🇸 English](../../ios/setup-website.md) · [🇩🇪 Deutsch](../../de/ios/setup-website.md) · [🇫🇷 Français](../../fr/ios/setup-website.md) · **🇪🇸 Español** · [🇨🇳 中文](../../zh/ios/setup-website.md)

> [!TIP]
> **¿Sin tiempo? Configuramos su app por usted.** Nuestro equipo configura, compila & publica su app WebViewGold: llave en mano, entrega rápida, Made in Germany. [Configurar mi app →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **Compile en su navegador:** Sin Mac ni IDE: el **WebViewGold Cloud Builder** configura, compila & sube su app en línea. [Descubra Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
