---
title: "WebViewGold for Android 文档 – 将网站转换为 Android 应用"
description: "WebViewGold for Android 官方文档：几分钟内将您的网站转换为原生 Android 应用——包含设置指南、30 多个 API 与功能，以及 Google Play 发布。"
lang: "zh"
product: "WebViewGold for Android"
platform: "Android"
canonical_url: "https://www.webviewgold.com/zh/docs/android/"
keywords:
  - "WebViewGold for Android"
  - "将网站转换为应用"
  - "WebView 应用文档"
  - "Android WebView SDK"
  - "PWA 转应用"
  - "HTML 转应用"
  - "JavaScript 桥接"
last_updated: "2026-10-09"
---

# WebViewGold for Android 文档

![WebViewGold for Android](../../assets/android/img/header.webp)

> WebViewGold for Android 官方文档：几分钟内将您的网站转换为原生 Android 应用——包含设置指南、30 多个 API 与功能，以及 Google Play 发布。

[文档](../README.md) › WebViewGold for Android

在几分钟内将您的网站、PWA、SaaS 仪表板、电商店面或 AI 生成的 Web 应用转换为原生 Android 应用。像使用轻量级应用 SDK 一样使用 WebViewGold：配置 URL、启用原生 API、集成 JavaScript 桥接命令，无需从头重建 Web 产品即可发布可上架的应用。

WebViewGold 兼容经典的 HTML/PHP 网站、WordPress、jQuery Mobile 项目，以及使用 Lovable、Base44、Bolt、Bubble、React、Vue、Angular 或类似工具创建的现代 Web 应用。以下文档以技术性、注重实现的方式介绍配置流程、原生功能 API、安全注意事项和发布步骤。

