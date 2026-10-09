---
title: "Plugin NFC – Documentación de WebViewGold para Android"
description: "Lea etiquetas NFC de forma nativa en su aplicación Android WebView y transfiera los datos de la etiqueta a su aplicación web."
lang: "es"
product: "WebViewGold para Android"
platform: "Android"
category: "API y funciones"
slug: "nfc"
canonical_url: "https://www.webviewgold.com/es/docs/android/nfc/"
keywords:
  - "Plugin NFC"
  - "WebViewGold para Android"
  - "convertir sitio web en app"
  - "documentación de app WebView"
  - "SDK WebView de Android"
  - "PWA a app"
  - "HTML a app"
  - "puente de JavaScript"
last_updated: "2026-10-09"
---

# Plugin NFC – WebViewGold para Android

> **Resumen:** Lea etiquetas NFC de forma nativa en su aplicación Android WebView y transfiera los datos de la etiqueta a su aplicación web.

[Documentación](../README.md) › [WebViewGold para Android](README.md) › Plugin NFC

**Plataforma:** Android · **Categoría:** API y funciones · **Versión en línea:** [www.webviewgold.com/es/docs/android/nfc/](https://www.webviewgold.com/es/docs/android/nfc/)

---

La **comunicación de campo cercano (NFC)** permite que dos dispositivos o un dispositivo y una etiqueta NFC se comuniquen de forma inalámbrica cuando están muy cerca. NFC se usa ampliamente en dispositivos Android para leer y escribir pequeñas cantidades de datos, lo que la convierte en una herramienta eficaz para compartir información a través de tarjetas o etiquetas habilitadas para NFC.

La **API NFC de WebViewGold** permite a su web app leer y escribir etiquetas NFC directamente a través de un puente JavaScript — desde compartir información de contacto hasta incorporar fragmentos de texto.

**Escritura**\
Para escribir un valor en una etiqueta NFC, envíe un comando desde su web app cargando la siguiente URL: `writenfc://?value=data`\
Ejemplo:\
`<a href="writenfc://?value=WebViewGold.com"> Escribir en una etiqueta NFC </a>`\
Esto pone su aplicación en modo de escritura y guarda el valor hasta que se escanee una etiqueta: en cuanto el usuario acerca una etiqueta NFC al dispositivo, el valor se escribe en ella.

**Escribir una VCARD (tarjeta de contacto)**\
Use la misma API que para escribir texto plano y formatee el texto así:

```
VCARD
FN:John Doe
Title:Developer
TEL;TYPE=CELL:0452641211
```

Separe las propiedades con un guion bajo (`_`), codifique los espacios como `%20` y anteponga `VCARD_` al texto. Ejemplo:

```
writenfc://?value=VCARD_FN:John%20Doe_Title:Developer_TEL;TYPE=CELL:0452641211
```

Consulte <https://en.wikipedia.org/wiki/VCard#Properties> para ver la lista de propiedades compatibles.

**Lectura**\
Para leer una etiqueta NFC, cargue `readnfc://`. Esto pone su aplicación en modo de lectura. Cuando el usuario escanea una etiqueta, la aplicación devuelve la información almacenada a su web app llamando a la función JavaScript `readNFCResult(data)`, donde `data` es el valor guardado en la etiqueta. Defina esta función JavaScript en su web app para procesar el valor:

```html
<script>
window.location.href = "readnfc://";

function readNFCResult(data) {
    alert("Contenido de la etiqueta NFC: " + data);
}
</script>
```

## Cómo probar la API

1. Abra el archivo Config del código de su aplicación.
2. Introduzca su código de compra.
3. Establezca la URL de la aplicación en la página de prueba de la API NFC: <https://webviewgoldtest.github.io/NFCtesting.html>
4. Ejecute la aplicación en un dispositivo físico con soporte NFC.
5. Pulse una de las opciones de lectura o escritura para activar el modo correspondiente. Si va a escribir, introduzca un valor.
6. Acerque la etiqueta NFC al dispositivo para completar la operación de lectura o escritura. La página de prueba y la aplicación mostrarán los resultados.

**¿Necesita más?** Si necesita funcionalidad NFC ampliada más allá de esta API (p. ej., tipos de etiquetas especiales o formatos de datos personalizados), ofrecemos integraciones personalizadas de plugin NFC de forma individual. Envíenos sus requisitos por correo electrónico a [webviewgold-nfc@onlineappcreator.com](mailto:webviewgold-nfc@onlineappcreator.com) para una consulta gratuita y un presupuesto sin compromiso.

---

## Seguir leyendo

- ← Anterior: [API de respuesta háptica](haptic-feedback.md)
- Siguiente →: [Open App Settings API](open-app-settings.md)
- La misma función en otras plataformas: [iOS – Plugin NFC](../ios/nfc.md)
- Idiomas: [🇺🇸 English](../../android/nfc.md) · [🇩🇪 Deutsch](../../de/android/nfc.md) · [🇫🇷 Français](../../fr/android/nfc.md) · **🇪🇸 Español** · [🇨🇳 中文](../../zh/android/nfc.md)

> [!TIP]
> **¿Sin tiempo? Configuramos su app por usted.** Nuestro equipo configura, compila & publica su app WebViewGold: llave en mano, entrega rápida, Made in Germany. [Configurar mi app →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_android_doc_online)
>
> **Compile en su navegador:** Sin Mac ni IDE: el **WebViewGold Cloud Builder** configura, compila & sube su app en línea. [Descubra Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=android_docs)
