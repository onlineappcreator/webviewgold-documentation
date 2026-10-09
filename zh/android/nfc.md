---
title: "NFC 插件 – WebViewGold for Android 文档"
description: "在您的 Android WebView 应用中以原生方式读取 NFC 标签，并将标签数据传递给您的 Web 应用。"
lang: "zh"
product: "WebViewGold for Android"
platform: "Android"
category: "API 与功能"
slug: "nfc"
canonical_url: "https://www.webviewgold.com/zh/docs/android/nfc/"
keywords:
  - "NFC 插件"
  - "WebViewGold for Android"
  - "将网站转换为应用"
  - "WebView 应用文档"
  - "Android WebView SDK"
  - "PWA 转应用"
  - "HTML 转应用"
  - "JavaScript 桥接"
last_updated: "2026-10-09"
---

# NFC 插件 – WebViewGold for Android

> **摘要：** 在您的 Android WebView 应用中以原生方式读取 NFC 标签，并将标签数据传递给您的 Web 应用。

[文档](../README.md) › [WebViewGold for Android](README.md) › NFC 插件

**平台：** Android · **类别：** API 与功能 · **在线版本：** [www.webviewgold.com/zh/docs/android/nfc/](https://www.webviewgold.com/zh/docs/android/nfc/)

---

**近场通信（NFC）**使两台设备，或一台设备与一个 NFC 标签，能够在近距离时进行无线通信。NFC 在 Android 设备上被广泛用于读取和写入少量数据，是通过支持 NFC 的卡片或标签共享信息的有效工具。

**WebViewGold NFC API** 让您的 Web 应用通过 JavaScript 桥接直接读写 NFC 标签 — 从共享联系人信息到嵌入文本片段。

**写入**\
要将一个值写入 NFC 标签，请在 Web 应用中加载以下 URL 发送命令：`writenfc://?value=data`\
示例：\
`<a href="writenfc://?value=WebViewGold.com"> 写入 NFC 标签 </a>`\
这会使应用进入写入模式并保存该值，直到扫描到标签：用户将 NFC 标签靠近设备后，该值即被写入标签。

**写入 VCARD（联系人名片）**\
使用与写入纯文本相同的 API，并按如下格式组织文本：

```
VCARD
FN:John Doe
Title:Developer
TEL;TYPE=CELL:0452641211
```

用下划线（`_`）分隔各属性，空格编码为 `%20`，并在文本前加上 `VCARD_` 前缀。示例：

```
writenfc://?value=VCARD_FN:John%20Doe_Title:Developer_TEL;TYPE=CELL:0452641211
```

支持的属性列表请参见 <https://en.wikipedia.org/wiki/VCard#Properties>。

**读取**\
要读取 NFC 标签，请加载 `readnfc://`。这会使应用进入读取模式。当用户扫描标签时，应用会调用 JavaScript 函数 `readNFCResult(data)` 将存储的信息返回给您的 Web 应用，其中 `data` 是标签上存储的值。请在您的 Web 应用中定义此 JavaScript 函数来处理该值：

```html
<script>
window.location.href = "readnfc://";

function readNFCResult(data) {
    alert("NFC 标签内容：" + data);
}
</script>
```

## 如何测试该 API

1. 打开应用代码库中的 Config 文件。
2. 输入您的购买码。
3. 将应用的 URL 设置为 NFC API 测试页面：<https://webviewgoldtest.github.io/NFCtesting.html>
4. 在支持 NFC 的实体设备上运行应用。
5. 点按读取或写入选项以启用相应模式。如需写入，请输入一个值。
6. 将 NFC 标签靠近设备以完成读取或写入操作。测试页面和应用将显示结果。

**需要更多功能？**如果您需要超出此 API 范围的扩展 NFC 功能（例如特殊标签类型或自定义数据格式），我们可根据具体情况提供定制的 NFC 插件集成。请将您的需求发送至 [webviewgold-nfc@onlineappcreator.com](mailto:webviewgold-nfc@onlineappcreator.com)，以获取免费咨询和无约束力的报价。

---

## 继续阅读

- ← 上一页： [触觉反馈 API](haptic-feedback.md)
- 下一页 →： [Open App Settings API](open-app-settings.md)
- 其他平台上的相同功能： [iOS – NFC 插件](../ios/nfc.md)
- 语言： [🇺🇸 English](../../android/nfc.md) · [🇩🇪 Deutsch](../../de/android/nfc.md) · [🇫🇷 Français](../../fr/android/nfc.md) · [🇪🇸 Español](../../es/android/nfc.md) · **🇨🇳 中文**

> [!TIP]
> **太忙了？我们替您搭建应用。** 我们的团队为您配置、构建并提交 WebViewGold 应用——全程代劳、交付迅速、德国制造。 [让我们搭建应用 →](https://www.WeSetupYourWebViewApp.com?ref=webviewgold_android_doc_online)
>
> **在浏览器中构建：** 无需 Mac、无需 IDE：**WebViewGold Cloud Builder** 在线为您配置、构建并上传应用。 [了解 Cloud Builder →](https://www.webviewgold.com/cloud-builder?ref=android_docs)
