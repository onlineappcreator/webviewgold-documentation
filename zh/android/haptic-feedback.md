---
title: "触觉反馈 API – WebViewGold for Android 文档"
description: "从您的 Web 应用触发原生振动触觉反馈，在 Android 上带来原生应用般的体验。"
lang: "zh"
product: "WebViewGold for Android"
platform: "Android"
category: "API 与功能"
slug: "haptic-feedback"
canonical_url: "https://www.webviewgold.com/zh/docs/android/haptic-feedback/"
keywords:
  - "触觉反馈 API"
  - "WebViewGold for Android"
  - "将网站转换为应用"
  - "WebView 应用文档"
  - "Android WebView SDK"
  - "PWA 转应用"
  - "HTML 转应用"
  - "JavaScript 桥接"
last_updated: "2026-10-09"
---

# 触觉反馈 API – WebViewGold for Android

> **摘要：** 从您的 Web 应用触发原生振动触觉反馈，在 Android 上带来原生应用般的体验。

[文档](../README.md) › [WebViewGold for Android](README.md) › 触觉反馈 API

**平台：** Android · **类别：** API 与功能 · **在线版本：** [www.webviewgold.com/zh/docs/android/haptic-feedback/](https://www.webviewgold.com/zh/docs/android/haptic-feedback/)

---

**WebViewGold** 允许在您的 Web 应用中实现原生的 Android 触觉控制。
使用我们的 API，您可以执行以下操作：

| 名称 | URL 协议 | 说明 |
| --- | --- | --- |
| 轻度冲击 | lighthaptic:// | 用于小而轻的 UI 元素之间的碰撞 |
| 重度冲击 | heavyhaptic:// | 用于大而重的 UI 元素之间的碰撞 |
| 成功通知 | successhaptic:// | 表示某项任务或操作已成功完成 |
| 警告通知 | warninghaptic:// | 表示某项任务或操作产生了某种警告 |
| 错误通知 | errorhaptic:// | 表示发生了错误 |

下面是一个如何使用该 API 的示例，其中包含一个与我们的触觉 API 交互的锚点标签和自定义 JavaScript 函数。

```html
<a onclick="lightHaptic('index.html')">Navigation Link with Haptics</a>

<script>
function lightHaptic(url) {
  if (isWebViewBrowser) {
    window.location.href = url;
    loadInnerHref("lighthaptic://");
  } else {
    window.location.href = url;
  }
}

function loadInnerHref(url) {
  iFrame = document.createElement("iframe");
  iFrame.setAttribute("src", url);
  document.body.appendChild(iFrame);
  iFrame.parentNode.removeChild(iFrame);
  iFrame = null;
}
</script>
```

点击[此处](https://webviewgoldtest.github.io/hapticFeedback.html)查看此功能的演示网页。检查该页面即可查看示例代码。

---

## 继续阅读

- ← 上一页： [动态 UI API](dynamic-ui.md)
- 下一页 →： [NFC 插件](nfc.md)
- 其他平台上的相同功能： [iOS – 触觉反馈 API](../ios/haptic-feedback.md)
- 语言： [🇺🇸 English](../../android/haptic-feedback.md) · [🇩🇪 Deutsch](../../de/android/haptic-feedback.md) · [🇫🇷 Français](../../fr/android/haptic-feedback.md) · [🇪🇸 Español](../../es/android/haptic-feedback.md) · **🇨🇳 中文**

> [!TIP]
> **太忙了？我们替您搭建应用。** 我们的团队为您配置、构建并提交 WebViewGold 应用——全程代劳、交付迅速、德国制造。 [让我们搭建应用 →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_android_doc_online)
>
> **在浏览器中构建：** 无需 Mac、无需 IDE：**WebViewGold Cloud Builder** 在线为您配置、构建并上传应用。 [了解 Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=android_docs)
