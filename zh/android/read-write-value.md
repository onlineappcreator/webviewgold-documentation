---
title: "Read/Write Value API – WebViewGold for Android 文档"
description: "Persist small strings on the device from JavaScript and read them back — for theme, language, session tokens, or onboarding state."
lang: "zh"
product: "WebViewGold for Android"
platform: "Android"
category: "API 与功能"
slug: "read-write-value"
canonical_url: "https://www.webviewgold.com/zh/docs/android/read-write-value/"
keywords:
  - "Read/Write Value API"
  - "WebViewGold for Android"
  - "将网站转换为应用"
  - "WebView 应用文档"
  - "Android WebView SDK"
  - "PWA 转应用"
  - "HTML 转应用"
  - "JavaScript 桥接"
last_updated: "2026-10-09"
---

# Read/Write Value API – WebViewGold for Android

> **摘要：** Persist small strings on the device from JavaScript and read them back — for theme, language, session tokens, or onboarding state.

[文档](../README.md) › [WebViewGold for Android](README.md) › Read/Write Value API

**平台：** Android · **类别：** API 与功能 · **在线版本：** [www.webviewgold.com/zh/docs/android/read-write-value/](https://www.webviewgold.com/zh/docs/android/read-write-value/)

---

**读/写值 API** 通过应用的私有存储将任意字符串持久存储在设备上，并将其读取回您的 JavaScript。值在应用重启和缓存清除后仍然存在 — 除非操作系统清除了应用数据。

## 写入值

`writevalue://` 之后的所有内容都会被原样存储为一个字符串。您可以设计自己的格式（查询字符串、JSON、CSV — 只要适合您的 Web 应用）：

```html
<a href="writevalue://darkmode=on;user=42">Save</a>
```

## 读取值

触发 `readvalue://` 时，应用会将存储的字符串注入回 WebView，以便您的 JavaScript 能够读取：

```html
<a href="readvalue://" onclick="setTimeout(showSettings, 200)">Load</a>
<script>
  function showSettings() {
    console.log(window.appSettings || "no settings yet");
  }
</script>
```

## 典型用例

- 在离线状态下记住用户的主题、语言或引导状态。
- 当无法依赖 cookie 时缓存会话令牌。
- 无需后端往返即可持久保存小型本地首选项。

**说明：** 值按应用安装和设备存储 — 它们**不会**在设备间同步。请保持值较小；此 API 面向设置存储，而非二进制大对象存储。

---

## 继续阅读

- ← 上一页： [Reconnect API](reconnect.md)
- 下一页 →： [Biometric Auth API](biometric-auth.md)
- 其他平台上的相同功能： [iOS – 读写值 API](../ios/read-write-value.md)
- 语言： [🇺🇸 English](../../android/read-write-value.md) · [🇩🇪 Deutsch](../../de/android/read-write-value.md) · [🇫🇷 Français](../../fr/android/read-write-value.md) · [🇪🇸 Español](../../es/android/read-write-value.md) · **🇨🇳 中文**

> [!TIP]
> **太忙了？我们替您搭建应用。** 我们的团队为您配置、构建并提交 WebViewGold 应用——全程代劳、交付迅速、德国制造。 [让我们搭建应用 →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_android_doc_online)
>
> **在浏览器中构建：** 无需 Mac、无需 IDE：**WebViewGold Cloud Builder** 在线为您配置、构建并上传应用。 [了解 Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=android_docs)
