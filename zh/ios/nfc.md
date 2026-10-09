---
title: "NFC 插件 – WebViewGold for iOS 文档"
description: "在您的 iOS WebView 应用中原生读取 NFC 标签，并将标签数据传递给您的网页应用。"
lang: "zh"
product: "WebViewGold for iOS"
platform: "iOS"
category: "扩展与插件"
slug: "nfc"
canonical_url: "https://www.webviewgold.com/zh/docs/iOS/nfc/"
keywords:
  - "NFC 插件"
  - "WebViewGold for iOS"
  - "将网站转换为应用"
  - "WebView 应用文档"
  - "iOS WebView SDK"
  - "PWA 转应用"
  - "HTML 转应用"
  - "JavaScript 桥接"
last_updated: "2026-10-09"
---

# NFC 插件 – WebViewGold for iOS

> **摘要：** 在您的 iOS WebView 应用中原生读取 NFC 标签，并将标签数据传递给您的网页应用。

[文档](../README.md) › [WebViewGold for iOS](README.md) › NFC 插件

**平台：** iOS · **类别：** 扩展与插件 · **在线版本：** [www.webviewgold.com/zh/docs/iOS/nfc/](https://www.webviewgold.com/zh/docs/iOS/nfc/)

---

**近场通信（NFC）**技术是最新技术之一，已在移动用户中变得非常流行。它使两台设备，或一台设备与一个 NFC 标签能够在近距离时进行无线通信。NFC 在 iOS 设备上被广泛用于读取和写入少量数据，是通过支持 NFC 的卡片或标签共享信息的有效工具。

NFC API 允许开发者直接从应用代码向 NFC 标签读取和写入数据。这为应用与用户的互动开辟了新方式，从共享联系人信息到嵌入文本片段。

## WebViewGold NFC 插件集成

虽然 NFC 不属于 WebViewGold 的常规功能范围，但我们可以根据具体需求提供定制、简便的 WebViewGold NFC 插件集成（通过 JavaScript）。

请通过电子邮件将您的需求（例如，向 NFC 标签写入/读取文本片段和/或联系人名片详情）发送至 [webviewgold-nfc@onlineappcreator.com](mailto:webviewgold-nfc@onlineappcreator.com)，以获取免费咨询和无约束力的报价。

**写入**\
要向 NFC 标签写入值，请从您的 Web 应用发送命令，加载以下 URL：`writenfc://?value=data`\
示例：\
`<a href="writenfc://?value=WebViewGold.com"> Write to an NFC tag </a>`\
这会使您的应用进入写入模式，并存储该值，直到扫描到标签为止。

**写入 VCARD**\
使用与写入纯文本相同的 API。按如下格式编排文本：

```
VCARD
FN:John Doe
Title:Developer
TEL;TYPE=CELL:0452641211
_
_
_
```

各属性之间用下划线（`_`）分隔，并在文本前加上 `VCARD_` 前缀。支持的属性列表请参见 <https://en.wikipedia.org/wiki/VCard#Properties>。

**读取**\
要读取 NFC 标签，请加载 `readnfc://`。应用会通过调用 `readNFCResult(data, id, tag)` 将信息返回给您的 Web 应用，其中 `data` 是存储的值，`id` 是标签标识符，`tag` 是标签类型。请在您的 Web 应用中定义此 JavaScript 函数以处理这些值。

## 如何测试该 API

1. 打开您应用代码库中的 Config 文件。
2. 输入您的购买代码。
3. 将应用的 URL 设置为 NFC API 测试页面：<https://webviewgoldtest.github.io/NFCtesting.html>
4. 运行应用。
5. 按下“读取”或“写入”选项之一以启用相应模式。如果是写入，请输入一个值。
6. 将 NFC 标签靠近设备以完成读取或写入操作。测试页面和应用将显示结果。

---

## 继续阅读

- ← 上一页： [MultiAPICall 功能](multi-api-call.md)
- 下一页 →： [Siri 插件](siri.md)
- 其他平台上的相同功能： [Android – NFC 插件](../android/nfc.md)
- 语言： [🇺🇸 English](../../ios/nfc.md) · [🇩🇪 Deutsch](../../de/ios/nfc.md) · [🇫🇷 Français](../../fr/ios/nfc.md) · [🇪🇸 Español](../../es/ios/nfc.md) · **🇨🇳 中文**

> [!TIP]
> **太忙了？我们替您搭建应用。** 我们的团队为您配置、构建并提交 WebViewGold 应用——全程代劳、交付迅速、德国制造。 [让我们搭建应用 →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_ios_doc_online)
>
> **在浏览器中构建：** 无需 Mac、无需 IDE：**WebViewGold Cloud Builder** 在线为您配置、构建并上传应用。 [了解 Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=ios_docs)
