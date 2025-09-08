---
title: 帐户受众
description: 通过分段构建客户受众以定位特定客户，并在Journey Optimizer B2B edition中启用基于客户的个性化历程。
feature: Audiences
role: User
exl-id: f9ba690f-bab2-4c31-9000-f0be1342c8b3
source-git-commit: ae1885dbe724dcc751a72325d90641decd355a4c
workflow-type: tm+mt
source-wordcount: '561'
ht-degree: 96%

---

# 帐户受众

受众是具有相似行为和/或特征的一个群体。Journey Optimizer B2B Edition 使用 Adobe Real-Time Customer Data Platform B2B 和 B2P 版本中的帐户分段功能。通过帐户分段，用户可以利用系统内任何 B2B 实体的数据来生成帐户受众。这些帐户受众用作 Journey Optimizer B2B Edition 帐户历程的输入，有助于实现无缝激活和个性化功能。

详细了解帐户受众，以及 [Adobe Experience Platform Segmentation Service 文档](https://experienceleague.adobe.com/zh-hans/docs/ experience-platform/segmentation/types/account-audiences){target="_blank"}中如何对其定义。

## 帐户受众工作流

您可以将 Journey Optimizer B2B Edition 视为未出现在目标目录中的 Experience Platform（AEP）目标。使用以下步骤将帐户受众激活到 Journey Optimizer B2B Edition：

1. 为 AEP 中的数据创建架构。
1. 将您的数据引入 AEP。
1. 创建一个帐户区段，以评估您的数据。
1. 将已评估的数据激活至 Journey Optimizer B2B Edition。

在 Journey Optimizer B2B Edition 中，帐户受众用作基于帐户的历程的输入，让您可以定位这些帐户中的人。例如，您可以使用帐户受众来检索所有那些首席运营官（COO）或首席营销官（CMO）职位人员缺少联系信息的帐户记录。

Journey Optimizer B2B Edition 允许您直接从左侧导航栏生成 Adobe Experience Platform（AEP）帐户受众，并将其纳入您的帐户历程中。

![访问帐户受众](./assets/account-audiences-browse.png){width="800" zoomable="yes"}

## 创建帐户受众

通过创建帐户分段来定义帐户受众。您可以选择直接在 Journey Optimizer B2B Edition 应用程序中，也可以使用[区段生成器 UI](https://experienceleague.adobe.com/zh-hans/docs/ experience-platform/segmentation/ui/segment-builder){target="_blank"} 创建帐户分段。以下是在 Journey Optimizer B2B Edition 中创建帐户分段的步骤。

1. 在左侧导航栏中，选择&#x200B;**[!UICONTROL 帐户]** > **[!UICONTROL 受众]**。

1. 单击右上角的&#x200B;**[!UICONTROL 创建受众]**。

1. 构建区段定义。

   帐户属性和受众显示在左侧导航栏中。在&#x200B;_[!UICONTROL 属性]_&#x200B;选项卡中，您可以添加平台创建的属性和自定义属性。拖动每个属性来构建该区段的逻辑。

   >[!TIP]
   >
   >创建帐户受众时，请注意事件列在&#x200B;_[!UICONTROL 人员]_&#x200B;中，因为这些属性与人员相关联。<br/>
   >
   >在&#x200B;_[!UICONTROL 受众]_&#x200B;选项卡中，您可以添加之前创建的基于人员的受众，并以此为基础创建自己的帐户受众。

   以下示例定义了使用 `Country Code`、`Revenue Amount` 和 `Market segment` 创建的受众。用中文查询的话就是“我想要财务区段中收入超过 100 万美元的所有美国帐户”。

   ![帐户受众区段生成器示例](./assets/audience-segment-builder-US-finance-1M.png){width="700" zoomable="yes"}
   <br/>

   >[!IMPORTANT]
   >
   >帐户记录的 `Account Name` 属性必须包含一个值，才能包含在帐户历程中。如果此属性为空（null），该帐户记录就会被排除。<br/>
   >为确保只包含帐户名称不为空的帐户，请添加&#x200B;**[!UICONTROL 帐户名称]**&#x200B;属性，并选择 _[!UICONTROL 存在]_ 作为匹配条件。<br/>
   >![帐户名称属性存在](./assets/audience-segment-builder-account-name-exists.png){width="600"}
   ><br/>如果您为帐户名称使用自定义属性，请在&#x200B;_[!UICONTROL 帐户名称]_&#x200B;处使用自定义属性名称。

1. 单击右上角的&#x200B;**[!UICONTROL 保存并关闭]**。

要激活 Journey Optimizer B2B Edition 的帐户受众，您必须[将其添加到帐户历程](../journeys/journey-overview.md#add-the-account-audience-for-your-journey)，然后[发布历程](../journeys/journey-overview.md)。
