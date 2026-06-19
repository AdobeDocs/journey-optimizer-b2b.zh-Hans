---
title: 资产
description: 从Journey Optimizer B2B edition管理电子邮件、模板和可视化片段的图像资源。
feature: Assets, Content
role: User
badgeBeta: label="Beta 版" type="informative" tooltip="此功能属于有限测试版。"
autotag-review: '2026-06-18T20:11:57.611Z'
TQID: 'https://experienceleague.adobe.com/Xsl4zqpk4xqXuOS85Z5U08tnbv8GWm3FXdqsegPCBI4'
product_v2: id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2: id: e666e996-b2cf-4c45-8fc2-1c625212ababid: aed878b8-11d0-487c-828b-d23b2051ec37
subfeature_v2: id: c8402946-ff35-44c5-ab98-74c1bba0975fid: d270a788-eb1d-40ed-b74e-9158ed975b1f
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 579f36911af99308294726e91e80c5d08015d5cf
workflow-type: tm+mt
source-wordcount: 524
ht-degree: 5%

---

# 资产

在[!DNL Adobe Journey Optimizer B2B Prime]中，资产通常是设计内容以支持历程时使用的图像。 您可以从资产选择器的[电子邮件](email-authoring.md)、[电子邮件模板](templates.md)和[可视片段](email-authoring.md#visual-fragments)中使用这些图像，也可以在可视设计空间中使用简单的拖放界面。

支持的文件格式：JPG、JPEG、GIF、PNG、EPS、SVG 和 RGB

>[!NOTE]
>
>在此Beta版本中，您可以直接从电子邮件画布中的Marketo Engage资源库的一次性副本中选择图像和资源。 在初始副本为&#x200B;**且未在[!DNL Journey Optimizer B2B Prime]中反映**&#x200B;后，在Marketo Engage中修改资源。
>
>您可以从&#x200B;_[!UICONTROL Assets]_&#x200B;库或内容设计空间上传其他图像资源。 这些上传的资产只能在[!DNL Journey Optimizer B2B Prime]实例中使用。
>
>从外部系统导入资源以及访问预填充的资源库尚不可用。 预计未来版本将包括从现有系统导入资产、文件夹支持和扩展的资产管理功能。

<!-- You can [edit these assets using Adobe Express](./image-edit-adobe-express.md), and move them into folders to organize them for use across your emails, templates, and fragments. -->

**Assets**&#x200B;库提供对集中式存储库的访问权限，该存储库用于存储和管理图像和其他创意资源。 它包括AI支持的功能，可自动生成元数据并启用自然语言搜索。

在左侧导航中，展开&#x200B;**[!UICONTROL 内容管理]**&#x200B;并选择&#x200B;**[!UICONTROL Assets]**。

![显示可排序元数据列的Assets库列表视图](./assets/dam-asset-library-list-view.png){width="800" zoomable="yes"}

>[!BEGINSHADEBOX]

首次访问&#x200B;_[!UICONTROL Assets]_&#x200B;库时，请查看[_[!UICONTROL 创作AI使用条款&#x200B;]_](https://www.adobe.com/cn/legal/licenses-terms/adobe-gen-ai-user-guidelines.html)，并确认您的协议。

![Assets库中的创作AI使用条款协议对话框](./assets/dam-asset-library-gen-ai-agree.png){width="500"}

>[!ENDSHADEBOX]

库支持两种布局选项：

* **[!UICONTROL 列表]** — 单击&#x200B;_列表视图_ （![列表视图图标](../../assets/do-not-localize/icon-falco-list-view.svg)）图标以在包含元数据列的可排序表中显示资源。
* **[!UICONTROL 图库]** — 单击&#x200B;_图库视图_ （ ![图库视图图标](../../assets/do-not-localize/icon-falco-gallery-view.svg) ）图标，将资产显示为可视缩略图网格。

## 搜索资源 {#find-assets}

使用&#x200B;_[!UICONTROL 搜索]_&#x200B;字段通过以自然语言描述所需内容来查找资源。 搜索结果基于人工智能生成的元数据，因此您不仅限于按文件名搜索。

**示例：**

* `team members`
* `nature`
* `exercise`

![从Assets库中的搜索结果中选择的图像](./assets/dam-asset-library-select-image.png){width="700" zoomable="yes"}

## 查看资源详细信息 {#view-details}

在列表或库视图中选择任意资源以在右侧打开其详细信息视图，其中显示AI生成的描述、标记、关键字和其他元数据字段。 上传资产时，会自动生成此信息。 选择&#x200B;**[!UICONTROL AI元数据]**&#x200B;选项卡以查看生成的描述、标记和元数据。

![显示AI生成的元数据和标记的资源详细信息视图](./assets/dam-asset-library-select-image-metadata.png){width="700" zoomable="yes"}

## 上传资源 {#upload}

1. 单击右上方的&#x200B;**[!UICONTROL 上传]**。

1. 在对话框中，从本地系统中拖放文件。

   ![上传图像资产](./assets/dam-upload-assets-dialog.png){width="450"}

   或者，您可以单击&#x200B;**[!UICONTROL 从计算机中选择文件]**&#x200B;以使用本地文件系统查找并选择该文件。

1. 单击&#x200B;**[!UICONTROL 上载文件]**&#x200B;以确认文件并将其上载到存储库。

上传完成后，系统自动生成描述，分配标签和关键字，提取主题和设置等可视属性。 无需手动标记。 在此过程完成之前，新图像以&#x200B;_[!UICONTROL PROCESSING]_&#x200B;状态显示。

![新图像资源处于处理状态](./assets/dam-asset-library-upload-processing.png){width="700" zoomable="yes"}
