---
title: "通讯录 API – WebViewGold for Android 文档"
description: "从您的 Web 应用访问设备通讯录：在 WebViewGold for Android 中经用户授权读取联系人。"
lang: "zh"
product: "WebViewGold for Android"
platform: "Android"
category: "API 与功能"
slug: "contacts"
canonical_url: "https://www.webviewgold.com/zh/docs/android/contacts/"
keywords:
  - "通讯录 API"
  - "WebViewGold for Android"
  - "将网站转换为应用"
  - "WebView 应用文档"
  - "Android WebView SDK"
  - "PWA 转应用"
  - "HTML 转应用"
  - "JavaScript 桥接"
last_updated: "2026-10-09"
---

# 通讯录 API – WebViewGold for Android

> **摘要：** 从您的 Web 应用访问设备通讯录：在 WebViewGold for Android 中经用户授权读取联系人。

[文档](../README.md) › [WebViewGold for Android](README.md) › 通讯录 API

**平台：** Android · **类别：** API 与功能 · **在线版本：** [www.webviewgold.com/zh/docs/android/contacts/](https://www.webviewgold.com/zh/docs/android/contacts/)

---

WebViewGold 允许将通讯录导出到一个 JavaScript 变量中，其格式如下所示，通过 **readcontacts://** API 实现。该 JSON 对象存储在 `contacts` 变量中。为了访问它，您的应用必须首先通过 **requestcontactpermission://** API 获得权限，该 API 会提示用户启用通讯录权限。如果未完成此步骤，**readcontacts://** 会将 `contacts` 变量填充为 null 值。\
存储在 JS `contacts` 变量中的示例输出：

```json
 {
   "John Appleseed":[
      "888-555-5512",
      "888-555-1212"
   ],
   "Daniel Higgins":[
      "555-478-7672",
      "(408) 555-5270",
      "(408) 555-3514"
   ],
   "David Taylor":[
      "555-610-6679"
   ],
   "Hank Zakroff":[
      "(555) 766-4823",
      "(707) 555-1854"
   ]
}
```

为了添加此通讯录功能，需要将 `android.permission.READ_CONTACTS` 权限添加到 *AndroidManifest.xml* 文件中，以便用户能够授予该权限。

---

## 继续阅读

- ← 上一页： [应用版本检查 API](app-version-check.md)
- 下一页 →： [动态 UI API](dynamic-ui.md)
- 其他平台上的相同功能： [iOS – 通讯录 API](../ios/contacts.md)
- 语言： [🇺🇸 English](../../android/contacts.md) · [🇩🇪 Deutsch](../../de/android/contacts.md) · [🇫🇷 Français](../../fr/android/contacts.md) · [🇪🇸 Español](../../es/android/contacts.md) · **🇨🇳 中文**

> [!TIP]
> **太忙了？我们替您搭建应用。** 我们的团队为您配置、构建并提交 WebViewGold 应用——全程代劳、交付迅速、德国制造。 [让我们搭建应用 →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_android_doc_online)
>
> **在浏览器中构建：** 无需 Mac、无需 IDE：**WebViewGold Cloud Builder** 在线为您配置、构建并上传应用。 [了解 Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=android_docs)
