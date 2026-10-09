---
title: "Health Connect API – Documentación de WebViewGold para Android"
description: "Read and write Android Health Connect records from JavaScript — mirrors the WebViewGold HealthKit API on iOS so one web app covers both platforms."
lang: "es"
product: "WebViewGold para Android"
platform: "Android"
category: "API y funciones"
slug: "health-connect"
canonical_url: "https://www.webviewgold.com/es/docs/android/health-connect/"
keywords:
  - "Health Connect API"
  - "WebViewGold para Android"
  - "convertir sitio web en app"
  - "documentación de app WebView"
  - "SDK WebView de Android"
  - "PWA a app"
  - "HTML a app"
  - "puente de JavaScript"
last_updated: "2026-10-09"
---

# Health Connect API – WebViewGold para Android

> **Resumen:** Read and write Android Health Connect records from JavaScript — mirrors the WebViewGold HealthKit API on iOS so one web app covers both platforms.

[Documentación](../README.md) › [WebViewGold para Android](README.md) › Health Connect API

**Plataforma:** Android · **Categoría:** API y funciones · **Versión en línea:** [www.webviewgold.com/es/docs/android/health-connect/](https://www.webviewgold.com/es/docs/android/health-connect/)

---

La **API de Health Connect** lee y escribe registros de salud a través de [Android Health Connect](https://health.google/health-connect-android/). Refleja la funcionalidad de HealthKit de iOS de WebViewGold, para que pueda distribuir una única aplicación web que se comunique con los datos de salud en ambas plataformas. Las lecturas siempre devuelven **los totales de hoy** para el tipo de registro solicitado.

## Lectura de un registro

```html
<a href="readhealthkit://StepsRecord" onclick="setTimeout(show, 300)">
  My steps today
</a>

<script>
function show() {
  // Injected variable name matches the sanitized record name.
  alert(StepsRecord); // e.g. "8421.0 steps"
}
</script>
```

## Escritura de un registro

Formato: `writehealthkit://<RecordName>//<value>`

```html
<a href="writehealthkit://StepsRecord//1000">Log 1000 steps</a>
```

En caso de éxito, la app inyecta `<RecordName> = "WRITE_SUCCESS"`. En caso de fallo, inyecta el texto del error.

**Registros compatibles:** Cualquier tipo de registro de Health Connect para el que su app haya solicitado permiso. Los más comunes son:

- `StepsRecord`
- `HeartRateRecord`
- `WeightRecord`
- `SleepSessionRecord`
- `HydrationRecord`
- `ActiveCaloriesBurnedRecord`
- `DistanceRecord`

## Configuración

1. Instale **Health Connect** en el dispositivo (viene preinstalado en Android 14+).
2. En el primer uso, la app abre el cuadro de diálogo de permisos de Health Connect; el usuario concede permisos de lectura y/o escritura para los tipos de registro solicitados.
3. Si Health Connect no es compatible, el valor inyectado se establece en la cadena `"Health Connect not supported"`.

**Notas:** Los valores se devuelven como `"<número> <unidad>"` (por ejemplo, `"75.4 kg"`). Requiere Android 8.0 (API 26) o superior.

---

## Seguir leyendo

- ← Anterior: [Printer API](printer.md)
- Siguiente →: [Firebase Crashlytics](crashlytics.md)
- La misma función en otras plataformas: [iOS – Plugin HealthKit](../ios/healthkit.md)
- Idiomas: [🇺🇸 English](../../android/health-connect.md) · [🇩🇪 Deutsch](../../de/android/health-connect.md) · [🇫🇷 Français](../../fr/android/health-connect.md) · **🇪🇸 Español** · [🇨🇳 中文](../../zh/android/health-connect.md)

> [!TIP]
> **¿Sin tiempo? Configuramos su app por usted.** Nuestro equipo configura, compila & publica su app WebViewGold: llave en mano, entrega rápida, Made in Germany. [Configurar mi app →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_android_doc_online)
>
> **Compile en su navegador:** Sin Mac ni IDE: el **WebViewGold Cloud Builder** configura, compila & sube su app en línea. [Descubra Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=android_docs)
