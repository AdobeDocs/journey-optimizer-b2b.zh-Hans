---
title: 发行说明
description: Adobe Journey Optimizer B2B Edition 的最新发行说明
exl-id: 7d3f1c26-d8a6-4065-a70f-5b30cb975dc8
source-git-commit: 9438b1472df38eddc3e1fa6cd5bc3992af0c9eec
workflow-type: tm+mt
source-wordcount: '895'
ht-degree: 10%

---

# Journey Optimizer B2B edition发行说明

Adobe Journey Optimizer B2B edition不断提供新功能、现有功能的增强以及错误修复。

Journey Optimizer B2B edition本机构建于[!DNL Adobe Experience Platform]之上并继承了其最新创新和改进。 在 [Adobe Experience Platform 发行说明](https://experienceleague.adobe.com/zh-hans/docs/experience-platform/release-notes/latest){target="_blank"}中，进一步了解这些更改。

查看[产品描述](https://helpx.adobe.com/legal/product-descriptions/adobe-journey-optimizer-b2b.html){target="_blank"}，了解有关授权、性能护栏和限制的信息。

## 2024 年 10 月发行说明 {#Oct-2024}

**发行日期**：2024年10月29日

此版本包括以下新增功能和增强功能：

| 类型 | 项目 | 描述 |
| ---- | ---- | ----------- |
| 新功能 | 电子邮件模板中的条件内容 | 在帐户和潜在客户级别上，根据收件人行为和用户档案特征个性化您的电子邮件内容。 <p>在email designer中为帐户历程创作电子邮件时，请使用条件规则为任何内容组件定义多个变体。 <a href="../content/conditional-content.md">了解详情</a> |
| 新功能 | _添加到列表_&#x200B;和&#x200B;_从列表中删除_&#x200B;历程中的人员操作 | 在帐户和潜在客户级别上，根据收件人行为和用户档案特征个性化您的电子邮件内容。 <a href="../journeys/action-nodes.md">了解详情</a> |
| 新功能 | 内容治理和组件锁定 | 要确保遵循已批准的内容设计，请使用内容治理功能来锁定电子邮件模板内容组件。 在电子邮件模板中激活内容治理后，营销人员可以仅更改允许的元素，以使其与内容策略保持一致。 <a href="../content/template-content-governance.md">了解详情</a> |
| 新功能 | 购买群组阶段 | 在定义和发布自定义购买组暂存模型时，您可以在整个购买组生命周期阶段跟踪购买组进展。 使用这些阶段来确定购买组成员的下一步最佳操作。 可配置过渡规则和历程节点，以确定暂存进程并根据更改触发操作。 <a href="../buying-groups/buying-group-stages.md">了解详情</a> |
| 增强功能 | 新的现成电子邮件模板 | 示例模板库现在包含其他为B2B营销人员设计的电子邮件模板。 使用这些示例模板作为起点，并添加您自己的品牌和消息。 <a href="../content/email-templates.md#select-a-design-template">了解详情</a> |
| 增强功能 | 将自定义字段作为人员属性 | 如果您在Experience Platform的帐户受众架构中定义了自定义人员字段，则这些字段也可用作条件中的人员属性。 在中使用这些自定义属性： <li>角色模板<a href="../buying-groups/buying-groups-role-templates.md#add-the-template-roles">了解更多</a></li><li>按人员历程节点拆分路径<a href="../journeys/split-merge-paths-nodes.md#add-a-split-path-by-people-node">了解详情</a></li> |
| 增强功能 | 电子邮件渠道设置 | 电子邮件设置现在显示在Journey Optimizer B2B edition界面中。 您可以快速查看当前配置，管理员可以单击&#x200B;_[!UICONTROL 编辑设置]_&#x200B;以直接转到Marketo Engage中的设置，并根据组织的要求对其进行更新。 <a href="../admin/configure-channels-emails.md">了解详情</a> |

## 2024 年 9 月发行说明 {#Sept-2024}

**发行日期**：2024年10月7日

此版本包括以下新增功能和增强功能：

| 类型 | 项目 | 描述 |
| ---- | ---- | ----------- |
| 增强功能 | 中央资产库 | 增强的&#x200B;_中央资源库_&#x200B;允许您在Design Studio工作区中使用Marketo Engage实例中的所有图像资源。 有内置的护栏，可阻止从Journey Optimizer B2B edition编辑Marketo Engage资源以及执行删除和移动操作。 这些保护可以确保维护源资源(Marketo EngageDesign Studio)，同时允许在Journey Optimizer B2B edition中无缝读取和重用。<p>对于在Journey Optimizer B2B edition中专门使用的资源，特定工作区提供了完整的资源管理功能。 <a href="../content/marketo-engage-design-studio.md">了解详情</a> |
| 新功能 | 最近访问的资源 | Journey Optimizer B2B edition应用程序中的主页现在包含&#x200B;_[!UICONTROL 最近访问的]_&#x200B;部分，该部分为营销人员或管理员提供了最近访问的资源列表。 您可以使用此列表直接转到您最近处理的资产，而无需浏览一系列资产页面并搜索。 <p>列表提供了有关修改的更多信息，以便您能够决定哪些资产需要从上一会话进一步修改。 对于电子邮件资产，它显示使用电子邮件资产的帐户历程。 <a href="../home-page.md">了解详情</a> |
| 增强功能 | 历程拆分节点 — 对路径重新排序 | 在拆分路径节点中，路径过滤按自上而下的顺序计算。 每个人员或帐户都会沿着匹配的第一个路径前进。 您可以通过单击每个路径卡右上角的向上和向下箭头将定义的路径重新排序，以在列表中将其向上或向下移动。 <a href="../journeys/split-merge-paths-nodes.md#split-paths">了解详情</a> |
| 增强功能 | 历程拆分节点 — 其他活动历史记录条件属性 | 使用条件为按人员划分的拆分节点定义路径筛选时，存在两个其他属性： _已打开的电子邮件_&#x200B;和&#x200B;_已送达电子邮件_。 这些添加内容提供了更大的灵活性，可以根据电子邮件活动筛选历程中的人员。 <a href="../journeys/journey-nodes.md#split-paths">了解详情</a> |

## 2024 年 8 月发行说明 {#Aug-2024}

**发行日期**： 2024年8月29日

此版本包括以下新增功能和增强功能：

| 类型 | 项目 | 描述 |
| ---- | ---- | ----------- |
| 新功能 | linkedIn帐户匹配的受众 | 通过帐户匹配受众生成LinkedIn广告受众，以帮助您在购买群组中填充空角色。 通过定义一组购买群组过滤器，您可以维护一个LinkedIn匹配受众，以定位与您的购买群组参数相匹配的潜在客户。 <p>此功能利用Experience Platform目标来管理集成的某些方面。 <a href="../data/linkedin-account-matched-audiences.md">了解详情</a> |
| 增强功能 | 可视化内容片段的状态生命周期 | 可视化片段现在使用状态生命周期进行管理。 片段状态决定了在电子邮件或电子邮件模板中使用的可用性，以及您可以对片段进行的更改。 <p>此增强的工作流使您可以轻松根据促销和通信日历管理重复使用的内容。 <a href="../content/fragments.md#fragment-status-and-lifecycle">了解详情</a> |
