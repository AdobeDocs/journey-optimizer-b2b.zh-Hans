---
title: 销售警报电子邮件
description: 了解如何在帐户历程中包含自动销售警报电子邮件。
feature: Email Authoring, Account Journeys
role: User
exl-id: 01bffbce-6c73-483a-8731-de4e5569cf61
source-git-commit: 4a54548ad061fc778fae3bc4b8499f3716850e4a
workflow-type: tm+mt
source-wordcount: '521'
ht-degree: 5%

---

# 销售警报电子邮件

_销售提醒电子邮件_&#x200B;表示将购买组移交给销售人员。 该电子邮件包含购买组的摘要以及有关购买组成员及其活动的信息。

作为营销人员，您可以在帐户历程中配置销售警报电子邮件节点，以提醒销售团队特定购买群组的历程已完成。 在该节点中，您可以指定销售团队的电子邮件地址或到达一组帐户的分配别名。

>[!IMPORTANT]
>
>确保贵组织的允许列表已更新，以便能够发送Sales alert电子邮件。 有关详细信息，请参阅[跟踪和电子邮件传递的协议](../start/email-protocols.md)。

## 电子邮件内容

+++示例销售警报电子邮件
![使用默认模板的销售警报电子邮件示例](./assets/sales-alert-email-example.png){width="500" zoomable="yes"}

+++

| 部分 | 名称 | 描述 |
| - | ---- | ----------- |
| 购买团体信息 | 购买团体名称 | 购买组的显示名称。 |
|   | 帐户名称 | 帐户的名称。 |
|   | 参与度评分 | 购买组的参与度分数，基于过去30天内的活跃参与活动。 |
|   | 完整性评分 | 购买组的完整性分数。 |
|   | 解决方案兴趣 | 与购买组相关的解决方案利息 |
|   | 状态 | 购买组的状态。 |
| 购买群组亮点 | 参与次数最多的成员 | 通过购买组成员参与度得分和角色，购买组的主要参与成员。 |
|   | 兴趣主题 | 内容参与中最常见的关键字，基于电子邮件、下载、聊天、PDF评论、活动摘要和网络研讨会问题。 |
|   | 缺少角色 | 模板中的必需角色，但在购买组中缺失。 |
| 购买团体摘要 | 活动摘要（由Generative AI提供支持） | 基于成员活动的人工智能生成的购买组摘要。 考虑过去30天的活动。 |
|   | 关键有趣时刻 | 最近与购买组成员有关的有趣时刻。 |
| 成员 | 四个购买成员的列表 | 按参与度得分和角色列出的前四个购买组成员的详细信息。 |
| 每个购买组成员 | 成员名称 | 购买组成员的名称。 |
|   | 标题 | 购买组成员的标题。 |
|   | 角色 | 成员的购买组角色。 |
|   | 参与度评分 | 购买组成员参与度分数。 得分基于过去30天的活跃参与活动。 |
|   | 上一个有趣的时刻 | 最近最有趣的时刻与成员有关。 |
|   | 最近活动 | 最近两个活动与购买组成员有关。 |
|   | 电子邮件ID | 购买组成员的电子邮件ID。 |
|   | 电话号码 | 购买组成员的电话号码。 |

## 在帐户历程中添加销售警报电子邮件操作

添加&#x200B;_[!UICONTROL 执行操作]_&#x200B;节点并执行以下操作时，您可以在帐户历程中设置销售警报电子邮件投放：

1. 对于&#x200B;_目标上的_&#x200B;操作，请选择&#x200B;**[!UICONTROL 帐户]**。

1. 若要对帐户&#x200B;_执行_&#x200B;操作，请选择&#x200B;**[!UICONTROL 发送销售警报]**。

1. 对于&#x200B;**[!UICONTROL 选择感兴趣的解决方案]**，请选择要用于生成的电子邮件内容的感兴趣的解决方案。

1. 对于&#x200B;**[!UICONTROL 发送电子邮件至]**，请输入要包含在投放中的各个电子邮件地址或别名。

   ![新建电子邮件对话框](assets/sales-alert-email-journey-node.png){width="600" zoomable="yes"}

   发布客户历程后，将根据这些参数发送销售警报。
