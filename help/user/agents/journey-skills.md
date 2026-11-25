---
title: B2B的历程技能
description: 了解如何准备历程简报、查看验证的草稿图形、配置保存的草稿，以及通过同事聊天检查帐户和人员历程。
feature: Account Journeys, Person Journeys, Agentic AI
role: User
exl-id: 5d2945ab-4f6c-4d9c-b0a1-1a93dc1849f3
autotag-review: '2026-06-05T16:42:46.785Z'
TQID: 'https://experienceleague.adobe.com/SgjavYf2Tp5yO8s3f0DQexRCUILQRsD5bM6UwmbcgyE'
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
    internal-label: Journey Optimizer B2B Edition
feature_v2:
  - id: a4b836d9-ffdd-4df3-a62a-f78b830cf059
    internal-label: Journeys
  - id: bef5003b-cad2-4f40-bdb2-a80426d52ef5
    internal-label: AI Assistant
subfeature_v2:
  - id: ff10f619-348f-47e3-99bf-3ce4c817cf2c
    internal-label: Agentic AI
  - id: c31bc6c7-76bc-467b-80c0-7315a4e3f6be
    internal-label: Account Journeys
  - id: ba367494-9862-4596-bd6f-299c7e10a46b
    internal-label: Person Journeys
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
    internal-label: Metadata
  - id: bbbea26f-9621-49eb-9ab8-e06fb3bbce8c
    internal-label: Artificial intelligence
  - id: d00e9f03-e50b-4162-b143-0c0817c937c2
    internal-label: Customer journeys
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
    internal-label: Insights
source-git-commit: 876251dd1b69fc768c790daf0b9b1482015d69af
workflow-type: tm+mt
source-wordcount: '788'
ht-degree: 0%
---
# B2B的历程技能

使用[!DNL Adobe CX Enterprise Coworker]聊天在[!DNL Adobe Journey Optimizer B2B Edition]中查找、创建和配置历程。 从简短的草稿创建已验证的草稿，更改已保存的草稿图形和重入设置，以及配置未配置的节点。 历程更改适用于已保存的草稿，而不是活动的历程。

有关查找、创建和规则技能标识符及其支持的操作，请参阅[同事历程技能参考](./coworker-overview.md#skills)。 本文提供了简要的准备指导和旅程可观察性示例：

* [历程创建指南](#journey-creation-skills)：在创建之前准备摘要并查看草稿。
* [历程可观察性指南](#journey-observability-skills)：询问有关帐户和人员如何在活动历程中移动的问题。

有关打开应用和开始对话的说明，请使用[同事界面指南](https://experienceleague.adobe.com/zh-hans/docs/coworker/content/chat/ui-guide){target="_blank"}。

## 历程创建技能 {#journey-creation-skills}

历程创建技能将简短转化为经过验证的帐户或人员历程图。 它会将已命名受众解析为其[!DNL Adobe Experience Platform]受众ID，并在创建草稿之前预览图形。

在[!DNL Coworker]创建草稿之前，您必须明确批准预览。 创建技能不会发现受众、配置节点规则、创作消息复制、发布或删除历程。

### 准备摘要 {#basic-usage}

用自然语言描述您想要的草稿历程。 包括以下详细信息：

* 历程类型：帐户或人员。
* 现有受众：要使用的受众的名称或ID。
* 历程流：要包括的操作、等待和分支。
* 重新输入设置：帐户或人员是否可以重新输入以及何时可以重新输入。

包括促销活动简介中的相关详细信息，以便[!DNL Coworker]能够解释目标。 如果预览与您的预期流程不匹配，请优化请求。

同事聊天中的![历程创建提示。](./assets/coworker-chat-b2b-journey-prompt.png){width="800" zoomable="yes"}

### 查看并创建草稿 {#end-to-end-b2b-journey-creation}

在验证的预览中查看历程类型、已解析的受众、节点和路径。 仅当图形与您的摘要匹配时批准创建。

批准后，[!DNL Coworker]将创建草稿并返回其链接。 使用跟进请求通过“规则”技能配置其未配置的节点。 在应用程序中添加邮件副本，然后完成[历程审阅和发布步骤](../journeys/create-publish-journey.md)。

有关完整示例，请参阅[构建帐户历程](./coworker-overview.md#build-account-journey)。

### 多阶段历程

对于包含多个阶段的历程，请在简介中描述每个阶段的操作、等待和分支。 将图形结构与您在创建草稿后配置的规则和报文副本区分开来。

要修订已保存的草稿，请请求图形或通过创建技能重新输入更改。 使用规则技能在未配置的节点上拆分条件、操作、事件和动态列表受众。

## 历程可观察性技能 {#journey-observability-skills}

历程可观察性技能让您能够询问关于帐户和人员如何在B2B历程中移动的自然语言问题，而无需挖掘历程地图、日志或仪表板。 它们涵盖两个主要领域：旅程进展和数据同步可观察性。

![在[!DNL CX Coworker]](./assets/journey-observability-prompt-response.png){width="800" zoomable="yes"}中历程可观察性提示和响应

### 帐户级别历程insight

通过提出以下问题，跟踪特定帐户如何在历程中流动：

* “给我有关Bodea Cloud帐户的基本信息。”
* “告诉我Northstar Services客户如何经历了ABM培养战略的历程。”
* “Contoso LLC客户何时开始此历程？”

### 分割路径推理和计数

了解为什么使用分支以及遵循每个路径的人员或帐户数量：

* “为什么帐户QiDemoAccount24转到位于拆分节点c764a9的美国加利福尼亚小型技术路径？”
* “告诉我拆分节点node-459c7c中每条路径的人员数。”
* “让我看看圣何塞帐户8的路径上的人。”

历程可观察性技能可分析拆分逻辑、帐户属性和活动，以解释路由选择决策和按路径返回计数或人员列表。

### 人员级别的历程结果

在一个帐户内或整个历程中分析单个结果 — 对于购买群体分析和跟踪决策者与影响者的行为特别有用：

* “让我计算一下Bodea下一次Web参与之旅的每个拆分路径中的人员数量。”
* “列出隐藏跳过路径中的人员。”
* “让我看看此帐户在圣地亚哥位置路径的人员。”

### 历程生命周期和时间

检索历程或特定帐户的关键时间戳：

* “这段旅程什么时候上线的？”
* “第一个帐户何时进入此历程？”
* “QiDemoAccount50帐户何时开始此历程？”

### 外部受众和激活可见性

对于推送到外部渠道（如LinkedIn）的历程，您可以检查激活状态：

* “bsmith@acme.com是否位于外部受众中？”
* “列出通过ObservabilityExtAudience01激活到LinkedIn的所有人员。”

### 数据同步和管道可观察性

历程可观察性技能还可以提供数据同步运行状况信息，帮助排除客户或商机为什么没有包含在历程中的问题：

* 外部受众导出作业指标和状态
* 批量分段计划和完成时间
* 购买团体维护计划
* 作业管理器统计信息（已完成/失败）