---
title: 侦听事件节点
description: 占位符
autotag-review: '2026-06-12T23:00:36.531Z'
TQID: 'https://experienceleague.adobe.com/SBEfrrIKSCnO5x1tGXQTz1EZryH0IKhQx4tuqVn78FI'
product_v2: id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2: id: a4b836d9-ffdd-4df3-a62a-f78b830cf059id: aed878b8-11d0-487c-828b-d23b2051ec37
subfeature_v2: id: d0031543-532c-4a26-8f90-01af2b91e6d0id: ba367494-9862-4596-bd6f-299c7e10a46bid: d270a788-eb1d-40ed-b74e-9158ed975b1f
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: bf2854a777f62ba2f74f79942ee3336b6e8ab9dd
workflow-type: tm+mt
source-wordcount: 165
ht-degree: 10%

---

# 侦听事件节点

添加&#x200B;_侦听事件_&#x200B;节点，以便在事件发生时将受众前进到历程中的下一步。

## 人员事件过滤器

| 过滤器 | 描述 |
| ------- | ----------- |
| 活动历史记录>电子邮件 | 电子邮件活动基于使用一封或多封选定的电子邮件评估的条件： <li>电子邮件中已点击的链接 <li>打开了电子邮件 |
| 活动历史记录>数据值已更改 | 对于选定的人员属性，发生值更改。 这些更改类型包括： <li>新值 <li>上一个值 <li>原因 <li>源 <li>活动日期 <li> 最低 次数 |

## 添加事件节点

1. 导航到历程图。

1. 单击路径上的加号( **+** )图标，然后选择&#x200B;**[!UICONTROL 侦听事件]**。

1. 在右侧的节点属性中，为事件类型选择&#x200B;**[!UICONTROL 人员]**。

   <!-- ![Journey node - listen to events on people](./assets/node-listen-events-people.png){width="700" zoomable="yes"} -->

1. 从列表中选择一个事件。

1. 单击&#x200B;**[!UICONTROL 编辑事件]**&#x200B;并定义该事件的详细信息。

>[!NOTE]
>
>侦听事件节点的超时功能当前不起作用，将在以后的阶段启用。
