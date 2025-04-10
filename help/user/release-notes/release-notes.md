---
title: 发行说明
description: Adobe Journey Optimizer B2B Edition 的最新发行说明
exl-id: 7d3f1c26-d8a6-4065-a70f-5b30cb975dc8
source-git-commit: 775cecb2aa4e305ba9a80ba0655e5e854ddf69e2
workflow-type: tm+mt
source-wordcount: '1863'
ht-degree: 87%

---

# Journey Optimizer B2B Edition 发行说明

Journey Optimizer B2B Edition 不断地提供新功能，对现有功能进行增强，并修复错误。

Journey Optimizer B2B Edition 原生构建于 [!DNL Adobe Experience Platform] 上，并继承了其最新的创新和改进。在 [Adobe Experience Platform 发行说明](https://experienceleague.adobe.com/zh-hans/docs/experience-platform/release-notes/latest){target="_blank"}中，进一步了解这些更改。

查看[产品描述](https://helpx.adobe.com/cn/legal/product-descriptions/adobe-journey-optimizer-b2b.html){target="_blank"}，了解有关权限、性能护栏和限制的信息。

## 2025.3 发行说明

**发行日期**：2025年4月1日

此版本包括以下新功能和增强功能：

| 类型 | 项目 | 描述 |
| ---- | ---- | ----------- |
| 新功能 | 帐户列表 | 您现在可以创建静态或动态帐户列表，以按定义的条件（如行业、位置或公司规模）定位指定帐户。 <a href="../accounts/account-lists.md">了解详情</a> |
| 新功能 | 帐户历程的我的令牌 | 您现在可以使用特定于帐户历程的值定义一组自定义令牌。 这组自定义令牌称为&#x200B;_我的令牌_，其中的任何自定义令牌均用于在创作历程电子邮件时进行个性化。 <a href="../content/personalization-my-tokens.md">了解详情</a> |
| 新功能 | 删除购买组阶段 | 当购买组阶段模型处于草稿或已发布状态时，您可以将其删除。 如果该文件已发布（实时），则只能在其与解决方案兴趣无关时将其删除。 <a href="../buying-groups/buying-group-stages.md#delete-the-buying-group-stages-model">了解详情</a> |
| 增强功能 | 历程节点计数 | 改进了节点级别上已发布历程成员资格计数的可见性。 在&#x200B;_历程映射_&#x200B;中，节点显示&#x200B;_[!UICONTROL 输入的帐户总数]_。 当您选择并操作节点时，右侧的详细信息还包括&#x200B;_[!UICONTROL 尚未对]_&#x200B;执行操作的帐户。 _侦听事件_&#x200B;节点的详细信息包括此步骤&#x200B;]_中的_[!UICONTROL &#x200B;帐户。 使用此信息验证您的实时、已完成和已中止历程中的帐户进展。 |

## 2025.2 发行说明

**发布日期**：2025 年 3 月 11 日

此版本包括以下新功能和增强功能：

| 类型 | 项目 | 描述 |
| ---- | ---- | ----------- |
| 新功能 | 可自定义字段——内容片段 | 作为内容片段设计者，您可以将片段中组件的参数指定为可编辑。这允许电子邮件或模板作者根据自己的需要指定自定义字段值。此自定义标志仅限于图像、文本和按钮可视组件。<a href="../content/fragment-authoring.md#enable-fragment-customization">了解详情</a> |
| 新功能 | B2B 内置角色和产品权限 | Experience Platform 现在包含一组内置（默认）角色，您可以使用它们来管理对 B2B 产品功能的访问。<a href="../admin/user-management.md#b2b-built-in-roles">了解详情</a> <br/>管理员现在可以在 Adobe Experience Platform 中定义自定义角色，以包含 Journey Optimizer B2B Edition 产品权限。<a href="../admin/user-management.md#b2b-product-permissions">了解详情</a> |
| 新功能 | 历程重复类型 | 复制帐户历程时，您可以包含节点详细信息，但不包括在Journey Optimizer B2B edition中创建的电子邮件和短信消息。 作为替代方法，您可以创建结构和路径流的骨架副本，而无需节点详细信息和设置。 <a href="../journeys/journey-overview.md#duplicate-journey">了解详情</a> |
| 增强功能 | 另外四个电子邮件模板示例 | 示例电子邮件模板库现在包含四个 SecurFinacial 模板，作为重新参与、通知、培养和反馈内容的示例 |

## 2025.1 发行说明 {#Jan-2025}

**发行日期**：2025 年 2 月 6 日

此版本包括以下新功能和增强功能：

| 类型 | 项目 | 描述 |
| ---- | ---- | ----------- |
| 新功能 | 体验事件转发 | 管理员可以配置基于 Adobe Experience Platform（AEP）的事件定义。这些配置使营销人员能够创建对 AEP 体验事件做出反应的帐户历程。<a href="../admin/configure-aep-events.md">了解详情</a> |
| 新功能 | 付费媒体目标 | 通过帐户历程确定已知人员是否有资格参与付费媒体营销活动，以便您可以在 LinkedIn 等广告平台上进一步吸引他们。在帐户历程中使用拆分路径节点，根据特定行为细分帐户受众，并确定承诺额外参与的帐户。然后，通过 Real-Time CDP 将这些帐户中的人员添加到外部客户受众中，并将其添加到受支持的付费媒体目标中。<a href="../journeys/action-nodes.md#journey-optimizer-b2b-actions">了解详情</a> |
| 新功能 | 智能仪表板 | 查看购买群组在帐户历程中的进展情况，包括 AI 生成的洞察，以便进行更智能的分析和准确的帐户优先级排序。<a href="../dashboards/intelligent-dashboard.md">了解详情</a> |
| 新功能 | 购买群组和帐户详细信息 | 查看购买群组和帐户级别的洞察，以便在开始吸引客户时掌握更多的背景信息和历史数据。<p>购买群组详细信息包括识别到的任何第一方意图。<a href="../buying-groups/buying-group-details.md">了解详情</a><p>帐户详细信息帐户突出显示了识别到的参与意图激增，这样您就可以告知销售人员那些愿意参与定制销售互动的帐户。<a href="../accounts/account-details.md">了解详情</a> |
| 新功能 | 历程概述 | 当您访问帐户历程时，“概述”选项卡会提供主要帐户历程的全面情况，使用圆形图和条形图详细说明帐户进度，对完成情况和参与活动进行分类和量化。<a href="../dashboards/journeys-dashboard.md">了解详情</a> |
| 新功能 | 使用 Adobe Express 图像编辑 | Adobe Express 快速操作允许您对图像进行简单的编辑（例如裁剪和调整大小），以使内容看起来更加精美。<a href="../content/image-edit-adobe-express.md#quick-actions-in-adobe-express">了解详情</a>  <p>为了提供更全面的设计工具，此集成可将完整的 Adobe Express 许可证纳入 Journey Optimizer B2B Edition。通过此设置，可在本地资产工作区内访问完整的 Adobe Express 用户界面。<a href="../content/image-edit-adobe-express.md#adobe-express-enterprise-license">了解详情</a> |
| 新功能 | 购买群组角色的意图过滤器 | 您提交意图关键词后，意图检测模型会根据潜在客户的活动，以足够高的置信度预测感兴趣的解决方案/产品。<a href="../admin/intent-data.md">了解详情</a> <p>此意图数据可用于定义购买群组角色条件<a href="../buying-groups/buying-groups-role-templates.md#add-the-template-roles">了解详情</a> |
| 增强功能 | 在历程中支持 Marketo Engage 事件 | _侦听事件_&#x200B;历程节点现在支持人员级别的两个 Marketo Engage 事件：_访问网页_&#x200B;和&#x200B;_填写表单_。<a href="../journeys/listen-for-event-nodes.md#listen-for-marketo-engage-event">了解详情</a> |
| 增强功能 | Marketo Engage 智能列表的购买群组过滤器 | 在 Marketo Engage 中查看并创建包含购买群组过滤器的智能列表。通过这些添加的过滤器，您可以从 Journey Optimizer B2B Edition 帐户历程中抑制或包含 Marketo Engage 营销活动和计划中的购买群组成员。<a href="../buying-groups/marketo-engage-smart-list-buying-group-filters.md">了解详情</a> |
| 增强功能 | 用于历程和角色的 Marketo Engage 列表会员资格过滤器 | 在 Journey Optimizer B2B 中，检查 Marketo Engage 列表会员资格作为&#x200B;_按人员拆分路径_&#x200B;节点的条件，以帮助消除历程活动中的重复。<a href="../journeys/split-merge-paths-nodes.md#add-a-split-path-by-people-node">了解详情</a> <p> 为购买群组角色模板使用列表会员资格作为角色条件。<a href="../buying-groups/buying-groups-role-templates.md#add-the-template-roles">了解详情</a> |
| 增强功能 | 参与度概述仪表板 | 此仪表板已更新，提供全面的参与度视图。它通过快照圆形图和显示一段时间内趋势的线形图，展示帐户和个人互动的实时量度。<a href="../dashboards/engagement-dashboard.md">了解详情</a> |


## 2024 年 10 月发行说明 {#Oct-2024}

**发行日期**：2024 年 10 月 29 日

此版本包括以下新功能和增强功能：

| 类型 | 项目 | 描述 |
| ---- | ---- | ----------- |
| 新功能 | 电子邮件模板中的条件内容 | 根据收件人的行为和轮廓特征个性化您的电子邮件内容——无论是在帐户级别还是潜在客户级别。 <p>当您在电子邮件可视设计空间中为您的帐户历程创作电子邮件时，使用条件规则为任何内容组件定义多个变体。<a href="../content/conditional-content.md">了解详情</a> |
| 新功能 | 在历程中将人员操作&#x200B;_添加到列表_&#x200B;以及&#x200B;_从列表中移除_ | 根据收件人的行为和轮廓特征个性化您的电子邮件内容——无论是在帐户级别还是潜在客户级别。<a href="../journeys/action-nodes.md">了解详情</a> |
| 新功能 | 内容监管和组件锁定 | 要确保遵守批准的内容设计，请使用内容监管功能锁定电子邮件模板内容组件。在电子邮件模板中激活内容监管后，营销人员只能更改允许的元素，使其与内容策略保持一致。<a href="../content/template-content-governance.md">了解详情</a> |
| 新功能 | 购买群组阶段 | 您定义并发布了自定义购买群组暂存模型后，可以在各个购买群组生命周期阶段跟踪购买群组进展情况。使用这些阶段来确定购买群组成员的下一步最佳操作。您可以配置过渡规则和历程节点，确定阶段进展情况并根据变化触发操作。<a href="../buying-groups/buying-group-stages.md">了解详情</a> |
| 增强功能 | 新的现成电子邮件模板 | 示例模板库现在包括专为 B2B 营销人员设计的额外电子邮件模板。使用这些示例模板作为起点，添加您自己的品牌和消息。<a href="../content/email-templates.md#select-a-design-template">了解详情</a> |
| 增强功能 | 自定义字段作为人员属性 | 如果您在 Experience Platform 中的帐户受众架构中定义了自定义人员字段，这些字段也可用作条件中的人员属性。将这些自定义属性用于： <li>角色模板<a href="../buying-groups/buying-groups-role-templates.md#add-the-template-roles">了解详情</a></li><li>按人员历程节点的拆分路径<a href="../journeys/split-merge-paths-nodes.md#add-a-split-path-by-people-node">了解详情</a></li> |
| 增强功能 | 电子邮件渠道设置 | 现在可在 Journey Optimizer B2B Edition 界面中看到电子邮件设置。您可以快速查看当前配置，管理员可以单击&#x200B;_[!UICONTROL 编辑设置]_，直接转到 Marketo Engage 中的设置，并根据组织的要求进行更新。<a href="../admin/configure-channels-emails.md">了解详情</a> |

## 2024 年 9 月发行说明 {#Sept-2024}

**发行日期**：2024 年 10 月 7 日

此版本包括以下新功能和增强功能：

| 类型 | 项目 | 描述 |
| ---- | ---- | ----------- |
| 增强功能 | 中央资产库 | 通过增强的&#x200B;_中央资产库_，您可以在 Design Studio 工作区的 Marketo Engage 实例中使用所有图像资产。内置护栏可防止从 Journey Optimizer B2B Edition 对 Marketo Engage 资产进行编辑、删除和移动的操作。这些保护措施可确保源资产（Marketo Engage Design Studio）得到保护，同时允许在 Journey Optimizer B2B Edition 中无缝读取和重复使用。<p>对于专供 Journey Optimizer B2B Edition 使用的资产，有一个特定的工作区提供完整的资产管理功能。<a href="../content/marketo-engage-design-studio.md">了解详情</a> |
| 新功能 | 最近访问的资产 | Journey Optimizer B2B Edition 应用程序中的主页现在包含&#x200B;_[!UICONTROL 最近访问的]_&#x200B;部分，该部分为营销人员或管理员提供了最近访问的资产列表。您可以使用此列表直接前往您最近使用的资产，而无需浏览一系列资产页面进行搜索。 <p>该列表提供了有关修改的额外信息，以便您决定自上次会话以来哪些资产需要进一步修改。在电子邮件资产方面，它显示了使用电子邮件资产的帐户历程。<a href="../home-page.md">了解详情</a> |
| 增强功能 | 历程拆分节点——重新排序路径 | 在拆分路径节点中，路径筛选按自上而下的顺序进行评估。每个人员或每个帐户都沿着第一条匹配的路径前进。您可以通过单击每个路径卡右上角的上下箭头来重新排序已定义的路径，将其在列表中向上或向下移动。<a href="../journeys/split-merge-paths-nodes.md#split-paths">了解详情</a> |
| 增强功能 | 历程拆分节点——其他活动历史记录条件属性 | 在使用条件定义按人员拆分节点的路径筛选时，有两个额外的属性：_打开的电子邮件_&#x200B;和&#x200B;_是已送达的电子邮件_。这些额外属性为历程中根据电子邮件活动筛选的人员提供了更大的灵活性。<a href="../journeys/journey-nodes.md#split-paths">了解详情</a> |

## 2024 年 8 月发行说明 {#Aug-2024}

**发行日期**：2024 年 8 月 29 日

此版本包括以下新功能和增强功能：

| 类型 | 项目 | 描述 |
| ---- | ---- | ----------- |
| 新功能 | LinkedIn 帐户匹配的受众 | 通过帐户匹配的受众生成 LinkedIn 广告受众，帮助您填充购买群组中的空角色。通过定义一组购买群组过滤器，您可以维护 LinkedIn 匹配的受众，定位与您的购买群组参数相匹配的潜在客户。 <p>此功能利用 Experience Platform Destinations 来管理集成的某些方面。<a href="../data/linkedin-account-matched-audiences.md">了解详情</a> |
| 增强功能 | 可视内容片段的状态生命周期 | 现在使用状态生命周期来管理可视片段。片段状态决定其是否可用于电子邮件或电子邮件模板，以及您可以对其进行的更改。 <p>这种增强的工作流使您可以根据促销和通信日程表轻松管理重复使用的内容。<a href="../content/fragments.md#fragment-status-and-lifecycle">了解详情</a> |
