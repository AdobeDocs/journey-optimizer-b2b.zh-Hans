---
title: 使用GenStudio for Performance Marketing创建电子邮件内容
description: 将GenStudio for Performance Marketing与Journey Optimizer B2B edition集成 — 导出HTML、创建支持AI的电子邮件体验和导入品牌内容。
feature: Email Authoring, Content, Integrations
topic: Content Supply Chain
level: Intermediate
role: User
badge: label="限量发布版" type="Informative"
exl-id: 13f45e8f-9d49-4ec2-90ef-689475c629f1
source-git-commit: 79012352c3ae4e2f3d38b632b1f523d262f74f96
workflow-type: tm+mt
source-wordcount: '794'
ht-degree: 8%

---

# 使用 GenStudio for Performance Marketing 创建电子邮件内容 {#genstudio-workflow}

>[!CONTEXTUALHELP]
>id="ajo-b2b_genstudio_button"
>title="使用 GenStudio 构建的模板"
>abstract="使用与 Adobe GenStudio for Performance Marketing 的集成，导入通过 Adobe AI 技术增强的 GenStudio 模板。"

>[!AVAILABILITY]
>
>[!DNL Adobe Journey Optimizer B2B Edition] 中的 GenStudio 集成当前不适用于 **Healthcare Shield** 或 **Privacy and Security Shield** 附加产品。
>
>此集成仅适用于电子邮件渠道。

为了提高工作流效率并维护品牌一致性，您可以将GenStudio for Performance Marketing体验与Adobe Journey Optimizer B2B edition电子邮件编排相结合。 这种扩展的工作流允许您利用GenStudio中人工智能强大的内容创建工具，通过帐户历程扩展并最大化电子邮件通信。

例如，使用Journey Optimizer B2B edition开发和自动化关键帐户的电子邮件通信的技术营销人员可以与使用GenStudio创建内容的性能营销人员协作。 借助此工作流程，两者可以协作将GenStudio中的品牌内内容合并到Journey Optimizer B2B edition基于帐户的营销自动化中，从而提供针对特定购买群体并提高销售额的吸引型电子邮件。

>[!BEGINSHADEBOX]

## GenStudio内容生成功能

