---
title: 添加历程节点
description: 人员历程节点的占位符页面。
autotag-review: '2026-06-12T23:02:52.147Z'
TQID: 'https://experienceleague.adobe.com/sTnrOvrGIrgboPqOMrrkUvNU1y6zZJX42zEJxuUInKQ'
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2:
  - id: a4b836d9-ffdd-4df3-a62a-f78b830cf059
  - id: aed878b8-11d0-487c-828b-d23b2051ec37
subfeature_v2:
  - id: d270a788-eb1d-40ed-b74e-9158ed975b1f
  - id: ba367494-9862-4596-bd6f-299c7e10a46b
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 2f4929e4fadeee87b9e31298d2a1de269fc007d5
workflow-type: tm+mt
source-wordcount: 1137
ht-degree: 2%

---

# 添加历程节点

创建人员历程后，添加受众并使用节点构建历程。 历程图提供了一个画布，您可以在其中构建多步骤B2B营销用例。

_[!UICONTROL 人员受众]_&#x200B;节点自动成为历程中的第一个节点。 选择受众后，通过将不同的操作、事件和设计节点组合为多步骤、跨渠道方案来构建旅程。 历程的每个节点表示逻辑路径上的一个步骤。

## 人员受众节点

人员受众节点指定哪些人员记录进入历程。 创建人员历程时，历程始终以定义其输入的人员受众节点开始。

1. 单击节点将其选定。
1. 在右侧的节点属性面板中，为人员受众历程节点使用以下输入选项之一：

   * **[!UICONTROL 动态列表]** — 使用基于规则的动态人员列表。 在历程运行时将评估列表规则，以限定历程的成员。 以后不符合动态列表资格的人不会从历程中删除。

   * **[!UICONTROL 静态列表]** — 使用静态人员列表作为历程的成员。 在历程运行时评估当前列表成员资格，以授予成员参加历程的资格。 以后从静态列表中删除的人员不会从历程中删除。

## 人员操作节点

在人员历程中，当您想要将更改应用于节点路径上的所有人员时，对人员使用操作。 对于帐户历程，此节点类型可以在拆分路径中按人员使用，也可以在拆分路径中按帐户使用。

### 操作和限制

| 操作 | 限制 |
| ------ | ---------- |
| **[!UICONTROL 发送电子邮件]** | <li>创建电子邮件 <li>发送时间优化（可选） |
| **[!UICONTROL 更改数据值]** | <li>选择人员属性 <li>设置新值 |

### 添加操作节点 {#add-an-action-node}

1. 导航到历程图。

1. 单击路径上的加号( **+** )图标，然后选择&#x200B;**[!UICONTROL 执行操作]**。

1. 在右侧的节点属性中，从列表中选择一个操作并设置该操作的任何值。

<!-- ![Person journey node - take an action](./assets/node-take-action-people.png){width="700" zoomable="yes"} -->

+++[!UICONTROL 发送电子邮件]

使用此操作发送电子邮件。 为节点创建电子邮件后，您可以在电子邮件设计空间设计、个性化和预览电子邮件（请参阅[电子邮件创作](../content/email-authoring.md)）。

<!-- ![Take an action - Send email](./assets/node-action-send-email-from-marketo.png){width="300"} -->

您可以使用[发送时间优化](../marketing/email-send-time-optimization.md)，通过预测每个用户档案最有可能参与的时间，使电子邮件投放时间个性化。

<!--
>[!NOTE]
>
>You can use email deduplication in account journeys to ensure that the same email is not sent multiple times to the same email address within a journey. For more information, see [Email deduplication](../content/email-deduplication.md).
-->

+++

+++[!UICONTROL 更改数据值]

使用此操作可更改数据库中人员配置文件属性的值。 选择属性，然后设置新值。

<!-- ![Take an action - Update person profile](./assets/node-action-update-person-profile.png){width="300"} -->

+++

## 事件节点

添加&#x200B;_侦听事件_&#x200B;节点，以便在事件发生时将受众前进到历程中的下一步。

### 人员事件过滤器

| 过滤器 | 描述 |
| ------- | ----------- |
| 活动历史记录>电子邮件 | 电子邮件活动基于使用一封或多封选定的电子邮件评估的条件： <li>电子邮件中已点击的链接 <li>打开了电子邮件 |
| 活动历史记录>数据值已更改 | 对于选定的人员属性，发生值更改。 这些更改类型包括： <li>新值 <li>上一个值 <li>原因 <li>源 <li>活动日期 <li> 最低 次数 |

### 添加事件节点

1. 导航到历程图。

1. 单击路径上的加号( **+** )图标，然后选择&#x200B;**[!UICONTROL 侦听事件]**。

