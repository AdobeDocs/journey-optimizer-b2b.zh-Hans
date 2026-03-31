---
title: Journey Optimizer B2B Edition 发行说明
description: 探索 Adobe Journey Optimizer B2B Edition 中的最新功能、增强功能和错误修复。 随时掌握最新功能与产品改进信息。
role: User, Admin
exl-id: 7d3f1c26-d8a6-4065-a70f-5b30cb975dc8
source-git-commit: 34a570a6e998ede7465e30d7ca42f19f268e1943
workflow-type: tm+mt
source-wordcount: '4885'
ht-degree: 48%

---

# Journey Optimizer B2B Edition 发行说明

Journey Optimizer B2B Edition 不断地提供新功能，对现有功能进行增强，并修复错误。

Journey Optimizer B2B Edition 原生构建于 [!DNL Adobe Experience Platform] 上，并继承了其最新的创新和改进。 在 [Adobe Experience Platform 发行说明](https://experienceleague.adobe.com/zh-hans/docs/experience-platform/release-notes/latest){target="_blank"}中进一步了解这些更改。

查看[产品描述](https://helpx.adobe.com/cn/legal/product-descriptions/adobe-journey-optimizer-b2b.html){target="_blank"}，了解有关权限、性能护栏和限制的信息。

## 2026.3发行说明

**部署日期**：2026年3月27日

| 类型 | 项目 | 描述 |
| ---- | ---- | ----------- |
| 功能 | 登陆页面 | 营销人员现在可以在Journey Optimizer B2B edition中创建和发布登陆页面，以支持历程和程序&#x200B;_（以前是Beta程序功能）_。 |
| 功能 | 表单 | 营销人员现在可以创建并发布可重复使用的表单组件，以便从在Journey Optimizer B2B edition _（以前是Beta项目功能）_&#x200B;中创建和发布的登陆页面提交数据。 |
| 功能 | WhatsApp 渠道 | 营销人员现在可以通过Meta Cloud API直接从帐户历程发送WhatsApp消息。 此功能可实现WhatsApp消息传送的无缝集成，以支持历程内容渠道。 |
| 功能 | 支持[!DNL Firefly]和自定义生成AI模型 | 营销团队现在可以启用标准和自定义[!DNL Firefly]模型以及批准的第三方图像模型（如[!DNL NanoBanana]）的集成。 电子邮件设计人员可以针对每个用例选择最佳模型：可满足一般需求的标准[!DNL Firefly]、用于品牌内生成的自定义[!DNL Firefly]，或针对专用或实验场景的已批准的第三方模型。 |
| 功能 | 历程的自定义外部操作 | [!BADGE 简化的架构]{type=Informative tooltip="提供简化的架构"}开发人员现在可以使用API构建与其第一方系统的集成。 通过这些自定义集成，营销人员可以添加&#x200B;_外部操作_&#x200B;和&#x200B;_外部拆分路径_&#x200B;节点，以在帐户历程执行期间向外部服务发出出站请求。 |
| 功能 | 品牌 | (Beta)营销团队可以通过存储和管理品牌配置文件来维护电子邮件内容资产中的品牌一致性。 通过添加资产（如颜色、字体、徽标、主题、可视内容和合规性指南），他们可以使用品牌配置文件来创建创作AI内容。 他们还可以衡量品牌一致性以确保法规遵从性。 |
| 增强功能 | 发送电子邮件 — 优化发送时间 | [!BADGE 简化的架构]{type=Informative tooltip="提供简化的架构"}对于&#x200B;_在个人历程中发送电子邮件_&#x200B;操作节点，您可以使用&#x200B;_发送时间优化_&#x200B;选项，通过预测每个用户档案最有可能参与的时间，来对电子邮件投放时间进行个性化设置。[了解详情](../content/email-send-time-optimization.md)) |
| 增强功能 | 电子邮件设计工具 — 专家模式 | 在电子邮件设计空间中使用&#x200B;_专家模式_，用户可以进行细微的HTML/CSS编辑，并向电子邮件添加脚本标记以解决渲染问题。 |
| 增强功能 | 人员自定义对象 — 购买群组角色模板 | [!BADGE 简化的架构]{type=Informative tooltip="提供简化的架构"}管理员配置与业务人员配置文件相关的自定义对象时，营销人员现在可以使用这些自定义对象定义购买群组角色。 |
| 增强功能 | 电子邮件内容评分 — 内容质量验证 | 除了品牌协调之外，您还可以评估总体内容质量，以发现可读性、一致性和有效性方面的潜在问题（独立于您的品牌指南）。 这些自动化检查有助于识别消息表述不清、语调不一致或结构性差距问题。 |

<!-- wait for later release
| Enhancement | Activate to destinations - Reusable audiences | You can now reuse virtual audiences in _Activate to destination_ journey actions within the same journey and remove accounts from virtual audiences. | -->

>[!NOTE]
>
>这些版本更改从2026年Marh 27开始部署，并分阶段推出每个功能和增强功能。 功能及增强功能的发布时间可能会有变动。


## 2026.2发行说明

**部署日期**：2026年2月20日

| 类型 | 项目 | 描述 |
| ---- | ---- | ----------- |
| 功能 | XDM字段/关系架构 — 支持人员自定义对象 | [!BADGE 简化的架构]{type=Informative tooltip="提供简化的架构"} (Beta)管理员现在可以通过与帐户的单级别一对一关系选择与人员相关的自定义对象。 此功能使您的营销组织能够呈现更丰富的真实业务数据视图，从而定向、个性化和报告人员或帐户级别以外的实体。[了解详情](../admin/xdm-field-management.md#relational-schemas) |
| 功能 | 历程重新进入 | [!BADGE 简化的架构]{type=Informative tooltip="提供简化的架构"}您现在可以通过历程工作流多次发送帐户/人员。 重返工作涉及多种情形，例如重新评估资格标准和可重复使用的培养工作流程。[了解详情](../journeys/journey-re-entry.md) |
| 增强功能 | 帐户和人员历程 — 支持人员自定义对象 | [!BADGE 简化的架构]{type=Informative tooltip="提供简化的架构"} (Beta)利用链接到帐户的关系数据来过滤帐户或人员历程中的人员。[了解详情](../journeys/split-merge-paths-nodes.md#custom-data-filtering) |
| 增强功能 | (Beta)内容个性化 — 支持人员自定义对象 | [!BADGE 简化的架构]{type=Informative tooltip="提供简化的架构"}当营销人员使用自定义对象定义内容个性化时，他们可以访问基于模型的类自定义对象（关系架构）的变量。[了解详情](../content/personalization.md#custom-datasets) |

>[!NOTE]
>
>这些版本更改从2026年2月20日开始部署，并分阶段推出每个功能和增强功能。 功能及增强功能的发布时间可能会有变动。

## 2026.1发行说明

**部署日期**：2026年2月3日

| 类型 | 项目 | 描述 |
| ---- | ---- | ----------- |
| 功能 | 品牌套件 | (Beta)在Journey Optimizer B2B edition中定义品牌，为创意团队创建任何可视或书面内容提供真实来源。 在编译这些指南并共享品牌资产后，任何团队成员或协作者都可以为您的产品创建品牌上内容。[了解详情](../content/brands-overview.md) |
| 功能 | 用于生成电子邮件内容的品牌 | 您可以定义品牌指南，并使用此信息生成电子邮件内容。 利用此功能，电子邮件内容将符合您特定品牌的版面制作准则、样式和语调。[了解详情](../content/ai-assistant-emails.md) |
| 增强功能 | 历程&#x200B;_等待_&#x200B;节点 — 高级设置 | [!BADGE 简化的架构]{type=Informative tooltip="提供简化的架构"}对于历程中的&#x200B;_等待_&#x200B;节点，营销人员现在可以指定退出日期和时间，并选择时区。 此增强功能可更好地控制历程编排和营销活动计时。[了解详情](../journeys/wait-nodes.md#advanced-wait-settings) |
| 增强功能 | 购买组成员过滤器 — 已删除 | 对于由人员&#x200B;_节点拆分的_&#x200B;路径，_[!UICONTROL 购买群组成员]_&#x200B;筛选器现在包含&#x200B;_Is Removed_&#x200B;约束。 选择该筛选器后，该筛选器可以包含或排除已移除的购买组成员。 Marketo Engage智能列表中也支持此功能，您可以在其中的&#x200B;_[!UICONTROL 购买组成员]_&#x200B;筛选器中使用此新限制。 |
| 增强功能 | 电子邮件设计 — 多级项目符号 | 电子邮件内容设计空间工具现在支持子项目符号（项目符号级别）。 |

>[!NOTE]
>
>这些版本更改从2026年2月3日开始部署，并分阶段推出每个功能。 功能及增强功能的发布时间可能会有变动。

## 代理式 AI 功能

现在，AI 助手界面中提供以下代理式 AI 功能用于 Journey Optimizer B2B edition：

| 代理 | 更新 | 描述 |
| ----- | ------ | ----------- |
| 历程生成代理 | 新增的和更新的 | 历程构建代理可实时分析、构思和联合创建历程，使营销人员能够更快地启动、提高参与度并促进更高转化率。[了解详情](../agents/journey-agent.md) |
| Audience 代理 | 新 | Audience 代理使用结构化和非结构化数据自动识别和构建购买群组。 它有助于营销人员更快、更准确地定位适当的人员。[了解详情](../agents/audience-agent-b2b.md) |
| 销售限定词 | 新 | Sales Qualifier是Adobe Journey Optimizer B2B edition的AI驱动附加应用程序，它包含Account Qualification Agent，旨在简化业务开发代表(BDR)的工作流。 它跨渠道自动化了潜在客户鉴别、外联和买方参与工作流程。[了解详情](../agents/sales-qualifier.md) |

## 2025.10 版本发行说明

**部署日期**：2025 年 10 月 31 日

| 类型 | 项目 | 描述 |
| ---- | ---- | ----------- |
| 功能 | 将历程激活至目标 | 使用新的&#x200B;_激活至目标_&#x200B;公司帐户操作，可直接面向公司进行激活，而非个人。 （此版本仅限于LinkedIn公司。） [了解详情](../journeys/action-nodes.md#activate-to-a-linkedin-destination) |
| 功能 | 品牌主题 | 对于品牌主题，非技术用户现在能够通过添加标准模板上的自定义样式来创建符合特定品牌和设计语言的可重用内容。[了解详情](../content/brand-themes.md) |
| 功能 | 电子邮件模板 – 将图像转换为 HTML | 您现在可以使用存储为JPG或PNG图像文件的设计文件并自动生成电子邮件模板。[了解详情](../content/email-template-image-convert.md) |
| 功能 | 人物角色映射 | 将帐户成员与已建立的角色与属性映射关联起来。[了解详情](../admin/persona-mapping.md) |
| 功能 | 适用于 Salesforce 和 Dynamics 的销售洞察 | 销售团队成员现在可在 Salesforce 或 Dynamics 集成中查看正在成熟的购买群体及相关洞察，从而发现新的销售机会。 包括购买组详细信息，如阶段、分数和相关成员。[了解详情](../buying-groups/incrm-insights.md) |
| 功能 | 将受众激活到[!DNL Adobe Target] | 您现在可以将受众从帐户历程激活到外部客户受众，并将其推送到[!DNL Adobe Target]。 通过此集成，您可以交付通过历程序列有资格参与在[!DNL Target]中设计的Web体验的受众。[了解详情](../audiences/target-external-audience.md) |
| 功能 | Web参与仪表板 | 新功能板，用于深入分析Web访客如何与关键内容进行交互。 它可跨客户行业和区域细分数据，以帮助您了解参与趋势。[了解详情](../dashboards/web-engagement-dashboard.md) |
| 功能 | 角色分析仪表板 | 新的&#x200B;_[!UICONTROL 角色分析]_&#x200B;仪表板提供有关营销活动和历程如何影响购买团体角色获取和参与情况的分析。[了解详情](../buying-groups/buying-group-role-insights.md) |
| 增强功能 | 改进的购买群组完整性评分 | 您现在可以通过为完整性评分自定义角色成员阈值，确保购买群体能够反映真实的决策过程。  [了解详情](../buying-groups/completeness-scores.md) |
| 增强功能 | 购买群组维护作业 | 购买群组维护作业的执行频率已由每周一次更新为每日一次。 |
| 增强功能 | 帐户历程进度 | 对于状态为&#x200B;_运行中_、_对新条目关闭_、_已中止_&#x200B;或&#x200B;_已完成_&#x200B;的已发布历程，您可以打开历程图以查看各节点的帐户列表。 |

>[!NOTE]
>
>这些版本更新于 2025 年 10 月 31 日开始部署，并将分阶段逐步推出各项功能。 功能及增强功能的发布时间可能会有变动。

### 简化的系统架构

Adobe Journey Optimizer B2B Edition 现已采用简化架构。 通过此更新，Journey Optimizer B2B Edition 与 Marketo Engage 不再共享同一系统或数据存储库。 Journey Optimizer B2B Edition 仅从 Adobe Experience Platform 接收数据。 但仍依赖 Marketo Engage 的使用权限及部分配置功能来完成系统的部署与设置。

此更新后的架构带来以下优势：

* **轻松统一并扩展数据**：更新后的平台支持复杂的数据模型，包括自定义对象、购买群组和帐户事件。
* **连接多个 Adobe Marketo Engage 实例**：可在同一位置管理并统一多个 Adobe Marketo Engage 环境中的数据。
* **保障数据安全**：高级隐私与安全功能有助于保护客户信息。
* **面向未来**：此更新为您的组织持续改进与创新奠定基础。

>[!NOTE]
>
>如果在此架构上配置了您的环境，请查看有关配置的[准则](../simplified-architecture.md)。

通过简化的架构，2025.10版本中提供了以下新增功能和增强功能：

| 类型 | 项目 | 描述 |
| ---- | ---- | ----------- |
| 功能 | 关系型数据模型 | 利用链接到B2B帐户的关系数据来过滤帐户历程中的帐户或个性化电子邮件内容。 此关系数据可以表示真实世界的商业实体，如购买记录、事件注册、软件许可证、服务订阅或预订。[了解详情](../admin/xdm-field-management.md#relational-schemas) |
| 功能 | 多个Marketo Engage激活 | 配置与远程Marketo Engage实例的连接，并使用这些连接设置历程的Marketo Engage操作。 这些操作（例如从列表中添加/删除人员，或将人员添加到请求营销活动）适用于指定的Marketo Engage实例。[了解详情](../admin/marketo-actions-connect.md) |
| 功能 | 电子邮件疲劳重复数据删除 | 您现在可以启用电子邮件重复数据删除功能，确保同一历程中不会向同一邮箱地址重复发送相同邮件。 重复的地址将被阻止，直到使用该电子邮件地址的第一条记录完成历程。  [了解详情](../content/email-deduplication.md) |
| 增强功能 | 参与度得分权重 — AEP事件 | 参与度得分权重现在可以包括任何标准或自定义Experience Platform事件，并根据您的需要进行加权。[了解详情](../admin/engagement-score-weighting.md) |
| 增强功能 | 通信限制 | 现在，系统尊重了Marketo Engage和Journey Optimizer B2B edition的组合通信限制。[了解详情](../admin/configure-channels-emails.md#communication-limits) |

<!-- There are additional functional changes with the simplified architecture:

| Item | Description |
| ---- | ----------- |
| Asset management | The system supports an internal asset repository where you can organize folders, edit images, import images, and remove images. It does not support Marketo Engage Design Studio workspaces for asset management. |
| | | -->

## 2025.9 版发行说明

**部署日期**：2025 年 9 月 30 日

此版本包括以下新功能和增强功能：

| 类型 | 项目 | 描述 |
| ---- | ---- | ----------- |
| 功能 | 电子邮件内容协作 | 现在，营销团队可以在电子邮件资源的上下文中与Journey Optimizer B2B edition同事进行评论和协作。 他们可以标记团队成员，以接收包含评论详细信息的电子邮件通知。 通知也可用作脉冲通知。[了解详情](../content/email-collaboration-tools.md) |
| 功能 | 用于电子邮件设计的深色模式 | 电子邮件设计空间现在包含能够切换到&#x200B;_深色模式_&#x200B;的功能。 在深色模式下，您可以预览电子邮件内容，并定义要专门为在深色模式下查看电子邮件的收件人显示的自定义设置。[了解详情](../content/email-dark-mode.md) |
| 增强功能 | 历程 - 按角色的人数拆分路径 | 使用一个通过帐户节点拆分的路径来针对一个具有一个或多个购买群组角色的人数的帐户。 在此路径中，您可以根据角色深度评估购买组对销售警报和其他参与情况的准备情况。[了解详情](../journeys/split-merge-paths-nodes.md#buying-group-filtering-accounts) |
| 增强功能 | 历程 - 事件的人员过滤器 | 使用人员过滤器来侦听人员事件。 这些过滤器包括定位匹配购买组的特定角色的能力。[了解详情](../journeys/listen-for-event-nodes.md#add-filters-to-the-people-event) |

>[!NOTE]
>
>这些版本更新于 2025 年 9 月 30 日开始部署，并将分阶段逐步推出各项功能。 功能及增强功能的发布时间可能会有变动。

## 2025.8 版发行说明

**部署日期**：2025 年 8 月 26 日

此版本包括以下新功能和增强功能：

| 类型 | 项目 | 描述 |
| ---- | ---- | ----------- |
| 功能 | 角色模板和历程的人员参与度评分过滤器 | 现在，您可以在用于创建购买群组的角色模板和拆分路径历程节点中使用&#x200B;_人员参与度分数_&#x200B;作为过滤器。[了解详情](../buying-groups/buying-groups-role-templates.md#add-the-template-roles) |
| 功能 | 购买群组自定义角色配置 | 现在，您可以灵活地为购买组配置自定义角色，从而定义特定于用例的角色。[了解详情](../buying-groups/default-custom-roles.md) |
| 功能 | 参与度评分权重配置 | 您现在可以为影响购买群体参与度评分的活动分配权重。 此功能包括定义您自己的自定义得分模型，以及更改影响参与得分计算的活动模型。[了解详情](../admin/engagement-score-weighting.md) |
| 增强功能 | 片段的条件内容 | 您现在可以使用条件内容工具进行可视化片段设计。[了解详情](../content/conditional-content.md) |
| 增强功能 | 参与度评分更新 | 更新了购买群组参与度评分逻辑，使评分规范化。 此外，您还可以使用成员级别的参与度分数，以及整个购买组的集体参与度分数。[了解详情](../buying-groups/engagement-scores.md) |
| 增强功能 | 活跃历程可观察性——每个节点的帐户 | 对于活跃的帐户历程，您可以访问那些已到达历程中每个帐户节点的帐户的列表。 |

## 2025.6 版发行说明

**部署日期**：2025 年 7 月 15 日

此版本包括以下新功能和增强功能：

| 类型 | 项目 | 描述 |
| ---- | ---- | ----------- |
| 功能 | 与 GenStudio for Performance Marketing 集成 | （数量有限）您现在可以将 GenStudio for Performance Marketing 电子邮件体验与 Journey Optimizer B2B Edition 集成，以提高营销效率并保持品牌一致性。 利用此集成，您可以将GenStudio AI支持的内容创建与Journey Optimizer B2B edition中的高级编排功能结合使用。[了解详情](../content/genstudio-email-workflow.md) |
| 功能 | 垃圾邮件检测报告 | 为避免垃圾邮件过滤器并确保将邮件传递到受众收件箱，您可以直接在电子邮件设计空间生成&#x200B;_垃圾邮件报告_。[了解详情](../content/email-spam-report.md) |
| 功能 | 人员详细信息页面 | 现在，当人员姓名显示在“智能仪表板”、“购买群组详细信息”页面和“帐户详细信息”页面中时（作为超链接），用户可以单击该人员姓名。 此操作将打开关联的人员详细信息页面，其中包含联系人、其活动和最常参与购买团体的信息。[了解详情](../accounts/person-details.md) |
| 功能 | 帐户和购买群组行动 | 直接在帐户详细信息和购买群组详细信息页面上采取行动，有助于意图明确地及时参与。 <li>使用&#x200B;_发送电子邮件_&#x200B;操作将已批准的Marketo Engage电子邮件发送给选定的帐户联系人或购买群组成员。[了解详情](../accounts/account-details.md#send-email) <li>在购买组详细信息中，操作还包括&#x200B;_分配新成员_、_删除成员_&#x200B;和&#x200B;_编辑角色_。[了解详情](../buying-groups/buying-group-details.md#members-tab) |
| 功能 | CRM 内访问详细信息页面 | 现在，您可以在客户关系管理(CRM)工具（如Journey Optimizer或Microsoft Dynamics）中配置指向帐户、联系人和潜在客户的Salesforce B2B edition详细信息页面的直接链接。[了解详情](../accounts/crm-linking.md) |
| 功能 | 用于内容设计的自定义 CSS 支持 | 现在，当您在设计空间中创作电子邮件和登陆页面内容时，可以添加您自己的自定义CSS。[了解详情](../content/design-custom-css.md) |
| 功能 | 意图关键词映射配置 | 要激活和管理意图检测模型，管理员现在可以上传电子表格以定义意图数据映射类别。[了解详情](../admin/intent-data.md) |
| 增强功能 | 模拟电子邮件摘要中的内容 | 当您从电子邮件列表中打开电子邮件时，您现在可以从电子邮件摘要（详细信息和属性）中访问&#x200B;_模拟内容_&#x200B;工具。 此访问权限是电子邮件设计空间的补充。[了解详情](../content/email-simulate-content.md#display-the-email-preview) |
| 增强功能 | 角色模板列表的总数显示 | _[!UICONTROL 角色模板]_&#x200B;列表页面的搜索栏旁边显示总数，进一步得到改进。 |

## 2025.5 版发行说明

**部署日期**：2025 年 6 月 3 日

此版本包括以下新功能和增强功能：

| 类型 | 项目 | 描述 |
| ---- | ---- | ----------- |
| 功能 | 使用 Litmus 进行电子邮件测试 | 通过 [Litmus Enterprise 帐户](https://www.litmus.com/email-testing){target="_blank"}，您现在可以在 Journey Optimizer B2B Edition 中预览电子邮件在主流邮件客户端中的呈现效果。 此集成可帮助您确保电子邮件内容看起来不错，并且在每个电子邮件收件箱中都正常工作。[了解详情](../content/email-test-rendering.md) |
| 增强功能 | 重复的电子邮件 | 当为历程节点添加电子邮件时，您现在可以复制现有的电子邮件。 修改重复电子邮件的设置或内容，也可以保持不变。  [了解详情](../content/add-email.md#add-an-email-to-your-journey) |
| 增强功能 | 电子邮件的 Handlebar 令牌格式 | 电子邮件内容的个性化令牌现在使用一种更新格式，与 Handlebar 脚本完全兼容。 此格式使用&#x200B;_驼峰式大小写_&#x200B;或下划线，消除空格。[了解详情](../content/email-authoring.md#content-authoring---personalization) |
| 增强功能 | 列表的总数显示 | 改进了&#x200B;_[!UICONTROL 解决方案兴趣]_&#x200B;和&#x200B;_[!UICONTROL 帐户历程]_&#x200B;两个列表页面，在搜索栏旁边显示总数。 |

## 2025.4 版发行说明

**部署日期**：2025 年 4 月 29 日

此版本包括以下新功能和增强功能：

| 类型 | 项目 | 描述 |
| ---- | ---- | ----------- |
| 功能 | 帐户列表 | 您现在可以创建静态或动态帐户列表，以按定义的条件（如行业、位置或公司规模）定位指定帐户。<a href="../accounts/account-lists.md">了解详情</a> |
| 功能 | 帐户列表历程编排 | 使用历程操作节点为静态帐户列表添加和删除帐户。<a href="../accounts/account-lists-journeys.md#take-an-action-node---add-to-account">了解详情</a> |
| 增强功能 | 在 Marketo Engage 中筛选历程会员资格 | 对历程受众使用Adobe Journey Optimizer B2B edition帐户列表，然后在Marketo Engage智能列表中使用&#x200B;_帐户列表的成员_&#x200B;筛选器。<a href="../accounts/account-lists-journeys.md#marketo-engage-program---member-of-account-list">了解详情</a> |
| 功能 | 非活动状态过滤器 | 根据Marketo Engage营销活动和项目中的不活动情况编排历程，包括电子邮件不活动、有趣的时刻、数据值更改和访问的网页。<a href="../journeys/split-merge-paths-nodes.md#activity-filtering">了解详情</a> |
| 增强功能 | 访问过的网页过滤器 | 根据与Marketo Engage活动和项目关联的已访问网页的活动编排历程。<a href="../journeys/split-merge-paths-nodes.md#people-path-filters">了解详情</a> |
| 增强功能 | 电子邮件列表 | 查看活动电子邮件和草稿电子邮件的全局列表，以搜索、审阅和更新关联帐户历程中的电子邮件。<a href="../content/emails-list.md">了解详情</a> |

## 2025.3 版发行说明

**部署日期**：2025 年 4 月 1 日

此版本包括以下新功能和增强功能：

| 类型 | 项目 | 描述 |
| ---- | ---- | ----------- |
| 功能 | 重复的帐户历程 | 现在为帐户历程提供重复操作。 您可以复制帐户历程的详细信息，也可以仅复制流量和路径结构的简单框架。<a href="../journeys/journeys-overview.md#duplicate-journey">了解详情</a> |
| 功能 | 我的帐户历程令牌 | 您现在可以定义一组具有帐户历程特定值的自定义令牌。 这组自定义令牌称为&#x200B;_我的令牌_，其中的任何自定义令牌均用于在创作历程电子邮件时进行个性化。<a href="../content/personalization-my-tokens.md">了解详情</a> |
| 功能 | 删除购买群组阶段 | 当购买群组阶段模型处于草稿或已发布状态时，您可以将其删除。 如果该文件已发布（实时），则只能在其与解决方案兴趣无关时将其删除。<a href="../buying-groups/buying-group-stages.md#delete-the-buying-group-stages-model">了解详情</a> |
| 增强功能 | 历程节点数 | 在节点层面提高了已发布历程会员资格数量的可见性。 在&#x200B;_历程图_&#x200B;中，节点会显示&#x200B;_[!UICONTROL 已进入的帐户总数]_。 当营销人员选择操作节点时，右侧的详细信息还包括&#x200B;_[!UICONTROL 尚未对]_&#x200B;执行操作的帐户。 _监听事件_&#x200B;节点的详细信息包括&#x200B;_[!UICONTROL 此步骤中的帐户]_。 此信息对于验证实时、已完成和已中止历程中的帐户进度非常有用。 |

## 2025.2 版发行说明

**部署日期**：2025 年 3 月 11 日

此版本包括以下新功能和增强功能：

| 类型 | 项目 | 描述 |
| ---- | ---- | ----------- |
| 功能 | 可自定义字段——内容片段 | 在设计可视片段的过程中，您可以将片段中某个组件的参数指定为可编辑。 此功能允许电子邮件或模板作者根据自己的需要指定自定义字段值。 此自定义标记仅限用于图像、文本和按钮可视组件。<a href="../content/fragment-authoring.md#enable-fragment-customization">了解详情</a> |
| 功能 | 历程复制类型 | 当您复制帐户历程时，您可以包含节点详细信息，其中不包括 Journey Optimizer B2B Edition 中创建的电子邮件和 SMS 消息。 作为替代方法，您可以创建结构和路径流的骨架副本，而无需节点详细信息和设置。<a href="../journeys/journeys-overview.md#duplicate-journey">了解详情</a> |
| 增强功能 | 另外四个电子邮件模板示例 | 示例电子邮件模板库现在包含四个&#x200B;_SecurFinancial_&#x200B;模板作为重新参与、通知、培养和反馈内容示例的示例。 |

<!-- | Feature | B2B built-in roles and product permissions | Experience Platform now includes a set of built-in (default) roles that you can use to manage access to the B2B product capabilities. <a href="../admin/user-management.md#b2b-built-in-roles">Learn more</a> <br/>Administrators can now define custom roles in Adobe Experience Platform to include Journey Optimizer B2B Edition product permissions.  <a href="../admin/user-management.md#b2b-product-permissions">Learn more</a> | -->

## 2025.1 版发行说明 {#Jan-2025}

**部署日期**：2025 年 2 月 6 日

此版本包括以下新功能和增强功能：

| 类型 | 项目 | 描述 |
| ---- | ---- | ----------- |
| 功能 | 体验事件转发 | 管理员可以配置基于 Adobe Experience Platform（AEP）的事件定义。 这些配置使营销人员能够创建对 AEP 体验事件做出反应的帐户历程。  <a href="../admin/configure-aep-events.md">了解详情</a> |
| 功能 | 付费媒体目标 | 通过帐户历程确定已知人员是否有资格参与付费媒体营销活动，以便您可以在 LinkedIn 等广告平台上进一步吸引他们。 根据特定行为，使用拆分路径节点区段帐户受众，并确定承诺额外参与的帐户。 然后，通过Real-time CDP将这些帐户中的人员添加到外部客户受众到支持的付费媒体目标。<a href="../journeys/action-nodes.md#journey-optimizer-b2b-actions">了解详情</a> |
| 功能 | 智能仪表板 | 查看购买组通过其帐户历程（包括人工智能生成的见解）的进度，以实现更智能的分析并准确划分帐户优先级。<a href="../dashboards/intelligent-dashboard.md">了解详情</a> |
| 功能 | 购买群组和帐户详细信息 | 查看购买群组和帐户级别的洞察，以便在开始吸引客户时掌握更多的背景信息和历史数据。<p>购买组详细信息包括检测到的任何第一方意图。<a href="../buying-groups/buying-group-details.md">了解详情</a><p>帐户详细信息页面突出显示检测到的参与意向激增，以便营销人员能够提醒销售人员哪些帐户已准备好进行以自定义销售为中心的参与。  <a href="../accounts/account-details.md">了解详情</a> |
| 功能 | 历程概述 | 当您访问帐户历程时，“概述”选项卡会提供主要帐户历程的全面情况，使用圆形图和条形图详细说明帐户进度，对完成情况和参与活动进行分类和量化。  <a href="../dashboards/journeys-dashboard.md">了解详情</a> |
| 功能 | 使用 Adobe Express 图像编辑 | Adobe Express快速操作允许您对图像执行简单的编辑（例如裁切和调整大小），以便在内容中更加光滑。<a href="../content/image-edit-adobe-express.md#quick-actions-in-adobe-express">了解详情</a>  <p>为了提供更全面的设计工具，此集成可将完整的 Adobe Express 许可证纳入 Journey Optimizer B2B Edition。 通过此设置，在本地资源工作区中即可访问完整的Adobe Express用户界面。<a href="../content/image-edit-adobe-express.md#adobe-express-enterprise-license">了解详情</a> |
| 功能 | 购买群组角色的意图过滤器 | 当您提交意图关键词时，意图检测模型会根据商机的活动预测具有足够高置信度的感兴趣的解决方案/产品。<a href="../admin/intent-data.md">了解详情</a> <p>此意图数据可用于定义购买群组角色条件<a href="../buying-groups/buying-groups-role-templates.md#add-the-template-roles">了解详情</a> |
| 增强功能 | 在历程中支持 Marketo Engage 事件 | _侦听事件_&#x200B;历程节点现在支持人员级别的两个Marketo Engage事件： _访问网页_&#x200B;和&#x200B;_填写表单_。<a href="../journeys/listen-for-event-nodes.md#listen-for-marketo-engage-event">了解详情</a> |
| 增强功能 | Marketo Engage 智能列表的购买群组过滤器 | 在 Marketo Engage 中查看并创建包含购买群组过滤器的智能列表。 这些添加的过滤器允许您从Journey Optimizer B2B edition中的帐户历程禁止跨多个Marketo Engage营销活动和项目购买组成员，并包括这些组成员。<a href="../buying-groups/marketo-engage-smart-list-buying-group-filters.md">了解详情</a> |
| 增强功能 | 用于历程和角色的 Marketo Engage 列表会员资格过滤器 | 在Journey Optimizer B2B中，检查Marketo Engage列表成员资格以作为&#x200B;_按人员拆分路径_&#x200B;节点的条件，以帮助消除旅程活动中的重复。<a href="../journeys/split-merge-paths-nodes.md#add-a-split-path-by-people-node">了解详情</a> <p> 要购买组角色模板，请使用列表成员资格作为角色条件。<a href="../buying-groups/buying-groups-role-templates.md#add-the-template-roles">了解详情</a> |
| 增强功能 | 参与度概述仪表板 | 此仪表板已更新，提供全面的参与度视图。 它通过快照圆图和随时间变化的趋势显示线形图，显示帐户和个体交互的实时量度。<a href="../dashboards/engagement-dashboard.md">了解详情</a> |

## 2024 版

展开以下列表，了解 2024 年发布的 Journey Optimizer B2B Edition 的功能和增强功能。

+++2024 年 10 月发行说明

**部署日期**：2024 年 10 月 29 日

此版本包括以下新功能和增强功能：

| 类型 | 项目 | 描述 |
| ---- | ---- | ----------- |
| 功能 | 电子邮件中的条件内容 | 根据帐户和潜在客户级别的收件人行为和用户档案特征，个性化您的电子邮件内容。 <p>在电子邮件可视化设计空间中为您的帐户历程创作电子邮件时，请使用条件规则为任何内容组件定义多个变体。<a href="../content/conditional-content.md">了解详情</a> |
| 功能 | 在历程中将人员操作&#x200B;_添加到列表_&#x200B;以及&#x200B;_从列表中移除_ | 在连接的Marketo Engage实例中，使用历程操作与您的帐户Journey Orchestration协调将人员添加到静态列表或从静态列表中删除人员。<a href="../journeys/action-nodes.md">了解详情</a> |
| 功能 | 内容监管和组件锁定 | 要确保遵守批准的内容设计，请使用内容监管功能锁定电子邮件模板内容组件。 在电子邮件模板中激活内容治理后，营销人员可以仅更改允许的元素，以使其与内容策略保持一致。<a href="../content/template-content-governance.md">了解详情</a> |
| 功能 | 购买群组阶段 | 您定义并发布了自定义购买群组暂存模型后，可以在各个购买群组生命周期阶段跟踪购买群组进展情况。 使用这些阶段来确定购买群组成员的下一步最佳操作。 可配置过渡规则和历程节点，以确定暂存进程并根据更改触发操作。<a href="../buying-groups/buying-group-stages.md">了解详情</a> |
| 增强功能 | 新的现成电子邮件模板 | 示例模板库现在包括专为 B2B 营销人员设计的额外电子邮件模板。 使用这些示例模板作为起点，并添加您自己的品牌和消息。<a href="../content/email-templates.md#select-a-design-template">了解详情</a> |
| 增强功能 | 自定义字段作为人员属性 | 如果您在 Experience Platform 中的帐户受众架构中定义了自定义人员字段，这些字段也可用作条件中的人员属性。 将这些自定义属性用于： <li>角色模板<a href="../buying-groups/buying-groups-role-templates.md#add-the-template-roles">了解详情</a></li><li>按人员历程节点的拆分路径<a href="../journeys/split-merge-paths-nodes.md#add-a-split-path-by-people-node">了解详情</a></li> |
| 增强功能 | 电子邮件渠道设置 | 现在可在 Journey Optimizer B2B Edition 界面中看到电子邮件设置。 您可以快速查看当前配置，管理员可以单击&#x200B;_[!UICONTROL 编辑设置]_&#x200B;直接转到Marketo Engage中的设置，并根据组织的要求更新它们。<a href="../admin/configure-channels-emails.md">了解详情</a> |

+++

+++2024 年 9 月发行说明

**部署日期**：2024 年 10 月 7 日

此版本包括以下新功能和增强功能：

| 类型 | 项目 | 描述 |
| ---- | ---- | ----------- |
| 增强功能 | 中央资产库 | 通过增强的&#x200B;_中央资产库_，您可以在 Design Studio 工作区的 Marketo Engage 实例中使用所有图像资产。 内置护栏可防止从 Journey Optimizer B2B Edition 对 Marketo Engage 资产进行编辑、删除和移动的操作。 这些保护措施可确保源资产（Marketo Engage Design Studio）得到保护，同时允许在 Journey Optimizer B2B Edition 中无缝读取和重复使用。<p>对于在Journey Optimizer B2B edition中专门使用的资源，特定工作区提供了完整的资源管理功能。<a href="../content/internal-image-assets.md">了解详情</a> |
| 功能 | 最近访问的资产 | Journey Optimizer B2B Edition 应用程序中的主页现在包含&#x200B;_[!UICONTROL 最近访问的]_&#x200B;部分，该部分为营销人员或管理员提供了最近访问的资产列表。 您可以使用此列表直接前往您最近使用的资产，而无需浏览一系列资产页面进行搜索。 <p>该列表提供了有关修改的额外信息，以便您决定自上次会话以来哪些资产需要进一步修改。 对于电子邮件资产，它显示使用电子邮件资产的帐户历程。<a href="../home-page.md">了解详情</a> |
| 增强功能 | 历程拆分节点——重新排序路径 | 在拆分路径节点中，路径筛选按自上而下的顺序进行评估。 每个人员或每个帐户都沿着第一条匹配的路径前进。 您可以通过单击每个路径卡右上角的向上和向下箭头将定义的路径重新排序，以在列表中将其向上或向下移动。<a href="../journeys/split-merge-paths-nodes.md#split-paths">了解详情</a> |
| 增强功能 | 历程拆分节点——其他活动历史记录条件属性 | 在使用条件定义按人员拆分节点的路径筛选时，有两个额外的属性：_打开的电子邮件_&#x200B;和&#x200B;_是已送达的电子邮件_。 这些添加内容提供了更大的灵活性，可以根据电子邮件活动筛选历程中的人员。<a href="../journeys/split-merge-paths-nodes.md#split-paths-by-accounts">了解详情</a> |

+++

+++2024 年 8 月发行说明

**部署日期**：2024 年 8 月 29 日

此版本包括以下新功能和增强功能：

| 类型 | 项目 | 描述 |
| ---- | ---- | ----------- |
| 功能 | LinkedIn 帐户匹配的受众 | 通过帐户匹配的受众生成 LinkedIn 广告受众，帮助您填充购买群组中的空角色。 通过定义一组购买群组过滤器，您可以维护 LinkedIn 匹配的受众，定位与您的购买群组参数相匹配的潜在客户。 <p>此功能利用Experience Platform目标来管理集成的某些方面。<a href="../data/linkedin-account-matched-audiences.md">了解详情</a> |
| 增强功能 | 可视内容片段的状态生命周期 | 现在使用状态生命周期来管理可视片段。 片段状态决定其是否可用于电子邮件或电子邮件模板，以及您可以对其进行的更改。 <p>此增强的工作流使您可以轻松根据促销和通信日历管理重复使用的内容。<a href="../content/fragments.md#fragment-status-and-lifecycle">了解详情</a> |

+++
