---
title: "应用版本检查 API – WebViewGold for iOS 文档"
description: "从您的网页应用检测已安装的应用版本，并在需要时提示用户更新。"
lang: "zh"
product: "WebViewGold for iOS"
platform: "iOS"
category: "API 与功能"
slug: "app-version-check"
canonical_url: "https://www.webviewgold.com/zh/docs/iOS/app-version-check/"
keywords:
  - "应用版本检查 API"
  - "WebViewGold for iOS"
  - "将网站转换为应用"
  - "WebView 应用文档"
  - "iOS WebView SDK"
  - "PWA 转应用"
  - "HTML 转应用"
  - "JavaScript 桥接"
last_updated: "2026-10-09"
---

# 应用版本检查 API – WebViewGold for iOS

> **摘要：** 从您的网页应用检测已安装的应用版本，并在需要时提示用户更新。

[文档](../README.md) › [WebViewGold for iOS](README.md) › 应用版本检查 API

**平台：** iOS · **类别：** API 与功能 · **在线版本：** [www.webviewgold.com/zh/docs/iOS/app-version-check/](https://www.webviewgold.com/zh/docs/iOS/app-version-check/)

---

借助这种 WebViewGold JavaScript API 方式，您的网站/Web 应用可以**获取用户当前所使用的 iOS 应用版本**。当您希望提醒使用旧版本的用户升级应用时，此功能尤其有用。此外，您还可以隐藏那些依赖特定应用版本才可用的 Web 应用区块。\
使用如下 JavaScript 调用相应 URL，即可读取并弹窗显示应用版本及应用 bundle 编号：

```html
<script>
window.location.href = "getappversion://";
alert(versionNumber);
alert(bundleNumber);
</script>
```

**或者，也可以考虑在 Config.swift 中将 `autoInjectVariable` 设置为 `true`，将此值（以及其他值）自动注入 JavaScript，而无需事先调用 URL。**

---

## 继续阅读

- ← 上一页： [截图 API](take-screenshot.md)
- 下一页 →： [动态 UI API](dynamic-ui.md)
- 其他平台上的相同功能： [Android – 应用版本检查 API](../android/app-version-check.md)
- 语言： [🇺🇸 English](../../ios/app-version-check.md) · [🇩🇪 Deutsch](../../de/ios/app-version-check.md) · [🇫🇷 Français](../../fr/ios/app-version-check.md) · [🇪🇸 Español](../../es/ios/app-version-check.md) · **🇨🇳 中文**

> [!TIP]
> **太忙了？我们替您搭建应用。** 我们的团队为您配置、构建并提交 WebViewGold 应用——全程代劳、交付迅速、德国制造。 [让我们搭建应用 →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **在浏览器中构建：** 无需 Mac、无需 IDE：**WebViewGold Cloud Builder** 在线为您配置、构建并上传应用。 [了解 Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
