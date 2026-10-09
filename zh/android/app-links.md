---
title: "App Links 与深度链接 API – WebViewGold for Android 文档"
description: "借助 App Links 和自定义 URL scheme 深度链接，将指向您域名的链接直接在 Android 应用中打开。"
lang: "zh"
product: "WebViewGold for Android"
platform: "Android"
category: "API 与功能"
slug: "app-links"
canonical_url: "https://www.webviewgold.com/zh/docs/android/app-links/"
keywords:
  - "App Links / 深度链接"
  - "WebViewGold for Android"
  - "将网站转换为应用"
  - "WebView 应用文档"
  - "Android WebView SDK"
  - "PWA 转应用"
  - "HTML 转应用"
  - "JavaScript 桥接"
last_updated: "2026-10-09"
---

# App Links 与深度链接 API – WebViewGold for Android

> **摘要：** 借助 App Links 和自定义 URL scheme 深度链接，将指向您域名的链接直接在 Android 应用中打开。

[文档](../README.md) › [WebViewGold for Android](README.md) › App Links / 深度链接

**平台：** Android · **类别：** API 与功能 · **在线版本：** [www.webviewgold.com/zh/docs/android/app-links/](https://www.webviewgold.com/zh/docs/android/app-links/)

---

WebViewGold 的应用链接 (App Links) / 深度链接 API 让用户能够从电子邮件、社交媒体或消息应用等外部来源打开您应用中的特定页面。

## 适用于 Android 的 WebViewGold 支持两种深度链接方式

- **基于标准 URL 的深度链接：** 例如 `https://www.example.org/subpages/example1`
- **自定义方案深度链接：** 例如 `webviewgold://https://www.example.org/subpages/example2`

## 步骤 1：在 AndroidManifest.xml 中配置链接方案

若要支持标准深度链接，请配置您的 **AndroidManifest.xml**，以将您的域名与应用关联起来。请将 `www.webviewgold.com` 替换为您的实际域名（例如 `www.example.org`）：

![用于应用链接配置的 AndroidManifest.xml](../../assets/android/img/applinks1.webp)

## 步骤 2：在 Config.java 中启用深度链接

在您的 **Config.java** 文件中，启用深度链接功能：

```java
// Enables standard deep linking (https:// links)
public static final boolean IS_DEEP_LINKING_ENABLED = true;

// Enables custom scheme deep linking (e.g., webviewgold://)
public static final boolean IS_CUSTOM_SCHEME_ENABLED = true;

// Set your desired scheme prefix (must match AndroidManifest.xml)
public static final String CUSTOM_DEEPLINK_SCHEME = "webviewgold";
```

![用于应用链接配置的 Config.java](../../assets/android/img/applinks2.webp)

## 步骤 3：验证域名所有权（针对基于 URL 的深度链接）

若要使用 HTTPS URL 启用深度链接，您必须向 Google 验证域名所有权。请遵循 [**Google 网站验证指南**](https://developer.android.com/training/app-links/verify-android-applinks)。

## 测试您的应用链接

您可以通过 Android Studio 或终端测试这两种类型的链接：

- **使用 Android Studio：** 从 **Tools** 菜单打开 **App Links Assistant**，以进行模拟和排查故障。
- **使用终端或命令提示符：**
  1. 运行以下命令：

     ```bash
     adb shell am start -a android.intent.action.VIEW -d "webviewgold://https://www.example.org/subpages/example2" com.webviewgold.myappname
     ```

     - 请将 `com.webviewgold.myappname` 替换为您的实际应用包名。
     - 您也可以使用类似 `https://www.example.org/subpages/example1` 的 URL 链接进行测试。

一切设置完成后，用户就可以使用如下深度链接直接打开您应用中的任意特定页面：

- `https://www.example.org/subpages/example1`
- `webviewgold://https://www.example.org/subpages/example2`

**有疑问？** 随时联系我们！

---

## 继续阅读

- ← 上一页： [手电筒 API](flashlight.md)
- 下一页 →： [ShareIntent API](share-intent.md)
- 其他平台上的相同功能： [iOS – Universal Links API](../ios/universal-links.md)
- 语言： [🇺🇸 English](../../android/app-links.md) · [🇩🇪 Deutsch](../../de/android/app-links.md) · [🇫🇷 Français](../../fr/android/app-links.md) · [🇪🇸 Español](../../es/android/app-links.md) · **🇨🇳 中文**

> [!TIP]
> **太忙了？我们替您搭建应用。** 我们的团队为您配置、构建并提交 WebViewGold 应用——全程代劳、交付迅速、德国制造。 [让我们搭建应用 →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_android_doc_online)
>
> **在浏览器中构建：** 无需 Mac、无需 IDE：**WebViewGold Cloud Builder** 在线为您配置、构建并上传应用。 [了解 Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=android_docs)
