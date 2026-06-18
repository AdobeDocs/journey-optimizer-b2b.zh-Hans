---
title: 执行操作节点
description: 占位符
autotag-review: '2026-06-12T22:58:21.806Z'
TQID: 'https://experienceleague.adobe.com/uR-WvNz3gA6V7yyN3RRXH-MggrmGb1qvu1CBhMZRuAc'
product_v2: id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2: id: a4b836d9-ffdd-4df3-a62a-f78b830cf059id: aed878b8-11d0-487c-828b-d23b2051ec37
subfeature_v2: id: af7eab5e-3580-4254-9f56-3c20b4f6ef42id: d270a788-eb1d-40ed-b74e-9158ed975b1f
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 0a877cc1fc0dfd9c3d8271c8f7be6a5e34a69a9a
workflow-type: tm+mt
source-wordcount: 821
ht-degree: 2%

---

# 执行操作节点

在人员历程中，当您想要将更改应用于节点路径上的所有人员时，对人员使用操作。

## 操作和限制 {#actions}

| 操作 | 约束 |
| ------ | ----------- |
| **[!UICONTROL 激活到目标]** | <li>选择或创建静态列表 <li>如果列表没有激活的目标，请激活列表 |
| **[!UICONTROL 将人员添加到历程]** | <li>选择计划的或实时历程 <li>未应用目标历程的受众条件 |
| **[!UICONTROL 添加到列表]** | <li>创建新的静态列表或选择现有列表 |
| **[!UICONTROL 添加到Marketo列表]** | <li>在Marketo Engage中选择静态列表 |
| **[!UICONTROL 更改数据值]** | <li>选择人员属性 <li>设置新值 |
| **[!UICONTROL 更改项目数据]** | <li>选择项目属性 <li>设置新值 |
| **[!UICONTROL 更改项目状态]** | <li>选择项目<li>选择新状态 |
| **[!UICONTROL 从列表中删除]** | <li>选择静态列表 <li>如果当前不是成员，则跳过人员 |
| **[!UICONTROL 从Marketo列表中删除]** | <li>在Marketo Engage中选择静态列表 <li>如果当前不是成员，则跳过人员 |
| **[!UICONTROL 从历程中删除人员]** | <li>选择实时历程 <li>如果当前不是目标历程成员，则跳过人员 |
| **[!UICONTROL 请求Marketo促销活动]** | <li>选择Marketo Engage营销活动 |
| **[!UICONTROL 发送电子邮件]** | <li>创建、编辑或使用人工智能个性化电子邮件 <li>发送时间优化（可选） |
| **[!UICONTROL 发送WhatsApp]** | <li>选择WhatsApp消息 |

## 添加操作节点 {#add-an-action-node}

1. 导航到历程画布。

1. 单击路径上的加号( **+** )图标，然后选择&#x200B;**[!UICONTROL 执行操作]**。

   ![单击历程路径上的“添加”图标](./assets/person-journey-canvas-add-node.png){width="200"}

1. 在右侧的节点属性中，从列表中选择一个操作并设置该操作的任何值。

+++激活到目标

使用此操作直接从历程将人员激活到Experience Platform目标。 选择目标并输入受众名称，以识别目标中的激活受众。

![执行操作 — 激活到目标](./assets/person-action-node-activate-to-destination.png){width="450"}

+++

+++[!UICONTROL 将人员添加到历程]

使用此操作将人员添加到其他计划或实时历程。 通过此操作添加的人员会立即添加到目标历程的受众；历程的受众标准不适用。

![执行操作 — 将人员添加到历程](./assets/person-action-node-add-to-journey.png){width="450"}

+++

+++[!UICONTROL 添加到列表]

使用此操作可在Journey Optimizer B2B Prime中将人员添加到静态列表。

![执行操作 — 添加到列表](./assets/person-action-node-add-to-list.png){width="450"}

选择下列选项之一：

* **[!UICONTROL 创建]** — 创建新的静态列表资源并向其中添加人员。 该列表可立即供Journey Optimizer B2B Prime中的其他资源使用。
* **[!UICONTROL 选择]** — 选择现有静态列表资源，您要在该资源中添加到达该节点的人员。

+++

+++[!UICONTROL 添加到Marketo列表]

使用此操作可将人员添加到Marketo Engage中的静态列表。

![执行操作 — 添加到Marketo列表](./assets/person-action-node-add-to-marketo-list.png){width="450"}

+++

+++[!UICONTROL 更改数据值]

使用此操作可更新人员记录上的属性值。 选择属性并设置新值。

>[!TIP]
>
>要清除属性的值，将该值设置为`NULL`。

![执行操作 — 更改数据值](./assets/person-action-node-change-data-value.png){width="450"}

+++

+++[!UICONTROL 更改项目数据]

使用此操作可更新项目属性的值。 选择程序属性并设置新值。

![执行操作 — 更改项目数据](./assets/person-action-node-change-program-data.png){width="450"}

+++

+++[!UICONTROL 更改项目状态]

使用此操作可更改Marketo Engage项目中人员的状态。 选择程序，然后选择新状态。

![执行操作 — 更改项目状态](./assets/person-action-node-change-status-program.png){width="450"}

+++

+++[!UICONTROL 从列表中删除]

使用此操作可从Journey Optimizer B2B Prime的静态列表中删除人员。 如果某个人当前不是该列表的成员，则会为该人员跳过该操作。

![执行操作 — 从列表中删除](./assets/person-action-node-remove-from-list.png){width="450"}

+++

+++[!UICONTROL 从Marketo列表中删除]

使用此操作可从Marketo Engage的静态列表中删除人员。 如果某个人当前不是该列表的成员，则会为该人员跳过该操作。

![执行操作 — 从Marketo列表中删除](./assets/person-action-node-remove-from-marketo-list.png){width="450"}

+++

+++[!UICONTROL 从历程中删除人员]

使用此操作可将人员从其他实时人员历程中删除。 该人员将立即从目标历程中删除，并且不会对其执行进一步操作。 如果人员当前不是目标历程的成员，则会为该人员跳过操作。

![执行操作 — 从历程中删除人员](./assets/person-action-node-remove-from-journey.png){width="450"}

+++

+++[!UICONTROL 请求Marketo促销活动]

使用此操作可在连接的Marketo Engage实例中将人员添加到请求营销活动。 选择要请求的Marketo Engage营销活动。

![执行操作 — 请求Marketo营销活动](./assets/person-action-node-request-marketo-campaign.png){width="450"}

+++

+++[!UICONTROL 发送电子邮件]

使用此操作向已选择加入的人员发送电子邮件。 取消订阅、列入阻止列表、电子邮件已暂停或营销已暂停的用户将跳过此操作。

![执行操作 — 发送电子邮件](./assets/person-action-node-send-email.png){width="450"}

您可以创建电子邮件、编辑现有电子邮件或使用AI个性化电子邮件。 有关创建和编辑电子邮件的信息，请参阅[电子邮件渠道](../marketing/email-channel.md)。

您可以使用[发送时间优化](../marketing/email-send-time-optimization.md)，通过预测每个用户档案最有可能参与的时间，使电子邮件投放时间个性化。

+++

+++[!UICONTROL 发送WhatsApp]

使用此操作发送WhatsApp消息。 您可以在可视设计空间创建、个性化和预览WhatsApp消息（请参阅[WhatsApp创作](../content/whatsapp-authoring.md)）。

![执行操作 — 发送WhatsApp](./assets/person-action-node-send-whatsapp.png){width="450"}

+++
