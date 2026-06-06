---
title: Adobe Journey Optimizer B2B Edition 概述
description: 了解 Adobe Journey Optimizer B2B Edition——通过购买群组、AI 洞察和 Experience Platform 集成，为 B2B 营销编排帐户历程。
exl-id: fdfbafdf-826f-44e9-bbb6-5e729d0e18ef
autotag-review: 2026-04-29T23:21:13.339Z
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2:
  - id: f467931a-9b22-4ca8-869f-adfbd64061ce
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: df401a2a-327d-468c-a5e4-b7b7ccd071a0
TQID: https://experienceleague.adobe.com/L58cK4MP-S-8U9fFiXU2qZn4HCieNzjoOaSRCLkyanI
source-git-commit: ca0c6b10cf6a979249901d514116f373014544ad
workflow-type: tm+mt
source-wordcount: 803
ht-degree: 66%

---

# Adobe Journey Optimizer B2B Edition 概述

借助 Adobe Journey Optimizer B2B Edition，您可以使用内置的生成式 AI 和行业领先的自动化功能来协调帐户和购买群组历程，以使用符合营销资格的购买群组来最大限度地满足特定产品的需求。

## 包含购买群组的帐户历程

将帐户历程与Marketo Engage和Adobe Journey Optimizer Standard中的历程功能进行比较时，关键的区别在于帐户历程在历程中移动帐户，而不是人员。 与帐户相关联的人员通常为非线性进展，该进展基于帐户在整个历程中的进度，而不是基于他们的个人操作。 例如，当客户处于购买历程的早期阶段时，发送的信息通常与一般解决方案功能或特性有关。 在购买过程中，内容会更加针对特定优惠或旨在结束销售的其他项目。 购买解决方案后，信息会再次更改，以提供操作指南、最佳实践、有关即将举行的活动的信息或有关其他追加销售的内容。 即使个人未与早期阶段内容进行交互，您仍可以根据其账户内或购买团体内其他人的行为将它们推进到当前阶段。

## 高层架构

Adobe Journey Optimizer B2B Edition 使用 Adobe Experience Platform 中的&#x200B;_帐户受众_&#x200B;和&#x200B;_人员受众_，来支持在 Marketo Engage 内部运行的帐户历程。 Experience Platform始终是此数据的主要来源，但客户历程的所有执行和处理都发生在Marketo Engage B2B营销基础架构中。 该编排通过现有的 Marketo Engage - Adobe Real-Time CDP B2B Edition 源连接器近乎实时地将数据带回 Experience Platform，该连接器将数据变化从 Marketo Engage 传输到 Experience Platform。

![高层数据架构](./assets/high-level-data-architecture.png){width="500" zoomable="yes"}

>[!NOTE]
>
>检查您的许可证授权和相应的[产品描述](https://helpx.adobe.com/cn/legal/product-descriptions/adobe-journey-optimizer-b2b.html){target="_blank"}，了解性能护栏和静态限制。

### 订阅模型

具有Experience Platform _Munchkin_&#x200B;订阅的一对Marketo Engage (AEP)沙盒定义了Journey Optimizer B2B edition订阅。 单个 Marketo Engage 订阅不能与多个 AEP 沙盒配对。 如果您不选择将现有的 Marketo Engage 订阅与 Journey Optimizer B2B Edition 配对，将获得一个新的空 Marketo Engage 订阅，以便与 Journey Optimizer B2B Edition 一起使用。

Experience Platform提供了来自Marketo Engage实例和附加的CRM系统的数据的统一视图，以便使用帐户历程处理这些数据。

### 帐户历程操作

在 Journey Optimizer B2B Edition 中创作帐户历程，并将其存储在与订阅相关联的 Marketo Engage 实例中。 尽管它们存储在Marketo Engage数据存储中，但在Marketo Engage UI中不可见，并且只能在Journey Optimizer B2B edition中使用。

帐户历程总是从选择使用一个帐户区段作为历程的帐户受众开始。 选择受众时，使用标准 Experience Platform 受众选择器组件。 然后，营销人员可以根据自己的标准（包括帐户标准、人员标准或购买群组标准）拆分历程路径来实施帐户历程。 在每个分支上都可以通过执行操作来实施历程，例如发送电子邮件或等待事件发生。

帐户历程创建后，必须将其发布。 发布时，帐户历程会被验证，并转换为一系列实施历程体验的 Marketo Engage 营销活动。 我们会联系Data Integration Services以启动数据流，进而启动帐户历程操作。 第一步是为帐户的人员创建区段。

### 数据流

Journey Optimizer B2B Edition 使用 Real-Time CDP 帐户分段，定义并执行历程所需的帐户区段和相关帐户人员区段。 随着已发布历程的运行，关于人员和帐户的数据可能会发生变化，并且会收集与历程互动人员的数据。 Journey Optimizer B2B edition依赖于Real-Time CDP B2B edition的Marketo Engage源连接器，将数据更改流回主要数据源Experience Platform沙盒。  此数据会近乎实时地提交到AEP。

只有 Marketo Engage 源连接器支持的现有数据类型（帐户、人员和机会）才会返回 Real-Time CDP。 这意味着购买群组数据不会流向 AEP，而是保留在 Journey Optimizer B2B Edition 订阅使用的 Marketo Engage 实例中。
