---
title: "API de contactos – Documentación de WebViewGold para Android"
description: "Acceda a la agenda del dispositivo desde su aplicación web: lea los contactos con el permiso del usuario en WebViewGold para Android."
lang: "es"
product: "WebViewGold para Android"
platform: "Android"
category: "API y funciones"
slug: "contacts"
canonical_url: "https://www.webviewgold.com/es/docs/android/contacts/"
keywords:
  - "API de contactos"
  - "WebViewGold para Android"
  - "convertir sitio web en app"
  - "documentación de app WebView"
  - "SDK WebView de Android"
  - "PWA a app"
  - "HTML a app"
  - "puente de JavaScript"
last_updated: "2026-10-09"
---

# API de contactos – WebViewGold para Android

> **Resumen:** Acceda a la agenda del dispositivo desde su aplicación web: lea los contactos con el permiso del usuario en WebViewGold para Android.

[Documentación](../README.md) › [WebViewGold para Android](README.md) › API de contactos

**Plataforma:** Android · **Categoría:** API y funciones · **Versión en línea:** [www.webviewgold.com/es/docs/android/contacts/](https://www.webviewgold.com/es/docs/android/contacts/)

---

WebViewGold permite exportar los contactos a una variable JavaScript, en el formato que se muestra a continuación, mediante la API **readcontacts://**. El objeto JSON se almacena en la variable `contacts`. Para poder acceder a ella, su app debe obtener primero el permiso a través de la API **requestcontactpermission://**, que solicitará a su usuario que active los permisos de contactos. Sin completar este paso, **readcontacts://** rellenará la variable `contacts` con un valor null.\
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

Para añadir esta funcionalidad de contactos, es necesario añadir el permiso `android.permission.READ_CONTACTS` al archivo *AndroidManifest.xml* para que los usuarios puedan concederlo.

---

## Seguir leyendo

- ← Anterior: [API de comprobación de versión](app-version-check.md)
- Siguiente →: [API de interfaz dinámica](dynamic-ui.md)
- La misma función en otras plataformas: [iOS – API de Contactos](../ios/contacts.md)
- Idiomas: [🇺🇸 English](../../android/contacts.md) · [🇩🇪 Deutsch](../../de/android/contacts.md) · [🇫🇷 Français](../../fr/android/contacts.md) · **🇪🇸 Español** · [🇨🇳 中文](../../zh/android/contacts.md)

> [!TIP]
> **¿Sin tiempo? Configuramos su app por usted.** Nuestro equipo configura, compila & publica su app WebViewGold: llave en mano, entrega rápida, Made in Germany. [Configurar mi app →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_android_doc_online)
>
> **Compile en su navegador:** Sin Mac ni IDE: el **WebViewGold Cloud Builder** configura, compila & sube su app en línea. [Descubra Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=android_docs)
