---
title: Adobe Journey Optimizer B2B Edition 概述
description: 了解 Adobe Journey Optimizer B2B Edition——通过购买群组、AI 洞察和 Experience Platform 集成，为 B2B 营销编排帐户历程。
exl-id: fdfbafdf-826f-44e9-bbb6-5e729d0e18ef
autotag-review: 2026-04-29T23:21:13.339Z
product_v2: id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2: id: f467931a-9b22-4ca8-869f-adfbd64061ce
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: df401a2a-327d-468c-a5e4-b7b7ccd071a0
TQID: https://experienceleague.adobe.com/L58cK4MP-S-8U9fFiXU2qZn4HCieNzjoOaSRCLkyanI
source-git-commit: 8d2fc3ebc7df1674ac9af441679228a9e19d8d5a
workflow-type: tm+mt
source-wordcount: 739
ht-degree: 15%

---

# Adobe Journey Optimizer B2B Edition 概述

借助Adobe Journey Optimizer B2B edition，您可以使用内置的创作AI和行业领先的自动化功能来编排人员和帐户历程，以通过符合营销条件的购买小组最大程度地满足特定产品的需求。

## 包含购买群组的帐户历程

将帐户历程与Marketo Engage和Adobe Journey Optimizer Standard中的历程功能进行比较时，关键的区别在于帐户历程在历程中移动帐户，而不是人员。 与帐户相关联的人员通常为非线性进展，该进展基于帐户在整个历程中的进度，而不是基于他们的个人操作。 例如，当客户处于购买历程的早期阶段时，发送的信息通常与一般解决方案功能或特性有关。 在购买过程中，内容会更加针对特定优惠或旨在结束销售的其他项目。 购买解决方案后，信息会再次更改，以提供操作指南、最佳实践、有关即将举行的活动的信息或有关其他追加销售的内容。 即使个人未与早期阶段内容进行交互，您仍可以根据其账户内或购买团体内其他人的行为将它们推进到当前阶段。

## 高层架构

Adobe Journey Optimizer B2B edition基于Adobe Experience Platform构建，包括Real-Time CDP B2B。 Journey Optimizer B2B edition和Marketo Engage在单独的系统上运行，每个系统都有自己的数据存储。 Experience Platform是客户、人员和机会的主要数据存储和权威来源。 Journey Optimizer B2B edition拥有您的帐户历程、购买群组和购买群组角色。

专用的Marketo Engage实例支持每个Journey Optimizer B2B edition订阅。 此实例不会存储您的帐户历程、受众或购买群体。 相反，它提供权利和后端服务，如电子邮件投放、发件人配置和品牌策略域。

要支持历程操作，您还可以连接一个或多个现有Marketo Engage实例，包括生产实例。 通过历程操作，营销人员可以在Journey Optimizer B2B edition中协调基于帐户的历程与Marketo Engage中基于商机的营销活动，例如将人员添加到列表或请求营销活动。 [了解有关连接Marketo Engage实例的更多信息](./admin/marketo-actions-connect.md)。

![高级数据架构显示连接到Adobe Experience Platform的Journey Optimizer B2B edition作为帐户和人员受众的真实来源，一个提供权利和后端服务的专用Marketo Engage实例，以及一个用于运行历程操作的可选生产Marketo Engage实例。](./assets/high-level-data-architecture.png){zoomable="yes"}

>[!NOTE]
>
>检查您的许可证授权和相应的[产品描述](https://helpx.adobe.com/cn/legal/product-descriptions/adobe-journey-optimizer-b2b.html){target="_blank"}以了解性能护栏和静态限制。

### 订阅模型

Experience Platform沙盒与专用的Marketo Engage实例配对，可定义Journey Optimizer B2B edition订阅。 此专用实例与您的生产Marketo Engage实例不同，它的存在是为了支持权利和后端服务，而不是存储帐户历程数据。 [了解有关设置的详细信息](./setup-ultimate.md)。

Experience Platform可让您统一查看连接的Marketo Engage实例和CRM系统中的数据。 使用该统一数据构建和运行您的历程。

### 历程操作

Journey Optimizer B2B edition创建、存储和运行您的帐户历程。 帐户历程不会显示在Marketo Engage中，并且只能在Journey Optimizer B2B edition中使用。

历程始终从符合潜在客户或客户及其人员历程条件的受众开始。 使用标准Experience Platform受众选择器选择此受众。 营销人员通过使用帐户标准、人员标准或购买群组标准拆分路径来实施历程。 在每个路径上，操作都会发送通信或等待事件发生。

创建帐户历程后，发布该历程以使其上线。 符合条件的帐户将在24小时内进入已发布的历程。

### 数据流

Journey Optimizer B2B edition可充当Adobe Real-Time CDP B2B edition目标。 使用Real-Time CDP帐户分段来构建和评估符合历程帐户和人员资格的帐户受众和人员受众。 发布历程时，Journey Optimizer B2B edition会从Experience Platform激活符合条件的受众。

在Journey Optimizer B2B edition中创建并存储购买群组、购买群组角色和购买群组得分。 [了解有关购买群组的详细信息](./buying-groups/buying-groups-overview.md)。
