---
title: Journey Optimizer B2B Edition 发行说明
description: 了解 Adobe Journey Optimizer B2B Edition 中的最新功能、增强功能和错误修复——随时了解新功能和产品改进动态。
role: User, Admin
exl-id: 7d3f1c26-d8a6-4065-a70f-5b30cb975dc8
source-git-commit: 6df235bc73066463e5fcfa71dc994f34e13e3ac0
workflow-type: tm+mt
source-wordcount: '3384'
ht-degree: 90%

---

# Journey Optimizer B2B Edition 发行说明

Journey Optimizer B2B Edition 不断地提供新功能，对现有功能进行增强，并修复错误。

Journey Optimizer B2B Edition 原生构建于 [!DNL Adobe Experience Platform] 上，并继承了其最新的创新和改进。在 [Adobe Experience Platform 发行说明](https://experienceleague.adobe.com/zh-hans/docs/experience-platform/release-notes/latest){target="_blank"}中进一步了解这些更改。

查看[产品描述](https://helpx.adobe.com/cn/legal/product-descriptions/adobe-journey-optimizer-b2b.html){target="_blank"}，了解有关权限、性能护栏和限制的信息。

## 2025.10 版发行说明

**部署日期**：2025年10月31日

| 类型 | 项目 | 描述 |
| ---- | ---- | ----------- |
| 功能 | 基于模型的自定义架构 | 从基于模型的类创建自定义架构。 |
| 功能 | 激活到目标 | 使用新的&#x200B;_激活到目标_&#x200B;公司帐户操作直接激活到公司，而不是个人。 （仅限此版本的LinkedIn公司。） |
| 功能 | 品牌主题 | 对于品牌主题，非技术用户现在能够通过添加标准模板上的自定义样式来创建符合特定品牌和设计语言的可重用内容。 [了解详情](../content/brand-themes.md) |
| 功能 | 用户画像映射 | 将帐户成员与已建立的角色与属性映射关联起来。 [了解详情](../admin/persona-mapping.md) |
| 增强功能 | 购买团体维护作业 | 购买组维护作业频率从每周更新到每天。 |
| 增强功能 | 帐户历程进展 | _更多信息_&#x200B;链接对访问帐户计数和列表的历程进程可见。 |

<!-- M1.5 changes
| Enhancement | Buying group scoring | The Buying Group completeness score is improved, including the ability to customize how the score is calculated. | -->

以下代理AI功能现在可在AI Assistant界面中用于Journey Optimizer B2B edition：

| 代理 | 更新 | 描述 |
| ----- | ------ | ----------- |
| Account Qualification Agent | 新的名称 | 在AI助手中使用Account Qualification Agent查看哪些帐户已准备好进行下一阶段。 此代理通过显示高价值潜在客户和自动化资格鉴定工作流程，使您的销售团队成员能够专注于适当的客户。 [了解详情](../agents/account-qualification-agent.md) |

>[!NOTE]
>
>版本更改从2025年10月31日开始部署，并分阶段推出每个功能。 功能及增强功能的发布时间可能会有变动。


<!-- hold for later release 

| Feature | Landing pages | You can now create and publish landing pages in Journey Optimizer B2B Edition to support your journeys and programs. _(Previously a Beta program feature.)_ [Learn more](../content/landing-pages.md) |
| Feature | Forms | You can now create and publish re-usable form components to enable data submission from landing pages that are created and published in Journey Optimizer B2B Edition. _(Previously a Beta program feature.)_ [Learn more](../content/forms.md) |

-->

## 2025.9 版发行说明

**部署日期**：2025 年 9 月 30 日

此版本包括以下新功能和增强功能：

| 类型 | 项目 | 描述 |
| ---- | ---- | ----------- |
| 功能 | 电子邮件内容协作 | 现在，您可以在电子邮件资产的上下文中评论与 Journey Optimizer B2B Edition 用户同事的合作。您可以标记您的团队成员，这样他们就会收到包含评论详细信息的电子邮件通知。也可以使用推送通知的方式。 |
| 功能 | 用于电子邮件设计的深色模式 | 电子邮件设计空间现在包含能够切换到&#x200B;_深色模式_&#x200B;的功能。在深色模式下，您可以预览电子邮件内容，并定义要专门为在深色模式下查看电子邮件的收件人显示的自定义设置。 |
| 功能 | 电子邮件疲劳重复数据删除 | 您现在可以启用电子邮件重复数据删除，以确保在历程中不会将同一电子邮件多次发送到同一地址。 重复的地址将被阻止，直到使用该电子邮件地址的第一条记录完成历程。 |
| 功能 | Salesforce和Dynamics的销售分析 | 销售团队成员现在可以在Salesforce或Dynamics集成中查看到期的购买组和相关见解，以识别新的商机。 包括购买组详细信息，如阶段、分数和相关成员。 |
| 增强功能 | 历程 - 按角色的人数拆分路径 | 使用一个通过帐户节点拆分的路径来针对一个具有一个或多个购买群组角色的人数的帐户。在这个路径中，您可以根据角色深度评估购买群组对销售警报和其他参与行动的意愿。[了解详情](../journeys/split-merge-paths-nodes.md#buying-group-filtering-for-accounts) |
| 增强功能 | 历程 - 事件的人员过滤器 | 使用人员过滤器来侦听人员事件。这些筛选条件可以针对一个匹配的购买群组的某个特定角色。[了解详情](../journeys/listen-for-event-nodes.md#add-filters-to-the-people-event) |

以下代理AI功能现在可在AI Assistant界面中用于Journey Optimizer B2B edition：

| 代理 | 更新 | 描述 |
| ----- | ------ | ----------- |
| 历程生成代理 | 新的名称 | 历程构建代理可实时分析、构思和联合创建历程，使营销人员能够更快地启动、提高参与度并促进更高转化率。 [了解详情](../agents/journey-agent.md) |
| Audience 代理 | 新的名称 | Audience Agent使用结构化和非结构化数据自动识别和构建购买组。 它有助于营销人员更快、更准确地定位适当的人员。 [了解详情](../agents/audience-agent-b2b.md) |

>[!NOTE]
>
>发行版变更将于 2025 年 9 月 30 日开始部署，将分阶段推出每个功能。功能及增强功能的发布时间可能会有变动。

## 2025.8 版发行说明

**部署日期**：2025 年 8 月 26 日

此版本包括以下新功能和增强功能：

| 类型 | 项目 | 描述 |
| ---- | ---- | ----------- |
| 功能 | 角色模板和历程的人员参与度评分过滤器 | 现在，您可以使用&#x200B;_人员参与度评分_&#x200B;作为角色模板中的过滤器，用于创建购买群组和拆分路径历程节点。[了解详情](../buying-groups/buying-groups-role-templates.md#add-the-template-roles) |
| 功能 | 购买群组自定义角色配置 | 您现在可以灵活地为购买群组配置自定义角色，这样您就可以定义您的用例中特有的角色。[了解详情](../buying-groups/default-custom-roles.md) |
| 功能 | 参与度评分权重配置 | 您现在可以为影响购买群体参与度评分的活动分配权重。此功能包括定义您自己的自定义评分模型以及更改会影响参与度评分计算的活跃模型。[了解详情](../admin/engagement-score-weighting.md) |
| 增强功能 | 片段的条件内容 | 您现在可以使用条件内容工具进行视觉片段设计。[了解详情](../content/conditional-content.md) |
| 增强功能 | 参与度评分更新 | 更新了购买群组参与度评分逻辑，使评分规范化。此外，您还可以使用会员级参与度评分以及整个购买群组的集体参与度评分。[了解详情](../buying-groups/engagement-scores.md) |
| 增强功能 | 活跃历程可观察性——每个节点的帐户 | 对于活跃的帐户历程，您可以访问那些已到达历程中每个帐户节点的帐户的列表。 |

## 2025.6 版发行说明

**部署日期**：2025 年 7 月 15 日

此版本包括以下新功能和增强功能：

| 类型 | 项目 | 描述 |
| ---- | ---- | ----------- |
| 功能 | 与 GenStudio for Performance Marketing 集成 | （数量有限）您现在可以将 GenStudio for Performance Marketing 电子邮件体验与 Journey Optimizer B2B Edition 集成，以提高营销效率并保持品牌一致性。通过这种集成，您可以将 GenStudio AI 驱动的内容创建与 Journey Optimizer B2B Edition 中的高级编排功能结合起来。[了解详情](../content/genstudio-email-workflow.md) |
| 功能 | 垃圾邮件检测报告 | 为了避开垃圾邮件过滤器并确保邮件送达受众收件箱，您可以直接在电子邮件设计空间中生成&#x200B;_垃圾邮件报告_。[了解详情](../content/email-spam-report.md) |
| 功能 | 人员详细信息页面 | 现在，当某人的姓名（作为超链接）显示在智能仪表板、购买群组详细信息页面和帐户详细信息页面中时，您可以单击该姓名。此操作将打开相关人员详细信息页面，其中包含有关联系方式、他们的活动以及参与度最高的购买群体的信息。[了解详情](../accounts/person-details.md) |
| 功能 | 帐户和购买群组行动 | 直接在帐户详细信息和购买群组详细信息页面上采取行动，有助于意图明确地及时参与。 <li>使用&#x200B;_发送电子邮件_&#x200B;操作，将已批准的 Marketo Engage 电子邮件发送给选定的帐户联系人或购买群组成员。[了解详情](../accounts/account-details.md#send-emails) <li>在购买群组详细信息中的行动还包括&#x200B;_分配新成员_、_删除成员_&#x200B;和&#x200B;_编辑角色_。[了解详情](../buying-groups/buying-group-details.md#members-tab) |
| 功能 | CRM 内访问详细信息页面 | 现在，您可以在客户关系管理 (CRM) 工具（例如 Salesforce 或 Microsoft Dynamics）中配置导向帐户、联系人和潜在客户的 Journey Optimizer B2B Edition 详细信息页面的直接链接。[了解详情](../accounts/crm-linking.md) |
| 功能 | 用于内容设计的自定义 CSS 支持 | 现在，您可以在设计空间中创作电子邮件和登陆页面内容时添加自己的自定义 CSS。[了解详情](../content/design-custom-css.md) |
| 功能 | 意图关键词映射配置 | 如要启用和管理意图检测模型，您现在可以上传一个电子表格来定义意图数据映射类别。[了解详情](../admin/intent-data.md) |
| 增强功能 | 模拟电子邮件摘要中的内容 | 当您从电子邮件列表中打开电子邮件时，您现在可以从电子邮件摘要（详细信息和属性）中访问&#x200B;_模拟内容_&#x200B;工具。此访问是电子邮件设计空间之外的补充。[了解详情](../content/email-simulate-content.md#display-the-email-preview) |
| 增强功能 | 角色模板列表的总数显示 | _[!UICONTROL 角色模板]_&#x200B;列表页面的搜索栏旁边显示总数，进一步得到改进。 |

<!-- The following capabilities are currently available only for a set of program participants (Beta):

**Brand Kit with AI Assistant** - Maintain brand consistency across email assets by storing and managing brand assets. Add assets, such as colors, fonts, logos, themes, visual content, and compliance guidelines, and use them for your generative AI content creation. -->

## 2025.5 版发行说明

**部署日期**：2025 年 6 月 3 日

此版本包括以下新功能和增强功能：

| 类型 | 项目 | 描述 |
| ---- | ---- | ----------- |
| 功能 | 使用 Litmus 进行电子邮件测试 | 通过 [Litmus Enterprise 帐户](https://www.litmus.com/email-testing){target="_blank"}，您现在可以在 Journey Optimizer B2B Edition 中预览电子邮件在主流邮件客户端中的呈现效果。此集成可帮助您确保电子邮件内容在各大邮箱中均呈现良好，并按预期效果运行。[了解详情](../content/email-test-rendering.md) |
| 增强功能 | 重复的电子邮件 | 当为历程节点添加电子邮件时，您现在可以复制现有的电子邮件。修改重复电子邮件的设置或内容，也可以保持不变。[了解详情](../content/add-email.md#add-an-email-to-your-journey) |
| 增强功能 | 电子邮件的 Handlebar 令牌格式 | 电子邮件内容的个性化令牌现在使用一种更新格式，与 Handlebar 脚本完全兼容。此格式使用&#x200B;_驼峰式大小写_&#x200B;或下划线，不使用空格。[了解详情](../content/email-authoring.md#content-authoring---personalization) |
| 增强功能 | 列表的总数显示 | 改进了&#x200B;_[!UICONTROL 解决方案兴趣]_&#x200B;和&#x200B;_[!UICONTROL 帐户历程]_&#x200B;两个列表页面，在搜索栏旁边显示总数。 |

## 2025.4 版发行说明

**部署日期**：2025 年 4 月 29 日

此版本包括以下新功能和增强功能：

| 类型 | 项目 | 描述 |
| ---- | ---- | ----------- |
| 功能 | 帐户列表 | 您现在可以创建静态或动态帐户列表，以根据您定义的标准（例如行业、地点或公司规模）定位命名帐户。<a href="../accounts/account-lists.md">了解详情</a> |
| 功能 | 帐户列表历程编排 | 使用历程操作节点来添加和移除静态帐户列表的帐户。<a href="../accounts/account-lists-journeys.md#take-an-action-node---add-to-account">了解详情</a> |
| 增强功能 | 在 Marketo Engage 中筛选历程会员资格 | 为历程受众使用 Adobe Journey Optimizer B2B Edition 帐户列表，然后使用 Marketo Engage 智能列表中的&#x200B;_帐户列表会员_&#x200B;过滤器。<a href="../accounts/account-lists-journeys.md#marketo-engage-program---member-of-account-list">了解详情</a> |
| 功能 | 非活动状态过滤器 | 根据 Marketo Engage 营销活动和计划中的非活动状态来编排历程，包括电子邮件非活动状态、有趣的时刻、数据值变化和访问过的网页。<a href="../journeys/split-merge-paths-nodes.md#activity-filtering">了解详情</a> |
| 增强功能 | 访问过的网页过滤器 | 根据与 Marketo Engage 营销活动和计划相关联的访问过的网页的活动状态来编排历程。<a href="../journeys/split-merge-paths-nodes.md#people-path-filters">了解详情</a> |
| 增强功能 | 电子邮件列表 | 查看活跃电子邮件和草稿电子邮件的全局列表，以便在相关联的帐户历程中搜索、审查和更新它们。<a href="../content/emails-list.md">了解详情</a> |

## 2025.3 版发行说明

**部署日期**：2025 年 4 月 1 日

此版本包括以下新功能和增强功能：

| 类型 | 项目 | 描述 |
| ---- | ---- | ----------- |
| 功能 | 重复的帐户历程 | 现在为帐户历程提供重复操作。您可以复制帐户历程的详细信息，或者仅复制流程和路径结构的简单框架。<a href="../journeys/journey-overview.md#duplicate-journey">了解详情</a> |
| 功能 | 我的账户历程令牌 | 您现在可以定义一组具有帐户历程特定值的自定义令牌。这组自定义令牌被称为&#x200B;_我的令牌_，所有这些自定义令牌都可以在创作历程电子邮件时用于进行个性化。<a href="../content/personalization-my-tokens.md">了解详情</a> |
| 功能 | 删除购买群组阶段 | 当购买群组阶段模型处于草稿或已发布状态时，您可以将其删除。如果它已发布（上线），则只有当它与任何解决方案兴趣都无关联时，您才能删除。<a href="../buying-groups/buying-group-stages.md#delete-the-buying-group-stages-model">了解详情</a> |
| 增强功能 | 历程节点数 | 在节点层面提高了已发布历程会员资格数量的可见性。在&#x200B;_历程图_&#x200B;中，节点会显示&#x200B;_[!UICONTROL 已进入的帐户总数]_。当您选择并操作节点时，右侧的详细信息还包括&#x200B;_[!UICONTROL 尚未执行操作的帐户]_。_监听事件_&#x200B;节点的详细信息包括&#x200B;_[!UICONTROL 此步骤中的帐户]_。使用此信息来验证您正在进行的、已完成的和已中止的历程中的帐户进展。 |

## 2025.2 版发行说明

**部署日期**：2025 年 3 月 11 日

此版本包括以下新功能和增强功能：

| 类型 | 项目 | 描述 |
| ---- | ---- | ----------- |
| 功能 | 可自定义字段——内容片段 | 在设计可视片段的过程中，您可以将片段中某个组件的参数指定为可编辑。此功能允许电子邮件或模板作者根据自己的需要指定自定义字段值。此自定义标志仅限于图像、文本和按钮可视组件。<a href="../content/fragment-authoring.md#enable-fragment-customization">了解详情</a> |
| 功能 | 历程复制类型 | 当您复制帐户历程时，您可以包含节点详细信息，其中不包括 Journey Optimizer B2B Edition 中创建的电子邮件和 SMS 消息。或者，您可以创建结构和路径流的精简副本，而不包含节点详细信息和设置。<a href="../journeys/journey-overview.md#duplicate-journey">了解详情</a> |
| 增强功能 | 另外四个电子邮件模板示例 | 示例电子邮件模板库现在包含四个 SecurFinacial 模板，作为重新参与、通知、培养和反馈内容的示例 |

<!-- | Feature | B2B built-in roles and product permissions | Experience Platform now includes a set of built-in (default) roles that you can use to manage access to the B2B product capabilities. <a href="../admin/user-management.md#b2b-built-in-roles">Learn more</a> <br/>Administrators can now define custom roles in Adobe Experience Platform to include Journey Optimizer B2B Edition product permissions.  <a href="../admin/user-management.md#b2b-product-permissions">Learn more</a> | -->

## 2025.1 版发行说明 {#Jan-2025}

**部署日期**：2025 年 2 月 6 日

此版本包括以下新功能和增强功能：

| 类型 | 项目 | 描述 |
| ---- | ---- | ----------- |
| 功能 | 体验事件转发 | 管理员可以配置基于 Adobe Experience Platform（AEP）的事件定义。这些配置使营销人员能够创建对 AEP 体验事件做出反应的帐户历程。<a href="../admin/configure-aep-events.md">了解详情</a> |
| 功能 | 付费媒体目标 | 通过帐户历程确定已知人员是否有资格参与付费媒体营销活动，以便您可以在 LinkedIn 等广告平台上进一步吸引他们。根据特定行为，使用拆分路径节点区段帐户受众，并确定承诺额外参与的帐户。然后，通过 Real-Time CDP 将这些帐户中的人员添加到外部客户受众中，并将其添加到受支持的付费媒体目标中。<a href="../journeys/action-nodes.md#journey-optimizer-b2b-actions">了解详情</a> |
| 功能 | 智能仪表板 | 查看购买群组在帐户历程中的进展情况，包括 AI 生成的洞察，以便进行更智能的分析和准确的帐户优先级排序。<a href="../dashboards/intelligent-dashboard.md">了解详情</a> |
| 功能 | 购买群组和帐户详细信息 | 查看购买群组和帐户级别的洞察，以便在开始吸引客户时掌握更多的背景信息和历史数据。<p>购买群组详细信息包括识别到的任何第一方意图。<a href="../buying-groups/buying-group-details.md">了解详情</a><p>帐户详细信息帐户突出显示了识别到的参与意图激增，这样您就可以告知销售人员那些愿意参与定制销售互动的帐户。<a href="../accounts/account-details.md">了解详情</a> |
| 功能 | 历程概述 | 当您访问帐户历程时，“概述”选项卡会提供主要帐户历程的全面情况，使用圆形图和条形图详细说明帐户进度，对完成情况和参与活动进行分类和量化。<a href="../dashboards/journeys-dashboard.md">了解详情</a> |
| 功能 | 使用 Adobe Express 图像编辑 | Adobe Express 快速操作允许您对图像进行简单的编辑（例如裁剪和调整大小），以使内容看起来更加精美。<a href="../content/image-edit-adobe-express.md#quick-actions-in-adobe-express">了解详情</a>  <p>为了提供更全面的设计工具，此集成可将完整的 Adobe Express 许可证纳入 Journey Optimizer B2B Edition。通过此设置，可在本地资产工作区内访问完整的 Adobe Express 用户界面。<a href="../content/image-edit-adobe-express.md#adobe-express-enterprise-license">了解详情</a> |
| 功能 | 购买群组角色的意图过滤器 | 您提交意图关键词后，意图检测模型会根据潜在客户的活动，以足够高的置信度预测感兴趣的解决方案/产品。<a href="../admin/intent-data.md">了解详情</a> <p>此意图数据可用于定义购买群组角色条件<a href="../buying-groups/buying-groups-role-templates.md#add-the-template-roles">了解详情</a> |
| 增强功能 | 在历程中支持 Marketo Engage 事件 | _侦听事件_&#x200B;历程节点现在支持人员级别的两个 Marketo Engage 事件：_访问网页_&#x200B;和&#x200B;_填写表单_。<a href="../journeys/listen-for-event-nodes.md#listen-for-marketo-engage-event">了解详情</a> |
| 增强功能 | Marketo Engage 智能列表的购买群组过滤器 | 在 Marketo Engage 中查看并创建包含购买群组过滤器的智能列表。通过这些添加的过滤器，您可以从 Journey Optimizer B2B Edition 帐户历程中抑制或包含 Marketo Engage 营销活动和计划中的购买群组成员。<a href="../buying-groups/marketo-engage-smart-list-buying-group-filters.md">了解详情</a> |
| 增强功能 | 用于历程和角色的 Marketo Engage 列表会员资格过滤器 | 在 Journey Optimizer B2B 中，检查 Marketo Engage 列表会员资格作为&#x200B;_按人员拆分路径_&#x200B;节点的条件，以帮助消除历程活动中的重复。<a href="../journeys/split-merge-paths-nodes.md#add-a-split-path-by-people-node">了解详情</a> <p> 为购买群组角色模板使用列表会员资格作为角色条件。<a href="../buying-groups/buying-groups-role-templates.md#add-the-template-roles">了解详情</a> |
| 增强功能 | 参与度概述仪表板 | 此仪表板已更新，提供全面的参与度视图。它通过快照圆形图和显示一段时间内趋势的线形图，展示帐户和个人互动的实时量度。<a href="../dashboards/engagement-dashboard.md">了解详情</a> |

## 2024 版

展开以下列表，了解 2024 年发布的 Journey Optimizer B2B Edition 的功能和增强功能。

+++2024 年 10 月发行说明

**部署日期**：2024 年 10 月 29 日

此版本包括以下新功能和增强功能：

| 类型 | 项目 | 描述 |
| ---- | ---- | ----------- |
| 功能 | 电子邮件中的条件内容 | 根据收件人的行为和轮廓特征个性化您的电子邮件内容——无论是在帐户级别还是潜在客户级别。 <p>当您在电子邮件可视设计空间中为您的帐户历程创作电子邮件时，使用条件规则为任何内容组件定义多个变体。<a href="../content/conditional-content.md">了解详情</a> |
| 功能 | 在历程中将人员操作&#x200B;_添加到列表_&#x200B;以及&#x200B;_从列表中移除_ | 根据收件人的行为和轮廓特征个性化您的电子邮件内容——无论是在帐户级别还是潜在客户级别。<a href="../journeys/action-nodes.md">了解详情</a> |
| 功能 | 内容监管和组件锁定 | 要确保遵守批准的内容设计，请使用内容监管功能锁定电子邮件模板内容组件。在电子邮件模板中激活内容监管后，营销人员只能更改允许的元素，使其与内容策略保持一致。<a href="../content/template-content-governance.md">了解详情</a> |
| 功能 | 购买群组阶段 | 您定义并发布了自定义购买群组暂存模型后，可以在各个购买群组生命周期阶段跟踪购买群组进展情况。使用这些阶段来确定购买群组成员的下一步最佳操作。您可以配置过渡规则和历程节点，确定阶段进展情况并根据变化触发操作。<a href="../buying-groups/buying-group-stages.md">了解详情</a> |
| 增强功能 | 新的现成电子邮件模板 | 示例模板库现在包括专为 B2B 营销人员设计的额外电子邮件模板。使用这些示例模板作为起点，添加您自己的品牌和消息。<a href="../content/email-templates.md#select-a-design-template">了解详情</a> |
| 增强功能 | 自定义字段作为人员属性 | 如果您在 Experience Platform 中的帐户受众架构中定义了自定义人员字段，这些字段也可用作条件中的人员属性。将这些自定义属性用于： <li>角色模板<a href="../buying-groups/buying-groups-role-templates.md#add-the-template-roles">了解详情</a></li><li>按人员历程节点的拆分路径<a href="../journeys/split-merge-paths-nodes.md#add-a-split-path-by-people-node">了解详情</a></li> |
| 增强功能 | 电子邮件渠道设置 | 现在可在 Journey Optimizer B2B Edition 界面中看到电子邮件设置。您可以快速查看当前配置，管理员可以单击&#x200B;_[!UICONTROL 编辑设置]_，直接转到 Marketo Engage 中的设置，并根据组织的要求进行更新。<a href="../admin/configure-channels-emails.md">了解详情</a> |

+++

+++2024 年 9 月发行说明

**部署日期**：2024 年 10 月 7 日

此版本包括以下新功能和增强功能：

| 类型 | 项目 | 描述 |
| ---- | ---- | ----------- |
| 增强功能 | 中央资产库 | 通过增强的&#x200B;_中央资产库_，您可以在 Design Studio 工作区的 Marketo Engage 实例中使用所有图像资产。内置护栏可防止从 Journey Optimizer B2B Edition 对 Marketo Engage 资产进行编辑、删除和移动的操作。这些保护措施可确保源资产（Marketo Engage Design Studio）得到保护，同时允许在 Journey Optimizer B2B Edition 中无缝读取和重复使用。<p>对于专供 Journey Optimizer B2B Edition 使用的资产，有一个特定的工作区提供完整的资产管理功能。<a href="../content/marketo-engage-design-studio.md">了解详情</a> |
| 功能 | 最近访问的资产 | Journey Optimizer B2B Edition 应用程序中的主页现在包含&#x200B;_[!UICONTROL 最近访问的]_&#x200B;部分，该部分为营销人员或管理员提供了最近访问的资产列表。您可以使用此列表直接前往您最近使用的资产，而无需浏览一系列资产页面进行搜索。 <p>该列表提供了有关修改的额外信息，以便您决定自上次会话以来哪些资产需要进一步修改。在电子邮件资产方面，它显示了使用电子邮件资产的帐户历程。<a href="../home-page.md">了解详情</a> |
| 增强功能 | 历程拆分节点——重新排序路径 | 在拆分路径节点中，路径筛选按自上而下的顺序进行评估。每个人员或每个帐户都沿着第一条匹配的路径前进。您可以通过单击每个路径卡右上角的上下箭头来重新排序已定义的路径，将其在列表中向上或向下移动。<a href="../journeys/split-merge-paths-nodes.md#split-paths">了解详情</a> |
| 增强功能 | 历程拆分节点——其他活动历史记录条件属性 | 在使用条件定义按人员拆分节点的路径筛选时，有两个额外的属性：_打开的电子邮件_&#x200B;和&#x200B;_是已送达的电子邮件_。这些额外属性为历程中根据电子邮件活动筛选的人员提供了更大的灵活性。<a href="../journeys/journey-nodes.md#split-paths">了解详情</a> |

+++

+++2024 年 8 月发行说明

**部署日期**：2024 年 8 月 29 日

此版本包括以下新功能和增强功能：

| 类型 | 项目 | 描述 |
| ---- | ---- | ----------- |
| 功能 | LinkedIn 帐户匹配的受众 | 通过帐户匹配的受众生成 LinkedIn 广告受众，帮助您填充购买群组中的空角色。通过定义一组购买群组过滤器，您可以维护 LinkedIn 匹配的受众，定位与您的购买群组参数相匹配的潜在客户。 <p>此功能利用 Experience Platform Destinations 来管理集成的某些方面。<a href="../data/linkedin-account-matched-audiences.md">了解详情</a> |
| 增强功能 | 可视内容片段的状态生命周期 | 现在使用状态生命周期来管理可视片段。片段状态决定其是否可用于电子邮件或电子邮件模板，以及您可以对其进行的更改。 <p>这种增强的工作流使您可以根据促销和通信日程表轻松管理重复使用的内容。<a href="../content/fragments.md#fragment-status-and-lifecycle">了解详情</a> |

+++