1. 在右侧的节点属性中，为事件类型选择&#x200B;**[!UICONTROL 人员]**。

   <!-- ![Journey node - listen to events on people](./assets/node-listen-events-people.png){width="700" zoomable="yes"} -->

1. 从列表中选择一个事件。

1. 单击&#x200B;**[!UICONTROL 编辑事件]**&#x200B;并定义该事件的详细信息。

>[!NOTE]
>
>侦听事件节点的超时功能当前不起作用，将在以后的阶段启用。

## 拆分路径节点

使用拆分节点，根据您定义的条件进行人员分段。 根据条件为受众列表创建路径，使用区段的操作和事件节点定义每个路径，然后组合路径并继续历程。

“拆分路径”节点根据人员筛选器定义一个或多个分段路径。

<!-- A split based on a people filter is automatically closed with a merge paths node so that all people can move forward to the next step. Split by people paths can include only people actions. These paths cannot be split again and automatically join back. _not currently true_ -->


_&#x200B;**按人员节点划分的拆分路径的工作方式**&#x200B;_

* 每个路径的评估是从上到下。 如果人员与第一条和第二条路径匹配，则他们仅沿着第一条路径前进。
* 该节点支持&#x200B;_其他人员_&#x200B;路径的定义，您可以在其中添加与定义的区段/路径之一不匹配的人员的操作或事件。

### 匹配过滤器

对于您为节点定义的每个路径，使用以下过滤器类型根据一个或多个条件匹配人员：

* 活动历史记录 — 您可以根据与以下项相关的人员活动定义路径：

   * 电子邮件消息
   * 数据值更改

* 人员属性 — 根据人员的属性定义条件，例如国家/地区、职务或列表成员资格。

### 添加拆分路径节点

<!--
>[!NOTE]
>
>When you split paths by people, a _Close split paths_ node is automatically inserted to end the split. A split-by-people path allows only _Take an action_ on people nodes.
-->

1. 导航到历程图。

1. 单击路径上的加号( **+** )图标，然后选择&#x200B;**[!UICONTROL 拆分路径]**。

   <!-- ![Add journey node - split paths](./assets/add-node-split.png){width="300" zoomable="no"} -->

1. 要定义适用于&#x200B;_[!UICONTROL 路径1]_&#x200B;的条件，请单击&#x200B;**[!UICONTROL 应用条件]**。

1. 在条件编辑器中，添加一个或多个过滤器以定义拆分路径。

   * 从左侧导航中拖放任何人员筛选器并完成匹配定义。

   * 通过在顶部应用&#x200B;**[!UICONTROL 筛选器逻辑]**&#x200B;来优化条件。 您可以选择匹配所有条件或任一条件。

     <!-- ![Split path node - conditions person filter logic](./assets/node-split-conditions-people.png){width="700" zoomable="yes"} -->

   * 单击&#x200B;**[!UICONTROL 完成]**。

1. 要添加更多路径，请单击&#x200B;**[!UICONTROL 添加路径]**，然后重复上述步骤以添加适用于该路径的条件。

   您还可以根据这些条件标记每个路径或使用默认标签。

1. 如果需要，可根据所需的拆分优先级对路径重新排序。

   路径过滤将按自上而下的顺序进行计算。 每个人沿着第一个匹配的路径前进。

   单击每个路径卡右上角的向上和向下箭头，将其在路径列表中向上或向下移动。

   <!-- ![Split path node - reorder paths](./assets/node-split-reorder-paths-people.png){width="500" zoomable="yes"} -->

1. 启用&#x200B;**[!UICONTROL 其他人]**&#x200B;选项，为与定义的路径不匹配的人添加默认路径。

   未启用此选项时，与定义的区段/路径不匹配的用户将越过拆分，继续历程中的下一步。

为每个路径定义了条件后，您可以添加要应用于路径上人员的操作或事件节点。

## 合并路径节点

1. 导航到历程图并找到包含两个或更多路径的拆分路径节点。

   每个路径都应该包含每个路径上的操作和事件的组合。

1. 单击这些路径中任一路径末尾的加号( **+** )图标，然后从显示的选项中选择&#x200B;**[!UICONTROL 合并路径]**。

   <!-- ![Journey node - merge paths](./assets/node-plus-icon-merge-paths.png){width="400" zoomable="no"} -->

1. 在右侧的节点属性中，选择要合并的路径。

   <!-- ![Journey node - merge paths](./assets/node-merge-select-paths.png){width="600" zoomable="yes"} -->

   此时，路径会被合并，以便选定路径中的人合并到单个路径中，从而继续完成历程。

1. 如果需要，您可以通过导航回合并路径节点属性并清除要删除的任何路径的复选框来取消合并路径。
