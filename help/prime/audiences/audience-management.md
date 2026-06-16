---
title: 受众管理
description: 受众的占位符页面。
autotag-review: '2026-06-12T22:47:10.727Z'
TQID: 'https://experienceleague.adobe.com/KWT9-Lr6358MQ0sLQyKAlb4SLERnBl-QQL7Cj1iXCZM'
product_v2: id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2: id: beb5f4be-cec3-471a-9db6-831a77dd3ac9id: aed878b8-11d0-487c-828b-d23b2051ec37
subfeature_v2: id: d270a788-eb1d-40ed-b74e-9158ed975b1f
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: c844cb4fb520f802c18a9988461c39106000b778
workflow-type: tm+mt
source-wordcount: 474
ht-degree: 3%

---

# 受众管理

在营销管理中心上，单击右侧导航栏中的&#x200B;**[!UICONTROL 人员列表]**。

![访问联系人列表以管理您的受众](./assets/people-lists.png){width="800" zoomable="yes"}

该页面有两个选项卡，您可以在其中查看和管理&#x200B;**[!UICONTROL 动态列表]**&#x200B;和&#x200B;**[!UICONTROL 静态列表]**。 单击选项卡，在每种类型之间切换列表视图。

从此页可以：

* 创建新的动态和静态列表
* 搜索现有列表
* 查看资源信息
* 访问列表以查看其成员资格

<!--
## Audience Hub

The AI Audience Hub is a centralized, AI-driven starting point for all audience-related capabilities across AJO B2B. It is designed to accelerate first-time user success while progressively unlocking advanced intelligence, insights, and control for returning and power users.

The Hub acts as:

* A guided starting point for discovering, creating, and refining person lists, account lists, and buying groups

* A visibility layer for audience health, coverage, overlap, engagement patterns, and AI-driven insights

* A control center for audience governance, optimization, reuse, and readiness for activation across journeys and sales workflows

### High level structure

Prompt-based starting point - Quick Start prompts and freeform input to help users discover, create, or optimize audiences.

1. AI insights feed - Surfaces key audience signals such as overlap, gaps, saturation risk, and optimization opportunities.

1. Adaptive audience library - A personalized view of people lists, account lists, and buying groups that adapts based on usage, relevance, and activation.

1. Optimization and arbitration nudges - Guides users to refine, split, or reuse audiences before activation.

1. Audience visibility and reporting - High-level insight into audience health, engagement patterns, and usage across active journeys.


### Empty and Error States (High-Level)

No audiences / no data - Show Quick Start prompts to help first-time users create or import person lists

Low data or incomplete audience - Explain what's missing (e.g., insufficient contacts, missing persona coverage, or low engagement data) and suggest next steps.

AI insights unavailable - Provide a graceful fallback with a clear explanation, so users understand why insights aren't shown and what actions they can take manually.
-->

## 创建人员列表


要创建动态或静态列表，请执行以下操作：

1. 单击&#x200B;_[!UICONTROL 人员列表]_&#x200B;页面右上角的&#x200B;**[!UICONTROL 创建列表]**。
1. 选择一个项目作为列表的&#x200B;**[!UICONTROL 父项]**。
1. 输入列表&#x200B;**[!UICONTROL Name]**&#x200B;和&#x200B;**[!UICONTROL Description]**（可选）。
1. 选择然后列出&#x200B;**[!UICONTROL 类型]**：

   * **[!UICONTROL 静态]** — 成员资格由您在创建列表时评估的合格筛选器决定。除非您手动使记录符合资格或取消符合资格，否则列表成员资格不会更新。
***[!UICONTROL 动态]** — 成员资格由符合条件的筛选器动态确定。列表成员资格将自动刷新。

1. 单击&#x200B;**[!UICONTROL 创建]**。

>[!NOTE]
>
>此Beta版本中的人员列表当前不支持删除和复制。

## 静态列表

静态列表成员资格由引用人员属性和活动的简单过滤器定义。 除非您手动授予成员资格或取消成员资格，否则成员资格不会更改。

>[!NOTE]
>
>在列表中添加或删除成员时，静态列表筛选器定义只应用一次。 定义的过滤器在之后不可用。 如果要使用过滤器维护一致的受众定义，请改用动态列表。

### 添加成员

1. 打开静态列表，然后单击右上方的&#x200B;**[!UICONTROL 添加人员]**。

1. 在对话框中，通过从左侧拖放过滤器来定义用于限定商机的规则。

   您可以使用以下任意组合来筛选人员：

   * 活动历史记录
   * 公司属性
   * 人员属性
   * 特殊过滤器，如历程成员资格

1. 要保存更改，请单击&#x200B;**[!UICONTROL 完成]**。

1. 选择&#x200B;**[!UICONTROL 成员]**&#x200B;选项卡。

   经过一段时间后，符合条件的成员会出现在列表中。

### 移除成员

1. 打开静态列表，然后单击右上方的&#x200B;**[!UICONTROL 删除人员]**。

1. 在对话框中，添加筛选器以匹配要取消资格的成员。

1. 要保存更改，请单击&#x200B;**[!UICONTROL 完成]**。

1. 选择&#x200B;**[!UICONTROL 成员]**&#x200B;选项卡。

   经过一段时间后，被取消资格的成员离开该列表。

## 动态列表

动态列表成员资格是使用引用人员属性和活动的简单过滤器定义的。 通过根据筛选逻辑鉴别和取消潜在客户资格来自动维护成员资格。

### 定义成员资格逻辑

1. 打开静态列表，然后选择“规则”选项卡。

1. 单击编辑规则。

1. 在对话框中，通过从左侧拖放过滤器来定义用于限定商机的规则。

   您可以使用以下任意组合来确定潜在客户是否符合列表的条件：

   * 活动历史记录
   * 公司属性
   * 人员属性
   * 特殊过滤器，如历程成员资格

1. 要保存更改，请单击&#x200B;**[!UICONTROL 完成]**。

1. 选择&#x200B;**[!UICONTROL 成员]**&#x200B;选项卡。

   经过一段时间后，符合条件的成员会出现在列表中。

要打开潜在客户配置文件详细信息页面，您可以在其中查看摘要和最近活动，请单击列表中的人员姓名。