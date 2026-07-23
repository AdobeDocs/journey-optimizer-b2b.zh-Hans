---
title: 销售限定词
description: 通过Sales Qualifier自动化B2B潜在客户鉴定和推广。 它为BDR提供AI支持的研究、电子邮件起草、CRM集成和AI出站工作流。
feature: Agentic AI, Sales Insights, Account Journeys
role: User
exl-id: cc590444-41df-44fe-830b-92241718ee81
autotag-review: '2026-06-05T16:42:16.451Z'
TQID: 'https://experienceleague.adobe.com/VNgs0cTpjCTG7JpFjFErnVMmRtR-gmw-iRRHZanZDUs'
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2:
  - id: c8f3fb27-3167-48ac-a66a-fa4bc3f58dda
  - id: fc1ff3b2-6614-41ad-a113-de48597598fd
  - id: f979fe0e-02fe-4599-b492-7b3df1d4e7dc
subfeature_v2:
  - id: fe583b80-65a2-48c2-b4e1-9ea8fbac0a8a
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
  - id: fd2e3797-f2ea-4b36-a9af-52acf5e90513
source-git-commit: a5145b53d6b5c9462392f7c540a81b7d85abdd7b
workflow-type: tm+mt
source-wordcount: 6084
ht-degree: 1%

---

# 销售限定词

Sales Qualifier是一个人工智能驱动的应用程序，可与Adobe Journey Optimizer B2B edition一起使用。 它实施了Account Qualification Agent，旨在简化业务开发代表(BDR)的工作流。 Sales Qualifier跨渠道自动执行潜在客户鉴别、外联和买方参与工作流程。 它减少了手动BDR负载，加快了企业B2B公司的管道速度。

BDR可以使用浏览器和电子邮件插件直接在CRM或Outlook中访问商业智能。 以下视频简要演示了Sales Qualifier和Account Qualification Agent。

