---
title: 动态人员列表
description: 在Journey Optimizer B2B Edition中定义成员资格规则和重复的动态人员列表。
feature: Audiences
role: User
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
    internal-label: Journey Optimizer B2B Edition
feature_v2:
  - id: beb5f4be-cec3-471a-9db6-831a77dd3ac9
    internal-label: Audiences
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
topic_v2:
  - id: ff2b9b37-92e0-45fc-b853-379d44c08c89
    internal-label: Audience segmentation
source-git-commit: 734966636b6d2addf014905431fa755f6fe92ee6
workflow-type: tm+mt
source-wordcount: '318'
ht-degree: 2%
---

# 动态人员列表

动态[人员列表](./people-lists.md)是由规则（过滤器）定义的人员配置文件的集合。 动态列表成员资格是使用引用人员属性和活动的简单过滤器定义的。 当配置文件根据筛选逻辑符合条件并取消符合条件时，会自动维护成员资格。

您无法在动态列表中添加或删除个人。 要更改列表成员资格，请更新其规则。 如果您需要手动或通过历程管理成员资格，请改用[静态列表](./people-lists-static.md)。

## 设置成员资格规则 {#set-membership-rules}

>[!NOTE]
>
>没有规则的动态列表没有成员。 要填充列表，请至少添加一个过滤器。

1. 打开动态列表并选择&#x200B;**[!UICONTROL 规则]**&#x200B;选项卡。

1. 单击&#x200B;**[!UICONTROL 编辑规则]**。

   ![用于生成动态人员列表的访问规则](./assets/people-list-dynamic-rules-edit.png){width="700" zoomable="yes"}

1. 在&#x200B;_[!UICONTROL 编辑规则]_&#x200B;对话框中，通过从左侧面板拖动筛选器来定义用于限定用户档案的规则。

   使用以下任意组合使配置文件符合列表条件：

   * 活动历史记录
   * [!DNL Experience Platform]启用的人员字段
   * 自定义字段
   * 意图数据
   * 人员属性
   * 特殊过滤器，如历程成员资格

   对于您添加的每个筛选器，单击&#x200B;**[!UICONTROL 添加约束]**&#x200B;以细化匹配条件。 通过在顶部应用&#x200B;**[!UICONTROL 筛选器逻辑]**&#x200B;来微调条件。 您可以选择匹配所有条件、任何条件，或定义高级逻辑。

   ![添加带有约束条件的筛选器以填充动态列表](./assets/people-list-dynamic-rules-edit-filter.png){width="700" zoomable="yes"}

1. 单击&#x200B;**[!UICONTROL 完成]**&#x200B;以保存更改。

   **[!UICONTROL 规则]**&#x200B;选项卡显示列表的筛选器和筛选逻辑，并且&#x200B;**[!UICONTROL 成员]**&#x200B;选项卡将刷新以反映更新的成员资格。 若要查找最新的受众资格，请使用&#x200B;**[!UICONTROL 更多]**&#x200B;菜单中的&#x200B;**[!UICONTROL 刷新成员]**。

1. 选择&#x200B;**[!UICONTROL 成员]**&#x200B;选项卡。

   合格成员在短暂延迟后出现在列表中。

   ![为动态联系人列表生成成员](./assets/people-list-dynamic-members.png){width="700" zoomable="yes"}

>[!NOTE]
>
>要随时更改列表规则，可以重复这些步骤。 列表成员资格会根据保存的筛选器进行刷新。

<!--

## Duplicate a dynamic list {#duplicate-dynamic-list}

Duplicating a dynamic list replicates its membership filtering so that you can reuse it in a different context.

1. In the _[!UICONTROL Dynamic lists]_ tab, click the _More menu_ ( **...** ) icon next to the list and choose **[!UICONTROL Duplicate]**.

1. Enter a unique **[!UICONTROL Name]** (required) and a **[!UICONTROL Description]** (optional).

   By default, the dialog appends `_copy` to the name of the originating list. Enter a different unique name as needed.

   ![Duplicate list dialog](./assets/people-list-duplicate-dialog.png){width="375"}

1. Click **[!UICONTROL Duplicate]**.
-->
