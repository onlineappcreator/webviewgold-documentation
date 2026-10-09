---
title: "API de pases de Apple Wallet – Documentación de WebViewGold para iOS"
description: "Permita que los usuarios añadan pases .pkpass (entradas, cupones, tarjetas de socio) desde su aplicación web a Apple Wallet."
lang: "es"
product: "WebViewGold para iOS"
platform: "iOS"
category: "API y funciones"
slug: "wallet-pass"
canonical_url: "https://www.webviewgold.com/es/docs/iOS/wallet-pass/"
keywords:
  - "API de pases de Apple Wallet"
  - "WebViewGold para iOS"
  - "convertir sitio web en app"
  - "documentación de app WebView"
  - "SDK WebView de iOS"
  - "PWA a app"
  - "HTML a app"
  - "puente de JavaScript"
last_updated: "2026-10-09"
---

# API de pases de Apple Wallet – WebViewGold para iOS

> **Resumen:** Permita que los usuarios añadan pases .pkpass (entradas, cupones, tarjetas de socio) desde su aplicación web a Apple Wallet.

[Documentación](../README.md) › [WebViewGold para iOS](README.md) › API de pases de Apple Wallet

**Plataforma:** iOS · **Categoría:** API y funciones · **Versión en línea:** [www.webviewgold.com/es/docs/iOS/wallet-pass/](https://www.webviewgold.com/es/docs/iOS/wallet-pass/)

---

La **API de pases de Apple Wallet** permite que su aplicación web entregue al usuario un archivo `.pkpass` (entrada de evento, tarjeta de embarque, cupón, tarjeta de fidelidad o de socio) para que pueda añadirlo a **Apple Wallet**.

## Cómo usarla

Enlace su archivo `.pkpass`, pero sustituya el prefijo `https://` de la URL del archivo por `addpkpass://`:

```html
<a href="addpkpass://example.com/passes/ticket.pkpass">Añadir entrada a Apple Wallet</a>
```

## Cómo funciona

1. La aplicación vuelve a convertir el enlace `addpkpass://` en una URL `https://`.
2. La URL del pase se abre en una pestaña del navegador integrado, que reconoce el contenido `.pkpass` y muestra la vista previa nativa **Añadir a Apple Wallet**.
3. El usuario confirma y el pase se guarda en la aplicación Wallet.

**Notas:** El pase debe servirse mediante HTTPS con el tipo MIME correcto `application/vnd.apple.pkpass` y estar firmado con un certificado válido de Apple Pass Type ID (consulte la [documentación de Apple Wallet Passes](https://developer.apple.com/documentation/walletpasses) para saber cómo generar pases).

---

## Seguir leyendo

- ← Anterior: [API de calendario iCal](ical-calendar.md)
- Siguiente →: [API UUID](uuid.md)
- Idiomas: [🇺🇸 English](../../ios/wallet-pass.md) · [🇩🇪 Deutsch](../../de/ios/wallet-pass.md) · [🇫🇷 Français](../../fr/ios/wallet-pass.md) · **🇪🇸 Español** · [🇨🇳 中文](../../zh/ios/wallet-pass.md)

> [!TIP]
> **¿Sin tiempo? Configuramos su app por usted.** Nuestro equipo configura, compila & publica su app WebViewGold: llave en mano, entrega rápida, Made in Germany. [Configurar mi app →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **Compile en su navegador:** Sin Mac ni IDE: el **WebViewGold Cloud Builder** configura, compila & sube su app en línea. [Descubra Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
