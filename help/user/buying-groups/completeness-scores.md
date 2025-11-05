---
title: 购买组的完整性分数
description: 在Journey Optimizer B2B edition中使用基于角色的阈值、可自定义的成员要求和完整性设置来计算购买组完整性分数。
feature: Buying Groups
role: User
source-git-commit: 1ebc27a709e1b82029c22950897505f3945a507f
workflow-type: tm+mt
source-wordcount: '884'
ht-degree: 3%

---


# 完整性分数 {#completeness-scores}

>[!CONTEXTUALHELP]
>id="ajo-b2b_buying_group_completeness_score"
>title="完整性评分"
>abstract="完整性得分反映购买群体成员资格与随时待售购买群体的匹配程度。"

完整性得分是一个百分比，它指明了购买组在其定义的角色中填充所需成员的程度。 这些得分基于您在角色模板中配置的角色成员阈值以及分配给购买组中每个角色的实际成员数。 由此得到的分数可帮助营销人员评估销售准备情况，并找出购买群体构成方面的差距。 当购买组成员资格发生变化时，会自动计算得分。

![购买群组完整性分数](./assets/buying-group-details-page-completeness-scores.png){width="800" zoomable="yes"}

完整性得分有两种类型：

* **购买群组完整性分数** — 购买群组完整性分数是一个介于0%到100%之间的百分比，表示购买群组的整体完整性（基于角色级别完整性计算）。

  购买群组完整性分数显示在[购买群组详细信息](./buying-group-details.md)页面中。 此得分提供了购买组是否有销售参与所必需的利益相关者的概览。

* **角色完整性分数** — 角色完整性分数是购买组中每个角色的百分比，基于分配给该角色的成员数。

  当您编辑角色并调整完整性设置时，每个角色的角色完整性得分会显示在购买组详细信息页面中。 这些分数可帮助您确定哪些特定角色需要额外的成员才能达到销售就绪阈值。

  详细信息页面显示前两个角色完整性分数，并带有用于任何其他角色的n_+链接。 单击链接可查看其他角色完整性分数。

完整性得分反映购买组成员资格的当前状态，并在添加或删除成员时自动更新。 显示的分数显示为全部百分比（例如，66.67%的分数显示为67%）。

## 评估销售就绪性

Adobe Journey Optimizer B2B edition为营销人员提供了确保购买群组与真实决策流程一致的工具。 您可以使用可自定义的角色成员阈值来定义完整的购买组，这些阈值反映了贵组织的销售方法。 通过为每个角色设置最低和最高成员要求，您可以为构成销售就绪采购组的内容建立明确的标准。

购买群体完整度得分为本集团提供准确的销售准备程度衡量。 例如，要完成特定解决方案的opportunity ，您可能需要至少两位决策者、一位影响者和一位实践者。 完整性得分计算考虑了每个特定于角色的要求，提供了购买组整体准备情况的视图。

## 衡量历程有效性

购买群体完整性作为历程有效性的关键绩效指标(KPI)。 特定历程的目标可能是将购买组的完整性提高一定百分比，或者在触发销售就绪警报之前达到最低阈值。

在大型企业中，您可以为每个角色确定一个人员。 但是，该人员可能不是正确的销售联系人，或者您可能需要多个关键角色的联系人。 例如，一家大型组织可能有多位信息技术(IT)决策者，分布在不同部门或业务部门。 对于复杂的企业销售，确定一个决策者可能还不够。

在分析当前购买组的完整性之后，您可以调整角色模板中每个角色的所需联系人数。 这些调整允许您根据实际模式和销售结果调整购买组策略。

<!-- ## Analyze audiences for journey optimization

Marketers can view the starting buying group completeness score of target account audiences to find the best performance indicators for a solution. This visibility enables marketers to:

* Determine if they need to adjust the completeness score requirements for each role to make journeys more effective.
* Identify which buying groups are closest to sales-ready status and prioritize them for acceleration campaigns.
* Segment buying groups by completeness score ranges and create tailored nurture strategies for different maturity levels.

>[!BEGINSHADEBOX]

