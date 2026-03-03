---
title: 内容创作AI
description: 了解如何在 [!DNL Journey Optimizer B2B Edition]中使用创作AI创建个性化电子邮件和登陆页面，包括提示最佳实践。
feature: AI Assistant, Generative AI, Content
level: Beginner
topic: Artificial Intelligence
role: User
source-git-commit: d3238fa94f28c6d7e3fc0dce5b59fd70d8e74e34
workflow-type: tm+mt
source-wordcount: '2506'
ht-degree: 2%

---

# 内容创作AI {#generative-ai-content}

>[!CONTEXTUALHELP]
>id="ajo_b2b_ai-generation-settings"
>title="AI内容生成"
>abstract="在编制布局后，您可以在[!DNL Journey Optimizer B2B Edition]中使用创作AI工具来增强您的内容。 此功能根据您的描述性提示微调内容，从而简化个性化和内容改进的过程。"

>[!CONTEXTUALHELP]
>id="ajo_b2b_ai-generation-reference-context"
>title="参考内容"
>abstract="使用&#x200B;_引用内容_&#x200B;上载包含为[!DNL Journey Optimizer B2B Edition]中的创作AI提供附加上下文的内容的资源文件，或者选择以前上载的文件。 此选项可确保提供所有必要的材料，以提高所生成内容的质量和相关性。"

>[!CONTEXTUALHELP]
>id="ajo_b2b_ai-generation-start"
>title="Adobe创作AI术语"
>abstract="此功能的访问取决于您是否同意遵守 Adobe Experience Cloud 生成式 AI 用户指南。 检查此功能的任何输出结果是否准确，并确保它适合您的用例。"
>additional-url="https://www.adobe.com/cn/legal/licenses-terms/adobe-dx-gen-ai-user-guidelines.html" text="Adobe 生成式 AI 用户准则"

由Microsoft Azure OpenAI和Adobe Firefly提供支持的[!DNL Adobe Journey Optimizer B2B Edition]中内容的创作AI，为文本和图像提供主动内容变体建议。 通过试验不同的主标题和图像，优化您的内容影响。

使用创作AI功能在[!DNL Journey Optimizer B2B Edition]中创建内容，以利用Adobe的创作AI功能。 为电子邮件、短信消息、登陆页面等制作个性化的文本和可视化图表。 当您构建整个促销活动或只是优化特定资产时，这些功能可帮助您将内容无缝地与品牌准则保持一致，同时节省宝贵的时间。

<!--
Generate multiple variants and build an experiment to compare them. Leveraging Journey Optimizer Content Experiment, you can define multiple message treatments to measure which one performs best for your target audience. You can choose to vary the delivery content, or subject. The message audience is randomly allocated to each treatment to determine which one works best in terms of the specified metric. Learn more about Content Experiment in this section. -->

>[!IMPORTANT]
>
>若要在[!DNL Journey Optimizer B2B Edition]中访问这些功能，您必须具有&#x200B;_[!UICONTROL AI助手]_ > _[!UICONTROL 生成内容]_&#x200B;权限。 有关产品管理员如何授予功能权限的详细信息，请参阅[编辑产品权限的角色](../admin/user-management.md#edit-roles-for-product-permissions)。

以下资源类型支持用于生成内容的AI助手工具：

* [电子邮件](../content/ai-assistant-emails.md)
* [!BADGE Beta] [登陆页面](../content/ai-assistant-landing-pages.md)

## 一般准则和限制 {#general-guidelines-and-limitations}

