---
title: 在历程和程序中使用帐户列表
description: 了解如何在历程中编排帐户列表成员资格，并根据帐户列表成员资格筛选Marketo Engage智能列表。
source-git-commit: 0845bff023741ebf8aca448c65950beceae77cf1
workflow-type: tm+mt
source-wordcount: '684'
ht-degree: 0%

---

# 在历程和程序中使用帐户列表

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

例如，您可能有一个发送电子邮件的历程路径，一些帐户会将各种操作作为响应操作。 您将此活动视为历程中的资格点，并希望将它们添加到帐户列表，该帐户列表用于作为另一个历程的受众，该历程具有不同的合格帐户流程。

>[!NOTE]
>
>如果执行节点时帐户已位于列表中，则将忽略该操作。

1. 选择&#x200B;_&#x200B;**[!UICONTROL 帐户]**&#x200B;上的_&#x200B;操作选项。

1. 若要对帐户&#x200B;_执行_&#x200B;操作，请选择&#x200B;**[!UICONTROL 添加到帐户列表]**。

   ![选择“添加到帐户列表”](../journeys/assets/node-action-account-add-to-account-list.png){width="500"}

1. 对于&#x200B;**[!UICONTROL 选择实时静态帐户列表]**，选择要添加帐户的帐户列表。

   ![选择“添加到帐户列表”](../journeys/assets/node-action-account-add-to-account-list-select.png){width="500"}

## 执行操作节点 — 从帐户中删除

**_仅限静态帐户列表_**

在帐户历程中，使用[a _执行操作_&#x200B;节点](../journeys/action-nodes.md)从静态帐户列表中删除帐户。

例如，您可能有一个发送电子邮件的历程路径，一些帐户会将各种操作作为响应操作。 您将此活动视为历程中的资格认证点，并想要将其从帐户列表中删除，该帐户列表用于作为另一历程的受众，该历程会发送其他电子邮件，以便您不会复制资格认证通信。

>[!NOTE]
>
>如果某个帐户不在计划删除的列表中，则该操作将被忽略。

1. 选择&#x200B;_&#x200B;**[!UICONTROL 帐户]**&#x200B;上的_&#x200B;操作选项。

1. 若要对帐户&#x200B;_执行_&#x200B;操作，请选择&#x200B;**[!UICONTROL 从帐户列表中删除]**。

   ![选择“添加到帐户列表”](../journeys/assets/node-action-account-remove-from-account-list.png){width="500"}

1. 对于&#x200B;**[!UICONTROL 选择实时静态帐户列表]**，选择要从中删除帐户的帐户列表。

   ![选择“添加到帐户列表”](../journeys/assets/node-action-account-remove-from-account-list-select.png){width="500"}

## Marketo Engage项目 — 帐户列表成员

作为营销人员，您可能希望在Marketo Engage中为属于Journey Optimizer B2B edition帐户列表的人员禁止显示项目。

在连接到Journey Optimizer B2B edition的Marketo Engage实例中，您可以使用智能列表中的&#x200B;_[!UICONTROL 帐户列表成员]_&#x200B;过滤器根据营销活动策略识别这些潜在客户。 有关智能列表的详细信息，请参阅[Marketo Engage文档](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/core-marketo-concepts/smart-lists-and-static-lists/understanding-smart-lists){target="_blank"}。

### 将筛选器添加到智能列表

1. 在Marketo Engage中，选择一个营销活动，然后单击&#x200B;**[!UICONTROL 智能列表]**&#x200B;选项卡。

1. 在右侧显示的筛选器列表中，输入`Member`并找到&#x200B;**[!UICONTROL 帐户列表的成员]**&#x200B;筛选器。

1. 将筛选器拖到“智能列表”画布上。

1. 在智能列表画布上，设置&#x200B;**[!UICONTROL 帐户]**&#x200B;的成员列表值。

   单击向下箭头显示所有帐户列表，或者输入部分帐户列表名称以帮助找到所需的帐户列表。

   针对帐户列表成员资格的![Marketo Engage智能列表筛选器](./assets/account-lists-marketo-engage-smart-list.png){width="800" zoomable="yes"}

1. 在营销活动流程中，添加&#x200B;**[!UICONTROL 添加到列表]**&#x200B;步骤，并从Journey Optimizer B2B edition帐户列表中选择要填充人员的列表。

   请参阅Marketo Engage文档中的&#x200B;_[将流程步骤添加到智能营销活动](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/core-marketo-concepts/smart-campaigns/flow-actions/add-a-flow-step-to-a-smart-campaign){target="_blank"}_，了解有关将步骤添加到流程的详细信息。

### 查看成员

流运行后，您可以查看列表中填充的人员的列表。 打开列表并选择“人员”选项卡。

![从帐户列表中填充的Marketo Engage促销活动列表](./assets/account-lists-marketo-engage-smart-list-people.png){width="800" zoomable="yes"}

