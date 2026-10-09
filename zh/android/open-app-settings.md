---
title: "Open App Settings API – WebViewGold for Android 文档"
description: "Send the user straight to the system App-info screen from your web app to manage permissions, notifications, storage, or force-stop your Android app."
lang: "zh"
product: "WebViewGold for Android"
platform: "Android"
category: "API 与功能"
slug: "open-app-settings"
canonical_url: "https://www.webviewgold.com/zh/docs/android/open-app-settings/"
keywords:
  - "Open App Settings API"
  - "WebViewGold for Android"
  - "将网站转换为应用"
  - "WebView 应用文档"
  - "Android WebView SDK"
  - "PWA 转应用"
  - "HTML 转应用"
  - "JavaScript 桥接"
last_updated: "2026-10-09"
---

# Open App Settings API – WebViewGold for Android

> **摘要：** Send the user straight to the system App-info screen from your web app to manage permissions, notifications, storage, or force-stop your Android app.

[文档](../README.md) › [WebViewGold for Android](README.md) › Open App Settings API

**平台：** Android · **类别：** API 与功能 · **在线版本：** [www.webviewgold.com/zh/docs/android/open-app-settings/](https://www.webviewgold.com/zh/docs/android/open-app-settings/)

---

WebViewGold 的 **Open App Settings API** 将用户直接发送到系统**应用信息**页面，从那里他们可以管理权限、通知、存储或强制停止应用 — 无需离开您的 Web 应用去 Android 设置中查找。

## 使用方法

通过 HTML 链接或 JavaScript 触发该屏幕：

```html
<a href="settingsapp://">Open app settings</a>
```

```javascript
window.location.href = "settingsapp://";
```

## 典型用例

- 用户拒绝了某项权限（相机、麦克风、位置、通知）— 将其直接引导至系统屏幕以重新启用。
- 引导用户从操作系统一侧禁用电池优化或清除缓存。

**说明：** 无参数。任何以 `settingsapp://` 开头的 URL 都会触发相同的屏幕。适用于所有受支持的 Android 版本。

---

## 继续阅读

- ← 上一页： [NFC 插件](nfc.md)
- 下一页 →： [Reconnect API](reconnect.md)
- 其他平台上的相同功能： [iOS – 打开应用设置 API](../ios/open-app-settings.md)
- 语言： [🇺🇸 English](../../android/open-app-settings.md) · [🇩🇪 Deutsch](../../de/android/open-app-settings.md) · [🇫🇷 Français](../../fr/android/open-app-settings.md) · [🇪🇸 Español](../../es/android/open-app-settings.md) · **🇨🇳 中文**

> [!TIP]
> **太忙了？我们替您搭建应用。** 我们的团队为您配置、构建并提交 WebViewGold 应用——全程代劳、交付迅速、德国制造。 [让我们搭建应用 →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_android_doc_online)
>
> **在浏览器中构建：** 无需 Mac、无需 IDE：**WebViewGold Cloud Builder** 在线为您配置、构建并上传应用。 [了解 Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=android_docs)