生成AI功能的使用受[Adobe Experience Cloud生成AI用户指南](https://www.adobe.com/cn/legal/licenses-terms/adobe-dx-gen-ai-user-guidelines.html){target="_blank"}的约束。 由于Adobe承诺在使用创作AI工具创建媒体时保持透明度，因此Adobe在下载或导出包含[!DNL Firefly]生成的资源的任何内容或项目时会应用[内容凭据](https://helpx.adobe.com/firefly/web/get-started/learn-the-basics/content-credentials-overview.html){target="_blank"}。

查看这些对[!DNL Journey Optimizer B2B Edition]中的内容使用创作AI的一般准则：

* 为创作AI模型使用定义良好的提示来准确地解释。 您提供的营销目标或提示会严重影响所生成内容的质量。

* 上传内容引用文件以包含准确的品牌内内容。 否则，内容将基于公开可用的信息。 上传的内容可以采用以下文件格式：PDF、JPEG、PNG或ZIP（包含支持的文件格式）。 上传文件的最大大小为50MB。 较大的文件或大量的图像可以工作，但这会增加处理时间。

* 使用特定于品牌或自定义的模板创建电子邮件内容。 建议使用最多包含8至10个图像的电子邮件模板。

* 选择变体时，请确保使用向上缩略图、向下缩略图或标记图标报告任何有问题的输出。

## 创新型人工智能的即时最佳实践 {#generative-ai-prompting-guide}

>[!CONTEXTUALHELP]
>id="ajo_b2b_ai_content_prompt"
>title="快速引导"
>abstract="浏览[!DNL Journey Optimizer B2B Edition]文档，了解如何创建有效的提示，以生成高转化率的品牌内营销内容。"

本指南可帮助您构建请求、清晰地传达意图，并确保AI生成的消息符合您的品牌准则、受众需求和营销活动目标。

了解如何编写有效的提示，以使AI助手能够根据您的目标生成高质量、品牌化的营销内容。

### 使用CO-STAR框架 {#costar-framework}

要获得生成内容的最佳结果，请使用CO-STAR框架组织您的提示。 这种结构化的方法能让您清楚地了解自己所需的内容。

| 组件 | 它的含义 | 为什么这很重要 |
| --- | ---- | ------ |
| **C — 上下文** | 有关营销活动、产品或情况的背景 | 有助于理解大局 |
| **O — 目标** | 您的特定营销目标 | 推动内容应实现的目标 |
| **S — 样式** | 您希望如何通信 | 设置方法 |
| **T — 音调** | 情感风格和声音 | 塑造您的信息感受 |
| **A — 受众** | 您定位的受众 | 确保消息可与适当的人产生共鸣 |
| **R — 要求** | 特定限制或必备项 | 定义边界和关键元素 |

{style="table-layout:fixed"}

### 提示要点 {#key-takeaways}

<table style="table-layout: fixed; width: 100%; border: 0;">
<thead style="border: 0; background-color: #FFFFFF;">
<tr>
<th>Do</th>
<th>不要</th>
</tr>
</thead>
<tbody>
<tr style="border: 0;">
<td>
<ul><li>使用CO-STAR框架进行结构
<li>明确说明最新内容与现有内容
<li>通过特定的提取指南聚焦文档使用
<li>选择语调、策略和区域设置
<li>将营销目标与内容类型功能相匹配
<li>为A/B测试生成多个变体</ul>
</td>
<td>
<ul><li>在提示中要求进行结构更改、样式设置或图像编辑
<li>在提示中提及提示音/策略（如果选项中可用）
<li>使用模糊的目标，如_promote产品_
<li>请求条件元素选择
<li>期待通过提示进行布局修改</ul>
</td>
</tr>
</tbody>
</table>

### 提示中不支持该内容

>[!TIP]
>
>使用设计工具或[!DNL Adobe Express]进行可视化/图像修改。

以下请求&#x200B;**_不受支持_**，应通过其他工具进行处理：

<table style="table-layout: fixed; border: 0;">
<thead style="border: 0; background-color: #FFFFFF">
<tr>
<th><img src="../../assets/do-not-localize/check-box-red.svg" alt="红色划线">  电子邮件结构修改</th>
<th><img src="../../assets/do-not-localize/check-box-red.svg" alt="红色划线">  视觉样式更改</th>
<th><img src="../../assets/do-not-localize/check-box-red.svg" alt="红色划线">  图像编辑操作</th>
</tr>
</thead>
<tbody>
<tr style="border: 0;">
<td>
<ul>
<li>选择要更改的特定部分</li>
<li>删除或克隆元素</li>
<li>条件选择</li>
<li>添加或删除布局部分</li>
</ul>
</td>
<td>
<ul>
<li>文本格式（粗体、斜体、字体大小）</li>
<li>颜色修改</li>
<li>布局样式（边框、填充、边距）</li>
<li>视觉效果（阴影）</li>
</ul>
</td>
<td>
<ul>
<li>背景更改</li>
<li>添加文本叠加图或徽标</li>
<li>图像裁剪或调整大小</li>
<li>颜色调整</li>
<li>图像替换</li>
</ul>
</td>
</tr>
</tbody>
</table>

### 质量核对清单 {#quality-checklist}

在生成内容之前，请确保满足以下条件：

![绿色复选标记](../../assets/do-not-localize/check-box-green.svg){width="20"} **清除目标**：明确说明操作、产品/服务、值和上下文。

![绿色复选标记](../../assets/do-not-localize/check-box-green.svg){width="20"} **已定义目标受众**：指定人口统计、角色或区段。

![绿色复选标记](../../assets/do-not-localize/check-box-green.svg){width="20"} **内容类型对齐方式**：目标与所选渠道或格式匹配。

![绿色复选标记](../../assets/do-not-localize/check-box-green.svg){width="20"} **审阅选择**：选择了音调、策略和区域设置，请勿将其包含在提示中。

![绿色复选标记](../../assets/do-not-localize/check-box-green.svg){width="20"} **指定了文档焦点**：突出显示要引用的内容或部分。

![绿色复选标记](../../assets/do-not-localize/check-box-green.svg){width="20"} **已应用品牌**：已选择适当的品牌准则。

![绿色复选标记](../../assets/do-not-localize/check-box-green.svg){width="20"} **实际范围**：避免请求布局更改、样式或结构编辑。

### 有效的营销目标 {#marketing-objectives}

在制定营销目标时，请确保这些目标明确、可操作且可衡量。 避免使用Vague或泛型语句。

**良好目标示例：**

![绿色复选标记](../../assets/do-not-localize/check-box-green.svg){width="20"}“推动注册以免费试用新的AI支持的分析仪表板30天”

![绿色复选标记](../../assets/do-not-localize/check-box-green.svg){width="20"}“为3月15日举行的‘将云成本降低40%’的B2B网络研讨会创造商机”

![绿色复选标记](../../assets/do-not-localize/check-box-green.svg){width="20"}“促销高级订阅的限时25%折扣，截止到12月25日”

**要避免的示例：**

![红色划线](../../assets/do-not-localize/check-box-red.svg){width="20"}“促销产品”（太模糊）

![红十字会去掉](../../assets/do-not-localize/check-box-red.svg){width="20"} “让别人签署协议”（价值不明）

![红色划线](../../assets/do-not-localize/check-box-red.svg){width="20"}“关于新功能的电子邮件”（目的不足）

#### 构建目标

始终为生成相关内容提供上下文和价值主张。 使用以下公式帮助您编写有效的目标： **操作+产品/服务+值/收益+紧急情况/上下文**

**良好目标示例：**

![绿色复选标记](../../assets/do-not-localize/check-box-green.svg){width="20"} “鼓励下载新的移动应用程序，帮助用户通过个性化的环保推荐跟踪可持续生活习惯”

![绿色复选标记](../../assets/do-not-localize/check-box-green.svg){width="20"}“促进注册营销专业人员高级数据可视化技术独家研讨会”

![绿色复选标记](../../assets/do-not-localize/check-box-green.svg){width="20"} “提高产品发布活动的出席率，展示革命性的AI编写助手，每周可节省5小时以上的时间”

**要避免的示例：**

![红色交叉表](../../assets/do-not-localize/check-box-red.svg){width="20"}“宣布新的应用程序”（缺少值主张和上下文）

![红十字会](../../assets/do-not-localize/check-box-red.svg){width="20"}“让人员注册参加研讨会”（缺少有关受众和优势的具体说明）

![红色交叉表](../../assets/do-not-localize/check-box-red.svg){width="20"}“促销事件”（无明确的操作、值或紧急性）

#### 按渠道类型显示的提示示例 {#channel-type-practices}

<table style="table-layout: auto; border: 0;">
<thead>
<tr style="border: 0;background-color: #FFFFFF;">
<th>渠道</th>
<th>示例</th>
</tr>
</thead>
<tbody>
<tr>
<td><strong>电子邮件</strong></td>
<td>“通过展示三个具有详细ROI指标的客户成功案例来培养企业前景(Oracle：成本降低45%，Accenture：潜在客户增加200%，Microsoft：时间节省60%)。 面向拥有1000多名员工的公司的IT主管”</td>
</tr>
<tr>
<td><strong>登陆页面</strong></td>
<td>“通过《财富500强》的推荐和免费的安全审核，展示企业安全解决方案如何防止99.9%的网络攻击，从而将B2B访客转化为合格的潜在客户”</td>
</tr>
</tbody>
</table>

<!-- channels not yet supported
<tr>
<td><strong>SMS</strong></td>
<td>"Alert VIP customers about a 4-hour flash sale on premium electronics with 40% discount, limited to the first 100 customers"</td>
</tr>
<tr>
<td><strong>Push Notifications</strong></td>
<td>"Re-engage users who haven't opened the app in 7 days with personalized content recommendations based on their reading history"</td>
</tr> -->

<!-- Wait on more B2B specific examples

### Industry-specific approaches {#industry-approaches}

<table style="table-layout: fixed; border-collapse: collapse; border: 0;">
<thead>
<tr style="border: 0;background-color: #FFFFFF;">
<th>Industry</th>
<th>Example Prompt</th>
</tr>
</thead>
<tbody>
<tr>
<td><strong>B2B Technology</strong></td>
<td>"Demonstrate ROI and technical specifications while addressing security concerns for IT decision-makers evaluating our cloud infrastructure solution, emphasizing 99.9% uptime SLA, SOC 2 compliance, and 40% cost savings."</td>
</tr>
<tr>
<td><strong>E-commerce Retail</strong></td>
<td>"Create urgency around limited-stock holiday items while highlighting free shipping and easy returns for last-minute shoppers, emphasizing limited quantities (less than 50 remaining) and 24-hour shipping cutoff."</td>
</tr>
<tr>
<td><strong>Financial Services</strong></td>
<td>"Educate clients about investment portfolio diversification strategies while maintaining regulatory compliance, featuring certified financial advisor insights and risk disclaimers."</td>
</tr>
<tr>
<td><strong>Healthcare & Wellness</strong></td>
<td>"Promote preventive care benefits and annual health screenings while maintaining medical accuracy, featuring board-certified physician recommendations and patient privacy assurances."</td>
</tr>
<tr>
<td><strong>Education & Training</strong></td>
<td>"Emphasize career advancement outcomes and industry certifications while showcasing instructor expertise, highlighting 92% job placement rate and project-based curriculum."</td>
</tr>
<tr>
<td><strong>SaaS Platforms</strong></td>
<td>"Highlight time savings and automation benefits with specific metrics while addressing integration concerns, featuring average 25-hour weekly time savings and integration with 200+ popular tools."</td>
</tr>
</tbody>
</table>
 -->

### 新内容与修改现有内容 {#new-vs-modify}

明确指示您的请求是否涉及生成新内容或更新现有材料。 这种区分很重要，因为它指导人工智能选择适当的方法，并确保产生更准确和有益的结果。

#### 创建新内容

在启动营销活动、发布新解决方案或启动更新/刷新通信时应用此策略。 它可确保您的消息开始变得强大并与目标保持一致。

**如何提示** ➤创建新内容时，请专注于营销目标而不引用现有内容。

>[!BEGINSHADEBOX “示例”]

* **SaaS试用版**：“向小型企业所有者发布新的CRM软件，突出显示50%的时间节省、90%的销售机会鉴定提速，并提供包含个性化入门的30天免费试用版”
* **功能发布**：“宣布新的API集成功能，将企业客户的开发时间减少60%，面向技术决策者”
* **活动促销活动**：“推动关于‘2024年数字营销趋势’网络研讨会的注册，欢迎来自Google、Meta和Adobe的专家参加，重点提供可操作的见解和有限的名额（最多500个）”

>[!ENDSHADEBOX]

#### 修改现有内容

>[!TIP]
>
>对于精细、汇总或简化等标准修改，请选择&#x200B;**_优化_**，而不是编写自定义提示。

在需要更新、刷新或调整当前营销活动时，使用修改提示。 此方法支持增量改进，确保消息传送保持相关状态而不从头开始。

**如何提示** ➤修改现有内容时，请明确指定要更改的内容以及如何更改内容。

>[!BEGINSHADEBOX “示例”]

* **Campaign更新**：“修改项目启动电子邮件，将重点放在企业安全功能而不是一般的生产力优势上，并将目标定位为具有合规性认证的IT决策者”
* **受众透视**：“调整软件演示邀请，使其专门面向医疗保健，将通用示例替换为医疗保健用例和HIPAA合规性好处”
* **季节性更新**：“更新第4季度假期购物的第3季度促销活动，将焦点从返校更改为强调快速送货的假日礼品馈送”

>[!ENDSHADEBOX]

## 高级文本设置 {#text-settings}

除了使用清晰且格式正确的提示外，AI助手内容工具中的文本设置还包括可用于优化生成的输出的文本设置。

>[!TIP]
>
>在&#x200B;_[!UICONTROL 文本设置]_&#x200B;中使用&#x200B;_[!UICONTROL 通信策略]_&#x200B;和&#x200B;_[!UICONTROL 色调]_&#x200B;选项，而不是在提示中提及这些特性。

### 沟通策略类型

您的沟通策略决定了如何展示您的消息以最大限度地扩大影响。 不同的策略可以更好地用于不同的目标，无论您是要建立紧迫感、建立信任，还是要立即采取行动。 选择最符合您的营销活动目标和受众思维的策略。

| **策略** | **最适合** | **消息样式** | **示例** |
| ------------ | ------------ | ------------------- | ------------ |
| **紧急** | 对时间敏感的优惠、截止日期、立即行动 | 使用基于时间的语言产生即时压力 | <li>“立即行动：优惠将在午夜过期” <li>“在污点填满前立即注册” <li>“48小时闪促销售开始啦” |
| **FOMO（害怕丢失）** | 限量优惠、事件、独占访问 | 使用紧迫性、稀缺性和时间压力提示 | <li>“只剩下24小时了！ 有限公司现享40%优惠” <li>“最后机会：早鸟的定价明天就结束了” <li>“只剩下100个Beta测试版名额” |
| **社交校对** | 建立信任、口碑、受欢迎的产品 | 利用他人的经验和验证 | <li>“加入50,000多个满意的客户” <li>“行业专家给予4.9/5星的评分” <li>“受财富500强企业信任” |
| **稀缺** | 库存有限、独占发放、高需求物料 | 强调有限的可用性和排他性 | <li>“库存只剩下5只” <li>“限量版：提供100台” <li>“独家发行：先到先得” |
| **奖励** | 促销活动、奖励计划、特殊优惠 | 突出显示的实实在在的好处和回报 | <li>“首次订购享受20%优惠” <li>“这个周末能赚到两分钱” <li>“订单金额超过50美元的免运费” |
| **排他性** | Premium产品、VIP体验、仅限成员的选件 | 使用高级定位和特殊访问语言 | <li>“私人预览的独家邀请” <li>“高级会员资格为高级分析解锁” <li>“加入精选的已使用我们的财富500强公司” |
| **Gamification** | 参与活动、忠诚度计划、交互式内容 | 使用游戏机制和成就语言 | <li>“解锁您的下一个奖励级别” <li>“获得徽章的完整挑战” <li>“登上独家奖项的排行榜” |
| **信息** | 教育、研究、复杂产品、思想领导力 | 使用事实、数据、见解和解释 | <li>“分析10,000多种交互得到的5个见解” <li>“新研究揭示了3种突破性方法” <li>“在营销中实施AI的完整指南” |
| **教育和见解** | 学习内容、行业趋势、最佳实践 | 提供宝贵的知识和可操作的外包 | <li>“使用专家指南学习高级技术” <li>“探索顶级营销人员使用的7种策略” <li>“了解如何通过5个步骤优化您的工作流” |

### 设定正确的语调 {#tone}

音调决定受众如何感知和响应您的消息。 始终选择与您的品牌声音和个人资料历程阶段一致的语调。

查看可用的色调选项，包括每种颜色何时效果最佳以及适合每种样式的内容示例。

| 色调 | 最适合 | 内容示例 |
| ---- | ----- | ----- |
| 专业 | B2B通信、正式公告 | “我们很高兴地宣布我们的战略伙伴关系……” |
| 同理心 | 客户支持，敏感主题 | “我们理解这个问题对你来说一定有多么令人沮丧……” |
| 幽默 | 参与营销活动，突出显示内容 | “警告：可能会导致生产率大幅提高！” |
| 令人兴奋 | 产品发布、事件促销 | “这是你一直在等待的时刻！” |
| 励志 | 激励活动，品牌目的 | “我们携手合作，就能改变世界……” |
| 有说服力 | 促销活动、转化 | “不要错过这个有限的时间…… |
| 友好 | 客户参与，欢迎消息 | “很高兴你跟我们一起来！” |
| 正式 | 法律通讯、正式通知 | “这是以下更改的通知……” |
| 抱歉 | 服务恢复，问题解决 | “Bodea对由此造成的不便深表歉意……” |
| 自信 | 领导力内容，权威消息 | “这是你现在需要做的……” |
| storytelling | 品牌叙事，情感联系 | “这一切都始于一个简单的问题……” |
| 对话 | 培养活动，建立关系 | “让我们谈谈这个计划能如何帮助你……” |

## 优化的参考内容 {#reference-content}

>[!TIP]
>
>如果您已通过&#x200B;**[!UICONTROL 引用内容]**&#x200B;菜单上传资产，则无需在提示中引用该资产。 系统会自动使用任何选定的文档。

参考内容文件提供了真实的信息，通过特定、准确的详细信息丰富了您生成的内容。 上传文档（如产品小册子或白皮书）时，请更改提示以包括哪些部件具有焦点：

* **不要使用** _“使用产品手册”_ **您应该使用** _“专注于高级安全功能和合规性认证，特别是SOC 2合规性和数据加密”_

* **而不是** _“参考案例研究”_ **您应该使用** _“突出医疗保健客户的ROI结果，特别是地区医疗中心的40%成本降低”_

* **您应该使用** _“强调API集成功能和开发人员优势，重点是REST API端点和99.9%的正常运行时间SLA”_，而不是&#x200B;**_“包括技术详细信息”_**

### 内容细化

生成内容后，使用&#x200B;**_[!UICONTROL 优化]_**&#x200B;功能通过以下选项对其进行迭代和增强：

* **[!UICONTROL 精心设计]** - AI助手可以帮助您展开特定主题，提供其他详细信息以便更好地了解和参与。

* **[!UICONTROL 摘要]** — 过长的信息可能会使页面查看者过载。 使用AI Assistant将关键点浓缩为清晰、简洁的摘要，以吸引注意并鼓励他们进一步阅读。

* **[!UICONTROL 重写]** — 重写邮件并保留其含义。 此选项可帮助您在不更改核心消息的情况下生成替代措辞、改善流量或调整词语。

* **[!UICONTROL 使用更简单的语言]** — 简化语言，确保更广受众的清晰度和可访问性。

* **[!UICONTROL 翻译]** — 将文本翻译成其他语言。 （目前，英语是唯一受支持的语言。）

* **[!UICONTROL 更改音调]** — 调整消息音调以符合您的沟通风格，例如，使消息更友好、更专业、更紧急或更具启发性。

* **[!UICONTROL 更改沟通策略]** — 根据您的目标修改消息传送方式，如创建紧迫感或强调令人兴奋的吸引力。