>[!VIDEO](https://video.tv.adobe.com/v/3476571?captions=chi_hans)

## 应用程序主页

销售限定符包含在[!UICONTROL Journey Optimizer B2B edition]中，但它是Adobe Experience Platform中的单独应用程序。

![销售限定词主屏幕](./assets/home-screen.png){width="800" zoomable="yes"}

### Account Qualification 代理

Account Qualification Agent (AQA)是Sales Qualifier的核心。 AQA使用人工智能读取您的帐户，并确定哪些帐户已准备好执行下一步。 当您的组织已连接CRM时，它有助于研究、电子邮件草稿和了解CRM的上下文。

<!--
## Edit the left navigation bar

At the bottom left of the application, click the _Edit_ ( ![Edit icon](../assets/do-not-localize/icon-edit.svg) ) icon to control which elements are visible in the left navigation. You can also drag and drop them to reorder as you want.
-->

### 基本代理使用情况

Adobe AI代理使用&#x200B;_自然语言查询_，这意味着他们在文本提示中使用与您与某人交谈时相同的语言。 你越详细，结果就越好。

使用自然语言，您可以要求代理：

* `Tell me the latest financial results of Bodea`
* `Tell me more about hiring at TechNova`
* `Tell me about the new AI features in Bodea LumaSecure4`

通过优化提示来迭代出站工作流，以获取所需的结果。 例如：

* _从收入电话或报告等上下文中起草后续电子邮件。_ 最多120字。 主题行：引人入胜，包含关键主题。 简介：从上下文源中的直接引号开始。 正文：连接到棘手问题和价值主张。 CTA：建议拨打短线电话以进一步探索。_

* _此电子邮件的目标是开始对话并建立信任。_ 起草一封有120个字的电子邮件，其语气具有咨询性和同理心。 避免使用过于熟悉或销售方法，不要使用“希望您一切顺利”、“登记就行”或“请”等词语。_

### 产品访问和用户组

对Sales Qualifier功能的访问通过Adobe Admin Console中的两个用户组进行管理。 产品管理员必须在用户引导期间设置群组，然后才能访问应用程序。

#### 销售限定词用户

用户必须是`Sales Qualifier`用户组的成员才能访问Sales Qualifier应用程序。

1. 在Adobe Admin Console中，创建一个名为`Sales Qualifier`的用户组。
1. 将&#x200B;**默认的生产所有访问权限** AEP配置文件分配给组。
1. 添加需要访问Sales Qualifier的用户

#### 销售限定词管理员

配置[CRM连接](#integrations-and-crm)、[知识中心](#knowledge-center)和全局电子邮件选择退出设置的管理员也必须是`Sales Qualifier Admins`用户组的成员。

1. 在Adobe Admin Console中，创建一个名为`Sales Qualifier Admins`的用户组。
1. 将管理员添加到`Sales Qualifier`和`Sales Qualifier Admins`组。

两个群组的成员身份使&#x200B;**[!UICONTROL 管理员设置]**&#x200B;在左侧导航栏的&#x200B;**[!UICONTROL 管理]**&#x200B;下可见。 标准用户可以使用配置的字段、筛选器和行动手册，配置的选择退出页脚将应用于其出站电子邮件。 他们无法更改这些设置。

>[!NOTE]
>
>用户组名必须与上一步骤中所示完全匹配。

## 潜在客户

在左侧导航中选择&#x200B;**[!UICONTROL 潜在客户]**&#x200B;以查看您可以访问的潜在客户列表。 该列表提供了对信息的快速查看，如潜在客户状态和上次活动。

![显示潜在客户管理的潜在客户状态和最后一个活动的潜在客户表](./assets/prospects.png){width="800" zoomable="yes"}

### 构建潜在客户列表

潜在客户列表将来自多个来源的人员组合在一起：

* **CRM源潜在客户** — 当您连接CRM时，它会自动导入连接用户拥有的潜在客户。 查看[集成和CRM](#integrations-and-crm)。
* **导入的潜在客户** — 从CSV文件导入潜在客户列表。
* **手动添加潜在客户** — 直接在应用程序中添加个人。

要添加不来自您的CRM的潜在客户，请执行以下操作：

1. 在&#x200B;**[!UICONTROL 潜在客户]**&#x200B;页面上，选择&#x200B;**[!UICONTROL 添加潜在客户]**。
1. 选择&#x200B;**[!UICONTROL 导入CSV]**&#x200B;或&#x200B;**[!UICONTROL 手动添加]**。

   * 对于CSV导入，请上传该文件并将其列映射到目标客户字段。
   * 要手动添加人员，请在表单中输入其详细信息。

1. 选择&#x200B;**[!UICONTROL 保存]**。

### 筛选和查找潜在客户

选择&#x200B;_筛选器_ ![筛选器图标](../../assets/do-not-localize/icon_filter-outline.svg)图标以缩小列表范围。 您可以按以下项过滤：

* 潜在客户状态
* 参与度评分
* 营销标记的有趣时刻
* 星级得分和火焰得分
* 关联的交易

管理员还可以使映射的CRM字段可用作过滤器。 在&#x200B;**[!UICONTROL 管理员设置]**&#x200B;中，他们为代表用于查找潜在客户的字段打开&#x200B;**[!UICONTROL 可筛选]**。 查看[映射CRM字段](#map-crm-fields-inbound-mapping)。

### 查看目标客户详细信息

选择目标客户以打开其配置文件。 在联系您之前，先查看重要的信号：

* **活动列表** — 按时间顺序排列的潜在客户活动列表，顶部有&#x200B;**AI活动摘要**，其中突出显示最新的相关行为。
* **时间线视图** — 跨渠道参与的可视时间线。
* **已查看内容** — 直接从活动中打开潜在客户查看的实际内容，如网页或资产。

## 帐户

在左侧导航中选择&#x200B;**[!UICONTROL 帐户]**&#x200B;以使用您销售到的帐户。 销售鉴定表将第一流的详细信息、渠道和参与结合在一起，以便您可以在客户层优先开展外展活动。

客户概述总结了收入、行业、公司规模和总部等基本要素。 除了这些详细信息外，每个帐户还会显示：

* **开放机会** — 与帐户关联的开放机会（来自您的连接CRM），以使外展与活动管道保持一致。
* **参与次数最多的会员** — 帐户中参与次数最近的联系人，以便您了解购买组内哪些人需要优先处理。
* **CRM输入** — 从连接的CRM中显示的帐户字段、商机和所有者信息。 请参阅[集成和CRM](#integrations-and-crm)，以了解如何映射此数据。

### 帐户深入研究

要开始深入分析，请开立一个账户。 Account Qualification Agent (AQA)会优先显示与贵组织的销售策略最相关的信号，以便您快速了解客户所在的位置并确定下一步行动。

## 出站工作流

>[!NOTE]
>
>产品管理员创建的出站工作流会与组织中的所有用户共享。

_出站工作流_&#x200B;是Sales Qualifier用于运行目标驱动节奏的结构。 您定义外联目标和定位标准，AI将建议多点接触节奏并为每个潜在客户编写个性化的电子邮件内容。 在注册激活节奏之前，您可以审核并批准每封电子邮件，以便仅在配置的窗口期间发送消息。

出站工作流会连接四个元素：

* **目标** — 您要从推广中获得的结果（例如，预订发现电话或驾驶事件注册）。
* **定位过滤器** — 确定哪些潜在客户符合条件的条件。
* **接触点的节奏** — 步骤的有序顺序，每个步骤在计划的一天完成。 接触点可以是&#x200B;**电子邮件**、**电话**&#x200B;或&#x200B;**LinkedIn InMails**。
* **个性化电子邮件内容** — 对于每个电子邮件接触点，AI将使用潜在客户个人资料、帐户上下文、参与历史记录和最近新闻来草稿内容。

目标驱动下游所有内容：AI使用它来建议定位过滤器、设计节奏、草稿接触点提示并为每个生成的电子邮件塑造个性化。

![出站工作流概述选项卡](./assets/outbound-workflow-overview.png){width="800" zoomable="yes"}

### 重要概念

| 概念 | 描述 |
| --- | --- |
| **工作流** | 由目标、定向过滤器、节奏和设置定义的可重用出站活动。 |
| **目标** | 外联工作应该取得什么成果。 |
| **接触点** | 按计划相对于注册步调执行一步（电子邮件、电话或链接In Mail）。 |
| **接触点提示** | 在生成潜在客户的电子邮件正文和主题时，AI将遵循相关说明，包括语调、时长、焦点和call to action。 |
| **节奏** | 接触点的完整序列：数量、顺序以及日期。 |
| **定位筛选器** | 将工作流限制为潜在客户子集的条件。 |
| **草稿** | 已生成准备好进行审查但尚未批准的电子邮件。 |
| **推理** | AI对其如何撰写给定电子邮件（使用的信号和数据源）的解释。 |
| **注册** | 批准目标客户的草稿，这将激活节奏并在工作流的发送窗口将电子邮件排入队列，以便发送。 |

以下各节描述了整个生命周期：在向导中创建工作流、审查生成的电子邮件、批准潜在客户以及管理随时间变化的工作流。

### 创建出站工作流

工作流创建是一个五步向导：**目标**、**定位**、**生成接触点**、**设置**&#x200B;和&#x200B;**添加潜在客户**。 每个步骤都建立在最后一步之上；您的初始目标决定了每个后续决策。

1. 在左侧导航中，选择&#x200B;**[!UICONTROL 出站工作流]**。

1. 在&#x200B;**[!UICONTROL 浏览]**&#x200B;选项卡上，单击右上角的&#x200B;**[!UICONTROL +创建工作流]**。

#### 步骤1：定义目标

目标是最重要的输入：它告知AI成功的外观，并锚定定位、节奏和电子邮件生成。

1. 选择&#x200B;**[!UICONTROL 从头开始]**&#x200B;以编写您自己的目标，或选择&#x200B;**[!UICONTROL 从模板开始]**&#x200B;以使用已保存的模板。

   ![从头开始创建出站工作流](./assets/outbound-workflow-create-start-from-scratch.png){width="700" zoomable="yes"}

1. 选择&#x200B;**[!UICONTROL 推荐目标]**&#x200B;之一作为起点，或输入您自己的目标。

1. 单击&#x200B;**[!UICONTROL 下一步：定位]**。

目标在陈述&#x200B;**具体结果**&#x200B;时效果最佳，而不仅仅是主题。 要让AI更好地工作，请使用诸如`Book a 15-minute discovery call with marketing leaders evaluating campaign automation`之类的目标而不是`Promote campaign automation`。

#### 步骤2：配置定位过滤器

定位过滤器定义哪些潜在客户符合条件。 当您稍后添加潜在客户时，只有符合这些过滤器的潜在客户才会显示在选择列表中。

1. 单击向下箭头以显示&#x200B;**[!UICONTROL 添加筛选器]**&#x200B;列表并选择要应用的筛选器。

   ![创建出站工作流定位过滤器](./assets/outbound-workflow-create-targeting-filter-list.png){width="700" zoomable="yes"}

1. 设置筛选器的值。

1. 如果需要缩小受众，请添加更多过滤器。

   ![创建出站工作流定位已添加具有值的筛选器](./assets/outbound-workflow-create-targeting-filters-values.png){width="600" zoomable="yes"}

1. 单击&#x200B;**[!UICONTROL 下一步：生成接触点]**。

#### 步骤3：生成并查看接触点

设置定位后，AI将构建&#x200B;**_节奏_**：它会分析您的目标和定位，定义接触点序列，并为每个步骤编写&#x200B;**_接触点提示_**。 在特定的一天中，您会看到每个接触点出现多步频率。 节奏可以混合使用电子邮件、电话和LinkedIn InMail步骤。

![出站工作流生成的接触点节奏和提示](./assets/outbound-workflow-create-touchpoints.png){width="700" zoomable="yes"}

要读取其提示，请展开电子邮件接触点。 此说明在编写每个潜在客户的电子邮件时指导AI，包括语调、时长、焦点和&#x200B;_call to action_。

**重新生成节奏**

如果节奏不是您想要的，请单击&#x200B;**[!UICONTROL 重新生成]**&#x200B;并输入精简指令。 例如：

* `Make it 3 touchpoints across 2 weeks`
* `Lead with an executive briefing offer in the first email`
* `Add a nurture touch focused on a relevant case study`

AI会根据您的指令重写整个节奏。

要调整单个电子邮件接触点而不重新生成整个节奏，请直接在其文本区域中编辑提示文本。

**在提示中使用行动手册**

如果您的组织已在[知识中心](#knowledge-center)中构建行动手册，则可以在编写电子邮件时指示AI从中提取。 在提示符下，命名文档以及您希望AI使用的上下文，例如，`Use the ABC positioning guide from the Knowledge Center and focus on the security value proposition`。 然后，生成的电子邮件将反映该剧本中的消息传送。

当节奏和提示看起来正确时，单击&#x200B;**[!UICONTROL 下一步：设置]**。

在生成潜在客户之前优化接触点提示很重要：这些提示是AI以后用于每个潜在客户的核心指令。 此处逗留时间可缩放到所有生成的电子邮件。

#### 步骤4：配置工作流设置

**设置**&#x200B;步骤控制工作流的运行方式。

![出站工作流设置](./assets/outbound-workflow-create-settings.png){width="700" zoomable="yes"}

1. 查看&#x200B;**[!UICONTROL 工作流名称]**，如果想要更清晰的标签，请更改该名称。
1. 在&#x200B;**[!UICONTROL 每个工作流的最大潜在客户数]**&#x200B;中，确认工作流可以同时管理多少潜在客户的上限。
1. 设置&#x200B;**[!UICONTROL 发送窗口]**&#x200B;为允许发送出站电子邮件的小时数。
1. 打开&#x200B;**[!UICONTROL 跳过周末]**，将周末的任何接触点移动到下一个工作日。
1. 若要在潜在客户预订会议后自动停止跟进接触点，请打开&#x200B;**[!UICONTROL 会议预订暂停]**。
1. 确认&#x200B;**[!UICONTROL 时区]**&#x200B;与您的受众匹配。
1. 单击&#x200B;**[!UICONTROL 保存并添加潜在客户]**。

选择退出页脚由管理员全局配置，并独立于工作流设置应用于出站电子邮件。 请参阅[全局选择退出同步](#global-opt-out-sync)。

#### 步骤5：添加潜在客户并开始生成电子邮件

保存将打开潜在客户选择视图，该视图已被您的步骤2目标定位所过滤。

![出站工作流添加潜在客户](./assets/outbound-workflow-create-add-prospects.png){width="700" zoomable="yes"}

1. 查看列表。

   行通常包括潜在客户名称、帐户、电子邮件、职务、参与状态和潜在客户状态。

1. 如果需要展开或缩小列表，请在此处调整筛选器。
1. 使用复选框选择潜在客户。
1. 单击&#x200B;**[!UICONTROL 下一步：查看接触点]**&#x200B;以开始&#x200B;**每个潜在客户**&#x200B;电子邮件生成。

AI会为节奏中&#x200B;**每个电子邮件接触点**&#x200B;的每个所选潜在客户生成个性化电子邮件。 Phone和LinkedIn InMail接触点按照计划的步骤保持不变。 生成可在后台运行 — 如果要在完成时继续其他工作，请使用&#x200B;**[!UICONTROL 准备就绪时通知]**。

对于每个潜在客户，AI将每个接触点提示与特定于潜在客户的数据（人员、帐户、参与历史记录、最近新闻）组合在一起，以产生主题行和正文。

### 查看和优化生成的电子邮件

生成完成后，工作流详细信息视图会显示用于审阅草稿的横幅。 需要审阅，在获得批准之前不会发送任何内容。

![出站工作流审核生成的电子邮件](./assets/outbound-workflow-create-review-generated-emails.png){width="700" zoomable="yes"}

1. 在工作流详细信息视图中，单击横幅中的&#x200B;**[!UICONTROL 审核草稿]**。
1. **[!UICONTROL 查看接触点]**&#x200B;步骤有两个选项卡：
   * **[!UICONTROL 准备好审查]** — 已完成生成的电子邮件。
   * **[!UICONTROL 正在生成]** — 仍在写入电子邮件。
1. 在左侧的目标客户列表中，单击某个名称以在右侧加载该目标客户的接触点。
1. 在接触点上使用V形(**>**)展开并读取完整的主题行和正文。

#### 阅读AI推理

对于每个生成的电子邮件，**[!UICONTROL 推理]**&#x200B;说明AI如何创建该消息，包括信号、属性和塑造内容和call to action的源。 在批准之前，请查看此信息并验证个性化。

![出站工作流生成的电子邮件人工智能推理](./assets/outbound-workflow-create-review-generated-email-reasoning.png){width="600" zoomable="yes"}

#### 直接编辑电子邮件

对于少量编辑（措辞、语调、单句）：

1. 在展开的接触点上，单击&#x200B;_编辑_&#x200B;图标以打开编辑器。
1. 编辑主题行或正文。
1. 单击&#x200B;**[!UICONTROL 保存]**。

#### 使用AI优化电子邮件

对于较大的更改（重新构建、转移强调或重新设置消息框架），请使用&#x200B;**[!UICONTROL 使用AI生成]**。 AI代理重写电子邮件，同时保留个性化上下文。

1. 在电子邮件编辑器中，单击&#x200B;**[!UICONTROL 使用AI生成]**。

   ![出站工作流使用AI生成的电子邮件细化](./assets/outbound-workflow-create-review-generated-email-edit-regenerate.png){width="600" zoomable="yes"}

1. 输入明确的指令，例如：
   * `Make it shorter and more direct. Keep it under 100 words.`
   * `Focus more on the prospect's role and how the solution helps them specifically.`
   * `Change the call-to-action to suggest a 15-minute introductory call instead.`
1. 查看修订版，并根据需要手动调整。
1. 单击&#x200B;**[!UICONTROL 保存]**。

>[!TIP]
>
>直接编辑套装的措辞和语气。 使用&#x200B;_[!UICONTROL 通过AI生成]_&#x200B;从头开始重写电子邮件。

### 批准和注册潜在客户

审批可激活目标客户的节奏。 在潜在客户获得批准和注册之前，系统不会向他们发送电子邮件。

1. 在左边的目标客户列表中，选择您审查并准备发送其电子邮件的目标客户。
1. 单击&#x200B;**[!UICONTROL 批准并注册潜在客户]** （右下角）。

![出站工作流选择和审批潜在客户](./assets/outbound-workflow-create-approve-enroll-prospects.png){width="700" zoomable="yes"}

在每个接触点相对于注册的预定日期内，在配置好的&#x200B;**时区**&#x200B;的工作流&#x200B;**发送窗口**&#x200B;内发送已批准的电子邮件。 在您采取行动之前，您未批准的潜在客户将保留在&#x200B;**[!UICONTROL 准备审核]**&#x200B;中。 批准后，工作流将根据您定义的节奏运行。

### 管理现有工作流

在&#x200B;_[!UICONTROL 出站工作流]_&#x200B;页面上，**[!UICONTROL 浏览]**&#x200B;选项卡列出了每个工作流。 每个信息卡都会显示目标、配置的接触点和性能指标。 使用此视图可监视活动的工作流、返回仍需要审核的草稿，或打开工作流以添加更多潜在客户。

### 出站工作流最佳实践

* **投资目标。** 下游定位、节奏和电子邮件都会追溯到目标。 具体的、以结果为重点的目标要优于模糊的目标。
* **在每个潜在客户生成之前完成接触点提示。** 在批量生成之后，通常一次只对一个潜在客户进行更改。
* **使用推理作为质量检查。** 如果强调了错误的信号（或明显缺少信号），请编辑电子邮件或重新访问接触点提示并重新生成频率。
* **将编辑工具与更改匹配。** 直接编辑文字和语调；**[!UICONTROL 使用AI生成]**&#x200B;以进行重组或重新定格。
* **仅批准您审查的内容。** 在注册之前，先展开接触点、阅读内容并在必要时对其进行优化。

### 全局选择退出同步

管理员可以为每个出站电子邮件附加一个使用预批准[!DNL Marketo]措辞的轻触式取消订阅页脚。 当目标客户选择选择退出链接时，销售限定词将永久阻止目标客户接收更多电子邮件，并将选择退出状态同步回连接的CRM。 请参阅[配置全局电子邮件选择退出](#configure-global-email-opt-out)。

## 电子邮件发件箱

电子邮件发件箱面板列出了您发送的所有自动电子邮件。

<!--
## Meeting bookings

This panel displays all meetings set up through automation.

## Chat inbox

This panel displays all your chat threads.

![Panel showing chat threads with contact and thread summaries for sales automation](assets/chat-inbox.png)

You can interact with clients, and see summaries for the contact and the thread so that you can quickly know where you are in the thread.

-->

## 任务

销售鉴定表中的&#x200B;_任务_&#x200B;区域为业务开发代表(BDR)提供了一个专用空间，用于管理和处理其出站工作流操作。 出站工作流引擎会自动生成任务，这些任务代表BDR需要对每个潜在客户执行的特定操作 — 电话呼叫、LinkedIn InMails和电子邮件审核。

任务管理体验是&#x200B;**处理队列**，而不是待办事项列表。 您可以打开任务、执行操作、标记任务完成并移至下一个任务 — 所有这些操作都无需离开页面。

在左侧导航栏中选择&#x200B;**[!UICONTROL 任务]**&#x200B;以打开完整的任务页面。 此页面是逐个处理任务的主要工作区。

![显示任务队列和详细信息面板的任务页面](./assets/tasks.png){width="800" zoomable="yes"}

<!--
**Homepage feed** - The homepage displays a running feed of your most urgent tasks, with overdue items at the top followed by today's tasks. Each item in the feed has an "Open" button that takes you directly to that task in the Tasks page with the detail panel already loaded.
-->

### 任务类型

所有任务都与出站工作流步骤相关联。 有三种类型：

**电话呼叫** — 在节奏到达电话呼叫步骤时创建。 任务面板显示座席生成的提示点以及用于捕获呼叫备注的内联备注字段。

**LinkedIn InMail** — 在节奏到达LinkedIn InMail步骤时创建。 任务面板显示AI生成的主题行和消息正文，您可以复制这些主题行和消息正文并在产品外部发送。

**电子邮件审阅** — 在系统完成为已注册工作流中的潜在客户生成个性化电子邮件后创建。 您可以在出站开始之前，审核并批准该潜在客户的电子邮件。 每个潜在客户都会获得一个单独的电子邮件审核任务；如果您在工作流中注册了10个潜在客户，则当生成完成时，您最多会看到10个电子邮件审核任务。

### 任务管理

“任务”页面分为两个面板：

* **左 — 任务列表：**&#x200B;您的任务队列，根据您选择的查看和排序设置排序和过滤。
* **右 — 任务工作面板：**&#x200B;选定任务的详细信息，包括目标客户信息、工作流上下文、任务特定的内容和操作控件。

在左侧面板中选择任何任务都会将其详细信息加载到右侧面板，而无需导航离开页面。

#### 队列控件

工作面板包含按顺序在任务队列中移动的&#x200B;**Next**&#x200B;和&#x200B;**Previous**&#x200B;控件。 队列会遵循您应用于列表的任何排序和过滤设置。 因此，如果您正在处理按截止日期排序的逾期电话呼叫任务，则&#x200B;_下一个_&#x200B;和&#x200B;_上一个_&#x200B;将完全按照该设置移动。

将任务标记为完成时，面板会自动前进到队列中的下一个任务。

#### 注释

对于“电话通话”和LinkedIn Mail任务，工作面板中提供了内联注释字段。 注释会在您单击离开时自动保存，这样当您在标记当前任务完成之前导航到其他任务时，便不会丢失注释。

#### 任务操作

使用以下操作管理您的任务：

* **[!UICONTROL 标记完成]** — 主要操作。 在执行任务后使用此操作 — 进行调用、发送InMail或审核并批准电子邮件。 完成后，任务被记录为&#x200B;**已完成**，队列自动前进。

* **[!UICONTROL 跳过接触点]** — 可从工作面板的溢出菜单访问。 当您无法完成此步骤，但潜在客户仍然是工作流中的有效目标时，请使用此选项。
  * 前景一步一步地前进。 未来的任务仍按计划生成。
  * 选择原因： *联系人信息错误*、*计时错误*、*内容不相关*&#x200B;或&#x200B;*其他*（使用自由文本字段）。
  * 任务状态设置为&#x200B;**已跳过**，并使用原因和时间戳进行记录。
  * 如果这是工作流中的最后一个步骤，则潜在客户的工作流运行将结束。 该任务仍记录为“已跳过（未删除）”。

* **[!UICONTROL 从工作流中删除]** — 可从工作面板的溢出菜单访问。 当目标客户不再属于此工作流时，使用此选项。

  从工作流中删除潜在客户时：
  * 此工作流中该潜在客户的所有待定和未来任务都已取消。
  * 潜在客户的注册状态更改为&#x200B;**由BDR**&#x200B;删除。
  * 选择原因： *离开公司*、*重复*、*调整错误*、*已转换*&#x200B;或&#x200B;*其他*（使用文本字段）。
  * 出现确认对话框： *&quot;此操作将取消[工作流名称]中[潜在客户]的所有其余接触点。 是否继续？&quot;*
  * 任务状态设置为&#x200B;**已删除**。 所有已取消的同级任务也标记为&#x200B;**已移除**。

>[!NOTE]
>
>跳过和删除原因数据会通知Analytics，包括渠道跳过率、工作流删除率和主要原因。 这有助于提高工作流质量，并会随着时间的推移通知性能分析。

**自动跳过**

如果停滞不前的LinkedIn InMail和电话呼叫任务两天仍未完成，则会自动跳过这些任务。 自动跳过可使潜在客户在节奏中移动而不会停止运行，并且不会影响电子邮件时间线。 计划的电子邮件接触点将继续按计划发送。

### 任务状态

每个任务都会经历以下状态：

| 状态 | 描述 |
|---|---|
| **挂起** | 已创建，但尚未完成上一个工作流步骤。 在您的任务列表中不可见。 |
| **即将推出** | 上一步已完成，但到期日期是将来的日期。 可见和可操作 — 如果时机正确，您可以提前完成它。 |
| **打开** | 今天到期。 可见且可操作。 |
| **过期** | 过期日期，尚未完成。 可见、可操作并具有视觉标记。 |
| **已完成** | 您已执行任务并将任务标记为完成。 |
| **跳过** | 您已跳过此接触点。 工作流中的潜在客户前进。 |
| **已删除** | 您已从工作流中删除潜在客户。 已取消所有同级任务。 |
| **已取消** | 由于工作流更改或潜在客户移除而取消系统。 |

### 列表视图

使用任务列表顶部的选项卡在视图之间切换：

* **今天** *（默认）* — 今天到期的任务尚未完成。

* **超期** — 到期日期已过，且仍未结束的任务。 请先解决这些任务。

* **即将开始** — 具有未来到期日期的任务，其中已完成上一个工作流步骤。 这些任务会提前显示，因此如果时间安排得当（例如，如果您已经在与潜在客户通话），您可以提前计划或提前采取行动。 将显示计划的到期日期，以便您了解预期的时间。

* **已完成** — 您已完成、跳过或删除的任务的记录。 用于审查和审计目的。

### 筛选和搜索

有多种方法可筛选任务列表：

* 使用多选列表按任务类型筛选。 选择多个类型会显示与所选类型中的&#x200B;*任意*&#x200B;匹配的任务（例如，电话呼叫&#x200B;**或**&#x200B;电子邮件审核）。

* 按任务状态筛选。 选择多个状态会显示与任意选定状态匹配的任务。

* 使用&#x200B;**AND**&#x200B;逻辑跨组筛选。 例如，`Type = Phone Call and Status = Overdue`只显示过期呼叫任务。

使用搜索栏按潜在客户名称、公司名称或预订名称查找任务。 搜索与任何活动的过滤器一起应用。 仅文本匹配 — 精确的部分匹配，无模糊搜索。

### 排序

使用&#x200B;**排序依据**&#x200B;控件选择任务列表的排序方式。 排序还可确定下一个和上一个在队列中的移动顺序。

| 排序选项 | 行为 |
|---|---|
| **到期日期（升序）** *（默认）* | 最早到期日期在前。 超期任务显示在今天的任务之前。 |
| **到期日期（降序）** | 最晚到期日期在前。 |
| **创建日期（最新）** | 首先显示最近创建的任务。 |
| **创建日期（最早）** | 最先创建的任务最旧。 |
| **任务类型** | 按类型按顺序分组：电话呼叫→LinkedIn InMail→电子邮件审核。 在每个组内，按到期日期升序排序。 |

### 超期任务

如果任务尚未完成，则会在到期日后的第二天过期。 超期任务：

* 显示在&#x200B;**过期**&#x200B;视图中，并位于主页信息源的顶部。
* 在任务列表中显示为“过期”标记。
* 保持完全可操作 — 您可以完成、跳过或删除它们。

### 近期任务

即使下一个步骤到期日期仍在未来，仍会在潜在客户完成工作流步骤时创建即将执行的任务。 这种可见性让您可以及早将insight纳入到您的渠道中，这样您就可以在机会出现时提前规划或提前行动。

近期任务会显示其计划的截止日期，因此您始终知道应何时解决这些任务。 完全支持提前完成即将到来的任务 — 工作流引擎记录实际完成日期并正常提前潜在客户。

### 任务完成

任务完成不限于任务页面。

**参与的潜在客户视图：**&#x200B;参与潜在客户页面上的接触点预览包括&#x200B;_标记完成_&#x200B;操作，以及内容预览和可选注释字段。 在此处完成任务会立即在“任务”页面中更新其状态。 此视图不会触发自动前进行为 — 它是一个视图和操作界面，而不是队列处理界面。

**Salesforce （CRM插件）：** Salesforce中的Sales Qualifier插件在出站工作流信息卡中显示任务状态（即将执行、挂起、已完成、过期、跳过）。 在当前版本中，CRM卡是&#x200B;**只读** — 您可以看到任务状态，但必须从Sales Qualifier中完成任务。

### 空状态

* **今天没有任务：**&#x200B;您看到一封&#x200B;_您今天已全部完成_&#x200B;邮件。 如果存在即将执行的任务，则提示将显示为&#x200B;_您有[N]即将执行的任务 — 查看即将执行的任务_。
* **存在逾期任务：**&#x200B;出现提示时，建议您先处理逾期任务。

## 会议预订

Sales Qualifier在不离开出站流程的情况下将参与的对话转换为已预订的会议。 在连接日历时，销售限定词将生成一个个人预订链接，潜在客户将使用该链接来为您安排时间。

* **预订链接** — 在[配置文件设置](#profile-settings)中配置日历连接和可用性。 可以将预订链接添加到您的电子邮件签名中，使其显示在出站电子邮件中。
* **以节奏自动插入** — 销售限定词将预订链接以节奏插入合适的位置，以便在最相关时显示邀请。 您可以手动覆盖投放位置。
* **Booking暂停** — 当潜在客户预订会议时，**[!UICONTROL Meeting Booking暂停]**&#x200B;将自动停止进一步的跟进。 请参阅[配置工作流设置](#step-4-configure-workflow-settings)。

在[性能](#performance)部分中跟踪预订结果。

## 知识中心

_[!UICONTROL 知识中心]_&#x200B;允许Account Qualification Agent (AQA)访问您自己的销售资料，以便销售鉴定表可以生成反映贵组织销售情况的研究、鉴定见解和推广活动。 构建和管理行动手册是一项管理员任务。

![知识中心](./assets/integrations-knowledge-center.png){width="700" zoomable="yes"}

### 上传销售宣传资料

1. 在左侧导航中，展开&#x200B;**[!UICONTROL 管理]**，然后选择&#x200B;**[!UICONTROL 管理设置]**。
1. 选择&#x200B;**[!UICONTROL 集成]**&#x200B;下的&#x200B;**[!UICONTROL 知识中心]**。
1. 设置Sales Qualifier用于调查您的公司和草稿电子邮件的&#x200B;**[!UICONTROL 公司名称]**&#x200B;和&#x200B;**[!UICONTROL 公司URL]**。
1. 以PDF、PPTX或DOCX格式上传销售重头戏、理想客户档案(ICP)、定位指南和其他销售宣传资料。

每个上载的文档都显示其处理状态（如&#x200B;**[!UICONTROL 就绪]**）以及上次更新的时间。

### 构建行动手册

上传文档后，选择&#x200B;**[!UICONTROL 生成行动手册]**&#x200B;以将其转换为行动手册。

>[!NOTE]
>
>行动手册需要大约24小时的处理时间才能准备使用。

当行动手册准备就绪时，它会提供外联和援助：

* **出站电子邮件提示** — 在生成电子邮件时，通过在提示中命名文档和上下文来引用行动手册。 查看[生成和查看接触点](#step-3-generate-and-review-touchpoints)。
* **对话式销售助理** — 若要从行动手册中提取，请将该助理指向知识中心。 查看[对话式销售助理](#conversational-sales-assistant)。

## 对话式销售助理

对话式销售助理是一种聊天体验，您可以用自然语言提问，并根据销售情况获得答案。 助手利用了以下内容：

* 您的内部知识库，包括任何[知识中心](#knowledge-center)行动手册
* 来自已连接CRM的CRM信号
* [!DNL Marketo]活动和参与数据
* Web研究

使用助理在外联之前进行准备，例如，在会议之前构建客户定位。 要从已构建的行动手册中获取信息，请向知识中心的助理提出您的问题。 例如：`From the Knowledge Center, help me position our security solution for ABC Corp ahead of tomorrow's call.`

## 性能

**[!UICONTROL 性能]**&#x200B;部分显示您的出站运行情况，以便您查看哪些项目正在运行以及在何处进行调整。

### 电子邮件绩效

检查出站电子邮件的数量和有效性：

* 已发送的电子邮件
* 打开率
* 点击率
* 回复率

销售鉴定表确定不在办公室回复和退回及其相应状态，以便您能够将它们与潜在客户参与区分开来。

### 会议预订性能

会议预订状态卡片概述了已预订会议的位置。 筛选卡片以重点关注要审阅的会议和状态。

## 集成和CRM

借助集成，Sales Qualifier可连接到您的CRM，以便Account Qualification Agent (AQA)和出站工作流在Salesforce或Microsoft Dynamics 365中共享商机、帐户、联系人、活动和所有者的一致视图。 销售鉴定表读取CRM销售数据和活动以丰富洞察，它可以写回已记录的外联活动和选择退出状态。 它不会通过此连接修改您的CRM记录。

CRM连接、入站字段映射和活动同步由管理员在&#x200B;**[!UICONTROL 管理]** > **[!UICONTROL 管理员设置]** > **[!UICONTROL CRM连接]**&#x200B;下配置。 标准用户使用配置的CRM数据和过滤器，但无法更改这些设置。

### CRM MCP和嵌入式插件

销售限定符可通过多种方式与您的CRM配合使用：

* **通过CRM MCP查询CRM数据** - Account Qualification Agent通过CRM MCP查询实时CRM数据，以便答案和见解反映记录的当前状态。
* **嵌入式插件** — 嵌入式CRM插件直接在您的CRM中显示[!DNL Marketo Sales Insights] (MSI)核心洞察以及新的代理数据。 在插件中，只需单击一下即可将目标客户添加到Sales Qualifier。
* **活动同步回退** — 管理员启用&#x200B;**[!UICONTROL 活动同步]**&#x200B;后，外联活动会同步回CRM，以便销售代表可以在他们已使用的工具中看到销售限定词活动。

>[!IMPORTANT]
>
>访问&#x200B;**[!UICONTROL 管理员设置]**&#x200B;需要`Sales Qualifier`和`Sales Qualifier Admins`用户组的成员资格。

### CRM访问范围

Sales Qualifier读取它需要的CRM实体，并且只能写回定义的数据集。 读取的典型实体包括用户、联系人、所有者映射、潜在客户、客户、机会和活动。 回写仅限于已记录的外联活动和选择退出状态。 您的CRM管理员已在Salesforce或Dynamics中准备API访问权限。 然后，您可以连接Sales Qualifier，映射入站字段，并选择是否同步应用程序中的活动。

>[!NOTE]
>
>下面的凭据步骤描述了对CRM对象的读取权限。 如果启用活动同步或选择退出回写，请与您的CRM管理员合作，以授予CRM配置所需的相应写入权限。

### 在CRM中准备凭据

在连接Sales Qualifier之前，请与CRM管理员合作。 下面总结了通常在每个系统中创建的内容。

#### Microsoft Dynamics 365 (Dataverse / Power Platform)

1. 在Azure Active Directory中，注册应用程序（**[!UICONTROL 应用程序注册]**）。

   记下&#x200B;**客户端ID**&#x200B;和&#x200B;**租户ID**，并创建&#x200B;**客户端密钥**。

1. 在&#x200B;**[!UICONTROL Power Platform管理中心]**&#x200B;中，打开您的环境，然后转到&#x200B;**[!UICONTROL 设置]** > **[!UICONTROL 用户+权限]** > **[!UICONTROL 应用程序用户]**。

1. 创建链接到该Azure AD应用程序的应用程序用户。

1. 分配一个安全角色，该角色授予对实体Sales Qualifier需要的&#x200B;**读取**&#x200B;访问权限，例如潜在客户、联系人、客户、商机和活动。

   应用程序需要具有读取权限的安全角色才能读取数据。

在连接Dynamics时要提供的&#x200B;**信息：**

* 客户端 ID
* 客户端密码
* 租户 ID
* Dynamics实例URL（组织URL）

#### Salesforce

在Salesforce中，[创建启用了OAuth的外部客户端应用程序](https://help.salesforce.com/s/articleView?id=xcloud.create_a_local_external_client_app.htm&type=5)（或&#x200B;_连接的应用程序_），以及允许API访问标识和数据的范围，并遵循组织的安全标准。 集成用户必须对潜在客户、客户、联系人、任务、事件和商机等对象具有读取权限。 管理任务通常要求具有&#x200B;**[!UICONTROL 管理连接的应用程序]**（及其他权限）的用户在创建后查看使用者密钥和密钥。

>[!PREREQUISITES]
>
>要创建外部客户端应用程序，产品管理员应验证您是否已启用（从配置文件或权限集中）以下项：
>
>* 自定义应用程序
>* 查看设置和配置
>* 修改所有数据
>* 管理连接的应用程序（重要信息）
>
>   如果未启用&#x200B;_管理连接的应用程序_，则在创建外部客户端应用程序后，您将无法查看客户端ID和客户端密钥。

创建外部客户端应用程序时，启用OAuth并授予权限。 同时启用以下客户端凭据：

* 访问身份URL服务（id、个人资料、电子邮件、地址、电话）
* 通过API (api)管理用户数据
* 访问唯一用户标识符(openid)

创建应用程序后，请再次启用客户端凭据流并使用联系电子邮件作为用户名。  启用客户端凭据后，将用户配置为&#x200B;_运行身份_。

确保配置的用户对以下对象具有读取权限：

* 潜在客户
* 帐户
* 联系人
* 任务
* 事件
* 机会
* Opportuncontactroles
* OpportunityLineItems

在Sales Qualifier中连接Salesforce时要提供的&#x200B;**信息：**

* 客户端 ID（消费方密钥）
* 客户端密码（使用者密码）
* 回调URL（在连接的应用程序上配置）
* Salesforce实例URL

>[!IMPORTANT]
>
>不要通过电子邮件发送客户端密钥。 使用您组织批准的安全渠道与在Sales Qualifier中输入凭据的人员共享凭据。

### 连接到您的CRM

1. 登录到Sales Qualifier ，并确认选择了正确的沙盒或环境。

1. 在左侧导航中，展开&#x200B;**[!UICONTROL 管理]**，然后选择&#x200B;**[!UICONTROL 管理设置]**。

1. 选择&#x200B;**[!UICONTROL 集成]**&#x200B;下的&#x200B;**[!UICONTROL CRM连接]**。

   页面会显示Salesforce和Microsoft Dynamics的信息卡。 非活动连接显示&#x200B;**[!UICONTROL 连接]**。 配置的连接显示&#x200B;**[!UICONTROL 已连接]**&#x200B;和&#x200B;**[!UICONTROL 管理]**&#x200B;操作。

   ![管理员设置与Salesforce和Dynamics连接卡的CRM连接](./assets/integrations-crm-connections.png){width="800" zoomable="yes"}

1. 单击您使用的CRM的&#x200B;**[!UICONTROL 连接]**。

1. 输入您的CRM管理员提供的客户端ID、密钥、租户或回调值以及&#x200B;**实例URL**。

1. 成功连接后，确认卡片显示&#x200B;**[!UICONTROL 已连接]**。

### 实例URL准则

**实例URL**&#x200B;必须是您的CRM用于API和集成配置的环境基本URL，而不是仅限UI的主机名。

**Salesforce**

1. 从浏览器地址栏登录并记下您的组织&#x200B;_我的域_&#x200B;子域（`{{mydomain}}`值）。

1. 对于Sales Qualifier ，请使用规范形式： `https://{{mydomain}}.my.salesforce.com` 。

   请&#x200B;**不**&#x200B;使用`lightning.force.com` URL作为实例URL。

**Microsoft Dynamics 365**

1. 在浏览器中打开CRM，并从地址栏复制基本URL。

   其格式通常为`https://{{org}}.crm.dynamics.com`。

### 映射CRM字段（入站映射）

连接CRM后，为连接选择&#x200B;**[!UICONTROL 管理]**&#x200B;并打开&#x200B;**[!UICONTROL 入站映射]**。 入站映射控制销售限定符提取到应用程序中的CRM字段。

1. 选择对象组： **[!UICONTROL 联系人]**、**[!UICONTROL 潜在客户]**&#x200B;或&#x200B;**[!UICONTROL 帐户]**。
1. 选择&#x200B;**[!UICONTROL 添加节]**&#x200B;并输入节名称和可选说明。
1. 将CRM字段添加到部分。

   每个字段行显示其&#x200B;**[!UICONTROL 显示名称]**、**[!UICONTROL 字段名称]**&#x200B;和&#x200B;**[!UICONTROL 数据类型]**。

1. 为&#x200B;**[!UICONTROL 潜在客户]**&#x200B;列表中应作为筛选器提供的每个字段打开&#x200B;**[!UICONTROL 可筛选]**。
1. 预览并保存映射。

映射字段显示在Sales Qualifier的相应区域中：

* 潜在客户和联系人字段显示在潜在客户的&#x200B;**[!UICONTROL 人员]**&#x200B;选项卡上。
* 帐户字段显示在帐户视图中。
* 与机会相关的字段显示在客户体验的opportunity区域中。

### 配置活动同步（出站映射）

1. 从&#x200B;**[!UICONTROL CRM连接]**&#x200B;中，为连接的CRM选择&#x200B;**[!UICONTROL 管理]**。
1. 打开&#x200B;**[!UICONTROL 出站映射]**。
1. 打开&#x200B;**[!UICONTROL 活动同步]**&#x200B;以将销售限定符外展活动同步回CRM。

关闭活动同步后，销售限定词可以继续使用入站CRM数据，但不会将外联活动写回CRM。

### 配置全局电子邮件选择退出

1. 在左侧导航中，展开&#x200B;**[!UICONTROL 管理]**，然后选择&#x200B;**[!UICONTROL 管理设置]**。
1. 选择&#x200B;**[!UICONTROL 合规性]**&#x200B;下的&#x200B;**[!UICONTROL 电子邮件设置]**。
1. 打开每封电子邮件中的&#x200B;**[!UICONTROL 包含选择退出链接]**&#x200B;以将取消订阅页脚附加到出站电子邮件。
1. 在&#x200B;**[!UICONTROL 选择退出消息模板]**&#x200B;中，输入页脚文本。 包含将显示可点击取消订阅链接的`{{opt_out_link}}`令牌。
1. 保存设置。

当目标客户选择链接时，“销售鉴定表”将永久禁止目标客户接收更多电子邮件。 选择退出状态还会同步回连接的CRM。

### 参考：示例API参数

您的CRM团队可以使用这些示例来确认是否返回预期的潜在客户字段。

**动态（OData样式摘录）**

```text
$select=fullname,_ownerid_value,leadid,emailaddress1,jobtitle,statuscode,createdon,modifiedon,statecode
$filter=_ownerid_value eq '<crmUserId>' [AND additional filters]
$expand=Lead_ActivityPointers(...),parentaccountid(...)
$orderby=modifiedon desc
```

**Salesforce （SOQL摘录）**

```sql
SELECT Id, Salutation, FirstName, LastName, Name, Title, Company, Email,
  LeadSource, Status, OwnerId, LastModifiedDate, LastActivityDate, CreatedDate,
  (SELECT Id, Subject, ActivityDate, Status FROM Tasks ORDER BY ActivityDate DESC LIMIT 1),
  (SELECT Id, Subject, ActivityDateTime FROM Events ORDER BY ActivityDateTime DESC LIMIT 1)
FROM Lead
WHERE OwnerId = '<crmUserId>' AND IsDeleted = false
ORDER BY LastModifiedDate DESC
```

## 轮廓设置

配置文件设置指定与您本人相关的信息，包括个人详细信息、电子邮件、日历和聊天可用性。

### 电子邮件设置

在&#x200B;**[!UICONTROL 电子邮件设置]**&#x200B;选项卡中，设置您的电子邮件连接。

![电子邮件设置选项卡，显示电子邮件连接选项和电子邮件签名配置](assets/email-settings.png)

* **[!UICONTROL 电子邮件连接]** — 单击&#x200B;**[!UICONTROL 连接]**&#x200B;并遵循Microsoft登录过程。

* **[!UICONTROL 电子邮件签名]** — 配置在自动生成电子邮件中使用的电子邮件签名。 将您的[会议预订](#meeting-booking)链接添加到签名，以便潜在客户可以安排与您共度的时间。

### 日程表配置

在&#x200B;**[!UICONTROL 日历配置]**&#x200B;选项卡上，设置您的时区和可用性。

<!-- 
![Calendar settings tab showing time zone and availability options](assets/calendar-settings.png)
-->

* **[!UICONTROL 日历连接]** — 单击&#x200B;**[!UICONTROL 连接]**&#x200B;并按照Microsoft登录过程集成您的日历。

* **[!UICONTROL 会议确认电子邮件]** — 当客户确认与您进行会议时，他们将收到确认电子邮件作为回复。 使用这些设置定义电子邮件主题和正文。

* **[!UICONTROL 首选项]** — 设置默认会议长度和连续会议之间的时间。

如果断开日历：

* 有效禁用了活动的预订链接。
* 预订页面显示友好、暂时不可用的状态。
* 重新连接会保留设置。

### 日历可用性

您在销售限定词中的日历可用性基于以下两个输入：

* 已连接的工作日历（Outlook或Gmail）
* 您在&#x200B;_日历设置_&#x200B;中配置的可用性+时间段规则。

Sales Qualifier从连接的日历中读取忙/闲状态，而不是读取完整的事件内容，并将其与配置的规则一起使用来确定潜在客户可以查看哪些预订空位。

您可以配置：

* 按星期几的工作时间
* 每天多个数据块（例如：9:00-12:00和1:00-5:00）
* 您的时区
* 会议时长
* 会议前/会议后缓冲
* 最低通知
* 预订窗口

<!-- 
### Chat settings

In the **[!UICONTROL Chat settings]** tab, set your Timezone Live chat availability.

![Chat settings tab for configuring timezone and live chat availability](assets/chat-settings.png)

## Representative management

The _[!UICONTROL Representative management]_ panel displays the defined representatives and their calendar status.

## Meeting performance

This panel presents analytics around your completed meetings.
-->

<!--
 SHPHR-24341 remove section
## Set up the Chrome plugin

The AI Assistant Chrome plugin is available on the [Google Store](https://chromewebstore.google.com/detail/ai-assistant/hancbabllcmckehonngbdkhilocpdfji?authuser=0&hl=en).

When the plugin is installed in Chrome, the Adobe logo appears on the middle right when you are on an integrated site:

* Adobe web applications
* Salesforce
* Outlook
* Microsoft Dynamics and web applications
* Google applications 
-->
