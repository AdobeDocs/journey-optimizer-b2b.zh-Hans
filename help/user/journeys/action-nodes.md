---
title: 执行操作
description: 为帐户和人员操作配置操作节点 — 发送电子邮件，更新购买群组，更改得分，以及在Journey Optimizer B2B edition中与Marketo Engage集成。
feature: Account Journeys
role: User
exl-id: 167cb627-96ee-42a8-8657-bb8040bb4bfe
source-git-commit: 3013da8c7178c68ec07bf8d8b56f4ca06c043486
workflow-type: tm+mt
source-wordcount: '1674'
ht-degree: 2%

---

# 执行操作

在您的帐户历程中，您可以添加&#x200B;_[!UICONTROL 执行操作]_&#x200B;节点以执行操作，例如发送电子邮件、更改分数、分配给购买组等。 操作通常是您希望因某种类型的触发器（例如事件或上一个操作）而发生的操作。

![视频](../../assets/do-not-localize/icon-video.svg){width="30"} [观看概述视频](#overview-video)

## 帐户操作

当您想要将更改应用到节点路径上属于帐户的所有人员时，请使用对帐户执行的操作。

### 操作和限制 {#account-action-constraints}

| 操作 | 约束 |
| ------ | ----------- |
| [!UICONTROL 帐户有趣的时刻] | 类型（电子邮件、里程碑或Web）<br/>描述（可选） |
| [!UICONTROL 激活到目标] | 选择一个目标 |
| [!UICONTROL 将帐户添加到（其他）历程] | 选择实时帐户历程 |
| [!UICONTROL 添加到帐户列表] | 选择实时静态帐户列表 |
| [!UICONTROL 从历程中删除帐户] | 选择实时帐户历程 |
| [!UICONTROL 从帐户列表中删除] | 选择实时静态帐户列表 |
| [!UICONTROL 发送销售警报] | 选择感兴趣的解决方案<br/>发送电子邮件至 |
| [!UICONTROL 更新帐户配置文件] | 选择属性<br/>新值 |
| [!UICONTROL 更新购买团体阶段] | 选择解决方案兴趣<br/>选择购买团体阶段 |
| [!UICONTROL 更新购买团体状态] | 选择感兴趣的解决方案<br/>状态（必需，最多50个字符） |

>[!NOTE]
>
>2025.10版本弃用&#x200B;_[!UICONTROL 帐户更改数据值]_&#x200B;操作。 已由&#x200B;_[!UICONTROL 简化的体系结构]_.[的](../simplified-architecture.md)更新帐户配置文件<br/>替换
>
>管理员可以通过更新&#x200B;_[!UICONTROL XDM类]_ > _[!UICONTROL 标准类]_&#x200B;中的字段来配置XDM业务帐户的可用属性。 有关详细信息，请参阅[标准类](../admin/xdm-field-management.md#standard-classes)。

### 添加基于帐户的操作

1. 导航到历程图。

1. 单击路径上的加号( **+** )图标，然后选择&#x200B;**[!UICONTROL 执行操作]**。

   ![添加历程节点 — 执行操作](./assets/add-node-action.png){width="400"}

1. 在右侧的节点属性中，为操作选择&#x200B;**[!UICONTROL 帐户]**。

1. 从列表中选择一个操作，并设置该操作的任何值。

   ![历程节点 — 对帐户执行操作](./assets/node-take-action-account.png){width="700" zoomable="yes"}

>[!BEGINSHADEBOX]

### 激活到LinkedIn目标

对帐户使用&#x200B;_激活到目标_&#x200B;操作，直接从历程将帐户激活到Experience Platform目标。 此操作可让您将符合条件的帐户（基于购买组过滤器、参与度得分和其他标准）推送到受支持目标的匹配受众。 It

从2025.10版本开始，**_LinkedIn_**&#x200B;是第一个受支持的目标类型。 使用适用于LinkedIn目标的操作，通过消除多系统切换并减少延迟来简化营销活动执行。 例如，作为营销人员，您可以在关键购买角色缺失时自动将高意图帐户激活到LinkedIn以进行重定向，或根据非活动过滤器重新吸引休眠帐户。

有关为LinkedIn目标使用帐户匹配受众的详细信息，请参阅[LinkedIn帐户匹配受众](../data/linkedin-account-matched-audiences.md)。

+++ 设置对LinkedIn目标的帐户激活

1. 在历程画布中选择&#x200B;_执行操作_&#x200B;节点后，将帐户&#x200B;**[!UICONTROL 上的]**&#x200B;操作设置为&#x200B;**[!UICONTROL 激活到目标]**。

1. 单击&#x200B;**[!UICONTROL 选择目标]**。

   ![历程节点 — 对帐户执行操作 — 激活到目标](./assets/node-activate-destination-select-destination.png){width="600" zoomable="yes"}

1. 在对话框中，选择配置的LinkedIn目标并单击&#x200B;**[!UICONTROL 保存]**。

![历程节点 — 对帐户执行操作 — 激活到目标 — 选择目标对话框](./assets/node-activate-destination-select-destination-dialog.png){width="700" zoomable="yes"}

1. 输入用于标识目标中已激活受众的&#x200B;**[!UICONTROL 受众名称]**。

   ![历程节点 — 对帐户执行操作 — 激活到目标 — 完成的设置](./assets/node-activate-destination-settings.png){width="550" zoomable="yes"}

+++

>[!ENDSHADEBOX]

## 人员操作

当您要将更改应用于节点路径上的所有人员时，可对人员执行操作。 此节点类型可以按人员拆分路径内使用，也可以按帐户拆分路径内使用。

### 操作和限制 {#people-action-constraints}

| 上下文 | 操作 | 约束 |
| ------- | ------ | ----------- |
| [Journey Optimizer B2B](#journey-optimizer-b2b-actions) | [!UICONTROL 添加到外部客户受众] | 选择外部客户受众 |
| | [!UICONTROL 分配给购买组] | 选择感兴趣的解决方案<br/>选择角色 |
| | [!UICONTROL 更改得分] | 得分名称<br/>得分更改 |
| | [!UICONTROL 个人有趣的时刻] | 类型<br/>描述 |
| | [!UICONTROL 从购买群中删除] | 选择解决方案兴趣 |
| | [!UICONTROL 发送电子邮件] | 从Marketo Engage创建新电子邮件<br/>选择电子邮件 |
| | [!UICONTROL 发送短信] | 创建短信 |
| | [!UICONTROL 更新人员配置文件] | 选择人员属性<br/>设置新值 |
| [Marketo Engage](#marketo-engage-actions) | [!UICONTROL 添加到Marketo Engage请求营销活动] | 选择Marketo Engage工作区<br/>选择请求营销活动 |
| | [!UICONTROL 添加到Marketo列表] | 选择外部Marketo连接的名称<br/>列表名称 |
| | [!UICONTROL 从Marketo列表中删除] | 选择外部Marketo连接的名称<br/>列表名称 |

>[!NOTE]
>
>Marketo Engage中的&#x200B;_[!UICONTROL 更改人员分区]_&#x200B;操作在2025.10版本中已弃用，并且在Journey Optimizer B2B edition的[简化架构](../simplified-architecture.md)中不可用。<br/>
>
>2025.10版本弃用&#x200B;_[!UICONTROL 更改数据值]_&#x200B;操作。 在简化的架构中，它已被替换为&#x200B;_[!UICONTROL 更新人员配置文件]_。

### 添加基于人员的操作

1. 导航到历程图。

1. 单击路径上的加号( **+** )图标，然后选择&#x200B;**[!UICONTROL 执行操作]**。

1. 在右侧的节点属性中，为操作选择&#x200B;**[!UICONTROL 人员]**。

1. 从列表中选择一个操作，并设置该操作的任何值。

![历程节点 — 对人员执行操作](./assets/node-take-action-people.png){width="700" zoomable="yes"}

### Journey Optimizer B2B操作

Journey Optimizer B2B基于人员的操作旨在通过配置的渠道管理通信，并管理购买组和帐户中的人员分类。 当具有人员配置文件的合格帐户到达节点时，历程将应用操作。

+++[!UICONTROL 添加到外部客户受众]

使用此操作可将人员推送至外部受众，该受众可通过付费媒体渠道激活，以进一步定位购买群组的成员。 此操作通过Real-Time CDP B2B/P版本执行。

>[!NOTE]
>
>当具有人员配置文件的合格帐户到达已发布历程中的&#x200B;_添加到外部客户受众_&#x200B;节点时，这些配置文件可能需要48小时才能填充到外部受众中。

![执行操作 — 添加到外部客户受众](./assets/node-action-add-to-external-audience-options.png){width="300"}

选择此基于人员的操作时，您可以创建新外部受众或从现有外部受众中选择。 对于现有受众，您可以从仅在Journey Optimizer B2B edition中创建的外部客户受众中进行选择。 在创建受众并将其用于此历程操作时，请确保连接目标。 有关详细信息，请参阅Experience Platform文档中的[创建新的目标连接](https://experienceleague.adobe.com/zh-hans/docs/experience-platform/destinations/ui/connect-destination){target="_blank"}和[激活概述](https://experienceleague.adobe.com/zh-hans/docs/experience-platform/destinations/ui/activate/activation-overview#activate-audiences-from-the-destinations-catalog){target="_blank"}。

![视频](../../assets/do-not-localize/icon-video.svg){width="30"} [观看付费媒体编排的视频概述](../data/linkedin-account-matched-audiences.md#orchestrate-paid-media-engagement)

创建外部受众(_T):_

1. 选择&#x200B;**[!UICONTROL 新建]**。

1. 单击&#x200B;**[!UICONTROL 创建外部客户受众]**。

1. 为新外部受众输入&#x200B;**[!UICONTROL 名称]**（必需）和&#x200B;**[!UICONTROL 描述]**（可选）。

   ![添加到外部客户受众 — 创建受众](./assets/node-action-add-to-external-create-new.png){width="300"}

1. 单击&#x200B;**[!UICONTROL 创建]**。

   系统会创建新受众并显示确认消息。 然后，您可以继续将其用作节点操作的现有受众。

   >[!NOTE]
   >
   >从Journey Optimizer B2B edition创建新的外部客户受众时，将植入一个虚拟记录(`test@email.com`)。 将第一个实际用户档案添加到历程的外部受众后，就会覆盖此记录。

使用现有受众(_T):_

1. 单击&#x200B;**[!UICONTROL 选择外部客户受众]**。

1. 在对话框中，选择要使用的受众。

   ![添加到外部客户受众 — 添加受众](./assets/node-action-add-to-external-audience-select.png){width="700" zoomable="yes"}

1. 单击&#x200B;**[!UICONTROL 添加受众]**。

+++

+++[!UICONTROL 分配给购买组]

使用此操作可根据所选的解决方案兴趣和角色，将人员配置文件添加到[购买群](../buying-groups/buying-groups-overview.md)。

![执行操作 — 添加到购买组](./assets/node-action-add-to-buying-group.png){width="300"}

+++

+++[!UICONTROL 更改得分]

使用此操作可更改Marketo Engage中的人员得分。 [了解详情](https://experienceleague.adobe.com/zh-hans/docs/marketo-learn/tutorials/lead-and-data-management/lead-scoring-learn){target="_blank"}

![执行操作 — 更改得分](./assets/node-action-change-score.png){width="300"}

+++

+++[!UICONTROL 个人有趣的时刻]

使用此操作记录人们的有趣时刻。 选择类型（电子邮件、里程碑或Web）并添加说明（可选）。

![采取行动 — 人员有趣的时刻](./assets/node-action-person-interesting-moment.png){width="300"}

+++

+++[!UICONTROL 从购买群中删除]

使用此操作可根据所选的解决方案兴趣从[购买群](../buying-groups/buying-groups-overview.md)中删除人员配置文件。

![执行操作 — 添加到购买组](./assets/node-action-remove-from-buying-group.png){width="300"}

+++

+++[!UICONTROL 发送电子邮件]

使用此操作发送电子邮件。 在您[为节点](../content/add-email.md#add-an-email-to-your-journey)创建电子邮件后，您可以在电子邮件设计空间设计、个性化和预览电子邮件（请参阅[电子邮件创作](../content/email-authoring.md)）。 您还可以从Marketo Engage[发送](https://experienceleague.adobe.com/zh-hans/docs/marketo/using/product-docs/email-marketing/general/creating-an-email/create-an-email){target="_blank"}电子邮件。 选择Marketo Engage工作区，然后选择要发送的电子邮件。

![执行操作 — 发送电子邮件](./assets/node-action-send-email-from-marketo.png){width="300"}

+++

+++[!UICONTROL 发送短信]

使用此操作可发送短信消息。 您可以在可视设计空间创建、个性化和预览短信消息（请参阅[短信创作](../content/sms-authoring.md)）。

![执行操作 — 发送短信](./assets/node-action-send-sms.png){width="300"}

+++

+++[!UICONTROL 更新人员配置文件]

使用此操作更改[人员配置文件属性](../admin/field-mapping.md#xdm-business-person-attributes)的值。 选择属性，然后设置新值。

![执行操作 — 更新人员配置文件](./assets/node-action-update-person-profile.png){width="300"}

>[!NOTE]
>
>_[!UICONTROL 更新人员配置文件]_&#x200B;替换了&#x200B;_[!UICONTROL 简化架构]_.[上的](../simplified-architecture.md)更改数据值<br/>操作
>
>管理员可以通过更新&#x200B;_[!UICONTROL XDM类]_ > [!UICONTROL 标准类]中的字段来配置XDM个人配置文件的可用属性。 有关详细信息，请参阅[标准类](../admin/xdm-field-management.md#standard-classes)。

+++

### Marketo Engage操作

Marketo Engage基于人员的操作可协调您在Journey Optimizer B2B edition中基于帐户的营销编排与Marketo Engage中基于商机的营销工作。 使用这些操作可编排列表成员资格并请求营销活动。

>[!NOTE]
>
>Marketo Engage操作需要配置与一个或多个外部Marketo Engage实例的集成。<!-- For detailed information about configuring these connections, see #. -->

例如，您可能希望在Marketo Engage中禁止属于Journey Optimizer B2B edition中的购买组的用户的促销活动。 在这种情况下，您可以在Marketo Engage中专门为解决方案利益创建一个静态列表。 然后，在购买群的分割路径上，使用历程节点中的&#x200B;_添加到Marketo列表_&#x200B;操作。 此操作将购买组成员添加到连接的Marketo Engage实例中的特定静态列表。 然后，在Marketo Engage中将以解决方案兴趣为中心的静态列表用于智能列表筛选器。

+++[!UICONTROL 添加到Marketo Engage请求营销活动]

使用此操作可将人员配置文件添加到Marketo Engage中的[请求营销活动](https://experienceleague.adobe.com/zh-hans/docs/marketo/using/product-docs/core-marketo-concepts/smart-campaigns/flow-actions/request-campaign){target="_blank"}。

首先，选择一个连接的Marketo Engage实例。 接下来，选择请求营销活动名称。

![执行操作 — 添加到Marketo Engage请求营销活动](./assets/node-action-add-to-request-campaign-options.png){width="300"}

+++

+++[!UICONTROL 添加到Marketo列表]

使用此操作将人员添加到Marketo Engage中的[静态列表](https://experienceleague.adobe.com/zh-hans/docs/marketo/using/product-docs/core-marketo-concepts/smart-lists-and-static-lists/static-lists/understanding-static-lists){target="_blank"}。

首先，选择一个连接的Marketo Engage实例。 接下来，选择列表名称。

![执行操作 — 添加到Marketo列表](./assets/node-action-add-to-list-options.png){width="300"}

+++

+++[!UICONTROL 从Marketo列表中删除]

使用此操作可从Marketo Engage中的[静态列表](https://experienceleague.adobe.com/zh-hans/docs/marketo/using/product-docs/core-marketo-concepts/smart-lists-and-static-lists/static-lists/understanding-static-lists){target="_blank"}中删除人员。

首先，选择一个连接的Marketo Engage实例。 接下来，选择列表名称。

![执行操作 — 从Marketo列表中删除](./assets/node-action-remove-from-list-options.png){width="300"}

+++

## 概述视频

>[!VIDEO](https://video.tv.adobe.com/v/3443255/?captions=chi_hans&learn=on)
