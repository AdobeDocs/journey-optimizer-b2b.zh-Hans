---
title: 销售限定词
description: 通过Sales Qualifier自动化B2B潜在客户鉴定和推广。 它为BDR提供AI支持的研究、电子邮件起草、CRM集成和参与计划。
feature: AI Assistant, Sales Insights, Account Journeys
role: User
source-git-commit: 38c4d68a9c21ca4d6b5f55d59a31becbf73642e7
workflow-type: tm+mt
source-wordcount: '1325'
ht-degree: 1%

---


# 销售限定词

>[!NOTE]
>
>此功能当前处于“有限可用”状态，并非对所有用户都可用。

Sales Qualifier是Adobe Journey Optimizer B2B edition的AI驱动附加应用程序，它包含Account Qualification Agent，旨在简化业务开发代表(BDR)的工作流。 Sales Qualifier跨渠道自动执行潜在客户鉴别、外联和买方参与工作流程。 它减少了手动BDR负载，加快了企业B2B公司的管道速度。
使用浏览器和电子邮件插件直接在CRM或Outlook中访问商业智能。

## 演示视频

以下视频简要演示了Sales Qualifier和Account Qualification Agent。

>[!VIDEO](https://video.tv.adobe.com/v/3476571?captions=chi_hans)

销售限定符包含在[!UICONTROL Journey Optimizer B2B edition]中，但它是Experience Platform Experience Cloud中的单独应用程序。

![销售鉴定表仪表板自动执行企业B2B的BDR潜在客户鉴定和推广](assets/home-screen.png)

## Account Qualification 代理

Account Qualification Agent (AQA)是Sales Qualifier的核心。 AQA使用人工智能读取您的帐户，并确定哪些帐户已准备好执行下一步。 它有助于研究、电子邮件草稿和CRM更新。

![AI支持的Account Qualification Agent仪表板，用于销售前景和客户研究](assets/acc-qualification-agent.png)

* **潜在客户研究**

  使用自动检索和显示关键潜在客户信息（如职务、最近工作、购买组成员资格）来进行潜在客户研究，以在几秒钟内提供完整的概况。

* **帐户研究**

  使用自动检索和显示有关潜在客户组织的详细信息来执行客户调查。 此信息包括公司重要信息、最新新闻、战略优先顺序以及最受关注的会员。

* **草稿电子邮件**

  通过综合来自潜在客户和客户洞察的研究来生成电子邮件草稿，以根据BDR的目标生成相关的个性化电子邮件内容。

* **参与计划电子邮件**

  创建针对BDR定义的外联节奏的每个步骤进行个性化的参与计划电子邮件草稿，确保整个序列都是个性化的。

### 基本用法

Adobe AI代理使用&#x200B;_自然语言查询_，这意味着他们在文本提示中使用与您与某人交谈时所用的语言相同的语言。 你越详细，结果就越好。

使用自然语言，您可以要求代理：

* `Show me my assigned leads with no engagement yet`
* `Show me all my leads that are not part of any autonomous engagement`
* `Give me a detailed summary on Acme company, including their buying group, recent intent signals, and our past engagement.`

您可以立即了解哪些客户和潜在客户最活跃并显示最高的意图，这样您可以将精力集中到最具影响力的地方。

通过优化提示以获取所需结果来循环访问您的历程。 例如：

* 从盈利电话或报告等上下文中起草后续电子邮件。 最多120字。 主题行：引人入胜，包含关键主题。 简介：用上下文源中的直接引号挂接。 正文：连接到棘手问题和价值主张。 CTA：建议进行简短的呼叫以进一步探索。

* 这封电子邮件的目的是展开对话，建立信誉。 起草一封有120个字的电子邮件，其语气具有咨询性和同理心。 请务必避免过于熟悉或过于熟悉的销售方式，不要使用“希望您一切顺利”、“登记使用”或“请”等词语。

## 潜在客户

此窗口列出了您有权访问的所有潜在客户。 它可快速检查各项指标，如商机状态和上次活动。

![显示潜在客户管理的潜在客户状态和最后一个活动的潜在客户表](assets/prospects.png)

单击&#x200B;_筛选器_ ![筛选器图标](../../assets/do-not-localize/icon_filter-outline.svg)图标可按潜在客户状态筛选显示的列表。

## 参与计划

此窗口提供有关任何已定义的参与计划的详细信息。

![显示计划详细信息、所选潜在客户和计划设置的参与计划仪表板](assets/engagement-plans.png)

要制定新的参与计划，请单击&#x200B;**[!UICONTROL 创建参与计划]**。

1. 在&#x200B;_详细信息_&#x200B;阶段，提供名称和可选描述。 单击&#x200B;**[!UICONTROL 保存并继续]**。
1. 在&#x200B;_选择潜在客户_&#x200B;阶段中，选择应属于此计划的潜在客户。
1. 在&#x200B;_定义节奏_&#x200B;阶段，设置计划的参数。
1. 在&#x200B;_预览_&#x200B;阶段中，确保一切按预期运行。

## 电子邮件发件箱

电子邮件发件箱面板列出了您发送的所有自动电子邮件。

## 会议预约

此面板显示通过自动化设置的所有会议。

## 聊天收件箱

此面板显示所有聊天线程。

![显示聊天会话的面板，其中包含联系人和会话摘要，以实现销售自动化](assets/chat-inbox.png)

您可以与客户进行交互，并查看联系人和跟帖的摘要，以便快速了解您在跟帖中的位置。

## 集成

通过集成，销售限定词可利用CRM和其他数据源来丰富客户配置文件并利用销售活动：

* 与您的电子邮件收件箱集成，以跟踪相关的传入电子邮件并帮助生成回复。
* 读取和更新CRM数据，例如Salesforce或Microsoft®Dynamics、ZoomInfo或BuildWith。

![与Microsoft Outlook的Sales Qualifier集成显示电子邮件和联系人摘要](assets/outlook.png)

### 设置新集成

要开始新的集成，请单击右上方的&#x200B;**[!UICONTROL 创建集成]**。

![显示URL、HTTP方法、标头和身份验证选项的集成设置表单](assets/integration-details.png)

定义集成的URL，并建立要发送的有效负载：

1. 为集成提供唯一名称和描述（可选）。
1. 将URL字段设置为集成站点的集成身份验证端点。
1. 在路径参数中，设置HTTP方法。
1. 在标头参数中，设置需要发送的任何HTTP标头。 通常，发送的JSON对象需要内容类型标头。
1. 在查询参数中，建立任何所需的参数。
1. 在身份验证下，设置集成站点的登录信息。

   * None
   * OAuth 2.0
   * API密钥
   * 基本身份验证

1. 在&#x200B;**[!UICONTROL 有效负载配置]**&#x200B;分区中设置限制和缓存值。
   * 单击铅笔图标。
   * 在&#x200B;_粘贴有效负载_&#x200B;对话框中，粘贴或输入您的JSON有效负载对象。

      * **[!UICONTROL 请求有效负载]** — 包含要发送到集成站点的数据的JSON对象。
      * **[!UICONTROL 响应有效负载]** — 您希望返回的数据结构。

1. 单击&#x200B;**[!UICONTROL 测试连接]**&#x200B;以确保您的设置正确。

当连接设置有效时，单击&#x200B;**[!UICONTROL 另存为草稿]**。

当您返回主&#x200B;_[!UICONTROL 集成]_&#x200B;表时，请选择该集成，然后单击&#x200B;**[!UICONTROL 激活]**&#x200B;以启用该集成。 如果您尚未准备好激活它，请单击&#x200B;**[!UICONTROL 另存为草稿]**。

#### 管理访问权限

您可以管理对用户的访问以及与不同用户组共享的数据类型。

单击&#x200B;**[!UICONTROL 管理访问权限]**&#x200B;以打开&#x200B;_[!UICONTROL 管理访问权限]_&#x200B;对话框。

此对话框列出了为您的组织建立的所有标签。 选择要应用于此集成的标签。

如果需要新标签，请单击&#x200B;**[!UICONTROL 创建标签]**，然后输入标签信息：

* 名称
* 友好名称
* 描述

## 代表性设置

代表设置指定与您本人相关的信息，包括个人详细信息、电子邮件和日历设置以及聊天可用性。

### 详细信息

**[!UICONTROL 详细信息]**&#x200B;选项卡是您输入自己相关信息的位置：

![显示代表个人信息、电子邮件和聊天可用性设置的“详细信息”选项卡](assets/details.png)

### 电子邮件设置

在&#x200B;**[!UICONTROL 电子邮件设置]**&#x200B;选项卡中，设置您的电子邮件连接。

![电子邮件设置选项卡，显示电子邮件连接选项和电子邮件签名配置](assets/email-settings.png)

* **[!UICONTROL 电子邮件连接]** — 单击&#x200B;**[!UICONTROL 连接]**&#x200B;并遵循Microsoft登录过程。

* **[!UICONTROL 电子邮件签名]** — 配置在自动生成电子邮件中使用的电子邮件签名。

### 日历设置

在&#x200B;**[!UICONTROL 日历设置]**&#x200B;选项卡中，设置您的时区和可用性。

![显示时区和可用性选项的“日历设置”选项卡](assets/calendar-settings.png)

* **[!UICONTROL 日历连接]** — 单击&#x200B;**[!UICONTROL 连接]**&#x200B;并按照Microsoft登录过程集成您的日历。

* **[!UICONTROL 会议确认电子邮件]** — 当客户确认与您进行会议时，他们将收到确认电子邮件作为回复。 使用这些设置定义电子邮件主题和正文。

* **[!UICONTROL 首选项]** — 设置您的默认会议时长，以及您希望在连续会议之间间隔的时间。

### 聊天设置

在&#x200B;**[!UICONTROL 聊天设置]**&#x200B;选项卡中，设置您的时区实时聊天可用性。

![用于配置时区和实时聊天可用性的“聊天设置”选项卡](assets/chat-settings.png)

## 代表管理

_[!UICONTROL 代表管理]_&#x200B;面板显示定义的代表及其日历状态。

## 会议性能

此面板提供有关已完成会议的分析。

<!-- SHPHR-24341 remove section 
## Set up the Chrome plugin

The AI Assistant Chrome plugin is available on the [Google Store](https://chromewebstore.google.com/detail/ai-assistant/hancbabllcmckehonngbdkhilocpdfji?authuser=0&hl=en).

When the plugin is installed in Chrome, the Adobe logo appears on the middle right when you are on an integrated site:

* Adobe web applications
* Salesforce
* Outlook
* Microsoft Dynamics and web applications
* Google applications -->

## 编辑左侧导航栏

在应用程序的左下方，单击&#x200B;**[!UICONTROL 编辑]**&#x200B;以控制在导航中可见的图标。 您还可以根据需要拖放它们以重新排序。
