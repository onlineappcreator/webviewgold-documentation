---
title: "加载指示 API – WebViewGold for Android 文档"
description: "按需显示或隐藏原生加载指示器，并自定义 Android 应用的加载体验。"
lang: "zh"
product: "WebViewGold for Android"
platform: "Android"
category: "API 与功能"
slug: "loading-sign"
canonical_url: "https://www.webviewgold.com/zh/docs/android/loading-sign/"
keywords:
  - "加载指示 API"
  - "WebViewGold for Android"
  - "将网站转换为应用"
  - "WebView 应用文档"
  - "Android WebView SDK"
  - "PWA 转应用"
  - "HTML 转应用"
  - "JavaScript 桥接"
last_updated: "2026-10-09"
---

# 加载指示 API – WebViewGold for Android

> **摘要：** 按需显示或隐藏原生加载指示器，并自定义 Android 应用的加载体验。

[文档](../README.md) › [WebViewGold for Android](README.md) › 加载指示 API

**平台：** Android · **类别：** API 与功能 · **在线版本：** [www.webviewgold.com/zh/docs/android/loading-sign/](https://www.webviewgold.com/zh/docs/android/loading-sign/)

---

WebViewGold 的原生 Android 加载指示器会在页面开始或完成加载时自动出现。不过，对于标准页面加载事件之外的场景，您也可以手动控制加载指示器。这对于需要让用户感知加载过程的操作尤其有用，例如：

- 在实时聊天队列中等待
- 在云服务器上运行后台进程
- 将任何其他耗时较长的过程可视化，以便让用户感知

## 用法

要为您的 WebView 应用手动控制加载指示器，请使用以下链接：

```html
<a href="spinneron://">Show the loading spinner</a>
<a href="spinneroff://">Hide the loading spinner</a>
```

---

## 继续阅读

- ← 上一页： [重置应用 API](reset-app.md)
- 下一页 →： [剪贴板 API](clipboard.md)
- 其他平台上的相同功能： [iOS – 加载标志 API](../ios/loading-sign.md)
- 语言： [🇺🇸 English](../../android/loading-sign.md) · [🇩🇪 Deutsch](../../de/android/loading-sign.md) · [🇫🇷 Français](../../fr/android/loading-sign.md) · [🇪🇸 Español](../../es/android/loading-sign.md) · **🇨🇳 中文**

> [!TIP]
> **太忙了？我们替您搭建应用。** 我们的团队为您配置、构建并提交 WebViewGold 应用——全程代劳、交付迅速、德国制造。 [让我们搭建应用 →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_android_doc_online)
>
> **在浏览器中构建：** 无需 Mac、无需 IDE：**WebViewGold Cloud Builder** 在线为您配置、构建并上传应用。 [了解 Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=android_docs)