The buying group completeness score is available to use for filtering in [journey split-path-by-account nodes](../journeys/split-merge-paths-nodes.md#account-path-filters) and for audience segmentation. Role completeness can be used to create personalized content that addresses specific gaps in buying group composition.

>[!ENDSHADEBOX] -->

## 角色完整性计算 {#role-completeness-calculation}

>[!CONTEXTUALHELP]
>id="ajo-b2b_buying_group_role_completeness_calculation"
>title="角色完整性计算"
>abstract="角色完整性得分根据分配给角色的成员数计算为一个百分比。"

Journey Optimizer B2B edition按百分比计算每个购买团体角色的完整性分数。 根据分配给角色的成员数量来计算此分数，而完成任务所需的成员数量是角色模板[中的](./buying-groups-role-templates.md#change-the-completeness-score-settings)数量。

角色完整性计算是介于零和指定阈值（需要成员）之间的线性百分比：

* 如果分配的成员数为&#x200B;**零**，则角色完整性为&#x200B;**0%**。
* 如果分配的成员数等于或大于阈值&#x200B;**，则角色完整性为** 100%**。**
* 如果分配的成员数介于1和阈值&#x200B;**之间**，则按比例计算完整性。

### 角色完整性公式

使用以下公式计算角色完整性百分比：

```text
Role Completeness % = ((Assigned Members - Threshold) / (Threshold)) × 100
```

其中：

* `Assigned Members` =角色中的当前成员数
* `Threshold` =在角色模板中设置成员所需的值

### 角色完整性示例

以下示例说明了使用不同阈值配置的角色完整性计算：

| 角色 | 必需的成员 | 已分配的成员 | 计算 | 角色完整性 |
|------|------------------|------------------|-------------|-------------------|
| 决策者 | 3 | 0 | None | 0% |
|  |  | 1 | 1/3 × 100 | 33% |
|  |  | 2 | 2/3 × 100 | 66% |
|  |  | 3 | 在阈值 | 100% |
|  |  | 4 | 高于阈值 | 100% |
| 影响者 | 5 | 0 | None | 0% |
|  |   | 1 | 1/5 × 100 | 20% |
|  |   | 2 | 2/5 × 100 | 40% |
|  |   | 3 | 3/5 × 100 | 60% |
|  |   | 4 | 4/5 × 100 | 80% |
|  |   | 5 | 在阈值 | 100% |
|  |   | 6 | 高于阈值 | 100% |

## 购买组完整性计算 {#buying-group-completeness-calculation}

购买群体完整性分数汇总各个角色完整性分数。 此计算提供跨所有已定义角色的购买组准备情况的整体视图。

### 购买组完整性公式

购买组完整性百分比使用以下公式计算：

```text
Buying Group Completeness % = Σ(Role Completeness %) / Number of defined roles
```

其中：

* `Role Completeness %` =单个角色完整性百分比(0-100%)
* `Σ` =购买组中所有角色的总和

<!--

## Use completeness scores in journeys

Use buying group completeness scores and role-level completeness scores to optimize your account journeys and personalize engagement strategies.

### Split paths by completeness

Use completeness thresholds in [journey split-path-by-account nodes](../journeys/split-merge-paths-nodes.md#account-path-filters) to route buying groups through different journey paths based on their readiness. For example:

* **High completeness path** (≥70%) - Buying groups that are nearly sales-ready can be routed to sales teams or receive call-to-action campaigns
* **Medium completeness path** (40-69%) - Buying groups in active development receive nurture campaigns focused on filling specific role gaps
* **Low completeness path** (<40%) - Newly formed buying groups receive awareness and education content to build initial engagement

### Trigger actions based on completeness milestones

Set up journey events that trigger specific actions when buying groups reach completeness milestones. FOr example:

* Alert sales teams when a buying group reaches 70% completeness.
* Send a _stakeholder alignment_ campaign when completeness increases by 20% or more within a defined timeframe.
* Trigger an automated assessment when a buying group stalls at the same completeness level for an extended period.

By leveraging completeness scores throughout the journey, you create more targeted, efficient campaigns that align with the actual composition and maturity of your buying groups.

-->