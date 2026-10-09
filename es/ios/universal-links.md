---
title: "API de Universal Links – Documentación de WebViewGold para iOS"
description: "Abra los enlaces a su dominio directamente en su app iOS con Apple Universal Links: configuración, archivo AASA y resolución de problemas."
lang: "es"
product: "WebViewGold para iOS"
platform: "iOS"
category: "API y funciones"
slug: "universal-links"
canonical_url: "https://www.webviewgold.com/es/docs/iOS/universal-links/"
keywords:
  - "API de Universal Links"
  - "WebViewGold para iOS"
  - "convertir sitio web en app"
  - "documentación de app WebView"
  - "SDK WebView de iOS"
  - "PWA a app"
  - "HTML a app"
  - "puente de JavaScript"
last_updated: "2026-10-09"
---

# API de Universal Links – WebViewGold para iOS

> **Resumen:** Abra los enlaces a su dominio directamente en su app iOS con Apple Universal Links: configuración, archivo AASA y resolución de problemas.

[Documentación](../README.md) › [WebViewGold para iOS](README.md) › API de Universal Links

**Plataforma:** iOS · **Categoría:** API y funciones · **Versión en línea:** [www.webviewgold.com/es/docs/iOS/universal-links/](https://www.webviewgold.com/es/docs/iOS/universal-links/)

---

La **API de Universal Links** simplifica la vinculación a contenido dentro de su aplicación, proporcionando una experiencia de usuario más fluida y nativa. WebViewGold le permite configurar su dominio para que los enlaces de aplicaciones como **Mail, Safari y otras** se abran automáticamente dentro de su aplicación basada en WebViewGold, sin necesidad de indicaciones adicionales.

**Nota:** la aplicación debe estar instalada primero en el dispositivo del usuario para que esta función funcione.

**Alternativamente**, es posible utilizar nuestra [**API de Deep Linking**](deep-linking.md). Aunque funciona de manera similar, utiliza una sintaxis diferente. No obstante, cabe señalar que la sintaxis de la [**API de Universal Links**](universal-links.md) es más común que la sintaxis de la API de Deep Linking. Para la mayoría de las aplicaciones, es aconsejable elegir una u otra, pero no ambas.

Para configurar los **Universal Links** en su aplicación iOS, siga los pasos que se indican a continuación:

1. **Configuración en el Apple Developer Center:**

1. Inicie sesión en su cuenta en el [Apple Developer Center](https://developer.apple.com/account/).
2. Haga clic en 'Certificates, Identifiers & Profiles'.
3. En 'Identifiers', seleccione 'App IDs' y luego elija el ID de su aplicación en la lista.
4. En la sección 'App Services', marque la opción 'Associated Domains' y guarde los cambios.

2. **Configuración en Xcode:**

1. Abra el proyecto de su aplicación en Xcode.
2. Seleccione el target (en la mayoría de los casos "WebViewGold"). En la pestaña 'Signing & Capabilities', vaya a la sección 'Associated Domains'. Haga clic en '+' para añadir un dominio. Su dominio debe llevar el prefijo 'applinks:', de esta manera: `applinks:example.org` & `applinks:www.example.org`:\
   ![Dominios asociados en Xcode](../../assets/ios/img/associateddomains.webp)
3. En Config.swift, establezca **ShowExternalLink** en **true**.
4. Tenga en cuenta los subdominios. Existe una distinción entre los dominios "www.\*" y los que no son "www" (considere añadir ambos). Asegúrese de tener el perfil de aprovisionamiento correcto con la capacidad 'Associated Domains'. Si no, Xcode debería pedirle que lo corrija.

3. **Configuración del servidor:**

1. En el servidor de su sitio web, debe alojar un archivo Apple App Site Association (AASA) en el nivel raíz de su servidor o utilizando el prefijo `/.well-known/`. Por ejemplo, `https://example.org/.well-known/apple-app-site-association`
2. El archivo AASA debe contener detalles sobre la aplicación y los dominios asociados. Consulte la [documentación oficial](https://developer.apple.com/documentation/safariservices/supporting_associated_domains) para conocer la estructura exacta. Asegúrese de que el archivo apple-app-site-association esté alojado en un servidor que admita HTTPS, no solo HTTP.

**¡Listo! :-)** Las pruebas en el Simulador no son tan efectivas como en un dispositivo real. Para obtener los mejores resultados, utilice un iPhone o iPad real.

---

## Seguir leyendo

- ← Anterior: [API de CSS y JS personalizados](custom-css-js.md)
- Siguiente →: [API de deep linking](deep-linking.md)
- La misma función en otras plataformas: [Android – App Links / Deep Linking](../android/app-links.md)
- Idiomas: [🇺🇸 English](../../ios/universal-links.md) · [🇩🇪 Deutsch](../../de/ios/universal-links.md) · [🇫🇷 Français](../../fr/ios/universal-links.md) · **🇪🇸 Español** · [🇨🇳 中文](../../zh/ios/universal-links.md)

> [!TIP]
> **¿Sin tiempo? Configuramos su app por usted.** Nuestro equipo configura, compila & publica su app WebViewGold: llave en mano, entrega rápida, Made in Germany. [Configurar mi app →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **Compile en su navegador:** Sin Mac ni IDE: el **WebViewGold Cloud Builder** configura, compila & sube su app en línea. [Descubra Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
