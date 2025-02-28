---
title: 片段
description: 重用注释和可视化元素来注释应用于特定版本的功能或页面
source-git-commit: d0b2f91754ce3c5e38c6aa2c49c816fd46510403
workflow-type: tm+mt
source-wordcount: '451'
ht-degree: 0%

---

# 片段

<!-- Content authoring steps for reuse -->

## 目的数据配置 {#intent-data-note}

>[!NOTE]
>
>为您的Journey Optimizer B2B edition实例配置目的数据后，即会包含目的数据。 还需要一个或多个已发布的历程&#x200B;**或**&#x200B;创建购买组。 有关意图检测模型以及如何提交关键字、产品和类别的详细信息，请参阅[意图数据](../user/admin/intent-data.md)。

## AEM assets许可说明 {#aem-assets-licensing-note}

>[!NOTE]
>
>AEM Assets as a Cloud Service的许可证和Dynamic Media许可证是进行集成的先决条件。 您应确保启用了[Dynamic Media withOpen API](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/assets/dynamicmedia/dynamic-media-open-apis/dynamic-media-open-apis-overview){target="_blank"}。<br/>
>根据您的合同和配置，在设计可视化内容时，可以直接从Adobe Experience Manager Assets B2B edition访问Adobe Journey Optimizer as a Cloud Service 。

## 内容创作 — 组件 — 结构步骤 {#structures-step}

1. 要开始内容设计，请从&#x200B;**[!UICONTROL 结构]**&#x200B;中拖动一个项，然后将其放到画布上。

   根据需要从&#x200B;_[!UICONTROL 结构]_&#x200B;添加任意数量的项，并编辑右侧窗格中每个项的设置。

   >[!TIP]
   >
   >选择&#x200B;_[!UICONTROL n：n列]_&#x200B;组件以定义您选择的列数（3到10之间）。 您还可以通过移动列下方的箭头来定义每列的宽度。

   ![将结构拖动到画布上并调整设置](../assets/content-design-shared/content-design-add-structure.png){width="800" zoomable="yes"}

   每个列大小不能小于结构组件总宽度的10%。 只能删除空列。

## 内容创作 — 组件 — 内容步骤 {#contents-step}

1. 展开&#x200B;**[!UICONTROL 内容]**&#x200B;部分并将所需数量的元素添加到一个或多个结构组件中。

   ![将内容元素拖到画布上并调整设置](../assets/content-design-shared/content-design-add-content.png){width="800" zoomable="yes"}
   <!--
   reference to the contents elements--->

## 内容创作 — 组件 — 设置步骤 {#settings-step}

1. 如果需要，您可以在&#x200B;_[!UICONTROL 设置]_&#x200B;或&#x200B;_[!UICONTROL 样式]_&#x200B;选项卡中为每个组件进行其他自定义。

   例如，可以更改每个组件的文本样式、填充或边距。

## 内容创作 — 资产步骤 {#assets-step}

1. 从&#x200B;_资产_&#x200B;选取器中，您可以直接选择存储在资产库中的资产。

   双击包含资产的文件夹。 将项目拖放到结构组件中。

   有关使用源类型中的资产的更多信息，请参阅[将资产添加到您的内容](../user/content/assets-overview.md#use-assets-for-content-authoring)。

   ![将Marketo Engage资源拖动到画布上并调整设置](../assets/content-design-shared/content-design-add-asset.png){width="800" zoomable="yes"}

## 内容创作 — 个性化步骤 {#personalization-step}

1. 插入个性化字段以根据用户档案属性、受众成员资格、上下文属性等自定义您的内容。

## 内容创作 — 启用条件内容步骤 {#dynamic-content-step}

1. 单击&#x200B;**[!UICONTROL 启用条件内容]**&#x200B;以添加动态内容，并根据条件规则将内容调整为目标配置文件。

## 内容创作 — 链接跟踪步骤 {#links-tracking-step}

1. 从左窗格中选择&#x200B;**[!UICONTROL 链接]**&#x200B;选项卡以显示您的内容中被跟踪的所有URL。

   您可以修改&#x200B;_跟踪类型_&#x200B;或&#x200B;_标签_，并根据需要添加标记。
