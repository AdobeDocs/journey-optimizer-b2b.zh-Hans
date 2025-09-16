---
title: Adobe Journey Optimizer B2B Edition 概述
description: 了解 Adobe Journey Optimizer B2B Edition——通过购买群组、AI 洞察和 Experience Platform 集成，为 B2B 营销编排帐户历程。
exl-id: fdfbafdf-826f-44e9-bbb6-5e729d0e18ef
source-git-commit: d3247a48ff1fbda54c559fa03580865da7252935
workflow-type: ht
source-wordcount: '819'
ht-degree: 100%

---

# Adobe Journey Optimizer B2B Edition 概述

借助 Adobe Journey Optimizer B2B Edition，您可以使用内置的生成式 AI 和行业领先的自动化功能来协调帐户和购买群组历程，以使用符合营销资格的购买群组来最大限度地满足特定产品的需求。

## 包含购买群组的帐户历程

当将 Adobe Journey Optimizer B2B Edition 与 Marketo Engage 和 Adobe Journey Optimizer 标准进行比较时，关键区别在于帐户历程是通过历程而不是人员来移动帐户的。与帐户相关联的人员通常为非线性进展，该进展基于帐户在整个历程中的进度，而不是基于他们的个人操作。例如，当帐户处于购买历程的早期阶段时，发送的信息可能是关于一般解决方案的功能或特性。在购买过程的进一步发展中，内容可能会变得更加针对特定的产品或其他旨在促成销售的事项。购买解决方案后，信息可能会再次更改，提供操作指南、最佳实践、即将举行的活动信息或有关额外追加销售的内容。即使某些个人尚未与早期阶段的内容进行互动，您仍然希望根据其帐户中或购买群组中其他人员的操作（而不是他们自己的操作）将他们推进到当前阶段。

## 高层架构

Adobe Journey Optimizer B2B Edition 使用 Adobe Experience Platform 中的&#x200B;_帐户受众_&#x200B;和&#x200B;_人员受众_，来支持在 Marketo Engage 内部运行的帐户历程。Experience Platform 始终是这些数据的真实来源，但帐户历程的所有执行和处理都发生在 Marketo Engage B2B 营销基础架构内部。该编排通过现有的 Marketo Engage - Adobe Real-Time CDP B2B Edition 源连接器近乎实时地将数据带回 Experience Platform，该连接器将数据变化从 Marketo Engage 传输到 Experience Platform。

![高层数据架构](./assets/high-level-data-architecture.png){width="500" zoomable="yes"}

>[!NOTE]
>
>检查您的许可证授权和相应的[产品描述](https://helpx.adobe.com/cn/legal/product-descriptions/adobe-journey-optimizer-b2b.html){target="_blank"}，了解性能护栏和静态限制。

### 订阅模型

Journey Optimizer B2B Edition 订阅由一对包含 Marketo Engage _Munchkin_ 订阅的 Experience Platform（AEP）沙盒定义。单个 Marketo Engage 订阅不能与多个 AEP 沙盒配对。如果您不选择将现有的 Marketo Engage 订阅与 Journey Optimizer B2B Edition 配对，将获得一个新的空 Marketo Engage 订阅，以便与 Journey Optimizer B2B Edition 一起使用。

Experience Platform 用此设置的目的是为来自 Marketo Engage 实例（以及任何附加的 CRM 系统）的数据提供统一视图，然后能够使用帐户历程对统一数据进行操作。

### 帐户历程操作

在 Journey Optimizer B2B Edition 中创作帐户历程，并将其存储在与订阅相关联的 Marketo Engage 实例中。虽然它被存储在 Marketo Engage 数据存储中，但在 Marketo Engage UI 中不可见，并且只能在 Journey Optimizer B2B Edition 中使用。

帐户历程总是从选择使用一个帐户区段作为历程的帐户受众开始。选择受众时，使用标准 Experience Platform 受众选择器组件。然后，营销人员可以根据自己的标准（包括帐户标准、人员标准或购买群组标准）拆分历程路径来实施帐户历程。在每个分支上都可以通过执行操作来实施历程，例如发送电子邮件或等待事件发生。

帐户历程创建后，必须将其发布。发布时，帐户历程会被验证，并转换为一系列实施历程体验的 Marketo Engage 营销活动。数据集成服务被触发，从而启动数据流，进而启动帐户历程操作。第一步是为帐户的人员创建区段。

### 数据流

Journey Optimizer B2B Edition 使用 Real-Time CDP 帐户分段，定义并执行历程所需的帐户区段和相关帐户人员区段。随着已发布历程的运行，关于人员和帐户的数据可能会发生变化，并且会收集与历程互动人员的数据。Journey Optimizer B2B Edition 使用 Real-Time CDP B2B Edition 的 Marketo Engage 源连接器，将数据变化返回真实来源 Experience Platform 沙盒。这些数据会以近乎实时的方式送达 AEP。

只有 Marketo Engage 源连接器支持的现有数据类型（帐户、人员和机会）才会返回 Real-Time CDP。这意味着购买群组数据不会流向 AEP，而是保留在 Journey Optimizer B2B Edition 订阅使用的 Marketo Engage 实例中。
