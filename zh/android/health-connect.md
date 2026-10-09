---
title: "Health Connect API – WebViewGold for Android 文档"
description: "Read and write Android Health Connect records from JavaScript — mirrors the WebViewGold HealthKit API on iOS so one web app covers both platforms."
lang: "zh"
product: "WebViewGold for Android"
platform: "Android"
category: "API 与功能"
slug: "health-connect"
canonical_url: "https://www.webviewgold.com/zh/docs/android/health-connect/"
keywords:
  - "Health Connect API"
  - "WebViewGold for Android"
  - "将网站转换为应用"
  - "WebView 应用文档"
  - "Android WebView SDK"
  - "PWA 转应用"
  - "HTML 转应用"
  - "JavaScript 桥接"
last_updated: "2026-10-09"
---

# Health Connect API – WebViewGold for Android

> **摘要：** Read and write Android Health Connect records from JavaScript — mirrors the WebViewGold HealthKit API on iOS so one web app covers both platforms.

[文档](../README.md) › [WebViewGold for Android](README.md) › Health Connect API

**平台：** Android · **类别：** API 与功能 · **在线版本：** [www.webviewgold.com/zh/docs/android/health-connect/](https://www.webviewgold.com/zh/docs/android/health-connect/)

---

**Health Connect API** 通过 [Android Health Connect](https://health.google/health-connect-android/) 读写健康记录。它镜像了 WebViewGold 的 iOS HealthKit 功能，因此您可以发布一款可在两个平台上访问健康数据的 Web 应用。读取操作始终返回请求的记录类型的**今日总量**。

## 读取记录

```html
<a href="readhealthkit://StepsRecord" onclick="setTimeout(show, 300)">
  My steps today
</a>

<script>
function show() {
  // Injected variable name matches the sanitized record name.
  alert(StepsRecord); // e.g. "8421.0 steps"
}
</script>
```

## 写入记录

格式：`writehealthkit://<RecordName>//<value>`

```html
<a href="writehealthkit://StepsRecord//1000">Log 1000 steps</a>
```

成功时，应用会注入 `<RecordName> = "WRITE_SUCCESS"`。失败时，则注入错误文本。

**支持的记录：** 您的应用已申请权限的任何 Health Connect 记录类型。常见的有：

- `StepsRecord`
- `HeartRateRecord`
- `WeightRecord`
- `SleepSessionRecord`
- `HydrationRecord`
- `ActiveCaloriesBurnedRecord`
- `DistanceRecord`

## 设置

1. 在设备上安装 **Health Connect**（在 Android 14+ 上预装）。
2. 首次使用时，应用会打开 Health Connect 权限对话框；用户会为请求的记录类型授予读取和/或写入权限。
3. 如果不支持 Health Connect，则注入的值会回退为字符串 `"Health Connect not supported"`。

**说明：** 值以 `"<number> <unit>"` 形式返回（例如 `"75.4 kg"`）。需要 Android 8.0（API 26）或更高版本。

---

## 继续阅读

- ← 上一页： [Printer API](printer.md)
- 下一页 →： [Firebase Crashlytics](crashlytics.md)
- 其他平台上的相同功能： [iOS – HealthKit 插件](../ios/healthkit.md)
- 语言： [🇺🇸 English](../../android/health-connect.md) · [🇩🇪 Deutsch](../../de/android/health-connect.md) · [🇫🇷 Français](../../fr/android/health-connect.md) · [🇪🇸 Español](../../es/android/health-connect.md) · **🇨🇳 中文**

> [!TIP]
> **太忙了？我们替您搭建应用。** 我们的团队为您配置、构建并提交 WebViewGold 应用——全程代劳、交付迅速、德国制造。 [让我们搭建应用 →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_android_doc_online)
>
> **在浏览器中构建：** 无需 Mac、无需 IDE：**WebViewGold Cloud Builder** 在线为您配置、构建并上传应用。 [了解 Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=android_docs)
