---
title: "推送通知 API（OneSignal、Firebase、Pushwoosh） – WebViewGold for Android 文档"
description: "通过 OneSignal、Firebase 或 Pushwoosh 向您的 Android 应用用户发送推送通知——详解设置、深度链接和按用户定向。"
lang: "zh"
product: "WebViewGold for Android"
platform: "Android"
category: "API 与功能"
slug: "push-notifications"
canonical_url: "https://www.webviewgold.com/zh/docs/android/push-notifications/"
keywords:
  - "推送通知 API"
  - "WebViewGold for Android"
  - "将网站转换为应用"
  - "WebView 应用文档"
  - "Android WebView SDK"
  - "PWA 转应用"
  - "HTML 转应用"
  - "JavaScript 桥接"
last_updated: "2026-10-09"
---

# 推送通知 API（OneSignal、Firebase、Pushwoosh） – WebViewGold for Android

> **摘要：** 通过 OneSignal、Firebase 或 Pushwoosh 向您的 Android 应用用户发送推送通知——详解设置、深度链接和按用户定向。

[文档](../README.md) › [WebViewGold for Android](README.md) › 推送通知 API

**平台：** Android · **类别：** API 与功能 · **在线版本：** [www.webviewgold.com/zh/docs/android/push-notifications/](https://www.webviewgold.com/zh/docs/android/push-notifications/)

---

推送通知是无需打开应用就能在您的智能手机上显示的通知。此类消息可实现与客户和应用用户的绝佳互动。您的应用无需处于打开状态。这样，您的客户就不会错过任何重要的新闻或消息。推送通知适用于多种场景，例如订单更新、实时动态或社交媒体社区。应用用户必须联网才能接收推送消息。WebViewGold 支持通过多种方式向您的用户发送推送通知。

## 方案 1：使用本地推送通知的 JavaScript API

您可以在网站中插入一段代码（JavaScript）来定义一条推送通知，该通知可以在您的应用**关闭之后**显示（在应用打开时进行计划安排）。此方式完全不需要 OneSignal 配置。

```html
<script>
var title = "Your cart is waiting!"; //notification title
var message = "You have left a cart full of dreams and deals behind. Dont leave it feeling abandoned"; //notification message
var seconds = 120; //seconds from now on
var url = "https://myshop.org/cart.php"; //deep-linking URL

window.location.href = "sendlocalpushmsg://push.send?s="+ seconds +"=msg!"+ message +"&!#"+ title +"&!#"+ url +"";
</script>
```

此功能可用于多种情境（倒计时、欢乐时光（如示例代码中所示）、提醒等）。\
要取消所有已计划的本地推送通知，请运行：

```html
<script>
window.location.href = "sendlocalpushmsg://push.send.cancel";
</script>
```

## 方案 2：使用 Pushwoosh 远程推送通知

**WebViewGold 用户可享受两个月免费的 Pushwoosh 服务！**\
要享受此优惠，请将您的 WebViewGold 许可证发送电子邮件至 [pushwoosh-love@webviewgold.com](mailto:pushwoosh-love@webviewgold.com)，稍后您将收到专属回复。

如果您希望在应用中使用 [Pushwoosh](https://www.pushwoosh.com)（这是不错的选择！）来发送推送通知，只需在 **Config.java** 中启用相应选项，将 **PUSHWOOSH_ENABLED** 设置为 **true**，并确保将 **string.xml** 和 **AndroidManifest.xml** 文件中的 **Pushwoosh ID** 更新为您自己的 Pushwoosh ID：\
![使用 Pushwoosh 向您的应用用户发送新的推送通知](../../assets/android/img/pushwoosh1.webp)\
![使用 Pushwoosh 向您的应用用户发送新的推送通知](../../assets/android/img/pushwoosh2a.webp)\
![使用 Pushwoosh 向您的应用用户发送新的推送通知](../../assets/android/img/pushwoosh2b.webp)

恭喜，您已完成设置。现在可以发送推送通知了：\
[![使用 Pushwoosh 向您的应用用户发送新的推送通知](../../assets/android/img/pushwoosh3.webp)](https://www.pushwoosh.com)\
想要获取**每位用户的独立设备 ID**，用于个性化推送通知或进一步处理？只需在 **Config.java** 中将 **WONDERPUSH_ENHANCE_WEBVIEW_URL** 设置为 **true**，即可在您的 WebView URL 后附加 ?pushwoosh_id=XYZ：\
![使用 Pushwoosh 向您的应用用户发送新的推送通知](../../assets/android/img/pushwoosh4.webp)\
例如，如果您的 WebView URL 为 https://www.example.org，WebViewGold 将改为调用 https://www.example.org?pushwoosh_id=XYZ。请注意，只有首次 URL 请求会接收该 GET 变量，请将其保存在 session 或 cookie 中，以便在关联页面中稍后使用。作为替代或补充方案，您可以**在任意页面通过 JavaScript 获取并处理此信息**：

```html
<script>
window.location.href = "getpushwooshid://";
alert(pushwooshplayerid);
</script>
```

## 方案 3：使用 OneSignal 远程推送通知

如果您希望使用 OneSignal 来配置远程推送通知，此视频教程将引导您逐步完成整个过程。

[![观看视频: 推送通知 API（OneSignal、Firebase、Pushwoosh）](https://img.youtube.com/vi/0cPNGqMQVm0/hqdefault.jpg)](https://www.youtube.com/watch?v=0cPNGqMQVm0)

完成本视频教程后，您将能够轻松使用 OneSignal 为您的移动应用设置远程推送通知。这将使您能够将重要的更新、提醒或推广内容直接发送到用户的设备，即使他们当前未在使用您的应用。

总结一下，OneSignal 推送通知的配置流程如下：

1. 前往 Android Studio 并找到 OneSignal 选项。默认情况下，PUSH_ENABLE、PUSH_ENHANCE_WEBVIEW_URL 和 PUSH_RELOAD_ON_USERID 显示为 false，请将其设置为 true。
2. 登录您的 OneSignal 账户，选择您的组织和应用名称。

***如果您尚未在 OneSignal 项目中创建您的应用，请先按照以下步骤操作。***

[![观看视频: 推送通知 API（OneSignal、Firebase、Pushwoosh）](https://img.youtube.com/vi/X9jepbGFw7A/hqdefault.jpg)](https://www.youtube.com/watch?v=X9jepbGFw7A)

***请注意，创建和配置 OneSignal 账户时您需要一个 JSON 文件。要获取此文件，您必须已配置好 Firebase 账户。如果您尚未配置 Firebase 以获取该 JSON 文件，请查看此附加教程。***

[![观看视频: 推送通知 API（OneSignal、Firebase、Pushwoosh）](https://img.youtube.com/vi/qAqdhcd3ngs/hqdefault.jpg)](https://www.youtube.com/watch?v=qAqdhcd3ngs)

- 创建 OneSignal 应用后，进入设置部分，选择 Native Android 作为平台，然后复制获取到的 App ID 代码。
- 打开 Android Studio，进入 Gradle Scripts 部分，并选择 build.gradle (Module:app)。
- 在 ONE_SIGNAL_APP_ID 部分，粘贴您从 OneSignal 复制的代码。
- 然后，生成您的 *APK* 文件并在实体设备上运行。
- 前往 OneSignal，在您的应用项目中选择 *New Message*，然后点击 *New Push*。
- 填写所需信息即可完成！您已成功测试 OneSignal 推送消息。

替换 **ic_stat_onesignal_default.png** 以替换 OneSignal 推送通知的**默认铃铛后备图标**。\
是否希望在您的服务器上获取**每个用户的订阅 ID**，以便进一步处理并向**<a id="firebaseruntime"></a>单个用户**发送推送消息？只需在 Config.java 中启用 **PUSH_ENHANCE_WEBVIEW_URL** 选项（将值从 false 切换为 true），即可在您的 WebView URL 后附加 ?onesignal_push_id=XYZ。如果您的 WebView URL 为 https://www.example.org，WebViewGold 将改为调用 https://www.example.org?onesignal_push_id=XYZ。仅您的首次 URL 请求会获得该 GET 变量，因此请将其保存在 session 或 cookie 中，以便在关联页面中访问它。另一种或额外的方式是**在任意页面通过 JavaScript 获取并处理该信息**：

```html
<script>
window.location.href = "getonesignalplayerid://";
alert(onesignalplayerid);
</script>
```

**或者，考虑在 Config.java 中将  `AUTO_INJECT_VARIABLES`  设置为 `true`，以便自动将此值（以及其他值）注入到 JavaScript 中，无需事先调用 URL。**

## 方案 4：使用 Firebase 远程推送通知

如果您希望使用 Firebase 来配置远程推送通知，此视频教程将引导您逐步完成整个过程。

[![观看视频: 推送通知 API（OneSignal、Firebase、Pushwoosh）](https://img.youtube.com/vi/X-02iJSBaAQ/hqdefault.jpg)](https://www.youtube.com/watch?v=X-02iJSBaAQ)

总结一下，Firebase 推送通知的配置流程如下：

### 1. 重命名包名并创建 Firebase 项目

请[重命名](publish.md#renamepackagename)您的 WebViewGold Android 应用的包名。然后，您需要在 [Firebase Console](https://console.firebase.google.com/) 中创建一个 Firebase 项目。

### 2. 在 WebViewGold 中启用 Firebase

在 Android Studio 中，打开 Config.java 文件，并将 **FIREBASE_PUSH_ENABLED** 变量设置为 **true**。

![替换您的 WebViewGold Android 应用中的 google-services.json](../../assets/android/img/firebase2.webp)

### 3. 将您的应用注册到 Firebase

创建好 Firebase 项目后，您可以将 WebViewGold 应用添加到其中。

a. 在 Firebase 控制台项目概览页面中央，点击 Android 图标以启动设置向导。

b. 如果您已经向 Firebase 项目添加过应用，请点击**添加应用**以显示平台选项。
输入您在[此步骤](publish.md)中修改/定义的应用包名。
请确保输入的是您的应用实际使用的包名。在向 Firebase 项目注册应用后，您将无法再添加或修改此值。\
**4. 点击*注册应用*按钮。**
**5. 下载 google-services.json**
点击"下载 google-services.json"以获取您的 Firebase Android 配置文件 (google-services.json)，并使用 Mac 的 Finder 或 Windows 资源管理器替换 WebViewGold 项目中已包含的示例文件：\
![替换您的 WebViewGold Android 应用中的 google-services.json](../../assets/android/img/firebase1.webp)\
 **就是这样！**\
如果您希望使用 Firebase URL 深度链接（点击通知时打开特定 URL），请在 **Custom Data** 字段（位于 **Additional options (optional)** 部分）中添加所需的 URL，**Key** = "url"，**Value** = {所需 URL}。\
![在 WebView 中为深度链接添加自定义 URL](../../assets/android/img/firebase_deeplinking.webp)\
是否希望在您的服务器上获取**每个用户的订阅 ID**，以便进一步处理并向**单个用户**发送推送消息？只需在 Config.java 中启用 **FIREBASE_PUSH_ENHANCE_WEBVIEW_URL** 选项（将值从 false 切换为 true），即可在您的 WebView URL 后附加 ?firebase_push_id=XYZ。如果您的 WebView URL 为 https://www.example.org，WebViewGold 将改为调用 https://www.example.org?firebase_push_id=XYZ。仅您的首次 URL 请求会获得该 GET 变量，因此请将其保存在 session 或 cookie 中，以便在关联页面中访问它。另一种或额外的方式是**在任意页面通过 JavaScript 获取并处理该信息**：

```html
<script>
window.location.href = "getfirebaseplayerid://";
alert(firebaseplayerid);
</script>
```

**或者，考虑在 Config.java 中将  `AUTO_INJECT_VARIABLES`  设置为 `true`，以便自动将此值（以及其他值）注入到 JavaScript 中，无需事先调用 URL。**

## 方案 5：使用 bubble.io 推送通知

[![观看视频: 推送通知 API（OneSignal、Firebase、Pushwoosh）](https://img.youtube.com/vi/C0HBXlMSK2E/hqdefault.jpg)](https://www.youtube.com/watch?v=C0HBXlMSK2E)

1. 创建一个 **bubble.io 应用**
2. 安装 **[WebViewGold OneSignal Push](https://bubble.io/plugin/webviewgold-onesignal-push-1602240916803x713805488222896100)** 插件：

[![bubble.io WebViewGold OneSignal Push 插件](../../assets/android/img/bubblepushplugin-2048x724.webp)](https://bubble.io/plugin/webviewgold-onesignal-push-1602240916803x713805488222896100)
3. 按照 **OneSignal 说明（见上文）**和**插件说明（见[此处](https://bubble.io/plugin/webviewgold-onesignal-push-1602240916803x713805488222896100)和[此处](https://www.youtube.com/watch?v=C0HBXlMSK2E)）**操作。

---

## 推送权限 API：在合适的时机询问并检查当前状态

### 手动请求推送通知权限（`registerpush://`）

默认情况下，WebViewGold 会在应用首次启动时向用户请求推送通知权限（**Config.java** 中 `requirePush = true`）。权限请求出现在合适的场景中时，同意率会高得多 — 因此您也可以将 `requirePush` 设置为 `false`，并在最佳时机（例如登录或引导流程之后）从 Web 应用触发原生权限对话框：

```html
<a href="registerpush://">启用通知</a>
```

```javascript
window.location.href = "registerpush://";
```

**注意：**这要求在 **Config.java** 中至少激活一个推送服务（`PUSH_ENABLED`、`FIREBASE_PUSH_ENABLED` 或 `PUSHWOOSH_ENABLED`）。

### 检查当前推送权限状态（`checkNativePushPermissions://`）

要了解用户当前是否允许推送通知，请调用：

```javascript
window.location.href = "checkNativePushPermissions://";
```

WebViewGold 随后会将 JavaScript 变量 `nativePushEnabled`（`true` 或 `false`）注入您的页面。在 Android 13 及更高版本上，系统通知设置和 `POST_NOTIFICATIONS` 运行时权限都必须已授予，该值才为 `true`。示例：

```html
<script>
window.location.href = "checkNativePushPermissions://";
setTimeout(function () {
    if (typeof nativePushEnabled !== "undefined" && nativePushEnabled) {
        console.log("推送通知已启用");
    } else {
        // 例如显示您自己的提示，并提供 registerpush:// 或 settingsapp://
    }
}, 500);
</script>
```

如果权限已被永久拒绝，您可以通过 [Open App Settings API](open-app-settings.md)（`settingsapp://`）引导用户前往系统设置。

---

## 继续阅读

- ← 上一页： [地理定位 API](geolocation.md)
- 下一页 →： [AdMob 广告 API](admob.md)
- 其他平台上的相同功能： [iOS – 推送通知 API](../ios/push-notifications.md)
- 语言： [🇺🇸 English](../../android/push-notifications.md) · [🇩🇪 Deutsch](../../de/android/push-notifications.md) · [🇫🇷 Français](../../fr/android/push-notifications.md) · [🇪🇸 Español](../../es/android/push-notifications.md) · **🇨🇳 中文**

> [!TIP]
> **太忙了？我们替您搭建应用。** 我们的团队为您配置、构建并提交 WebViewGold 应用——全程代劳、交付迅速、德国制造。 [让我们搭建应用 →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_android_doc_online)
>
> **在浏览器中构建：** 无需 Mac、无需 IDE：**WebViewGold Cloud Builder** 在线为您配置、构建并上传应用。 [了解 Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=android_docs)
