---
title: 人员受众历程节点
description: 在Journey Optimizer B2B中配置人员受众节点，以指定哪些用户档案使用动态人员列表或基于事件的受众进入历程。
badgeBeta: label="Beta 版" type="informative" tooltip="此功能当前为有限测试版"
autotag-review: '2026-06-16T21:21:01.614Z'
TQID: 'https://experienceleague.adobe.com/pk1NGg3M67oRieuCOZFdaguKl2bVkiZyEPVnJDTUBJs'
product_v2: id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2: id: a4b836d9-ffdd-4df3-a62a-f78b830cf059id: beb5f4be-cec3-471a-9db6-831a77dd3ac9id: aed878b8-11d0-487c-828b-d23b2051ec37
subfeature_v2: id: ba367494-9862-4596-bd6f-299c7e10a46bid: d270a788-eb1d-40ed-b74e-9158ed975b1f
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 6227b7f64baf307e3778e73bcceabb140ab65fb8
workflow-type: tm+mt
source-wordcount: 225
ht-degree: 4%

---

# 人员受众节点

_人员受众_&#x200B;节点指定哪些人员配置文件进入历程。 当您[创建人员历程](./person-journeys.md)时，该历程始终以定义其输入的人员受众节点开始。 人员受众节点可以具有以下两种受众输入类型之一：动态人员列表或事件触发器。

如果人员历程所需的动态人员列表不存在，请[创建人员列表](../audiences/people-lists.md#create-a-people-list)，然后配置人员受众节点。

配置历程受众(_T):_

1. 单击&#x200B;**[!UICONTROL 人员受众]**&#x200B;节点。

   此操作在右侧显示节点属性。

   ![人员受众历程节点](./assets/person-audience-node-properties.png){width="500" zoomable="yes"}

1. 对人员受众使用以下受众配置选项之一：

   * **[!UICONTROL 动态列表]** — 使用基于规则的动态人员列表。 在历程运行时将评估列表规则，以限定历程的成员。 以后不符合动态列表资格的人不会从历程中删除。 请参阅&#x200B;_[动态列表](../audiences/people-lists.md#dynamic-lists)_。

   * **[!UICONTROL 事件受众]** — 使用事件受众根据符合条件的事项定义历程受众。 使用人员配置文件筛选定义受众成员，并使用事件标准触发历程条目。 查看&#x200B;_[基于事件的受众](../audiences/event-based-audiences.md)_。
