---
title: Content Credentials
description: 了解Adobe Journey Optimizer B2B Prime如何自动将Content Credentials应用于通过创作AI生成的图像，以及这对于您的内容意味着什么。
feature: Assets, Content
role: User
badgeBeta: label="Beta 版" type="informative" tooltip="此功能属于有限测试版。"
autotag-review: '2026-07-31T22:31:06.899Z'
TQID: 'https://experienceleague.adobe.com/fBPnAmupve3xMSw5fZPQBDTUfr-rwiH2-R3wbKvox-E'
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2:
  - id: a65c8aea-b21a-41ce-9ed7-6b517a69fd0b
  - id: e666e996-b2cf-4c45-8fc2-1c625212abab
  - id: aed878b8-11d0-487c-828b-d23b2051ec37
subfeature_v2:
  - id: d270a788-eb1d-40ed-b74e-9158ed975b1f
  - id: c8402946-ff35-44c5-ab98-74c1bba0975f
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: ad794b50f6c6f3b59e853e99f7983136ee098e18
workflow-type: tm+mt
source-wordcount: 560
ht-degree: 0%

---

# Content Credentials

营销机构比以往任何时候都更关注内容透明度、人工智能披露，以及防止资产被篡改。 Adobe的Content Authenticity Initiative (CAI)构建符合[内容来源和授权联盟](https://c2pa.org/specifications/specifications/1.1/specs/C2PA_Specification.html#_trust_model) (C2PA)技术标准的工具。 _Content Credentials_，加密且易于篡改的元数据，可以帮助查看者了解内容的历程并确保品牌资产的完整性。 此信息包括：

* 发行者或签名者 — 关于发行数字签名以证明或签署资产的实体或公司的信息。
* 问题日期 — 将Content Credential应用于资源的日期。
* 信用和使用 — 有关资产制作者的信息，包括名称、社交媒体句柄或其他身份相关信息。
* 进程 — 对资产进行任何编辑或修改的记录。
* 设备详细信息 — 有关用于创建或编辑资产的应用程序或设备的信息。
* 使用的AI工具 — 如果使用创作AI创建资产，则可能会包含所使用的模型的名称。
* 其他相关信息 — 还可以包含其他数据，以帮助提供有关资产历史的详细信息。

有关资产历史记录的全面信息，您可以使用Adobe Content Authenticity [检查工具](https://contentauthenticity.adobe.com/inspect)。

Content Credentials会与图像文件一起保留。 使用创作AI生成或编辑的图像上传到[!DNL Adobe Journey Optimizer B2B Prime]或从导出时，其Content Credentials将保留。

>[!NOTE]
>
>将图像导入内容的某些方法(例如从PDF或从嵌入的(base64)源中提取图像)可能无法保留原始Content Credentials。 在这些情况下，无法从源中读取Content Credentials，并且不会为结果创建任何内容。

>[!BEGINSHADEBOX]

## Content Credentials通过渠道持续性 {#channels}

当您将图像包含在电子邮件或WhatsApp消息中时，将会保留已投放图像的Content Credentials：

* **电子邮件** — 当您使用&#x200B;_发送电子邮件_&#x200B;历程操作时，请将该图像从&#x200B;_Assets_&#x200B;库添加到您的电子邮件内容。 在发送电子邮件时，收件人可以从邮件中下载图像，并且Content Credentials是完整的。
* **WhatsApp** — 将图像添加到Meta业务帐户的WhatsApp消息模板中。 您可以直接从自己的系统添加该文件，或从&#x200B;_Assets_&#x200B;库下载图像文件。 使用此模板进行&#x200B;_发送WhatsApp_&#x200B;历程操作。 在传递WhatsApp消息时，收件人可以从消息中下载图像，并且Content Credentials是完整的。

>[!ENDSHADEBOX]

## 图像生成 {#generate}

>[!INFO]
>
>围绕创新型人工智能透明度的新法律正在出现，Adobe正在努力满足跨司法辖区的适用要求。 Content Credentials是Adobe用于满足这些法律要求的来源工具。

当您使用创作AI在[!DNL Journey Optimizer B2B Prime]中为您的电子邮件内容创建图像时，Content Credentials会自动附加到生成的图像，您无需执行任何操作。 创作AI工具为具有现有凭据（包括原始源）的图像变体生成组合的Content Credentials元素。

>[!NOTE]
>
>[!DNL Journey Optimizer B2B Prime]当前不支持手动图像编辑操作。 用于这些操作的Content Credentials工作流目前不适用。
