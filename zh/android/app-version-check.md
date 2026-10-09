---
title: "应用版本检查 API – WebViewGold for Android 文档"
description: "从您的 Web 应用检测已安装的应用版本，并在需要时提示用户更新。"
lang: "zh"
product: "WebViewGold for Android"
platform: "Android"
category: "API 与功能"
slug: "app-version-check"
canonical_url: "https://www.webviewgold.com/zh/docs/android/app-version-check/"
keywords:
  - "应用版本检查 API"
  - "WebViewGold for Android"
  - "将网站转换为应用"
  - "WebView 应用文档"
  - "Android WebView SDK"
  - "PWA 转应用"
  - "HTML 转应用"
  - "JavaScript 桥接"
last_updated: "2026-10-09"
---

# 应用版本检查 API – WebViewGold for Android

> **摘要：** 从您的 Web 应用检测已安装的应用版本，并在需要时提示用户更新。

[文档](../README.md) › [WebViewGold for Android](README.md) › 应用版本检查 API

**平台：** Android · **类别：** API 与功能 · **在线版本：** [www.webviewgold.com/zh/docs/android/app-version-check/](https://www.webviewgold.com/zh/docs/android/app-version-check/)

---

使用此 WebViewGold App Version Check API，您的网站/Web 应用可以**获取您的 Android 应用用户所使用的 Android 应用的版本**。如果您想通知使用旧版本的用户更新其应用，此 API 会特别有用。此外，您还可以隐藏那些需要特定应用版本所支持的应用功能的 Web 应用板块。\
使用 JavaScript 访问此类 URL，即可读取并弹出显示应用版本号和应用 Bundle 编号：

```html
<script>
window.location.href = "getappversion://";
alert(versionNumber);
alert(bundleNumber);
</script>
```

**或者，可以考虑在 Config.java 中将  `AUTO_INJECT_VARIABLES`  设置为 `true`，以自动将此值（以及其他值）注入到 JavaScript 中，而无需事先调用 URL。**

---

## 继续阅读

- ← 上一页： [截屏 API](take-screenshot.md)
- 下一页 →： [通讯录 API](contacts.md)
- 其他平台上的相同功能： [iOS – 应用版本检查 API](../ios/app-version-check.md)
- 语言： [🇺🇸 English](../../android/app-version-check.md) · [🇩🇪 Deutsch](../../de/android/app-version-check.md) · [🇫🇷 Français](../../fr/android/app-version-check.md) · [🇪🇸 Español](../../es/android/app-version-check.md) · **🇨🇳 中文**

> [!TIP]
> **太忙了？我们替您搭建应用。** 我们的团队为您配置、构建并提交 WebViewGold 应用——全程代劳、交付迅速、德国制造。 [让我们搭建应用 →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_android_doc_online)
>
> **在浏览器中构建：** 无需 Mac、无需 IDE：**WebViewGold Cloud Builder** 在线为您配置、构建并上传应用。 [了解 Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=android_docs)
