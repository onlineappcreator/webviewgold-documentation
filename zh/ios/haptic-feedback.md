---
title: "触觉反馈 API – WebViewGold for iOS 文档"
description: "从您的网页应用触发原生触觉反馈（振动），在 iOS 上带来真正原生的应用体验。"
lang: "zh"
product: "WebViewGold for iOS"
platform: "iOS"
category: "API 与功能"
slug: "haptic-feedback"
canonical_url: "https://www.webviewgold.com/zh/docs/iOS/haptic-feedback/"
keywords:
  - "触觉反馈 API"
  - "WebViewGold for iOS"
  - "将网站转换为应用"
  - "WebView 应用文档"
  - "iOS WebView SDK"
  - "PWA 转应用"
  - "HTML 转应用"
  - "JavaScript 桥接"
last_updated: "2026-10-09"
---

# 触觉反馈 API – WebViewGold for iOS

> **摘要：** 从您的网页应用触发原生触觉反馈（振动），在 iOS 上带来真正原生的应用体验。

[文档](../README.md) › [WebViewGold for iOS](README.md) › 触觉反馈 API

**平台：** iOS · **类别：** API 与功能 · **在线版本：** [www.webviewgold.com/zh/docs/iOS/haptic-feedback/](https://www.webviewgold.com/zh/docs/iOS/haptic-feedback/)

---

**WebViewGold** 支持在您的 Web 应用中实现原生的 iOS 触感（Haptic）控制。
使用我们的 API，您可以执行以下操作：

| 名称 | URL 协议 | 说明 |
| --- | --- | --- |
| 轻度冲击 | lighthaptic:// | 用于小型、轻量 UI 元素之间的碰撞 |
| 中度冲击 | mediumhaptic:// | 用于中等大小 UI 元素之间的碰撞 |
| 重度冲击 | heavyhaptic:// | 用于大型、重量级 UI 元素之间的碰撞 |
| 成功通知 | successhaptic:// | 表示某项任务或操作已成功完成 |
| 警告通知 | warninghaptic:// | 表示某项任务或操作产生了某种警告 |
| 错误通知 | errorhaptic:// | 表示发生了错误 |

在将这些功能集成到您的应用之前，建议先查看 Apple 的 [最佳实践](https://developer.apple.com/design/human-interface-guidelines/playing-haptics)概述。
以下是该 API 的使用示例，通过一个锚标签和自定义的 JavaScript 函数与我们的触感 API 进行交互。

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

点击[这里](https://webviewgoldtest.github.io/hapticFeedback.html)查看此功能的演示网页。您可以审查页面元素以查看示例代码。

---

## 继续阅读

- ← 上一页： [生物识别认证 API](biometric-authentication.md)
- 下一页 →： [快捷方式 API](shortcut.md)
- 其他平台上的相同功能： [Android – 触觉反馈 API](../android/haptic-feedback.md)
- 语言： [🇺🇸 English](../../ios/haptic-feedback.md) · [🇩🇪 Deutsch](../../de/ios/haptic-feedback.md) · [🇫🇷 Français](../../fr/ios/haptic-feedback.md) · [🇪🇸 Español](../../es/ios/haptic-feedback.md) · **🇨🇳 中文**

> [!TIP]
> **太忙了？我们替您搭建应用。** 我们的团队为您配置、构建并提交 WebViewGold 应用——全程代劳、交付迅速、德国制造。 [让我们搭建应用 →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **在浏览器中构建：** 无需 Mac、无需 IDE：**WebViewGold Cloud Builder** 在线为您配置、构建并上传应用。 [了解 Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
