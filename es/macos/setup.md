---
title: "Configuración de WebViewGold para aplicaciones de escritorio en macOS – WebViewGold para macOS Documentación"
description: "Instale Xcode, abra el proyecto de WebViewGold para macOS, introduzca su URL en index.html y configure config.json, o empaquete su propio contenido HTML local."
lang: "es"
product: "WebViewGold para macOS"
platform: "macOS"
category: "Primeros pasos"
slug: "setup"
canonical_url: "https://www.webviewgold.com/es/docs/mac/#setup"
keywords:
  - "Configuración de WebViewGold"
  - "WebViewGold para macOS"
  - "convertir sitio web en app"
  - "documentación de app WebView"
  - "SDK WebView de macOS"
  - "PWA a app"
  - "HTML a app"
  - "puente de JavaScript"
last_updated: "2026-10-09"
---

# Configuración de WebViewGold para aplicaciones de escritorio en macOS – WebViewGold para macOS

> **Resumen:** Instale Xcode, abra el proyecto de WebViewGold para macOS, introduzca su URL en index.html y configure config.json, o empaquete su propio contenido HTML local.

[Documentación](../README.md) › [WebViewGold para macOS](README.md) › Configuración de WebViewGold

**Plataforma:** macOS · **Categoría:** Primeros pasos · **Versión en línea:** [www.webviewgold.com/es/docs/mac/#setup](https://www.webviewgold.com/es/docs/mac/#setup)

---

Xcode es necesario para configurar aplicaciones utilizando WebViewGold para macOS. Xcode es un potente entorno de desarrollo integrado (IDE) que se utiliza para crear aplicaciones para dispositivos Apple como iPhones, iPads y Macs. Es importante tener en cuenta que Xcode es un programa grande y puede ocupar una cantidad significativa de espacio de almacenamiento en su Mac. Además, Xcode solo está disponible para Macs y no es compatible con Windows o Linux. A continuación se ofrece una guía paso a paso para descargar e instalar Xcode en su Mac:

- Haga clic aquí: [**Descargar Xcode en la Mac App Store**](https://apps.apple.com/us/app/xcode/id497799835)
- Haga clic en el botón «Obtener» o «Descargar» para iniciar el proceso de descarga.
- Una vez completada la descarga, el instalador de Xcode se iniciará automáticamente.
- Siga las instrucciones del instalador para completar el proceso de instalación.
- Cuando la instalación finalice, abra Xcode desde la carpeta Aplicaciones o desde la búsqueda de Spotlight.
- La primera vez que abra Xcode, es posible que se le pida instalar componentes adicionales o aceptar los términos y condiciones. Siga las indicaciones para completar el proceso de configuración.

En el siguiente paso, **[descargue WebViewGold para macOS](https://www.webviewgold.com/download/mac/)** para crear aplicaciones de escritorio de macOS. A continuación, abra el **archivo de proyecto de Xcode**:\
![Archivo principal del proyecto de Xcode](../../assets/macos/img/xcodefile.jpg)

Elija la **carpeta public** y configure el archivo **config.json**:\
![Archivo de configuración de WebViewGold para macOS](../../assets/macos/img/config1.png)

Abra el archivo **index.html** para editar la URL:\
![Inserte la URL de su aplicación web en el archivo index.html](../../assets/macos/img/config2.png)

Si desea utilizar **contenido HTML local** (en lugar de una URL remota), simplemente reemplace el archivo index.html por su propio contenido.

---

## Seguir leyendo

- ← Anterior: [Configuración de su aplicación web](setup-website.md)
- Siguiente →: [Icono de la aplicación](app-icon.md)
- La misma función en otras plataformas: [iOS – Configurar WebViewGold](../ios/setup.md) · [Android – Configurar WebViewGold](../android/setup.md)
- Idiomas: [🇺🇸 English](../../macos/setup.md) · [🇩🇪 Deutsch](../../de/macos/setup.md) · [🇫🇷 Français](../../fr/macos/setup.md) · **🇪🇸 Español** · [🇨🇳 中文](../../zh/macos/setup.md)

