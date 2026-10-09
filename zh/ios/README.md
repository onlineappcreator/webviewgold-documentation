---
title: "WebViewGold for iOS 文档——将网站转换为 iOS 应用"
description: "WebViewGold for iOS 官方文档：几分钟内将您的网站转换为原生 iOS 应用——设置指南、40 多个 API 与功能，以及 App Store 发布。"
lang: "zh"
product: "WebViewGold for iOS"
platform: "iOS"
canonical_url: "https://www.webviewgold.com/zh/docs/iOS/"
keywords:
  - "WebViewGold for iOS"
  - "将网站转换为应用"
  - "WebView 应用文档"
  - "iOS WebView SDK"
  - "PWA 转应用"
  - "HTML 转应用"
  - "JavaScript 桥接"
last_updated: "2026-10-09"
---

# WebViewGold for iOS 文档

![WebViewGold for iOS](../../assets/ios/img/header.webp)

> WebViewGold for iOS 官方文档：几分钟内将您的网站转换为原生 iOS 应用——设置指南、40 多个 API 与功能，以及 App Store 发布。

[文档](../README.md) › WebViewGold for iOS

在几分钟内将您的网站、PWA、SaaS 仪表板、电商店面或 AI 生成的 Web 应用转换为原生 iOS 应用。像使用轻量级应用 SDK 一样使用 WebViewGold：配置 URL、启用原生 API、集成 JavaScript 桥接命令，无需从头重建 Web 产品即可发布可上架的应用。

WebViewGold 兼容经典的 HTML/PHP 网站、WordPress、jQuery Mobile 项目，以及使用 Lovable、Base44、Bolt、Bubble、React、Vue、Angular 或类似工具创建的现代 Web 应用。以下文档以技术性、注重实现的方式介绍配置流程、原生功能 API、安全注意事项和发布步骤。

