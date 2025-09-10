---
title: 资产
description: 从Marketo Engage Design Studio和AEM Assets中管理Journey Optimizer B2B edition中的电子邮件、模板和片段的图像资源。
feature: Assets, Content
role: User
exl-id: f3848e65-3196-4d1f-90cf-7aa6ceeafabb
source-git-commit: 79012352c3ae4e2f3d38b632b1f523d262f74f96
workflow-type: tm+mt
source-wordcount: '883'
ht-degree: 91%

---

# 资产

在 [!DNL Adobe Journey Optimizer B2B Edition] 中，资产通常是为了支持帐户历程而设计内容时所使用的图像。您可以在电子邮件、电子邮件模板以及资产选择器中的片段中使用这些图像，也可以在可视设计空间中使用简单的拖放界面。

[!DNL Journey Optimizer B2B Edition] 为营销人员提供两种类型的资产库：[!DNL Adobe Marketo Engage] [!DNL Design Studio] 和 [!DNL Adobe Experience Manager Assets as a Cloud Service]。您可以仅使用Adobe Marketo Engage Design Studio，或使用同时配置的两个库（基于您拥有的[!DNL Experience Manager Assets]许可证）。

## 资产管理

如果您已配置 [!DNL Adobe Experience Manager as a Cloud Services]，当您的用户帐户具有必需的权限时，您就可以访问 [!DNL Marketo Engage Design Studio] 和 [!DNL Adobe Experience Manager Assets as a Cloud Service] 的存储库。这两个存储库是独立的，且不同步。您可以使用两者中任一来源的图像。

### Adobe Marketo Engage 资产

每个 [!DNL Journey Optimizer B2B Edition] 订阅都默认提供 [!DNL Adobe Marketo Engage Design Studio] 资产存储库。这意味着您可以访问存储在 [!DNL Adobe Marketo Engage]（[!UICONTROL Design Studio] > [!UICONTROL 图像和文件]）中的任何图像资产。您可以将该存储库用作您的本地资产库，包含上传和下载资产功能。您还可以在历程内容中使用这些资产。

内置防护栏可防止对来自 [!DNL Journey Optimizer B2B Edition] 的 [!DNL Marketo Engage] 资产进行编辑，以及防止删除和移动操作。这些保护措施可确保源资产（Marketo Engage Design Studio）得到维护，同时允许在 [!DNL Journey Optimizer B2B Edition] 中无缝读取和重复使用。

支持的文件格式：JPG、JPEG、GIF、PNG、EPS、SVG 和 RGB

### Adobe Experience Manager Assets as a Cloud Service

利用 [!DNL Adobe Experience Manager Assets] 整合营销和创意工作流。它与 [!DNL Journey Optimizer B2B Edition] 原生集成，因此您可以轻松访问 Assets as a Cloud Service，以发现和使用数字资产。它提供了对 Assets 存储库的访问，您可以使用这些资产来填充您的消息。

[!DNL Adobe Journey Optimizer B2B Edition] 可以与 [!DNL Adobe Experience Manager Assets as a Cloud Service] 连接以进行集中资产管理，从而扩展您的创意系统，统一数字资产以提供体验。[!DNL Adobe Experience Manager Assets as a Cloud Service] 提供了一种易于使用的云解决方案，以实现高效的数字资产管理和动态媒体操作。它无缝地融合了先进的功能，包括人工智能和机器学习。

更多详情请参阅 [Adobe Experience Manager as a Cloud Service 文档](https://experienceleague.adobe.com/zh-hans/docs/experience-manager-cloud-service/content/assets/overview){target="_blank"}。

{{aem-assets-licensing-note}}

从内容设计左侧导航中的 **[!UICONTROL Experience Manager Assets]** 项中的 [!DNL Journey Optimizer B2B Edition] 直接访问 [!DNL Adobe Experience Manager Assets]。您还可以在设计电子邮件、电子邮件模板和可视片段内容时访问资产和文件夹。

目前，您只能在 Adobe Journey Optimizer B2B Edition 中使用来自 Adobe Experience Manager Assets 的图像。

## 使用资产进行内容创作

在创作电子邮件、电子邮件模板和可视片段时使用资产。通过可视内容编辑器可访问所连接资产存储库中的图像。如果您订阅了 Experience Manager Assets as a Cloud Service 以及默认的 Adobe Marketo Engage Design Studio，就可以选择任一来源的图像资产。您还可以上传图像资产，将其放置在已连接的 [!DNL Marketo Engage Design Studio] 存储库的 [!DNL Journey Optimizer B2B Edition] 工作区中。

您可以在编辑图像组件的设置时选择图像源，也可以直接在画布上选择：

* **_图像组件设置_**——如果您在可视化设计空间中选择了图像组件，就可以在右侧面板中查看和编辑设置。要添加或更改组件中显示的图像文件，请选择源类型，然后选择一个图像文件。

  ![在右侧面板中编辑图像组件设置](./assets/content-assets-image-settings.png){width="350"}

* **_空组件_**——如果您在可视化设计空间中添加了图像组件，该组件是空的，您可以通过它轻松选择来源和图像文件。

  ![为空图像组件选择来源和图像文件](./assets/content-assets-image-component-empty.png){width="500"}

* **_图像组件工具栏_**——如果您在可视化设计空间中选择了图像组件，您就可以在工具栏中轻松选择来源和图像文件。

  ![使用工具栏为图像组件选择来源和图像文件](./assets/content-assets-image-toolbar-settings.png){width="500"}

您可以在创作内容时添加图像资产，具体取决于图像资产来源。您还可以在某个结构组件的背景设置中选择图像资产。

>[!BEGINTABS]

>[!TAB Marketo Engage Assets]

点击 **[!UICONTROL Marketo Engage Assets]** 打开资产选择器，您可以从 [!DNL Marketo Engage] 工作区或 Journey Optimizer B2B Edition 工作区中选择图像。

![从工作区中选择图像资产](./assets/content-assets-image-me-selected.png){width="700" zoomable="yes"}

您可以使用搜索和过滤器来找到所需的图像资产。选择资产，然后单击&#x200B;**[!UICONTROL 选择]**，将其用于图像组件。

有关使用 [!DNL Marketo Engage] 图像资产的详细信息，请参阅[在您的内容中使用资产](./marketo-engage-design-studio.md#use-assets-in-your-content)。

>[!TAB Experience Manager Assets]

单击 **[!UICONTROL Experience Manager Assets]** 打开资产选择器，您可以从 Experience Manage Assets 存储库中选择图像。

![从 AEM Assets 存储库中选择图像资产](./assets/content-assets-image-aem-selected.png){width="700" zoomable="yes"}

您可以使用搜索和过滤器来找到所需的图像资产。选择资产，然后单击&#x200B;**[!UICONTROL 选择]**，将其用于图像组件。

有关使用 [!DNL Experience Manager Assets] 中图像文件的详细信息，请参阅[访问 AEM Assets 图像](./aem-assets.md#access-aem-assets-images)。

>[!TAB 导入媒体]

单击&#x200B;**[!UICONTROL 导入媒体]**，选择图像文件，并将其导入为可用于 Journey Optimizer B2B Edition 内容的资产。

![选择您自己的图像文件导入为资产](./assets/content-assets-image-import-file-selected.png){width="500" zoomable="yes"}

拖放文件或从文件系统中选择文件后，单击&#x200B;**[!UICONTROL 导入]**。导入的资产被存储在 [!DNL Adobe Marketo Engage Design Studio] 存储库的 [!DNL Journey Optimizer B2B Edition] 工作区中。

>[!ENDTABS]
