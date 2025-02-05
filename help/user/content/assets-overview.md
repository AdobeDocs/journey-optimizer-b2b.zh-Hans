---
title: 资源
description: 了解Journey Optimizer B2B edition中的资源管理。
feature: Assets, Content
exl-id: f3848e65-3196-4d1f-90cf-7aa6ceeafabb
source-git-commit: 728d5316cfdeee92bd4f67277d299bbec2773a4f
workflow-type: tm+mt
source-wordcount: '981'
ht-degree: 0%

---

# 资源

在Adobe Journey Optimizer B2B edition中，资源通常是在设计内容以支持帐户历程时使用的图像。 您可以通过资产选择器或可视内容编辑器中的简单拖放界面，在电子邮件、电子邮件模板和片段中使用这些图像。

Adobe Journey Optimizer B2B edition为营销人员提供了对两种类型的资源库的访问权限：Adobe Marketo Engage Design Studio和Adobe Experience Manager Assetsas a Cloud Service。 您可以仅使用Adobe Marketo Engage Design Studio，或使用同时配置的两个库(基于您拥有的AEM Assets许可证)。

## 资产管理

如果您配置了Adobe Experience Manager作为Cloud Service，则当您的用户帐户具有所需的权限时，您将有权访问Marketo EngageDesign Studio和Adobe Experience Manager Assetsas a Cloud Service的存储库。 这些存储库是独立的，且不同步。 您可以使用任一源中的图像。

### Adobe Marketo Engage资源

默认情况下，每个Adobe Marketo Engage B2B edition订阅都提供Journey Optimizer Design Studio Assets存储库。 这意味着您可以访问Adobe Marketo Engage中存储的任何图像资源（[!UICONTROL Design Studio] > [!UICONTROL 图像和文件]）。 您可以将此存储库用作本地资源库，包括上传和下载资源功能。 您还可以在历程内容中使用这些资产。

有内置的护栏，阻止从Journey Optimizer B2B edition编辑Marketo Engage资源以及执行删除和移动操作。 这些保护可以确保维护源资源(Marketo EngageDesign Studio)，同时允许在Journey Optimizer B2B edition中无缝读取和重用。

支持的文件格式：JPG、JPEG、GIF、PNG、EPS、SVG和RGB

### Adobe Experience Manager Assetsas a Cloud Service

使用Adobe Experience Manager Assets将营销工作流程和创意工作流程整合在一起。 它与Adobe Journey Optimizer B2B edition原生集成，因此您可以轻松访问Assets as a Cloud Service以发现和使用数字资源。 它提供对Assets存储库的访问权限，以便您使用这些资源填充消息。

Adobe Journey Optimizer B2B edition可连接到Adobe Experience Manager Assetsas a Cloud Service以实现集中式资源管理，从而扩展您的创意系统并统一数字资源以交付体验。 Adobe Experience Manager Assets as a Cloud Service为高效的数字资产管理和Dynamic Media操作提供了一个易于使用的云解决方案。 它将人工智能和机器学习等高级功能无缝地整合在一起。

请参阅[Adobe Experience Manager as a Cloud Service文档](https://experienceleague.adobe.com/zh-hans/docs/experience-manager-cloud-service/content/assets/overview)以了解详情。

{{aem-assets-licensing-note}}

从内容设计左侧导航栏中的&#x200B;**[!UICONTROL Adobe Experience Manager Assets]**&#x200B;项，直接在Journey Optimizer B2B edition中访问Experience Manager Assets。 在设计电子邮件、电子邮件模板和可视化片段内容时，您还可以访问资源和文件夹。

目前，您只能在Adobe Journey Optimizer B2B edition中使用Adobe Experience Manager Assets中的图像。

## 使用资产进行内容创作

在创作电子邮件、电子邮件模板和可视化片段时使用资产。 通过可视内容编辑器，可访问您连接的资产存储库中的图像。 如果您订阅了Experience Manager Assetsas a Cloud Service以及默认的Adobe Marketo Engage Design Studio，则可以从任一源选择图像资源。 您还可以上传图像资源，并将其置于所连接的Marketo EngageDesign Studio存储库的Journey Optimizer B2B edition工作区中。

您可以在编辑图像组件的设置时或直接在画布上选择图像源。

* **_图像组件设置_** — 在可视设计器中选择了图像组件后，您可以在右侧面板中查看和编辑设置。 要添加或更改组件中显示的图像文件，请选择源类型并选择图像文件。

  ![在右侧面板中编辑图像组件设置](./assets/content-assets-image-settings.png){width="350"}

* **_空组件_** — 在可视设计器中添加图像组件时，该组件为空，因此可以方便地选择源并选择图像文件。

  ![选择源以选择空图像组件的图像文件](./assets/content-assets-image-component-empty.png){width="500"}

* **_图像组件工具栏_** — 在可视设计器中选择了图像组件后，可通过工具栏轻松选择源并选择图像文件。

  ![使用工具栏选择源以选择图像组件的图像文件](./assets/content-assets-image-toolbar-settings.png){width="500"}

您可以在创作内容时添加图像资源，具体取决于图像资源源。

>[!BEGINTABS]

>[!TAB Marketo EngageAssets]

单击&#x200B;**[!UICONTROL Marketo EngageAssets]**&#x200B;以打开资源选择器，您可以从中从Marketo Engage工作区或Journey Optimizer B2B edition工作区中选择图像。

![从工作区中选择图像资源](./assets/content-assets-image-me-selected.png){width="700" zoomable="yes"}

您可以使用搜索和筛选来查找所需的图像资源。 选择资源并单击&#x200B;**[!UICONTROL 选择]**&#x200B;将其用于图像组件。

有关使用Marketo Engage图像资源的更多详细信息，请参阅[在内容中使用资源](./marketo-engage-design-studio.md#use-assets-in-your-content)。

>[!TAB Experience Manager Assets]

单击&#x200B;**[!UICONTROL Experience Manager Assets]**&#x200B;以打开资源选择器，您可以从中从Experience Manage Assets存储库中选择图像。

![从AEM Assets存储库中选择图像资源](./assets/content-assets-image-aem-selected.png){width="700" zoomable="yes"}

您可以使用搜索和筛选来查找所需的图像资源。 选择资源并单击&#x200B;**[!UICONTROL 选择]**&#x200B;将其用于图像组件。

有关从Experience Manager Assets使用图像文件的更多详细信息，请参阅[访问AEM Assets图像](./aem-assets.md#access-aem-assets-images)。

>[!TAB 导入媒体]

单击&#x200B;**[!UICONTROL 导入媒体]**&#x200B;以选择图像文件，并将其作为可用于Journey Optimizer B2B edition内容的资源导入。

![选择您自己的图像文件作为资产导入](./assets/content-assets-image-import-file-selected.png){width="500" zoomable="yes"}

拖放文件或从文件系统选择文件后，单击&#x200B;**[!UICONTROL 导入]**。 导入的资源存储在Adobe Marketo Engage Design Studio存储库的Journey Optimizer B2B edition工作区中。

>[!ENDTABS]
