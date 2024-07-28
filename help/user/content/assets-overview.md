---
title: 资源
description: 了解Journey Optimizer B2B版本中的资源管理。
feature: Assets, Content
exl-id: f3848e65-3196-4d1f-90cf-7aa6ceeafabb
source-git-commit: 16b798f18f72eeb63e68a8d32e69164930aa1e22
workflow-type: tm+mt
source-wordcount: '990'
ht-degree: 0%

---

# 资源

Assets通常是在Adobe Journey Optimizer B2B版本中创建历程内容时使用的图像。 您可以通过可视内容编辑器中的资产选择器或简单的拖放界面，在Journey Optimizer B2B Edition中创作的电子邮件、电子邮件模板和片段中使用这些图像。

Adobe Journey Optimizer B2B版本为营销人员提供了对两种类型的资源库的访问权限：Adobe Marketo Engage Design Studio和Adobe Experience Manager Assetsas a Cloud Service。 您可以仅使用Adobe Marketo Engage Design Studio，或使用同时配置的两个库(基于您拥有的AEM Assets许可证)。

## 资产管理

如果您配置了Marketo Engage帐户和Adobe Experience Manager作为Cloud Service，那么当您的用户帐户具有所需的权限时，您将同时拥有Marketo EngageDAM和Adobe Experience Manager Assetsas a Cloud Service的存储库的访问权限。 这些存储库是独立的，且不同步。 您可以使用任一源中的图像，但一次只能在内容编辑器中启用一个图像。 管理员可以将从Marketo EngageDAM切换到Adobe Experience Manager Assetsas a Cloud Service。 左侧导航栏中的&#x200B;_[!UICONTROL Assets]_&#x200B;项显示当前设置的存储库。

### Adobe Marketo Engage Design Studio

默认情况下，每个Journey Optimizer B2B Edition订阅都提供Adobe Marketo Engage Design Studio Assets存储库。 这意味着您可以访问存储在Adobe Marketo Engage > Design Studio >图像和文件中的任何图像资源。 您可以将此存储库用作本地资源库，包括上传、删除和下载资源功能。 您还可以在历程内容中使用这些资产。

支持的文件格式：JPG、JPEG、GIF、PNG、EPS、SVG、RGB

### Adobe Experience Manager Assetsas a Cloud Service

使用Adobe Experience Manager Assets将营销工作流程和创意工作流程整合在一起。 它与Adobe Journey Optimizer B2B版本原生集成，因此您可以轻松访问Assets as a Cloud Service以发现和使用数字资源。 它提供对Assets存储库的访问权限，以便您使用这些资源填充消息。

Adobe Experience Manager Assets可以连接到Adobe Experience Manager Assets as a Cloud Service以实现集中式资源工作区，进而扩展您的创意系统并统一数字资源以交付体验。 Adobe Experience Manager Assets as a Cloud Service为高效的数字资产管理和Dynamic Media操作提供了一个易于使用的云解决方案。 它将人工智能和机器学习等高级功能无缝地整合在一起。

请参阅[Adobe Experience Manager as a Cloud Service文档](https://experienceleague.adobe.com/zh-hans/docs/experience-manager-cloud-service/content/assets/overview)以了解详情。

可从左侧导航栏中的&#x200B;**[!UICONTROL Assets]**&#x200B;项直接在Adobe Journey Optimizer B2B版本中访问Adobe Experience Manager Assets。 在设计电子邮件内容时，您还可以访问资源和文件夹。

>[!NOTE]
>
>AEM Assets作为Cloud Service以及Dynamic Media许可证是此集成的先决条件。<br/>
>根据您的合同和配置，可直接从Adobe Journey Optimizer B2B版本通过左侧菜单Assets部分访问Adobe Experience Manager Assetsas a Cloud Service。 在设计电子邮件内容时，您还可以访问资源和文件夹。

目前，您只能在Adobe Journey Optimizer B2B版本中使用Adobe Experience Manager Assets中的图像。

## 使用资产进行内容创作

在创作电子邮件、电子邮件模板和可视化片段时使用资产。 通过可视内容编辑器UI，可访问您连接的资产存储库中的图像。

### 选择资产源

如果您订阅了Experience Manager Assetsas a Cloud Service以及默认的Adobe Marketo Engage Design Studio，则可以从任一源选择图像资源。 要实现此目的，您必须在创建新电子邮件、电子邮件模板或可视片段时选择图像源。 或者，您可以在编辑内容时选择图像源。 所选内容仅适用于编辑体验，您可以根据需要更改图像源以从其他库访问资产。

_**创建内容资源**_ — 要在创建电子邮件、电子邮件模板或片段时选择图像源，请在创建时设置&#x200B;**[!UICONTROL 图像源]**。

_**编辑内容资源**_ — 若要在可视编辑器中选择图像资源源，请使用画布顶部的&#x200B;**[!UICONTROL 选择图像源]**&#x200B;选择器。

### 将资源添加到您的内容

您可以在创作内容时添加图像资源，具体取决于您选择的图像资源源。

>[!BEGINTABS]

>[!TAB 添加Marketo EngageDesign Studio图像资源]

您可以使用以下任一方法添加Marketo Engage Design Studio资源：

* 添加一个结构元素，然后将左侧导航中的资产拖放到可视画布中。
* 添加结构元素，然后将&#x200B;_image_&#x200B;内容类型拖放到结构中。 在右侧的属性设置中，可通过两种方式指定图像：
   * 单击&#x200B;**[!UICONTROL 浏览]**&#x200B;以打开资源选择器，您可以从中从Adobe Marketo Engage Design Studio资源库中选择图像。
   * 单击&#x200B;**[!UICONTROL 导入媒体]**&#x200B;以从本地系统导入资产。 导入的资源存储在Adobe Marketo Engage Design Studio库的Assets根文件夹中。

要更改图像，您可以在右侧的属性中更新图像的源URL。

>[!TAB 添加Experience Manager Assets图像]

1. 在Email Designer中创作电子邮件内容时，请将图像元素拖动到画布上。

   右侧的属性反映图像元素选择。

1. 单击&#x200B;**[!UICONTROL 选择资源]**&#x200B;以打开Experience Manager资源选择器。

   在这里，您可以搜索、筛选和访问要添加到营销资源的所需内容资源。 有关如何使用选择器的更多详细信息，请参阅此页面。

   >[!NOTE]
   >
   >如果配置了多个存储库，则可以使用资产选择器上的存储库切换器

1. 选择要插入到电子邮件中的所需资源。

>[!ENDTABS]
