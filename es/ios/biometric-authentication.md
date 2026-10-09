---
title: "API de autenticación biométrica (Face ID / Touch ID) – Documentación de WebViewGold para iOS"
description: "Proteja su app iOS con Face ID o Touch ID y verifique a los usuarios de forma biométrica desde su aplicación web."
lang: "es"
product: "WebViewGold para iOS"
platform: "iOS"
category: "API y funciones"
slug: "biometric-authentication"
canonical_url: "https://www.webviewgold.com/es/docs/iOS/biometric-authentication/"
keywords:
  - "API de autenticación biométrica"
  - "WebViewGold para iOS"
  - "convertir sitio web en app"
  - "documentación de app WebView"
  - "SDK WebView de iOS"
  - "PWA a app"
  - "HTML a app"
  - "puente de JavaScript"
last_updated: "2026-10-09"
---

# API de autenticación biométrica (Face ID / Touch ID) – WebViewGold para iOS

> **Resumen:** Proteja su app iOS con Face ID o Touch ID y verifique a los usuarios de forma biométrica desde su aplicación web.

[Documentación](../README.md) › [WebViewGold para iOS](README.md) › API de autenticación biométrica

**Plataforma:** iOS · **Categoría:** API y funciones · **Versión en línea:** [www.webviewgold.com/es/docs/iOS/biometric-authentication/](https://www.webviewgold.com/es/docs/iOS/biometric-authentication/)

---

**Esta es una alternativa independiente, más potente pero más complicada que nuestra sencilla opción *enableBioMetricAuth* basada en Config.swift.** Esta API le permite utilizar la autenticación biométrica en su aplicación y devolver el resultado a su sitio web mediante JavaScript. La autenticación biométrica incluye Face ID (en los diseños más recientes de iPhone) y Touch ID (en los diseños más antiguos), con código como alternativa. Al llamar al comando URL "bioauth://", puede activar la autenticación biométrica de forma nativa en su aplicación. Una vez completado el proceso, WebViewGold devolverá los resultados a su aplicación web llamando a una de las siguientes funciones:

- **onBioAuthSuccess()**
  - Se invoca cuando el proceso de autenticación se ha realizado correctamente.
- **onBioAuthFailure(errorCode, errorMessage)**
  - Se invoca cuando el proceso de autenticación falla y proporciona información sobre el error.
- **onBioAuthUnavailable()**
  - Se invoca cuando se detecta que la autenticación biométrica no está disponible en el dispositivo.

Para utilizar esta API, primero debe añadir la clave de privacidad para la autenticación biométrica con Face ID en su archivo **Info.plist**. Para ello, abra **Info.plist**, sitúe el cursor sobre una clave existente, haga clic en el símbolo (+) para añadir una nueva clave debajo de la seleccionada y elija la opción "**Privacy - Face ID Usage Description**". Sin esta clave, la aplicación no admitirá Face ID. El valor de esta clave es una descripción que se presenta al usuario la primera vez que su aplicación intenta usar Face ID. Esta descripción debe explicar claramente por qué su aplicación necesita usar Face ID. A continuación se muestra un ejemplo de descripción para esta clave:

![Ejemplo de la clave de privacidad de Face ID en Info.plist.](../../assets/ios/img/faceID_key.webp)\
A continuación, debe definir las siguientes funciones (en JavaScript) en su aplicación web para gestionar los resultados de una autenticación biométrica:

```html
<script>

function onBioAuthSuccess() {
    alert("Bio Authentication Succeeded");
}

function onBioAuthFailure(errorCode, errorMessage) {
    // errorCode = Int, errorMessage = String
    alert(`Bio Authentication Failed, ${errorMessage} (code ${errorCode})`);
}

function onBioAuthUnavailable() {
    alert("Bio Authentication Unavailable");
}

</script>
```

Después, cargue este tipo de URL para desencadenar el proceso de autenticación biométrica en su aplicación web:

```html
<script>

window.location.href = "bioauth://";

</script>
```

**Aviso de seguridad:** Debe tenerse en cuenta que usuarios malintencionados pueden lograr que la función onBioAuthSuccess() se invoque sin haber completado el proceso de autenticación. Dado que la autenticación es un proceso sensible, se recomienda añadir una capa adicional de seguridad en su aplicación web, como una comprobación de cookies o de geolocalización, para ayudar a garantizar la integridad de la autenticación. Consulte al experto en ciberseguridad de su sitio web para obtener orientación adaptada a las necesidades de su aplicación web.

---

## Seguir leyendo

- ← Anterior: [API de Contactos](contacts.md)
- Siguiente →: [API de respuesta háptica](haptic-feedback.md)
- La misma función en otras plataformas: [Android – Biometric Auth API](../android/biometric-auth.md)
- Idiomas: [🇺🇸 English](../../ios/biometric-authentication.md) · [🇩🇪 Deutsch](../../de/ios/biometric-authentication.md) · [🇫🇷 Français](../../fr/ios/biometric-authentication.md) · **🇪🇸 Español** · [🇨🇳 中文](../../zh/ios/biometric-authentication.md)

> [!TIP]
> **¿Sin tiempo? Configuramos su app por usted.** Nuestro equipo configura, compila & publica su app WebViewGold: llave en mano, entrega rápida, Made in Germany. [Configurar mi app →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **Compile en su navegador:** Sin Mac ni IDE: el **WebViewGold Cloud Builder** configura, compila & sube su app en línea. [Descubra Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
