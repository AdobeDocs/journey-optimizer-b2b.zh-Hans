---
title: 人员受众历程节点
description: 人员历程的占位符页面。
autotag-review: '2026-06-16T21:21:01.614Z'
TQID: 'https://experienceleague.adobe.com/pk1NGg3M67oRieuCOZFdaguKl2bVkiZyEPVnJDTUBJs'
product_v2: id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2: id: a4b836d9-ffdd-4df3-a62a-f78b830cf059id: beb5f4be-cec3-471a-9db6-831a77dd3ac9id: aed878b8-11d0-487c-828b-d23b2051ec37
subfeature_v2: id: ba367494-9862-4596-bd6f-299c7e10a46bid: d270a788-eb1d-40ed-b74e-9158ed975b1f
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: b7cb8c2a43b8a562e55923d709f518b8f1d74b2a
workflow-type: tm+mt
source-wordcount: 212
ht-degree: 0%

---

# 人员受众节点

_人员受众_&#x200B;节点指定哪些人员配置文件进入历程。 当您[创建人员历程](./person-journeys.md)时，该历程始终以定义其输入的人员受众节点开始。 人员受众节点可以具有以下两种受众输入类型之一：静态人员列表或动态人员列表。

如果人员历程所需的人员列表不存在，请[创建人员列表](../audiences/audience-management.md#create-a-people-list)，然后配置Peson受众节点。

## 设置人员受众节点的受众

1. 单击&#x200B;**[!UICONTROL 人员受众]**&#x200B;节点。

   此操作在右侧显示节点属性。

   <!-- ![Person audience journey node](./assets/person-journey-person-audience-node.png){width="700" zoomable="yes"} -->

1. 在右侧的节点属性面板中，为人员受众历程节点使用以下输入选项之一：

   * **[!UICONTROL 动态列表]** — 使用基于规则的动态人员列表。 在历程运行时将评估列表规则，以限定历程的成员。 以后不符合动态列表资格的人不会从历程中删除。

   * **[!UICONTROL 静态列表]** — 使用静态人员列表作为历程的成员。 在历程运行时评估当前列表成员资格，以授予成员参加历程的资格。 以后从静态列表中删除的人员不会从历程中删除。

