---
title: "Modificar el tamaño de la Safe Area – Documentación de WebViewGold para iOS"
description: "Ajuste la safe area y active la barra inferior personalizada para que su aplicación web se vea perfecta en los iPhone con barra de inicio."
lang: "es"
product: "WebViewGold para iOS"
platform: "iOS"
category: "Diseño de la app"
slug: "safe-area"
canonical_url: "https://www.webviewgold.com/es/docs/iOS/safe-area/"
keywords:
  - "Modificar la Safe Area"
  - "WebViewGold para iOS"
  - "convertir sitio web en app"
  - "documentación de app WebView"
  - "SDK WebView de iOS"
  - "PWA a app"
  - "HTML a app"
  - "puente de JavaScript"
last_updated: "2026-10-09"
---

# Modificar el tamaño de la Safe Area – WebViewGold para iOS

> **Resumen:** Ajuste la safe area y active la barra inferior personalizada para que su aplicación web se vea perfecta en los iPhone con barra de inicio.

[Documentación](../README.md) › [WebViewGold para iOS](README.md) › Modificar la Safe Area

**Plataforma:** iOS · **Categoría:** Diseño de la app · **Versión en línea:** [www.webviewgold.com/es/docs/iOS/safe-area/](https://www.webviewgold.com/es/docs/iOS/safe-area/)

---

El salto del iPhone 8 al iPhone X y modelos posteriores cambió mucho la interfaz de usuario en el sector móvil al eliminar el botón de inicio e introducir la barra de inicio. Según el diseño de su aplicación web, la barra de menú inferior puede quedar mal posicionada en los dispositivos (solapándose con el contenido) que tienen la barra de inicio, debido al cambio en el área segura predeterminada.\
La buena noticia es que WebViewGold cuenta con una función que le permite activar una **bottombar** y elegir su color para que coincida con el tema de su aplicación. Dado que el problema de que la barra de inicio se solape con el contenido de la aplicación puede no aparecer en los iPad (debido a la pantalla más grande y a un posible diseño diferente), también existe una opción para deshabilitar la función en los iPad.\
Para implementar esta función, utilice las siguientes variables en **Config.swift** bajo el encabezado "Custom Bottom Bar Design". Asegúrese de establecer **bottombar** en **true**.\
![Variables de configuración de la función de barra inferior](../../assets/ios/img/bottombar_config.webp)\
**Avanzado:** En lugar de usar la función bottombar, puede buscar esta parte del fragmento de código *(pulse **CMD+F** y luego introduzca "*`switch UIDevice.current.userInterfaceIdiom`*")* en el archivo **WebViewController.swift**, donde puede cambiar el valor del borde 20 por cualquier valor que desee, como 10, 30, etc., como se muestra a continuación:\
![Redimensionar el área segura en aplicaciones WebView para iPhone X/XS/XS Max](../../assets/ios/img/edgeinsets.webp)

---

## Seguir leyendo

- ← Anterior: [Nombre, icono y splash](app-name-icon-splash.md)
- Siguiente →: [API de geolocalización](geolocation.md)
- Idiomas: [🇺🇸 English](../../ios/safe-area.md) · [🇩🇪 Deutsch](../../de/ios/safe-area.md) · [🇫🇷 Français](../../fr/ios/safe-area.md) · **🇪🇸 Español** · [🇨🇳 中文](../../zh/ios/safe-area.md)

> [!TIP]
> **¿Sin tiempo? Configuramos su app por usted.** Nuestro equipo configura, compila & publica su app WebViewGold: llave en mano, entrega rápida, Made in Germany. [Configurar mi app →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **Compile en su navegador:** Sin Mac ni IDE: el **WebViewGold Cloud Builder** configura, compila & sube su app en línea. [Descubra Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
