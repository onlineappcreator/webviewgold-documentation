---
title: "Biometric Authentication API – WebViewGold for Android 文档"
description: "Prompt fingerprint or face authentication with the native Android BiometricPrompt directly from your web app."
lang: "zh"
product: "WebViewGold for Android"
platform: "Android"
category: "API 与功能"
slug: "biometric-auth"
canonical_url: "https://www.webviewgold.com/zh/docs/android/biometric-auth/"
keywords:
  - "Biometric Auth API"
  - "WebViewGold for Android"
  - "将网站转换为应用"
  - "WebView 应用文档"
  - "Android WebView SDK"
  - "PWA 转应用"
  - "HTML 转应用"
  - "JavaScript 桥接"
last_updated: "2026-10-09"
---

# Biometric Authentication API – WebViewGold for Android

> **摘要：** Prompt fingerprint or face authentication with the native Android BiometricPrompt directly from your web app.

[文档](../README.md) › [WebViewGold for Android](README.md) › Biometric Auth API

**平台：** Android · **类别：** API 与功能 · **在线版本：** [www.webviewgold.com/zh/docs/android/biometric-auth/](https://www.webviewgold.com/zh/docs/android/biometric-auth/)

---

**生物识别身份验证 API** 使用设备原生的 `BiometricPrompt` 提示用户进行指纹或人脸身份验证。如果操作系统已作相应配置，则会回退到设备 PIN 码或图案。

## 使用方法

通过 HTML 链接或 JavaScript 触发系统对话框：

```html
<a href="bioauth://">Unlock</a>
```

```javascript
window.location.href = "bioauth://";
```

## 典型用例

- 限制访问 Web 应用中的"钱包"、"设置"或"订单"页面。
- 在敏感的结账步骤之前要求重新进行身份验证。

## 行为

- 系统对话框由应用绘制 — 您的 Web 应用无需渲染任何 UI。
- 身份验证成功后，应用会正常恢复，使您的 Web 应用能够做出响应（例如导航到受保护的页面）。
- 在某些没有生物识别功能的设备上，操作系统可能会显示 PIN 码提示。

## 相关配置

**Config.java** 中的 `enableBioMetricAuth` 会开启内置的**应用锁**流程，每次启动应用时都会要求进行生物识别身份验证。`bioauth://` 独立于此标志，可随时通过 JavaScript 触发。

---

## 继续阅读

- ← 上一页： [Read/Write Value API](read-write-value.md)
- 下一页 →： [Document Scanner](document-scanner.md)
- 其他平台上的相同功能： [iOS – 生物识别认证 API](../ios/biometric-authentication.md)
- 语言： [🇺🇸 English](../../android/biometric-auth.md) · [🇩🇪 Deutsch](../../de/android/biometric-auth.md) · [🇫🇷 Français](../../fr/android/biometric-auth.md) · [🇪🇸 Español](../../es/android/biometric-auth.md) · **🇨🇳 中文**

> [!TIP]
> **太忙了？我们替您搭建应用。** 我们的团队为您配置、构建并提交 WebViewGold 应用——全程代劳、交付迅速、德国制造。 [让我们搭建应用 →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_android_doc_online)
>
> **在浏览器中构建：** 无需 Mac、无需 IDE：**WebViewGold Cloud Builder** 在线为您配置、构建并上传应用。 [了解 Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=android_docs)
