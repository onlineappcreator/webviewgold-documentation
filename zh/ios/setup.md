---
title: "为 iOS 设置并配置 WebViewGold – WebViewGold for iOS 文档"
description: "下载 WebViewGold 的 Xcode 模板，在 Config.swift 中填入您的 URL，并探索所有内置配置选项——无需任何编程技能。"
lang: "zh"
product: "WebViewGold for iOS"
platform: "iOS"
category: "快速开始"
slug: "setup"
canonical_url: "https://www.webviewgold.com/zh/docs/iOS/setup/"
keywords:
  - "配置 WebViewGold"
  - "WebViewGold for iOS"
  - "将网站转换为应用"
  - "WebView 应用文档"
  - "iOS WebView SDK"
  - "PWA 转应用"
  - "HTML 转应用"
  - "JavaScript 桥接"
last_updated: "2026-10-09"
---

# 为 iOS 设置并配置 WebViewGold – WebViewGold for iOS

> **摘要：** 下载 WebViewGold 的 Xcode 模板，在 Config.swift 中填入您的 URL，并探索所有内置配置选项——无需任何编程技能。

[文档](../README.md) › [WebViewGold for iOS](README.md) › 配置 WebViewGold

**平台：** iOS · **类别：** 快速开始 · **在线版本：** [www.webviewgold.com/zh/docs/iOS/setup/](https://www.webviewgold.com/zh/docs/iOS/setup/)

---

**下载**适用于 iOS 的 WebViewGold 应用模板 **[点此下载](https://www.webviewgold.com/download/ios)**。\
[![购买适用于 iOS/Xcode 的 WebView 应用模板](../../assets/ios/img/cart.webp)](https://www.webviewgold.com/download/ios)

> [!NOTE]
> 希望避免安装任何软件吗？[**WebViewGold Cloud Builder**](https://www.webviewgold.com/cloud-builder?ref=ios_docs)（付费附加组件）让您无需打开 Xcode，即可直接在浏览器中配置、构建并上传您的应用。
>
> [![观看视频: 为 iOS 设置并配置 WebViewGold](https://img.youtube.com/vi/nzgCkydN9OM/hqdefault.jpg)](https://www.youtube.com/watch?v=nzgCkydN9OM)

从 CodeCanyon 下载 WebViewGold 的 .zip 文件后，Xcode 有**两种设置方案**可供选择。您应采用哪种方案，取决于您是否拥有 Mac 系统：

**a) 您没有使用任何 Mac 系统：**\
如果您没有可运行 Xcode 应用的 Mac，可以查看 [MacInCloud](https://www.macincloud.com)，它允许您在线租用虚拟 Mac（我们与该服务提供商没有任何关联）。借助该服务，即使没有 Mac，您也可以构建基于 WebViewGold 的 iOS 应用。此外，[**WebViewGold Cloud Builder**](https://www.webviewgold.com/cloud-builder?ref=ios_docs)（付费附加组件）让您无需 Mac，即可直接在浏览器中配置、构建并上传您的应用。\
**或**\
**b) 您使用的是 Mac 系统：**\
请从 [**Mac App Store**](https://apps.apple.com/de/app/xcode/id497799835?mt=12) 下载并安装 **Xcode** 应用。WebViewGold 可在 Intel 和 Apple Silicon Mac 上原生运行，因此您可以直接使用标准 iOS 模拟器构建和测试您的应用。

**大功告成，Xcode 已为 WebViewGold 做好准备！**\
如果 Xcode 已经在运行，请完全退出（*Command/CMD* + *Q*）。然后请打开 **WebViewGold.xcworkspace**（而不是 WebView.xcodeproj）：\
![打开 Xcode 项目时请确保选择正确的 WebView 项目文件](../../assets/ios/img/file.webp)

在 [Xcode](https://developer.apple.com/xcode/) 中打开 **Config.swift**，您会看到如下所示的文档：\
![使用 Config.swift 配置文件即可轻松完成配置](../../assets/ios/img/Configswift-img.webp)\
您可以在此轻松设置您的应用。使用 WebViewGold 设置应用**非常简单**，无需任何编程知识。请务必在您发布的每个应用中，在 **purchasecode** 字段填写您的 [Envato/CodeCanyon 购买代码](https://help.market.envato.com/hc/en-us/articles/202822600-Where-Is-My-Purchase-Code-)。每个定制后的最终产品需要一份许可证。有关您在 CodeCanyon 购买的许可证信息：[https://codecanyon.net/licenses/standard](https://codecanyon.net/licenses/standard?ref=onlineappcreator)

请查看下面对所有内置配置选项的**概览**：

[![观看视频: 为 iOS 设置并配置 WebViewGold](https://img.youtube.com/vi/E4D-Q_FhEOM/hqdefault.jpg)](https://www.youtube.com/watch?v=E4D-Q_FhEOM)

| 设置项 | 值 | 说明 |
| --- | --- | --- |
| purchasecode | **必填值** | 请输入您的 Envato/CodeCanyon 购买代码 |
| app_admin_email | 可选 | 用于接收状态更新的电子邮件地址（保留默认值即可禁用） |
| host | **必填值** | 您的域名主机（例如，"example.org"）。默认情况下，WebViewGold for iOS 允许 HTTPS 和 HTTP 内容。但是，如果您希望通过仅启用 HTTPS 内容来增强应用安全性，可以选择[修改此设置](https://www.webviewgold.com/support-center/knowledgebase/how-to-prevent-non-https-connections-in-webviewgold-for-ios-removing-nsallowsarbitraryloadsinwebcontent-from-info-plist/)（也可以考虑使用 'blockfaultyandselfsignedhttpscerts' 选项） |
| webviewurl | **必填值** | 您完整的 WebView URL（例如，"example.org/app.html"），将被加载到 WebView 中。默认情况下，WebViewGold for iOS 允许 HTTPS 和 HTTP 内容。但是，如果您希望通过仅启用 HTTPS 内容来增强应用安全性，可以选择[修改此设置](https://www.webviewgold.com/support-center/knowledgebase/how-to-prevent-non-https-connections-in-webviewgold-for-ios-removing-nsallowsarbitraryloadsinwebcontent-from-info-plist/)（也可以考虑使用 'blockfaultyandselfsignedhttpscerts' 选项） |
| uselocalhtmlfolder | **true** 或 **false** | 设置为 *true* 以使用本地 "local-www/index.html" HTML 文件，而非远程 WebView URL（请确保不要在 local-www 中创建或使用子文件夹） |
| externalLinkHandlingOptions | **0**、**1** 或 **2** | 设置为 *0*，默认在应用内打开外部链接；或设置为 *2*，始终在其他浏览器（Safari）中打开；参见 [URL Handling API](url-handling.md) |
| specialLinkHandlingOptions | **0**、**1** 或 **2** | 设置为 *0*，在应用内打开特殊链接（例如 target="_blank"）；设置为 *1*，在新标签页（附加的应用内浏览器）中打开；或设置为 *2*，在其他浏览器（Safari）中打开 |
| safariwhitelist | 列表 | 在此添加应当**始终**在 Safari 中打开的域名，无论 **externalLinkHandlingOptions** 选项设置为何；要添加另一个域名，请按以下方式插入另一个主机：["alwaysopeninsafari.com", "google.com", "m.facebook.com"]。请按您使用链接的方式准确输入主机（可带或不带 www，但始终不带 http/https）。 |
| safariblacklist | 列表 | 在此添加**永远不应**在 Safari 中打开的域名，无论 **externalLinkHandlingOptions** 选项设置为何；要添加另一个域名，请按以下方式插入另一个主机：["alwaysopeninsafari.com", "google.com", "m.facebook.com"]。请按您使用链接的方式准确输入主机（可带或不带 www，但始终不带 http/https）。 |
| alwaysOpenInInAppTab | 列表 | 在此添加应**始终**在应用内标签页中打开的域名，不受 **externalLinkHandlingOptions** 选项设置的影响 |
| neverOpenInInAppTab | 列表 | 在此添加**永远不**应在应用内标签页中打开的域名，不受 **externalLinkHandlingOptions** 选项设置的影响 |
| enableBioMetricAuth | **true** 或 **false** | 设置为 *true* 以启用我们的应用锁功能，该功能要求使用 Face ID、Touch ID 或密码对应用进行身份验证。这是一项独立且额外的选项，与我们基于 JavaScript 的[生物识别身份验证 API](biometric-authentication.md) 相互补充 |
| autoInjectVariable | **true** 或 **false** | 设置为 *true* 以自动加载 JavaScript 变量（例如 UUID、应用版本、OneSignal 和 Firebase 订阅 ID 以及 App Store 所在地区），无需调用特定的 URL（如 get-uuid://）。（目前支持应用版本、OneSignal 和 Firebase 订阅 ID、UUID 以及 App Store 所在地区。） |
| disablecallout | **true** 或 **false** | 设置为 *true*，移除 WKWebView 针对链接的 3D Touch 链接预览/呼出窗口（大多数情况下推荐启用） |
| deletecache | **true** 或 **false** | 设置为 *true*，每次应用启动时清除 WebView 缓存和 Cookie，不使用您 Web 应用/网站的缓存版本 |
| deletecacheonexit | **true** 或 **false** | 设置为 *true*，在完全退出应用时清除 WebView 缓存和 Cookie（您可能还需要激活 *deletecache*，因为不同 iOS 版本之间的差异可能会影响可靠性） |
| okbutton | 可选 | 设置 "OK" 按钮的文本标签（可通过 *alternatelanguage1*/*alternatelanguage2* 进行翻译） |
| cancelbutton | 可选 | 设置 "取消" 按钮的文本标签（可通过 *alternatelanguage1*/*alternatelanguage2* 进行翻译） |
| bigstatusbar | **true** 或 **false** | 设置为 *true* 以增大状态栏的尺寸 |
| hideverticalscrollbar | **true** 或 **false** | 设置为 *true* 以隐藏垂直滚动条 |
| hidehorizontalscrollbar | **true** 或 **false** | 设置为 *true* 以隐藏水平滚动条 |
| enableswipenavigation | **true** 或 **false** | 设置为 *false*，防止向左/向右滑动触发后退/前进导航 |
| orientationiphone | "portrait"、"landscape" 或 "auto" | 将 iPhone 上的方向设置为 portrait、landscape 或 auto |
| orientationipad | "portrait"、"landscape" 或 "auto" | 将 iPad 上的方向设置为 portrait、landscape 或 auto |
| preventsleep | **true** 或 **false** | 设置为 *true*，在应用处于活动状态时防止设备进入睡眠状态 |
| preventZoom | **true** 或 **false** | 设置为 *true*，通过注入代码防止在网站上进行缩放，从而禁用用户缩放 |
| preventoverscroll | **true** 或 **false** | 设置为 *true* 以移除 WKWebView 的回弹动画（大多数情况下推荐启用）。如需使用下拉刷新，请设置为 *false*。 |
| enhanceUrlUUID | **true** 或 **false** | 设置为 *true*，在首个 URL 请求中附加 UUID 参数 'uuid=XYZ' |
| linkDragAndDrop | **true** 或 **false** | 设置为 *false* 以禁用链接的拖放 |
| useShortcuts | **true** 或 **false** | 设置为 *true*，注册在 Shortcuts.json 中定义的动态快捷方式 |
| pulltorefresh | **true** 或 **false** | 设置为 *true*，在您的应用中启用下拉刷新。请注意，要启用此功能，**preventoverscroll** 需要设置为 *false*。此外，您可以随时从网站调用 `enablepulltorefresh://` 或 `disablepulltorefresh://`，以动态激活或停用下拉刷新。 |
| pulltorefresh_loadingsigncolour_lightmode | 颜色 | 设置浅色模式下下拉刷新加载指示器的颜色 |
| pulltorefresh_backgroundcolour_lightmode | 颜色 | 设置浅色模式下下拉刷新背景的颜色 |
| pulltorefresh_loadingsigncolour_darkmode | 颜色 | 设置深色模式下下拉刷新加载指示器的颜色；需要 iOS 13 或更高版本 |
| pulltorefresh_backgroundcolour_darkmode | 颜色 | 设置深色模式下下拉刷新背景的颜色；需要 iOS 13 或更高版本 |
| useragent_iphone | 可选 | 为 iPhone 定义自定义 UserAgent（或留空以使用默认的 iOS UserAgent） |
| useragent_ipad | 可选 | 为 iPad 定义自定义 UserAgent（或留空以使用默认的 iOS UserAgent） |
| google_login_helper_triggers | 可选 | 定义在网站进行 Google 登录时会加载的 URL 前缀；这些前缀将作为登录辅助工具的触发条件；示例：["https://accounts.google.com", "https://accounts.youtube.com"] |
| facebook_login_helper_triggers | 可选 | 定义在网站进行 Facebook 登录时会加载的 URL 前缀；这些前缀将作为登录辅助工具的触发条件；示例：["https://www.facebook.com", "https://m.facebook.com"] |
| activatefirstrundialog | **true** 或 **false** | 设置为 *true* 以激活 "首次运行" 对话框 |
| firstrunmessagetitle | 可选 | 设置 "首次运行" 对话框的标题文本（如有需要，您可以使用 Config.swift 文件末尾的 'alternatelanguage1' 和 'alternatelanguage2' 字符串将此字符串翻译为另外两种语言） |
| firstrunmessage | 可选 | 设置 "首次运行" 对话框的消息内容（如有需要，您可以使用 Config.swift 文件末尾的 'alternatelanguage1' 和 'alternatelanguage2' 字符串将此字符串翻译为另外两种语言） |
| askforpushpermissionatfirstrun | **true** 或 **false** | 设置为 *true*，在应用首次运行时向用户请求推送通知权限。设置为 "false" 则永远不请求，或稍后通过您 Web 应用中的 *registerpush://* 链接/按钮/重定向来请求 |
| offlinetitle | 可选 | 设置离线对话框的标题文本（如有需要，您可以使用 Config.swift 文件末尾的 'alternatelanguage1' 和 'alternatelanguage2' 字符串将此字符串翻译为另外两种语言） |
| offlinemsg | 可选 | 设置离线对话框的文本内容（如有需要，您可以使用 Config.swift 文件末尾的 'alternatelanguage1' 和 'alternatelanguage2' 字符串将此字符串翻译为另外两种语言） |
| screen1 | 可选 | 设置离线界面的文本标签 1（如有需要，您可以使用 Config.swift 文件末尾的 'alternatelanguage1' 和 'alternatelanguage2' 字符串将此字符串翻译为另外两种语言） |
| screen2 | 可选 | 设置离线界面的文本标签 2（如有需要，您可以使用 Config.swift 文件末尾的 'alternatelanguage1' 和 'alternatelanguage2' 字符串将此字符串翻译为另外两种语言） |
| offlinebuttontext | 可选 | 设置 "重试" 按钮的文本标签（如有需要，您可以使用 Config.swift 文件末尾的 'alternatelanguage1' 和 'alternatelanguage2' 字符串将此字符串翻译为另外两种语言） |
| offlinescreenautoretry | **true** 或 **false** | 设置为 *true*，让应用每秒自动尝试重新连接（即使用户未点击按钮） |
| activateratemyappdialog | **true** 或 **false** | 设置为 *true* 以激活 "在 App Store 上为该应用评分" 对话框 |
| activatefacebookfriendsdialog | **true** 或 **false** | 设置为 *true* 以激活 "在 Facebook 上关注" 对话框 |
| becomefacebookfriendstitle | 可选 | 设置 "在 Facebook 上关注" 对话框的标题文本（如有需要，您可以使用 Config.swift 文件末尾的 'alternatelanguage1' 和 'alternatelanguage2' 字符串将此字符串翻译为另外两种语言） |
| becomefacebookfriendstext | 可选 | 设置 "在 Facebook 上关注" 对话框的文本内容（如有需要，您可以使用 Config.swift 文件末尾的 'alternatelanguage1' 和 'alternatelanguage2' 字符串将此字符串翻译为另外两种语言） |
| becomefacebookfriendsyes | 可选 | 设置 "在 Facebook 上关注" 对话框中 "是" 按钮的文本标签（如有需要，您可以使用 Config.swift 文件末尾的 'alternatelanguage1' 和 'alternatelanguage2' 字符串将此字符串翻译为另外两种语言） |
| becomefacebookfriendsno | 可选 | 设置 "在 Facebook 上关注" 对话框中 "否" 按钮的文本标签（如有需要，您可以使用 Config.swift 文件末尾的 'alternatelanguage1' 和 'alternatelanguage2' 字符串将此字符串翻译为另外两种语言） |
| becomefacebookfriendsurl | 可选 | 设置您 Facebook/Instagram/YouTube/… 页面的 URL（例如，"https://facebook.com/OnlineAppCreator/"） |
| imagedownloadedtitle | 可选 | 设置 "图片已保存至相册" 对话框的标题文本（如有需要，您可以使用 Config.swift 文件末尾的 'alternatelanguage1' 和 'alternatelanguage2' 字符串将此字符串翻译为另外两种语言） |
| imagenotfound | 可选 | 设置 "未找到图片" 对话框的标题文本（如有需要，您可以使用 Config.swift 文件末尾的 'alternatelanguage1' 和 'alternatelanguage2' 字符串将此字符串翻译为另外两种语言） |
| transparentStatusBar | **true** 或 **false** | 设置为 *true*，使状态栏透明，让 Web 内容可以显示在其后方 |
| autoAdjustSafeAreaInsets | **true** 或 **false** | 如果您的网站已自行处理安全区域内边距，请将此项设置为 *false*（与 *transparentStatusBar* 一起使用） |
| statusBarBackgroundColor | 颜色 | 定义自定义的状态栏背景色 |
| darkModeStatusBarBackgroundColor | 颜色 | 定义用户使用 iOS 深色模式时的自定义状态栏背景色 |
| statusBarTextColor | **white** 或 **black** | 定义状态栏的文字颜色 |
| darkModeStatusBarTextColor | **white** 或 **black** | 定义用户使用 iOS 深色模式时状态栏的文字颜色 |
| showNavFooter | **true** 或 **false** | 设置为 *true* 以启用原生导航页脚栏（通过 FooterBar.json 配置） |
| bottombar | **true** 或 **false** | 设置为 *true* 以启用底部栏，防止 Home 条（存在于无 Home 按钮的 iOS 设备上，例如 iPhone X）遮挡应用内容 |
| iPadBottombar | **true** 或 **false** | 设置为 *true*，同时在 iPad 上启用底部栏（由于 iPad 屏幕较大，布局不同，Home 条可能不会遮挡内容，因此可能不需要底部栏） |
| bottombarBackgroundColor | 颜色 | 定义底部栏的自定义背景色 |
| darkmodeBottombarBackgroundColor | 颜色 | 定义用户使用 iOS 深色模式时底部栏的自定义背景色；需要 iOS 13 或更高版本 |
| qrcodelinks | **0** 或 **1** 或 **2** 或 **3** 或 **4** | 设置为 (0) 在应用中打开扫描到的二维码 URL；(1) 在应用内标签页中打开；(2) 在新浏览器中打开；(3) 如为外部链接则在应用内标签页中打开；(4) 如为外部链接则在新浏览器中打开；此外，您还可以选择在 SwiftQRScanner.swift 文件的 "allowedQRurls" 数组中限制允许的二维码扫描前缀 |
| ShowExternalLink | 可选 | 设置为 *true*，打开通过[通用链接 API](universal-links.md)（语法：https://example.org）和[深度链接 API](deep-linking.md)（语法：example://url?link=https://example.org）传递的链接。 |
| splashScreenEnabled | 可选 | 设置为 *false*，如果您希望在应用启动期间禁用启动画面并改为显示加载指示器 |
| remainSplashOption | 可选 | 设置为 *true*，如果您希望启动画面持续显示直到主页首次加载完成（而不是显示加载指示器） |
| splashTimeout | 数值（毫秒） | 以*毫秒*为单位设置启动画面超时时间（如果主页 URL 仍在加载中，加载指示界面将在此时间过后显示） |
| splashMinTime | 数值（毫秒） | 启动画面应显示的最短时间（毫秒）；设置为 *0* 可禁用最短显示时长 |
| splashFadeTime | 数值（毫秒） | 启动画面淡出动画的时长（毫秒）；设置为 *0* 可禁用淡出效果 |
| scaleSplashImage | 百分比值 [0-100] | 按设备的最小宽度/高度设置启动画面图片的尺寸；百分比范围 [0-100]；值 = 0 将完全隐藏该图片，值 = 100 将全屏显示该图片 |
| useLoadingSign | **true** 或 **false** | 设置为 *false*，在加载 URL 时隐藏加载指示器 |
| useLoadingProgressBar | **true** 或 **false** | 设置为 *true*，在加载 URL 时使用加载进度条（代替加载指示器） |
| loadingIndicatorColor | 颜色 | 为加载指示器设置颜色 |
| alternativeAppIconNames | 列表 | 编辑此列表以更改备用应用图标的文件名 |
| backgroundlocation | **true** 或 **false** | 设置为 *true* 以允许后台定位访问（此外，请确保 Xcode 项目设置中的 "Background Modes" 功能包含 "Location updates"。根据您的 Web 应用，您可能还需要启用 "Background Processing"；在这种情况下，还需在 Info.plist 文件中添加一个数组，键为 "Permitted background task scheduler identifiers"——在该数组下添加包含您应用 Bundle ID 的字符串，例如 "com.onlineappcreator.webviewgold"） |
| appendlanguage | **true** 或 **false** | 设置为 *true*，如果您希望在 URL 请求中附加系统语言，例如 ?webview_language=LANGUAGE CODE（如 ?webview_language=EN 对应英语用户） |
| blockfaultyandselfsignedhttpscerts | **true** 或 **false** | 设置为 *true*，阻止使用自签名 SSL（用户）证书和有问题的 SSL 证书签名的内容；也可以考虑[阻止所有非 HTTPS 内容](https://www.webviewgold.com/support-center/knowledgebase/how-to-prevent-non-https-connections-in-webviewgold-for-ios-removing-nsallowsarbitraryloadsinwebcontent-from-info-plist/) |
| jailbreakBlock | **true** 或 **false** | 设置为 *true*，在越狱/被破解的设备上阻止应用运行。注意：检测并非绝对可靠，但会采用多种方法来识别越狱和破解行为 |
| autoRefreshEnabled | **true** 或 **false** | 设置为 *true*，当应用从后台返回前台时，WebView 会自动刷新其内容。 |
| offlinelocalhtmlswitch | **true** 或 **false** | 设置为 *true*，当用户离线时使用 "local-html" 文件夹，当用户在线时使用远程 URL。 |
| extentionARY | 列表 | 添加应触发文件下载功能的文件格式（例如 .pdf、.docx 等） |
| autodownloader | **true** 或 **false** | 设置为 *true*，无论上面 extentionARY 变量中列出何种文件格式，都启用基于 Content-Disposition HTTP 头的下载功能 |
| splashscreencolor | 颜色 | 为启动画面设置背景色 |
| extentionARY | 列表 | 添加应触发文件下载功能的文件格式（例如 .pdf、.docx 等） |
| offlinelocalhtmlswitch | **true** 或 **false** | 设置为 *true*，当用户离线时使用 "local-html" 文件夹，当用户在线时使用远程 URL。 |
| zipfiledownloadfromserver | **true** 或 **false** | 设置为 *true*，从远程 URL 下载一个 .zip 存档，以便在用户离线时解压并显示（此外，请将 turnofflinelocalhtmlswitch 变量设置为 true）；每次完全重启应用时都会进行更新 |
| zipfileremoteurl | URL | 用户离线时应解压并显示的、来自远程 URL 的 .zip 存档 |
| zipfilename | 文件名 | 用户设备上 .zip 文件的内部文件名（建议不要更改） |
| zipfileextractpath | 文件夹名 | 用户设备上解压路径的内部文件夹名（建议不要更改） |
| zipfileextractindexindex | 文件名 | 解压后的 .zip 存档中应首先打开的文件 |
| zipfilepopuptitle | 文本 | 下载 .zip 文件期间将显示的弹窗标题（如有需要，您可以使用 Config.swift 文件末尾的 'alternatelanguage1' 和 'alternatelanguage2' 字符串将此字符串翻译为另外两种语言） |
| zipfilepopupmessage | 文本字符串 | 下载 .zip 文件期间将显示的弹窗消息（如有需要，您可以使用 Config.swift 文件末尾的 'alternatelanguage1' 和 'alternatelanguage2' 字符串将此字符串翻译为另外两种语言） |
| InAppPurchAppBundleIdentifier | 可选 | 设置默认应用标识符，以便为默认的 IAP 产品启用应用内购买 API（详细信息可在 App Store Connect 中配置） |
| IAPSharedSecret | 可选 | 设置 App Secret 以启用应用内购买 API（更多信息请参阅[此处](in-app-purchases.md)） |
| iapsuccessurl | 可选 | 设置通过 WebView 包装器完成成功的应用内购买/应用内订阅后应打开的默认 URL。例如，该 URL 可以是 "https://www.example.org/thanks.php"，其中 thanks.php 可以设置用于访问高级内容的持久 Cookie。 |
| iapexpiredurl | 可选 | 设置通过 WebView 包装器完成的应用内订阅到期后应打开的默认 URL。例如，该 URL 可以是 "https://www.example.org/expired.php"，其中 expired.php 可以删除用于访问高级内容的 Cookie |
| revenueCatAPIKey | 可选 | 您的 RevenueCat API 密钥（请先通过 [tinyurl.com/register-revenuecat](https://tinyurl.com/register-revenuecat) 注册，然后按照 [tinyurl.com/api-key-revenuecat](https://tinyurl.com/api-key-revenuecat) 的说明查找） |
| revenueCatProjectID | 可选 | 您的 RevenueCat 项目 ID（请先通过 [tinyurl.com/register-revenuecat](https://tinyurl.com/register-revenuecat) 注册，然后按照 [tinyurl.com/project-id-revenuecat](https://tinyurl.com/project-id-revenuecat) 的说明查找） |
| oneSignalID | 可选 | OneSignal 推送功能所必需 |
| kPushEnabled | **true** 或 **false** | 设置为 *true* 以启用 OneSignal 推送功能 |
| kPushEnhanceUrl | **true** 或 **false** | 设置为 *true*，如果您希望在 WebView 主 URL 请求中以 ?onesignal_push_id=XYZ 的形式附加 OneSignal 订阅 ID（此外，您也可以随时通过调用 [getonesignalplayerid://](push-notifications.md#onesignalruntime) 获取 OneSignal 订阅 ID，或将 Config.swift 中的 "autoInjectVariable" 设为 "true" 自动获取） |
| kPushReloadOnUserId | **true** 或 **false** | 设置为 *true*，在从 OneSignal 收到 UserID 后重新加载 WebView |
| kPushOpenDeeplinkInBrowser | **true** 或 **false** | 设置为 *true*，将来自 OneSignal 的深度链接 URL 在 Safari 浏览器中打开，而不是在主 WebView 中打开；重要提示：如需从 OneSignal 发送包含链接的通知，请**不要**使用 'Launch URL'，而必须使用 'Additional Data Field'，键为：url，值为您想使用的链接 |
| kFirebasePushEnabled | **true** 或 **false** | 设置为 *true* 以将您的应用连接到 Firebase 推送服务 |
| kFirebaseEnhanceUrl | **true** 或 **false** | 设置为 *true*，如果您希望在 WebView 主 URL 请求中附加 ?firebase_push_id=XYZ（此外，您也可以随时通过调用 [getfirebaseplayerid://](push-notifications.md#firebaseruntime) 获取 OneSignal 订阅 ID，或将 Config.swift 中的 "autoInjectVariable" 设为 "true" 自动获取） |
| firebaseTopic | **可选** | 设置要订阅的 Firebase Topic |
| kPushwooshEnable | **可选** | 设置为 *true* 以启用 Pushwoosh 推送功能（在 Info.plist 中的 Pushwoosh_APPID 列设置 ID） |
| kPushwooshEnhanceUrl | **可选** | 设置为 *true*，如果您希望在 WebView 主 URL 请求中附加 ?pushwoosh_id=XYZ |
| showBannerAd | **true** 或 **false** | 设置为 *true*，如果您希望展示 AdMob 横幅广告（请同时在 Config.swift 和 Info.plist 中设置 AdMob ID，请参阅[此处](admob.md)） |
| showFullScreenAd | **true** 或 **false** | 设置为 *true*，如果您希望在网站被点击 X 次后展示 AdMob 插页广告（请同时在 Config.swift 和 Info.plist 中设置 AdMob ID，请参阅[此处](admob.md)） |
| showadAfterX | 可选 | 定义数字 X，用于每 X 次（例如 10 次）网站点击或屏幕点击后显示一则 AdMob 插页广告，具体取决于 **incrementWithTaps** 的设置（请同时在 Config.swift 和 Info.plist 中设置 AdMob ID，请参阅[此处](admob.md)）。 |
| incrementWithTaps | **true** 或 **false** | 设置为 *true*，如果您希望在 X 次屏幕点击后显示插页广告；设置为 *false*，则在 X 次网站跳转后显示。 |
| enableRewardedAds | **true** 或 **false** | 设置为 *true* 以启用 AdMob 激励广告。即使是手动激活广告，也需要将此项设置为 *true*。 |
| useRewardedAdsWherePossible | **true** 或 **false** | 设置为 *true*，在原本应播放 AdMob 插页广告的场景（例如 X 次点击后）改为播放 AdMob 激励广告。如果希望通过您网站的代码来控制其激活，请保持为 *false*。要覆盖插页广告，还需将 showFullScreenAd 也设置为 *true*。 |
| admobadstriggerurls | 可选 | 在此添加页面触发词，URL 中出现这些词时将触发 AdMob 插页广告（例如，["see-highscore.php", "/thank-you/", "/next-step.html"]） |
| useFacebookAds | **true** 或 **false** | 设置为 *true* 以启用 Facebook 插页广告 |
| facebookAdsID | 可选 | 输入您的 Placement ID，可在 Facebook Monetization Manager 中创建资产并关联 iOS 应用后获取。该 ID 形如：3937960198956424_3969441893142587 |
| useTimedAds | **true** 或 **false** | 对 Facebook 广告使用定时广告（例如每 60 秒一次），而不是每 X 次点击一次 |
| fbadstriggerurls | 可选 | 在此添加页面触发词，URL 中出现这些词时将触发 Facebook 广告（例如，["see-highscore.php", "/thank-you/", "/next-step.html"]） |
| showFBAdsEveryNSeconds | 可选 | 每 X 秒显示一次 Facebook 插页广告；建议设置为 120 秒或以上 |
| ATTDeniedShowAds | **true** 或 **false** | 设置为 *false*，如果用户拒绝 AppTrackingTransparency (ATT) 权限，则完全停止显示广告 |
| useAdsenseAds | **true** 或 **false** | 设置为 *true* 以启用对 AdSense 网页广告的支持（独立于 AdMob 广告） |
| askForAdConsent | **true** 或 **false** | 设置为 *false*，如果您希望停用 AdMob 的 Google 同意管理（请事先查阅 <https://support.google.com/admob/answer/13554116>） |
| showBarcodeScanner | **true** 或 **false** | 设置为 *false*，阻止网站通过 `barcodescanner://` 请求开启条形码扫描器 |
| kFlashLightEnabled | **true** 或 **false** | 设置为 *false*，阻止网站通过 `enableflashlight://` 请求开启手电筒 |
| widgetRefreshTime | 数字 | 小组件的刷新间隔（分钟） |
| widgetfallbackURL | 字符串 | 小组件使用的备用图片 URL |
| preventScreenCapture | **true** 或 **false** | 设置为 *true*，当用户进行截屏或屏幕录制时在您的 Web 应用中调用 onScreenCaptureAttempt |
| kVisionKitEnable | **true** 或 **false** | 设置为 *true*，通过 [VisionKit 文档扫描仪](document-scanner.md)在文件上传对话框中添加扫描选项（需要 iOS 18.4 或更高版本） |
| enableSidebar | **true** 或 **false** | 设置为 *true* 可启用一个浮动按钮，用于打开[原生侧边栏](sidebar.md)，可在 **Sidebar.json** 中自定义 |
| showcustomrateappdialog | **true** 或 **false** | 设置为 *true*，在触发 [rateapp:// API](in-app-rating.md) 时显示自定义评分对话框，而不是尝试原生评分调用 |
| ratemyappurl | URL | 设置您应用的 App Store URL，供自定义评分对话框使用 |
| cookieonlaunch | **true** 或 **false** | 设置为 *true*，在 WebView 启动时添加 Cookie；可通过 **cookieonlaunchname**、**cookieonlaunchvalue** 和 **cookieonlaunchissecure** 变量进行配置 |
| useCustomHeaders | **true** 或 **false** | 设置为 *true*，随每个 WebView 请求发送在 **customHeaders** 字典中定义的自定义 HTTP 标头 |
| siriEnabled | 插件令牌 | 输入令牌以启用 Siri 插件功能 |
| NFCEnabled | 插件令牌 | 输入令牌以启用 NFC 插件功能 |
| HealthKitEnabled | 插件令牌 | 输入令牌以启用 HealthKit 插件功能 |
| alternatelanguage1_langcode（以及 _alternatelanguage1_ 字符串列表） | **true** 或 **false**（以及字符串列表） | 设置语言代码，或将此字符串留空以不使用备用语言 #1 的字符串（字符串列表位于 Config.swift 文件底部）；如果您希望激活此备用语言，请使用符合 ISO 639-1 语言代码标准的双字母代码（例如，"de" 表示德语，"fr" 表示法语，"it" 表示意大利语，"pt" 表示葡萄牙语，"ca" 表示加泰罗尼亚语，"es" 表示西班牙语，……） |
| alternatelanguage2_langcode（以及 _alternatelanguage2_ 字符串列表） | **true** 或 **false**（以及字符串列表） | 设置语言代码，或将此字符串留空以不使用备用语言 #2 的字符串（字符串列表位于 Config.swift 文件底部）；如果您希望激活此备用语言，请使用符合 ISO 639-1 语言代码标准的双字母代码（例如，"de" 表示德语，"fr" 表示法语，"it" 表示意大利语，"pt" 表示葡萄牙语，"ca" 表示加泰罗尼亚语，"es" 表示西班牙语，……） |

---

## 继续阅读

- ← 上一页： [设置网页应用](setup-website.md)
- 下一页 →： [名称、图标和启动屏](app-name-icon-splash.md)
- 其他平台上的相同功能： [Android – 配置 WebViewGold](../android/setup.md) · [macOS – 设置 WebViewGold](../macos/setup.md)
- 语言： [🇺🇸 English](../../ios/setup.md) · [🇩🇪 Deutsch](../../de/ios/setup.md) · [🇫🇷 Français](../../fr/ios/setup.md) · [🇪🇸 Español](../../es/ios/setup.md) · **🇨🇳 中文**

> [!TIP]
> **太忙了？我们替您搭建应用。** 我们的团队为您配置、构建并提交 WebViewGold 应用——全程代劳、交付迅速、德国制造。 [让我们搭建应用 →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **在浏览器中构建：** 无需 Mac、无需 IDE：**WebViewGold Cloud Builder** 在线为您配置、构建并上传应用。 [了解 Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
