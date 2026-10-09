---
title: "Biometric Authentication API – Documentación de WebViewGold para Android"
description: "Prompt fingerprint or face authentication with the native Android BiometricPrompt directly from your web app."
lang: "es"
product: "WebViewGold para Android"
platform: "Android"
category: "API y funciones"
slug: "biometric-auth"
canonical_url: "https://www.webviewgold.com/es/docs/android/biometric-auth/"
keywords:
  - "Biometric Auth API"
  - "WebViewGold para Android"
  - "convertir sitio web en app"
  - "documentación de app WebView"
  - "SDK WebView de Android"
  - "PWA a app"
  - "HTML a app"
  - "puente de JavaScript"
last_updated: "2026-10-09"
---

# Biometric Authentication API – WebViewGold para Android

> **Resumen:** Prompt fingerprint or face authentication with the native Android BiometricPrompt directly from your web app.

[Documentación](../README.md) › [WebViewGold para Android](README.md) › Biometric Auth API

**Plataforma:** Android · **Categoría:** API y funciones · **Versión en línea:** [www.webviewgold.com/es/docs/android/biometric-auth/](https://www.webviewgold.com/es/docs/android/biometric-auth/)

---

La **API de autenticación biométrica** solicita al usuario que se autentique mediante huella dactilar o rostro utilizando el `BiometricPrompt` nativo del dispositivo. Si el sistema operativo está configurado de esa manera, recurre al PIN o al patrón del dispositivo.

## Cómo utilizarla

Active el cuadro de diálogo del sistema desde un enlace HTML o desde JavaScript:

```html
<a href="bioauth://">Unlock</a>
```

```javascript
window.location.href = "bioauth://";
```

## Casos de uso típicos

- Restringir el acceso a una página de «cartera», «configuración» o «pedidos» dentro de su aplicación web.
- Exigir una nueva autenticación antes de un paso sensible del proceso de compra.

## Comportamiento

- El cuadro de diálogo del sistema lo dibuja la app; su aplicación web no necesita renderizar ninguna interfaz.
- Tras una autenticación correcta, la app se reanuda con normalidad para que su aplicación web pueda reaccionar (por ejemplo, navegando a la página protegida).
- En algunos dispositivos sin biometría, el sistema operativo puede mostrar un aviso de PIN en su lugar.

## Configuración relacionada

`enableBioMetricAuth` en **Config.java** activa el flujo integrado de **bloqueo de la app**, que requiere autenticación biométrica en cada inicio de la aplicación. `bioauth://` es independiente de este indicador y puede activarse en cualquier momento desde JavaScript.

---

## Seguir leyendo

- ← Anterior: [Read/Write Value API](read-write-value.md)
- Siguiente →: [Document Scanner](document-scanner.md)
- La misma función en otras plataformas: [iOS – API de autenticación biométrica](../ios/biometric-authentication.md)
- Idiomas: [🇺🇸 English](../../android/biometric-auth.md) · [🇩🇪 Deutsch](../../de/android/biometric-auth.md) · [🇫🇷 Français](../../fr/android/biometric-auth.md) · **🇪🇸 Español** · [🇨🇳 中文](../../zh/android/biometric-auth.md)

> [!TIP]
> **¿Sin tiempo? Configuramos su app por usted.** Nuestro equipo configura, compila & publica su app WebViewGold: llave en mano, entrega rápida, Made in Germany. [Configurar mi app →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_android_doc_online)
>
> **Compile en su navegador:** Sin Mac ni IDE: el **WebViewGold Cloud Builder** configura, compila & sube su app en línea. [Descubra Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=android_docs)
