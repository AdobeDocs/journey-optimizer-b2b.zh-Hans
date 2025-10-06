---
title: Audience Agent B2B
description: 历程OptimizerB2B版本中的Audience Agent B2B使用意图分析和角色映射来创建购买组并加快B2B营销工作流程。
feature: Audiences, AI Assistant
role: User
source-git-commit: 7f1c1533c226a2626978ada221c7026bc3d1432b
workflow-type: tm+mt
source-wordcount: '417'
ht-degree: 0%

---

# Audience Agent B2B

Audience Agent B2B由[Adobe Experience Platform Agent Orchestrator](https://experienceleague.adobe.com/zh-hans/docs/experience-cloud-ai/experience-cloud-ai/agents/agent-orchestrator)提供支持，在Journey Optimizer B2B edition中可用。 使用此代理提高了探索和扩展受众的效率和有效性，加快了购买组创建以及历程激活的无缝工作流：

* **_按意图排列目标受众的优先级_** — 根据各种受众的产品意图推断角色并简化活动计划，从而减少验证受众所花费的时间。

* **_利用AI检测购买组_** — 使用AI、结构化、非结构化数据和统一的第一方数据来简化购买组的发现和创建。

处于全页模式的![Audience Agent B2B](./assets/audience-agent-full.png){width="700" zoomable="yes"}

## Audience Agent功能

| 面积 | 作用 | 商业价值 |
| ---- | ------------ | -------------- |
| 目的分析 | <li> 测量特定产品的帐户意图强度（例如低、中和高）。 <li>比较一段时间的产品兴趣趋势（例如过去&#x200B;_n_&#x200B;天排名最前的产品）。 <li>识别积极显示对特定产品感兴趣的客户。 <li>将帐户活动与角色覆盖相结合的表面参与模式。 | <li>帮助团队在适当的时间将精力集中在适当的客户上。 <li>通过优先处理具有真实购买信号的帐户，提高管道质量。 <li>在竞争对手采取行动之前实现主动参与。 |
| 角色映射 | <li>按产品意图检测和排名最前的角色。 <li>识别购买一个或多个产品所涉及的角色。 <li>合理地将角色映射到职能角色（冠军、决策者、影响者等）。 <li>验证给定人员被视为冠军的原因。 | <li>确保销售能够吸引真正的决策者和影响者。 <li>减少在影响较小的联系人上浪费精力。 <li>通过使推广与买方力量动态保持一致，提高赢率。 |
| 购买团体评估 | <li>评估购买组规模（例如，拥有n个以上成员的组）。 <li>衡量跨帐户的角色覆盖范围（例如，x%以下）。 <li>跟踪购买小组内的角色分配和覆盖缺口。 <li>突出显示在最近交易中表现出色客户的客户。 | <li>揭示可能会阻碍交易的覆盖缺口。 <li>通过确保完全角色表示来加强多线程策略。 <li>通过组级别的参与洞察来改进交易运行状况跟踪。 |

## 提示示例

这些提示示例演示了可以使用代理的一些方法：

* 显示趋势窗口：针对每个产品的帐户产品意向的最早和最新更新。
* 对于`<product>`，列出具有产品意向和得分的购买组。
* 对于`<product>`，列出角色及其机会量度（获胜率、会员资格率、计数）。
* 对于`<industry>`中的帐户，`<product>`的平均帐户角色覆盖率是多少？
* 哪些客户对任何产品的意图都不高，但仍存在开放机会（值得培养）？
* 哪些帐户本周为`<account_name>`添加了新意图信号？
