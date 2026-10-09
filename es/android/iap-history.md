---
title: "In-App Purchase History API – Documentación de WebViewGold para Android"
description: "Return the user's Google Play purchase history as window.purchaseHistory so your web app can list subscriptions or unlock premium content client-side."
lang: "es"
product: "WebViewGold para Android"
platform: "Android"
category: "API y funciones"
slug: "iap-history"
canonical_url: "https://www.webviewgold.com/es/docs/android/iap-history/"
keywords:
  - "IAP History API"
  - "WebViewGold para Android"
  - "convertir sitio web en app"
  - "documentación de app WebView"
  - "SDK WebView de Android"
  - "PWA a app"
  - "HTML a app"
  - "puente de JavaScript"
last_updated: "2026-10-09"
---

# In-App Purchase History API – WebViewGold para Android

> **Resumen:** Return the user's Google Play purchase history as window.purchaseHistory so your web app can list subscriptions or unlock premium content client-side.

[Documentación](../README.md) › [WebViewGold para Android](README.md) › IAP History API

**Plataforma:** Android · **Categoría:** API y funciones · **Versión en línea:** [www.webviewgold.com/es/docs/android/iap-history/](https://www.webviewgold.com/es/docs/android/iap-history/)

---

La **API de historial de compras dentro de la app** devuelve la lista de compras anteriores del usuario (ID de producto, marcas de tiempo, tokens) realizadas a través de Google Play Billing y la inyecta en su aplicación web como `window.purchaseHistory`. Asegúrese de disponer de una [Licencia Extendida](credits.md) de WebViewGold si tiene previsto utilizar esta función en un producto final.

## Cómo utilizarla

```html
<a href="getpurchasehistory://" onclick="setTimeout(renderHistory, 300)">My purchases</a>

<script>
function renderHistory() {
  const data = window.purchaseHistory;
  if (!data) return;
  data.purchases.forEach(function (p) {
    console.log(p.productId, p.purchaseTime, p.orderId);
  });
}
</script>
```

## Formato de la carga útil

```json
{
  "purchases": [
    {
      "productId": "com.example.premium",
      "purchaseTime": 1721600000000,
      "orderId": "GPA.xxxx-xxxx-xxxx",
      "purchaseToken": "..."
    }
  ]
}
```

Los campos exactos dependen del registro de la tienda: trate el valor como un array JSON para iterar.

## Casos de uso típicos

- Mostrar una página «Mis suscripciones» o «Mis compras» dentro de su aplicación web.
- Desbloqueo del lado del cliente de contenido premium basado en compras anteriores sin consultar su backend.
- Flujos de trabajo de depuración y atención al cliente.

**Notas:** La lista contiene únicamente las compras realizadas con la cuenta de Google Play actualmente conectada en este dispositivo.

---

## Seguir leyendo

- ← Anterior: [API de compras integradas](in-app-purchases.md)
- Siguiente →: [API de escáner de QR](qr-code-scanner.md)
- La misma función en otras plataformas: [iOS – API del historial de compras](../ios/iap-history.md)
- Idiomas: [🇺🇸 English](../../android/iap-history.md) · [🇩🇪 Deutsch](../../de/android/iap-history.md) · [🇫🇷 Français](../../fr/android/iap-history.md) · **🇪🇸 Español** · [🇨🇳 中文](../../zh/android/iap-history.md)

> [!TIP]
> **¿Sin tiempo? Configuramos su app por usted.** Nuestro equipo configura, compila & publica su app WebViewGold: llave en mano, entrega rápida, Made in Germany. [Configurar mi app →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_android_doc_online)
>
> **Compile en su navegador:** Sin Mac ni IDE: el **WebViewGold Cloud Builder** configura, compila & sube su app en línea. [Descubra Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=android_docs)
