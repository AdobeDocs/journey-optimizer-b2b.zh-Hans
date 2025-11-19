---
title: 资产
description: 从Journey Optimizer B2B edition和AEM Assets管理电子邮件、模板和片段的图像资源。
feature: Assets, Content
role: User
exl-id: f3848e65-3196-4d1f-90cf-7aa6ceeafabb
source-git-commit: 1c5a08b293db9287d03b103d794cc17a1c186af0
workflow-type: tm+mt
source-wordcount: '852'
ht-degree: 60%

---

# 资产

在 [!DNL Adobe Journey Optimizer B2B Edition] 中，资产通常是为了支持帐户历程而设计内容时所使用的图像。您可以在电子邮件、电子邮件模板以及资产选择器中的片段中使用这些图像，也可以在可视设计空间中使用简单的拖放界面。

[!DNL Journey Optimizer B2B Edition]使设计人员和营销人员能够访问两种类型的资源库：内部[!DNL Journey Optimizer B2B Edition]资源存储库和[!DNL Adobe Experience Manager Assets as a Cloud Service]。 您可以仅使用内置存储库，或同时使用这两种库类型（基于您拥有的[!DNL Experience Manager Assets]许可证）。

## 资产管理

如果您已配置[!DNL Adobe Experience Manager as a Cloud Services]并在[!DNL Journey Optimizer B2B Edition]中将其配置为资产源，则当您的用户帐户具有所需的权限时，您可以访问这两种存储库类型。 这两个存储库是独立的，且不同步。您可以使用两者中任一来源的图像。

### 内部资产

默认情况下，每[!DNL Journey Optimizer B2B Edition]订阅都会提供内部资源存储库。 这意味着您有权访问所连接[!DNL Adobe Marketo Engage]资源文件系统中存储的任何图像资源。 您可以将该存储库用作您的本地资产库，包含上传和下载资产功能。您还可以在历程内容中使用这些资产。

您可以[使用Adobe Express](./image-edit-adobe-express.md)编辑这些资源，并将它们移动到文件夹中，以整理它们以供在电子邮件、模板和片段中使用。

支持的文件格式：JPG、JPEG、GIF、PNG、EPS、SVG 和 RGB

### Adobe Experience Manager Assets as a Cloud Service

利用 [!DNL Adobe Experience Manager Assets] 整合营销和创意工作流。它与 [!DNL Journey Optimizer B2B Edition] 原生集成，因此您可以轻松访问 Assets as a Cloud Service，以发现和使用数字资产。它提供了对 Assets 存储库的访问，您可以使用这些资产来填充您的消息。

[!DNL Adobe Journey Optimizer B2B Edition] 可以与 [!DNL Adobe Experience Manager Assets as a Cloud Service] 连接以进行集中资产管理，从而扩展您的创意系统，统一数字资产以提供体验。[!DNL Adobe Experience Manager Assets as a Cloud Service] 提供了一种易于使用的云解决方案，以实现高效的数字资产管理和动态媒体操作。它无缝地融合了先进的功能，包括人工智能和机器学习。

更多详情请参阅 [Adobe Experience Manager as a Cloud Service 文档](https://experienceleague.adobe.com/zh-hans/docs/experience-manager-cloud-service/content/assets/overview){target="_blank"}。

{{aem-assets-licensing-note}}

从内容设计左侧导航中的 **[!UICONTROL Experience Manager Assets]** 项中的 [!DNL Journey Optimizer B2B Edition] 直接访问 [!DNL Adobe Experience Manager Assets]。您还可以在设计电子邮件、电子邮件模板和可视片段内容时访问资产和文件夹。

目前，您只能在 Adobe Journey Optimizer B2B Edition 中使用来自 Adobe Experience Manager Assets 的图像。

## 使用资产进行内容创作

在创作电子邮件、电子邮件模板和可视片段时使用资产。通过可视内容编辑器可访问所连接资产存储库中的图像。如果您还订阅了Experience Manager Assets as a Cloud Service，则可以从任一源选择图像资源。 您还可以上传图像资产，并将其放置在内部资产存储库中。

您可以在编辑图像组件的设置时选择图像源，也可以直接在画布上选择：

* **_图像组件设置_** — 在画布中选择了图像组件后，您可以在右侧面板中查看和编辑设置。 要添加或更改组件中显示的图像文件，请选择源类型，然后选择一个图像文件。

  ![在右侧面板中编辑图像组件设置](./assets/content-assets-image-settings.png){width="350"}

* **_空组件_** — 将图像组件添加到画布时，该组件是空的，因此可以方便地选择源并选择图像文件。

  ![为空图像组件选择来源和图像文件](./assets/content-assets-image-component-empty.png){width="500"}

* **_图像组件工具栏_** — 在画布中选择了图像组件后，可通过工具栏轻松选择源并选择图像文件。

  ![使用工具栏为图像组件选择来源和图像文件](./assets/content-assets-image-toolbar-settings.png){width="500"}

您可以在创作内容时添加图像资产，具体取决于图像资产来源。您还可以在某个结构组件的背景设置中选择图像资产。

>[!BEGINTABS]

>[!TAB 选择资源]

单击&#x200B;**[!UICONTROL 选择资源]**&#x200B;以打开资源选择器，您可以从中从Journey Optimizer B2B edition资源存储库中选择图像。

![选择图像资源](./assets/content-assets-internal-image-selected.png){width="700" zoomable="yes"}

您可以使用搜索和过滤器来找到所需的图像资产。选择资产，然后单击&#x200B;**[!UICONTROL 选择]**，将其用于图像组件。

有关使用内部图像资源的更多详细信息，请参阅[在内容中使用资源](./internal-image-assets.md#use-assets-in-your-content)。

>[!TAB Experience Manager Assets]

单击 **[!UICONTROL Experience Manager Assets]** 打开资产选择器，您可以从 Experience Manage Assets 存储库中选择图像。

![从 AEM Assets 存储库中选择图像资产](./assets/content-assets-image-aem-selected.png){width="700" zoomable="yes"}

您可以使用搜索和过滤器来找到所需的图像资产。选择资产，然后单击&#x200B;**[!UICONTROL 选择]**，将其用于图像组件。

有关使用 [!DNL Experience Manager Assets] 中图像文件的详细信息，请参阅[访问 AEM Assets 图像](./aem-assets.md#access-aem-assets-images)。

>[!TAB 导入媒体]

单击&#x200B;**[!UICONTROL 导入媒体]**，选择图像文件，并将其导入为可用于 Journey Optimizer B2B Edition 内容的资产。

![选择您自己的图像文件导入为资产](./assets/content-assets-image-import-file-selected.png){width="450" zoomable="yes"}

拖放文件或从文件系统中选择文件后，单击&#x200B;**[!UICONTROL 导入]**。导入的资源存储在[!DNL Journey Optimizer B2B Edition]资源存储库中。

>[!ENDTABS]
