---
title: "ShareIntent API – WebViewGold for Android 文档"
description: "通过 Share Intent 在您的 WebView 应用中直接接收从其他 Android 应用分享的内容。"
lang: "zh"
product: "WebViewGold for Android"
platform: "Android"
category: "API 与功能"
slug: "share-intent"
canonical_url: "https://www.webviewgold.com/zh/docs/android/share-intent/"
keywords:
  - "ShareIntent API"
  - "WebViewGold for Android"
  - "将网站转换为应用"
  - "WebView 应用文档"
  - "Android WebView SDK"
  - "PWA 转应用"
  - "HTML 转应用"
  - "JavaScript 桥接"
last_updated: "2026-10-09"
---

# ShareIntent API – WebViewGold for Android

> **摘要：** 通过 Share Intent 在您的 WebView 应用中直接接收从其他 Android 应用分享的内容。

[文档](../README.md) › [WebViewGold for Android](README.md) › ShareIntent API

**平台：** Android · **类别：** API 与功能 · **在线版本：** [www.webviewgold.com/zh/docs/android/share-intent/](https://www.webviewgold.com/zh/docs/android/share-intent/)

---

WebViewGold 的 **ShareIntent API** 让您的应用能够作为目标出现在 Android 的原生分享对话框中。这样，用户就可以将文本、URL 或图片（以 base64 字符串形式）等内容从任何其他应用直接分享到您基于 WebView 的应用中。

## 使用场景

- 将指向用户个人资料、笔记或文章的链接直接分享到您的应用中
- 接收来自消息或浏览器应用的内容
- 将图库中的图片发送到您的 WebView 界面（base64 编码）

## 步骤 1：在 AndroidManifest.xml 中启用分享支持

若要让您的应用能够接收分享的数据，请取消您 **AndroidManifest.xml** 文件中相关 intent 过滤器的注释：

```html
<!-- Receive shared text (e.g., URLs or notes) -->
<intent-filter>
    <action android:name="android.intent.action.SEND" />
    <category android:name="android.intent.category.DEFAULT" />
    <data android:mimeType="text/plain" />
</intent-filter>

<!-- Receive a single shared image -->
<intent-filter>
    <action android:name="android.intent.action.SEND" />
    <category android:name="android.intent.category.DEFAULT" />
    <data android:mimeType="image/*" />
</intent-filter>

<!-- Receive multiple shared images -->
<intent-filter>
    <action android:name="android.intent.action.SEND_MULTIPLE" />
    <category android:name="android.intent.category.DEFAULT" />
    <data android:mimeType="image/*" />
</intent-filter>
```

这些过滤器生效后，每当用户从其他应用分享内容时，您基于 WebViewGold 的应用图标就会作为分享目标出现。

## 步骤 2：在 WebView 中处理分享的数据

当用户向您的应用分享内容时，WebViewGold 会自动将分享的内容注入到名为 `sharedData` 的 JavaScript 变量中。

```html
<script>
    alert(sharedData); // Displays the shared content (text or base64 image)

</script>
```

- **文本或 URL：** 将作为纯文本传入 `sharedData`
- **图片：** 将被转换为 base64 编码的字符串并传入 `sharedData`

**使用示例：** 根据接收到的内容自动填充表单或预览图片：

```html
<script>
    if (sharedData) {
        document.getElementById("myInput").value = sharedData;
    }
</script>
```

**注意：** 请确保您的 JavaScript 已准备好同时处理纯文本和较长的 base64 字符串。您也可以实现客户端检查，以区分不同的内容类型。

---

## 继续阅读

- ← 上一页： [App Links / 深度链接](app-links.md)
- 下一页 →： [应用分享对话框 API](app-sharing-dialog.md)
- 其他平台上的相同功能： [iOS – Share Extension](../ios/share-extension.md)
- 语言： [🇺🇸 English](../../android/share-intent.md) · [🇩🇪 Deutsch](../../de/android/share-intent.md) · [🇫🇷 Français](../../fr/android/share-intent.md) · [🇪🇸 Español](../../es/android/share-intent.md) · **🇨🇳 中文**

> [!TIP]
> **太忙了？我们替您搭建应用。** 我们的团队为您配置、构建并提交 WebViewGold 应用——全程代劳、交付迅速、德国制造。 [让我们搭建应用 →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_android_doc_online)
>
> **在浏览器中构建：** 无需 Mac、无需 IDE：**WebViewGold Cloud Builder** 在线为您配置、构建并上传应用。 [了解 Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=android_docs)
