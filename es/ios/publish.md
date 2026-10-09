---
title: "Compilar y publicar su app en la App Store – Documentación de WebViewGold para iOS"
description: "Publique su app WebView en la Apple App Store: servicio de publicación completo, proceso manual y cambio del identificador de bundle."
lang: "es"
product: "WebViewGold para iOS"
platform: "iOS"
category: "Compilar y publicar"
slug: "publish"
canonical_url: "https://www.webviewgold.com/es/docs/iOS/publish/"
keywords:
  - "Compilar y publicar"
  - "WebViewGold para iOS"
  - "convertir sitio web en app"
  - "documentación de app WebView"
  - "SDK WebView de iOS"
  - "PWA a app"
  - "HTML a app"
  - "puente de JavaScript"
last_updated: "2026-10-09"
---

# Compilar y publicar su app en la App Store – WebViewGold para iOS

> **Resumen:** Publique su app WebView en la Apple App Store: servicio de publicación completo, proceso manual y cambio del identificador de bundle.

[Documentación](../README.md) › [WebViewGold para iOS](README.md) › Compilar y publicar

**Plataforma:** iOS · **Categoría:** Compilar y publicar · **Versión en línea:** [www.webviewgold.com/es/docs/iOS/publish/](https://www.webviewgold.com/es/docs/iOS/publish/)

---

¿Su aplicación está lista y ahora es el momento de subirla a la Apple App Store y llegar a una audiencia de millones de personas? ¡Emocionante! La siguiente sección le mostrará cómo hacerlo, tanto si desea hacerlo usted mismo como si prefiere que le hagamos parte del trabajo.

> [!NOTE]
> ¿Prefiere un flujo de trabajo basado en el navegador? El [**WebViewGold Cloud Builder**](https://www.webviewgold.com/cloud-builder?ref=ios_docs) (complemento de pago) se encarga de la configuración, la compilación y las subidas directamente desde su navegador, sin Xcode.
>
> [![Ver el vídeo: Compilar y publicar su app en la App Store](https://img.youtube.com/vi/nzgCkydN9OM/hqdefault.jpg)](https://www.youtube.com/watch?v=nzgCkydN9OM)

## Opción A) Servicio completo de publicación de la aplicación

Llevar su aplicación a la App Store debería ser sencillo y sin complicaciones. Permítase recibir algo de ayuda: con [appsubmitter.io](https://www.appsubmitter.io), puede disfrutar de un **proceso de publicación cómodo y dirigido por expertos**, para que pueda centrarse en lo más importante mientras nosotros nos ocupamos de los detalles.

**¿Por qué elegir appsubmitter.io?**

- **Ahorre tiempo** – Nos encargamos de los certificados, las capturas de pantalla y las subidas.
- **Gestión experta** – Su aplicación se envía de forma profesional, sin complicaciones.
- **Publicada bajo su cuenta** – Usted tiene el control total, sin restricciones.
- **Garantía de aprobación** – Si Apple rechaza su aplicación, se le devolverá el importe íntegro (consulte los [Términos y Condiciones](https://www.onlineappcreator.com/terms.php)).

**¿Listo para el lanzamiento?** [Reserve una videollamada](https://www.appsubmitter.io/order-wizard/?platform=ios) ¡y pongamos su aplicación en marcha!

[![Servicio de publicación en la Apple App Store](../../assets/ios/img/apppublishingservice-ios.webp)](https://www.appsubmitter.io)

[![Ver el vídeo: Compilar y publicar su app en la App Store](https://img.youtube.com/vi/3o0xgQXagI8/hqdefault.jpg)](https://www.youtube.com/watch?v=3o0xgQXagI8)

## Opción B) Proceso de publicación manual

¿No quiere usar nuestro servicio de envío sin complicaciones, sino que prefiere encargarse usted mismo? Por supuesto, siga esta guía:

Utilice su **[suscripción al Apple Developer Program](https://developer.apple.com)** para publicar su aplicación en la App Store. Antes de subirla, cambie el **Bundle Identifier** (también llamado "Bundle ID"):

[![Ver el vídeo: Compilar y publicar su app en la App Store](https://img.youtube.com/vi/xqChOhStl3Q/hqdefault.jpg)](https://www.youtube.com/watch?v=xqChOhStl3Q)

*Consejo:* El [**WebViewGold Cloud Builder**](https://www.webviewgold.com/cloud-builder?ref=ios_docs) (complemento de pago) gestiona automáticamente los bundle identifiers y las subidas a la App Store, por lo que puede omitir este paso.

Repita este proceso para cada target, como `OneSignalNotificationServiceExtension`, `AppClip` y otras extensiones. El bundle identifier de cada target debe usar el bundle ID de su aplicación principal como prefijo. Por ejemplo, si el bundle ID de su aplicación principal es `com.my.app`, el bundle ID de la extensión de aplicación de OneSignal debería ser `com.my.app.OneSignalNotificationServiceExtension`.

*Tenga en cuenta que el **Bundle Identifier** y el nombre visible de su aplicación (el **Product Name**) son los únicos componentes de identificación que necesita cambiar en la plantilla de la aplicación. Evite cambiar el Project Name (llamado "WebViewGold"; es el nombre que aparece en la parte superior del navegador de proyecto, en el panel izquierdo de la ventana de Xcode), ya que puede causar problemas. El Project Name no es visible para los usuarios de su aplicación y no es importante en el proceso de envío de la aplicación.*

Después, añada textos personalizados a los detalles de los permisos en cuanto a la ubicación, el acceso a fotos/cámara y todos los demás detalles de la API. Elimine los permisos que su aplicación no necesite, excepto la clave **Privacy - Tracking Usage Description** (que Apple exige para todas las aplicaciones; eliminar esta clave hará que su aplicación se bloquee). Encontrará los detalles en el archivo **Info.plist**: \
![Activar o desactivar los permisos de iOS en el archivo Info.plist](../../assets/ios/img/infoplist2.webp)\
Después, considere realizar una revisión profesional de experiencia de usuario/UX en [UXreviewer.io](https://www.uxreviewer.io) o servicios similares para obtener los mejores resultados de aprobación en la App Store. Este tipo de revisión de UX también le ayuda a lograr una mejor retención de clientes en general para su producto, con sugerencias de mejora.\
Estupendo, ahora está listo para el envío a la App Store de su aplicación web. La aprobación en la App Store funciona en la mayoría de los casos sin ningún problema, pero depende en gran medida del contenido que proporcione en su aplicación, ya que WebViewGold no proporciona contenido por sí mismo. Asegúrese de enviar una aplicación que utilice un sitio web/aplicación web que se comporte como una aplicación móvil (por ejemplo, utilizando **diseño responsivo**). Asegúrese de que el contenido no contradiga los requisitos legales del Apple Developer Program. Utilice colores de enlace distintos de los colores HTML estándar para una mejor experiencia de usuario.

Después, siga los pasos de este segundo vídeo:

[![Ver el vídeo: Compilar y publicar su app en la App Store](https://img.youtube.com/vi/YPLs3xrDcm0/hqdefault.jpg)](https://www.youtube.com/watch?v=YPLs3xrDcm0)

**Un añadido al vídeo tutorial:**
En el minuto 07:00, después de crear el App Identifier, asegúrese de activar las capacidades "App Groups" y "Push Notifications" en la sección App Identifier del Apple Developer Portal (elija el App ID correcto [aquí](https://developer.apple.com/account/resources/identifiers/list)). Consulte estas capturas de pantalla: <https://prnt.sc/xz4hg5> & <https://prnt.sc/xz4j01>. Reinicie Xcode después.

**¿La subida a la App Store le pregunta si utiliza cifrado?**
No ofrecemos asesoramiento jurídicamente vinculante, pero en la mayoría de los casos aquí se debe indicar "No". Sin embargo, si se utiliza HTTPS, es posible que haya que presentar un informe de seguridad anual a las autoridades de EE. UU. Puede encontrar más información al respecto [aquí](https://developer.apple.com/documentation/security/complying_with_encryption_export_regulations).

**¿La subida a la App Store le pregunta si utiliza el Ad ID / IDFA?**
El Ad ID se incluye porque AdMob está integrado, pero no está activo de forma predeterminada. Eliminar el SDK de AdMob generará numerosos errores de dependencia, por lo que la sugerencia más sencilla sería elegir "Yes" en la pregunta "Does your app use the Ad ID?" y marcar únicamente la casilla "Attribute this app installation to a previously served advertisement" (deje todas las demás casillas en blanco). Así pues, si utiliza anuncios de banner/intersticiales de AdMob en WebViewGold, configure esta pantalla de [esta](https://prnt.sc/t8cj0a) manera. Si no utiliza anuncios de banner/intersticiales de AdMob en WebViewGold mientras el SDK sigue integrado (que es el caso habitual cuando no se usa AdMob en WebViewGold), seleccione [estas](https://prnt.sc/t8ci23) opciones.

Si Apple rechaza su aplicación, utilice el **Apple Resolution Center** para explicar la funcionalidad de la aplicación en general (como "Our app enables our existing users to login in/use our products on their handheld device/....). Si Apple sigue rechazando su aplicación, podemos ofrecerle un **reembolso completo** de la licencia de WebViewGold (reclamándolo dentro de los 14 días posteriores a la compra; consulte los [Términos y Condiciones](https://www.onlineappcreator.com/terms.php)). Solo tiene que contactarnos por correo electrónico.\
**¡Enhorabuena por su propia aplicación iOS publicada! 🎉**\
¿No tiene tiempo o no le apetece firmar y subir la aplicación manualmente? Considere el servicio [appsubmitter.io](https://www.appsubmitter.io):\
[![Servicio de publicación en la Apple App Store](../../assets/ios/img/apppublishingservice-ios.webp)](https://www.appsubmitter.io)

Por supuesto, ¡primero hay que celebrar el lanzamiento! Pero quizás el próximo proyecto ya esté en la agenda. Nuestros especialistas en aplicaciones también estarán encantados de ayudarle con [servicios de desarrollo individuales](https://www.onlineappcreator.com/custom-development-services.php) para aplicaciones web, aplicaciones iOS, aplicaciones Android, chatbots, ideas de marketing y mucho más. **[Más información](https://www.onlineappcreator.com/custom-development-services.php)**

---

## Seguir leyendo

- ← Anterior: [Plugin HealthKit](healthkit.md)
- Siguiente →: [Créditos y licencias](credits.md)
- La misma función en otras plataformas: [Android – Compilar y publicar](../android/publish.md)
- Idiomas: [🇺🇸 English](../../ios/publish.md) · [🇩🇪 Deutsch](../../de/ios/publish.md) · [🇫🇷 Français](../../fr/ios/publish.md) · **🇪🇸 Español** · [🇨🇳 中文](../../zh/ios/publish.md)

> [!TIP]
> **¿Sin tiempo? Configuramos su app por usted.** Nuestro equipo configura, compila & publica su app WebViewGold: llave en mano, entrega rápida, Made in Germany. [Configurar mi app →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **Compile en su navegador:** Sin Mac ni IDE: el **WebViewGold Cloud Builder** configura, compila & sube su app en línea. [Descubra Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
