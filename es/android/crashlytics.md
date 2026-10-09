---
title: "Firebase Crashlytics – Documentación de WebViewGold para Android"
description: "Ship crash reports and non-fatal events to your Firebase project, with runtime opt-in / opt-out from your web app."
lang: "es"
product: "WebViewGold para Android"
platform: "Android"
category: "Compilar y publicar"
slug: "crashlytics"
canonical_url: "https://www.webviewgold.com/es/docs/android/crashlytics/"
keywords:
  - "Firebase Crashlytics"
  - "WebViewGold para Android"
  - "convertir sitio web en app"
  - "documentación de app WebView"
  - "SDK WebView de Android"
  - "PWA a app"
  - "HTML a app"
  - "puente de JavaScript"
last_updated: "2026-10-09"
---

# Firebase Crashlytics – WebViewGold para Android

> **Resumen:** Ship crash reports and non-fatal events to your Firebase project, with runtime opt-in / opt-out from your web app.

[Documentación](../README.md) › [WebViewGold para Android](README.md) › Firebase Crashlytics

**Plataforma:** Android · **Categoría:** Compilar y publicar · **Versión en línea:** [www.webviewgold.com/es/docs/android/crashlytics/](https://www.webviewgold.com/es/docs/android/crashlytics/)

---

La integración de **Firebase Crashlytics** envía informes de fallos anónimos y eventos no fatales a su proyecto de Firebase, para que pueda detectar problemas de estabilidad en producción.

## Cómo activarla

1. Configure Firebase para su app y coloque `google-services.json` en `AndroidStudioSourceCode/app/`.
2. En **Config.java**, active el seguimiento:

   ```java
   public static final boolean TRACKING_EVENT = true;
   ```

`TRACKING_EVENT = false` desactiva todas las funciones relacionadas con el seguimiento, incluido el registro de eventos de Crashlytics y los activadores `starttracking://` / `endtracking://`.

## Aceptación/rechazo en tiempo de ejecución desde su aplicación web

WebViewGold respeta un indicador de seguimiento por usuario que se conserva en el dispositivo. Utilice los activadores de seguimiento estándar para cambiarlo en tiempo de ejecución:

```html
<a href="starttracking://">Enable analytics & crash reports</a>
<a href="endtracking://">Disable analytics & crash reports</a>
```

Cuando el usuario ha optado por no participar, la recopilación de Crashlytics se desactiva: no se sube nada.

## Qué se informa

- Fallos no controlados (rastros de pila, modelo del dispositivo, versión del sistema operativo).
- Excepciones no fatales registradas internamente por el envoltorio de la app.
- De forma predeterminada, no se adjuntan datos personales del usuario.

**Dónde ver los informes:** Abra el panel de **Firebase Console → Crashlytics**. Los informes suelen aparecer a los pocos minutos de un fallo.

**Notas:** La inicialización de Crashlytics es de mejor esfuerzo: si Firebase está mal configurado, la app sigue funcionando con normalidad. Considere añadir una pantalla de consentimiento (GDPR / CCPA) antes de llamar a `starttracking://` por primera vez.

---

## Seguir leyendo

- ← Anterior: [Health Connect API](health-connect.md)
- Siguiente →: [Compilar y publicar](publish.md)
- Idiomas: [🇺🇸 English](../../android/crashlytics.md) · [🇩🇪 Deutsch](../../de/android/crashlytics.md) · [🇫🇷 Français](../../fr/android/crashlytics.md) · **🇪🇸 Español** · [🇨🇳 中文](../../zh/android/crashlytics.md)

> [!TIP]
> **¿Sin tiempo? Configuramos su app por usted.** Nuestro equipo configura, compila & publica su app WebViewGold: llave en mano, entrega rápida, Made in Germany. [Configurar mi app →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_android_doc_online)
>
> **Compile en su navegador:** Sin Mac ni IDE: el **WebViewGold Cloud Builder** configura, compila & sube su app en línea. [Descubra Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=android_docs)
