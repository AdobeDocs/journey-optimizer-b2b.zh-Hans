---
title: 在历程中使用帐户列表
description: 在Journey Orchestration中使用帐户列表，并在Journey Optimizer B2B Edition中动态添加/删除帐户。
feature: Account Lists, Account Journeys
role: User
exl-id: 7cda080d-6263-4ccd-b144-432e4e78c298
autotag-review: 2026-03-27T22:29:03.719Z
TQID: 'https://experienceleague.adobe.com/FokJGxTj7abTN01WCcrVLDEuNLW0oI-i-8z0j-rFBO4'
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
    internal-label: Journey Optimizer B2B Edition
feature_v2:
  - id: e935834c-48b7-43d8-b754-a815196a1b05
    internal-label: Account lists
  - id: a4b836d9-ffdd-4df3-a62a-f78b830cf059
    internal-label: Journeys
subfeature_v2:
  - id: c31bc6c7-76bc-467b-80c0-7315a4e3f6be
    internal-label: Account Journeys
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
topic_v2:
  - id: d00e9f03-e50b-4162-b143-0c0817c937c2
    internal-label: Customer journeys
source-git-commit: d713d57bddf2ac6f8cf7e7a7d163281f607d729c
workflow-type: tm+mt
source-wordcount: '914'
ht-degree: 0%
---
# 在历程中使用帐户列表

您可以通过多种方式将实时（已发布）帐户列表合并到帐户历程中。

## 帐户受众节点

所有帐户历程都以&#x200B;[_帐户受众_&#x200B;节点](../journeys/account-audience-nodes.md)开始。 将此节点设置为使用帐户列表时，成员帐户将在历程上线（发布）时移动历程。

1. 为起始&#x200B;_帐户受众_&#x200B;节点选择&#x200B;**[!UICONTROL 帐户列表]**&#x200B;选项。

   ![为帐户受众节点选择帐户列表选项](../journeys/assets/node-audience-account-list.png){width="500"}

1. 单击&#x200B;**[!UICONTROL 添加帐户列表]**。

1. 选中帐户列表的复选框，然后单击&#x200B;**[!UICONTROL 保存]**。

   ![为帐户受众节点选择帐户列表选项](../journeys/assets/node-audience-account-list-select-dialog.png){width="600" zoomable="yes"}

## 执行操作节点 — 添加到帐户

**_仅限静态帐户列表_**

