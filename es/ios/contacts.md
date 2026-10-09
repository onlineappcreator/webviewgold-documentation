---
title: "API de Contactos – Documentación de WebViewGold para iOS"
description: "Acceda a la agenda del dispositivo desde su aplicación web: lea los contactos con el permiso del usuario en WebViewGold para iOS."
lang: "es"
product: "WebViewGold para iOS"
platform: "iOS"
category: "API y funciones"
slug: "contacts"
canonical_url: "https://www.webviewgold.com/es/docs/iOS/contacts/"
keywords:
  - "API de Contactos"
  - "WebViewGold para iOS"
  - "convertir sitio web en app"
  - "documentación de app WebView"
  - "SDK WebView de iOS"
  - "PWA a app"
  - "HTML a app"
  - "puente de JavaScript"
last_updated: "2026-10-09"
---

# API de Contactos – WebViewGold para iOS

> **Resumen:** Acceda a la agenda del dispositivo desde su aplicación web: lea los contactos con el permiso del usuario en WebViewGold para iOS.

[Documentación](../README.md) › [WebViewGold para iOS](README.md) › API de Contactos

**Plataforma:** iOS · **Categoría:** API y funciones · **Versión en línea:** [www.webviewgold.com/es/docs/iOS/contacts/](https://www.webviewgold.com/es/docs/iOS/contacts/)

---

WebViewGold permite exportar los contactos a una variable de JavaScript, con el formato que se muestra a continuación, mediante la API **readcontacts://**. El objeto JSON se almacena en la variable `contacts`. Para poder acceder a él, su aplicación debe primero obtener el permiso a través de la API **requestcontactpermission://**, que solicitará al usuario que habilite los permisos de contactos. Sin completar este paso, **readcontacts://** rellenará la variable `contacts` con un valor nulo.\
Ejemplo de salida almacenada en la variable JS `contacts`:

```json
 {
   "John Appleseed":[
      "888-555-5512",
      "888-555-1212"
   ],
   "Daniel Higgins":[
      "555-478-7672",
      "(408) 555-5270",
      "(408) 555-3514"
   ],
   "David Taylor":[
      "555-610-6679"
   ],
   "Hank Zakroff":[
      "(555) 766-4823",
      "(707) 555-1854"
   ]
}
```

---

## Seguir leyendo

- ← Anterior: [API de icono de app dinámico](dynamic-app-icon.md)
- Siguiente →: [API de autenticación biométrica](biometric-authentication.md)
- La misma función en otras plataformas: [Android – API de contactos](../android/contacts.md)
- Idiomas: [🇺🇸 English](../../ios/contacts.md) · [🇩🇪 Deutsch](../../de/ios/contacts.md) · [🇫🇷 Français](../../fr/ios/contacts.md) · **🇪🇸 Español** · [🇨🇳 中文](../../zh/ios/contacts.md)

> [!TIP]
> **¿Sin tiempo? Configuramos su app por usted.** Nuestro equipo configura, compila & publica su app WebViewGold: llave en mano, entrega rápida, Made in Germany. [Configurar mi app →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **Compile en su navegador:** Sin Mac ni IDE: el **WebViewGold Cloud Builder** configura, compila & sube su app en línea. [Descubra Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
