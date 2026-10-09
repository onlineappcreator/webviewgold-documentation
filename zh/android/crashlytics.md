---
title: "Firebase Crashlytics – WebViewGold for Android 文档"
description: "Ship crash reports and non-fatal events to your Firebase project, with runtime opt-in / opt-out from your web app."
lang: "zh"
product: "WebViewGold for Android"
platform: "Android"
category: "构建与发布"
slug: "crashlytics"
canonical_url: "https://www.webviewgold.com/zh/docs/android/crashlytics/"
keywords:
  - "Firebase Crashlytics"
  - "WebViewGold for Android"
  - "将网站转换为应用"
  - "WebView 应用文档"
  - "Android WebView SDK"
  - "PWA 转应用"
  - "HTML 转应用"
  - "JavaScript 桥接"
last_updated: "2026-10-09"
---

# Firebase Crashlytics – WebViewGold for Android

> **摘要：** Ship crash reports and non-fatal events to your Firebase project, with runtime opt-in / opt-out from your web app.

[文档](../README.md) › [WebViewGold for Android](README.md) › Firebase Crashlytics

**平台：** Android · **类别：** 构建与发布 · **在线版本：** [www.webviewgold.com/zh/docs/android/crashlytics/](https://www.webviewgold.com/zh/docs/android/crashlytics/)

---

**Firebase Crashlytics** 集成会将匿名崩溃报告和非致命事件发送到您的 Firebase 项目，从而帮助您发现生产环境中的稳定性问题。

## 如何启用

1. 为您的应用设置 Firebase，并将 `google-services.json` 放到 `AndroidStudioSourceCode/app/` 中。
2. 在 **Config.java** 中启用跟踪：

   ```java
   public static final boolean TRACKING_EVENT = true;
   ```

`TRACKING_EVENT = false` 会禁用所有与跟踪相关的功能，包括 Crashlytics 事件日志记录以及 `starttracking://` / `endtracking://` 触发器。

## 从您的 Web 应用运行时选择加入/退出

WebViewGold 会遵循持久保存在设备上的每用户跟踪标志。使用标准的跟踪触发器在运行时更改它：

```html
<a href="starttracking://">Enable analytics & crash reports</a>
<a href="endtracking://">Disable analytics & crash reports</a>
```

当用户选择退出时，Crashlytics 采集将被关闭 — 不会上传任何内容。

## 报告内容

- 未处理的崩溃（堆栈跟踪、设备型号、操作系统版本）。
- 由应用外壳内部记录的非致命异常。
- 默认不附带任何个人用户数据。

**查看报告的位置：** 打开您的 **Firebase 控制台 → Crashlytics** 仪表板。报告通常会在崩溃后几分钟内出现。

**说明：** Crashlytics 初始化采用尽力而为策略 — 即使 Firebase 配置有误，应用仍能正常运行。请考虑在首次调用 `starttracking://` 之前添加同意屏幕（GDPR / CCPA）。

---

## 继续阅读

- ← 上一页： [Health Connect API](health-connect.md)
- 下一页 →： [构建并发布](publish.md)
- 语言： [🇺🇸 English](../../android/crashlytics.md) · [🇩🇪 Deutsch](../../de/android/crashlytics.md) · [🇫🇷 Français](../../fr/android/crashlytics.md) · [🇪🇸 Español](../../es/android/crashlytics.md) · **🇨🇳 中文**

> [!TIP]
> **太忙了？我们替您搭建应用。** 我们的团队为您配置、构建并提交 WebViewGold 应用——全程代劳、交付迅速、德国制造。 [让我们搭建应用 →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_android_doc_online)
>
> **在浏览器中构建：** 无需 Mac、无需 IDE：**WebViewGold Cloud Builder** 在线为您配置、构建并上传应用。 [了解 Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=android_docs)
