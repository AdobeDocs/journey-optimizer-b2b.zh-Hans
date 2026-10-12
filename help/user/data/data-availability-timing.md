---
title: 数据可用性和同步计时
description: 了解数据更改在[!DNL Journey Optimizer B2B Edition]历程中的显示速度以及哪些时间线正常。
feature: Journeys, Data Management
role: User
autotag-review: '2026-10-08T18:36:33.252Z'
TQID: 'https://experienceleague.adobe.com/PA1IeRHnGWHmBtDpffzveoWIHOn99-Ctt4Y0OQb7CwE'
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
    internal-label: Journey Optimizer B2B Edition
  - id: edbd1a0e-46c8-49da-8c10-dba9ec80bba9
    internal-label: Experience Platform
  - id: b27e5950-9033-45ac-9f86-eb22e567f615
    internal-label: Marketo Engage
feature_v2:
  - id: 095e8119-1425-57eb-9d8c-9e684f2c9771
    internal-label: Audiences
  - id: 33ca0c14-7e3b-55a1-8fd7-8a61b47da4e1
    internal-label: B2B
  - id: a4b836d9-ffdd-4df3-a62a-f78b830cf059
    internal-label: Journeys
  - id: a50ad69b-1331-40e9-b634-531a085a6a54
    internal-label: Identities
  - id: afadf741-c5fe-42cd-8013-23bb6ff2d1bc
    internal-label: Buying Groups
  - id: beb5f4be-cec3-471a-9db6-831a77dd3ac9
    internal-label: Audiences
  - id: eec185bd-7d60-4193-ba3f-da427569936a
    internal-label: Destinations
  - id: f2da1b69-6919-4386-a5d2-9c7b5c9033db
    internal-label: Data management
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
level_v2:
  - id: d378ca77-2da1-4f39-ad92-1917fe974a38
    internal-label: Experienced
topic_v2:
  - id: df401a2a-327d-468c-a5e4-b7b7ccd071a0
    internal-label: Data integration
  - id: ebde5b41-29c9-4f5e-9ef6-1197e85409e3
    internal-label: Data management
source-git-commit: 827c313f032d482ac2b0a5fa8f41d6506e67b9cb
workflow-type: tm+mt
source-wordcount: '612'
ht-degree: 0%
---
# 数据可用性和同步计时 {#data-availability}

通过本主题了解数据更改在[!DNL Adobe Journey Optimizer B2B Edition]历程中的显示速度以及哪些时间线正常。 了解预期的时间可帮助您相应地设计旅程，并识别延迟何时是预期行为。

## 预期等待时间

| 数据类型 | 典型可用性 |
| --- | --- |
| [受众成员资格](#daily-refresh) | 长达24小时（每日周期） |
| [帐户和人员关系更改](#daily-refresh) | 长达24小时（每日周期） |
| [数据从 [!DNL Experience Platform] 到 [!DNL Journey Optimizer B2B Edition]](#platform-sync) | 长达30分钟（近乎实时） |
| [数据从 [!DNL Journey Optimizer B2B Edition] 到 [!DNL Experience Platform]](#platform-sync) | 长达4小时（微批） |
| [活动事件，例如点击和打开](#activity-and-actions) | 最多四小时 |
| [[!DNL Marketo Engage] 列表添加或删除](#activity-and-actions) | 在30分钟内（近乎实时） |
| 由Journey Optimizer B2B Edition生成的[事件](#activity-and-actions) | 仅在批量受众中可用 |
| [LinkedIn受众群体](#linkedin-timing) | 当天到36-40小时（最坏情况） |

## 受众和关系数据 {#daily-refresh}

[!DNL Journey Optimizer B2B Edition]每天评估一次帐户和人员受众成员资格，由批处理作业调度程序触发。 因此：

* 新获得受众资格的客户或人员有资格在获得资格后的24小时内进入历程。
* 对受众标准的更改将在下一个每日评估周期中生效。
* 如果某个帐户今天符合受众资格但尚未进入历程，请等到下一个每日周期完成时再进行调查。
* 当人员的帐户关联发生更改（例如，当联系人转到其他帐户时）时，关系更新会在24小时内通过每日同步周期传播。 依赖于帐户成员资格的历程反映了在下一个每日周期后更新的关系。 无需执行任何操作。

>[!TIP]
>
>设计历程，了解受众会员资格是每天更新的，而不是实时更新。 如果需要近乎实时的响应，请使用[基于事件的触发器](../journeys/listen-for-event-nodes.md)，而不是基于受众的条目。

## 与[!DNL Experience Platform]同步数据 {#platform-sync}

[!DNL Experience Platform]是帐户、人员和机会的主要数据存储区，[!DNL Journey Optimizer B2B Edition]拥有历程、购买群组和购买群组角色。 [了解有关架构的更多信息](../about-journey-optimizer-b2b-edition.md#high-level-architecture)。

数据在两个系统之间以不同的速度沿每个方向移动：

* **[!DNL Experience Platform]到[!DNL Journey Optimizer B2B Edition]** — 近乎实时地同步数据，最多可能需要30分钟。
* **[!DNL Journey Optimizer B2B Edition]到[!DNL Experience Platform]** — 以微批次同步数据，最多可能需要4小时。

## 活动事件和历程操作 {#activity-and-actions}

活动数据和历程操作的时间取决于数据在系统之间的移动方式：

* **活动数据** — 人员活动记录（如电子邮件打开、链接点击和表单填写）大约需要4小时才能显示在[!DNL Journey Optimizer B2B Edition]中。 此时间适用于批处理活动数据；[!DNL Experience Platform]体验事件触发器使用流式数据，可以近乎实时地做出反应。
* **[!DNL Marketo Engage]操作** — 调用[!DNL Marketo Engage]的历程操作近乎实时，因为它们是API调用。 例如，当历程步骤从[!DNL Marketo]列表中添加或删除人员时，操作通常在30分钟内完成。 [了解有关历程操作的更多信息](../journeys/action-nodes.md)。
* **通过[!DNL Experience Platform]**&#x200B;的操作 — 任何首先返回到[!DNL Experience Platform]的操作都将进行批处理，因此该操作受批量计时的约束，而不是近乎实时的计时。
* **由[!DNL Journey Optimizer B2B Edition]**&#x200B;生成的事件 — [!DNL Journey Optimizer B2B Edition]在[!DNL Experience Platform]中生成的事件只能在批处理受众中使用。

## [!DNL LinkedIn]受众目标 {#linkedin-timing}

如果您的历程包含[!DNL LinkedIn]目标操作，则在发布历程后可期待以下时间线。

| 场景 | 预期等待 |
| --- | --- |
| 发布历程时，帐户已在受众中 | 当天，如果处理在当地时间午夜之前完成 |
| 帐户在历程发布后到达 | 长达24小时 |
| 帐户在第一个每日同步窗口之后到达 | 长达36-40小时 |

[!DNL LinkedIn]受众规模可能不会立即更新。 此滞后是[!DNL Experience Platform]处理并将受众文件提交到[!DNL LinkedIn]时的预期延迟。 如果48小时后受众规模仍为0，请调查。 [了解有关LinkedIn帐户匹配受众的详细信息](./linkedin-account-matched-audiences.md)。
