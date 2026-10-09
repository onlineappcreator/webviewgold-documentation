---
title: "Plugin HealthKit – Documentación de WebViewGold para iOS"
description: "Conecte su aplicación web con Apple HealthKit y lea los datos de salud con el permiso del usuario en iOS."
lang: "es"
product: "WebViewGold para iOS"
platform: "iOS"
category: "Extensiones y plugins"
slug: "healthkit"
canonical_url: "https://www.webviewgold.com/es/docs/iOS/healthkit/"
keywords:
  - "Plugin HealthKit"
  - "WebViewGold para iOS"
  - "convertir sitio web en app"
  - "documentación de app WebView"
  - "SDK WebView de iOS"
  - "PWA a app"
  - "HTML a app"
  - "puente de JavaScript"
last_updated: "2026-10-09"
---

# Plugin HealthKit – WebViewGold para iOS

> **Resumen:** Conecte su aplicación web con Apple HealthKit y lea los datos de salud con el permiso del usuario en iOS.

[Documentación](../README.md) › [WebViewGold para iOS](README.md) › Plugin HealthKit

**Plataforma:** iOS · **Categoría:** Extensiones y plugins · **Versión en línea:** [www.webviewgold.com/es/docs/iOS/healthkit/](https://www.webviewgold.com/es/docs/iOS/healthkit/)

---

Active las funciones de HealthKit configurando `static let HealthKitEnabled` en `Config.swift` con su token de plugin y añadiendo la capacidad de HealthKit.\
Contacte con [webviewgold-healthkit@onlineappcreator.com](mailto:webviewgold-healthkit@onlineappcreator.com) para más información.

## Uso de la API (una vez activada)

**Lea** un valor de HealthKit llamando a `readhealthkit://` seguido de un [identificador de HealthKit](https://developer.apple.com/documentation/healthkit/hkquantitytypeidentifier). El resultado se inyecta en su aplicación web como una variable de JavaScript con el nombre del identificador (con el valor y la unidad como cadena):

```html
<a href="readhealthkit://HKQuantityTypeIdentifierStepCount" onclick="setTimeout(function(){ alert(HKQuantityTypeIdentifierStepCount); }, 500)">Leer recuento de pasos</a>
```

**Escriba** un valor de HealthKit con la sintaxis `writehealthkit://Identificador//Valor`:

```html
<a href="writehealthkit://HKQuantityTypeIdentifierStepCount//100">Guardar 100 pasos</a>
```

**Nota:** Requiere la capacidad de HealthKit y las entradas *Privacy - Health Share Usage Description* / *Privacy - Health Update Usage Description* en **Info.plist**.

---

## Seguir leyendo

- ← Anterior: [Plugin Siri](siri.md)
- Siguiente →: [Compilar y publicar](publish.md)
- La misma función en otras plataformas: [Android – Health Connect API](../android/health-connect.md)
- Idiomas: [🇺🇸 English](../../ios/healthkit.md) · [🇩🇪 Deutsch](../../de/ios/healthkit.md) · [🇫🇷 Français](../../fr/ios/healthkit.md) · **🇪🇸 Español** · [🇨🇳 中文](../../zh/ios/healthkit.md)

> [!TIP]
> **¿Sin tiempo? Configuramos su app por usted.** Nuestro equipo configura, compila & publica su app WebViewGold: llave en mano, entrega rápida, Made in Germany. [Configurar mi app →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **Compile en su navegador:** Sin Mac ni IDE: el **WebViewGold Cloud Builder** configura, compila & sube su app en línea. [Descubra Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
