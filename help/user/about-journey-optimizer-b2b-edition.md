---
title: Adobe Journey Optimizer B2B edition概述
description: 探索 Adobe Journey Optimizer B2B Edition 的主要功能、用例和架构。
exl-id: fdfbafdf-826f-44e9-bbb6-5e729d0e18ef
source-git-commit: d1696eb54c9ff25963b51a0e3934a02e103923e4
workflow-type: tm+mt
source-wordcount: '811'
ht-degree: 5%

---

# Adobe Journey Optimizer B2B edition概述

借助 Adobe Journey Optimizer B2B 版本，您可以使用内置的生成式 AI 和行业领先的自动化功能来协调帐户和购买群组历程，以使用符合营销资格的购买群组来最大限度地满足特定产品的需求。

## 与购买团体相关的帐户历程

将Adobe Journey Optimizer B2B edition与Marketo Engage和Adobe Journey Optimizer标准相比，关键区别在于客户历程通过历程而不是人员移动客户。 与帐户关联的人员通常具有非线性进展，该进展基于帐户在历程中的进展，而不是基于其个人操作。 例如，当客户处于购买历程的早期阶段时，发送的信息可能涉及常规解决方案功能或特性。 在购买过程中，内容可能会变得更加针对特定优惠或旨在结束销售的其他项目。 购买解决方案后，信息可能会再次更改，以提供操作指南、最佳实践、有关即将举行的活动的信息或有关其他追加销售的内容。 即使个人尚未与早期阶段内容进行交互，您仍希望根据客户或购买团体内其他人员的操作（而非他们自己的操作）将内容推进到当前阶段。

## 高级体系结构

Adobe Journey Optimizer B2B edition使用Adobe Experience Platform中的&#x200B;_帐户受众_&#x200B;和&#x200B;_人员受众_&#x200B;来推动在Marketo Engage内运行的帐户历程。 Experience Platform始终是这些数据的真实来源，但客户历程的所有执行和处理都发生在Marketo EngageB2B营销基础设施内部。 该编排通过现有Marketo Engage(Adobe Real-Time CDP B2B edition源连接器)近乎实时地将数据带回Experience Platform，该连接器可将数据更改从Marketo Engage流式传输到Experience Platform。

![高级数据架构](./assets/high-level-data-architecture.png){width="500" zoomable="yes"}

>[!NOTE]
>
>检查您的许可证授权和相应的[产品描述](https://helpx.adobe.com/legal/product-descriptions/adobe-journey-optimizer-b2b.html){target="_blank"}，了解性能护栏和静态限制。

### 订阅模式

Journey Optimizer B2B edition订阅由具有Marketo Engage _Munchkin_&#x200B;的一对Experience Platform(AEP)沙盒定义。 单个Marketo Engage订阅无法与多个AEP沙盒配对。 如果您不选择将现有Marketo Engage订阅与Journey Optimizer B2B edition配对，则会为您预配一个新的空Marketo Engage订阅，以便与Journey Optimizer B2B edition一起使用。

在此设置中Experience Platform的目的在于提供来自Marketo Engage实例（以及任何附加的CRM系统）的统一数据视图，然后能够使用帐户历程对统一数据执行操作。

### 帐户历程操作

帐户历程在Journey Optimizer B2B edition中创作，并存储在与订阅关联的Marketo Engage实例中。 尽管它存储在Marketo Engage数据存储中，但在Marketo EngageUI中不可见，并且只能从Journey Optimizer B2B edition中使用。

帐户历程始终从选择用作历程的帐户受众的帐户区段开始。 受众选择使用标准Experience Platform受众选择器组件。 然后，营销人员可以根据自己的标准（包括帐户标准、人员标准或购买群组标准）拆分历程路径，以实施帐户历程。 在每个分支上，可以采取操作来实施历程，例如发送电子邮件或等待事件发生。

创建帐户历程后，必须发布该历程。 在发布时，将验证帐户历程并转换为一系列实施旅程体验的Marketo Engage营销活动。 我们会联系数据集成服务，以启动数据流，进而启动帐户历程操作。 第一步是为帐户人员创建区段。

### 数据流

Journey Optimizer B2B edition使用Real-Time CDP帐户分段来定义和执行历程所需的帐户区段和相关帐户人员区段。 随着已发布的历程的运行，有关人员和帐户的数据可能会发生更改，并且与历程交互的人员将会收集相关数据。 Journey Optimizer B2B edition依赖于Real-Time CDP B2B edition的Marketo Engage源连接器，将数据更改流回Experience Platform沙盒，这是事实来源。  此数据将以近乎实时的方式传送到AEP。

只有Marketo Engage源连接器支持的现有数据类型（帐户、人员和机会）会返回到Real-Time CDP。 这意味着购买组数据不会流入AEP，而是驻留在Journey Optimizer B2B edition订阅使用的Marketo Engage实例中。