**[开始教程 →](setup-website.md)** · [下载 WebViewGold](https://www.webviewgold.com/download/ios) · [Cloud Builder](https://www.webviewgold.com/cloud-builder?ref=ios_docs)

## 快速上手

从网站到已发布应用，只需三步：

1. **[设置您的 Web 应用](setup-website.md)** — 使用远程 URL、打包本地 HTML 文件，或将两者结合并提供离线回退。
2. **[配置 WebViewGold](setup.md)** — 插入您的 URL，并在一个简单的配置文件中微调每个选项——无需编写代码。
3. **[构建并发布](publish.md)** — 将您的应用发布到商店——自行发布、通过 Cloud Builder，或使用我们的发布服务。

## 最新动态

WebViewGold 会定期更新。查看完整更新日志 [点此](https://www.webviewgold.com/changelog/ios/).

## 所有主题、API 与功能

WebViewGold for iOS 的全部能力——每个主题独立成页：

### 快速开始

- **[设置网页应用](setup-website.md)** — 为您的 iOS 应用准备网站、PWA 或本地 HTML 文件：使用远程 URL、将文件离线打包到应用中，或将两者结合并提供离线回退方案。
- **[配置 WebViewGold](setup.md)** — 下载 WebViewGold 的 Xcode 模板，在 Config.swift 中填入您的 URL，并探索所有内置配置选项——无需任何编程技能。

### 应用设计

- **[名称、图标和启动屏](app-name-icon-splash.md)** — 重命名您的 iOS 应用，添加自定义应用图标，并为您的 WebViewGold 应用设置个性化的启动屏幕图形。
- **[修改安全区域](safe-area.md)** — 调整安全区域并启用自定义底栏，让您的网页应用在带有主页横条的 iPhone 上完美显示。

### API 与功能

- **[地理定位 API](geolocation.md)** — 在您的 iOS WebView 应用中启用 HTML5 地理定位，并以正确的方式请求精确位置权限。
- **[推送通知 API](push-notifications.md)** — 使用 OneSignal、Firebase 或 Pushwoosh 向您的 iOS 应用用户发送推送通知——详解设置、深度链接和按用户定向。
- **[AdMob 广告 API](admob.md)** — 通过 Google AdMob 横幅、插屏和激励广告为您的 iOS 应用变现——配置与 JavaScript 触发器。
- **[Facebook 广告 API](facebook-ads.md)** — 在您的 WebViewGold iOS 应用中展示 Facebook Audience Network 横幅和插屏广告。
- **[HTML 音频 API](html-audio.md)** — 让 HTML 音频在您的 iOS WebView 应用后台持续播放——即使屏幕锁定也不中断。
- **[原生视频 API](native-video.md)** — 在 iOS 原生视频播放器中播放视频流并支持画中画——直接从您的 Web 应用触发。
- **[文件下载 API](file-downloader.md)** — 让用户将图片、PDF 和其他文件从您的网页应用直接下载到 iPhone 或 iPad 上。
- **[打印机 API](printer.md)** — 通过 AirPrint 从您的 Web 应用打印图片和 PDF：只需一个链接即可将文件发送到 iOS 原生打印对话框。
- **[iCal 日历 API](ical-calendar.md)** — 通过 iCal 日历 API 将网页应用中的日历事件添加到原生 iOS 日历中。
- **[Apple Wallet 凭证 API](wallet-pass.md)** — 让用户将 .pkpass 凭证（门票、优惠券、会员卡）从您的 Web 应用添加到 Apple Wallet。
- **[UUID API](uuid.md)** — 通过附加到 WebView URL 或经由 JavaScript 获取的唯一 UUID 来识别应用安装。
- **[手电筒 API](flashlight.md)** — 在 WebViewGold for iOS 中，通过简单的 JavaScript 链接从您的网页应用控制设备手电筒。
- **[重置应用 API](reset-app.md)** — 通过单个链接或 JavaScript 调用重置您的 iOS WebView 应用的缓存、Cookie 和本地存储。
- **[用户跟踪决定 API](user-tracking.md)** — 遵循 App Tracking Transparency：在您的 WebViewGold iOS 应用中读取用户的跟踪决定并作出响应。
- **[加载标志 API](loading-sign.md)** — 按需显示或隐藏原生加载指示器，并自定义您的 iOS 应用的加载体验。
- **[下拉刷新 API](pull-to-refresh.md)** — 在您的 iOS WebView 应用中启用原生下拉刷新手势，自定义其颜色，并从您的 Web 应用动态开启或关闭。
- **[URL 处理 API](url-handling.md)** — 决定哪些链接在应用内、应用内浏览器标签页或 Safari 中打开——为 iOS 提供完整的 URL 处理控制。
- **[社交登录助手](social-login.md)** — 借助内置的社交登录助手，让 Google、Facebook 和 Apple 的 OAuth 登录在您的 iOS WebView 应用中可靠运行。
- **[重新连接 API](reconnect.md)** — 在您的离线回退页面上添加“重试”按钮，重新加载您 iOS 应用的最后一个在线 URL。
- **[自定义 CSS 和 JS API](custom-css-js.md)** — 将自定义 CSS 样式和 JavaScript 代码注入您的 iOS WebView 应用的任意页面——非常适合仅限应用的调整。
- **[Universal Links API](universal-links.md)** — 借助 Apple Universal Links，将指向您域名的链接直接在 iOS 应用中打开——设置、AASA 文件与故障排除。
- **[深度链接 API](deep-linking.md)** — 通过自定义 URL 方案启动您的 iOS 应用，并将用户深度链接到网页应用的特定页面。
- **[应用分享对话框 API](app-sharing-dialog.md)** — 从您的网页应用触发原生 iOS 分享面板，让用户分享您的应用或任意 URL。
- **[应用内评分对话框 API](in-app-rating.md)** — 在最佳时机请求用户进行 App Store 评分——从您的 Web 应用触发 iOS 原生评分对话框。
- **[应用内购买 API](in-app-purchases.md)** — 借助由 StoreKit 驱动的应用内购买，在您的 iOS WebView 应用中销售数字商品和订阅。
- **[购买历史 API](iap-history.md)** — 以 JSON 形式从您的 Web 应用读取用户的历史应用内购买——非常适合“我的购买”页面。
- **[QR 码扫描 API](qr-code-scanner.md)** — 从您的网页应用打开原生 QR 码扫描器，并通过 URL 或 JavaScript 处理扫描结果。
- **[条形码扫描 API](barcode-scanner.md)** — 在您的 iOS WebView 应用中原生扫描 EAN、UPC 及其他条形码，并将结果传递给网页应用。
- **[扫描模式 API](scanning-mode.md)** — 在 WebViewGold for iOS 中微调 QR 码和条形码扫描器的相机扫描行为。
- **[文档扫描仪](document-scanner.md)** — 让用户使用相机扫描纸质文档，并通过您 Web 应用的文件上传功能上传——由 Apple VisionKit 驱动。
- **[截图 API](take-screenshot.md)** — 通过 JavaScript 以编程方式捕获当前应用屏幕的截图，并进行分享或保存。
- **[应用版本检查 API](app-version-check.md)** — 从您的网页应用检测已安装的应用版本，并在需要时提示用户更新。
- **[动态 UI API](dynamic-ui.md)** — 从您的网页应用动态更改原生 UI 元素，例如状态栏或底栏的颜色。
- **[动态应用图标 API](dynamic-app-icon.md)** — 在您的 iOS WebView 应用中于运行时切换备用应用图标——由您的网页应用触发。
- **[通讯录 API](contacts.md)** — 从您的网页应用访问设备通讯录：在 WebViewGold for iOS 中经用户授权读取联系人。
- **[生物识别认证 API](biometric-authentication.md)** — 使用 Face ID 或 Touch ID 保护您的 iOS 应用，并从您的网页应用对用户进行生物识别验证。
- **[触觉反馈 API](haptic-feedback.md)** — 从您的网页应用触发原生触觉反馈（振动），在 iOS 上带来真正原生的应用体验。
- **[快捷方式 API](shortcut.md)** — 为您的 iOS 应用添加主屏幕快速操作快捷方式，深度链接到特定页面。
- **[剪贴板 API](clipboard.md)** — 通过 JavaScript 从您的网页应用将文本复制到 iOS 剪贴板并读取剪贴板内容。
- **[读写值 API](read-write-value.md)** — 在设备上持久化存储字符串值，并将其读回到您 Web 应用的 JavaScript 中。
- **[打开应用设置 API](open-app-settings.md)** — 将用户直接引导至 iOS 设置应用中您的应用页面，以管理权限和通知。

### 扩展与插件

- **[Share Extension](share-extension.md)** — 借助 Share Extension，让用户将其他应用中的内容直接分享到您的 iOS WebView 应用中。
- **[Widget Extension](widget-extension.md)** — 为您的 iOS WebView 应用添加主屏幕小组件，将用户直接引导至您的网页应用。
- **[App Clip Extension](app-clip.md)** — 为您的 iOS 应用提供轻量级 App Clip 版本，无需安装即可即时打开。
- **[原生导航底栏](navigation-footer.md)** — 在您的 iOS 应用中启用带有后退、前进和自定义按钮的原生底部导航栏。
- **[原生侧边栏](sidebar.md)** — 启用带有自定义链接和 SF Symbols 图标的原生滑动侧边栏菜单——通过 Sidebar.json 配置。
- **[屏幕捕获检测](screen-capture.md)** — 在您的 iOS 应用中检测截图和屏幕录制，并从您的网页应用作出响应。
- **[MultiAPICall 功能](multi-api-call.md)** — 借助适用于 iOS 的 MultiAPICall 功能，在单个请求中串联多个 WebViewGold API 调用。
- **[NFC 插件](nfc.md)** — 在您的 iOS WebView 应用中原生读取 NFC 标签，并将标签数据传递给您的网页应用。
- **[Siri 插件](siri.md)** — 为您的 iOS WebView 应用添加 Siri 快捷指令支持，并通过语音打开应用内容。
- **[HealthKit 插件](healthkit.md)** — 将您的网页应用连接到 Apple HealthKit，并在 iOS 上经用户授权读取健康数据。

### 构建与发布

- **[构建与发布](publish.md)** — 将您的 WebView 应用发布到 Apple App Store：完整的发布服务、手动流程以及更改 bundle identifier。

### 更多

- **[鸣谢与许可](credits.md)** — WebViewGold for iOS 的许可条款、何时需要 Envato Extended License，以及开源鸣谢。
- **[为 WebViewGold 评分](rate.md)** — 喜欢 WebViewGold 吗？只需几秒即可在 CodeCanyon 上为它评分——这将持续推动更新。
- **[Android 和 macOS 版本](more-platforms.md)** — 将您的应用拓展到更多平台：获取适用于 Android 和 macOS 的 WebViewGold，复用同一个网页应用。
- **[支持与联系](support.md)** — 快速获取帮助：浏览 WebViewGold 支持中心，直接联系我们的团队，或申请德国制造的专业定制应用开发。

## 一个 Web 应用，覆盖所有平台

使用 WebViewGold，将同一个网站复用于 iOS、Android & macOS 应用。

- [WebViewGold for Android](../android/README.md)
- [WebViewGold for macOS](../macos/README.md)

**语言：** [🇺🇸 English](../../ios/README.md) · [🇩🇪 Deutsch](../../de/ios/README.md) · [🇫🇷 Français](../../fr/ios/README.md) · [🇪🇸 Español](../../es/ios/README.md) · **🇨🇳 中文**

> [!TIP]
> **太忙了？我们替您搭建应用。** 我们的团队为您配置、构建并提交 WebViewGold 应用——全程代劳、交付迅速、德国制造。 [让我们搭建应用 →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **在浏览器中构建：** 无需 Mac、无需 IDE：**WebViewGold Cloud Builder** 在线为您配置、构建并上传应用。 [了解 Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
