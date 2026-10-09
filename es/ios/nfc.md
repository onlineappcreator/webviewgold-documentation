---
title: "Plugin NFC – Documentación de WebViewGold para iOS"
description: "Lea etiquetas NFC de forma nativa en su app WebView de iOS y transfiera los datos de la etiqueta a su aplicación web."
lang: "es"
product: "WebViewGold para iOS"
platform: "iOS"
category: "Extensiones y plugins"
slug: "nfc"
canonical_url: "https://www.webviewgold.com/es/docs/iOS/nfc/"
keywords:
  - "Plugin NFC"
  - "WebViewGold para iOS"
  - "convertir sitio web en app"
  - "documentación de app WebView"
  - "SDK WebView de iOS"
  - "PWA a app"
  - "HTML a app"
  - "puente de JavaScript"
last_updated: "2026-10-09"
---

# Plugin NFC – WebViewGold para iOS

> **Resumen:** Lea etiquetas NFC de forma nativa en su app WebView de iOS y transfiera los datos de la etiqueta a su aplicación web.

[Documentación](../README.md) › [WebViewGold para iOS](README.md) › Plugin NFC

**Plataforma:** iOS · **Categoría:** Extensiones y plugins · **Versión en línea:** [www.webviewgold.com/es/docs/iOS/nfc/](https://www.webviewgold.com/es/docs/iOS/nfc/)

---

La tecnología **Near-Field Communication (NFC)** es una de las tecnologías más recientes que se ha vuelto muy popular entre los usuarios de dispositivos móviles. Permite que dos dispositivos, o un dispositivo y una etiqueta NFC, se comuniquen de forma inalámbrica cuando están muy cerca. NFC se utiliza ampliamente en dispositivos iOS para leer y escribir pequeñas cantidades de datos, lo que la convierte en una herramienta eficaz para compartir información a través de tarjetas o etiquetas compatibles con NFC.

La API de NFC permite a los desarrolladores leer y escribir datos en etiquetas NFC directamente desde el código de la aplicación. Esto abre nuevas formas para que las aplicaciones interactúen con los usuarios, desde compartir información de contacto hasta incrustar fragmentos de texto.

## Integración del plugin NFC de WebViewGold

Aunque NFC no forma parte del conjunto general de funciones de WebViewGold, ofrecemos una integración personalizada y sencilla del plugin NFC de WebViewGold (mediante JavaScript) de forma individual.

Envíenos sus requisitos (por ejemplo, escribir/leer fragmentos de texto o detalles de tarjetas de contacto en/desde etiquetas NFC) mediante un correo electrónico a [webviewgold-nfc@onlineappcreator.com](mailto:webviewgold-nfc@onlineappcreator.com) para una consulta gratuita y un presupuesto sin compromiso.

**Escritura**\
Para escribir un valor en una etiqueta NFC, envíe un comando desde su aplicación web cargando la siguiente URL: `writenfc://?value=data`\
Ejemplo:\
`<a href="writenfc://?value=WebViewGold.com"> Write to an NFC tag </a>`\
Esto pone su aplicación en Modo de Escritura y almacena el valor hasta que se escanea una etiqueta.

**Escritura en una VCARD**\
Utilice la misma API que para escribir texto sin formato. Dé formato al texto de la siguiente manera:

```
VCARD
FN:John Doe
Title:Developer
TEL;TYPE=CELL:0452641211
_
_
_
```

Separe las propiedades con un guion bajo (`_`) y anteponga `VCARD_` al texto. Consulte <https://en.wikipedia.org/wiki/VCard#Properties> para ver una lista de las propiedades compatibles.

**Lectura**\
Para leer una etiqueta NFC, cargue `readnfc://`. La aplicación devolverá la información a su aplicación web llamando a `readNFCResult(data, id, tag)`, donde `data` es el valor almacenado, `id` el identificador de la etiqueta y `tag` el tipo de etiqueta. Defina esta función JavaScript en su aplicación web para gestionar los valores.

## Cómo probar la API

1. Abra el archivo Config de la base de código de su aplicación.
2. Introduzca su código de compra.
3. Establezca la URL de la aplicación en la página de prueba de la API de NFC: <https://webviewgoldtest.github.io/NFCtesting.html>
4. Ejecute la aplicación.
5. Pulse una de las opciones de Lectura o Escritura para habilitar el modo correspondiente. Si va a escribir, introduzca un valor.
6. Acerque la etiqueta NFC al dispositivo para completar la operación de lectura o escritura. La página de prueba y la aplicación mostrarán los resultados.

---

## Seguir leyendo

- ← Anterior: [Función MultiAPICall](multi-api-call.md)
- Siguiente →: [Plugin Siri](siri.md)
- La misma función en otras plataformas: [Android – Plugin NFC](../android/nfc.md)
- Idiomas: [🇺🇸 English](../../ios/nfc.md) · [🇩🇪 Deutsch](../../de/ios/nfc.md) · [🇫🇷 Français](../../fr/ios/nfc.md) · **🇪🇸 Español** · [🇨🇳 中文](../../zh/ios/nfc.md)

> [!TIP]
> **¿Sin tiempo? Configuramos su app por usted.** Nuestro equipo configura, compila & publica su app WebViewGold: llave en mano, entrega rápida, Made in Germany. [Configurar mi app →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **Compile en su navegador:** Sin Mac ni IDE: el **WebViewGold Cloud Builder** configura, compila & sube su app en línea. [Descubra Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
