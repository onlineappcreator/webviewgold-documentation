---
title: "API UUID – WebViewGold pour macOS Documentation"
description: "Transmettez un identifiant d'appareil unique et non personnel (UUID) à JavaScript via get-uuid:// pour reconnaître les appareils et restaurer les réglages."
lang: "fr"
product: "WebViewGold pour macOS"
platform: "macOS"
category: "API et fonctionnalités"
slug: "uuid"
canonical_url: "https://www.webviewgold.com/fr/docs/mac/#uuid"
keywords:
  - "API UUID"
  - "WebViewGold pour macOS"
  - "convertir un site web en app"
  - "documentation d’app WebView"
  - "SDK WebView macOS"
  - "PWA en app"
  - "HTML en app"
  - "pont JavaScript"
last_updated: "2026-10-09"
---

# API UUID – WebViewGold pour macOS

> **Résumé :** Transmettez un identifiant d'appareil unique et non personnel (UUID) à JavaScript via get-uuid:// pour reconnaître les appareils et restaurer les réglages.

[Documentation](../README.md) › [WebViewGold pour macOS](README.md) › API UUID

**Plateforme :** macOS · **Catégorie :** API et fonctionnalités · **Version en ligne :** [www.webviewgold.com/fr/docs/mac/#uuid](https://www.webviewgold.com/fr/docs/mac/#uuid)

---

WebViewGold permet de transmettre un **identifiant d'appareil unique et non personnel** (UUID / « Universally Unique Identifier ») à JavaScript, qui **peut être utilisé pour identifier de manière unique les appareils macOS**. Cette API peut être utile, par exemple, pour enregistrer des paramètres ou des valeurs côté serveur et les restaurer côté client. Veuillez respecter les **réglementations locales et internationales en matière de confidentialité** si vous utilisez cette API.

```html
<a href="get-uuid://">Get UDID</a>
<a href="#" onClick="alert(uuid);">Show UDID</a>
```

---

## Continuer la lecture

- ← Précédent : [API In-App Purchases](in-app-purchases.md)
- Suivant → : [API Deeplinking](deep-linking.md)
- Même fonctionnalité sur les autres plateformes : [iOS – API UUID](../ios/uuid.md) · [Android – API UUID](../android/uuid.md)
- Langues : [🇺🇸 English](../../macos/uuid.md) · [🇩🇪 Deutsch](../../de/macos/uuid.md) · **🇫🇷 Français** · [🇪🇸 Español](../../es/macos/uuid.md) · [🇨🇳 中文](../../zh/macos/uuid.md)

