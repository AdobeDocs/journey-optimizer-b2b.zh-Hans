---
title: 侦听事件节点
description: 在Journey Optimizer B2B edition Prime中配置侦听事件节点 — 设置事件触发器，应用可选过滤器，并在发生活动或数据更改时提升人员。
autotag-review: '2026-06-12T23:00:36.531Z'
TQID: 'https://experienceleague.adobe.com/SBEfrrIKSCnO5x1tGXQTz1EZryH0IKhQx4tuqVn78FI'
product_v2: id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2: id: a4b836d9-ffdd-4df3-a62a-f78b830cf059id: aed878b8-11d0-487c-828b-d23b2051ec37
subfeature_v2: id: d0031543-532c-4a26-8f90-01af2b91e6d0id: ba367494-9862-4596-bd6f-299c7e10a46bid: d270a788-eb1d-40ed-b74e-9158ed975b1f
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 3368f815edc0ce817cb7ed371157b63fa548d848
workflow-type: tm+mt
source-wordcount: 233
ht-degree: 8%

---

# 侦听事件节点

添加&#x200B;_侦听事件_&#x200B;节点，以便在事件发生时将受众前进到历程中的下一步。

## 事件触发器 {#event-triggers}

从PM获取列表

## 事件过滤器 {#event-filters}

从下午获取更新的列表

| 过滤器 | 描述 |
| ------- | ----------- |
| 活动历史记录>电子邮件 | 电子邮件活动基于使用一封或多封选定的电子邮件评估的条件： <li>电子邮件中已点击的链接 <li>打开了电子邮件 |
| 活动历史记录>数据值已更改 | 对于选定的人员属性，发生值更改。 这些更改类型包括： <li>新值 <li>上一个值 <li>原因 <li>源 <li>活动日期 <li> 最低 次数 |

## 添加事件节点 {#add-event-node}

1. 导航到历程画布。

1. 单击路径上的加号( **+** )图标，然后选择&#x200B;**[!UICONTROL 侦听事件]**。

   ![单击历程路径上的“添加”图标](./assets/person-journey-canvas-add-node.png){width="200"}

1. 在右侧的节点属性中，单击&#x200B;**[!UICONTROL 添加事件条件]**。

1. 在&#x200B;_[!UICONTROL 编辑事件]_&#x200B;对话框中，添加要触发的事件。

   ![编辑事件 — 事件触发器](./assets/edit-event-triggers.png){width="600" zoomable="yes"}

1. （可选）在对话框中选择&#x200B;**[!UICONTROL 筛选器]**&#x200B;选项卡，并为触发器添加筛选条件。

1. 单击&#x200B;**[!UICONTROL 编辑事件]**&#x200B;并定义该事件的详细信息。

   ![编辑事件 — 事件筛选](./assets/edit-event-filters.png){width="600" zoomable="yes"}

1. 单击&#x200B;**[!UICONTROL 保存]**。

<!--
1. If needed, set the **[!UICONTROL Timeout]** option to limit the time period to listen for the event.

   >[!NOTE]
   >
   >The journey ends after a timeout unless you define a timeout path, where you can add other nodes.

   Enable the **[!UICONTROL Timeout]** option and select the duration for which the journey waits for an event to occur before it times out.

   You can choose to end the path here or take a different course of action by setting another path. To create a new path in the journey where you can add actions and events applicable to accounts when the event does not occur, select the **[!UICONTROL Set timeout path]** check box.

   ![Journey event node - set timeout path](../../user/journeys/assets/node-event-timeout-set-path.png){width="700" zoomable="yes"}
-->

>[!NOTE]
>
>侦听事件节点的超时功能当前不起作用。 计划在以后的版本中发布。
