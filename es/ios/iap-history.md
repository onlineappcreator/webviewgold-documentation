---
title: "API del historial de compras In-App – Documentación de WebViewGold para iOS"
description: "Lea las compras In-App anteriores del usuario desde su aplicación web como JSON, perfecto para páginas de «Mis compras»."
lang: "es"
product: "WebViewGold para iOS"
platform: "iOS"
category: "API y funciones"
slug: "iap-history"
canonical_url: "https://www.webviewgold.com/es/docs/iOS/iap-history/"
keywords:
  - "API del historial de compras"
  - "WebViewGold para iOS"
  - "convertir sitio web en app"
  - "documentación de app WebView"
  - "SDK WebView de iOS"
  - "PWA a app"
  - "HTML a app"
  - "puente de JavaScript"
last_updated: "2026-10-09"
---

# API del historial de compras In-App – WebViewGold para iOS

> **Resumen:** Lea las compras In-App anteriores del usuario desde su aplicación web como JSON, perfecto para páginas de «Mis compras».

[Documentación](../README.md) › [WebViewGold para iOS](README.md) › API del historial de compras

**Plataforma:** iOS · **Categoría:** API y funciones · **Versión en línea:** [www.webviewgold.com/es/docs/iOS/iap-history/](https://www.webviewgold.com/es/docs/iOS/iap-history/)

---

La **API del historial de compras In-App** devuelve la lista de compras anteriores del usuario realizadas mediante la [API de compras In-App](in-app-purchases.md) en este dispositivo y la inyecta en su aplicación web como `window.purchaseHistory`. Asegúrese de poseer una [Extended License](credits.md) de WebViewGold si planea usar esta función en un producto final.

## Cómo usarla

```html
<a href="getpurchasehistory://" onclick="setTimeout(renderHistory, 300)">Mis compras</a>

<script>
function renderHistory() {
  const data = window.purchaseHistory;
  if (!data) return;
  data.purchases.forEach(function (p) {
    console.log(p.productId, p.transactionId, p.purchaseDateMs);
  });
}
</script>
```

## Formato de los datos

```json
{
  "purchases": [
    {
      "productId": "com.example.premium",
      "transactionId": "2000000123456789",
      "purchaseDateMs": "1721600000000"
    }
  ]
}
```

`purchaseDateMs` es la marca de tiempo de la compra en milisegundos Unix (como cadena).

## Casos de uso típicos

- Mostrar una página «Mis suscripciones» o «Mis compras» dentro de su aplicación web.
- Desbloquear contenido premium en el cliente basándose en compras anteriores sin consultar su backend.
- Flujos de depuración y de atención al cliente.

**Notas:** La lista contiene las compras realizadas dentro de la aplicación en este dispositivo. Se almacena localmente, por lo que no se sincroniza entre dispositivos; para comprobar derechos entre dispositivos, valide los recibos en su servidor.

---

## Seguir leyendo

- ← Anterior: [API de compras integradas](in-app-purchases.md)
- Siguiente →: [API de escáner de QR](qr-code-scanner.md)
- La misma función en otras plataformas: [Android – IAP History API](../android/iap-history.md)
- Idiomas: [🇺🇸 English](../../ios/iap-history.md) · [🇩🇪 Deutsch](../../de/ios/iap-history.md) · [🇫🇷 Français](../../fr/ios/iap-history.md) · **🇪🇸 Español** · [🇨🇳 中文](../../zh/ios/iap-history.md)

> [!TIP]
> **¿Sin tiempo? Configuramos su app por usted.** Nuestro equipo configura, compila & publica su app WebViewGold: llave en mano, entrega rápida, Made in Germany. [Configurar mi app →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **Compile en su navegador:** Sin Mac ni IDE: el **WebViewGold Cloud Builder** configura, compila & sube su app en línea. [Descubra Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
