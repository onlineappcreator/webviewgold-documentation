---
title: "Asistente de inicio de sesión social (Google, Facebook & Apple) – Documentación de WebViewGold para iOS"
description: "Haga que los inicios de sesión OAuth de Google, Facebook y Apple funcionen de forma fiable en su app WebView de iOS con los asistentes de inicio de sesión integrados."
lang: "es"
product: "WebViewGold para iOS"
platform: "iOS"
category: "API y funciones"
slug: "social-login"
canonical_url: "https://www.webviewgold.com/es/docs/iOS/social-login/"
keywords:
  - "Social Login Helper"
  - "WebViewGold para iOS"
  - "convertir sitio web en app"
  - "documentación de app WebView"
  - "SDK WebView de iOS"
  - "PWA a app"
  - "HTML a app"
  - "puente de JavaScript"
last_updated: "2026-10-09"
---

# Asistente de inicio de sesión social (Google, Facebook & Apple) – WebViewGold para iOS

> **Resumen:** Haga que los inicios de sesión OAuth de Google, Facebook y Apple funcionen de forma fiable en su app WebView de iOS con los asistentes de inicio de sesión integrados.

[Documentación](../README.md) › [WebViewGold para iOS](README.md) › Social Login Helper

**Plataforma:** iOS · **Categoría:** API y funciones · **Versión en línea:** [www.webviewgold.com/es/docs/iOS/social-login/](https://www.webviewgold.com/es/docs/iOS/social-login/)

---

Google, Facebook y otros proveedores de OAuth restringen los inicios de sesión desde WebViews integrados (p. ej., el error *«disallowed_useragent»* de Google). El **Social Login Helper** integrado en WebViewGold hace que estos inicios de sesión funcionen de forma fiable dentro de su app de iOS, sin cambiar el flujo de inicio de sesión de su sitio web.

## Cómo funciona

Usted define prefijos de URL que aparecen durante el flujo de inicio de sesión de su app web. En cuanto se carga una de estas URL desencadenantes, WebViewGold abre el inicio de sesión en una ventana emergente de inicio de sesión dedicada con un user agent ajustado que el proveedor de OAuth acepta. Tras un inicio de sesión correcto, el flujo vuelve automáticamente a su app web. «Sign in with Apple» (`appleid.apple.com`) se detecta y gestiona automáticamente, sin configuración alguna.

## Configuración

Abra **Config.swift** y defina los prefijos de URL desencadenantes de su flujo de inicio de sesión:

```javascript
var google_login_helper_triggers: [String] = ["https://accounts.google.com", "https://accounts.youtube.com"]
var facebook_login_helper_triggers: [String] = ["https://m.facebook.com", "https://www.facebook.com"]
```

- `google_login_helper_triggers`: prefijos de URL que se cargan durante un inicio de sesión con Google en su sitio web.
- `facebook_login_helper_triggers`: prefijos de URL que se cargan durante un inicio de sesión con Facebook en su sitio web.

Para encontrar las URL desencadenantes correctas, inicie el flujo de inicio de sesión de su sitio web en un navegador de escritorio y anote por qué URL pasa la redirección de OAuth.

## Abrir una URL de autenticación en el navegador externo

Como alternativa, puede entregar explícitamente una URL de inicio de sesión al navegador del sistema (la sesión vive entonces en el navegador, no en la app):

```javascript
window.location.href = "googlelogin://" + encodeURIComponent("https://accounts.google.com/o/oauth2/v2/auth?...");
```

WebViewGold decodifica la URL tras el prefijo `googlelogin://` y la abre externamente.

## Cuándo usar el helper

Pruebe primero las opciones más sencillas; en muchos casos ya resuelven los problemas de inicio de sesión:

- Abra el dominio de inicio de sesión en una pestaña de navegador in-app o en el navegador externo mediante la [API URL Handling](url-handling.md) (p. ej., `specialLinkHandlingOptions`, `safariblacklist`).
- Establezca un [user agent personalizado](setup.md) (`useragent_iphone` / `useragent_ipad`).

Si el inicio de sesión sigue fallando dentro de la app, los desencadenantes del Social Login Helper son la solución recomendada.

---

## Seguir leyendo

- ← Anterior: [API de gestión de URL](url-handling.md)
- Siguiente →: [API de reconexión](reconnect.md)
- Idiomas: [🇺🇸 English](../../ios/social-login.md) · [🇩🇪 Deutsch](../../de/ios/social-login.md) · [🇫🇷 Français](../../fr/ios/social-login.md) · **🇪🇸 Español** · [🇨🇳 中文](../../zh/ios/social-login.md)

> [!TIP]
> **¿Sin tiempo? Configuramos su app por usted.** Nuestro equipo configura, compila & publica su app WebViewGold: llave en mano, entrega rápida, Made in Germany. [Configurar mi app →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **Compile en su navegador:** Sin Mac ni IDE: el **WebViewGold Cloud Builder** configura, compila & sube su app en línea. [Descubra Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