[Adobe GenStudio for Performance Marketing](https://business.adobe.com/products/genstudio-for-performance-marketing.html){target="_blank"}是一个创新型人工智能优先应用程序，它使营销团队能够创建符合品牌标准并遵守其企业政策的有影响力的个性化广告和电子邮件。 通过利用Adobe AI技术，它提供了一套全面的工具，可简化内容创建和管理过程，以便创意人员可以专注于创新。

![视频](../../assets/do-not-localize/icon-video.svg){width="30"} [创建品牌内营销电子邮件](https://experienceleague.adobe.com/zh-hans/docs/genstudio-for-performance-marketing-learn/tutorials/creating-experiences/creating-on-brand-emails){target="_blank"}

在[文档](https://experienceleague.adobe.com/zh-hans/docs/genstudio-for-performance-marketing/user-guide/home){target="_blank"}中了解有关GenStudio for Performance Marketing功能的更多信息

>[!ENDSHADEBOX]

## 从Journey Optimizer B2B edition导出HTML

首先，在Journey Optimizer B2B edition中，从包含品牌准则的电子邮件中导出HTML。

1. 在Journey Optimizer B2B edition中，在可视设计空间中访问电子邮件的内容。

1. 从电子邮件设计空间顶部的&#x200B;_[!UICONTROL 更多……]_&#x200B;菜单中，选择&#x200B;**[!UICONTROL 导出HTML]**。

   ![单击“更多”并选择“导出HTML”](./assets/email-export-html.png){width="600"}

   此操作会生成一个下载的.zip文件，其中包含HTML和图像文件。

## 在GenStudio for Performance Marketing中使用导出的HTML

当导入的电子邮件HTML中的某些元素使用可识别的字段名称进行标识时，GenStudio for Performance Marketing会识别这些元素。 在导出的HTML中使用Handlebars语法添加字段名称，您需要GenStudio for Performance Marketing在其中生成特定类型的内容。

| 字段 | 内容类型 |
| ----------------- | ------------------------- |
| `{{pre_header}}` | 预编译标头 |
| `{{headline}}` | 标题 |
| `{{sub_headline}}` | 副标题 |
| `{{body}}` | 正文文本 |
| `{{cta}}` | call to action（按钮） |
| `{{image}}` | 图像 |
| `{{link}}` | 图像上的Call to action |

### 创建模板

使用HTML文件在GenStudio for Performance Marketing中创建模板。

有关在Adobe GenStudio for Performance Marketing中将HTML模板上传到GenStudio的详细信息，请参阅GenStudio for Performance Marketing文档中的[添加模板](https://experienceleague.adobe.com/en/docs/genstudio-for-performance-marketing/user-guide/content/templates/use-templates#add-a-template)。

上传导出的HTML作为模板时，GenStudio for Performance Marketing会扫描HTML文件以查找可识别的字段。 使用预览可查看模板元素，并确认您使用可识别的字段名称正确标识了它们。

### 生成电子邮件体验

在GenStudio for Performance Marketing中，使用模板创建多个电子邮件体验变体并保存它们。

有关生成品牌电子邮件体验的详细信息，请参阅GenStudio for Performance Marketing文档中的[创建电子邮件体验](https://experienceleague.adobe.com/en/docs/genstudio-for-performance-marketing/user-guide/create/create-email-experience)。

## 将生成的电子邮件体验添加到Journey Optimizer B2B edition

>[!NOTE]
>
>GenStudio for Performance Marketing集成仅适用于创建电子邮件，而不能用于创建电子邮件模板。

要使用从导出的GenStudio B2B edition电子邮件HTML文件创建的Journey Optimizer电子邮件变体，请执行以下步骤：

1. 在Journey Optimizer B2B edition中，[使用](./add-email.md)执行操作&#x200B;_[!UICONTROL 节点，将电子邮件]_&#x200B;添加到帐户历程。

   * 对于&#x200B;_[!UICONTROL 目标上的]_&#x200B;操作，请选择&#x200B;**[!UICONTROL 人员]**。

   * 若要对人员&#x200B;_[!UICONTROL 执行]_&#x200B;操作，请选择&#x200B;**[!UICONTROL 发送电子邮件]**。

     ![执行操作 — 发送电子邮件](./assets/journey-node-send-email.png){width="700" zoomable="yes"}

   * 对于&#x200B;_[!UICONTROL 电子邮件源]_，请选择&#x200B;**[!UICONTROL 新建电子邮件]**，以便在Journey Optimizer B2B edition中以本机方式创建电子邮件。

1. 在&#x200B;_创建电子邮件_&#x200B;页面上，选择&#x200B;**[!UICONTROL 导入HTML]**。

1. 在&#x200B;_[!UICONTROL 导入电子邮件]_&#x200B;对话框中，单击&#x200B;**[!UICONTROL Adobe GenStudio for Performance Marketing]**。

   ![从GenStudio for Performance Marketing导入HTML](./assets/email-import-html-genstudio.png){width="500" zoomable="yes"}

1. 浏览已发布的体验。

   您可以根据多个条件筛选体验，例如&#x200B;_模板_&#x200B;和&#x200B;_创建者_。

   ![从GenStudio for Performance Marketing导入HTML](./assets/email-import-select-gen-studio-experience.png){width="600" zoomable="yes"}

1. 选择一个体验，然后单击&#x200B;**[!UICONTROL 使用]**&#x200B;开始生成电子邮件内容。

   >[!NOTE]
   >
   >从GenStudio B2B edition或Journey Optimizer模板创建的Marketo Engage体验直接导入电子邮件设计空间。 在没有Journey Optimizer B2B edition模板的情况下创建的体验将导入兼容模式。

1. 使用[电子邮件内容和个性化工具](./email-authoring.md)根据需要编辑并保存电子邮件。

   ![从GenStudio for Performance Marketing导入HTML](./assets/email-imported-experience.png){width="800" zoomable="yes"}