在帐户历程中，使用[a _执行操作_&#x200B;节点](../journeys/action-nodes.md)将帐户添加到静态帐户列表。

例如，您有一个历程路径，您可以在其中发送电子邮件，并且一些帐户会执行各种操作作为响应。 您将此活动视为历程中的资格点。 利用资格，您希望将它们添加到帐户列表，该帐户列表用作另一个历程的受众，该历程具有不同的合格帐户流程。

>[!NOTE]
>
>如果执行节点时帐户已位于列表中，则将忽略该操作。

1. 选择&#x200B;]_**[!UICONTROL 帐户]**上的_[!UICONTROL &#x200B;操作选项。

1. 若要对帐户&#x200B;]_执行_[!UICONTROL &#x200B;操作，请选择&#x200B;**[!UICONTROL 添加到帐户列表]**。

   ![选择“添加到帐户列表”](../journeys/assets/node-action-account-add-to-account-list.png){width="500"}

1. 对于&#x200B;**[!UICONTROL 选择实时静态帐户列表]**，选择要添加帐户的帐户列表。

   ![选择“添加到帐户列表”](../journeys/assets/node-action-account-add-to-account-list-select.png){width="500"}

## 执行操作节点 — 从帐户中删除

**_仅限静态帐户列表_**

在帐户历程中，使用[a _执行操作_&#x200B;节点](../journeys/action-nodes.md)从静态帐户列表中删除帐户。

例如，您有一个历程路径，您可以在其中发送电子邮件，并且一些帐户会执行各种操作作为响应。 您将此活动视为历程中的资格点。 通过此资格，您要将他们从帐户列表中删除。 此列表用作另一历程的受众，该历程会发送其他电子邮件，以便您不会复制资格信息。

>[!NOTE]
>
>如果某个帐户不在计划删除的列表中，则该操作将被忽略。

1. 选择&#x200B;]_**[!UICONTROL 帐户]**上的_[!UICONTROL &#x200B;操作选项。

1. 若要对帐户&#x200B;]_执行_[!UICONTROL &#x200B;操作，请选择&#x200B;**[!UICONTROL 从帐户列表中删除]**。

   ![选择“从帐户列表中移除”](../journeys/assets/node-action-account-remove-from-account-list.png){width="500"}

1. 对于&#x200B;**[!UICONTROL 选择实时静态帐户列表]**，选择要从中删除帐户的帐户列表。

   ![选择“从帐户列表中移除”](../journeys/assets/node-action-account-remove-from-account-list-select.png){width="500"}

## 拆分路径节点 — 帐户列表的帐户成员 {#split-paths-account-member-of-account-list}

**_仅限帐户历程_**

在按帐户拆分的&#x200B;[_拆分路径_&#x200B;节点](../journeys/split-merge-paths-nodes.md#add-a-split-path-by-account-node)中使用帐户列表的&#x200B;_[!UICONTROL 帐户成员]_&#x200B;筛选器。 该帐户是或不是一个或多个所选帐户列表的成员。 要在列表中包括帐户，请将成员资格设置为`true`，或将其设置为`false`以排除这些帐户。

若要排除阻止列表上的帐户，请添加&#x200B;_[!UICONTROL 帐户列表的成员]_&#x200B;筛选器，将成员资格设置为`false`，然后选择该列表。

1. 导航到历程图。

1. 单击路径上的加号( **+** )图标，然后选择&#x200B;**[!UICONTROL 拆分路径]**。

1. 在右侧的节点属性中，为拆分选择&#x200B;**[!UICONTROL 帐户]**。

1. 要为&#x200B;_[!UICONTROL 路径1]_&#x200B;定义条件，请单击&#x200B;**[!UICONTROL 应用条件]**。

1. 定义帐户列表筛选器。

   * 在条件编辑器中，展开&#x200B;_[!UICONTROL 特殊筛选器]_&#x200B;文件夹，并将&#x200B;**[!UICONTROL 帐户列表的帐户成员]**&#x200B;筛选器拖到条件工作区上。

   * 要在列表中包括帐户，请将成员资格设置为`true`，或将其设置为`false`以排除这些帐户。

   * Select一个或多个帐户列表。

   ![使用帐户列表筛选器的帐户成员拆分路径条件编辑器](./assets/account-lists-journeys-split-path-account-filter.png){width="700" zoomable="yes"}

   您可以将帐户列表成员资格筛选器与其他帐户筛选器组合，并选择匹配所有条件或任何条件。 通过在顶部应用&#x200B;**[!UICONTROL 筛选器逻辑]**&#x200B;优化条件。

1. 单击&#x200B;**[!UICONTROL 完成]**。

继续配置拆分路径节点，如[按帐户节点添加拆分路径](../journeys/split-merge-paths-nodes.md#add-a-split-path-by-account-node)中所述。

## 拆分路径节点 — 帐户列表中的人员成员 {#split-paths-member-of-account-list}

**_仅限人员历程_**

在人员历程的&#x200B;[_拆分路径_&#x200B;节点](../journeys/split-merge-paths-nodes.md)中使用帐户列表成员资格筛选器，根据人员的帐户是否为帐户列表的成员来路由人员。 提供了两个过滤器：

| 过滤器 | 描述 |
| ------ | ----------- |
| [!UICONTROL 帐户动态列表的成员] | 人员的帐户是否属于一个或多个动态帐户列表。 |
| [!UICONTROL 帐户静态列表的成员] | 此人的帐户是否属于一个或多个静态帐户列表。 |

若要从培养路径中排除列入阻止列表帐户中的人员，请添加&#x200B;_[!UICONTROL 帐户静态列表的人员成员]_&#x200B;筛选器，将运算符设置为`is not`，然后选择该列表。

1. 导航到历程图。

1. 单击路径上的加号( **+** )图标，然后选择&#x200B;**[!UICONTROL 拆分路径]**。

1. 要为&#x200B;_[!UICONTROL 路径1]_&#x200B;定义条件，请单击&#x200B;**[!UICONTROL 应用条件]**。

1. 定义帐户列表筛选器

   * 在条件编辑器中，展开&#x200B;_[!UICONTROL 特殊筛选器]_&#x200B;文件夹，并将&#x200B;**[!UICONTROL 帐户动态列表的人员成员]**&#x200B;或&#x200B;**[!UICONTROL 帐户静态列表的人员成员]**&#x200B;筛选器拖动到条件工作区。

   * 要包含帐户在列表中的人员，请将运算符设置为`is`，或将其设置为`is not`以排除这些人员。

   * Select一个或多个帐户列表。

     ![使用帐户列表筛选器的人员成员拆分路径条件编辑器](./assets/account-lists-journeys-split-path-person-member-account-filter.png){width="700" zoomable="yes"}

   您可以将帐户列表成员资格筛选器与其他人员筛选器组合，并选择匹配所有条件或任何条件。 通过在顶部应用&#x200B;**[!UICONTROL 筛选器逻辑]**&#x200B;优化条件。

1. 单击&#x200B;**[!UICONTROL 完成]**。

继续配置拆分路径节点，如[按人员添加拆分路径](../journeys/split-merge-paths-nodes.md#add-a-split-path-by-people-node)中所述。
