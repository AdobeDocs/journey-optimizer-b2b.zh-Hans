---
title: 静态人员列表
description: 在Journey Optimizer B2B Edition中添加和删除静态人员列表的成员。
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
source-git-commit: d713d57bddf2ac6f8cf7e7a7d163281f607d729c
workflow-type: tm+mt
source-wordcount: '462'
ht-degree: 2%
---

# 静态人员列表

静态[人员列表](./people-lists.md)是人员配置文件的集合，其成员资格仅在您添加或删除人员时更改。 引用人员属性和活动的简单筛选器可定义静态列表成员资格。 仅在添加或删除成员时，成员身份才会更改。 您可以：

* [通过应用一次计算的筛选器集来添加人员](#static-list-add-members)。
* 使用[!UICONTROL 添加到人员列表]和[!UICONTROL 从人员列表中删除]操作，通过帐户或人员历程添加和删除人员。 （请参阅[在历程中使用人员列表](./people-lists-journeys.md)）
<!-- * [Activate the list to a destination](#static-list-activate) to sync its membership downstream. -->

>[!NOTE]
>
>将成员添加到列表时，会应用一次静态列表筛选器定义。 定义的过滤器随后不可用。 如果要使用过滤器保持一致的受众定义，请改用[动态列表](./people-lists-dynamic.md)。

## 添加成员 {#static-list-add-members}

>[!NOTE]
>
>如果您希望静态列表以空开头，请不要应用过滤器。 当您计划通过历程添加成员时，空的静态列表很有用。

1. 打开静态列表，然后单击右上方的&#x200B;**[!UICONTROL 添加人员]**。

   ![将联系人添加到静态联系人列表](./assets/people-list-static-add-people.png){width="700" zoomable="yes"}

1. 在&#x200B;_[!UICONTROL 添加人员]_&#x200B;对话框中，通过从左侧面板拖动筛选器来定义用于限定用户档案的规则。

   使用下列任意组合筛选用户档案：

   * 活动历史记录
   * 启用Experience Platform的人员字段
   * 自定义字段
   * 意图数据
   * 人员属性
   * 特殊过滤器，如历程成员资格

   过滤器嵌套在类别文件夹中。 展开每个文件夹并滚动浏览可用的筛选器，或使用顶部的&#x200B;_搜索_&#x200B;字段找到所需的筛选器。 对于您添加的每个过滤器：

   * 将筛选器从左侧面板拖到筛选器定义空间。
   * 完成匹配评估定义。
   * 单击&#x200B;**[!UICONTROL 添加约束]**&#x200B;以细化匹配条件。

   通过在顶部应用&#x200B;**[!UICONTROL 筛选器逻辑]**&#x200B;来微调条件。 您可以选择匹配所有条件、任何条件，或定义高级逻辑。

   ![添加带约束的筛选器以将人添加到静态列表](./assets/people-list-static-add-people-filters.png){width="800" zoomable="yes"}

1. 单击&#x200B;**[!UICONTROL 完成]**&#x200B;以保存更改。

   系统处理请求并在添加人员时显示确认消息。 处理时间取决于要评估的人员数量以及您选择的筛选标准。 在列表继续填充时，使用&#x200B;_[!UICONTROL 更多]_&#x200B;菜单中的&#x200B;**[!UICONTROL 刷新成员]**&#x200B;刷新列表。

   合格成员在短暂延迟后出现在列表中。 过滤器集只评估一次，因此以后匹配过滤器的人不会自动添加。 您可以随时重复此过程以将更多人员添加到列表中。

   静态联系人列表的![成员](./assets/people-list-static-members.png){width="700" zoomable="yes"}

## 移除成员 {#static-list-remove-members}

您可以使用[!UICONTROL 从人员列表中删除]操作，通过历程自动从静态列表中删除人员。 （请参阅[在历程中使用人员列表](./people-lists-journeys.md)）

<!--
TODO: Restore this section when the activate to a destination function is released.

## Activate to a destination {#static-list-activate}

Activating a static people list sends its membership to a connected destination, with ongoing sync instead of a one-time export. This is useful for paid media targeting, suppression, and downstream orchestration.

* The static list acts as a container for the people.
* The activation sends and syncs that membership to a destination.
* People added to the list later are propagated automatically.
* People removed later are deactivated automatically.

>[!PREREQUISITES]
>
>You must have one or more configured destinations for your [!DNL Journey Optimizer B2B Edition] sandbox before you can activate a static list to a destination. See [Destinations](./destinations.md).

1. Select the **[!UICONTROL Static lists]** tab.

1. Locate the static list that you want to activate, click the _More menu_ ( **...** ) icon next to the list, and choose **[!UICONTROL Activate to destination]**.

   ![Access the More menu for a static people list](./assets/people-lists-static-more-menu.png){width="450"}

   You can also open the static list and use the **[!UICONTROL More]** menu at the top right.

1. Select the check box for the configured destination connection.

   ![Configured destinations available for activation](./assets/people-list-activate-destination-select.png){width="600" zoomable="yes"}

1. Click **[!UICONTROL Save]**.

1. In the _[!UICONTROL Activate list to destination]_ dialog, click **[!UICONTROL Activate]** to confirm.

When activation completes, a confirmation message appears and the destination shows as **[!UICONTROL Active]** on the **[!UICONTROL Destinations]** tab of the list. You can activate a static list to more than one destination at a time. Membership syncs to all of them.

To review the destinations that a static list is activated to, open the list and select the **[!UICONTROL Destinations]** tab.

### Deactivate a destination {#deactivate-destination}

Remove a destination connection from a static list when you no longer want its membership synced downstream.

1. Open the static list and select the **[!UICONTROL Destinations]** tab.

1. Use the row action to remove the destination that you want to disconnect.

1. Confirm in the _[!UICONTROL Deactivate destination]_ dialog.

Deactivating removes the destination from the list. The people in the list are also removed from the connected destination audience.

-->