**[开始教程 →](setup-website.md)** · [下载 WebViewGold](https://www.webviewgold.com/download/android) · [Cloud Builder](https://www.webviewgold.com/cloud-builder?ref=android_docs)

## 快速上手

从网站到已发布应用，只需三步：

1. **[设置您的 Web 应用](setup-website.md)** — 使用远程 URL、打包本地 HTML 文件，或将两者结合并提供离线回退。
2. **[配置 WebViewGold](setup.md)** — 插入您的 URL，并在一个简单的配置文件中微调每个选项——无需编写代码。
3. **[构建并发布](publish.md)** — 将您的应用发布到商店——自行发布、通过 Cloud Builder，或使用我们的发布服务。

## 最新动态

WebViewGold 会定期更新。查看完整更新日志 [点此](https://www.webviewgold.com/changelog/android/).

## 所有主题、API 与功能

WebViewGold for Android 的全部能力——每个主题独立成页：

### 快速开始

- **[设置 Web 应用](setup-website.md)** — 为您的 Android 应用准备网站、PWA 或本地 HTML 文件：使用远程 URL、将文件离线打包到应用中，或将两者结合并提供离线回退方案。
- **[配置 WebViewGold](setup.md)** — 下载 WebViewGold 的 Android Studio 模板，填入您的 URL，探索所有内置配置选项——无需任何编程技能。

### 应用设计

- **[应用图标](app-icon.md)** — 在 Android Studio 中为您的 WebViewGold Android 应用添加自定义应用图标——分步指南。
- **[启动画面](splash-screen.md)** — 使用您自己的图形自定义 Android WebView 应用的启动画面。
- **[Navigation Drawer & Footer](navigation-drawer.md)** — Ship an app-like navigation experience with the built-in Material navigation drawer and Material 3 bottom navigation bar — no changes to your website required.

### API 与功能

- **[URL 处理 API](url-handling.md)** — 决定哪些链接在您的 Android 应用内、Chrome Custom Tabs 中或外部浏览器中打开。
- **[自定义 CSS 和 JS API](custom-css-js.md)** — 将自定义 CSS 样式和 JavaScript 代码注入 Android WebView 应用的任意页面——非常适合仅在应用中生效的调整。
- **[Multi API Call](multi-api-call.md)** — 在一次 window.location.href 赋值中调用多个 WebViewGold 数据 API — 非常适合同时使用 iOS 版本的跨平台 Web 应用。
- **[地理定位 API](geolocation.md)** — 在您的 Android WebView 应用中启用 HTML5 地理定位，并正确请求位置权限。
- **[推送通知 API](push-notifications.md)** — 通过 OneSignal、Firebase 或 Pushwoosh 向您的 Android 应用用户发送推送通知——详解设置、深度链接和按用户定向。
- **[AdMob 广告 API](admob.md)** — 使用 Google AdMob 横幅广告和插页式广告让您的 Android 应用实现变现——配置与 JavaScript 触发器。
- **[Facebook 广告 API](facebook-ads.md)** — 在您的 WebViewGold Android 应用中展示 Facebook Audience Network 横幅广告和插页式广告。
- **[文件下载 API](file-downloader.md)** — 让用户将图片、PDF 及其他文件从您的 Web 应用下载到 Android 设备。
- **[原生视频（PiP）API](native-video.md)** — 在您的 Android WebView 应用中以原生方式播放视频，并支持 Picture-in-Picture 画中画。
- **[重置应用 API](reset-app.md)** — 通过单个链接或 JavaScript 调用即可重置 Android WebView 应用的缓存、Cookie 和本地存储。
- **[加载指示 API](loading-sign.md)** — 按需显示或隐藏原生加载指示器，并自定义 Android 应用的加载体验。
- **[剪贴板 API](clipboard.md)** — 通过 JavaScript 将文本复制到 Android 剪贴板，并从您的 Web 应用读取剪贴板内容。
- **[UUID API](uuid.md)** — 通过附加到 WebView URL 或经由 JavaScript 获取的唯一 UUID 来识别应用安装。
- **[手电筒 API](flashlight.md)** — 在 WebViewGold for Android 中，通过简单的 JavaScript 链接从您的 Web 应用控制设备手电筒。
- **[App Links / 深度链接](app-links.md)** — 借助 App Links 和自定义 URL scheme 深度链接，将指向您域名的链接直接在 Android 应用中打开。
- **[ShareIntent API](share-intent.md)** — 通过 Share Intent 在您的 WebView 应用中直接接收从其他 Android 应用分享的内容。
- **[应用分享对话框 API](app-sharing-dialog.md)** — 从您的 Web 应用触发原生 Android 分享对话框，让用户分享您的应用或任意 URL。
- **[应用内评分 API](in-app-rating.md)** — 请求用户在 Google Play 上评分：通过 rateapp:// 从您的 Web 应用触发原生“为此应用评分”对话框，或让 WebViewGold 自动询问。
- **[应用内购买 API](in-app-purchases.md)** — 使用 Google Play Billing 在您的 Android WebView 应用中销售数字商品和订阅。
- **[IAP History API](iap-history.md)** — Return the user's Google Play purchase history as window.purchaseHistory so your web app can list subscriptions or unlock premium content client-side.
- **[QR 码扫描 API](qr-code-scanner.md)** — 从您的 Web 应用打开原生 QR 码扫描器，并通过 URL 或 JavaScript 处理扫描结果。
- **[扫描模式 API](scanning-mode.md)** — 在 WebViewGold for Android 中微调 QR 码和条形码扫描器的相机扫描行为。
- **[条形码扫描 API](barcode-scanner.md)** — 在您的 Android WebView 应用中以原生方式扫描 EAN、UPC 及其他条形码，并将结果传递给您的 Web 应用。
- **[截屏 API](take-screenshot.md)** — 通过编程方式捕获当前应用屏幕的截图，并使用 JavaScript 进行分享或保存。
- **[应用版本检查 API](app-version-check.md)** — 从您的 Web 应用检测已安装的应用版本，并在需要时提示用户更新。
- **[通讯录 API](contacts.md)** — 从您的 Web 应用访问设备通讯录：在 WebViewGold for Android 中经用户授权读取联系人。
- **[动态 UI API](dynamic-ui.md)** — 从您的 Web 应用在 Android 上动态更改状态栏颜色等原生 UI 元素。
- **[触觉反馈 API](haptic-feedback.md)** — 从您的 Web 应用触发原生振动触觉反馈，在 Android 上带来原生应用般的体验。
- **[NFC 插件](nfc.md)** — 在您的 Android WebView 应用中以原生方式读取 NFC 标签，并将标签数据传递给您的 Web 应用。
- **[Open App Settings API](open-app-settings.md)** — Send the user straight to the system App-info screen from your web app to manage permissions, notifications, storage, or force-stop your Android app.
- **[Reconnect API](reconnect.md)** — Reload the last online URL from your offline / fallback HTML page — the perfect "Try again" button for your custom offline screen.
- **[Read/Write Value API](read-write-value.md)** — Persist small strings on the device from JavaScript and read them back — for theme, language, session tokens, or onboarding state.
- **[Biometric Auth API](biometric-auth.md)** — Prompt fingerprint or face authentication with the native Android BiometricPrompt directly from your web app.
- **[Document Scanner](document-scanner.md)** — Add a Scan document option to the file upload dialog — the user scans up to 5 pages and your web app receives a PDF like any other upload.
- **[Printer API](printer.md)** — Send a remote image or PDF to the Android system print dialog — Wi-Fi printers, cloud print, or Save-as-PDF, straight from your web app.
- **[Health Connect API](health-connect.md)** — Read and write Android Health Connect records from JavaScript — mirrors the WebViewGold HealthKit API on iOS so one web app covers both platforms.

### 构建与发布

- **[Firebase Crashlytics](crashlytics.md)** — Ship crash reports and non-fatal events to your Firebase project, with runtime opt-in / opt-out from your web app.
- **[构建并发布](publish.md)** — 将您的 WebView 应用发布到 Google Play 商店：完整的发布服务、手动流程以及更改包名。

### 更多

- **[鸣谢与许可](credits.md)** — WebViewGold for Android 的许可条款、何时需要 Envato Extended License，以及开源鸣谢。
- **[为 WebViewGold 评分](rate.md)** — 喜欢 WebViewGold 吗？在 CodeCanyon 上花几秒钟为它评分——这将支持我们持续更新。
- **[iOS 与 macOS 版本](more-platforms.md)** — 将您的应用扩展到更多平台：获取适用于 iOS 和 macOS 的 WebViewGold，并复用同一个 Web 应用。
- **[支持与联系](support.md)** — 快速获取帮助：浏览 WebViewGold 支持中心，直接联系我们的团队，或申请德国制造的专业定制应用开发服务。

## 一个 Web 应用，覆盖所有平台

使用 WebViewGold，将同一个网站复用于 iOS、Android & macOS 应用。

- [WebViewGold for iOS](../ios/README.md)
- [WebViewGold for macOS](../macos/README.md)

**语言：** [🇺🇸 English](../../android/README.md) · [🇩🇪 Deutsch](../../de/android/README.md) · [🇫🇷 Français](../../fr/android/README.md) · [🇪🇸 Español](../../es/android/README.md) · **🇨🇳 中文**

> [!TIP]
> **太忙了？我们替您搭建应用。** 我们的团队为您配置、构建并提交 WebViewGold 应用——全程代劳、交付迅速、德国制造。 [让我们搭建应用 →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_android_doc_online)
>
> **在浏览器中构建：** 无需 Mac、无需 IDE：**WebViewGold Cloud Builder** 在线为您配置、构建并上传应用。 [了解 Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=android_docs)
