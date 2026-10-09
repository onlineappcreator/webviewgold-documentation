---
title: "API de icono de app dinámico – Documentación de WebViewGold para iOS"
description: "Cambie entre iconos de app alternativos en tiempo de ejecución en su app WebView de iOS, activado desde su aplicación web."
lang: "es"
product: "WebViewGold para iOS"
platform: "iOS"
category: "API y funciones"
slug: "dynamic-app-icon"
canonical_url: "https://www.webviewgold.com/es/docs/iOS/dynamic-app-icon/"
keywords:
  - "API de icono de app dinámico"
  - "WebViewGold para iOS"
  - "convertir sitio web en app"
  - "documentación de app WebView"
  - "SDK WebView de iOS"
  - "PWA a app"
  - "HTML a app"
  - "puente de JavaScript"
last_updated: "2026-10-09"
---

# API de icono de app dinámico – WebViewGold para iOS

> **Resumen:** Cambie entre iconos de app alternativos en tiempo de ejecución en su app WebView de iOS, activado desde su aplicación web.

[Documentación](../README.md) › [WebViewGold para iOS](README.md) › API de icono de app dinámico

**Plataforma:** iOS · **Categoría:** API y funciones · **Versión en línea:** [www.webviewgold.com/es/docs/iOS/dynamic-app-icon/](https://www.webviewgold.com/es/docs/iOS/dynamic-app-icon/)

---

Esta API **permite que los usuarios de su aplicación cambien el icono de la aplicación con solo pulsar un botón**. WebViewGold admite **hasta tres iconos alternativos** además del icono predeterminado. Siempre que el icono de la aplicación se cambie dinámicamente, se notificará al usuario tras completarse correctamente el cambio:\
![Notificación al usuario del cambio dinámico del icono de la aplicación.](../../assets/ios/img/icon-change-notice.jpeg)\
Si desea cambiar el icono de la aplicación en nombre de sus usuarios, puede hacerlo publicando una nueva versión de su aplicación con el nuevo icono instalado. Consulte cómo cambiar el icono de su aplicación en WebViewGold [aquí](app-name-icon-splash.md).\
Para cambiar dinámicamente el icono de la aplicación, basta con enlazar a uno de los siguientes formatos de URL:

```html
<script>
// Change to Alternative App Icon 1
window.location.href = "changeicon://icon1"

// Change to Alternative App Icon 2
window.location.href = "changeicon://icon2"

// Change to Alternative App Icon 3
window.location.href = "changeicon://icon3"

// Revert to the Default App Icon
window.location.href = "changeicon://default"

</script>
```

Vea una página de demostración y de prueba para esta API [aquí](https://webviewgoldtest.github.io/alticonsios.html).\
Para configurar sus iconos alternativos, abra los archivos de su aplicación en el Finder y diríjase a **WebView-Swift/WebView/ApplicationIcon/AppIconAlternate**.\
En esta carpeta encontrará plantillas de iconos para todos los tamaños requeridos en iOS (iPhones y iPads), correspondientes a cada icono alternativo:\
![La carpeta 'AppIconAlternate' contiene los iconos alternativos que puede editar.](../../assets/ios/img/alternative-app-icon-files.webp)\
Los nombres predeterminados de cada icono alternativo son: "AppIconAlternate1", "AppIconAlternate2" y "AppIconAlternate3".\
Si lo desea, puede cambiar los nombres predeterminados editando la variable **alternativeAppIconNames** en el archivo **Config**:\
![Use esta variable en Config para editar los nombres de archivo de los iconos alternativos.](../../assets/ios/img/alternative-app-icon-names.webp)\
Cada icono de la aplicación (por ejemplo, 'AppIconAlternateX') requiere cinco tamaños distintos, indicados por el sufijo del nombre de archivo:

- Para iPhones:

- AppIconAlternateX *(60x60 píxeles)*
- AppIconAlternateX**@2x** *(120x120 píxeles)*
- AppIconAlternateX**@3x** *(180x180 píxeles)*

- Para iPads:

- AppIconAlternateX**-ipad@2x** *(152x152 píxeles)*
- AppIconAlternateX**-ipad@3x** *(167x167 píxeles)*

Al reemplazar estas plantillas de iconos con las suyas propias, asegúrese de respetar el mismo formato de nombre de archivo (con los sufijos indicados arriba) y el tamaño de imagen correcto.\
Consulte una guía más detallada sobre las especificaciones de los iconos de aplicación [aquí](https://developer.apple.com/design/human-interface-guidelines/foundations/app-icons/).

Para activar esta API (también para la revisión de la App Store), abra Info.plist como código fuente (haga clic derecho sobre el archivo y seleccione "Open As" -> "Source Code" en el menú contextual):
Dentro de Info.plist, busque

```xml
<key>CFBundleIcons</key>
	<dict>
		<key>CFBundlePrimaryIcon</key>
		<dict>
			<key>CFBundleIconFiles</key>
			<array>
				<string></string>
			</array>
			<key>UIPrerenderedIcon</key>
			<false/>
		</dict>
	</dict>
```

y reemplácelo por

```xml
<key>CFBundleIcons</key>
<dict>
	<key>CFBundleAlternateIcons</key>
	<dict>
		<key>AppIconAlternate1</key>
		<dict>
			<key>CFBundleIconFiles</key>
			<array>
				<string>AppIconAlternate1</string>
			</array>
			<key>UIPrerenderedIcon</key>
			<false/>
		</dict>
		<key>AppIconAlternate2</key>
		<dict>
			<key>CFBundleIconFiles</key>
			<array>
				<string>AppIconAlternate2</string>
			</array>
			<key>UIPrerenderedIcon</key>
			<false/>
		</dict>
		<key>AppIconAlternate3</key>
		<dict>
			<key>CFBundleIconFiles</key>
			<array>
				<string>AppIconAlternate3</string>
			</array>
			<key>UIPrerenderedIcon</key>
			<false/>
		</dict>
	</dict>
	<key>CFBundlePrimaryIcon</key>
	<dict>
		<key>CFBundleIconFiles</key>
		<array>
			<string></string>
		</array>
		<key>UIPrerenderedIcon</key>
		<false/>
	</dict>
</dict>
```

Además, busque

```xml
<key>CFBundleIcons~ipad</key>
<dict>
    <key>CFBundlePrimaryIcon</key>
    <dict>
        <key>CFBundleIconFiles</key>
        <array>
            <string></string>
        </array>
        <key>UIPrerenderedIcon</key>
        <false/>
    </dict>
</dict>
```

y reemplácelo por

```xml
<key>CFBundleIcons~ipad</key>
<dict>
	<key>CFBundleAlternateIcons</key>
	<dict>
		<key>AppIconAlternate1</key>
		<dict>
			<key>CFBundleIconFiles</key>
			<array>
				<string>AppIconAlternate1-ipad</string>
			</array>
			<key>UIPrerenderedIcon</key>
			<false/>
		</dict>
		<key>AppIconAlternate2</key>
		<dict>
			<key>CFBundleIconFiles</key>
			<array>
				<string>AppIconAlternate2-ipad</string>
			</array>
			<key>UIPrerenderedIcon</key>
			<false/>
		</dict>
		<key>AppIconAlternate3</key>
		<dict>
			<key>CFBundleIconFiles</key>
			<array>
				<string>AppIconAlternate3-ipad</string>
			</array>
			<key>UIPrerenderedIcon</key>
			<false/>
		</dict>
	</dict>
	<key>CFBundlePrimaryIcon</key>
	<dict>
		<key>CFBundleIconFiles</key>
		<array>
			<string></string>
		</array>
		<key>UIPrerenderedIcon</key>
		<false/>
	</dict>
</dict>
```

Esta es la configuración predeterminada en cuanto a los nombres de los iconos alternativos y la cantidad de archivos de iconos alternativos.

---

## Seguir leyendo

- ← Anterior: [API de UI dinámica](dynamic-ui.md)
- Siguiente →: [API de Contactos](contacts.md)
- Idiomas: [🇺🇸 English](../../ios/dynamic-app-icon.md) · [🇩🇪 Deutsch](../../de/ios/dynamic-app-icon.md) · [🇫🇷 Français](../../fr/ios/dynamic-app-icon.md) · **🇪🇸 Español** · [🇨🇳 中文](../../zh/ios/dynamic-app-icon.md)

> [!TIP]
> **¿Sin tiempo? Configuramos su app por usted.** Nuestro equipo configura, compila & publica su app WebViewGold: llave en mano, entrega rápida, Made in Germany. [Configurar mi app →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **Compile en su navegador:** Sin Mac ni IDE: el **WebViewGold Cloud Builder** configura, compila & sube su app en línea. [Descubra Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
