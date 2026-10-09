---
title: "Configure su aplicación web o sitio web – Documentación de WebViewGold para Android"
description: "Prepare su sitio web, PWA o archivos HTML locales para su aplicación de Android: use una URL remota, incluya archivos sin conexión en la aplicación o combine ambos con un respaldo sin conexión."
lang: "es"
product: "WebViewGold para Android"
platform: "Android"
category: "Primeros pasos"
slug: "setup-website"
canonical_url: "https://www.webviewgold.com/es/docs/android/setup-website/"
keywords:
  - "Configurar la aplicación web"
  - "WebViewGold para Android"
  - "convertir sitio web en app"
  - "documentación de app WebView"
  - "SDK WebView de Android"
  - "PWA a app"
  - "HTML a app"
  - "puente de JavaScript"
last_updated: "2026-10-09"
---

# Configure su aplicación web o sitio web – WebViewGold para Android

> **Resumen:** Prepare su sitio web, PWA o archivos HTML locales para su aplicación de Android: use una URL remota, incluya archivos sin conexión en la aplicación o combine ambos con un respaldo sin conexión.

[Documentación](../README.md) › [WebViewGold para Android](README.md) › Configurar la aplicación web

**Plataforma:** Android · **Categoría:** Primeros pasos · **Versión en línea:** [www.webviewgold.com/es/docs/android/setup-website/](https://www.webviewgold.com/es/docs/android/setup-website/)

---

## Opción A) Utilice una URL para acceder a su aplicación web (=almacenar archivos en línea)

Cree un sitio web o una aplicación web optimizados para dispositivos móviles y cárguelos en su servidor web/espacio web. WebViewGold para Android admite HTML clásico, PHP, WordPress, aplicaciones web progresivas, juegos HTML5, Wix, apprat.io, Bubble, jQuery Mobile y creadores modernos de IA/sin código como Lovable, Base44 y Bolt. Un patrón de implementación común es crear la interfaz de usuario del producto en jQuery, Lovable, Base44, Bolt, React, Vue, Angular o su pila preferida, luego usar WebViewGold como shell de la aplicación nativa de Android que agrega paquetes de Google Play, notificaciones push, API de dispositivo, manejo de URL y otras capacidades nativas.

Para obtener los mejores resultados de revisión de Google Play, optimice el sitio web para que se comporte como una aplicación de Android pulida: puntos de interrupción receptivos, carga rápida, estados de error/sin conexión claros, objetivos de toque accesibles y comportamiento predecible del botón Atrás. De forma predeterminada, WebViewGold para Android permite contenido HTTPS y HTTP. Para obtener un perfil de seguridad de mayor nivel de producción, restrinja el tráfico a HTTPS mediante[desactivar el tráfico de texto sin cifrar](https://www.webviewgold.com/support-center/knowledgebase/how-to-prevent-non-https-connections-in-webviewgold-for-android-switching-usescleartexttraffic-from-true-to-false/)y considere el`BLOCK_SELF_SIGNED_AND_FAULTY_SSL_CERTS`opción. Considere una revisión profesional de experiencia de usuario/UX en[UXreviewer.io](https://www.uxreviewer.io)o servicios similares para mejorar la preparación para la aprobación y la retención a largo plazo.

## Opción B) Utilice una carpeta HTML local para acceder a su aplicación web (=almacenar archivos dentro de la aplicación)

WebViewGold también admite aplicaciones web basadas en carpetas HTML locales: copie sus archivos HTML/CSS/JavaScript al proyecto de Android Studio y configure**USE_LOCAL_HTML_FOLDER**a**true**(ver[siguiente paso](setup.md)). Considere una revisión profesional de experiencia de usuario/UX en[UXreviewer.io](https://www.uxreviewer.io)o servicios similares para obtener los mejores resultados de aprobación de Play Store. Una revisión de UX de este tipo también le ayuda a lograr una mejor retención de clientes en general para su producto con sugerencias de mejora.

[![Ver el vídeo: Configure su aplicación web o sitio web](https://img.youtube.com/vi/CtyyZrNVcek/hqdefault.jpg)](https://www.youtube.com/watch?v=CtyyZrNVcek)

## Opción C) Utilice una carpeta HTML si el usuario está desconectado y utilice una URL remota si el usuario está conectado (=almacenar archivos en línea + almacenar archivos de respaldo/alternativo dentro de la aplicación)

Copie sus archivos HTML/CSS/JavaScript al proyecto de Android Studio, configure**USE_LOCAL_HTML_FOLDER**a**false**(ver[siguiente paso](setup.md)) y establecer**FALLBACK_USE_LOCAL_HTML_FOLDER_IF_OFFLINE**a**true**(ver[siguiente paso](setup.md)). Considere una revisión profesional de experiencia de usuario/UX en[UXreviewer.io](https://www.uxreviewer.io)o servicios similares para obtener los mejores resultados de aprobación de Play Store. Una revisión de UX de este tipo también le ayuda a lograr una mejor retención de clientes en general para su producto con sugerencias de mejora.

[![Ver el vídeo: Configure su aplicación web o sitio web](https://img.youtube.com/vi/W0NrpCKB7aU/hqdefault.jpg)](https://www.youtube.com/watch?v=W0NrpCKB7aU)

---

## Seguir leyendo

- ← Volver a: [Resumen](README.md)
- Siguiente →: [Configurar WebViewGold](setup.md)
- La misma función en otras plataformas: [iOS – Configurar la aplicación web](../ios/setup-website.md) · [macOS – Configuración de su aplicación web](../macos/setup-website.md)
- Idiomas: [🇺🇸 English](../../android/setup-website.md) · [🇩🇪 Deutsch](../../de/android/setup-website.md) · [🇫🇷 Français](../../fr/android/setup-website.md) · **🇪🇸 Español** · [🇨🇳 中文](../../zh/android/setup-website.md)

> [!TIP]
> **¿Sin tiempo? Configuramos su app por usted.** Nuestro equipo configura, compila & publica su app WebViewGold: llave en mano, entrega rápida, Made in Germany. [Configurar mi app →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_android_doc_online)
>
> **Compile en su navegador:** Sin Mac ni IDE: el **WebViewGold Cloud Builder** configura, compila & sube su app en línea. [Descubra Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=android_docs)
