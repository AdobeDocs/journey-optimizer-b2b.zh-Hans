---
title: Adobe Journey Optimizer B2B版本概述
description: 了解Adobe Journey Optimizer B2B版本的关键功能、用例和体系结构。
source-git-commit: b9fc31ed31cf05370f1370510d966b8151e14695
workflow-type: tm+mt
source-wordcount: '805'
ht-degree: 0%

---

# Adobe Journey Optimizer B2B版本概述

借助Adobe Journey Optimizer B2B版，您可以使用内置的创作AI和行业领先的自动化功能来编排帐户和购买团体历程，以通过符合营销条件的购买团体最大程度地满足特定产品的需求。

## 与购买团体相关的帐户历程

在将Adobe Journey Optimizer B2B版本与Marketo Engage和Adobe Journey Optimizer标准进行比较时，关键的区别在于帐户历程是通过历程移动帐户，而不是通过人员。 与帐户关联的人员很可能具有非线性进展，其进展取决于帐户在历程中的进度，而不是其个人行为。 例如，当客户处于购买历程的早期阶段时，发送的信息可能涉及常规解决方案功能或特性。 在购买过程中，内容可能会变得更加针对特定优惠或旨在结束销售的其他项目。 购买解决方案后，信息可能会再次更改，以提供操作指南、最佳实践、有关即将举行的活动的信息或有关其他追加销售的内容。 即使个人尚未与早期阶段内容进行交互，您仍希望根据客户或购买团体内其他人员的操作（而非他们自己的操作）将内容推进到当前阶段。

## 高级体系结构

Adobe Journey Optimizer B2B版本使用Adobe Experience Platform中的&#x200B;_帐户受众_&#x200B;和帐户的&#x200B;_人员受众_&#x200B;来推动在Marketo Engage内运行的帐户历程。 Experience Platform始终是这些数据的真实来源，但客户历程的所有执行和处理都发生在Marketo EngageB2B营销基础设施内部。 该编排通过现有的Marketo Engage- Adobe Real-Time CDP B2B版源连接器近乎实时地将数据重新Experience Platform，该连接器可将数据更改从Marketo Engage流式传输到Experience Platform。

![高级数据架构](./assets/high-level-data-architecture.png){width="600" zoomable="yes"}

### 订阅模式

Journey Optimizer B2B版本订阅由具有Marketo Engage _munchkin_&#x200B;订阅的一对Experience Platform(AEP)沙盒定义。 单个Marketo Engage订阅无法与多个AEP沙盒配对。 如果您未选择将现有Marketo Engage订阅与Journey Optimizer B2B版本一起使用，或者您当前未使用Marketo Engage，则会为您预配一个空的新Marketo Engage订阅，以便与Journey Optimizer B2B版本一起使用。

在此设置中Experience Platform的目的在于提供来自Marketo Engage实例（以及任何附加的CRM系统）的统一数据视图，然后能够使用帐户历程对统一数据执行操作。

### 帐户历程操作

帐户历程在Journey Optimizer B2B版本中创作，并存储在与订阅关联的Marketo Engage实例中。 尽管它存储在Marketo Engage数据存储中，但在Marketo EngageUI中不可见，并且只能从Journey Optimizer B2B版本中使用。

帐户历程始终从选择用作历程的帐户受众的帐户区段开始。 受众选择使用标准Experience Platform受众选择器组件。 然后，营销人员可以根据自己的标准（包括帐户标准、人员标准或购买群组标准）拆分历程路径，以实施帐户历程。 在每个分支上，可以采取操作来实施历程，例如发送电子邮件或等待事件发生。

创建帐户历程后，必须发布该历程。 在发布时，将验证帐户历程并转换为一系列实施历程体验的Marketo Engage活动，并联系数据集成服务以启动数据流，进而启动帐户历程操作。 第一步是为帐户人员创建区段。

### 数据流

Journey Optimizer B2B版本使用Real-Time CDP帐户分段定义和执行历程所需的帐户区段和相关帐户人员区段。 随着已发布的历程的运行，有关人员和帐户的数据可能会发生更改，并且与历程交互的人员将会收集相关数据。 Journey Optimizer B2B版本依赖于Real-Time CDP B2B版本的Marketo Engage源连接器将数据更改流回Experience Platform沙盒，这是事实来源。  此数据将以近乎实时的方式传送到AEP。

只有Marketo Engage源连接器支持的现有数据类型（帐户、人员和机会）会返回到Real-Time CDP。 这意味着购买组数据不会流入AEP，而是驻留在Journey Optimizer B2B版本订阅使用的Marketo Engage实例中。

