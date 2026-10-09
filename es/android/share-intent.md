---
title: "API ShareIntent – Documentación de WebViewGold para Android"
description: "Reciba el contenido compartido desde otras aplicaciones de Android directamente en su aplicación WebView mediante Share Intents."
lang: "es"
product: "WebViewGold para Android"
platform: "Android"
category: "API y funciones"
slug: "share-intent"
canonical_url: "https://www.webviewgold.com/es/docs/android/share-intent/"
keywords:
  - "API ShareIntent"
  - "WebViewGold para Android"
  - "convertir sitio web en app"
  - "documentación de app WebView"
  - "SDK WebView de Android"
  - "PWA a app"
  - "HTML a app"
  - "puente de JavaScript"
last_updated: "2026-10-09"
---

# API ShareIntent – WebViewGold para Android

> **Resumen:** Reciba el contenido compartido desde otras aplicaciones de Android directamente en su aplicación WebView mediante Share Intents.

[Documentación](../README.md) › [WebViewGold para Android](README.md) › API ShareIntent

**Plataforma:** Android · **Categoría:** API y funciones · **Versión en línea:** [www.webviewgold.com/es/docs/android/share-intent/](https://www.webviewgold.com/es/docs/android/share-intent/)

---

La **API ShareIntent** de WebViewGold permite que su aplicación aparezca como destino en el cuadro de diálogo Compartir nativo de Android. Esto permite a los usuarios compartir contenido como texto, URL o imágenes (como cadenas base64) desde cualquier otra aplicación directamente en su aplicación basada en WebView.

## Casos de uso

- Compartir enlaces a perfiles de usuario, notas o artículos directamente en su aplicación
- Recibir contenido de aplicaciones de mensajería o navegador
- Envío de imágenes desde la galería a su interfaz WebView (codificada en base64)

## Paso 1: Habilite el soporte para compartir en AndroidManifest.xml

Para permitir que su aplicación reciba datos compartidos, descomente los filtros de intención relevantes en su archivo **AndroidManifest.xml**:

```html
<!-- Receive shared text (e.g., URLs or notes) -->
<intent-filter>
    <action android:name="android.intent.action.SEND" />
    <category android:name="android.intent.category.DEFAULT" />
    <data android:mimeType="text/plain" />
</intent-filter>

<!-- Receive a single shared image -->
<intent-filter>
    <action android:name="android.intent.action.SEND" />
    <category android:name="android.intent.category.DEFAULT" />
    <data android:mimeType="image/*" />
</intent-filter>

<!-- Receive multiple shared images -->
<intent-filter>
    <action android:name="android.intent.action.SEND_MULTIPLE" />
    <category android:name="android.intent.category.DEFAULT" />
    <data android:mimeType="image/*" />
</intent-filter>
```

Una vez que estos filtros estén activos, el icono de su aplicación basada en WebViewGold aparecerá como un objetivo para compartir cada vez que los usuarios compartan contenido de otra aplicación.

## Paso 2: Maneje los datos compartidos en su WebView

Cuando un usuario comparte contenido en su aplicación, WebViewGold inyectará automáticamente el contenido compartido en una variable de JavaScript llamada`sharedData`.

```html
<script>
    alert(sharedData); // Displays the shared content (text or base64 image)

</script>
```

- **Texto o URL:**Se pasará como texto sin formato a`sharedData`
- **Imagen:**Se convertirá en una cadena codificada en base64 y se pasará a`sharedData`

**Uso de ejemplo:**Complete automáticamente un formulario o obtenga una vista previa de una imagen según el contenido recibido:

```html
<script>
    if (sharedData) {
        document.getElementById("myInput").value = sharedData;
    }
</script>
```

**Nota:**Asegúrese de que su JavaScript esté listo para manejar texto sin formato y cadenas largas en base64. También puede implementar comprobaciones del lado del cliente para distinguir entre diferentes tipos de contenido.

---

## Seguir leyendo

- ← Anterior: [App Links / Deep Linking](app-links.md)
- Siguiente →: [API de diálogo para compartir](app-sharing-dialog.md)
- La misma función en otras plataformas: [iOS – Share Extension](../ios/share-extension.md)
- Idiomas: [🇺🇸 English](../../android/share-intent.md) · [🇩🇪 Deutsch](../../de/android/share-intent.md) · [🇫🇷 Français](../../fr/android/share-intent.md) · **🇪🇸 Español** · [🇨🇳 中文](../../zh/android/share-intent.md)

> [!TIP]
> **¿Sin tiempo? Configuramos su app por usted.** Nuestro equipo configura, compila & publica su app WebViewGold: llave en mano, entrega rápida, Made in Germany. [Configurar mi app →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_android_doc_online)
>
> **Compile en su navegador:** Sin Mac ni IDE: el **WebViewGold Cloud Builder** configura, compila & sube su app en línea. [Descubra Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=android_docs)
