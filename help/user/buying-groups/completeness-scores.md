---
title: Completeness Scores for Buying Groups
description: Calculate buying group completeness scores using role-based thresholds, customizable member requirements, and completeness settings in Journey Optimizer B2B Edition.
feature: Buying Groups
role: User
exl-id: 6f54d4ac-9d1a-4009-b9bf-8bc80e4cc63c
source-git-commit: b369ef39715f327fcff7237e827bebf4e82c27f6
workflow-type: tm+mt
source-wordcount: '895'
ht-degree: 9%

---

# 完整性评分 {#completeness-scores}

>[!CONTEXTUALHELP]
>id="ajo-b2b_buying_group_completeness_score"
>title="完整性评分"
>abstract="完整度评分反映销售就绪型购买群组的成员匹配程度。"

A completeness score is a percentage that indicates how well a buying group is populated with the required members across its defined roles. These scores are based on role member thresholds that you configure in the roles template and the actual number of members assigned to each role in the buying group. The resulting scores help marketers evaluate sales readiness and identify gaps in buying group composition. Score calculation occurs automatically as buying group membership changes.

![Buying group completeness scores](./assets/buying-group-details-page-completeness-scores.png){width="800" zoomable="yes"}

There are two types of completeness scores:

* **Buying group completeness score** - The buying group completeness score is a percentage between 0% to 100% and represents the overall completeness of the buying group based on role-level completeness calculations.

  The buying group completeness score is displayed in the [Buying group details](./buying-group-details.md) page. This score provides an at-a-glance view of whether the buying group has the required stakeholders in place for sales engagement.

* **Role completeness score** - The role completeness score is a percentage for each individual role within a buying group, based on the number of members assigned to that role.

  The role completeness score for each role is displayed in the buying group details page when you edit roles and adjust completeness settings. These scores help you identify which specific roles need additional members to reach the sales-ready threshold.

  The details page displays the first two role completeness scores with an n_+ link for any additional roles. Click the link to view the additional role completeness scores.

Completeness scores reflect the current state of buying group membership and update automatically as members are added or removed. Displayed scores are shown as whole percentages (for example, a score of 66.67% is displayed as 67%).

## Evaluate sales readiness

Adobe Journey Optimizer B2B Edition equips marketers with tools that ensure buying groups align with real decision-making processes. You can define complete buying groups using customizable role member thresholds that reflect your organization&#39;s sales methodology. By setting minimum and maximum member requirements for each role, you establish clear criteria for what constitutes a sales-ready buying group.

The buying group completeness score provides an accurate measure of sales readiness for the group. For example, to complete an opportunity for a specific solution, you might need at least two decision makers, one influencer, and at least one practitioner. The completeness score calculation accounts for each of these role-specific requirements, providing a view of overall buying group readiness.

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

## 角色完整度计算 {#role-completeness-calculation}

>[!CONTEXTUALHELP]
>id="ajo-b2b_buying_group_role_completeness_calculation"
>title="角色完整度计算"
>abstract="角色完整度评分基于分配到某一角色的成员数量，以百分比形式计算。"

Journey Optimizer B2B edition按百分比计算每个购买团体角色的完整性分数。 根据分配给角色的成员数量来计算此分数，而完成任务所需的角色模板](./buying-groups-role-templates.md#change-the-completeness-score-settings)数量为[。

角色完整性计算是介于零和指定阈值（需要成员）之间的线性百分比：

* 如果分配的成员数为&#x200B;**零**，则角色完整性为&#x200B;**0%**。
* 如果分配的成员数等于或大于阈值&#x200B;****，则角色完整性为&#x200B;**100%**。
* 如果分配的成员数介于&#x200B;**和阈值**&#x200B;之间，则将按比例计算完整性。

### 角色完整性公式

使用以下公式计算角色完整性百分比：

```text
Role Completeness % = ((Assigned Members - Threshold) / (Threshold)) × 100
```

其中：

* `Assigned Members` =角色中的当前成员数
* `Threshold` =在角色模板中设置成员必需值

### 角色完整性示例

以下示例说明了使用不同阈值配置的角色完整性计算：

| 角色 | 必需成员数 | 已分配的成员 | 计算 | 角色完整性 |
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
