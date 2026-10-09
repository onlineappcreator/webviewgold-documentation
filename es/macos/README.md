---
title: "Documentación de WebViewGold para macOS – Convierta su sitio web en app de Mac"
description: "Documentación oficial de WebViewGold para macOS: convierta su sitio web, PWA, panel SaaS o proyecto HTML en una app de escritorio nativa para Mac con configuración de Xcode, opciones de configuración, API de JavaScript, guía de publicación y notas de implementación estilo SDK."
lang: "es"
product: "WebViewGold para macOS"
platform: "macOS"
canonical_url: "https://www.webviewgold.com/es/docs/mac/"
keywords:
  - "WebViewGold para macOS"
  - "convertir sitio web en app"
  - "documentación de app WebView"
  - "SDK WebView de macOS"
  - "PWA a app"
  - "HTML a app"
  - "puente de JavaScript"
last_updated: "2026-10-09"
---

# Documentación de WebViewGold para macOS

![WebViewGold para macOS](../../assets/macos/img/header.png)

> Documentación oficial de WebViewGold para macOS: convierta su sitio web, PWA, panel SaaS o proyecto HTML en una app de escritorio nativa para Mac con configuración de Xcode, opciones de configuración, API de JavaScript, guía de publicación y notas de implementación estilo SDK.

[Documentación](../README.md) › WebViewGold para macOS

Convierta su sitio web, PWA, panel SaaS, tienda de comercio electrónico o app web generada por IA en una app nativa de macOS en minutos. Use WebViewGold como un SDK de app ligero: configure su URL, habilite API nativas, integre comandos del puente de JavaScript y publique una app lista para la tienda sin reconstruir su producto web desde cero.

WebViewGold funciona con sitios HTML/PHP clásicos, WordPress, proyectos de jQuery Mobile y apps web modernas creadas con Lovable, Base44, Bolt, Bubble, React, Vue, Angular o constructores similares. La documentación siguiente explica el flujo de configuración, las API de funciones nativas, las consideraciones de seguridad y los pasos de publicación en un formato técnico centrado en la implementación.

**[Empezar la guía →](setup-website.md)** · [Descargar WebViewGold](https://www.webviewgold.com/download/mac/)

## Inicio rápido

1. **[Configure su app web](setup-website.md)** — Use una URL remota, empaquete archivos HTML locales o combine ambos con una alternativa sin conexión.
2. **[Configure WebViewGold](setup.md)** — Introduzca su URL y ajuste cada opción en un sencillo archivo de configuración, sin programar.

## Todos los temas, API & funciones

Todo lo que WebViewGold para macOS puede hacer: cada tema en su propia página:

### Primeros pasos

- **[Configuración de su aplicación web](setup-website.md)** — Prepare su sitio web, PWA o app web para WebViewGold para macOS: tecnologías compatibles (HTML, PHP, WordPress, PWA, Lovable, Base44, Bolt…) y consejos para una experiencia de escritorio nativa.
- **[Configuración de WebViewGold](setup.md)** — Instale Xcode, abra el proyecto de WebViewGold para macOS, introduzca su URL en index.html y configure config.json, o empaquete su propio contenido HTML local.

### Diseño de la app

- **[Icono de la aplicación](app-icon.md)** — Sustituya el icono de su app de escritorio WebViewGold para macOS por sus propios archivos de imagen redimensionados.
- **[Nombre de la aplicación](app-name.md)** — Cambie el nombre de su app de escritorio WebViewGold para macOS en Xcode.
- **[Texto de la pantalla sin conexión](offline-screen.md)** — Personalice el texto de la pantalla sin conexión de su app WebView para Mac editando OfflineOverlay.xib en Interface Builder.
- **[Diálogo de primer inicio](first-run-dialog.md)** — Edite el texto del diálogo de primer inicio de su app WebView para Mac en FirstRunWindow.xib (Interface Builder).
- **[Pantalla de inicio](splash-screen.md)** — Cambie el texto de la pantalla de inicio en SplashScreen.xib y su duración máxima en Preferences.m de WebViewGold para macOS.

### API y funciones

- **[API In-App Purchases](in-app-purchases.md)** — Venda compras integradas y suscripciones de la Mac App Store desde su app web: añada el ID de producto en Constants.h y active la compra con un enlace inapppurchase://.
- **[API UUID](uuid.md)** — Pase un ID de dispositivo único y no personal (UUID) a JavaScript mediante get-uuid:// para identificar dispositivos y restaurar ajustes.
- **[API Deeplinking](deep-linking.md)** — Abra su app WebViewGold para macOS mediante un esquema de URL personalizado y lleve al usuario a una página concreta: deeplinking explicado paso a paso.

### Más

- **[Créditos y licencias](credits.md)** — Información de licencia, marcas registradas y créditos de código abierto (MacGap, licencia MIT) de WebViewGold para macOS.
- **[Valorar WebViewGold](rate.md)** — ¿Le gusta WebViewGold para macOS? Valórelo en CodeCanyon en 10 segundos: así seguimos publicando actualizaciones.
- **[Continuar con iOS y Android](more-platforms.md)** — Reutilice su app web en móviles: obtenga WebViewGold para iOS y Android, además de photos2webgallery para macOS.
- **[Contáctenos](support.md)** — Obtenga ayuda con WebViewGold para macOS: consulte el Centro de soporte o contacte directamente con el equipo.

## Una app web, todas las plataformas

Reutilice el mismo sitio web para apps de iOS, Android & macOS con WebViewGold.

- [WebViewGold para iOS](../ios/README.md)
- [WebViewGold para Android](../android/README.md)

**Idiomas:** [🇺🇸 English](../../macos/README.md) · [🇩🇪 Deutsch](../../de/macos/README.md) · [🇫🇷 Français](../../fr/macos/README.md) · **🇪🇸 Español** · [🇨🇳 中文](../../zh/macos/README.md)

